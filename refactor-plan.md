# Joymew 互动体系重构方案

## 1. 当前架构快照

### 1.1 微信 H5 核心（`joymew-h5`）
- Vue2 单页应用通过 `src/router/index.js` 暴露签到、红包雨、游戏、酒店预定、充值等 60+ 页面，是未来要承载全部能力的主体 (joymew-h5.md:7700)。
- `src/store/modules/live.js` 与 `src/store/modules/app.js` 保存活动/用户/设备/场景等状态，包含红包口袋、座位表、送礼抽奖、婚礼堂专属配置等所有互动元素 (joymew-h5.md:4775, 7089)。
- 网络层 `src/utils/request.js` 与 `src/utils/requestMp.js` 直接从 URL 读取 `token` 并透传 `appid`，说明 H5 目前默认运行在小程序 WebView 里，由壳子负责注入凭证 (joymew-h5.md:2744, 2831)。
- `src/utils/service.js` 的 `getGameInfoByGameCode` 在小程序环境下仍大量返回 `enterType === 'mp'` 的页面跳转，暴露出哪些游戏尚未完成 H5 化 (joymew-h5.md:8243)。
- `src/utils/wxApi.js` 负责判断运行环境、调用 JSSDK 支付、在需要时通过 `wx.miniProgram.navigateTo` 跳回壳子 (joymew-h5.md:3307)。

### 1.2 小程序壳子

#### 互动主壳 (`joymew-mp`, 覆盖嗨猫/嗨喵/嗨喵跃动)
- `pages/joymewIndex/joymewIndex.js` 完成扫码/分享进入后的 liveId 解析、签到、强制手机号、身份选择等逻辑，并在完成后跳至 WebView (joymew-mp.md:43066, 36731)。
- `appGlobalData/splidInfo` 负责拼出 `spidInfo_liveH5Path = https://shm.hudongmiao.com/?liveId=...&token=...&mpType=...` 并缓存，用于 `pages/live/live.wxml` `<web-view>` 直接承载 H5 (joymew-mp.md:43066, 18381)。
- `pages/pay/pay.js` + `api/pay.js` 把所有充值/送礼/点歌/喵钻/霸屏等支付场景聚合在小程序侧，底层通过 `wx.requestPayment` 调起微信支付 (joymew-mp.md:36731, 32633)。
- 包结构：`packageA/B/C` 分别包含红包口袋、照片墙、投诉、协议、外链 WebView 等功能，其中协议/照片墙等已经纯 WebView 嵌入 H5 (joymew-mp.md:5642, 8020)；`packageGame` 仍有喊红包、红包墙、开宝箱等原生小游戏。

#### 婚礼堂壳 (`joymew-mp-hlt`)
- `app.json` 除主互动页外大量内嵌婚宴预定相关页面，这些页面实际也是 WebView，把 `liveId/token/isHlt/userPhone` 拼到 H5 URL 后加载酒店模块 (joymew-mp-hlt.md:23430)。
- `browseRecord`、`setIsHlt` 等逻辑保障婚礼堂分店、请柬定制等 BI 需求 (joymew-mp-hlt.md:37134)。

#### 同庆楼壳 (`joymew-mp-tql`)
- 页面与主壳接近，但裁剪掉部分包体，只保留核心签到、充值、红包墙、酒店预定等能力 (joymew-mp-tql.md:1200)。

#### 字节/抖音壳 (`joymew-mp-tt`)
- 页面仅包含入口、直播 WebView 以及婚宴预定，`pages/joymewIndex/joymewIndex.js` 在签到前需要检查/引导关注抖音号并在 `tt.navigateTo` 时跳往 `pages/live/live.ttml` WebView (joymew-mp-tt.md:477, 4487, 5622)。

### 1.3 关键耦合点
- **Token/Session**：H5 依赖壳子在 URL 中注入 `token/mpType/userPhone`，否则 `axios` 请求直接返回 401 (joymew-h5.md:2748, 2831)。
- **支付**：仅在小程序 `reqWxPay` 中实现，H5 通过 `wxApi.pay` 只是 JSSDK 封装但仍假设 WebView 注入的支付参数来自壳子 (joymew-mp.md:32633, joymew-h5.md:3309)。
- **小游戏**：`hmPlay2/3/4/5/15/16/30/31` 等编码仍走小程序页面 (joymew-h5.md:8243-8438)。
- **多壳差异**：婚礼堂/同庆楼需要 `isHlt` 标识、抖音壳需要 `followAwemeState` 等扩展字段，当前由各壳子的 `storage` 或 `globalData` 管 (joymew-mp-hlt.md:23430, joymew-mp-tt.md:4487)。

## 2. 主要痛点
1. **H5 入口不可独立**：没有小程序注入的 token，H5 无法初始化 store 与接口；同样 `wxApi.judgeEnv` 默认存在微信/抖音容器 (joymew-h5.md:3307)。
2. **支付与钱包深度绑定壳子**：所有支付场景集中在 `pages/pay/pay.js`，H5 无法直接调起，导致红包口袋、嘉年华等能力必须回到壳里 (joymew-mp.md:36731)。
3. **小游戏与 WebView 互跳复杂**：`getGameInfoByGameCode` 要根据环境拼接 `mp` 路径并通过 `wx.miniProgram.navigateTo` 跳转，且部分游戏需要频繁刷 token (joymew-h5.md:8243)。
4. **多壳配置分散**：`setIsHlt`、`setOrigin`、`followAwemeState` 等在不同项目重复实现，H5 难以识别具体入口差异 (joymew-mp-hlt.md:37134, joymew-mp-tt.md:4487)。
5. **调试/审核模式混杂**：`appGlobalData/splidInfo` 内置 `useDevPageHost`、`LIVEID` 等逻辑，H5 也有 `EXAMINELIVID` 常量，后续维护困难 (joymew-mp.md:43066, joymew-h5.md:4775)。

## 3. 目标蓝图（纯微信 H5 + 极简壳）
1. **H5 自主登录**：H5 能通过公众号网页授权 / 手机号验证码 / 扫码参数获取 token，并在本地加密存储，无需依赖小程序注入。
2. **支付中台化**：在 H5 内封装统一支付 SDK（微信 JSAPI + 抖音 JSAPI），壳子只负责无法绕过的支付调起页面，实现“无头 Pay 页”。
3. **业务模块完全 H5 化**：所有互动游戏、红包口袋、充值、投诉、酒店预定等均在 H5 内实现，壳子仅提供入口页 + Pay + 登录授权。
4. **入口壳子抽象**：四个小程序统一成“入口 SDK”，只负责扫码解析、权限申请、open-id/token 下发、WebView 跳转、Pay 调起与极少数原生能力。
5. **多端兼容层**：H5 通过 `env bridge` 识别当前渠道（壳子 / 微信浏览器 / 抖音 / 纯 H5）并选择合适的登录与支付策略。
6. **可配置的功能矩阵**：以活动/门店为维度配置“所需功能列表”，H5 根据配置决定哪些模块展示、哪些走外链。
7. **双容器蓝绿发布**：生产新增独立容器/域名承载“新 H5”，旧域名继续服务存量活动，小程序壳子可按 liveId 或渠道把 WebView 指向不同地址，实现“掏空”的同时具备即刻回滚能力。

## 4. 迁移路线（建议 5 个阶段）

### 阶段 0：盘点与能力矩阵
- 输出「功能 × 渠道 × 依赖」矩阵，确认哪些依赖 `wx.openChannels`、蓝牙、录音等必须保留壳内（例如喊红包需要原生录音，见 `packageGame/pages/shoutHb/modules/game`，joymew-mp.md:43146）。
- 将 `joymew-mp`、`joymew-mp-hlt`、`joymew-mp-tql`、`joymew-mp-tt` 的差异配置抽象成 JSON（如 `isHlt`、`followAwemeState`、`miniProgramType`），并预留在 H5 `store.app` 中 (joymew-h5.md:7089)。
- 明确“新旧 H5 容器”资源：与运维确定新域名（例如 `https://new.shm.hudongmiao.com`）、证书、跨域策略及日志归集方式，保证旧容器 (`https://shm.hudongmiao.com`) 持续稳定运行，可与新容器并行多年。

### 阶段 1：身份认证改造
1. **统一 token 服务**：在后端提供 `code -> token`（公众号/小程序）、`liveId -> token`（扫码）接口；H5 `request.js` 改为读取本地存储而非 URL，同步更新 `store.app.token` 生命周期 (joymew-h5.md:2744)。
2. **入口协议**：壳子只负责把 `liveId`、`channel`、`device` 注入 WebView，H5 根据渠道自行走授权。`appGlobalData/splidInfo` 仍生成旧 URL 以兼容过渡，但逐步切换为新协议 (joymew-mp.md:43066)。
3. **开放环境检测**：增强 `wxApi.judgeEnv`，支持「公众号网页」和「纯浏览器」分支，必要时提示“请在微信中打开” (joymew-h5.md:3307)。
4. **双栈联调**：在新容器上部署裁剪后的 H5 版本，小程序壳子通过 liveId 白名单切换 WebView URL，验证 token 注入、登录链路在新/旧容器之间互不影响，并记录切流指标。

### 阶段 2：支付与钱包
1. **支付参数服务**：把 `pages/pay/pay.js` 的 `originPay` 场景拆成后端 API（返回支付参数 + 成功后需要触发的业务），H5 直接调用；壳子仅保留支付兜底页 (joymew-mp.md:36731)。
2. **H5 支付 SDK**：封装 `WxPayService` / `DouyinPayService`，统一调用 `wx.chooseWXPay` 或抖音 JSSDK（参考 `wxApi.pay`，joymew-h5.md:3309）；构建失败重试、取消回调等机制。
3. **钱包/红包口袋迁移**：将 `packageA/pages/hbkdRecharge` 的 UI/逻辑迁入 H5 `views/hbkdRecharge`，并复用新支付服务 (joymew-mp.md:32370)。
4. **验证**：对照原 `reqDiamondRecharge`、`reqSendGiftGameRecharge` 等接口，补齐 H5 调用链 (joymew-mp.md:32633)。
5. **蓝绿切流**：支付链路打通后，先让单个渠道/活动在小程序中指向新 H5 容器，持续监控支付成功率与退款率，确认稳定再扩大范围，旧容器保持热备随时可回切。

### 阶段 3：小游戏与模块迁移
1. **WebGL/Canvas 游戏评估**：针对 `hmPlay2/3/4/5/15/16/30/31` 等仍走小程序的游戏，评估是否有现成 H5 版本或需要重写；若技术上仍需原生（如实时录音的喊红包），则通过壳子保留极少数原生页，其余全部 H5 化 (joymew-h5.md:8243)。
2. **功能拆迁顺序**：按照业务影响逐个迁移，例如：
   - 红包墙/开宝箱：与支付联动紧密，优先迁移。
   - 猜红包/争分夺秒：依赖 WebSocket +支付，作为下一批。
   - 喊红包：若短期内难以脱离录音组件，可作为长期保留模块。
3. **婚礼堂/酒店预定**：将 `pages/hotelReserve/*` WebView 页直接替换为 H5 内路由，并让壳子仅保留入口卡片 (joymew-mp-hlt.md:23430)。
4. **抖音壳特性**：把 `followAwemeState`、`tt.navigateTo` 相关逻辑迁入 H5 某个“渠道插件”，壳子只传入 `dy_appid/dy_bind_id` (joymew-mp-tt.md:4487)。

### 阶段 4: 壳子瘦身与统一
1. **新壳脚手架**：封装统一的 `entry-shell-sdk`（Taro/原生均可），仅含：扫码参数解析、登录授权、WebView 承载、支付兜底、少量原生组件（录音、摄像）。
2. **配置驱动**：壳子拉取远端配置决定显示哪些入口按钮（签到、婚礼堂专区等），H5 根据 `channel` 渲染对应 UI。
3. **旧逻辑退场**：删除 `packageC` 中指向 H5 的重复页面（协议、照片墙、外链等）以及多余的 `wx:if` 判断，减少包体。

### 阶段 5：发布与监控
- **灰度**：按活动类型/渠道逐步切流，确保 H5 自主登录与支付链路稳定。
- **埋点/告警**：在 H5 增加登录/支付/游戏等核心指标监控，并在壳子保留最低限度的可观测性（如 `browseRecord` 的进入/离开事件, joymew-mp-hlt.md:23430）。
- **开发者体验**：简化本地启动流程，允许独立运行 H5（本地 mock token），并提供统一的壳子模拟器。

#### 模块迁移优先级示例

| 模块 | 当前承载 | 迁移策略 | 依赖/备注 |
| --- | --- | --- | --- |
| 签到入口 | `pages/joymewIndex/joymewIndex` (joymew-mp.md:43066) | H5 实现扫码进入页，壳子仅做授权 & 跳转 | 需保留 `sceneType/identitySwitch` 配置 |
| 支付/充值 | `pages/pay/pay.js` + `api/pay.js` (joymew-mp.md:36731, 32633) | H5 支付 SDK，壳子提供 Pay fallback | 高风险，需与财务对齐 |
| 红包口袋 | `packageA/pages/hbkdRecharge` (joymew-mp.md:32370) | 迁入 `views/hbkdRecharge` 并复用新支付 | UI 已有 H5 版本，可复用 |
| 现场照片/协议等 WebView | `packageC/*` (joymew-mp.md:5642, 8020) | 直接从壳子移除，统一入口在 H5 | 低风险 |
| 婚宴预定 | `pages/hotelReserve/*` (joymew-mp-hlt.md:23430) | H5 模块 + 渠道参数 | 需保留 `isHlt` |
| 抖音关注引导 | `joymew-mp-tt` (joymew-mp-tt.md:4487) | H5 渠道插件，调用抖音 JS-SDK | 与字节侧联调 |
| 小游戏 `hmPlay2/5/15/16/30/31` | `getGameInfoByGameCode` (joymew-h5.md:8243) | 逐个重写或保留小程序页 | 涉及资产与特效 |

## 5. 风险与对策
1. **支付合规风险**：H5 发起的 JSAPI 需要公众号资质，并区分服务号/小程序；需确认业务主体与支付商户一致。可在小程序壳保留支付兜底，确保审核通过前不放量。
2. **录音/传感器能力缺失**：如喊红包依赖原生录音 (joymew-mp.md:43146)，需评估是否用 WebRTC + 公众号接口替代，或暂时保留原生模块。
3. **多渠道差异**：婚礼堂/同庆楼/抖音存在不同的 CRM、埋点需求，迁移时要抽象配置并确保历史数据连续。
4. **历史活动兼容**：部分老活动依赖 `mpType` 区分皮肤，H5 需要支持旧参数，确保不会影响尚未迁移的壳子。
5. **包体与审核**：瘦身过程中要确保壳子通过小程序审核（保留必要的隐私合规组件，如 `privacyAuthorize`，joymew-mp.md:18370）。
6. **双容器一致性**：新旧 H5 容器需在配置、静态资源、监控上保持同步，避免出现“同一活动在不同域名体验不一致”或缓存错乱；必要时引入版本号对齐和文件指纹校验。

## 6. 验证与交付标准
1. **功能验收清单**：登录、签到、送礼/充值、红包口袋、酒店预定、小游戏、投诉/协议、婚礼堂专区、抖音关注等全部可在纯 H5 环境完成。
2. **回归用例**：对照 `getGameInfoByGameCode` 枚举的所有 gameCode 做全量回归，确保 `enterType` 均为 `h5/popup/thirdParty`，只有保留的极少数仍为 `mp` (joymew-h5.md:8243)。
3. **自动化验证**：新增冒烟脚本，模拟不同渠道的 URL 参数组合，验证 token 注入、支付调起、WebSocket 连接等关键路径。
4. **壳子回退策略**：在小程序中保留 `useLegacyH5` 开关，一旦 H5 新逻辑异常，可快速切换到旧模式；开关指向旧容器 URL，以蓝绿方式秒级回滚。

> 以上计划遵循「逐模块迁移、壳子退化为入口+支付」的宏观思路，便于在保证业务连续性的前提下逐步实现纯 H5 化。后续可根据业务优先级对阶段任务做更细的排期与资源分配。111
