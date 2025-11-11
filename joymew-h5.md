This file is a merged representation of a subset of the codebase, containing specifically included files, combined into a single document by Repomix.

# File Summary

## Purpose
This file contains a packed representation of a subset of the repository's contents that is considered the most important context.
It is designed to be easily consumable by AI systems for analysis, code review,
or other automated processes.

## File Format
The content is organized as follows:
1. This summary section
2. Repository information
3. Directory structure
4. Repository files (if enabled)
5. Multiple file entries, each consisting of:
  a. A header with the file path (## File: path/to/file)
  b. The full contents of the file in a code block

## Usage Guidelines
- This file should be treated as read-only. Any changes should be made to the
  original repository files, not this packed version.
- When processing this file, use the file path to distinguish
  between different files in the repository.
- Be aware that this file may contain sensitive information. Handle it with
  the same level of security as you would the original repository.

## Notes
- Some files may have been excluded based on .gitignore rules and Repomix's configuration
- Binary files are not included in this packed representation. Please refer to the Repository Structure section for a complete list of file paths, including binary files
- Only files matching these patterns are included: src/api, src/assets/constant, src/assets/styles@/src/components, src/router, src/store, src/utils, src/App.vue, src/main.js, package.json, vue.config.js
- Files matching patterns in .gitignore are excluded
- Files matching default ignore patterns are excluded
- Files are sorted by Git change count (files with more changes are at the bottom)

# Directory Structure
```
package.json
src/api/api-game.js
src/api/chat/index.js
src/api/clickTiger/index.js
src/api/comment/index.js
src/api/countMoney/index.js
src/api/diamondHb/index.js
src/api/duiduipeng/index.js
src/api/giveMark/giveMark.js
src/api/guessHb/index.js
src/api/happyQA.js
src/api/hby/allHby.js
src/api/hby/index.js
src/api/hotelReserve/hlt.js
src/api/hotelReserve/index.js
src/api/index/index.js
src/api/kbx/index.js
src/api/majiang/majiang.js
src/api/nyn/index.js
src/api/photoWall/photoWall.js
src/api/pigOut/index.js
src/api/playFootball/index.js
src/api/shake/index.js
src/api/vote/brideVote.js
src/api/vote/vote.js
src/api/zyz/index.js
src/App.vue
src/assets/constant/audio.js
src/assets/constant/effect.js
src/assets/constant/host.js
src/assets/constant/index.js
src/assets/constant/others.js
src/assets/constant/scene.js
src/main.js
src/router/index.js
src/store/index.js
src/store/modules/app.js
src/store/modules/chat/index.js
src/store/modules/chat/utils/cardChat.js
src/store/modules/chat/utils/func.js
src/store/modules/chat/utils/index.js
src/store/modules/game.js
src/store/modules/live.js
src/store/modules/user.js
src/utils/hdOptimizationTmpPatch.js
src/utils/index.js
src/utils/loadFile.js
src/utils/preloadFile.js
src/utils/request.js
src/utils/requestGuessHbPay.js
src/utils/requestMp.js
src/utils/requestUpload.js
src/utils/requestWWW.js
src/utils/service.js
src/utils/tools.js
src/utils/ttjssdk.js
src/utils/websocket/handleMessage.js
src/utils/websocket/index.js
src/utils/wxApi.js
vue.config.js
```

# Files

## File: package.json
```json
{
  "name": "joymew-h5",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "vue-cli-service serve",
    "build:prod": "vue-cli-service build",
    "build:stage": "vue-cli-service build --mode staging",
    "build:stageonline": "vue-cli-service build --mode stageonline",
    "lint": "vue-cli-service lint"
  },
  "dependencies": {
    "axios": "^0.18.1",
    "core-js": "^3.6.5",
    "createjs-cmd": "^0.1.0",
    "lottie-web": "^5.12.2",
    "phaser": "^3.87.0",
    "phaser-ce": "^2.8.0",
    "qs": "^6.9.4",
    "svgaplayerweb": "^2.3.0",
    "v-tap": "^3.0.3",
    "vant": "^2.12.48",
    "video-animation-player": "^1.0.5",
    "vue": "^2.6.11",
    "vue-concise-slider": "^2.4.9",
    "vue-cropper": "^0.4.9",
    "vue-pickers": "^2.5.3",
    "vue-router": "^3.2.0",
    "vue-swipe": "^2.4.0",
    "vue-wechat-title": "^2.0.7",
    "vue2-toast": "^2.0.2",
    "vuescroll": "^4.12.0",
    "vuex": "^3.4.0",
    "websocket-heartbeat-js": "^1.0.12",
    "weixin-js-sdk": "^1.6.0"
  },
  "devDependencies": {
    "@vue/cli-plugin-babel": "~4.5.0",
    "@vue/cli-plugin-eslint": "~4.5.0",
    "@vue/cli-plugin-router": "~4.5.0",
    "@vue/cli-plugin-vuex": "~4.5.0",
    "@vue/cli-service": "~4.5.0",
    "@vue/eslint-config-airbnb": "^5.0.2",
    "babel-eslint": "^10.1.0",
    "babel-plugin-import": "^1.13.3",
    "compression-webpack-plugin": "^6.1.1",
    "cssnano-preset-advanced": "^4.0.7",
    "eslint": "^6.7.2",
    "eslint-plugin-import": "^2.20.2",
    "eslint-plugin-vue": "^6.2.2",
    "expose-loader": "^0.7.3",
    "less": "^3.0.4",
    "less-loader": "^5.0.0",
    "postcss-aspect-ratio-mini": "^0.0.2",
    "postcss-cssnext": "^3.1.0",
    "postcss-exclude-files": "^1.0.15",
    "postcss-import": "^12.0.1",
    "postcss-px-to-viewport": "^1.1.0",
    "postcss-url": "^8.0.0",
    "postcss-write-svg": "^3.0.1",
    "prettier": "3.0.2",
    "vue-template-compiler": "^2.6.11"
  }
}
```

## File: src/api/api-game.js
```javascript
// 游戏通用接口
import store from '@/store/index';
import request from '@/utils/request';

/**
 * 提交分数通用接口，后端接收到分数后，会和已有的分数进行比较，如果比已有的分数高，则更新分数
 * @param {number} score 分数
 */
export const submitScore = (score) => {
  return request.post('play/shangfen16', {
    splid: store.state.live.liveId,
    fenshu: score,
    userId: store.state.user.userId,
  });
};

/**
 * 获取大屏的传过来的通信数据
 */
export const reqDataFromScreen = () => {
  return request.post('sendMsgController/h5GetInfo', {
    splid: store.state.live.liveId,
  });
};
```

## File: src/api/chat/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 文本内容验证
export function securityMsgCheck(ct) {
  return request.post('subscribeController/msg_sec_check', {
    content: ct,
  });
}

// 发送聊天消息
export function sendChatMessage(message, color) {
  return request.post('sendMsgController/msgGo6', {
    content: message,
    color,
    splid: store.state.live.liveId,
  });
}

// 获取聊天记录
export function getChatMessage() {
  return request.get(
    `wxScan/getMsgInfo?splid=${store.state.live.liveId}&num=1&size=30`,
  );
}

// 发礼物的广播
export function sendGiftMessage({
  miaoColor = '',
  sendType = '',
  giftId = store.state.app.currentGiftType,
}) {
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: giftId,
    content: '',
    miaoColor,
    send_type: sendType,
  });
}

// 发推荐礼物的广播
export function sendRecommendGiftMessage({ giftId, content = '' }) {
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: giftId,
    content,
  });
}

// 发送照片礼物的广播
export function sendPhotoGiftMessage({
  giftId = store.state.app.currentPhotoType,
  content,
  imgUrl,
  sendType = '',
}) {
  const choosedPhotoType = store.state.live.photoTypeList.find(
    (item) => item.giftId === giftId,
  );
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: giftId,
    content,
    tpUrl: imgUrl,
    times: choosedPhotoType.time,
    send_type: sendType,
  });
}

// 发送照片墙礼物的广播
export function sendPhotoWallGiftMessage(imgUrl) {
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: 'Miao_PhotoWall',
    content: '爱心照片墙',
    tpUrl: imgUrl,
    times: 10,
  });
}

// 发送霸气弹幕礼物广播
export function sendDanmuGiftMessage({
  giftId = store.state.app.currentDanmuType,
  content,
  sendType = '',
}) {
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: giftId,
    content,
    send_type: sendType,
  });
}

// 发送超级弹幕礼物广播
export function sendSuperDanmuGiftMessage({
  content,
  giftId = store.state.app.currentSuperDanmuType,
  sendType = '',
}) {
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: giftId,
    content,
    send_type: sendType,
  });
}

// 发送霸屏礼物广播
export function sendBapinGiftMessage({
  content,
  sendType = '',
  giftId = store.state.app.currentBapinType,
}) {
  return request.post('sendMsgController/liwuGo6', {
    splid: store.state.live.liveId,
    liwuId: giftId,
    content,
    send_type: sendType,
  });
}

// 发送广播
export function sendBroasCast(paramObj) {
  return request.post('sendMsgController/duxin6', {
    ykq_info: paramObj.c,
    splid: store.state.live.liveId,
  });
}
```

## File: src/api/clickTiger/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 提交分数
export default function submitScore(score) {
  return request.post('play/shangfen16', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay18',
    fenshu: score,
    userId: store.state.user.userId,
  });
}
```

## File: src/api/comment/index.js
```javascript
import { getUrlParam } from '@/utils/index';
import requestWWW from '../../utils/requestWWW';
import store from '../../store/index';

// 获取我的评价及主持人信息
export const getHostInfo = () => {
  return requestWWW.post('/splidComment/getMyComment', {
    splid: store.state.live.liveId,
    token: getUrlParam('token'),
  });
};
// 进行评价
export const commitComment = (pObj) => {
  return requestWWW.post('/splidComment/saveUserComment', {
    splid: store.state.live.liveId,
    content: pObj.content,
    type: '3',
    label: pObj.label,
    satisfaction: pObj.satisfaction,
  });
};
// 获取评价汇总信息
export const getHostCommentBase = () => {
  return requestWWW.post('/splidComment/getUserComment', {
    splid: store.state.live.liveId,
  });
};
// 获取所欲评价用户评价列表
export const getHostCommentList = (pObj) => {
  return requestWWW.post('/splidComment/getCommentList', {
    splid: store.state.live.liveId,
    type: '3',
    currentPage: pObj.currentPage,
    showCount: pObj.showCount,
  });
};
// 打赏主持
export const Reward = (pObj) => {
  return requestWWW.post('/splidComment/getCommentList', {
    splid: store.state.live.liveId,
    totalfee: pObj.totalfee,
  });
};
// 回复
export const replyUser = (pObj) => {
  return requestWWW.post('/splidComment/getCommentList', {
    splid: store.state.live.liveId,
    type: '5',
    album_comment_id: pObj.album_comment_id,
    content: pObj.content,
  });
};

// 获取验证码
export const getValidateCode = (pObj) => {
  return requestWWW.post('/dengLuHm/faSongCode', {
    phonenumber: pObj.phone,
    source: '6',
  });
};

// 验证手机号
export const checkPhone = (pObj) => {
  return requestWWW.post('/dengLuHm/checkPhone', {
    phonenumber: pObj.phone,
    code: pObj.code,
    token: pObj.token,
    id: pObj.id,
  });
};
```

## File: src/api/countMoney/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 数钞票提交分数
export default function submitScore(score) {
  return request.post('play/shangfen16', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay7',
    fenshu: score,
    userId: store.state.user.userId,
  });
}
```

## File: src/api/diamondHb/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 发送喵钻红包
export function sendDiamondHb(pObj) {
  return request.post('redPackage/sendRedPackage', {
    splid: store.state.live.liveId,
    total: pObj.total,
    size: pObj.size,
    type: pObj.type,
  });
}

// 抢喵钻红包
export function robDiamondHb(packageId) {
  return request.post('redPackage/robRedPackage', {
    splid: store.state.live.liveId,
    package_id: packageId,
  });
}

// 获取喵钻红包列表
export function getDiamondHbList() {
  return request.post('redPackage/getRedPackageList', {
    splid: store.state.live.liveId,
  });
}

// 根据id获取某个喵钻红包列表
export function getDiamondHbRankById(packageId) {
  return request.post('redPackage/getRedPackageInfo', {
    package_id: packageId,
  });
}
```

## File: src/api/duiduipeng/index.js
```javascript
import store from '../../store/index';
import request from '../../utils/request';

//  获取用户信息
export function getUserInfo() {
  return request.post('/pair/getPairUserInfo', {
    splid: store.state.live.liveId,
  });
}

//  保存信息
export function saveUserInfo(params) {
  return request.post('/pair/savePairUserInfo', {
    splid: store.state.live.liveId,
    sex: params.sex,
    wx_name: params.wx_name,
    avator: params.avator,
    age_type: params.age,
  });
}

//  获取历史匹配结果
export function getRecordResult() {
  return request.post('/pair/getMyPairResult', {
    splid: store.state.live.liveId,
  });
}
```

## File: src/api/giveMark/giveMark.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 获取当前人员信息
export function getCurrentMarkUserInfo() {
  return request.post('vote/getPlayerInfo', {
    splid: store.state.live.liveId,
  });
}

// 评分
export function sendMark(paramObj) {
  return request.post('vote/savePlayerScore', {
    splid: store.state.live.liveId,
    order_by: paramObj.orderBy,
    target_id: paramObj.markUserId,
    score: paramObj.score,
  });
}
```

## File: src/api/guessHb/index.js
```javascript
import requestGuessHbPay from '../../utils/requestGuessHbPay';
import requestMp from '../../utils/requestMp';
import { getUrlParam } from '../../utils/index';
import store from '../../store/index';

// 猜红包支付
export function payGuessHb(pObj) {
  return requestGuessHbPay.post('kpPay/chbWxPay_h5', {
    splid: getUrlParam('splid'),
    shen_fen: pObj.identity,
    money: pObj.money,
    pay_type: 'wx',
    token: getUrlParam('token'),
  });
}

// 获取appId
export function getAppId() {
  return requestGuessHbPay.post('dengLuHm/qianMing', {
    url: window.location.href.split('#')[0],
  });
}

// 获取充值状态
export function getPayStatus() {
  return requestGuessHbPay.post('hb/getPhotoUserInfo', {
    splid: getUrlParam('splid'),
    token: getUrlParam('token'),
  });
}

// 获取猜红包状态
export function getGuessInfo() {
  return requestMp.post('guessRedPackage/getGuessInfo', {
    splid: store.state.live.liveId,
  });
}

// 参与猜红包
export function attendGuess(pObj) {
  return requestMp.post('guessRedPackage/robRedPackage', {
    splid: store.state.live.liveId,
    sort: pObj.sort,
    rob_sort: pObj.robSort,
    guess_money: pObj.guessMoney,
    red_package_id: pObj.hbId,
  });
}

// 猜红包充值
export function guessHbRecharge(paramObj) {
  return requestMp.post('hmWxmoney/chongzhiKbx', {
    splid: store.state.live.liveId,
    giftId: 'guess',
    total: paramObj.money,
    userId: store.state.user.userId,
    openid: store.state.user.openId,
  });
}
```

## File: src/api/happyQA.js
```javascript
import request from '../utils/request';
import store from '../store/index';

// 获取答题基本信息
export const getHappyData = () => {
  return request.post('happy/getHappyData', {
    splid: store.state.live.liveId,
  });
};

/**
 * 提交答题结果
 * @param {object}
 * @example
 * 参数：
 * {
 *  submitSort: 1, // 第1题
 *  answers: 'A', // 选择A
 *  isCorrect: 1 // 正确
 * }
 */
export const submitAnswer = ({ submitSort, answers, isCorrect }) => {
  return request.post('happy/submitAnswers', {
    splid: store.state.live.liveId,
    submit_sort: submitSort.toString(),
    answers,
    isCorrect,
  });
};

// 获取排行榜
export const getHappyRank = () => {
  return request.post('happy/getHappyRank', {
    splid: store.state.live.liveId,
  });
};
```

## File: src/api/hby/allHby.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 初始化全场红包雨游戏
export function initAllHby() {
  return request.get(`allHby/initAllHby?splid=${store.state.live.liveId}`);
}

// 全场红包雨上传分数
export function uploadAllHbyScore(size) {
  return request.get(
    `allHby/robAllHby?size=${size}&splid=${store.state.live.liveId}&hbId=${store.state.game.hbId}`,
  );
}
```

## File: src/api/hby/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 开始红包雨game
export function startHby() {
  return request.get(`play/initHby6?userId=${store.state.user.userId}&spoId=${store.state.live.liveId}&playInfo=hmPlay1`);
}
// 抢红包
export function robHb(score) {
  return request.post('play/bietiansheng6', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay1',
    score,
    userId: store.state.user.userId,
    hbId: store.state.game.hbId,
  });
}
export function getHbyRank() {
  return request.get(`play/redBaoRank6?splid=${store.state.live.liveId}&userId=${store.state.user.userId}`);
}

// 开始点红包game
export function startClickHb() {
  return request.get(`play/initHby6?userId=${store.state.user.userId}&spoId=${store.state.live.liveId}&playInfo=hmPlay11`);
}
// 点红包
export function robClickHb(score) {
  return request.post('play/bietiansheng6', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay11',
    score,
    userId: store.state.user.userId,
    hbId: store.state.game.hbId,
  });
}
```

## File: src/api/hotelReserve/hlt.js
```javascript
import { getUrlParam } from '@/utils/index';
import requestWWW from '@/utils/requestWWW';
import store from '../../store/index';

// 获取抽奖数据
export function getChouJiangData() {
  return requestWWW.post('/activity/getActivityData', {
    splid: store.state.live.liveId,
    token: getUrlParam('token'),
  });
}

// 抽奖
export function chouJiang() {
  return requestWWW.post('/weddingConpon/lottery', {
    activity_id: store.state.live.activityId,
    splid: store.state.live.liveId,
    token: getUrlParam('token'),
  });
}

// 获取我的优惠信息
export function getMyPreferentialData({ showCount, currentPage }) {
  return requestWWW.post('/weddingConpon/getMyCouponList', {
    activity_id: store.state.live.activityId,
    query_type: '1',
    token: getUrlParam('token'),
    currentPage,
    showCount,
  });
}
```

## File: src/api/kbx/index.js
```javascript
import requestMp from '../../utils/requestMp';
import store from '../../store/index';

// 开宝箱充值
export function kbxRecharge(paramObj) {
  return requestMp.post('hmWxmoney/chongzhiKbx', {
    userId: store.state.user.userId,
    splid: store.state.live.liveId,
    openid: store.state.user.openId,
    giftId: 'kbx',
    total: paramObj.money,
  });
}

// 抢宝箱
export function robBox(paramObj) {
  return requestMp.post('kakaluote/guipaiqigong6', {
    order_by: paramObj.sort,
    boxIdList: paramObj.boxIds,
    splid: store.state.live.liveId,
  });
}

// 获取宝箱列表
export function getBoxesList() {
  return requestMp.get(`kakaluote/chaojisaiyaren6?splid=${store.state.live.liveId}`);
}

// 获取game状态
export function getGameState() {
  return requestMp.get(`play/baiyan6?splid=${store.state.live.liveId}&userId=${store.state.user.userId}`);
}

// 获取我的宝箱
export function getMyBoxes() {
  return requestMp.get(`kakaluote/jianlai6?splid=${store.state.live.liveId}`);
}

// 获取红包列表
export function getHbList() {
  return requestMp.get(`hbqController/showHbqList6?splid=${store.state.live.liveId}`);
}

// 买红包
export function buyHb(paramObj) {
  return requestMp.post('hbqController/hbqPay6', {
    order_by: paramObj.sort,
    eggIdList: paramObj.hbIds,
    splid: store.state.live.liveId,
  });
}

// 红包墙充值
export function hbqRecharge(paramObj) {
  return requestMp.post('hmWxmoney/chongzhiKbx', {
    userId: store.state.user.userId,
    splid: store.state.live.liveId,
    openid: store.state.user.openId,
    giftId: 'hbq',
    total: paramObj.money,
  });
}

// 获取红包排行榜
export function getHbRankList() {
  return requestMp.get(`hbqController/hbqRankList6?splid=${store.state.live.liveId}`);
}
```

## File: src/api/majiang/majiang.js
```javascript
// 雀神大赛接口
import store from '@/store/index';
import request from '@/utils/request';

/** 获取等待界面的麻将题目 */
export const getWaitQs = () => {
  return request.get(`newPlay/getExampleMjTopic?splid=${store.state.live.liveId}`);
};

/** 获取本局游戏的所有题目 */
export const getAllQs = () => {
  return request.get(`newPlay/getMjTopic?splid=${store.state.live.liveId}`);
};

/** 记录答题时间
 * @param {string} answerTime 答题所用的时间
 * @param {string} answerTopic 回答的题目的轮次
 */
export const recordReplyTime = (answerTime, answerTopic) => {
  return request.post('newPlay/recordMj', {
    splid: store.state.live.liveId,
    answerTime,
    answerTopic,
  });
};

/** 获取用户排行榜数据 */
export const getRankList = () => {
  return request.post('newPlay/userRank', {
    splid: store.state.live.liveId,
  });
};

/** 中途加入获取当前轮次及当前轮次剩余的时间 */
export const getCurrentRoundInfo = () => {
  return request.post('newPlay/mjEnterGame', {
    splid: store.state.live.liveId,
  });
};
```

## File: src/api/nyn/index.js
```javascript
import request from '../../utils/request';
import requestMp from '../../utils/requestMp';
import store from '../../store/index';

// 获取奖池金额
export function getPoolMoney() {
  return request.get(`jianLai/luckyDbList6?splid=${store.state.live.liveId}`);
}

// 获取扭一扭相关信息
export function getNynInfo() {
  return request.get(
    `jianLai/getLuckyId6?splid=${store.state.live.liveId}&playInfo=hdGame88`,
  );
}

// 获取扭一扭排行榜列表
export function getNynRank() {
  return request.get(`jianLai/luckyDbRank6?splid=${store.state.live.liveId}`);
}

// 扭一扭充值
export function nynRecharge() {
  return requestMp.post('hmWxmoney/chongzhiNyn', {
    USER_ID: store.state.user.userId,
    splid: store.state.live.liveId,
    openid: store.state.user.openId,
    giftId: 'one',
  });
}

// 扭一扭开始game
export function startNyn(paramObj) {
  return request.post('jianLai/niuyiniu6', {
    splid: store.state.live.liveId,
    playInfo: 'hdGame88',
    id: paramObj.turnId,
  });
}

// 扭一扭发送中奖信息
export function sendPrizeInfo(paramObj) {
  return request.post('jianLai/luoXuanWan6', {
    type: '2',
    gold: paramObj.gold,
    balance: paramObj.remainCoin,
    splid: store.state.live.liveId,
    id: paramObj.turnId,
  });
}
```

## File: src/api/photoWall/photoWall.js
```javascript
import request from '../../utils/request';
import requestWWW from '../../utils/requestWWW';
import store from '../../store/index';

// 获取照片墙列表
export function getPhotoWallList() {
  return request.post('hmGiftController/heartWallList', {
    splid: store.state.live.liveId,
    type: 'xin',
    is_delete: '0',
  });
}

// 发送照片墙
export function sendPhoto(pObj) {
  return request.post('hmGiftController/sendHeartWall', {
    splid: store.state.live.liveId,
    photo_start_url: pObj.imgPathOrigin,
    photo_end_url: pObj.imgPath,
    type: 'xin',
    sort: pObj.id,
  });
}

// 删除照片墙
export function deletePhoto(pObj) {
  return request.post('hmGiftController/editHeartWall', {
    splid: store.state.live.liveId,
    is_delete: '1',
    heart_wall_id: pObj.id,
  });
}

// 获取摄影师照片墙列表
export function getLivePhotoInfo() {
  return requestWWW.post('photo/getPhotoShiList', {
    splid: store.state.live.liveId,
    source: '1',
    token: store.state.app.token,
  });
}

// 获取照片墙图片详情
export function getLivePhotoDetail(imgId) {
  return requestWWW.post('photo/getPhotoShiInfo', {
    splid: store.state.live.liveId,
    id: imgId,
    token: store.state.app.token,
  });
}

// 购买下载照片
export function buyLivePhoto(livePhotoId) {
  return request('hmGiftController/buyPhoto', 'POST', {
    id: livePhotoId,
    splid: store.state.live.liveId,
  });
}
```

## File: src/api/pigOut/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 提交分数
export default function submitScore(score) {
  return request.post('play/shangfen16', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay17',
    fenshu: score,
    userId: store.state.user.userId,
  });
}
```

## File: src/api/playFootball/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 提交分数
export default function submitScore(score) {
  return request.post('play/shangfen16', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay20',
    fenshu: score,
    userId: store.state.user.userId,
  });
}
```

## File: src/api/shake/index.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 发送摇一摇分数
export function sendScore(score, gameCode = 'hmPlay6', isNeedRank = 0) {
  const params = {
    splid: store.state.live.liveId,
    playInfo: gameCode,
    fenshu: score,
    userId: store.state.user.userId,
  };

  if (isNeedRank !== 0) {
    params.is_need_rank = isNeedRank;
  }

  return request.post('play/shangfen26', params);
}
// 获取摇一摇排行榜
export function getRank(gameCode, isNeedRank = 0) {
  const params = {
    splid: store.state.live.liveId,
    userId: store.state.user.userId,
    playInfo: gameCode,
  };

  if (isNeedRank !== 0) {
    params.is_need_rank = isNeedRank;
  }

  return request.get('play/newChaKeLaList6', { params });
}

// export function sendCattleScore(score) {
//   return request.post('play/shangfen26', {
//     splid: store.state.live.liveId,
//     playInfo: 'hmPlay8',
//     fenshu: score,
//     userId: store.state.user.userId,
//   });
// }

// 获取赛龙舟信息
export function getDragonBoatTeamInfo() {
  return request.post('/dragon/getDragonInfo', {
    splid: store.state.live.liveId,
  });
}

// 选择赛龙舟团队
export function chooseDragonBoatTeam(teamId) {
  return request.post('/dragon/joinDragon', {
    splid: store.state.live.liveId,
    teamId,
  });
}

// 赛龙舟提交分数
export function commitDragonBoatTeamScore(pObj) {
  return request.post('/dragon/addScore', {
    splid: store.state.live.liveId,
    fenshu: pObj.fenshu,
    teamId: pObj.teamId,
  });
}

// 赛龙舟排行榜列表
export function getDragonBoatTeamRank() {
  return request.post('/dragon/dragonRankList', {
    splid: store.state.live.liveId,
    playInfo: 'hmPlay12',
  });
}
```

## File: src/api/vote/brideVote.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 初始化投票
export function initBrideVote() {
  return request.post('vote/getPlayerInfo2', {
    splid: store.state.live.liveId,
  });
}

// 投票
export function submitBrideVote({
  playerId,
  type,
}) {
  return request.post('vote/submitVoteGroomsman', {
    splid: store.state.live.liveId,
    player_id: playerId,
    number_info: type,
  });
}
```

## File: src/api/vote/vote.js
```javascript
import request from '../../utils/request';
import store from '../../store/index';

// 初始化投票
export function initVote() {
  return request.post('vote/startHmVote6', {
    splid: store.state.live.liveId,
    playInfo: 'vote',
  });
}

// 投票
export function submitVote(paramObj) {
  return request.post('vote/submitVote6', {
    splid: store.state.live.liveId,
    vote_id: paramObj.voteId,
    vote_limit: paramObj.voteSize,
  });
}

// 范围投票
export function submitVoteRange(voteIds) {
  return request.post('vote/submitVote2', {
    splid: store.state.live.liveId,
    vote_ids: voteIds,
  });
}

// 保存已选投票项到缓存
export function saveActiveVoteToLocal(voteIds) {
  if (!voteIds) {
    return;
  }
  const activeVoteObj = {
    splid: store.state.live.liveId,
    voteIds,
  };
  localStorage.setItem('activeVote', JSON.stringify(activeVoteObj));
}
/* eslint-disable */
// 获取已选投票项
export function getActiveVoteFromLocal(voteInfo) {
  const activeVoteStr = localStorage.getItem('activeVote');
  if (!activeVoteStr) {
    return;
  }
  const { splid, voteIds } = JSON.parse(activeVoteStr);
  const { voteType, remain_vote, voteSize } = voteInfo;
  // 非本场活动清空activeVote缓存
  if (splid !== store.state.live.liveId) {
    localStorage.removeItem('activeVote');
    return;
  }
  // 单选情况下 剩余票数和总票数相等则清空缓存
  if (remain_vote === voteSize && voteType === '1') {
    localStorage.removeItem('activeVote');
    return;
  }
  // 自由投票情况下 不需要缓存
  if (voteType === '3') {
    localStorage.removeItem('activeVote');
    return;
  }
  return voteIds;
}
```

## File: src/api/zyz/index.js
```javascript
import request from '../../utils/request';
import requestMp from '../../utils/requestMp';
import store from '../../store/index';

// 获取奖池金额
export function getPoolMoney() {
  return request.get(`jianLai/luckyDbList6?splid=${store.state.live.liveId}`);
}

// 获取转一转相关信息
export function getZyzInfo() {
  return request.get(
    `jianLai/getLuckyId6?splid=${store.state.live.liveId}&playInfo=hdGame89`,
  );
}

// 获取转一转排行榜列表
export function getZyzRank() {
  return request.get(`jianLai/luckyDbRank6?splid=${store.state.live.liveId}`);
}

// 转一转充值
export function zyzRecharge() {
  return requestMp.post('hmWxmoney/chongzhiNyn', {
    USER_ID: store.state.user.userId,
    splid: store.state.live.liveId,
    openid: store.state.user.openId,
    giftId: 'one',
  });
}

// 转一转开始game
export function startZyz(paramObj) {
  return request.post('jianLai/luckyDb6', {
    splid: store.state.live.liveId,
    playInfo: 'hdGame89',
    id: paramObj.turnId,
  });
}

// 转一转发送中奖信息
export function sendPrizeInfo(paramObj) {
  return request.post('jianLai/luoXuanWan6', {
    type: '2',
    gold: paramObj.gold,
    balance: paramObj.remainCoin,
    splid: store.state.live.liveId,
    id: paramObj.turnId,
  });
}
```

## File: src/assets/constant/audio.js
```javascript
import { STATIC_HOST } from './host';

export default {
  countMoney: `${STATIC_HOST}audio/countMoney02.mp3`,
  pigOut: `${STATIC_HOST}audio/pigOut.mp3`,
  gbqq: `${STATIC_HOST}audio/gbqqNew.mp3`,
  cutFruitBg: `${STATIC_HOST}audio/bg.mp3`,
  cutFruitBoom: `${STATIC_HOST}audio/boom.mp3`,
  cutFruitCut: `${STATIC_HOST}audio/cut.mp3`,
  cutFruitOver: `${STATIC_HOST}audio/over.mp3`,
  getMoney: `${STATIC_HOST}audio/getMoney.mp3`,
  getMoneyNew: `${STATIC_HOST}audio/getMoneyNew.mp3`,
  clickStep: `${STATIC_HOST}audio/clickStep.mp3`,
  clickTiger: `${STATIC_HOST}audio/clickTiger.mp3`,
  footballHit: `${STATIC_HOST}audio/footballHit.mp3`,
  moneyIn: `${STATIC_HOST}audio/lingqiandaozhang.m4a`,
};
```

## File: src/assets/constant/effect.js
```javascript
import { STATIC_HOST, STATIC_SCREENHOST } from './host';

export const superDanmuPreview = `${STATIC_HOST}animation/superDanmuPreview.gif`; // 超级弹幕预览
export const superDanmuEntry = `${STATIC_HOST}animation/superDanmuEntry.gif`; // 超级弹幕入口
export const startBtn = `${STATIC_HOST}animation/startBtn.svga`; // 开始game按钮
export const bsDanmu = `${STATIC_HOST}animation/giftBsDanmuPhone.svga`; // 礼物伴生弹幕
export const RocketDanmu = {
  small: `${STATIC_SCREENHOST}animation/rocketSmall.svga`, // 小号火箭
  mid: `${STATIC_SCREENHOST}animation/rocketMid.svga`, // 中号火箭
  big: `${STATIC_SCREENHOST}animation/rocketBig.svga`, // 大号火箭
  headBox: `${STATIC_SCREENHOST}animation/rocketHeadBox.svga`, // 火箭头像框, 装饰用
  rocketStar: `${STATIC_SCREENHOST}animation/rocketStar.svga`, // 火箭星星, 装饰用
};
// 皇冠霸屏(废弃)
export const Bapin = {
  crownBapinLevel1: `${STATIC_HOST}animation/crownBapinLevel1.svga`,
  crownBapinLevel2: `${STATIC_HOST}animation/crownBapin2.svga`,
  crownBapinLevel3: `${STATIC_HOST}animation/crownBapin3.svga`,
};
export const BapinLove = {
  bapinLove1: `${STATIC_HOST}animation/bapinLove1New.svga`,
  bapinLove2: `${STATIC_HOST}animation/bapinLove2New.svga`,
  bapinLove3: `${STATIC_HOST}animation/bapinLove3New.svga`,
  bapinLove4: `${STATIC_HOST}animation/bapinLove4New.svga`,
};

export const BapinEnterprise = {
  bapinEnterprise1: `${STATIC_HOST}animation/baping_yidong_lanse_00.svga`,
  bapinEnterprise2: `${STATIC_HOST}animation/baping_yidong_hongse_00.svga`,
  bapinEnterprise3: `${STATIC_HOST}animation/baping_yidong_zise_00.svga`,
  bapinEnterprise4: `${STATIC_HOST}animation/baping_yidong_jinse_00.svga`,
};
// 进场效果
export const enterEffect = {
  enterGoat: `${STATIC_HOST}animation/enterGoat.svga`,
  enterGoatText: `${STATIC_HOST}animation/enterGoatTextNew.svga`,
  enterBird: `${STATIC_HOST}animation/enterBirdNew.svga`,
  enterBirdText: `${STATIC_HOST}animation/enterBirdTextNew.svga`,
  enterDragon: `${STATIC_HOST}animation/enterDragon.svga`,
  enterDragonText: `${STATIC_HOST}animation/enterDragonTextNew.svga`,
  enterLion: `${STATIC_HOST}animation/enterLion.svga`,
  enterPhoenix: `${STATIC_HOST}animation/enterPhoenix.svga`,
  enterPhoenixText: `${STATIC_HOST}animation/enterPhoenixtext.svga`,
};

export const clickHbWaitBg = `${STATIC_HOST}animation/clickHbWaitBg.svga`;

export const weddingLoadBg = `${STATIC_HOST}animation/weddingLoadBg.svga`;

/** 兔子投篮相关常量 */
export const BASKETBALL_SHOOT = {
  /** 标题svga图片地址 */
  waitTitle: 'https://static.hudongmiao.com/joymewScreen/animation/basketball-shoot-wait-title.svga',
  /** 替换的svga图片地址 */
  replaceImg: 'https://static.hudongmiao.com/joymewScreen/animation/replace-img.png',
  waitBall: 'https://static.hudongmiao.com/joymewScreen/animation/basketball-shoot-wait-ball.svga',
  prizeSheetTitle: 'https://static.hudongmiao.com/joymewScreen/animation/basketball-shoot-prize-sheet-title.svga',
};

/** 中式婚礼霸屏礼物预览效果
 *
 */
// export const ZSHL_BAPIN_PREVIEW = [
//   'https://ustatic.joymew.com/joymewH5/img/zsbapin1.gif',
//   'https://ustatic.joymew.com/joymewH5/img/zsbapin2.gif',
//   'https://ustatic.joymew.com/joymewH5/img/zsbpin3.gif',
//   'https://ustatic.joymew.com/joymewH5/img/zsbapin4.gif',
// ];

export const ZSHL_BAPIN_PREVIEW = [
  'https://ustatic.joymew.com/joymewMp/img/bapinPrew1.gif',
  'https://ustatic.joymew.com/joymewMp/img/bapinPrew2.gif',
  'https://ustatic.joymew.com/joymewMp/img/bapinPrew3.gif',
  'https://ustatic.joymew.com/joymewMp/img/bapinPrew4.gif',
];
```

## File: src/assets/constant/host.js
```javascript
export const CHAT_HOST = process.env.VUE_APP_CHAT_API;
export const STATIC_HOST = 'https://static.hudongmiao.com/joymewH5/';
export const STATIC_SCREENHOST = 'https://static.hudongmiao.com/joymewScreen/';
```

## File: src/assets/constant/others.js
```javascript
// 其他的一些常量
import BasketImg from '@/assets/image/basketball-shoot/basket-goal-ani.png';
import BallImg from '@/assets/image/basketball-shoot/shoot-ball-ani.png';

/** 兔子投篮游戏相关常量 */
export const BASKETBALL_SHOOT_GAME = {
  /** 页面宽度 */
  pageWidth: document.documentElement.clientWidth,
  /** 页面高度 */
  pageHeight: document.documentElement.clientHeight,
  /** 原始设计稿宽度 */
  designWidth: 375,
  /** 原始设计稿高度 */
  designHeight: 812,
  /** 原始篮筐宽度 */
  basketWidth: 99,
  /** 原始篮筐距上边界距离 */
  basketTop: 185,
  /** 原始篮球宽度 */
  ballWidth: 90,
  /** 原始篮球距下边界距离 */
  ballBottom: 240,
  /** 篮筐图片（精灵图） */
  basketImg: BasketImg,
  /** 篮球图片 */
  ballImg: BallImg,
  /** 篮筐单次循环的时间 */
  basketMoveTime: 2000,
  /** 篮球抛出后回到底部的时间 */
  ballBackTime: 1000,
};
```

## File: src/store/index.js
```javascript
import Vue from 'vue';
import Vuex from 'vuex';
import app from './modules/app';
import live from './modules/live';
import user from './modules/user';
import game from './modules/game';
import chat from './modules/chat/index';

Vue.use(Vuex);

const store = new Vuex.Store({
  modules: {
    app,
    live,
    user,
    game,
    chat,
  },
});

export default store;
```

## File: src/store/modules/chat/index.js
```javascript
import { getChatMessage } from '@/api/chat/index';
import store from '@/store';
import { formatChatList, formatChat, getCardChat } from './utils';
import { createCardChatTask, canSendCardChat } from './utils/cardChat';

const CARD_CHAT_TIMER = 10; // 消息记录不更新后CARD_CHAT_TIMER秒发送一次卡片消息

const state = {
  chatList: [], // 聊天记录(包括发送礼物记录、聊天记录)
};

const mutations = {
  initChatList: (state, data) => {
    state.chatList = data;
    // 如果可以发卡片消息，则创建个n秒后发送一次卡片消息的任务
    if (canSendCardChat()) {
      createCardChatTask(CARD_CHAT_TIMER);
    }
  },
  addChat: (state, data) => {
    if (state.chatList.length > 30) {
      state.chatList.shift();
    }
    state.chatList.push(
      formatChat({
        chat: data,
        giftListAll: store.state.live.giftListAll,
        sceneType: store.state.live.sceneType,
      }),
    );
    // 如果可以发卡片消息，则创建个n秒后发送一次卡片消息的任务
    if (canSendCardChat()) {
      createCardChatTask(CARD_CHAT_TIMER);
    }
  },
  /**
   * 添加卡片消息
   */
  addCardChat: (state) => {
    const {
      card_json, avatar, emcee_name, rank_city, rank_country, rank_province,
    } = store.state.user.emceeInfo;
    state.chatList.push(
      getCardChat({
        cardJson: card_json,
        avatar,
        name: emcee_name,
        rankCity: rank_city,
        rankCountry: rank_country,
        rankProvince: rank_province,
      }),
    );
  },
};

const actions = {
  async getChatList(ctx) {
    try {
      const res = await getChatMessage();
      // 监听礼物列表获取到后再设置chatList...
      if (store.state.live.giftListAll.length > 0) {
        // 根据giftListAll设置chatList
        ctx.commit(
          'initChatList',
          formatChatList({
            chatList: res.chat_list,
            giftListAll: store.state.live.giftListAll,
            sceneType: store.state.live.sceneType,
          }),
        );
      } else {
        // 监听giftListAll有值后再根据它设置chatList...
        const unsuscribe = store.subscribe((mutation, state) => {
          if (mutation.type === 'live/setGiftList' && state.live.giftListAll.length > 0) {
            ctx.commit(
              'initChatList',
              formatChatList({
                chatList: res.chat_list,
                giftListAll: state.live.giftListAll,
                sceneType: state.live.sceneType,
              }),
            );
          }
          unsuscribe();
        });
      }
    } catch (err) {
      console.log(err);
    }
  },
};

export default {
  namespaced: true,
  state,
  mutations,
  actions,
};
```

## File: src/store/modules/chat/utils/cardChat.js
```javascript
import store from '@/store';

let timer = null;
/**
 * 判断是否可以发送卡片消息
 */
export const canSendCardChat = () => {
  // 定制婚礼堂小程序可以发
  if (store.state.live.dz_hltcard && store.state.app.hotelReserveVisible) {
    return true;
  }
  // 字节小程序不可以发
  if (store.state.app.env === 'tt') {
    return false;
  }
  // 被拉黑了不可以发
  if (store.state.user.isForbidBuyHbq) {
    return false;
  }
  // 非互动小程序不可以发
  if (!store.state.app.mpType) {
    return false;
  }
  return store.getters['user/cardChatSwitch'];
};

/**
 * 创建发卡片消息的任务
 * @param {number} n 多少秒后发送
 */
export const createCardChatTask = (n) => {
  // 如果任务进行中，则重置计时器
  if (timer) {
    clearTimeout(timer);
    timer = null;
  }
  timer = setTimeout(() => {
    store.commit('chat/addCardChat');
  }, n * 1000);
};
```

## File: src/store/modules/chat/utils/func.js
```javascript
// ------regionStart(亲友)------

const RELATIVES = {
  0: '亲友',
  1: '父母',
  2: '舅舅',
  3: '叔叔',
  4: '伯伯',
  5: '阿姨',
  6: '姐妹',
  7: '兄弟',
  8: '朋友',
  9: '同学',
  10: '师长',
  11: '同事',
  12: '自定义',
};

/**
 * type取值格式 1(男方亲友),2(女方亲友),''或者1-1(表示男方父母)、2-1(表示女方父母)
 */
const getRelativeTypeLabel = (type) => {
  if (type.includes('-')) {
    const tmpSubTypeInfos = type.split('-');
    const firstLevelType = tmpSubTypeInfos[0];
    const secondLevelType = tmpSubTypeInfos[1];
    const firstLevelTypeLabel = firstLevelType === '1' ? '男方' : '女方';
    let secondLevelTypeLabel;
    if (/^\d+$/.test(secondLevelType)) {
      secondLevelTypeLabel = RELATIVES[secondLevelType];
    } else {
      secondLevelTypeLabel = secondLevelType;
    }
    return `${firstLevelTypeLabel}${secondLevelTypeLabel}`;
  }
  if (type === '1') {
    return '男方亲友';
  }
  if (type === '2') {
    return '女方亲友';
  }
  return '';
};

/**
 * 获取亲友信息
 */
export const getRelativeInfo = (type) => {
  return {
    relativeType: type || '',
    relativeTypeLabel: getRelativeTypeLabel(type),
  };
};

// ------regionEnd(亲友)------

// ------regionStart(礼物信息)------
/**
 * 聊天记录中的礼物图标(通用)
 */
const CHAT_ICON = {
  bapin: 'https://ustatic.joymew.com/joymewScreen/hd2/bapinIconNew.png',
  photo: 'https://ustatic.joymew.com/joymewScreen/hd2/photoIconNew.png',
  rocket: 'https://ustatic.joymew.com/joymewScreen/hd2/danmuIconNew.png',
  superDanmu: 'https://ustatic.joymew.com/joymewScreen/hd2/superDanmuIcon.png',
  hbkd: 'https://ustatic.joymew.com/joymewScreen/hd2/hbkdIconNew.png',
  photoWall: 'https://ustatic.joymew.com/joymewScreen/hd2/photoWallIconNew.png',
};
/**
 * 中式婚礼版聊天记中的图标
 */
const CHATICON_ZSHL = {
  bapin: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/zfhfIconEtry.png',
  photo: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/photoIcon.png',
  rocket: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/zsdm.png',
  superDanmu: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/allScreenIcon.png',
  hbkd: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/hbkdIcon.png',
  photoWall: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/photoInstant.png',
};
/**
 * 获取霸气弹幕名称
 */
const getBqName = ({ giftId, sceneType }) => {
  if (sceneType === '91') {
    const DANMU_NAME = ['飞龙在天', '有凤来仪', '麒麟送子'];
    const targetNum = Number(giftId.split('_')[2]);
    return DANMU_NAME[targetNum - 1];
  }
  return '火箭弹幕';
};

/**
 * 获取礼物图片
 */
const getGiftImg = ({ giftType, giftId, sceneType }) => {
  if (sceneType === '91') {
    if (giftId.includes('Miao_Bq')) {
      const XR_DANMUS = [
        'https://ustatic.joymew.com/joymewMp/zshl/danmu/dragonIcon.png',
        'https://ustatic.joymew.com/joymewMp/zshl/danmu/phonixIcon.png',
        'https://ustatic.joymew.com/joymewMp/zshl/danmu/sklinIcon.png',
      ];
      const targetNum = Number(giftId.split('_')[2]);
      return XR_DANMUS[targetNum - 1];
    }
    return CHATICON_ZSHL[giftType];
  }
  return CHAT_ICON[giftType];
};
/**
 * 根据已知条件获取礼物信息
 */
const judgeAndGetGiftInfo = ({ giftId, sceneType, giftListAll }) => {
  const giftInfo = {
    giftName: '',
    giftType: '',
    giftImg: '',
  };
  if (giftId.includes('Miao_Bp')) {
    giftInfo.giftName = '祝福横幅';
    giftInfo.giftType = 'bapin';
    giftInfo.giftImg = getGiftImg({ giftType: giftInfo.giftType, giftId, sceneType });
  } else if (giftId.includes('Miao_Tp')) {
    giftInfo.giftName = '照片霸屏';
    giftInfo.giftType = 'photo';
    giftInfo.giftImg = getGiftImg({ giftType: giftInfo.giftType, giftId, sceneType });
  } else if (giftId.includes('Miao_Bq')) {
    giftInfo.giftName = getBqName({ giftId, sceneType });
    giftInfo.giftType = 'rocket';
    giftInfo.giftImg = getGiftImg({ giftType: giftInfo.giftType, giftId, sceneType });
  } else if (giftId.includes('Miao_SuperDanmu')) {
    giftInfo.giftName = '超级弹幕';
    giftInfo.giftType = 'superDanmu';
    giftInfo.giftImg = getGiftImg({ giftType: giftInfo.giftType, giftId, sceneType });
  } else if (giftId.includes('hbkd')) {
    giftInfo.giftName = '红包';
    giftInfo.giftType = 'hbkd';
    giftInfo.giftImg = getGiftImg({ giftType: giftInfo.giftType, giftId, sceneType });
  } else if (giftId.includes('Miao_PhotoWall')) {
    giftInfo.giftName = '照片墙';
    giftInfo.giftType = 'photoWall';
    giftInfo.giftImg = getGiftImg({ giftType: giftInfo.giftType, giftId, sceneType });
  } else if (giftId) {
    const tmpGift = giftListAll.find((item) => item.giftconst === giftId);
    if (tmpGift) {
      giftInfo.giftName = tmpGift.giftname;
      giftInfo.giftType = 'gift';
      giftInfo.giftImg = tmpGift.imglink;
    }
  }

  return giftInfo;
};

/**
 * 获取礼物信息
 */
export const getGiftInfo = ({ giftId, sceneType, giftListAll }) => {
  if (!giftId) {
    return {};
  }
  const { giftName, giftType, giftImg } = judgeAndGetGiftInfo({ giftId, sceneType, giftListAll });
  return {
    giftName,
    giftType,
    giftImg,
  };
};

// ------regionEnd(礼物信息)------
```

## File: src/store/modules/game.js
```javascript
import { getSendGiftGameList } from '@/api/index/index';

const state = {
  currentGameCode: '',
  enterType: 'h5',
  needShake: false,
  gameUrl: '',
  gameStatus: 0, // 0：未开始、1：等待、2：进行中、3：已结束
  hbId: '', // 红包雨id
  canGetMarkUserInfo: false, // 是否能获取被评分选手的信息
  logoInfo: {
    fontColor: '',
    fontSize: '',
    name: '',
    logoPath: '',
    logoSize: '',
  },
  sendGiftGameList: [],
  giveMarkVersion: 'new', // 评分版本 new: 新版 old：旧版
  majiangRound: 1, // 雀神大赛的轮次
  canExposeCurrentQuestion: false, // 可以揭晓当前题目的答案了
  canNextQuestion: false, // 可以到下一题了
};

const mutations = {
  setGameInfo: (state, data) => {
    state.currentGameCode = data.currentGameCode;
    state.enterType = data.enterType;
    state.gameUrl = data.gameUrl;
    state.needShake = data.needShake;
  },
  setGameStatus: (state, data) => {
    state.gameStatus = data;
  },
  resetGameInfo: (state) => {
    state.currentGameCode = '';
    state.enterType = 'h5';
    state.gameUrl = '';
    state.needShake = false;
  },
  setHbyId: (state, data) => {
    state.hbId = data;
  },
  setCanMarkUserInfo: (state, data) => {
    state.canGetMarkUserInfo = data;
  },
  setLogoInfo: (state, data) => {
    if (data.logoPath) {
      state.logoInfo.fontColor = data.fontColor;
      state.logoInfo.fontSize = data.fontSize;
      state.logoInfo.name = data.name;
      state.logoInfo.logoPath = data.logoPath;
      state.logoInfo.logoSize = data.logoSize;
    }
  },
  setSendGiftGameList: (state, data) => {
    state.sendGiftGameList.splice(0);
    const tmpLen = data.length;
    for (let i = 0; i < tmpLen; i += 1) {
      state.sendGiftGameList.push(data[i]);
    }
  },
  setGiveMarkVersion: (state, data) => {
    state.giveMarkVersion = data === '2' ? 'old' : 'new';
  },
  /** 变更雀神大赛的轮次 */
  setMajiangRound: (state, data) => {
    state.majiangRound = Number(data || 1);
  },
  setCanExposeCurrentQuestion: (state, data) => {
    state.canExposeCurrentQuestion = data;
  },
  setCanNextQuestion: (state, data) => {
    state.canNextQuestion = data;
  },
};

const actions = {
  initSendGiftGameList(ctx) {
    // ctx.commit('setSendGiftGameList', );
    console.log(ctx);
    if (ctx.state.sendGiftGameList.length > 0) {
      return;
    }
    getSendGiftGameList()
      .then((res) => {
        console.log(res);
        ctx.commit('setSendGiftGameList', res.list);
      })
      .catch((err) => {
        console.log(err);
      });
  },
};

export default {
  namespaced: true,
  state,
  mutations,
  actions,
};
```

## File: src/store/modules/user.js
```javascript
import { reqGetUserInfo } from '@/api/index';
import { getRelativeTypeLabel } from '@/assets/constant/index';

import live from './live';

const state = {
  userPhone: '',
  userId: '',
  openId: '',
  unionid: '',
  name: '',
  headImg: '',
  money: 0,
  freeSendGift: false, // 是否拥有免费发礼物权限
  miao_vip_splid: '', // 最近一次领取了vip头像框的liveId
  miao_vip: '', // vip头像框
  isVipHeadBoxGetted: false, // 本场活动是否领过头像框
  vipLevel: '', // vip等级
  relativeType: '', // 男女方亲友
  currentStatus: '', // 单身、高富帅等
  deskNum: '', // 桌号,
  enterEffect: '', // 进场特效
  isForbidBuyHbq: false, // 是否禁止买宝箱和红包墙 拉黑功能
  vip_add_recharge: '',
  emceeInfo: {
    highPrivilege: 0, // 3和4:表示同庆楼用户 5表示婚礼堂用户
    isHideSuper: false, // 是否隐藏超级霸屏
    isUserH5: false, // 本场活动是否是h5
    signShowPhone: false, // 是否签到获取手机号
    phone_advert_json: '',
    isOpenAdvert: '',
    emcee_name: '',
    avatar: '',
    comment_json: '', // 微信二维码
    card_json: [], // 广告弹幕
    rank_city: '999',
    rank_country: '999',
    rank_province: '999',
    phonenumber: '',
    yue_switch: '0',
    unionid: '',
  },
};

const mutations = {
  setUserInfo: (state, data) => {
    state.userId = data.userId || state.userId;
    state.openId = data.openId || state.openId;
    state.unionid = data.unionid || state.unionid;
    state.name = data.name || state.name;
    state.headImg = data.headImg || state.headImg;
    state.miao_vip_splid = data.miao_vip_splid || state.miao_vip_splid;
    state.miao_vip = data.miao_vip || state.miao_vip;
    state.vipLevel = data.vipLevel || state.vipLevel;
    state.relativeType = data.relativeType || state.relativeType;
    state.currentStatus = data.currentStatus || state.currentStatus;
    state.deskNum = data.deskNum || state.deskNum;
    state.enterEffect = data.enterEffect || state.enterEffect;
    if (live.state.liveId === state.miao_vip_splid) {
      // 本场活动已经领过vip头像框了
      state.isVipHeadBoxGetted = true;
    } else {
      state.isVipHeadBoxGetted = false;
    }
    if (parseFloat(data.money) === 0 || parseFloat(data.money)) {
      state.money = parseFloat(data.money);
    }
    if (data.freeSendGift === '0' || data.freeSendGift === '1') {
      if (data.freeSendGift === '0') {
        state.freeSendGift = false;
      } else if (data.freeSendGift === '1') {
        state.freeSendGift = true;
      }
    }
    if (data.isForbidBuyHbq === true || data.isForbidBuyHbq === false) {
      state.isForbidBuyHbq = data.isForbidBuyHbq;
    }
    if (data.vip_add_recharge && data.vip_add_recharge !== '0') {
      state.vip_add_recharge = data.vip_add_recharge;
    }
  },
  setFreeSendGift: (state, data) => {
    if (data === '1') {
      state.freeSendGift = true;
    }
  },
  setEmceeInfo: (state, data) => {
    state.emceeInfo.highPrivilege = data.highPrivilege;
    state.emceeInfo.isHideSuper = data.isHideSuper === '1';
    state.emceeInfo.isUserH5 = data.isUserH5 === '1';
    state.emceeInfo.signShowPhone = data.signShowPhone === '1';
    if (data.is_open_advert) {
      const tmpIsOpenAdvert = String(data.is_open_advert);
      state.emceeInfo.isOpenAdvert = tmpIsOpenAdvert === '2';
    }
    state.emceeInfo.emcee_name = data.emcee_name;
    state.emceeInfo.avatar = data.avatar;
    state.emceeInfo.unionid = data.unionid;
    if (data.phone_advert_json) {
      try {
        const phoneAdverJsonObj = JSON.parse(data.phone_advert_json);
        state.emceeInfo.phone_advert_json = phoneAdverJsonObj.open_ping || '';
      } catch (err) {
        console.log(err);
      }
    }
    if (data.comment_json) {
      try {
        if (data.comment_json.indexOf('http') > -1) {
          state.emceeInfo.comment_json = data.comment_json;
        }
      } catch (err) {
        console.log(err);
      }
    }
    if (data.card_json) {
      try {
        state.emceeInfo.card_json = JSON.parse(data.card_json);
      } catch (err) {
        console.log(err);
      }
    }
    if (data.rank_city) {
      state.emceeInfo.rank_city = data.rank_city;
    }
    if (data.rank_country) {
      state.emceeInfo.rank_country = data.rank_country;
    }
    if (data.rank_province) {
      state.emceeInfo.rank_province = data.rank_province;
    }
    if (data.phonenumber) {
      state.emceeInfo.phonenumber = data.phonenumber;
    }
    if (data.yue_switch && data.yue_switch === '1') {
      state.emceeInfo.yue_switch = '1';
    }
  },
  setUserPhone: (state, data) => {
    state.userPhone = data || '';
  },
};

const actions = {
  async refreshUserInfo({ commit }) {
    try {
      const userRes = await reqGetUserInfo();
      commit('setUserInfo', {
        name: userRes.wx_name,
        headImg: userRes.avator,
        money: userRes.money.balance,
      });
    } catch (err) {
      console.log(err);
    }
  },
};

const getters = {
  isTql(state) {
    return state.emceeInfo.highPrivilege === 3 || state.emceeInfo.highPrivilege === 4;
  },
  isLiveMaster(state) {
    return state.emceeInfo.unionid === state.unionid ? '1' : '0';
  },
  relativeTypeText(state) {
    return live.state.sceneType === '0' && live.state.identitySwitch ? getRelativeTypeLabel(state.relativeType) : '';
  },
  yuehunSwitch(state) {
    if (state.emceeInfo.card_json.length > 0) {
      for (let i = 0; i < state.emceeInfo.card_json.length; i++) {
        if (state.emceeInfo.card_json[i].type === 'hostCard' && state.emceeInfo.card_json[i].yuehunSwitch === '1') {
          return true;
        }
      }
    }
    return false;
  },
  cardChatSwitch(state) {
    if (state.emceeInfo.card_json.length > 0) {
      for (let i = 0; i < state.emceeInfo.card_json.length; i++) {
        if (state.emceeInfo.card_json[i].type === 'hostCard' && state.emceeInfo.card_json[i].switch === '1') {
          return true;
        }
      }
    }
    return false;
  },
};

export default {
  namespaced: true,
  state,
  getters,
  mutations,
  actions,
};
```

## File: src/utils/index.js
```javascript
import Vue from 'vue';

// 定时器任务
export const timeoutTask = (task, time) => {
  const tmpTimeout = setTimeout(() => {
    task();
    clearTimeout(tmpTimeout);
  }, time);
};

// 获取url中的参数
export const getUrlParam = (key) => {
  const tmpRes = window.location.search.match(
    new RegExp(`[?&]${key}=([^&]+)`, 'i'),
  );
  let result;
  if (tmpRes === null || tmpRes.length < 1) {
    result = '';
  } else {
    [, result] = tmpRes;
  }
  return result;
};

// 生成随机数(min到max,不包括max)
export const generateRandom = (min, max) => {
  return Math.floor(Math.random() * (max - min)) + min;
};

// 生成随机id(随机字母加当前时间戳构成)
export const generateRandomId = (pLen) => {
  let tmpId = '';
  const charStr = 'ABCDEFGHJKMNPQRSTWXYZabcdefhijkmnprstwxyz';
  const tmpLen1 = charStr.length;
  const tmplen2 = pLen || 6; // 生成的id字母部分的长度，默认长度为6
  for (let i = 0; i < tmplen2; i += 1) {
    tmpId += charStr.charAt(Math.floor(Math.random() * tmpLen1));
  }
  tmpId += new Date().getTime();
  return tmpId;
};

const ismobile = () => {
  const u = navigator.userAgent;
  let tmpResult = '';
  if (
    /AppleWebKit.*Mobile/i.test(navigator.userAgent)
    || /MIDP|SymbianOS|NOKIA|SAMSUNG|LG|NEC|TCL|Alcatel|BIRD|DBTEL|Dopod|PHILIPS|HAIER|LENOVO|MOT-|Nokia|SonyEricsson|SIE-|Amoi|ZTE/.test(
      navigator.userAgent,
    )
  ) {
    if (window.location.href.indexOf('?mobile') < 0) {
      try {
        if (/iPhone|mac|iPod|iPad/i.test(navigator.userAgent)) {
          tmpResult = '0';
        } else {
          tmpResult = '1';
        }
      } catch (e) {
        console.log(e);
      }
    }
  } else if (u.indexOf('iPad') > -1) {
    tmpResult = '0';
  } else {
    tmpResult = '1';
  }
  return tmpResult;
};
// GMT转普通日期格式如：2021-09-27T11:13:26.403+0000转2021-09-27 19:13:26
export const newDateTransform = (timedata, t) => {
  let target = t;
  if (ismobile() === '0') {
    target = t - 8;
  }
  const date = new Date(timedata.substr(0, 19));
  const currentTime = date.getTime();
  const offset = date.getTimezoneOffset() * 60000;
  const utcTime = currentTime + offset;
  const newDate = new Date(utcTime + target * 3600000);
  const Year = newDate.getFullYear();
  const Month = newDate.getMonth() + 1 < 10
    ? `0${newDate.getMonth() + 1}`
    : newDate.getMonth() + 1;
  const d = newDate.getDate() < 10 ? `0${newDate.getDate()}` : newDate.getDate();
  const Hours = newDate.getHours() < 10 ? `0${newDate.getHours()}` : newDate.getHours();
  const Minutes = newDate.getMinutes() < 10
    ? `0${newDate.getMinutes()}`
    : newDate.getMinutes();
  const Seconds = newDate.getSeconds() < 10
    ? `0${newDate.getSeconds()}`
    : newDate.getSeconds();
  const overTime = `${Year}/${Month}/${d} ${Hours}:${Minutes}:${Seconds}`;
  return overTime;
};
// 获取圆形头像
export const getRoundImg = (img) => {
  const canvas = document.createElement('canvas');
  canvas.width = img.width;
  canvas.height = img.height;
  const r = canvas.width / 2;
  const ctx = canvas.getContext('2d');
  ctx.fillStyle = ctx.createPattern(img, 'no-repeat');
  ctx.clearRect(0, 0, img.width, img.height);
  ctx.arc(img.width / 2, img.height / 2, r, 0, Math.PI * 2);
  ctx.fill();
  const dataURL = canvas.toDataURL('image/png');
  return dataURL;
};

export const loadImg = (path) => new Promise((resolve, reject) => {
  const img = new Image();
  img.crossOrigin = '';
  img.src = path;
  img.onload = () => {
    resolve(img);
  };
  img.onerror = () => {
    reject();
  };
});

// 判断字符串是否以某个字符串结尾
export const isEndWithX = (tStr, endStr) => {
  const d = tStr.length - endStr.length;
  return d >= 0 && tStr.lastIndexOf(endStr) === d;
};

// 判断非负数
export const isUnNegtiveDigit = (targetStr) => {
  const r = /^(\d+)$|^(\d+\.\d{1,2})$/;
  return r.test(targetStr);
};
// 判断正整数
export const isPositiveInteger = (value) => {
  return /^[1-9]\d*$/.test(value);
};

// 秒转分:秒
export const sCtMs = (seconds) => {
  const minute = parseInt(seconds / 60, 10);
  let second = seconds % 60;
  if (second === 0) {
    second = '00';
  } else if (second < 10) {
    second = `0${second}`;
  }
  return `${minute}:${second}`;
};

// yyyy-MM-dd HH:mm:ss格式转时间戳
export const formatDateConvertTS = (dateStr) => {
  return new Date(dateStr.replace(/-/g, '/')).getTime();
};
// 获取当前时间
export const getCurrentDate = () => {
  return new Date(+new Date() + 8 * 3600 * 1000)
    .toJSON()
    .substr(0, 19)
    .replace('T', ' ');
};
// 日期字符串转Date
export const dateStrConvert = (dateStr) => {
  const SEPARATOR_BAR = '-';
  const SEPARATOR_SLASH = '/';
  const SEPARATOR_DOT = '.';
  let dateArray;
  if (dateStr.indexOf(SEPARATOR_BAR) > -1) {
    dateArray = dateStr.split(SEPARATOR_BAR);
  } else if (dateStr.indexOf(SEPARATOR_SLASH) > -1) {
    dateArray = dateStr.split(SEPARATOR_SLASH);
  } else {
    dateArray = dateStr.split(SEPARATOR_DOT);
  }
  return new Date(dateArray[0], dateArray[1] - 1, dateArray[2]);
};
// 比较日期
export const dateCompare = (dateStr) => {
  const dateTime = dateStrConvert(dateStr).getTime();

  // 减去24小时
  const compareDateTime = new Date().getTime() - 24 * 60 * 60 * 1000;
  if (compareDateTime > dateTime) {
    return true;
  }
  if (compareDateTime === dateTime) {
    return false;
  }
  return false;
};

// 获取当前位置
export const getCurrentLocation = () => {
  return new Promise((resolve, reject) => {
    navigator.geolocation.getCurrentPosition(
      (position) => {
        console.log(position);
        const tmpCrd = position.coords;
        resolve(tmpCrd);
      },
      (positionError) => {
        console.log(positionError);
        reject(positionError);
      },
      {
        enableHighAccuracy: true,
        timeout: 10000,
        maximumAge: 0,
      },
    );
  });
};

// 根据两个点的经纬度信息计算出距离 单位km
export const getDistance = (lat1, lng1, lat2, lng2) => {
  const radLat1 = (lat1 * Math.PI) / 180.0;
  const radLat2 = (lat2 * Math.PI) / 180.0;
  const a = radLat1 - radLat2;
  const b = (lng1 * Math.PI) / 180.0 - (lng2 * Math.PI) / 180.0;
  let s = 2
    * Math.asin(
      Math.sqrt(
        (Math.sin(a / 2) ** 2)
          + Math.cos(radLat1) * Math.cos(radLat2) * (Math.sin(b / 2) ** 2),
      ),
    );
  s *= 6378.137;
  s = Math.round(s * 10000) / 10000;
  return s;
};

// 动态渲染某个组件到某个节点下
export const renderComp = (root, compConfig) => {
  const vueInstance = new Vue(compConfig);
  vueInstance.$mount();
  root.appendChild(vueInstance.$el);
};
```

## File: src/utils/loadFile.js
```javascript
/**
 * 目标模块资源加载
 * 属性：
 *    文件列表：
 *      moduleFileList:[
 *          {
 *              path,
 *              type,// type取值img、audio
 *          },
 *      ]
 *    总进度：
 *      totalProgress
 *    当前进度：
 *      currentProgress
 * 方法：
 *    更新当前进度：
 *      updateCurrentProgress
 *    加载两种格式文件资源
 *      loadImgFile、loadAudioFile
 *     提交模块资源(moduleFileList push值)
 *      commitModuleFileList
 *     清空资源列表
 *      clearModuleFileList
 *     加载模块资源
 *      loadModuleFileList
 *     加载索引
 *      loadIndex
 */
import store from '@/store/index';

const moduleFileList = [];
let totalProgress = 0;
let currentProgress = 0;
let loadIndex = 0;
const Observer = {};
// 加载图片文件
const loadImgFile = (path) => {
  const img = new Image();
  img.src = path;
  return new Promise((resolve, reject) => {
    img.onload = () => {
      resolve(path);
    };
    img.onerror = () => {
      reject();
    };
  });
};

// 加载音频文件
const loadAudioFile = (path) => {
  const audio = new Audio();
  audio.src = path;
  return new Promise((resolve, reject) => {
    audio.addEventListener('canplay', () => {
      resolve(path);
    });
    audio.onerror = () => {
      reject();
    };
  });
};
// 更新当前进度
const updateCurrentProgress = () => {
  if (currentProgress < totalProgress) {
    store.commit('app/updateCurrentLoadingProgress', currentProgress);
  } else {
    Observer.moduleFileListLoaded = true;
  }
};

// 加载moduleFileList
const loadModuleFileList = () => {
  if (moduleFileList[loadIndex]) {
    if (moduleFileList[loadIndex].type === 'img') {
      loadImgFile(moduleFileList[loadIndex].path)
        .then(() => {
          currentProgress += 1;
          updateCurrentProgress();
          loadIndex += 1;
          loadModuleFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (moduleFileList[loadIndex].type === 'audio') {
      loadAudioFile(moduleFileList[loadIndex].path)
        .then(() => {
          currentProgress += 1;
          updateCurrentProgress();
          loadIndex += 1;
          loadModuleFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    }
  }
};

// 清空模块资源
const clearModuleFileList = () => {
  loadIndex = 0;
  moduleFileList.splice(0);
};
Object.defineProperty(Observer, 'moduleFileListCommited', {
  configurable: true,
  enumerable: true,
  get() {
    return false;
  },
  set(val) {
    console.log('***moduleFileListCommited***');
    if (val) {
      console.log('***compute totalProgress and start load moduleFileList***');
      totalProgress = moduleFileList.length;
      loadModuleFileList();
    }
  },
});
Object.defineProperty(Observer, 'moduleFileListLoaded', {
  configurable: true,
  enumerable: true,
  get() {
    return false;
  },
  set(val) {
    console.log('***moduleFileListLoaded***');
    if (val) {
      console.log('***clear moduleFileList and hide loading page***');
      clearModuleFileList();
      store.commit('app/setLoading', false);
    }
  },
});

// 提交模块资源
const commitModuleFileList = (fileList, type) => {
  fileList.forEach((item) => {
    moduleFileList.push({
      path: item,
      type,
    });
  });
};

export default commitModuleFileList;
```

## File: src/utils/preloadFile.js
```javascript
/**
 * 文件预加载模块
 * 资源文件分为：系统直接引入(default前缀)的和接口获取的(dynamic前缀)
 * 过程：commit文件、加载文件
 * 数据结构：
 *     file:{ path,type } path:文件路径 type:文件类型(取值：img、video、audio、svga)
 *     backgroundFileList:[]<--->backgroundFileList文件加载完毕 loading页面关闭
 *     defaultFileList:[]
 *     dynamicFileList:[]
 *
 * 思路：
 *    手机请求到背景图片--->commit背景图片--->加载背景图片--->加载完毕发送通知--->开始加载defaultFileList中的资源
 *    defaultFileList中的资源加载完毕 && dynamicFileList commit完毕通知--->开始加载dynamicFileList
 */

import SVGA from 'svgaplayerweb';
import store from '@/store/index';
// import audioResource from '@/assets/constant/audio';
// import { startBtn } from '@/assets/constant/effect';
import { timeoutTask } from '@/utils/index';
import createjs from 'createjs-cmd';

const loadingBg = 'https://static.hudongmiao.com/joymewH5/img/loading/bg.png';
const loadingFan = 'https://static.hudongmiao.com/joymewH5/img/loading/fan.png';
const loadingLeaf = 'https://static.hudongmiao.com/joymewH5/img/loading/leaf.png';
const loadingProgressBarWhite = 'https://static.hudongmiao.com/joymewH5/img/loading/progressBarWhite.png';
const loadingProgressBarYellow = 'https://static.hudongmiao.com/joymewH5/img/loading/progressBarYellow.png';

const backgroundFileList = [];
const defaultFileList = [];
const dynamicFileList = [];

let backgroundFileListIndex = 0;
let defaultFileListIndex = 0;
let dynamicFileListIndex = 0;

let totalProgress = 0; // 总进度
let currentProgress = 0; // 当前进度
// 观察者模式(被观察：背景图片加载完毕、defaultFileList资源加载完毕&&dynamicFileList commit)
const Observer = {
  defaultFileListLoaded_display: false,
  dynamicFileListCommited_display: false,
};
// 加载图片文件
const loadImgFile = (path) => {
  const img = new Image();
  img.src = path;
  return new Promise((resolve, reject) => {
    img.onload = () => {
      resolve(path);
    };
    img.onerror = () => {
      reject();
    };
  });
};
// 加载视频文件
const loadVideoFile = (path) => {
  const video = document.createElement('video');
  return new Promise((resolve, reject) => {
    video.src = path;
    video.addEventListener('canplay', () => {
      resolve(path);
    });
    video.onerror = () => {
      reject();
    };
  });
};
// 加载音频文件
const loadAudioFile = (path) => {
  const audio = new Audio();
  audio.src = path;
  return new Promise((resolve, reject) => {
    audio.addEventListener('canplay', () => {
      resolve(path);
    });
    audio.onerror = () => {
      reject();
    };
  });
};
// 加载svga文件
const loadSVGAFile = (path) => {
  const parser = new SVGA.Parser();
  return new Promise((resolve, reject) => {
    parser.load(
      path,
      (videoItem) => {
        resolve(videoItem);
      },
      (err) => {
        reject(err);
      },
    );
  });
};
// 更新当前进度
const updateCurrentProgress = () => {
  let tmpPercentage = 0;
  if (totalProgress === 0 || currentProgress >= totalProgress) {
    tmpPercentage = 100;
  } else {
    tmpPercentage = ((currentProgress / totalProgress) * 100).toFixed(0);
  }

  store.commit('app/updateCurrentLoadingProgress', tmpPercentage);
  if (currentProgress >= totalProgress && totalProgress !== 0) {
    timeoutTask(() => {
      store.commit('app/setLoading', false);
    }, 500);
    // 通知加载defaultFileList
    // Observer.backgroundFileListLoaded = true;
  }
};
// 计算总进度
const computeTotalProgress = () => {
  totalProgress = backgroundFileList.length;
};
// 加载backgroundFileList
const loadBackgroundFileList = () => {
  if (backgroundFileList[backgroundFileListIndex]) {
    if (backgroundFileList[backgroundFileListIndex].type === 'img') {
      loadImgFile(backgroundFileList[backgroundFileListIndex].path)
        .then(() => {
          currentProgress += 1;
          updateCurrentProgress();
          backgroundFileListIndex += 1;
          loadBackgroundFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    }
  }
};
// 加载defaultFileList
const loadDefaultFileList = () => {
  if (defaultFileList[defaultFileListIndex]) {
    if (defaultFileList[defaultFileListIndex].type === 'img') {
      loadImgFile(defaultFileList[defaultFileListIndex].path)
        .then(() => {
          defaultFileListIndex += 1;
          loadDefaultFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (defaultFileList[defaultFileListIndex].type === 'video') {
      loadVideoFile(defaultFileList[defaultFileListIndex].path)
        .then(() => {
          defaultFileListIndex += 1;
          loadDefaultFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (defaultFileList[defaultFileListIndex].type === 'svga') {
      loadSVGAFile(defaultFileList[defaultFileListIndex].path)
        .then(() => {
          defaultFileListIndex += 1;
          loadDefaultFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (defaultFileList[defaultFileListIndex].type === 'audio') {
      loadAudioFile(defaultFileList[defaultFileListIndex].path)
        .then(() => {
          defaultFileListIndex += 1;
          loadDefaultFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    }
  } else {
    Observer.defaultFileListLoaded = true;
    Observer.defaultFileListLoaded_display = true;
  }
};
// 加载dynamicFileList
const loadDynamicFileList = () => {
  if (dynamicFileList[dynamicFileListIndex]) {
    if (dynamicFileList[dynamicFileListIndex].type === 'img') {
      loadImgFile(dynamicFileList[dynamicFileListIndex].path)
        .then(() => {
          dynamicFileListIndex += 1;
          loadDynamicFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (dynamicFileList[dynamicFileListIndex].type === 'video') {
      loadVideoFile(dynamicFileList[dynamicFileListIndex].path)
        .then(() => {
          dynamicFileListIndex += 1;
          loadDynamicFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (dynamicFileList[dynamicFileListIndex].type === 'svga') {
      loadSVGAFile(dynamicFileList[dynamicFileListIndex].path)
        .then(() => {
          dynamicFileListIndex += 1;
          loadDynamicFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    } else if (dynamicFileList[dynamicFileListIndex].type === 'audio') {
      loadAudioFile(dynamicFileList[dynamicFileListIndex].path)
        .then(() => {
          dynamicFileListIndex += 1;
          loadDynamicFileList();
        })
        .catch((err) => {
          console.log(err);
        });
    }
  }
};
// 定义属性backgroundFileListCommited 背景图片提交完毕开始加载背景图片
Object.defineProperty(Observer, 'backgroundFileListCommited', {
  configurable: true,
  enumerable: true,
  get() {
    return false;
  },
  set(val) {
    if (val) {
      console.log('backgroundFileList Commited');
      computeTotalProgress();
      // 加载背景资源
      loadBackgroundFileList();
    }
  },
});

// 定义属性backgroundFileListLoaded 背景图片加载完毕开始加载defaultFileList
Object.defineProperty(Observer, 'backgroundFileListLoaded', {
  configurable: true,
  enumerable: true,
  get() {
    return false;
  },
  set(val) {
    if (val) {
      console.log('backgroundFileList loaded');
      // 开始加载defaultFileList
      loadDefaultFileList();
    }
  },
});

// 定义属性defaultFileListLoaded  defaultFileList加载完毕
Object.defineProperty(Observer, 'defaultFileListLoaded', {
  configurable: true,
  enumerable: true,
  get() {
    return Observer.defaultFileListLoaded_display;
  },
  set(val) {
    console.log('defaultFileList Loaded', Observer.dynamicFileListCommited);
    if (val && Observer.dynamicFileListCommited) {
      console.log('load dynamicFileList');
      // 开始加载dynamicFileList
      loadDynamicFileList();
    }
  },
});

// 定义属性dynamicFileListCommited 接口获取的文件提交完毕并且背景图片加载完毕 开始加载dynamicFileList
Object.defineProperty(Observer, 'dynamicFileListCommited', {
  configurable: true,
  enumerable: true,
  get() {
    return Observer.dynamicFileListCommited_display;
  },
  set(val) {
    console.log('dynamicFileListCommited');
    if (val && Observer.defaultFileListLoaded) {
      console.log('load dynamicFileList');
      // 开始加载dynamicFileList
      loadDynamicFileList();
    }
  },
});

// 系统直接引入的资源先commit
// Object.keys(audioResource).forEach((item) => { defaultFileList.push({ path: audioResource[item], type: 'audio' }); });
// Object.keys(RocketDanmu).forEach((item) => { defaultFileList.push({ path: RocketDanmu[item], type: 'svga' }); });
// Object.keys(Bapin).forEach((item) => { defaultFileList.push({ path: Bapin[item], type: 'svga' }); });

// defaultFileList.push({ path: LoadingMew, type: 'svga' });
// defaultFileList.push({ path: startBtn, type: 'svga' });
backgroundFileList.push({ path: loadingBg, type: 'img' });
backgroundFileList.push({ path: loadingFan, type: 'img' });
backgroundFileList.push({ path: loadingLeaf, type: 'img' });
backgroundFileList.push({ path: loadingProgressBarWhite, type: 'img' });
backgroundFileList.push({ path: loadingProgressBarYellow, type: 'img' });

/**
 * 接口获取的资源提交
 */
export const commitDynamicFileList = (fileList, type) => {
  fileList.forEach((item) => {
    dynamicFileList.push({
      path: item,
      type,
    });
  });
  // Observer.dynamicFileListCommited = true;
  // Observer.dynamicFileListCommited_display = true;
};
/**
 * 接口获取的背景资源提交后触发资源加载逻辑
 * 背景资源加载映射为进度条更新--->背景资源加载完毕其他类型资源开始加载
 */
export const commitBackgroundFileList = (pFile) => {
  backgroundFileList.push(pFile);
  // 通知加载背景资源
  Observer.backgroundFileListCommited = true;
};

/**
 * 加载指定的资源
 * @param [] fileList
 * @return Promise
 */
export const preloadFileList = (fileList) => {
  const loader = new createjs.LoadQueue(false);
  return new Promise((resolve, reject) => {
    loader.loadManifest(fileList);
    loader.on('complete', () => {
      resolve();
    });
    loader.on('error', () => {
      reject();
    });
  });
};
```

## File: src/utils/request.js
```javascript
import axios from 'axios';
import qs from 'qs';
import store from '@/store/index';
import { getUrlParam } from './index';
import { recommendGiftLogic, funcTipLogic } from './service';
// import app from '../main';

// 执行弹出礼物逻辑
const resetRecommendInterval = recommendGiftLogic();
// 执行弹出功能提示逻辑
const resetFuncTipInterval = funcTipLogic();
// 转换form-data
function transformRequestData(data) {
  if (data instanceof FormData) {
    return data;
  }
  return qs.stringify(data);
}
// 创建axios实例
const service = axios.create({
  baseURL: process.env.VUE_APP_BASE_API,
  headers: {
    token: getUrlParam('token'),
    'Content-Type': 'application/x-www-form-urlencoded',
  },
  transformRequest: [transformRequestData],
  timeout: 10000,
});
// 过滤请求(每发送一次请求则重置定时器)
service.interceptors.request.use((config) => {
  // 重置弹出礼物定时器
  resetRecommendInterval();
  // 重置功能提示定时器
  resetFuncTipInterval();
  return config;
});
// 过滤响应
service.interceptors.response.use((result) => {
  if (result.data.message === '401') {
    console.log(result);
    // app.$toast.center('登录已过期,请删除小程序重新进入!');
    // 通知websocket关闭
    store.commit('app/setNeedLogin', true);
    return Promise.reject();
  }
  return result.data.data;
});

export default service;
```

## File: src/utils/requestGuessHbPay.js
```javascript
import axios from 'axios';
import qs from 'qs';

// 转换form-data
function transformRequestData(data) {
  if (data instanceof FormData) {
    return data;
  }
  return qs.stringify(data);
}

// 创建axios实例
const service = axios.create({
  baseURL: 'https://www.hudongmiao.com/',
  headers: {
    'Content-Type': 'application/x-www-form-urlencoded',
  },
  transformRequest: [transformRequestData],
  timeout: 10000,
});
// 过滤请求
service.interceptors.request.use((config) => {
  return config;
});
// 过滤响应
service.interceptors.response.use((result) => {
  return result.data;
});

export default service;
```

## File: src/utils/requestMp.js
```javascript
import axios from 'axios';
import qs from 'qs';
import store from '@/store/index';
import { getUrlParam } from './index';
// import app from '../main';

// 转换form-data
function transformRequestData(data) {
  if (data instanceof FormData) {
    return data;
  }
  return qs.stringify(data);
}
// 创建axios实例
const service = axios.create({
  baseURL: process.env.VUE_APP_BASE_API,
  headers: {
    token: getUrlParam('token'),
    'Content-Type': 'application/x-www-form-urlencoded',
    appid: 'wxb21a91c9a406e836',
  },
  transformRequest: [transformRequestData],
  timeout: 10000,
});
// 过滤请求
service.interceptors.request.use((config) => {
  return config;
});
// 过滤响应
service.interceptors.response.use((result) => {
  if (result.data.message === '401') {
    console.log(result);
    // app.$toast.center('登录已过期,请删除小程序重新进入!');
    // 通知websocket关闭
    store.commit('app/setNeedLogin', true);
    return Promise.reject();
  }
  return result.data;
});

export default service;
```

## File: src/utils/requestUpload.js
```javascript
import axios from 'axios';
import qs from 'qs';

// 转换form-data
function transformRequestData(data) {
  if (data instanceof FormData) {
    return data;
  }
  return qs.stringify(data);
}

// 创建axios实例
const service = axios.create({
  baseURL: 'https://www.hudongmiao.com/',
  headers: {
    'Content-Type': 'multipart/form-data',
  },
  transformRequest: [transformRequestData],
  timeout: 60000,
});
// 过滤请求
service.interceptors.request.use((config) => {
  return config;
});
// 过滤响应
service.interceptors.response.use((result) => {
  return result.data.data;
});

export default service;
```

## File: src/utils/requestWWW.js
```javascript
import axios from 'axios';
import qs from 'qs';
// 转换form-data
function transformRequestData(data) {
  if (data instanceof FormData) {
    return data;
  }
  return qs.stringify(data);
}

// 创建axios实例
const service = axios.create({
  baseURL: 'https://www.hudongmiao.com/',
  headers: {
    'Content-Type': 'application/x-www-form-urlencoded',
  },
  transformRequest: [transformRequestData],
  timeout: 10000,
});
// 过滤请求
service.interceptors.request.use((config) => {
  return config;
});
// 过滤响应
service.interceptors.response.use((result) => {
  const tmpResult = result.data.data ? result.data.data : result.data;
  return tmpResult;
});

export default service;
```

## File: src/utils/tools.js
```javascript
/** 获取 [min, max) 区间的任意整数 */
export const getRandomNum = (min, max) => {
  return Math.floor(Math.random() * (max - min) + min);
};
```

## File: src/utils/ttjssdk.js
```javascript
/* eslint-disable */
export const tt = (function() {
  'use strict';
  function e(e) {
    for (var n = '', t = new Uint8Array(e), r = t.byteLength, a = 0; a < r; a++)
      n += String.fromCharCode(t[a]);
    return _(n);
  }
  function n(e) {
    for (var n = C(e), t = n.length, r = new Uint8Array(t), a = 0; a < t; a++)
      r[a] = n.charCodeAt(a);
    return r.buffer;
  }
  function t(n) {
    return { base64: e(n) };
  }
  function r(e) {
    if (null != e) return e.base64 ? n(e.base64) : void 0;
  }
  function a(e) {
    return function(n) {
      return (
        Object.prototype.toString.call(n).toLowerCase() ===
        ('[object ' + e + ']').toLowerCase()
      );
    };
  }
  function o(e) {
    if (!1 === a('Object')(e)) return e;
    var n = [];
    for (var r in e) {
      var o = e[r];
      if (void 0 !== o && o instanceof ArrayBuffer && void 0 !== o.byteLength) {
        var i = t(o);
        (i.key = r), n.push(i);
      }
    }
    if (n.length > 0) {
      for (var s = 0; s < n.length; s++) delete e[n[s].key];
      e.__nativeBuffers__ = n;
    }
    return e;
  }
  function i(e) {
    if (!1 === a('Object')(e) || null == e.__nativeBuffers__) return e;
    var n = e.__nativeBuffers__;
    delete e.__nativeBuffers__;
    for (var t = 0; t < n.length; t++) {
      var o = n[t];
      if (null != o) {
        var i = r(o);
        void 0 !== i && i instanceof ArrayBuffer && (e[o.key] = i);
      }
    }
    return e;
  }
  function s(e, n) {
    if (void 0 !== e && 'function' == typeof O[n] && '' !== e && null !== e) {
      try {
        (e = JSON.parse(e)), (e = B.unpack(e));
      } catch (n) {
        e = {};
      }
      O[n](e), delete O[n];
    }
  }
  function c(e, n, t) {
    if (
      E &&
      D.needCache.find(function(n) {
        return n === e;
      })
    )
      return void F.push([e, n, t]);
    if (k) s(k.invoke(e, n, t), t);
    else {
      var r = { event: e, paramsString: n, callbackId: t };
      S.messageHandlers.invoke.postMessage(r);
    }
  }
  function f(e, n, t) {
    k
      ? k.publish(e, n, t)
      : S.messageHandlers.publish.postMessage({
          event: e,
          paramsString: n,
          webviewIds: t,
        });
  }
  function u(e, n, t) {
    n = B.pack(n);
    var r = JSON.stringify(n || {}),
      a = ++j;
    (O[a] = t), 'openSchema' === e && L.push(a), c(e, r, a);
  }
  function l(e, n) {
    'string' == typeof n && (n = JSON.parse(n)), (n = B.unpack(n));
    var t = O[e];
    'function' == typeof t && t(n), -1 === L.indexOf(e) && delete O[e];
  }
  function p(e, n) {
    J[e] = n;
  }
  function d(e, n, t) {
    (t = t || []), (t = JSON.stringify(t)), f(
      'custom_event_' + e,
      JSON.stringify(n),
      t,
    );
  }
  function g(e, n) {
    M['custom_event_' + e] = n;
  }
  function v(e, n, t, r) {
    if (e === T.onAppEnterBackground) E = !0;
    else if (e === T.onAppEnterForeground)
      for (E = !1; F.length; ) c.apply(null, F.shift());
    if (
      !E ||
      !D.needDisabled.find(function(n) {
        return n === e;
      })
    ) {
      'string' == typeof n && (n = JSON.parse(n)), (n = B.unpack(n));
      var a = e.indexOf('custom_event_') > -1 ? M[e] : J[e];
      'function' == typeof a && a(n, t, r);
    }
  }
  function h(e) {
    e();
  }
  function y() {
    var e = Array.prototype.slice.call(arguments);
    (e[1] = { data: e[1], options: { timestamp: Date.now() } }), h(function() {
      N.publish.apply(N, e);
    });
  }
  function b(e) {
    var n = e.name,
      t = void 0 === e.type ? 'sdk' : e.type,
      r = void 0 === e.args ? {} : e.args,
      a = void 0 === e.ext ? {} : e.ext;
    (H[x] = {
      success: r.success || R,
      fail: r.fail || R,
      complete: r.complete || R,
    }), (I[x] = {
      beforeAll: a.beforeAll || R,
      beforeSuccess: a.beforeSuccess || R,
      afterSuccess: a.afterSuccess || R,
      beforeFail: a.beforeFail || R,
      afterFail: a.afterFail || R,
      afterAll: a.afterAll || R,
    }), y('invokeAppServiceMethod', {
      name: n,
      type: t,
      args: r,
      callbackId: x,
    }), (x += 1);
  }
  var m = new Function('return this;')(),
    k = m.ttJSCore,
    S = m.webkit;
  m.ttJSCore &&
    (m.ttJSCore = {
      onDocumentReady: function() {
        return k.onDocumentReady();
      },
    });
  var A = navigator.userAgent.toLocaleLowerCase().includes('toutiaomicroapp');
  m.webkit &&
    A &&
    (m.webkit = {
      messageHandlers: {
        onDocumentReady: {
          postMessage: function() {
            return S.messageHandlers.onDocumentReady.postMessage('');
          },
        },
      },
    });
  var w = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=',
    _ =
      _ ||
      function(e) {
        for (
          var n, t, r = String(e), a = '', o = 0, i = w;
          r.charAt(0 | o) || ((i = '='), o % 1);
          a += i.charAt(63 & (n >> (8 - o % 1 * 8)))
        ) {
          if ((t = r.charCodeAt((o += 0.75))) > 255)
            throw new Error('"btoa" failed');
          n = (n << 8) | t;
        }
        return a;
      },
    C =
      C ||
      function(e) {
        var n = String(e).replace(/=+$/, ''),
          t = '';
        if (n.length % 4 == 1) throw new Error('"atob" failed');
        for (
          var r, a, o = 0, i = 0;
          (a = n.charAt(i++));
          ~a && ((r = o % 4 ? 64 * r + a : a), o++ % 4)
            ? (t += String.fromCharCode(255 & (r >> ((-2 * o) & 6))))
            : 0
        )
          a = w.indexOf(a);
        return t;
      },
    B = { new: t, get: r, pack: o, unpack: i },
    O = {},
    j = 0,
    J = {},
    M = {},
    F = [],
    E = !1,
    L = [],
    T = {
      onAppEnterBackground: 'onAppEnterBackground',
      onAppEnterForeground: 'onAppEnterForeground',
    },
    D = {
      needCache: ['showModal', 'showToast', 'showActionSheet', 'hideToast'],
      needDisabled: ['onAccelerometerChange', 'onCompassChange'],
    },
    N = { on: p, publish: d, invoke: u, subscribe: g };
  m.ttJSBridge = {
    get invokeHandler() {
      return l;
    },
    get subscribeHandler() {
      return v;
    },
  };
  var x = 0,
    H = [],
    I = [],
    R = function() {};
  return (function() {
    var e = Array.prototype.slice.call(arguments),
      n = e[1];
    (e[1] = function(e, t) {
      'string' == typeof e && (e = JSON.parse(e));
      var r = e.data;
      'function' == typeof n && n(r, t);
    }), h(function() {
      N.subscribe.apply(N, e);
    });
  })('callbackAppServiceMethod', function(e) {
    var n = e.res,
      t = e.isSuccess,
      r = e.callbackId,
      a = H[r],
      o = I[r];
    o.beforeAll(
      n,
    ), t ? (o.beforeSuccess(n), a.success(n), o.afterSuccess(n)) : (o.beforeFail(n), a.fail(n), o.afterFail(n)), a.complete(n), o.afterAll(n);
  }), {
    miniProgram: {
      redirectTo: function(e) {
        b({ name: 'redirectTo', args: e, type: 'jssdk' });
      },
      navigateTo: function(e) {
        b({ name: 'navigateTo', args: e, type: 'jssdk' });
      },
      switchTab: function(e) {
        b({ name: 'switchTab', args: e, type: 'jssdk' });
      },
      reLaunch: function(e) {
        b({ name: 'reLaunch', args: e, type: 'jssdk' });
      },
      navigateBack: function(e) {
        b({ name: 'navigateBack', args: e, type: 'jssdk' });
      },
      postMessage: function(e) {
        e && b({ name: 'postMessage', args: e, type: 'jssdk' });
      },
      setSwipeBackModeSync: function() {
        b({
          name: 'setSwipeBackMode',
          args: {
            mode:
              arguments.length > 0 && void 0 !== arguments[0]
                ? arguments[0]
                : 0,
          },
          type: 'jssdk',
        });
      },
    },
  };
})();
```

## File: src/utils/websocket/index.js
```javascript
import WebsocketHeartbeatJs from 'websocket-heartbeat-js';
import { CHAT_HOST } from '@/assets/constant/host';
import store from '@/store/index';
import handleMessage from './handleMessage';
import app from '../../main';
// 定义websocketHeartbeatJs
// 用于保证全局只有一个websocket连接
let websocketHeartbeatJs;

export default function connectWS() {
  // 连接websocket
  if (store.state.app.isInOtherWeviewH5) {
    // 其他webview容器打开应用的情况下不需要连接websocket
    console.log('其他webview容器打开应用的情况下不需要连接websocket');
    return;
  }
  if (websocketHeartbeatJs) {
    // 如果websocketHeartbeatJs已经存在,则不需要再次连接
    console.log('websocketHeartbeatJs已经存在,则不需要再次连接');
    return;
  }
  websocketHeartbeatJs = new WebsocketHeartbeatJs({
    url: `${CHAT_HOST}haimiao?miaoId=${store.state.app.token}&splid=${store.state.live.liveId}&kind=2`,
    pingTimeout: 120000,
    pingMsg: 'wxhb',
    repeatLimit: 100,
  });
  websocketHeartbeatJs.onopen = () => {
    app.$toast.center('聊天服务器连接成功');
  };
  websocketHeartbeatJs.onmessage = (e) => {
    try {
      const message = JSON.parse(e.data);
      handleMessage(message);
    } catch (e2) {
      // 非json格式空操作
    }
  };
  websocketHeartbeatJs.onreconnect = () => {
    if (store.state.app.needLogin) {
      websocketHeartbeatJs.close();
    }
    app.$toast.center('聊天服务器重连中....');
  };
  websocketHeartbeatJs.onerror = () => {
    if (store.state.app.needLogin) {
      app.$toast.center('登录已过期,请删除小程序重新进入!');
      return;
    }
    app.$toast.center('聊天服务器连接失败');
  };
}
```

## File: src/utils/wxApi.js
```javascript
// weixin-jssdk api封装
import { getAppId } from '@/api/guessHb/index';
import store from '@/store/index';
import wx from 'weixin-js-sdk';
import { tmpGetNewUrl } from './hdOptimizationTmpPatch';
import { tt } from './ttjssdk';

export default {
  // 初始化api
  initWXAPI: () => {
    return new Promise((resolve, reject) => {
      getAppId()
        .then((res) => {
          console.log(res);
          const {
            appId, timestamp, nonceStr, signature,
          } = res.qianMing;
          wx.config({
            debug: false,
            appId,
            timestamp,
            nonceStr,
            signature,
            jsApiList: ['chooseWXPay', 'updateAppMessageShareData', 'updateTimelineShareData'],
          });
          wx.error((err) => {
            reject(err);
            console.log('wxApi校验失败', err);
          });
          wx.ready((res) => {
            resolve(res);
            console.log('wxApi校验成功', res);
          });
        })
        .catch((err) => {
          reject(err);
          console.log(err);
        });
    });
  },
  // 支付
  pay: (param) => {
    return new Promise((resolve, reject) => {
      wx.chooseWXPay({
        timestamp: param.obj.timeStamp,
        nonceStr: param.obj.nonceStr,
        package: param.obj.package,
        signType: param.obj.signType,
        paySign: param.obj.paySign,
        success: (res) => {
          resolve(res);
        },
        fail: (err) => {
          reject(err);
        },
        complete: (res) => {
          if (res.errMsg === 'chooseWXPay:ok') {
            resolve(res);
          } else {
            reject(res);
          }
        },
      });
    });
  },
  // 小程序页面跳转
  navigateTo: (path) => {
    // 兼容性代码
    if (store.state.app.mpType) {
      localStorage.setItem('refreshUserInfoFlag', '1');
    }
    wx.miniProgram.navigateTo({
      url: path,
    });
  },
  /**
   * 临时跳转
   * 为了兼容重构后的互动小程序
   * 待另外两个小程序也重构完毕统一写法
   * @param {String} pageName 页面名称
   * @param {Object} queryObj 跳转页面携带的参数
   */
  tmpNavigateTo(pageName, queryObj) {
    const newUrl = tmpGetNewUrl(pageName, queryObj);
    console.log('newUrl:', newUrl);
    // 兼容性代码
    if (store.state.app.mpType) {
      localStorage.setItem('refreshUserInfoFlag', '1');
    }
    wx.miniProgram.navigateTo({
      url: newUrl,
    });
  },
  // 抖音小程序页面跳转
  navigateToTt: (path) => {
    tt.miniProgram.navigateTo({
      url: path,
    });
  },
  // 获取执行环境
  getEnv: () => {
    return new Promise((resolve, reject) => {
      try {
        wx.miniProgram.getEnv((res) => {
          resolve(res);
        });
      } catch (err) {
        reject(err);
      }
    });
  },
  // 判断代码执行环境
  judgeEnv() {
    return new Promise((resolve, reject) => {
      const ua = navigator.userAgent.toLowerCase();
      console.log(ua);
      if (ua && ua.match(/MicroMessenger/i) && ua.match(/MicroMessenger/i).toString() === 'micromessenger') {
        // ios的ua中无miniProgram，但都有MicroMessenger（表示是微信浏览器）
        this.getEnv()
          .then((res) => {
            console.log(res);
            if (res.miniprogram) {
              console.log('在小程序里');
              store.commit('app/setEnv', 'miniProgram');
              resolve('miniProgram');
            } else {
              console.log('不在小程序里');
              store.commit('app/setEnv', 'h5');
              store.commit('app/setInWeixinBrowse', true); // 在微信浏览器里
              resolve('h5');
            }
          })
          .catch((err) => {
            console.log(err);
            reject(err);
          });
      } else if (ua && ua.match(/toutiaomicroapp/i) && ua.match(/toutiaomicroapp/i).toString() === 'toutiaomicroapp') {
        console.log('在抖音里');
        store.commit('app/setEnv', 'tt');
        resolve('tt');
      } else {
        console.log('不在微信和抖音里');
        store.commit('app/setEnv', 'h5');
        store.commit('app/setInWeixinBrowse', false); // 不在微信浏览器里
        resolve('h5');
      }
    });
  },
  postMsg(msg) {
    wx.miniProgram.postMessage({
      data: msg,
    });
  },
  onSharePYQ({ title, link, imgUrl }) {
    wx.updateTimelineShareData({
      title,
      link,
      imgUrl,
      success: (res) => {
        console.log(res);
      },
    });
  },
  onShareHY({
    title, desc, link, imgUrl,
  }) {
    wx.updateAppMessageShareData({
      title,
      desc,
      link,
      imgUrl,
      success: (res) => {
        console.log(res);
      },
    });
  },
  /**
   * 开始录音
   */
  startRecord() {
    wx.startRecord();
  },
  /**
   * 停止录音
   */
  stopRecord() {
    return new Promise((resolve) => {
      wx.stopRecord({
        success: (res) => {
          resolve(res);
        },
      });
    });
  },
  /**
   * 监听录音自动停止
   */
  onVoiceRecordEnd() {
    return new Promise((resolve) => {
      wx.onVoicePlayEnd({
        complete: (res) => {
          resolve(res);
        },
      });
    });
  },
};
```

## File: vue.config.js
```javascript
const path = require('path');

const CompressionWebpackPlugin = require('compression-webpack-plugin');

const productionGzipExtensions = ['js', 'css'];

function resolve(dir) {
  return path.join(__dirname, dir);
}
const name = '嗨喵悦动'; // 标题
module.exports = {
  publicPath:
    process.env.VUE_APP_ENV === 'production'
      ? 'https://static.hudongmiao.com/hmydh5-qn/'
      : '/',
  outputDir: 'dist',
  assetsDir: 'static',
  lintOnSave: process.env.NODE_ENV === 'development',
  productionSourceMap: false,
  devServer: {
    host: '0.0.0.0',
    port: 80,
    open: false,
    proxy: {
      [process.env.VUE_APP_BASE_API]: {
        target: 'https://shm.hudongmiao.com/',
        // target: 'http://192.168.66.39:8022/',
        changeOrigin: true,
        pathRewrite: {
          [`^${process.env.VUE_APP_BASE_API}`]: '',
        },
      },
    },
    disableHostCheck: true,
  },
  configureWebpack: {
    name,
    resolve: {
      alias: {
        '@': resolve('src'),
      },
    },
    plugins: [
      // 配置compression-webpack-plugin压缩
      new CompressionWebpackPlugin({
        algorithm: 'gzip',
        test: new RegExp(`\\.(${productionGzipExtensions.join('|')})$`),
        threshold: 10240,
        minRatio: 0.8,
      }),
    ],
  },
};
```

## File: src/api/hotelReserve/index.js
```javascript
import requestWWW from '../../utils/requestWWW';
import request from '../../utils/request';
import store from '../../store/index';

// 获取酒店信息
export const getHotelInfo = () => {
  return requestWWW.post('/wedding/newGetWedding', {
    userId: store.state.live.emceeId,
  });
};
// 获取宴会厅列表
export const getBanquetList = (weddingId) => {
  return requestWWW.get(
    `/weddingBanquet/getWeddingBanquetList?wedding_id=${weddingId}`,
  );
};
// 获取菜单列表
export const getMenuList = (weddingId) => {
  return requestWWW.get(
    `/weddingMenu/getWeddingMenuList?wedding_id=${weddingId}`,
  );
};
// 获取套餐列表
export const getSetMealList = (weddingId) => {
  return requestWWW.get(
    `/weddingPackage/getWeddingPackageList?wedding_id=${weddingId}`,
  );
};
// 获取优惠活动列表
export const getDiscountList = (weddingId) => {
  return requestWWW.get(
    `/weddingActivity/getWeddingActivityList?wedding_id=${weddingId}`,
  );
};

// 预定主持
export const reserveHost = (pObj) => {
  return requestWWW.post('/schedule/save', pObj);
};
// 云境预定
export const reserveHostHlt = (pObj) => {
  return requestWWW.post('/schedule/save2', pObj);
};
// 获取预定信息
export const getReserveInfo = ({ splid, token }) => {
  return requestWWW.post('/schedule/getUserSchedule', {
    splid,
    token,
  });
};
// 保存浏览记录
export const saveBrowseRecord = (pObj) => {
  return requestWWW.post('/book/saveBookInfo', pObj);
};

// 获取主持人信息
export function reqGetHostProfile() {
  return request.get(
    `hostStyle/getInfo?userId=${store.state.live.emceeId}`,
  );
}
```

## File: src/api/index/index.js
```javascript
import axios from 'axios';
import request from '../../utils/request';
import requestMp from '../../utils/requestMp';
import requestUpload from '../../utils/requestUpload';
import store from '../../store/index';

// 获取活动信息
export function getLiveInfo() {
  return request.post('wxScan/chaoJiSaiYaRen', {
    splid: store.state.live.liveId,
  });
}

// 获取礼物列表
export function getGiftList() {
  return request.post('hmGiftController/listGift7', {
    splid: store.state.live.liveId,
  });
}
// 获取红包口袋信息
export function getHBKDInfo() {
  return request.post('hbkd/shenLuoTianZheng6', {
    splid: store.state.live.liveId,
  });
}

// 加入game
export function attendGame() {
  return request.get(`sendMsgController/renGo6?splid=${store.state.live.liveId}&userId=${store.state.user.userId}`);
}

// 获取game状态
export function getGameStatus() {
  return request.get(`play/baiyan6?splid=${store.state.live.liveId}&userId=${store.state.user.userId}`);
}

// 上传照片
export function uploadPhoto(formData) {
  console.log(formData.get('prefix'), formData.get('file'));
  return requestUpload.post('beiJing/shangchuanTomcat', formData);
}
// 发送礼物
export function sendGift(
  { giftId = store.state.app.currentGiftType } = {
    giftId: store.state.app.currentGiftType,
  },
) {
  return request.post('hmGiftController/sendGift6', {
    splid: store.state.live.liveId,
    giftconst: giftId,
  });
}

// 发送嘉年华礼物
export function sendGiftCarnival(
  { giftId = store.state.app.currentGiftType } = {
    giftId: store.state.app.currentGiftType,
  },
) {
  return request.post('hmGiftController/buySuperBp', {
    splid: store.state.live.liveId,
    giftconst: giftId,
    gstate: '6',
  });
}

// 发送推荐礼物
export function sendRecommendGift({ giftId = '' }) {
  return request.post('hmGiftController/sendGift6', {
    splid: store.state.live.liveId,
    giftconst: giftId,
  });
}
// 发送照片礼物
export function sendPhotoGift({ content, imgUrl, giftId = store.state.app.currentPhotoType }) {
  return request.post('hmGiftController/sendGift6', {
    splid: store.state.live.liveId,
    giftconst: giftId,
    content,
    tpUrl: imgUrl,
  });
}

// 发送霸气弹幕礼物
export function sendDanmuGift({ content, giftSource = '', giftId = store.state.app.currentDanmuType }) {
  return request.post('hmGiftController/sendGift6', {
    splid: store.state.live.liveId,
    giftconst: giftId,
    content,
    gift_source: giftSource,
  });
}

// 发送超级弹幕礼物
export function sendSuperDanmuGift({ content, giftId = store.state.app.currentSuperDanmuType }) {
  return request.post('hmGiftController/buySuperBp', {
    splid: store.state.live.liveId,
    giftconst: giftId,
    title: content,
  });
}

// 发送霸屏礼物
export function sendBapinGift({ content, giftId = store.state.app.currentBapinType }) {
  return request.post('hmGiftController/sendGift6', {
    splid: store.state.live.liveId,
    giftconst: giftId,
    content,
  });
}

// 发送手写签到文字
export function sendBubbleSignText(text) {
  return request.post('hmGiftController/sendHandSign', {
    splid: store.state.live.liveId,
    title: text,
    type: 'hand',
  });
}

// 获取发送礼物排行榜
export function getGiftRankList() {
  return request.post('hmGiftController/findGiftRankList6', {
    splid: store.state.live.liveId,
  });
}

// 购买进场特效
export function buyVipEnterEffect(giftId) {
  return request.post('hmGiftController/buyVipJc', {
    splid: store.state.live.liveId,
    giftconst: giftId,
  });
}

// 修改个人信息
export function editUserInfo(paramObj) {
  return request.post('hmGiftController/editUserInfo', {
    wx_name: paramObj.wx_name,
    avator: paramObj.avator,
    table_number: paramObj.table_number,
    position: paramObj.position,
    type: paramObj.type,
    splid: store.state.live.liveId,
  });
}

// 获取个人信息
export function reqGetUserInfo() {
  return request.get('wxScan/getUserBaseInfo', {});
}

// 签到
export function signIn(paramObj) {
  return request.post('hmScanReportController/qianDao', {
    avator: store.state.user.headImg,
    splid: store.state.live.liveId,
    bless_str: paramObj.wish,
    wx_name: paramObj.name,
  });
}

// 获取男女方发送礼物排行榜
export function getRoleGiftRankList() {
  return request.get(`hmGiftController/findGiftRankList7?splid=${store.state.live.liveId}`);
}

// 提交反馈
export function submitFeedback(paramObj) {
  return request.post('wxScan/commandInfo6', {
    userId: store.state.user.userId,
    content: paramObj.desc,
    phone_number: paramObj.phone,
    reason: paramObj.type,
    splid: store.state.live.liveId,
    piclink: paramObj.imgurl,
  });
}

// 红包口袋充值
export function rechageHbkd(paramObj) {
  return requestMp.post('hmWxmoney/chongZhiRedB', {
    USER_ID: store.state.user.userId,
    splid: store.state.live.liveId,
    openid: store.state.user.openId,
    totalfee: paramObj.total,
  });
}

// 喵钻充值
export function diamondRecharge(paramObj) {
  return requestMp.post('hmWxmoney/chongzhiMiao', {
    userId: store.state.user.userId,
    openid: store.state.user.openId,
    total: paramObj.total,
  });
}

// 抢签到红包
export function robSignHb() {
  return request.post('/hmScanReportController/robSunMoney', {
    splid: store.state.live.liveId,
  });
}

// 送祝福游戏礼物列表
export function getSendGiftGameList() {
  return request.post('/hmGiftController/wishGiftList', {
    splid: store.state.live.liveId,
  });
}

// h5链接直接进入婚宴预定前调用的接口
export function getH5DirectVisitInfo() {
  return request.get('h5UserLogin/getYunJingBaseInfo?type=1');
}

// 获取签到排名
export function getSignRankList() {
  return request.get(`hmGiftController/findGiftRankListAll?splid=${store.state.live.liveId}`);
}

// 获取点歌列表
export function getSongOrderedList() {
  return request.post('hmGiftController/getMusicList', {
    splid: store.state.live.liveId,
  });
}

// 获取顶部飘动的礼物数据
export function getFloatGiftList() {
  return request.post('hmGiftController/piaoGiftList', {
    splid: store.state.live.liveId,
  });
}

// 获取云端的json文件配置
export function getJsonConfig(jsonPath) {
  return axios.get(jsonPath);
}

/**
 * 修改男女方亲友
 * @param {string} type 取值格式 1|2|'' 或者1-1 2-1... 或者 【自定义】
 * @returns
 */
export function reqEditRelatives(type) {
  return request.post('common/updateType', {
    type,
  });
}

/**
 * 获取抽奖机会
 */
export function reqGetSendGiftChance() {
  return request.post('giftLotteryController/getChance', {
    splid: store.state.live.liveId,
  });
}

// 获取签到信息
export function getQianDaoInfo() {
  return request.get(`hmScanReportController/getQianDaoInfo?splid=${store.state.live.liveId}`);
}
```

## File: src/App.vue
```vue
<template>
  <div id="app">
    <router-view />
    <loading v-if="!isInOtherWeviewH5" />
  </div>
</template>
<script>
import { mapMutations, mapState } from 'vuex';
import wxApi from '@/utils/wxApi';
import connectWS from '@/utils/websocket/index';
import { getUrlParam, isEndWithX, timeoutTask } from '@/utils/index';
import {
  formatPhotoTypeList,
  formatDanmuTypeList,
  formatSuperDanmuTypeList,
  formatBapinTypeList,
  getGameInfoByGameCode,
  getSeatPopupFlag,
  updateSeatPopupFlag,
  removeSeatPopupFlag,
} from '@/utils/service';
import {
  getLiveInfo,
  getGiftList,
  getHBKDInfo,
  getGameStatus,
  buyVipEnterEffect,
  editUserInfo,
  sendGift,
  sendBapinGift,
  sendDanmuGift,
  uploadPhoto,
  sendPhotoGift,
  sendGiftCarnival,
  getH5DirectVisitInfo,
} from '@/api/index/index';
import {
  sendGiftMessage, sendBapinGiftMessage, sendDanmuGiftMessage, sendPhotoGiftMessage,
} from '@/api/chat/index';
import { sendDiamondHb } from '@/api/diamondHb/index';
import { POPUP_MODULE, WEBVIEWH5 } from '@/assets/constant/index';
import loading from '@/components/loading/loading.vue';

export default {
  name: 'App',
  components: {
    loading,
  },
  computed: {
    ...mapState({
      isInOtherWeviewH5: (state) => state.app.isInOtherWeviewH5,
      isCloseCoin: (state) => state.app.isCloseCoin,
    }),
  },
  created() {
    // 扫码进入猜红包支付
    if (isEndWithX(window.location.href, 'guessHbPay')) {
      this.setIsInOtherWeviewH5(true);
      this.initGuessHbLogic();
      return;
    }
    this.setToken(getUrlParam('token'));
    this.setLiveId(getUrlParam('liveId'));
    this.setUserPhone(getUrlParam('userPhone'));
    this.setIsHlt(getUrlParam('isHlt'));
    this.setMiniProgramType(getUrlParam('miniProgramType'));
    this.setMpType(getUrlParam('mpType'));
    this.setHotelConfig({
      type: getUrlParam('type'),
      bottom: getUrlParam('bottom'),
      enter: getUrlParam('enter'),
      userphone: getUrlParam('userphone'),
    });
    // 判断是否是在其他webview容器中打开应用或者其他场景直接打开应用页面
    this.setIsInOtherWeviewH5(WEBVIEWH5.some((item) => isEndWithX(window.location.href, item)));
    // 判断执行环境后获取活动信息
    wxApi
      .judgeEnv()
      .then(() => {
        return this.$store.state.app.env;
      })
      .then((rEnv) => {
        if (rEnv === 'h5' && isEndWithX(window.location.href, 'hotelReserve')) {
          // 直接点h5链接进入婚宴预定
          this.initH5HotelReserveLogic();
        } else if (rEnv === 'h5') {
          // h5访问
          wxApi.initWXAPI().then((res) => {
            console.log(res);
          });
        }
        return getLiveInfo();
      })
      .then((res) => {
        console.log('活动信息:', res);
        if (res) {
          this.handleLiveInfo(res);
          // if (this.$store.state.app.env === 'miniProgram' || this.$store.state.app.env === 'tt') {
          //   this.setEnterSceneInfo();
          // }
        }
      })
      .catch((err) => {
        console.log(err);
      });
  },
  mounted() {
    connectWS();
    // 注入svga音频播放脚本支持
    this.insertAudioSupportScript();
  },
  methods: {
    ...mapMutations({
      setToken: 'app/setToken',
      setActivityId: 'live/setActivityId',
      setActivityTitle: 'live/setActivityTitle',
      setActivityIntro: 'live/setActivityIntro',
      setAwardConfig: 'live/setAwardConfig',
      setTotalAward: 'live/setTotalAward',
      setIsCanLottery: 'live/setIsCanLottery',
      setLotterySize0: 'live/setLotterySize0',
      setTotalLotteryPerson: 'live/setTotalLotteryPerson',
      setUserInfo: 'user/setUserInfo',
      setEmceeInfo: 'user/setEmceeInfo',
      setLiveId: 'live/setLiveId',
      setHotelConfig: 'app/setHotelConfig',
      setSceneType: 'live/setSceneType',
      setTitle: 'live/setTitle',
      setBackground: 'live/setBackground',
      togglePopup: 'app/togglePopup',
      setGiftList: 'live/setGiftList',
      setPhotoTypeList: 'live/setPhotoTypeList',
      setCurrentPhotoType: 'app/setCurrentPhotoType',
      setDanmuTypeList: 'live/setDanmuTypeList',
      setCurrentDanmuType: 'app/setCurrentDanmuType',
      setSuperDanmuTypeList: 'live/setSuperDanmuTypeList',
      setCurrentSuperDanmuType: 'app/setCurrentSuperDanmuType',
      setBapinTypeList: 'live/setBapinTypeList',
      setCurrentBapinType: 'app/setCurrentBapinType',
      setRechargeList: 'live/setRechargeList',
      setHbkdRechargeList: 'live/setHbkdRechargeList',
      setHbkdInfo: 'live/setHbkdInfo',
      setQrcodeUrl: 'live/setQrcodeUrl',
      setZyzList: 'live/setZyzList',
      setNynList: 'live/setNynList',
      setCustomSignWish: 'live/setCustomSignWish',
      setOrigin: 'app/setOrigin',
      initRcGiftAtText: 'app/initRcGiftAtText',
      setGiftSendVisible: 'app/setGiftSendVisible',
      setHbkdVisible: 'app/setHbkdVisible',
      setHbkdRemainVisible: 'app/setHbkdRemainVisible',
      setHeartWallPrice: 'app/setHeartWallPrice',
      setEditUserInfoPrice: 'app/setEditUserInfoPrice',
      setIsFreeSendPhoto: 'live/setIsFreeSendPhoto',
      setEmceeId: 'live/setEmceeId',
      setPhotographerWallInfo: 'app/setPhotographerWallInfo',
      setHotelReserveVisible: 'app/setHotelReserveVisible',
      setHotelReserveIcon: 'app/setHotelReserveIcon',
      setIsInOtherWeviewH5: 'app/setIsInOtherWeviewH5',
      setForcePhone: 'live/setForcePhone',
      setIsOverDate: 'live/setIsOverDate',
      setAllFreeSendGift: 'live/setAllFreeSendGift',
      setLogoInfo: 'game/setLogoInfo',
      setIsCloseCoin: 'app/setIsCloseCoin',
      setSeatInfo: 'live/setSeatInfo',
      setUserPhone: 'user/setUserPhone',
      setSeatSearchInfo: 'live/setSeatSearchInfo',
      setIsGiftToHbkd: 'app/setIsGiftToHbkd',
      setIsHlt: 'app/setIsHlt',
      setMiniProgramType: 'app/setMiniProgramType',
      setMpType: 'app/setMpType',
      setHltHotelName: 'app/setHltHotelName',
      setIsBrideVote: 'app/setIsBrideVote',
      setChooseSongVisible: 'app/setChooseSongVisible',
      setSongSheetList: 'app/setSongSheetList',
      setIsForbidSend: 'live/setIsForbidSend',
      setGiveMarkVersion: 'game/setGiveMarkVersion',
      setSignHbConfig: 'app/setSignHbConfig',
      setHbkdRechargeNewList: 'live/setHbkdRechargeNewList',
      setLocationVal: 'live/setLocationVal',
      setIdentitySwitch: 'live/setIdentitySwitch',
      setSwitchFuligoAd: 'app/setSwitchFuligoAd',
      setSwitchContent: 'app/setSwitchContent',
    }),
    setEnterSceneInfo() {
      if (this.$store.state.app.isInOtherWeviewH5) {
        // 其他webview容器打开应用的情况下不需要设置进入场景
        return;
      }
      if (this.$store.state.app.env === 'h5') {
        // h5版互动不需要设置进入场景
        return;
      }
      if (this.$store.state.app.mpType) {
        return;
      }
      // 进入场景
      const origin = getUrlParam('origin');
      if (origin === 'sendGift') {
        if (this.isCloseCoin && localStorage.getItem('tmpGiftId')) {
          sendGift({
            giftId: localStorage.getItem('tmpGiftId'),
          })
            .then((res1) => {
              // 更新 用户余额
              this.setUserInfo({
                money: res1.result.balance,
              });
              return sendGiftMessage({
                giftId: localStorage.getItem('tmpGiftId'),
              }); // 发送礼物的广播
            })
            .then(() => {
              localStorage.removeItem('tmpGiftId');
              this.$toast.center('发送成功!');
            })
            .catch((err) => {
              console.log(err);
            });
        } else {
          // 发礼物
          this.togglePopup(POPUP_MODULE.giftModule.key);
        }
      } else if (origin === 'sendGiftCarnival') {
        if (this.isCloseCoin && localStorage.getItem('tmpGiftId')) {
          sendGiftCarnival({
            giftId: localStorage.getItem('tmpGiftId'),
          })
            .then((res1) => {
              // 更新 用户余额
              this.setUserInfo({
                money: res1.result.balance,
              });
              return sendGiftMessage({
                giftId: localStorage.getItem('tmpGiftId'),
              }); // 发送礼物的广播
            })
            .then(() => {
              localStorage.removeItem('tmpGiftId');
              this.$toast.center('发送成功!');
            })
            .catch((err) => {
              console.log(err);
            });
        } else {
          // 发礼物
          this.togglePopup(POPUP_MODULE.giftModule.key);
        }
      } else if (origin === 'sendBapin') {
        if (this.isCloseCoin && localStorage.getItem('tmpGiftId') && localStorage.getItem('tmpGiftText')) {
          sendBapinGift({
            content: localStorage.getItem('tmpGiftText'),
            giftId: localStorage.getItem('tmpGiftId'),
          })
            .then((res1) => {
              console.log(res1);
              // 更新 用户余额
              this.setUserInfo({
                money: res1.result.balance,
              });
              return sendBapinGiftMessage({
                giftId: localStorage.getItem('tmpGiftId'),
                content: localStorage.getItem('tmpGiftText'),
              }); // 发送礼物的广播
            })
            .then(() => {
              localStorage.removeItem('tmpGiftId');
              localStorage.removeItem('tmpGiftText');
              this.$toast.center('发送成功!');
            })
            .catch((err) => {
              console.log(err);
            });
        } else {
          // 发霸屏
          this.togglePopup(POPUP_MODULE.bapinModule.key);
        }
      } else if (origin === 'sendPhoto') {
        if (
          this.isCloseCoin
          && localStorage.getItem('tmpGiftId')
          && localStorage.getItem('tmpGiftText')
          && localStorage.getItem('tmpGiftPicture')
        ) {
          this.uploadPhoto().then((res1) => {
            console.log(res1);
            return sendPhotoGift({
              imgUrl: res1.filePath,
              giftId: localStorage.getItem('tmpGiftId'),
              content: localStorage.getItem('tmpGiftText'),
            })
              .then((res2) => {
                // 更新 用户余额
                this.setUserInfo({
                  money: res2.result.balance,
                });
                return sendPhotoGiftMessage({
                  giftId: localStorage.getItem('tmpGiftId'),
                  content: localStorage.getItem('tmpGiftText'),
                  imgUrl: res1.filePath,
                }); // 发送礼物的广播
              })
              .then((res3) => {
                console.log(res3);
                localStorage.removeItem('tmpGiftId');
                localStorage.removeItem('tmpGiftText');
                localStorage.removeItem('tmpGiftPicture');
                this.$toast.center('发送成功!');
              })
              .catch((err) => {
                console.log(err);
              });
          });
        } else {
          // 发照片
          this.togglePopup(POPUP_MODULE.photoModule.key);
        }
      } else if (origin === 'sendDanmu') {
        if (this.isCloseCoin && localStorage.getItem('tmpGiftId') && localStorage.getItem('tmpGiftText')) {
          sendDanmuGift({
            giftId: localStorage.getItem('tmpGiftId'),
            content: localStorage.getItem('tmpGiftText'),
          })
            .then((res1) => {
              // 更新 用户余额
              this.setUserInfo({
                money: res1.result.balance,
              });
              return sendDanmuGiftMessage({
                giftId: localStorage.getItem('tmpGiftId'),
                content: localStorage.getItem('tmpGiftText'),
              }); // 发送礼物的广播
            })
            .then(() => {
              this.$toast.center('发送成功!');
              localStorage.removeItem('tmpGiftId');
              localStorage.removeItem('tmpGiftText');
            })
            .catch((err) => {
              console.log(err);
            });
        } else {
          // 发弹幕
          this.togglePopup(POPUP_MODULE.danmuModule.key);
        }
      } else if (origin === 'sendDanmuHby') {
        // 红包雨等待界面发弹幕
        this.$router.push({
          path: '/hby',
        });
        if (this.isCloseCoin && localStorage.getItem('tmpGiftId') && localStorage.getItem('tmpGiftText')) {
          sendDanmuGift({
            content: localStorage.getItem('tmpGiftText'),
            giftId: localStorage.getItem('tmpGiftId'),
          })
            .then((res1) => {
              // 更新 用户余额
              this.setUserInfo({
                money: res1.result.balance,
              });
              return sendDanmuGiftMessage({
                giftId: localStorage.getItem('tmpGiftId'),
                content: localStorage.getItem('tmpGiftText'),
              }); // 发送礼物的广播
            })
            .then(() => {
              this.$toast.center('发送成功!');
              localStorage.removeItem('tmpGiftId');
              localStorage.removeItem('tmpGiftText');
            })
            .catch((err) => {
              console.log(err);
            });
        } else {
          timeoutTask(() => {
            this.togglePopup(POPUP_MODULE.danmuModule.key);
          }, 1000);
        }
      } else if (origin === 'purchaseEnterEffect') {
        const tmpGiftId = localStorage.getItem('tmpGiftId');
        // 购买进场特效
        buyVipEnterEffect(tmpGiftId)
          .then((res) => {
            console.log(res);
            localStorage.removeItem('tmpGiftId');
            if (res.code === '200') {
              this.$toast.center('进场特效购买成功!');
              timeoutTask(() => {
                window.location.reload();
              }, 1000);
            }
          })
          .catch((err) => {
            console.log(err);
          });
      } else if (origin === 'editInfo') {
        const tmpEditInfo = JSON.parse(localStorage.getItem('tmpEditInfo'));
        editUserInfo(tmpEditInfo)
          .then((res) => {
            localStorage.removeItem('tmpEditInfo');
            if (res.code === '200') {
              this.$toast.center('修改成功!');
              this.setUserInfo({
                name: tmpEditInfo.wx_name,
                headImg: tmpEditInfo.avator,
                relativeType: tmpEditInfo.type,
                deskNum: tmpEditInfo.table_number,
                currentStatus: tmpEditInfo.position,
              });
            }
          })
          .catch((err) => {
            console.log(err);
          });
      } else if (origin === 'sendDiamondHb') {
        const tmpSendDiamondHbData = JSON.parse(localStorage.getItem('tmpSendDiamondHbData'));
        sendDiamondHb(tmpSendDiamondHbData)
          .then((res) => {
            console.log(res);
            localStorage.removeItem('tmpSendDiamondHbData');
            // 更新 用户余额
            this.setUserInfo({
              money: res.user.balance,
            });
            this.$toast.center('发送成功!');
          })
          .catch((err) => {
            console.log(err);
            this.$toast.center('发送失败!');
          });
      }
      this.setOrigin('');
    },
    handleLiveInfo(res) {
      // 设置用户信息
      let tempOpenId = res.user.openid;
      if (this.$store.state.app.env === 'h5' && res.user.h5_openid) {
        console.log('设置h5版的openId');
        tempOpenId = res.user.h5_openid;
      }
      this.setUserInfo({
        userId: res.user.USER_ID,
        openId: tempOpenId,
        unionid: res.user.unionid,
        name: res.user.wx_name,
        headImg: res.user.avator,
        money: res.money.balance,
        freeSendGift: res.freeSendGift,
        miao_vip_splid: res.user.miao_vip_splid,
        miao_vip: res.user.miao_vip,
        vipLevel: res.user.vip_level,
        relativeType: res.user.type,
        currentStatus: res.user.position,
        deskNum: res.user.table_number,
        enterEffect: res.user.miao_vip_car,
        isForbidBuyHbq: res.isForBidBuyHbq,
        vip_add_recharge: res.user.vip_add_recharge,
      });
      // 设置司仪信息
      if (res.siyiInfo) {
        this.setEmceeInfo({
          highPrivilege: res.siyiInfo.high_privilege,
          isHideSuper: res.siyiInfo.is_hide_super,
          isUserH5: res.siyiInfo.is_user_h5,
          signShowPhone: res.siyiInfo.sign_show_phone,
          phone_advert_json: res.siyiInfo.phone_advert_json,
          is_open_advert: res.siyiInfo.is_open_advert,
          emcee_name: res.siyiInfo.emcee_name,
          avatar: res.siyiInfo.avator,
          comment_json: res.siyiInfo.comment_json,
          card_json: res.siyiInfo.card_json,
          rank_city: res.siyiInfo.rank_city,
          rank_country: res.siyiInfo.rank_country,
          rank_province: res.siyiInfo.rank_province,
          phonenumber: res.siyiInfo.phonenumber,
          yue_switch: res.siyiInfo.yue_switch,
          unionid: res.siyiInfo.unionid,
        });
        this.setChooseSongVisible(res.siyiInfo.is_open_music);
        if (res.siyiInfo.is_open_music === '1') {
          this.setSongSheetList(res.siyiInfo.musicList);
        }
      }
      // 进场动画
      if (res.user.miao_vip_car) {
        this.$createEnterEffect({
          name: res.user.wx_name,
          headImg: res.user.avator,
          enterEffectType: res.user.miao_vip_car,
        });
      } else {
        this.$createEnterEffect({
          name: res.user.wx_name,
          headImg: res.user.avator,
          enterEffectType: 'common',
        });
      }
      // 设置抽奖活动（幸运大转盘）的id
      if (res.splid && res.splid.activity && res.splid.activity.id) {
        // 保存对应的id
        this.setActivityId(res.splid.activity.id);
      }
      // 保存大转盘抽奖活动的奖项配置数据
      if (res.splid && res.splid.activity && res.splid.activity.prize_json) {
        // 保存抽奖活动的奖项数据
        // 1.将json数据格式进行转化
        const copy = JSON.parse(res.splid.activity.prize_json);
        const target = [];
        // 2.将奖项数据进行存储
        Object.keys(copy).forEach((key) => {
          // 如果key为数字，保存对应索引数据
          if (!Number.isNaN(Number(key))) {
            target.push({ ...copy[key] });
          }
        });
        this.setTotalAward(copy.totalPrizeCount);
        // 3.保存总奖品数量
        this.setAwardConfig(target);
      }
      // 保存大转盘抽奖人数数据
      if (res.splid && res.splid.activity && res.splid.activity.info_json) {
        const copy = JSON.parse(res.splid.activity.info_json);
        // 保存抽到一等奖的人数
        if (copy.lotterySize0) {
          this.setLotterySize0(copy.lotterySize0);
        }
        // 保存抽了奖的总人数
        if (copy.totalSize) {
          this.setTotalLotteryPerson(copy.totalSize);
        }
      }
      // 保存抽奖活动的基本设置
      if (res.splid && res.splid.activity && res.splid.activity.data_json) {
        const copy = JSON.parse(res.splid.activity.data_json);
        const { tips } = copy;
        this.setActivityIntro(tips || '');
      }
      if (res.splid && res.splid.activity && res.splid.activity.title) {
        this.setActivityTitle(res.splid.activity.title);
      }
      // 是否能够抽奖
      if (res.isCanLottery) {
        this.setIsCanLottery(res.isCanLottery);
      }
      // 是否能幸运抽奖
      if (res.sendGiftLotterySwitch) {
        this.$store.commit('live/setSendGiftLotterySwitch', res.sendGiftLotterySwitch);
      }
      // 设置活动信息
      this.setSceneType(res.splid.scenario);
      this.initRcGiftAtText();
      this.setTitle(res.splid.theme);
      this.setBackground(res.splid.phone_piclink);
      this.setQrcodeUrl(res.splid.sp_qrurl);
      this.setGiftSendVisible(res.splid.hide_gift_switch);
      this.setHbkdVisible(res.splid.hide_hbkd_switch);
      this.setHbkdRemainVisible(res.splid.hui_suo_switch);
      this.setIsFreeSendPhoto(res.splid.isFreeSendPhoto);
      this.setEmceeId(res.splid.userId);
      this.setHotelReserveIcon(res.splid.wedding_icon);
      this.setHotelReserveVisible(res.splid.is_show_wedding);
      this.setForcePhone(res.splid.forcephone);
      this.setAllFreeSendGift(res.splid.is_free_send_gift);
      this.setIsCloseCoin(res.splid.is_close_coin);
      this.setIsGiftToHbkd(res.splid.is_gift_to_hbkd);
      this.setIsBrideVote(res.splid.vote_switch);
      this.setIsForbidSend(res.splid.is_forbid_send);
      this.setIsOverDate({
        usingDate: res.splid.using_date,
        isEndWedding: res.splid.is_end_wedding,
      });
      this.setLocationVal(res.splid.location_val);
      this.setIdentitySwitch(res.splid.identity_switch);
      if (res.splid.seatSwitch && res.splid.seatSwitch === '1') {
        this.setSeatInfo(res.splid.seatList);
        if (!getSeatPopupFlag()) {
          this.togglePopup(POPUP_MODULE.seatModule.key);
          updateSeatPopupFlag();
        }
        this.setSeatSearchInfo();
      } else {
        removeSeatPopupFlag();
      }
      // 设置评分游戏版本
      this.setGiveMarkVersion(res.splid.pf_switch);
      // 设置充值列表
      this.setRechargeList(res.miaoBiList);
      this.setHbkdRechargeList(res.redBaoList);
      // 设置幸运大转盘奖项
      this.setZyzList(res.luckyNynList);
      // 设置扭一扭奖项
      this.setNynList(res.nynList);
      // 设置照片墙价格
      this.setHeartWallPrice(res.heart_wall_price);
      // 设置编辑个人信息价格
      this.setEditUserInfoPrice(res.edit_user_price);
      // 设置摄影师照片墙信息
      this.setPhotographerWallInfo({
        photo_shi_switch: res.splid.photo_shi_switch,
        photo_one_price: res.photo_one_price,
      });
      // 设置自定义签到语
      this.setCustomSignWish(res.signWish);
      // 设置logo信息
      if (res.splid.title_piclink) {
        this.setLogoInfo({
          fontColor: res.splid.title_fontcolor,
          fontSize: res.splid.title_fontsize,
          name: res.splid.title_name,
          logoPath: res.splid.title_piclink,
          logoSize: res.splid.picsize,
        });
      }
      // 设置当前婚礼堂酒店名
      this.setHltHotelName(res.splid.hotel_name);
      // 设置红包口袋New列表
      this.setHbkdRechargeNewList(res?.siyiInfo?.hbkd_str);
      // 直接点链接进入婚宴预定的情况取消执行下面的逻辑
      if (this.$store.state.app.env === 'h5' && isEndWithX(window.location.href, 'hotelReserve')) {
        return;
      }
      // 获取game状态
      this.getGameState();
      // 获取礼物列表
      this.getGiftList();
      // 获取红包口袋金额
      this.getHBKDInfo();
      // 获取喵钻红包列表
      this.$store.dispatch('live/getDiamondHbList');
      // 获取签到排名
      this.$store.dispatch('live/getSignRankList');
      // 签到红包
      if (res.is_can_rob_sun === '1') {
        this.togglePopup(POPUP_MODULE.signHbModule.key);
      }

      // 设置不需要文本内容审核的内容列表
      this.$store.commit('live/initNoMsgSeckCheckList');

      // 设置签到红包的配置信息
      if (res.splid && res.splid.sun_info_json) {
        this.setSignHbConfig(JSON.parse(res.splid.sun_info_json));
      }
      // 获取当前位置信息
      if (this.$store.state.live.locationVal) {
        this.$store.dispatch('live/initLocationLogic');
      }
      // 设置福利购广告是否可见
      this.setSwitchFuligoAd({
        fuliSwitch: res.switch_fuligo_jianlai,
        url: res.switch_fuligo_jianlai_url,
      });
      // 设置更多开关
      this.setSwitchContent(res.switch_content);
    },
    handleGiftInfo(res) {
      console.log('*****new gift_list******');
      console.log(res);
      this.setGiftList({
        giftTitleList: res.title,
        giftListObj: res.data,
      });
      // 照片类型列表赋值
      if (res.data.list4) {
        const photoTypeListFormat = formatPhotoTypeList(res.data.list4);
        this.setPhotoTypeList(photoTypeListFormat);
        this.setCurrentPhotoType(photoTypeListFormat[0].giftId);
      }
      // 霸气弹幕类型列表赋值
      const danmuTypeListFormat = formatDanmuTypeList(res.data.list2);
      this.setDanmuTypeList(danmuTypeListFormat);
      this.setCurrentDanmuType(danmuTypeListFormat[0].giftId);

      // 超级弹幕类型列表赋值
      const superDanmuTypeListFormat = formatSuperDanmuTypeList(res.data.list667);
      this.setSuperDanmuTypeList(superDanmuTypeListFormat);
      this.setCurrentSuperDanmuType(superDanmuTypeListFormat[0].giftId);

      //  霸屏类型列表赋值
      const bapinTypeListFormat = formatBapinTypeList(res.data.list3);
      this.setBapinTypeList(bapinTypeListFormat);
      this.setCurrentBapinType(bapinTypeListFormat[0].giftId);
    },
    getGameState() {
      if (this.$store.state.app.isInOtherWeviewH5) {
        // 其他webview容器打开应用的情况下不需要获取进入game状态
        return;
      }
      getGameStatus()
        .then((res) => {
          console.log('game状态:', res);
          if (res.playInfo) {
            const gameBaseInfo = getGameInfoByGameCode(res.playInfo, res?.webSocketData);
            this.$store.commit('game/setGameInfo', {
              currentGameCode: res.playInfo,
              enterType: gameBaseInfo.enterType,
              gameUrl: gameBaseInfo.gameUrl,
              needShake: gameBaseInfo.needShake,
            });
            if (res.status === '0' || res.status === '1') {
              // game等待中
              this.$store.commit('game/setGameStatus', 1);
              // game按钮出现
              if (res.playInfo === 'sign' || res.playInfo === 'hmPlay19') {
                console.log('签到或送祝福游戏无等待界面执行空操作');
              } else {
                this.$store.commit('app/setGameBtnVisible', true);
              }
              // TODO 以后这个地方需要后端优化，或者先在路由的meta中配置，然后这里直接读取meta中的配置生成
              // NOTENEW 新的游戏需要加到这里
              const specialHandleGame = [
                'hmPlay1',
                'hmPlay6',
                'hmPlay7',
                'hmPlay8',
                'hmPlay9',
                'hmPlay11',
                'hmPlay12',
                'hmPlay13',
                'hmPlay17',
                'hmPlay18',
                'hmPlay19',
                'hmPlay20',
                'hmPlay21',
                'hmPlay23',
                'hmPlay24',
                'hmPlay25',
                'hmPlay26',
                'hmPlay27',
                'hmPlay28',
                'hmPlay32',
                'hmPlay33',
                'hmPlay34',
              ];
              if (specialHandleGame.indexOf(res.playInfo) > -1 && res.status === '1') {
                // 狼吞虎咽、红包雨、摇一摇、数钞票、谁最牛、跳一跳、武松打虎、踢足球特殊处理(0表示game等待、1表示game进行中)
                this.$store.commit('game/setGameStatus', 2);
                if (res.playInfo === 'hmPlay19') {
                  this.$store.commit('app/setGameBtnVisible', true);
                  this.togglePopup(16);
                }
              }
            } else if (res.status === '2') {
              this.$store.commit('game/setGameStatus', 2);
            } else if (res.status === '3') {
              this.$store.commit('game/setGameStatus', 3);
              // game按钮消失
              this.$store.commit('app/setGameBtnVisible', false);
            }
          }
        })
        .catch((err) => {
          console.log(err);
        });
    },
    getGiftList() {
      if (this.$store.state.app.isInOtherWeviewH5) {
        // 其他webview容器打开应用的情况下不需要获取礼物列表
        return;
      }
      getGiftList()
        .then((res) => {
          console.log(res);
          this.handleGiftInfo(res);
          if (this.$store.state.app.env === 'miniProgram' || this.$store.state.app.env === 'tt') {
            this.setEnterSceneInfo();
          }
        })
        .catch((err) => {
          console.log(err);
        });
    },
    getHBKDInfo() {
      if (this.$store.state.app.isInOtherWeviewH5) {
        // 其他webview容器打开应用的情况下不需要获取红包口袋金额
        return;
      }
      getHBKDInfo()
        .then((res) => {
          console.log(res);
          this.setHbkdInfo({
            remainMoney: res.money,
          });
        })
        .catch((err) => {
          console.log(err);
        });
    },
    initGuessHbLogic() {
      console.log('初始化猜红包逻辑');
    },
    initH5HotelReserveLogic() {
      console.log('h5直接访问婚宴预定逻辑');
      if (getUrlParam('token')) {
        return;
      }
      if (this.$store.state.app.inWeixinBrowse) {
        window.location.href = `/h5UserLogin/yunJingH51?splid=${getUrlParam('splid')}`;
        return;
      }
      getH5DirectVisitInfo()
        .then((res) => {
          console.log(res);
          window.location = `/?liveId=${getUrlParam('splid')}&token=${res.token}&isHlt=${getUrlParam('isHlt')}&time=${getUrlParam(
            'time',
          )}#/hotelReserve`;
        })
        .catch((err) => {
          console.log(err);
        });
    },
    uploadPhoto() {
      const formData = new FormData();
      const tmpPreviewImg = localStorage.getItem('tmpGiftPicture');
      const arr = tmpPreviewImg.split(',');
      const bstr = atob(arr[1]);
      let n = bstr.length;
      const u8arr = new Uint8Array(n);
      /* eslint-disable */
      while (n--) {
        u8arr[n] = bstr.charCodeAt(n);
      }
      const file = new File([u8arr], 'photo');
      formData.append('file', file);
      formData.append('prefix', 'love');
      return uploadPhoto(formData);
    },
    // 注入svga音频播放脚本支持
    insertAudioSupportScript() {
      const audioSupportScript = document.createElement('script');
      audioSupportScript.src = 'https://static.hudongmiao.com/joymewH5/howler.core.min.js';
      document.getElementsByTagName('head')[0].appendChild(audioSupportScript);
    },
  },
};
</script>
<style>
/* 全局样式 */
* {
  margin: 0;
  padding: 0;
}
body,
html {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

div {
  box-sizing: border-box;
}

#app {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}
</style>
```

## File: src/store/modules/live.js
```javascript
import {
  generateRandomId,
  isEndWithX,
  formatDateConvertTS,
  sCtMs,
  dateCompare,
  getCurrentLocation,
  getDistance,
} from '@/utils/index';
import { WEBVIEWH5 } from '@/assets/constant/index';
import { getSceneInfoBySceneType } from '@/assets/constant/scene';
import { routes } from '@/router/index';
import { getDiamondHbList } from '@/api/diamondHb/index';
import { getSignRankList, reqGetSendGiftChance } from '@/api/index/index';
import { commitBackgroundFileList } from '@/utils/preloadFile';
import { getWishBySceneType, generateQuickWishBySceneType } from '@/utils/service';

import app from './app';
import store from '../index';

const EXAMINELIVID = 'afb94fa7142f43adb3c5dc8bc61d2d9b';
const DZ_HLT_EMCEEID = ['a87b4032a1424e45add71e9e49a139f2', '667b9b5a87ae4c51bd3fd1ec02b1e833'];

const state = {
  liveId: '',
  emceeId: '',
  sceneType: '',
  title: '',
  background: '',
  qrcodeUrl: '',
  giftTitleList: [], // 礼物标题列表
  giftList: [],
  giftListAll: [],
  giftNavId: 'list1',
  rcGiftList: [], // 推荐礼物列表
  giftQueue: [], // 礼物队列
  currentGiftEffect: {
    // 当前展示的礼物效果
    id: '',
    path: '',
    imgPath: '',
    giftName: '',
    userName: '',
    headImg: '',
  },
  photoTypeList: [], // 照片类型列表
  danmuTypeList: [], // 霸气弹幕类型列表
  bapinTypeList: [], // 霸屏类型列表
  superDanmuTypeList: [], // 超级弹幕类型列表
  rechargeList: [], // 充值列表
  hbkdRechargeList: [], // 红包口袋充值列表
  hbkdRechargeNewList: [], // 新版红包口袋充值列表
  remainMoney: 0, // 红包口袋余额
  zyzList: '',
  nynList: '',
  isFreeSendPhoto: false, // 是否是免费发照片礼物场次
  diamondHbQueue: [], // 喵钻红包队列
  diamondHbCdp: {
    // 当前展示的喵钻红包
    id: '',
    diamondNum: 0,
    wx_name: '',
    avator: '',
    startTime: '', // 红包可点时间
    hbCd: '',
    status: 0, // 0:不可点(倒计时中) 1:可点 2:点开
    diamondNumLucky: 0, // 抢到的喵钻数量
    isPrize: false, // 是否抢到喵钻
  },
  isOpenDiamondHb: false, // 正在开红包
  isExamineLive: false, // 是否是应付审核的活动
  customSignWish: [], // 自定义签到语
  isForcePhone: false, // 是否强制获取手机号
  isOverDate: false, // 活动是否过期
  allFreeSendGift: false, // 全场免费发礼物
  seatSwitch: false, // 席位表功能是否开启
  seatList: [],
  seatSearchList: [],
  seatMy: '',
  noMsgSeckCheckList: [], // 不需要文本内容安全检测的文本
  advertiseDanmuTypeList: [], // 所有的广告弹幕类型列表(跟司仪账号有关)
  advertiseDanmuTypeQueue: [], // 待发送的广告弹幕类型队列(跟这场活动有关)
  activityId: '', // 幸运大转盘的id
  activityTitle: '', // 大转盘活动名称
  activityIntro: '', // 大转盘活动简介
  awardConfig: [], // 幸运大转盘配置的奖项数据
  totalAward: 0, // 幸运大转盘所有奖品数量
  lotterySize0: 0, // 幸运大转盘抽到一等奖的人数
  totalLotteryPerson: 0, // 幸运大转盘已经抽奖的人数
  isCanLottery: '1', // 是否可以进行抽奖, '1'不弹窗
  hotelTel: '', // 酒店电话
  signRankList: [], // 签到排名列表
  signRankListSize: 0, // 签到排名列表总数
  myRankNum: '99+', // 我的排名
  isForbidSend: false, // 禁止自定义文本内容
  locationVal: '', // 地理位置配置信息
  isLocationInvalid: false, // 地理位置信息是否非法 默认合法
  locationInvalidReason: '', // 地理位置非法原因
  identitySwitch: false, // 亲友设置开关
  sendGiftLotteryNum: 0, // 发送礼物抽奖次数
  sendGiftLotterySwitch: false, // 发送礼物抽奖开关
  dz_hltcard: false, // 定制婚礼堂小程序卡片
};

const mutations = {
  setHotelTel: (state, data) => {
    state.hotelTel = data;
  },
  setLotterySize0: (state, data) => {
    state.lotterySize0 = data;
  },
  setActivityTitle: (state, data) => {
    state.activityTitle = data;
  },
  setActivityIntro: (state, data) => {
    state.activityIntro = data;
  },
  setIsCanLottery: (state, data) => {
    state.isCanLottery = data;
  },
  setTotalLotteryPerson: (state, data) => {
    state.totalLotteryPerson = data;
  },
  setTotalAward: (state, data) => {
    state.totalAward = data;
  },
  setActivityId: (state, data) => {
    state.activityId = data;
  },
  setAwardConfig: (state, data) => {
    state.awardConfig.splice(0);
    state.awardConfig = data;
  },
  setLiveId: (state, data) => {
    state.liveId = data;
    if (state.liveId === EXAMINELIVID) {
      state.isExamineLive = true;
    }
  },
  setEmceeId: (state, data) => {
    state.emceeId = data;
    if (DZ_HLT_EMCEEID.includes(state.emceeId)) {
      state.dz_hltcard = true;
    }
  },
  setSceneType: (state, data) => {
    console.log('***setSceneType***');
    console.log(data);
    state.sceneType = data;
  },
  setZyzList: (state, data) => {
    state.zyzList = data;
  },
  setNynList: (state, data) => {
    state.nynList = data;
  },
  setTitle: (state, data) => {
    state.title = data;
    routes[0].meta.title = state.title;
    routes[1].meta.title = state.title;
    const tmpFlag = WEBVIEWH5.some((item) => isEndWithX(window.location.href, item));
    if (!tmpFlag) {
      document.title = state.title;
    }
  },
  setBackground: (state, data) => {
    let tmpBg = '';
    // state.background = data || state.background;
    if (data && data !== '0') {
      tmpBg = data;
    } else {
      const tmpSceneInfo = getSceneInfoBySceneType(state.sceneType);
      tmpBg = tmpSceneInfo && tmpSceneInfo.bg;
    }
    state.background = tmpBg;
    commitBackgroundFileList({
      path: state.background,
      type: 'img',
    });
  },
  setGiftList: (state, data) => {
    const NAVMAP = {
      list1: '经典',
      list5: '华丽',
      list666: '特效',
      list6: '嘉年华',
    };
    // data.giftTitleList<-> {list1: '',list5: '',...}
    const keyArr = Object.keys(data.giftTitleList);
    // 嘉年华礼物调整到第二个位置
    const tmpIndexList6 = keyArr.indexOf('list6');
    const valIndex1 = keyArr[1];
    let tempVal;
    if (tmpIndexList6 > -1 && valIndex1) {
      tempVal = keyArr[tmpIndexList6];
      keyArr[tmpIndexList6] = valIndex1;
      keyArr[1] = tempVal;
    }
    const tmpTitle = [];
    const tmpList = [];
    let tmpListAll = [];
    keyArr.forEach((keyItem) => {
      if (data.giftListObj[keyItem].length > 0) {
        tmpTitle.push({
          id: keyItem,
          name: NAVMAP[keyItem],
        });
        tmpList.push(data.giftListObj[keyItem]);
        tmpListAll = tmpListAll.concat(data.giftListObj[keyItem]);
      }
    });
    // 中式婚礼不需要发红包
    if (state.sceneType !== '91') {
      tmpTitle.push({
        id: 'sendHb',
        name: '红包',
      });
    }
    // 非婚礼版、同庆楼版本、婚礼堂版本去掉特效
    if (state.sceneType !== '0' || store.getters['user/isTql'] || store.state.user.emceeInfo.highPrivilege === 5) {
      const tmpEnterEffectIndex = tmpTitle.findIndex((item) => item.id === 'list666');
      tmpTitle.splice(tmpEnterEffectIndex, 1);
      tmpList.splice(tmpEnterEffectIndex, 1);
    }
    state.giftTitleList = tmpTitle;
    state.giftList = tmpList;
    state.giftListAll = tmpListAll;
    const tmpJdGiftIndex = tmpTitle.findIndex((item) => item.id === 'list1'); // 经典礼物索引
    state.rcGiftList = state.giftList[tmpJdGiftIndex]
      .filter((item) => {
        return item.is_pop === '1';
      })
      .map((item) => {
        return {
          giftImg: item.imglink,
          giftName: item.giftname,
          price: item.giftprice,
          giftId: item.giftconst,
        };
      });
    store.commit('app/setCurrentGiftType', state.giftList[0][0].giftconst);
  },
  setGiftNavId: (state, data) => {
    state.giftNavId = data;
  },
  setPhotoTypeList: (state, data) => {
    state.photoTypeList = data;
  },
  setDanmuTypeList: (state, data) => {
    state.danmuTypeList = data;
  },
  setSuperDanmuTypeList: (state, data) => {
    state.superDanmuTypeList = data;
  },
  setBapinTypeList: (state, data) => {
    state.bapinTypeList = data;
  },
  setRechargeList: (state, data) => {
    state.rechargeList = data.split(',');
  },
  setHbkdRechargeList: (state, data) => {
    state.hbkdRechargeList = data;
  },
  setHbkdRechargeNewList: (state, data) => {
    if (!data || data === '0') {
      return;
    }
    try {
      const tmpHbkdObj = JSON.parse(data);
      // 旧版数据结构 废弃
      // {id,title,value:{[sceneType]:[]}}
      if (tmpHbkdObj.value && typeof tmpHbkdObj.value === 'object') {
        state.hbkdRechargeNewList = [];
      } else {
        // 新版数据结构
        // {[sceneType]: {id,title,value:[]}}
        state.hbkdRechargeNewList = tmpHbkdObj[state.sceneType]?.value ?? [];
      }
    } catch (err) {
      console.log(err);
    }
  },
  setHbkdInfo: (state, data) => {
    state.remainMoney = data.remainMoney;
  },
  addToGiftQueue: (state, data) => {
    if (state.currentGiftEffect.id === '') {
      state.currentGiftEffect = {
        id: generateRandomId(),
        path: data.coupontype,
        imgPath: data.imglink,
        giftName: data.giftname,
        userName: data.userName,
        headImg: data.headImg,
        shijian: data.shijian,
        miaoColor: data.miaoColor,
      };
    } else {
      const list = state.giftQueue;
      list.push(data);
      state.giftQueue = list;
    }
  },
  removeFromGiftQueue: (state) => {
    const list = state.giftQueue;
    if (list.length === 0) {
      state.currentGiftEffect = {
        id: '',
        path: '',
        imgPath: '',
        giftName: '',
        userName: '',
        headImg: '',
        shijian: '',
        miaoColor: '',
      };
    } else {
      const g = list.shift();
      state.giftQueue = list;
      state.currentGiftEffect = {
        id: generateRandomId(),
        path: g.coupontype,
        imgPath: g.imglink,
        giftName: g.giftname,
        userName: g.userName,
        headImg: g.headImg,
        shijian: g.shijian,
        miaoColor: g.miaoColor,
      };
    }
  },
  setQrcodeUrl: (state, data) => {
    state.qrcodeUrl = data;
  },
  setIsFreeSendPhoto: (state, data) => {
    if (data === true || data === false) {
      state.isFreeSendPhoto = data;
    }
  },
  // 更新喵钻红包队列
  updateDiamondHbQueue: (state, data) => {
    state.diamondHbQueue.splice(0);
    const tmpLen = data.length;
    for (let i = 0; i < tmpLen; i += 1) {
      if (data[i].isRobRedPackage === '0') {
        state.diamondHbQueue.push({
          id: data[i].package_id,
          diamondNum: data[i].send_money,
          wx_name: data[i].wx_name,
          avator: data[i].avator,
          startTime: formatDateConvertTS(data[i].start_time),
          hbCd: '',
          status: 0,
        });
      }
    }
    // 执行倒计时逻辑
    if (state.diamondHbQueue[0]) {
      store.commit('live/updateHeadDiamondHbCd');
    }
  },
  // 更新喵钻红包队列队首红包的cd时间
  updateHeadDiamondHbCd: (state) => {
    const { startTime } = state.diamondHbQueue[0];
    let subSecond = parseInt((startTime - new Date().getTime()) / 1000, 10); // 时间差
    if (subSecond >= 0) {
      const tmpInterval = setInterval(() => {
        subSecond = parseInt((startTime - new Date().getTime()) / 1000, 10);
        if (subSecond > 0) {
          state.diamondHbQueue[0].hbCd = sCtMs(subSecond);
        } else {
          clearInterval(tmpInterval);
          state.diamondHbQueue[0].status = 1;
          state.diamondHbQueue[0].hbCd = '';
        }
      }, 1000);
    } else {
      // 红包变成可点状态
      state.diamondHbQueue[0].status = 1;
    }
  },
  // 更新当前展示的喵钻红包
  updateDiamondHbCdp: (state, data) => {
    const tmpDiamondHb = state.diamondHbQueue[0];
    if (tmpDiamondHb) {
      state.diamondHbCdp.id = tmpDiamondHb.id;
      state.diamondHbCdp.diamondNum = tmpDiamondHb.diamondNum;
      state.diamondHbCdp.wx_name = tmpDiamondHb.wx_name;
      state.diamondHbCdp.avator = tmpDiamondHb.avator;
      state.diamondHbCdp.startTime = tmpDiamondHb.startTime;
      state.diamondHbCdp.hbCd = tmpDiamondHb.hbCd;
      state.diamondHbCdp.status = tmpDiamondHb.status;
    }
    // 抢到的喵钻数目、是否中奖赋值
    if (data) {
      state.diamondHbCdp.diamondNumLucky = data.gold;
      if (data.status === 1) {
        state.diamondHbCdp.isPrize = true;
      } else {
        state.diamondHbCdp.isPrize = false;
      }
    }
  },
  // 更新当前展示的喵钻红包状态
  updateDiamondHbCdpStatus: (state, data) => {
    state.diamondHbCdp.status = data;
  },
  setIsOpenDiamondHb: (state, data) => {
    state.isOpenDiamondHb = data;
  },
  setCustomSignWish: (state, data) => {
    if (data && data.length > 0) {
      state.customSignWish = data;
    }
  },
  setForcePhone: (state, data) => {
    if (state.sceneType === '1' || state.sceneType === '0') {
      let tmpFlag = false;
      if (data === '1') {
        tmpFlag = true;
      }
      state.isForcePhone = tmpFlag;
    }
  },
  setIsOverDate: (state, data) => {
    if (dateCompare(data.usingDate) || data.isEndWedding === '1') {
      state.isOverDate = true;
    } else {
      state.isOverDate = false;
    }
  },
  setAllFreeSendGift: (state, data) => {
    // 字节小程序环境默认全场免费发礼物
    if (app.state.env === 'tt') {
      state.allFreeSendGift = true;
      return;
    }
    if (data === '0' || data === '1') {
      if (data === '0') {
        state.allFreeSendGift = false;
      } else if (data === '1') {
        state.allFreeSendGift = true;
      }
    }
  },
  setSeatInfo: (state, data) => {
    if (data && data.length > 0) {
      state.seatSwitch = true;
      state.seatList = data.map((item) => {
        const tmpUserList = item.seat_val.split(',').filter((item) => item);
        const tmpLen = tmpUserList.length;
        for (let i = 0; i < tmpLen; i += 1) {
          if (tmpUserList[i].indexOf('_') > -1) {
            [tmpUserList[i]] = tmpUserList[i].split('_');
          }
        }
        return {
          userList: item.seat_val.split(',').filter((item) => item),
          userListReal: tmpUserList,
          ...item,
        };
      });
    }
  },
  setSeatSearchInfo: (state, data) => {
    if (data) {
      const targetSeat = state.seatList.find((item) => item.seat_val.indexOf(data.namephone) > -1);
      if (targetSeat) {
        state.seatSearchList = targetSeat.userListReal;
        state.seatMy = targetSeat.seat_number;
      }
    } else if (store.state.user.userPhone) {
      const targetSeat = state.seatList.find((item) => item.seat_val.indexOf(store.state.user.userPhone) > -1);
      if (targetSeat) {
        state.seatSearchList = targetSeat.userListReal;
        state.seatMy = targetSeat.seat_number;
      }
    } else if (store.state.user.name) {
      const targetSeat = state.seatList.find((item) => item.seat_val.indexOf(store.state.user.name) > -1);
      if (targetSeat) {
        state.seatSearchList = targetSeat.userListReal;
        state.seatMy = targetSeat.seat_number;
      }
    } else {
      state.seatSearchList = [];
      state.seatMy = '';
    }
    if (state.seatMy) {
      localStorage.setItem('seatMy', state.seatMy);
      localStorage.setItem('seatSearchList', JSON.stringify(state.seatSearchList));
    } else {
      state.seatMy = localStorage.getItem('seatMy') || '';
      const tmpLsListStr = localStorage.getItem('seatSearchList');
      if (tmpLsListStr) {
        state.seatSearchList = JSON.parse(tmpLsListStr);
      } else {
        state.seatSearchList = [];
      }
    }
  },
  initNoMsgSeckCheckList: (state) => {
    if (state.noMsgSeckCheckList.length > 0) {
      return;
    }
    const tmpWishList = getWishBySceneType(state.sceneType, 'list');
    const tmpWishListCustom = state.customSignWish;
    const tmpQuickWishList = generateQuickWishBySceneType(state.sceneType, 'list');
    state.noMsgSeckCheckList = tmpWishList.concat(tmpWishListCustom).concat(tmpQuickWishList);
  },
  resetAdvertiseDanmuTypeQueue: (state) => {
    // h5刷新都能重新发送(提高广告弹幕发送频次，如果嫌频次过多则使用上面注释掉的逻辑)
    localStorage.removeItem('advertiseDanmuStorage');
    // state.advertiseDanmuTypeQueue = state.advertiseDanmuTypeList;
    state.advertiseDanmuTypeList.forEach((typeItem) => {
      if (typeItem.switch === '1') {
        state.advertiseDanmuTypeQueue.push(typeItem);
      }
    });

    console.log('初始化待发送的广告类型队列', state.advertiseDanmuTypeQueue);
  },
  setSignRankList: (state, data) => {
    if (data && data.length > 0) {
      const getTypeLabel = (type) => {
        if (!type) {
          return '';
        }
        return type.startsWith('1') ? '男方' : '女方';
      };
      state.signRankList = data.map((dataItem) => {
        return {
          ...dataItem,
          money: parseInt(dataItem.money, 10),
          positionName: getTypeLabel(dataItem.position),
        };
      });
      const myIndex = state.signRankList.findIndex((item) => item.userId === store.state.user.userId);
      if (myIndex > -1) {
        state.myRankNum = myIndex + 1;
      }
    }
  },
  setSignRankListSize: (state, data) => {
    if (data) {
      state.signRankListSize = parseInt(data, 10);
    }
  },
  setIsForbidSend: (state, data) => {
    if (data === '1' || data === '0') {
      state.isForbidSend = data === '1';
    }
  },
  setLocationVal: (state, data) => {
    if (!data || data === '0') {
      return;
    }
    try {
      const locationObj = JSON.parse(data);
      const { lat, lng } = locationObj;
      if (lat && lng) {
        state.locationVal = locationObj;
      }
    } catch (err) {
      console.log(err);
    }
  },
  setIsLocationInvalid: (state, data) => {
    state.isLocationInvalid = data;
  },
  setLocationInvalidReason: (state, data) => {
    state.locationInvalidReason = data;
  },
  setIdentitySwitch: (state, data) => {
    state.identitySwitch = data === '1';
  },
  /**
   * 设置抽奖次数
   */
  setSendGiftLotteryNum: (state, data) => {
    state.sendGiftLotteryNum = data;
  },
  /**
   * 设置抽奖开关
   */
  setSendGiftLotterySwitch: (state, data) => {
    state.sendGiftLotterySwitch = data === '1';
  },
};

const actions = {
  getDiamondHbList(ctx) {
    getDiamondHbList()
      .then((res) => {
        console.log(res);
        ctx.commit('updateDiamondHbQueue', res.inList);
      })
      .catch((err) => {
        console.log(err);
      });
  },
  getSignRankList(ctx) {
    getSignRankList()
      .then((res) => {
        console.log(res);
        ctx.commit('setSignRankList', res.list1);
        ctx.commit('setSignRankListSize', res.size);
      })
      .catch((err) => {
        console.log(err);
      });
  },
  // locationVal有值的情况下调用该方法
  initLocationLogic(ctx) {
    getCurrentLocation()
      .then((res) => {
        console.log(res);
        const { latitude: currentLatitude, longitude: currentLongitude } = res;
        const { lat: locationLatitude, lng: locationLongitude, scope } = ctx.state.locationVal;
        const currentDistance = getDistance(currentLatitude, currentLongitude, locationLatitude, locationLongitude);
        console.log(currentDistance, scope);
        if (currentDistance > scope) {
          ctx.commit('setIsLocationInvalid', true);
          ctx.commit('setLocationInvalidReason', '您不在活动范围内!');
        }
      })
      .catch((err) => {
        console.log(err);
        ctx.commit('setIsLocationInvalid', true);
        ctx.commit('setLocationInvalidReason', '手机未开启定位服务权限!');
      });
  },
  /**
   * 请求接口获取发礼物抽奖次数
   * 如果次数不为0则显示抽奖次数弹窗
   * 自己发了礼物调用
   */
  getSendGiftLotteryNumFromServer(ctx) {
    return new Promise((resolve, reject) => {
      reqGetSendGiftChance().then((res) => {
        console.log('抽奖机会有无?', res);
        const remainChance = parseInt(res.size, 10);
        ctx.commit('setSendGiftLotteryNum', remainChance);
        resolve(remainChance);
      }).catch((err) => {
        console.log(err);
        reject(err);
      });
    });
  },
};

const getters = {
  signRankListTopThree(state) {
    return state.signRankList.slice(0, 3);
  },
};

export default {
  namespaced: true,
  state,
  mutations,
  actions,
  getters,
};
```

## File: src/utils/hdOptimizationTmpPatch.js
```javascript
import store from '@/store/index';

/**
 * 新旧url映射对象
 * {
 *   页面名称: {
 *     'old': pageInfo-a,
 *     'new': pageInfo-b
 *   }
 * }
 *
 * pageInfo: string | object
 *     string: 页面路径
 *     object: 多个页面路径、根据具体业务选择对应的页面地址
 *
 */
export const URL_MAP = {
  recharge: {
    old: {
      wedding: '/pages/recharge2/recharge2',
      other: '/pages/recharge/recharge',
    },
    new: {
      wedding: '/packageA/pages/rechargeWedding/rechargeWedding',
      other: '/packageA/pages/recharge/recharge',
    },
  },
  hbkdRecharge: {
    old: {
      template: '/pages/hbkdRechargeNew/hbkdRechargeNew',
      other: '/pages/hbkdRecharge/hbkdRecharge',
    },
    new: '/packageA/pages/hbkdRecharge/hbkdRecharge',
  },
};

/**
 * 调整游戏地址
 * @param {Object} gameInfo
 * gameInfo: {
 *   enterType: 'h5' | 'mp',
 *   gameUrl: string,
 *   needShake: boolean
 * }
 * @returns {void}
 * @description 调整gameInfo中的gameUrl
 */
export const tmpAdjustGameUrl = (gameInfo) => {
  const { gameUrl: oldGameUrl } = gameInfo;
  const newGameUrl = `/packageGame${oldGameUrl}`;
  gameInfo.gameUrl = newGameUrl;
};

/**
 * 对象转queryParam
 * {a:1,b:2,c:3} => a=1&b=2&c=3
 * @returns {string}
 */
const objectToQueryParam = (obj) => {
  return Object.keys(obj).map((key) => `${key}=${obj[key]}`).join('&');
};

/**
 * 根据业务参数得到页面信息类型
 * @returns {'wedding' | 'other' | 'template'}
 */
const getPageInfoTypeByService = (pageName, queryObj, options) => {
  if (pageName === 'recharge') {
    const { sceneType, isTql } = options;
    if (sceneType === '0' && !isTql) {
      return 'wedding';
    }
    return 'other';
  }
  if (pageName === 'hbkdRecharge') {
    const { templateMode } = queryObj;
    if (templateMode) {
      return 'template';
    }
    return 'other';
  }
  return undefined;
};

/**
 * 获取新的url
 * @param {String} pageName 页面名称
 * @param {Object} queryObj 跳转页面携带的参数
 */
export const tmpGetNewUrl = (pageName, queryObj) => {
  let targetPath;
  // 1、从URL_MAP中得到页面信息
  const isHltValid = store.state.app.isHlt;
  const pageInfo = store.state.app.mpType || isHltValid ? URL_MAP[pageName].new : URL_MAP[pageName].old;

  // 2、逻辑分支：页面信息的类型是对象还是字符串
  if (typeof pageInfo === 'string') {
    // 如果是字符串 直接作为目标路径
    targetPath = pageInfo;
  } else {
    // 如果是对象 根据页面名称、业务参数获取到对应的页面信息类型
        const pageInfoType = getPageInfoTypeByService(pageName, queryObj, {
          sceneType: store.state.live.sceneType,
          isTql: store.getters['user/isTql'],
        });
    // 根据类型得到目标路径
    targetPath = pageInfo[pageInfoType];
  }
  // 3、拼接路径和参数得到最终跳转地址
  return `${targetPath}?${objectToQueryParam(queryObj)}`;
};
```

## File: src/utils/websocket/handleMessage.js
```javascript
import Vue from 'vue';
import store from '@/store/index';
// import { generateRandomId, getCurrentDate } from '@/utils/index';
import { getGameInfoByGameCode } from '@/utils/service';
import router from '@/router/index';
// import { CHATICON, CHATICON_ZSHL, getRelativeTypeLabel } from '@/assets/constant/index';

// function getGiftImg(type, miaoLiwuId) {
//   let giftImg;
//   if (store.state.live.sceneType === '91') {
//     const XR_DANMUS = [
//       'https://ustatic.joymew.com/joymewMp/zshl/danmu/dragonIcon.png',
//       'https://ustatic.joymew.com/joymewMp/zshl/danmu/phonixIcon.png',
//       'https://ustatic.joymew.com/joymewMp/zshl/danmu/sklinIcon.png',
//     ];
//     if (miaoLiwuId?.includes('Miao_Bq')) {
//       const targetNum = Number(miaoLiwuId.split('_')[2]);
//       giftImg = XR_DANMUS[targetNum - 1];
//     } else {
//       giftImg = CHATICON_ZSHL[type];
//     }
//   } else {
//     giftImg = CHATICON[type];
//   }
//   return giftImg;
// }

// function getGiftName(miaoLiwuId) {
//   const DANMU_NAME = ['飞龙在天', '有凤来仪', '麒麟送子'];
//   const targetNum = Number(miaoLiwuId.split('_')[2]);
//   return DANMU_NAME[targetNum - 1];
// }

// function getTargetUserName(miaoName) {
//   let cutLen;
//   if (store.state.live.sceneType === '0') {
//     cutLen = 9;
//   } else {
//     cutLen = 18;
//   }
//   return miaoName.length > cutLen ? `${miaoName.slice(0, cutLen)}...` : miaoName;
// }
/**
 * 如果是本人发送的礼物需要将发礼物弹窗关闭
 * @param {string} userId 礼物发送者的id
 */
function closePopupWhenSelf(userId) {
  if (store.state.user.userId === userId && store.state.app.popupAreaVisible) {
    store.commit('app/togglePopup');
  }
}
/**
 * 如果是本人发的礼物需要判断有没有抽奖机会
 * 排除免费发礼物的情况
 * 排序发礼物抽奖功能关闭的情况
 * 只限于互动小程序
 */
function checkLotteryChanceWhenSelf(userId) {
  if (!store.state.live.sendGiftLotterySwitch) {
    return;
  }
  if (store.state.user.freeSendGift || store.state.live.allFreeSendGift) {
    return;
  }
  if (!['haimao', 'ledong', 'haimiao'].includes(store.state.app.mpType)) {
    return;
  }

  if (store.state.user.userId === userId) {
    store.dispatch('live/getSendGiftLotteryNumFromServer').then((remainChance) => {
      console.log('剩余抽奖次数:', remainChance);
      if (remainChance > 0) {
        // 弹出引导抽奖的弹窗
        store.commit('app/togglePopup', 20);
      }
    });
  }
}

// 处理聊天消息
function handleChatMessage(message) {
  // if (!message.data.miaoLwId && !message.data.miaoBless) {
  //   // 无效消息不作处理
  //   return;
  // }
  // const resultGiftInfo = {
  //   giftName: '',
  //   giftType: '',
  //   giftImg: '',
  // };
  // if (message.data.miaoLwId) {
  //   if (message.data.miaoLwId.indexOf('Miao_Bp') > -1) {
  //     resultGiftInfo.giftName = '祝福横幅';
  //     resultGiftInfo.giftType = 'bapin';
  //     resultGiftInfo.giftImg = getGiftImg('bapin');
  //   } else if (message.data.miaoLwId.indexOf('Miao_Tp') > -1) {
  //     resultGiftInfo.giftName = '照片霸屏';
  //     resultGiftInfo.giftType = 'photo';
  //     resultGiftInfo.giftImg = getGiftImg('photo');
  //   } else if (message.data.miaoLwId.indexOf('Miao_Bq') > -1) {
  //     resultGiftInfo.giftName = store.state.live.sceneType === '91' ? getGiftName(message.data.miaoLwId) : '火箭弹幕';
  //     resultGiftInfo.giftType = 'rocket';
  //     resultGiftInfo.giftImg = getGiftImg('rocket', message.data.miaoLwId);
  //   } else if (message.data.miaoLwId.indexOf('Miao_SuperDanmu') > -1) {
  //     resultGiftInfo.giftName = '超级霸屏';
  //     resultGiftInfo.giftType = 'superDanmu';
  //     resultGiftInfo.giftImg = getGiftImg('superDanmu');
  //   } else if (message.data.miaoLwId === 'hbkd') {
  //     resultGiftInfo.giftName = `${message.data.miaoBless}元红包`;
  //     resultGiftInfo.giftType = 'hbkd';
  //     resultGiftInfo.giftImg = getGiftImg('hbkd');
  //     message.data.miaoBless = '';
  //   } else if (message.data.miaoLwId === 'Miao_PhotoWall') {
  //     resultGiftInfo.giftName = `${message.data.miaoBless}元红包`;
  //     resultGiftInfo.giftType = 'photoWall';
  //     resultGiftInfo.giftImg = getGiftImg('photoWall');
  //     message.data.miaoBless = '';
  //   } else if (currentGift) {
  //     resultGiftInfo.giftName = currentGift.giftname;
  //     resultGiftInfo.giftType = 'gift';
  //     resultGiftInfo.giftImg = currentGift.imglink;
  //   }
  // }
  // store.commit('live/addChat', {
  //   id: generateRandomId(),
  //   headImg: message.data.miaoHeadUrl,
  //   content: message.data.miaoBless,
  //   userName: getTargetUserName(message.data.miaoName),
  //   photoUrl: message.data.miaoTuUrl,
  //   miaoVip: store.state.live.liveId === message.data.miaoVipSplid ? message.data.miaoVip : '',
  //   vipLevel: message.data.miaoVipLevel,
  //   relativeType: message.data.miaoType,
  //   relativeTypeLabel: getRelativeTypeLabel(message.data.miaoType),
  //   currentStatus: message.data.miaoPosition,
  //   deskNum: message.data.miaoTableNumber,
  //   sendDate: getCurrentDate(),
  //   ...resultGiftInfo,
  // });
  store.commit('chat/addChat', message.data);
}
// 处理礼物相关的消息
function handleGiftMessage(message) {
  console.log('礼物消息:', message);
  if (message.data.miaoLwId.indexOf('Miao_Bq') > -1) {
    // 火箭弹幕
    let tmpRocketType;
    if (message.data.miaoLwId.indexOf('Miao_Bq_2') > -1) {
      tmpRocketType = 1;
    } else if (message.data.miaoLwId.indexOf('Miao_Bq_3') > -1) {
      tmpRocketType = 2;
    } else {
      tmpRocketType = 0;
    }
    Vue.prototype.$createRocketDanmu({
      name: message.data.miaoName,
      headImg: message.data.miaoHeadUrl,
      content: message.data.miaoBless,
      rocketType: tmpRocketType,
    });
    // handleChatMessage(message);
  } else if (message.data.miaoLwId.indexOf('Miao_Bp') > -1) {
    // 祝福横幅
    let tmpBapinType;
    const bapinTList = store.state.live.bapinTypeList;
    const bapinTListLen = bapinTList.length;
    for (let i = 0; i < bapinTListLen; i += 1) {
      if (bapinTList[i].giftId === message.data.miaoLwId) {
        tmpBapinType = i;
        break;
      }
    }
    const tmpTime = parseInt(bapinTList[tmpBapinType].shijian, 10);
    Vue.prototype.$createLoveBapin({
      name: message.data.miaoName,
      headImg: message.data.miaoHeadUrl,
      content: message.data.miaoBless,
      bapinType: tmpBapinType,
      time: tmpTime,
    });
    // handleChatMessage(message);
  } else if (message.data.miaoLwId.indexOf('Miao_Tp') > -1) {
    // 照片
    // handleChatMessage(message);
  } else if (message.data.miaoLwId.indexOf('Miao_SuperDanmu') > -1) {
    // 超级弹幕
    // handleChatMessage(message);
  } else if (message.data.miaoLwId.indexOf('hbkd') > -1) {
    // 红包口袋充值
    // handleChatMessage(message);
  } else if (message.data.miaoLwId.indexOf('Miao_PhotoWall') > -1) {
    // 红包墙
    // handleChatMessage(message);
  } else {
    // 普通礼物
    const tmpGift = store.state.live.giftListAll.find((item) => item.giftconst === message.data.miaoLwId);
    // handleChatMessage(message, tmpGift);
    store.commit('live/addToGiftQueue', {
      userName: message.data.miaoName,
      headImg: message.data.miaoHeadUrl,
      miaoColor: message.data.miaoColor,
      ...tmpGift,
    });
  }
  // 如果是本人发送的礼物需要将发礼物弹窗关闭
  closePopupWhenSelf(message.data.miaoId);
  // 只有重构后的互动小程序才可以执行此逻辑
  if (store.state.app.mpType) {
    // 如果是本人发送的礼物需要判断有没有抽奖机会
    checkLotteryChanceWhenSelf(message.data.miaoId);
  }
}
// 处理game相关的消息
function handleGameMessage(message) {
  const gameBaseInfo = getGameInfoByGameCode(message.data.playInfo, message?.data?.data);
  store.commit('game/setGameInfo', {
    currentGameCode: message.data.playInfo,
    enterType: gameBaseInfo.enterType,
    gameUrl: gameBaseInfo.gameUrl,
    needShake: gameBaseInfo.needShake,
  });
  if (message.data.miaoState === '1') {
    // 防止页面上本来就有game开始按钮
    store.commit('app/setGameBtnVisible', false);
    // game等待中
    if (message.data.playInfo === 'sign' || message.data.playInfo === 'hmPlay19') {
      console.log('签到或送祝福游戏无等待界面执行空操作');
    } else {
      // game按钮出现
      store.commit('app/setGameBtnVisible', true);
      store.commit('game/setGameStatus', 1);
    }
    router.replace('/');
  } else if (message.data.miaoState === '2') {
    store.commit('game/setGameStatus', 2);
    if (message.data.playInfo === 'hmPlay19') {
      store.commit('app/setGameBtnVisible', true);
      store.commit('app/togglePopup', 16);
    }
  } else if (message.data.miaoState === '3') {
    store.commit('game/setGameStatus', 3);
    // game按钮消失
    store.commit('app/setGameBtnVisible', false);
    if (message.data.playInfo === 'hmPlay19') {
      store.commit('app/togglePopup');
    }
    if (message.data.playInfo === 'hdGame') {
      // 空game
      router.replace('/');
    }
    if (
      store.state.app.rcGiftGameCodes.indexOf(message.data.playInfo) === -1
      && store.state.app.giftSendVisible
      && store.state.app.env !== 'tt'
    ) {
      // 每个game结束后弹出一次推荐礼物
      store.commit('app/togglePopup', 6);
      store.commit('app/updateRcGiftGameCodes', message.data.playInfo);
    }
  }
}
// 处理进场消息
function handleEnterMessage(message) {
  if (store.state.user.userId === message.data.miaoId || !store.state.user.userId) {
    return;
  }
  if (message.data.miaoVipCar) {
    Vue.prototype.$createEnterEffect({
      name: message.data.miaoName,
      headImg: message.data.miaoHeadUrl,
      enterEffectType: message.data.miaoVipCar,
    });
  } else {
    Vue.prototype.$createEnterEffect({
      name: message.data.miaoName,
      headImg: message.data.miaoHeadUrl,
      enterEffectType: 'common',
    });
  }
}
// 处理评分消息
function handleGiveMarkMessage(message) {
  console.log(message.data);
  store.commit('game/setCanMarkUserInfo', true);
}
// 处理喵钻红包消息
function handleDiamondHbMessage(message) {
  console.log(message);
  store.dispatch('live/getDiamondHbList');
}
/** 处理麻将的广播 */
function handlerMajiang(message) {
  console.log(message.data);
  const round = message.data.miaoBless || 1;
  store.commit('game/setMajiangRound', round);
}
// 处理开心答题的消息
function handleHappyQA(message) {
  // 通知揭晓当前题目的答案
  if (message.type === 'happy_announce') {
    store.commit('game/setCanExposeCurrentQuestion', true);
  } else if (message.type === 'happy_qa2') {
    // 通知可以进入下一题
    store.commit('game/setCanNextQuestion', true);
  }
}

const CODE = Object.freeze({
  /** 调用toH5接口发送的通用消息 */
  OTHERS: 'toH5',
});

/** 其他信息的处理器 */
export const otherMessageHandler = (() => {
  /** 响应时执行的函数集合 */
  const callbackList = new Set();

  /**
   * 设置响应时执行的函数
   * @param {Function} fn 其他响应执行的函数
   */
  const on = (fn) => {
    callbackList.add(fn);
  };

  /** 移除响应时执行的函数
   * @param {Function} fn 其他响应执行的函数
   */
  const off = (fn) => {
    callbackList.delete(fn);
  };

  /** 触发响应 */
  const triggerAllCallback = (msg) => {
    callbackList.forEach((fn) => {
      fn(msg);
    });
  };

  return {
    on,
    off,
    triggerAllCallback,
  };
})();

// 处理消息(汇总方法)
export default function handleMessage(message) {
  console.log('chatMessage:', message);
  switch (message.type) {
    case 'wsya':
      handleChatMessage(message);
      break;
    case 'liwu':
      handleGiftMessage(message);
      handleChatMessage(message); // 礼物消息也要加入到聊天记录
      break;
    case 'play':
      handleGameMessage(message);
      break;
    case 'jinchang':
      handleEnterMessage(message);
      break;
    case 'Player_1':
      handleGiveMarkMessage(message);
      break;
    case 'Player_2':
      handleDiamondHbMessage(message);
      break;
    case 'mahjong':
      handlerMajiang(message);
      break;
    case 'refresh':
      window.location.reload();
      break;
    case 'happy_announce':
    case 'happy_qa2':
      handleHappyQA(message);
      break;
    case CODE.OTHERS:
      otherMessageHandler.triggerAllCallback(message);
      break;
    default:
      break;
  }
}
```

## File: src/assets/constant/index.js
```javascript
export const DANMU_COLOR = [
  {
    name: 'white',
    color: 'rgb(0, 0, 0.8)',
  },
  {
    name: 'violet',
    color: 'rgb(198, 168, 254)',
  },
  {
    name: 'red',
    color: 'rgb(211, 16, 16)',
  },
  {
    name: 'blue',
    color: 'rgb(56, 173, 249)',
  },
  {
    name: 'pink',
    color: 'rgb(247, 128, 176)',
  },
  {
    name: 'yellow',
    color: 'rgb(255, 145, 39)',
  },
];
// 祝福语
export const WISH = {
  wedding: [
    '十年修得同船渡，百年修得共枕眠！',
    '衷心的祝福你们：相互珍惜，同心永结！',
    '祝福你们永远互敬互爱，甜美幸福！',
    '比翼齐飞，事业更昌盛！',
    '美满良缘，白首成约！',
    '愿你们相亲相爱，永结同心！',
    '和和美美，白头偕老！',
    '恭喜你大婚达成，祝福你们盟结良缘！',
    '愿你们一直带着这喜悦和幸福走进人生的新篇章！',
    '祝你们山盟永在、海誓长存！',
    '祝天天恩恩爱爱！新婚快乐！',
    '露出幸福真面目，只缘身在祝福中。',
    '祝你们新婚快乐、永远幸福！',
    '婚姻永美满，幸福在人间！恭喜恭喜！',
    '同心结已成，愿爱永同行！',
    '祝你们百年恩爱结连理，一生幸福永同心！',
    '百年好合！新婚愉快，甜甜蜜蜜！早生贵子！',
    '祝你们相亲相爱一百年不动摇！',
    '海枯石烂同心永结，地阔天高比翼齐飞！',
    '珠联壁合洞房春暖，花好月圆鱼水情深！',
    '新婚快乐！我们一起摇红包、做game、中大奖、沾喜气，嗨起来！',
  ],
  zshl: [
    '十年修得同船渡，百年修得共枕眠！',
    '衷心的祝福你们：相互珍惜，同心永结！',
    '祝福你们永远互敬互爱，甜美幸福！',
    '比翼齐飞，事业更昌盛！',
    '美满良缘，白首成约！',
    '愿你们相亲相爱，永结同心！',
    '和和美美，白头偕老！',
    '恭喜你大婚达成，祝福你们盟结良缘！',
    '愿你们一直带着这喜悦和幸福走进人生的新篇章！',
    '祝你们山盟永在、海誓长存！',
    '祝天天恩恩爱爱！新婚快乐！',
    '露出幸福真面目，只缘身在祝福中。',
    '祝你们新婚快乐、永远幸福！',
    '婚姻永美满，幸福在人间！恭喜恭喜！',
    '同心结已成，愿爱永同行！',
    '祝你们百年恩爱结连理，一生幸福永同心！',
    '百年好合！新婚愉快，甜甜蜜蜜！早生贵子！',
    '祝你们相亲相爱一百年不动摇！',
    '海枯石烂同心永结，地阔天高比翼齐飞！',
    '珠联壁合洞房春暖，花好月圆鱼水情深！',
    '新婚快乐！我们一起摇红包、做game、中大奖、沾喜气，嗨起来！',
  ],
  annualMeeting: [
    '祝公司蓬勃发展，生意兴隆，财源广进！',
    '祝我们企业的明天更加辉煌！',
    '祝公司在未来的发展中吉祥如意，大展宏图！',
    '祝愿我们公司再创辉煌，越来越好！',
    '祝愿公司生意兴隆通四海，财源茂盛达三江。',
    '我们会更加的努力，更加的奋进，迎接新的辉煌！',
    '一路有你，尽显雄风，携手共进，再创天地辉煌！',
    '根深叶茂无疆业，源远流长有道财！',
    '东风利市春来有象，生意兴隆日进无疆！',
    '祝愿公司未来创新不止、扬帆起航！',
    '一份耕耘，一份收获，风雨同舟，共创辉煌！',
    '展望未来，满怀信心，同心协力，积极进取！',
    '普天同庆艳阳天，霖霖甘露兆丰年！',
    '包打天下鸿图展，装潢华丽伟业坚！',
    '五十耕耘磨一剑，周全服务暖人间！',
    '年年好运财源广，庆语欢歌谱新篇！',
    '年年若得齐心处，庆功谈笑斩荆棘！',
    '福禄双收业兴旺，瑞气东来鸿运长！',
    '博大精深科技强，德厚载物美名扬！',
    '十全十美峥嵘榜，周天日月齐光芒！',
  ],
  birth: [
    '年年有今日，岁岁有今朝！',
    '祝你生日快乐！天天开心，身体健康！',
    '愿快乐、幸福永远围绕在你身边!生日快乐!',
    '衷心地祝愿你生日快乐!万事如意！',
    '生日快乐!你快乐所以我快乐！',
    '声声的祝福，深深的情谊，祝你生日快乐！',
    '祝你百事可乐，万事芬达，天天娃哈哈！',
    '祝你在新的一岁里事事顺利!生日快乐!',
    '愿健康快乐与你日夜相伴，祝你生日快乐!',
    '让我为你祝福，让我为你欢笑，祝你生日快乐！',
    '愿你天天快乐，年年好运，一生幸福！',
    '身体健康，心想事成，万事如意！',
    '快事长伴友，乐衔月下杯！',
    '快意人生勤登攀，乐娱生日庆华年！',
  ],
  bby: [
    '祝福宝宝百日康乐，千时如意，万事顺心！',
    '祝愿宝宝健康成长，在爱的呵护下享受阳光和欢乐！',
    '恭喜！祝家庭美满幸福，宝宝天真可爱',
    '值得记念的日子，世界因为有了你而更加美好',
    '祝小宝宝健康成长，平安快乐。',
    '欣闻喜得贵子，特向您和全家表示衷心的祝贺和良好的祝愿!',
    '我前来贺喜，愿新生的小宝贝给你们带来数不尽的快乐!',
    '百岁宝，百岁好，岁岁宝宝都是宝;吃得好，睡得好，陪您过得好',
    '百年百月百天，长久长顺长安;百分怜爱祝，身体强壮永安康',
    '恭喜恭喜!家庭美满幸福，宝宝天真可爱。',
    '希望你身体强壮，快快长大，越长越可爱哦！',
    '宝宝，你的到来点亮了我们的生命，为我们的生活赋予了全新的意义，生日快乐！',
    '值得记念的日子，宝贝，世界因为有了你而更加美好，生日快乐!',
    '宝贝，生日快乐。记住，你生命的每一次扬帆出海。我的祝福都会伴你同行!',
    '祝福宝宝健康成长，前途无量，有一个美好的未来，快乐、成就、功名、财富应有尽有！。',
    '愿你像颗种子，勇敢地冲破泥沙，将嫩绿的幼芽伸出地面，指向天空。',
    '青春、阳光、欢笑，为这属于你的日子，舞出欢乐的节拍。祝宝贝生日快乐!',
    '祝你在每个成长的日子里都开开心心!生日快乐!',
    '宝贝，你的生日就在今天，祝你可爱依旧，快乐多多!',
    '以后要听妈妈的话，做个乖宝宝哦!',
    '祝福宝宝聪明伶俐、听话乖巧。',
    '送宝宝一份温馨，两份问候，三份美好，四份懵懂，五份高贵，六份前程，七份典雅，八份柔情，九份财运，十份真诚。生日快乐，幸福安康。',
    '希望未来的日子，你都能快乐的成长，有个快乐美好的童年!',
    '宝宝生日快乐，原所有的快乐，所有的幸福，所有的温馨，所有的好运永远围绕在你身边!生日快乐!',
    '祝福这个可爱的孩子，我祝福他健康成长，快乐幸福，将来一定事业有成。',
    '愿所有的幸福，所有的快乐，所有的温馨，所有的好运，永远围绕在宝宝身边。',
  ],
  bly: [
    '祝孩子像林间的仙子一样快乐幸福，歌声相伴，美满一生!',
    '百日宝宝百岁康，岁岁岁平安，祝您宝宝平安又健康!',
    '感谢你，宝贝。因为你，花朵开放，随你而来的满天希望!',
    '宝贝。你生命的每一次扬帆出海。我的祝福都会伴你同行!',
    '百年百月百天，长久长顺长安',
    '青春、阳光、欢笑，为这属于你的日子，舞出欢乐的节拍。',
  ],
  myy: [
    '一月已满，健康快乐，平安成长，更加欣喜，举杯同庆。',
    '满月宴，祝福满满，健康满满，幸福满满，快乐满满。',
    '美好到，得小宝。命运好，才情高。合家欢，父母笑。',
    '宝宝降临，全家欢笑，再无烦绕；宝宝一笑，万事变好。',
    '喜气伴绕；恭喜喜得宝宝，开心常绕',
    '祝愿宝宝，满月快乐，健康围绕，乐得逍遥！',
    '宝宝满月到，幸福吹响集结号，喜鹊鸿雁传喜报，远亲近邻都请到！',
    '宝宝满月，送去满满的祝愿：愿工资涨满，广开财源，多赚宝宝的奶粉钱！',
  ],
  sy: [
    '福如东海寿比南山;日月昌明松鹤长春;笑口常开天伦永享。',
    '嘉宾旨酒，笑指青山来献寿。愿百岁平安，人共梅花老岁寒。',
    '今天是个喜庆的日子，在您辛劳了几十年的今天，子孙欢聚一堂，同享天伦之乐，祝您寿与天齐',
    '岁月飞逝，青春不老， 愿快乐与您永随',
    '千里送蟠桃，福多寿多，祝您老福如东海',
    '麻姑献寿，松鹤同寿，祝您寿比南山不老松',
    '子孙绕膝福气多，日月增辉年寿长',
    '如月之恒，如日之升，如南山之寿，不骞不崩。如松柏之茂，无不尔或承',
  ],
  crl: [
    '愿此去前程似锦 再相逢依旧少年',
    '愿你走到哪里都不缺重头再来的勇气',
    '愿你的未来，要咩有咩，前程似锦，踮到飞起',
    '愿你出走半生 归来仍是少年',
    '愿你成为自己的太阳 不必凭借谁的光',
    '愿你 有良善、有勇气、有梦想、有担当、有满满的爱。',
    '愿你开启一段新的美丽人生!愿你真诚、美丽、善良',
    '成人告别幼稚走向成熟,克服依赖,走向独立，愿你今后的每一天万事顺意，不惧风雨，勇往直前',
    '成年了可以放心大胆谈恋爱了',
  ],
  bydl: [
    '我不想说再见,更不想说不见，我只想说您不要忘了朋友。',
    '毕业了我们不要哭好不好。',
    '毕业了，我怕连偷偷看你的机会都没有了。',
    '我不怕毕业，我怕毕业后的离别。',
    '毕业了，曾经那些不在意的人和事，现在想来多么珍贵。',
    '校服很丑但是我想陪你多穿几年。',
    '下一个夏天，教室里又坐满了人，可惜不再是我们。',
    '我不喜欢毕业，即使毕业没有作业。',
    '母校就是那个你一天骂它八遍，却不许别人骂的地方。',
    '同桌至上，这个夏天，我们不毕业。',
    '好好珍惜穿校服的日子吧，因为一脱就是一辈子。',
    '今天天气不错，明天没有课，以后都没有课了。',
    '我们和学校再见，却不跟青春道别。',
    '请再谱一支青春曲，伴随你我在明天的征途中继续奋进!',
    '不说难过，不说再见，我们后会有期。',
    '真正的毕业不是离开那所学校，而是那群人散了。',
    '让生命的书页，永远记住点燃过心灵的温暖阳光。',
    '毕业季。友情不毕业，青春不毕业。',
    '我们都是再快毕业的时候才爱上学校的。',
    '谁把光阴剪成了烟花，一瞬间，看尽繁华。',
    '离开的不是学校，而是教室里的那帮逗比。',
    '再遇见或许我们都不记得曾经的年少轻狂。',
    '时光不老，我们不散。',
    '有一种美好叫做青春，有一种离别叫做毕业。',
    '最初遇见羞了脸，如今离别却红了眼。',
    '几载青春，几载情谊，同学少年总相忆。',
    '毕业了，结束了！可是到底是结束，还是另一个新的开始？',
    '毕业，我说是结束，你却说是成熟。',
    '我们一起奋斗的日子，一起跑过的日子是最值得怀念的。',
    '毕业了，心中有太多太多的不舍！',
    '毕业了，懂得什么是友谊，懂得了什么是师生情。',
  ],
  xsy: [
    ' 举杯谢恩师,一日教诲一世情。',
    '桃李芬芳,师恩难忘。',
    '青云直上日,难忘教诲时。',
    '投之以桃,报之以李,老师,谢谢您!',
    '成功源自您的栽培，优秀出自您的耕耘，感谢老师！',
    '金榜题名时，师恩永难忘。',
    '师德高尚人敬仰，恩泽稚童情意长。',
    '祝前程似锦，贺金榜题名。',
    '今日金榜提名,明日鹏程万里。',
    '春风得意马蹄疾，一日看尽长安花。',
    '学业有成，美好未来。',
    '星光不负赶路人,时光不负有心人。',
    '远大前程已扬帆，乘风破浪在此刻。',
    '鸦反哺，羊跪乳，学子永记教师恩。',
    '师生情谊深似海，愿您生活美满，身体康泰！',
    '春风育桃李，秋果谢恩情。',
    '纸短情长，师恩难忘。',
    '十年树木百年人，老师恩情犹海深。',
    '师长恩情深似海,同学缘分高于天。',
    '厚谊常存魂梦里，深恩永志我心中。',
    '芬芳四溢,桃李天下。',
    '不惧风霜,宽厚弘毅，感谢您，老师。',
    '桃李满天下，春晖遍四方。',
    '点点滴滴，言传身教，悠然于心。',
    '好风凭借力，送我上青云。',
  ],
  jbtm: [
    '今日金榜提名,明日鹏程万里。',
    '学业有成，未来可期。',
    '祝前程似锦，贺金榜题名',
    '壮志凌云，妙笔生花，愿未来前程似锦。',
    '好风凭借力，送我上青云。',
    '披星戴月走过的路，终将会繁花遍地。',
    '一步登科，蟾宫稳步，桂香满袖。',
    '一鸣从此始，相望青云端。',
    '春风得意马蹄疾，一日看尽长安花。',
    '东风擢第上瑶京，金榜天门列姓名。',
    '鹰击天风壮，鹏飞海浪春。',
    '大鹏一日同风起，扶摇直上九万里。',
    '画凌烟，上甘泉，自古功名属少年。',
    '天道酬勤，力耕不欺。',
    '远大前程已扬帆，乘风破浪在此刻。',
    '向道是龙刚不信，果然夺得锦标归。',
    '知汝十年磨一剑，一朝飞出虹云端。',
    '金榜高悬姓字真，分明折得一枝春。',
    '桃花直透三层浪，桂子高攀第一枝。',
    '金榜题名，马到功成，不负韶华。',
    '须知少时凌云志，曾许人间第一流。',
    '乡里亲情相见日，一时携酒贺高堂。',
    '希君生羽翼，一化北溟鱼。',
    '知君志不小，一举凌鸿鹄。',
    '愿祝君如此山水，滔滔岌岌风云起。',
  ],
  txh: [
    '人生的幸福不是走平坦的路，而是在坎坷的路上有位患难与共的朋友;的快乐不是没有眼泪的生活，而是有位为你擦眼泪的知己。我亲爱的朋友，愿您拥有幸福和快乐!',
    '敬爱的老师，作为你们的学生，得到你们的谆谆教诲，终生受益，我们感到无比的骄傲!',
    '亲爱的同学，作为学子同窗共读，留存真挚无私的友情，我们倍感珍惜!',
    '不论是身居高位，还是一介布衣;不论是富甲一方，还是清贫如水，但是，师生情永在，同学谊永存!',
    '人和人相遇，靠的是一点缘分，人和人相处，靠的是一份诚意，人和人相爱，靠的是一颗真心，正因为人世间每段缘份都来之不易，我希望我们永远是的朋友!',
    '晚上笑笑睡个美满觉，早晨笑笑全天生活有情调，工作之余笑笑满堂欢喜又热闹，烦恼之时笑笑一切忧愁全抛掉，收到短信笑笑感受生活真美妙。',
    '你的美丽雅纯是子弹，会深深地击中我的心，让你的情话和动人在我心中一生美丽，一条短信却蕴含着我千千万万个心愿，祝你天天快乐高兴。',
    '我送你一颗忘忧草，再为你逮只幸福鸟，当幸福鸟含着忘忧草像你飞来时，请把你的心整理好，那是我对你的祝福，只希望你能快乐到老幸福到老!',
    '选对一个环境可以快乐一生!选对一个伴侣可以幸福一生!选对一个朋友可以智慧一生!选对一份事业可以成就一生!您是我一生最美丽的相遇!',
    '我不知道流星能飞多久，值不值得追求;我不知道樱花能开多久，值不值得等候;但我知道你我的友谊，能像樱花般美丽，像恒星般永恒，值得我用一生去保留。',
    '给回忆永不褪去的色彩，给思念自由飞翔的翅膀，给幸福永恒不朽的生命，给生活轻松灿烂的笑脸，给朋友诚挚美好的友谊，给你当然是一生一世的祝福!',
    '紧地握一握手。手有意，手有情，掌心中千言万语，也有我难言的秘密。',
    '忧他人之忧，乐他人之乐，你那善良热诚无私的品性，永远铭刻在我心怀。',
    '你珍惜今天，又以百倍的热情去拥抱明天，那未，未来就一定属于你!',
    '我们这一代，是跨世纪的青年。历史不允许我们愧对古人与后代。愿我们以卓越的智慧坚强的意志大无畏的精神，不断开拓，不断奋进!',
    '高尚的理想是人生的指路明灯。有了它，生活就有了方向;有了它，内心就感到充实。迈开坚定的步伐，走向既定的目标吧!',
    '不论从事哪种职业，要走向成功，首先应对职业感兴趣。',
    '当我走进你，本想获得一滴水，你却给了我整个海洋;本想采摘一片树叶，你却给了我整个森林;本想获得一缕春风，你却给了我整整一个春天。',
    '难忘今宵，今宵我们欢声笑语歌舞飞扬',
    '请再谱一支青春曲，伴随你我在明天的征途中继续奋进!',
    '我们曾是并肩的两棵小树，我们曾是二重唱的两个声部，我们曾是张课桌上的学友。当我们挥手告别的时候，请接受我深情的祝福。',
    '岁月的车轮即将驶出青春的校园，甚至来不及去想一想，我们就要走向生活的前方。这样匆匆，说些什么?――让我们的心间加固童年时架设起来的桥梁。',
    '我们相逢在陌生时，我们分手在熟悉后。明天，我们要到生活的星图上找寻自己的新位置，让我们用自己闪烁的星光相互问讯表情达意。',
    '大地上有五色土，海滩边有五彩贝，乐章里有五线谱，人生中有五彩路。',
    '今日同窗分手，说一声：珍重!明朝校友相逢，贺一句：成功!',
    '相聚的时光虽然短暂，同学情谊将远播四方',
    '一丝真情胜过千两黄金，一丝温暖能抵万里寒霜，一声问候送来温馨甜蜜，一条短信捎去我万般心意，忙碌的日子好好照顾自己。',
    '一份真诚的感动令我们常存心间，一份诚挚的祝福将陪伴我们直到永远，为了心中这份感情，我们在这里绽开笑颜。',
    '美酒传递着我们深深的祝福，友情让我们的心彼此相连，为了这份真挚的情感，我们在这里推杯换盏。',
    '关于相遇有一种解释叫缘分，关于生命有一种信念叫做轮回，而对于我有一种情感叫做思念，如果真有轮回，我希望每一次生命中有你这个永远不变的朋友!',
    '纵然岁月流逝，空间分隔了我们，时间冲散了你我，但关怀祝福之心却长伴左右。',
    '步入大学迎来一片新的天地，为了理想为了将来去拼搏去努力;海阔凭鱼跃，天高任鸟飞!祝福大一新生大展宏图，捷报连连!',
    '友情的延续来自心灵，不论联系有多少，只要内心留有彼此的一片天空，那么偶尔一声问侯就会带来会心的一笑。',
    '送上一份温馨的牵挂，赠予一腔火热的恋情。',
    '痛苦是别人的，快乐才是自己的;麻烦将是暂时的，朋友总是永恒的;爱情是用心经营的，世界上没有什么大不了的;祝今天，哈哈!',
    '相知是天意，相识是人意，相加便是友谊，有情便有意，我们能聚在一起，因为心有灵犀。',
    '心似乎不得休息，总是不停地想你，哪怕是夜深人静，但愿星星能送去我的万千祝福。',
    '星光依旧灿烂，激情仍然燃烧。因为有梦想，所以我存在。你在你的领域里不惜青春，我在我的道路上不知疲倦。',
    '夜色茫茫照四周，天边新月如钩。往事恍如梦，梦境何处求。人隔千里，路悠悠，请明月，代问候。',
    '一丝真情胜过千两黄金，一丝温暖能抵万里寒霜，一声问候送来温馨甜蜜，一条短信捎去我万般心意，忙碌的日子好好照顾自己。',
    '初遇你的心情是温馨的，和你交友的时候是真心的，与你在一起的时候是开心的，认识你这个朋友是无怨无悔的。',
    '春风得意马蹄疾。新年伊始，愿你乘着和煦的春风，朝着灿烂的前景，马不停蹄，奔腾捷进!',
    '当你成功时，喷嚏如歌;当你失败时，歌如喷嚏。',
    '当你早上开机时，能见到我对你的祝福，一朵心中的玫瑰，为你带来一天的好运。',
    '对你的思念像袅袅的轻烟不绝如缕，对你的祝福似潺潺的小溪伴随一生一世。',
    '方寸间，历数世上桑田沧海;时空里，细问人间暑往寒来;是朋友，星移斗转情不改;是知音，天涯海角记心怀。',
    '风吹走了祝福的心絮，雨模煳了期盼的视线，我扎紧了思念的情结，相信总有一天我们会再度重逢!',
    '不管工作有多么的繁忙，只要记得我时刻都在远方关望你祝福你就好。',
    '把生活酿成酒浆，用快乐作瓶，用微笑命名，用和谐构图，用舒畅着色，聘请看短信的你，做永远的品酒师。',
    '你好，我的朋友，你一定还在忙吧，注意保重身体，你的好朋友!',
  ],
  qqy: [
    '笑语声声，共庆乔迁喜！',
    '仁里莺迁崇四美，新居燕喜庆三春！',
    '乔宅喜，天地人共喜！',
    '乔迁之喜祝福你，真诚祝福做贺礼！',
    '良辰吉日，从此金银财宝滚进门！',
    '乔迁大喜拍拍手，祝福送到喝喜酒！',
    '鞭炮啪啪啪，锣鼓铛铛铛，新天新地新福绕，新宅新院新财罩！',
    '乔新迁，好运到，入金窝，福星照！',
  ],
  hx: [
    '祝愿贵公司蓬勃发展，日胜一日!明天展会圆满成功!',
    '机遇蕴含精彩，发展充满信心，号角催人奋进。',
    '惨淡经营历千辛，一举成名天下闻，虎啸龙吟展宏图，盘马弯弓创新功!',
    '团结，是一个重要的精神，一个人要想成功，要有能够同别人合作的精神！',
    '事业是连结我们的纽带，愿我们的事业旺发达，友谊之花也随之盛开！',
    '祝你一气呵成马到成功，一帆风顺事业有成，一鸣惊人大展宏图，一年到头和和美美快快乐乐',
    '成就是辉煌的，业绩是突出的，目标是超过的，心情是开心的，愿来大家再接再厉，再创辉煌，身体健康，万事如意。',
  ],
  dhy: [
    '十年修得同船渡，百年修得共枕眠！',
    '衷心的祝福你们：相互珍惜，同心永结！',
    '祝福你们永远互敬互爱，甜美幸福！',
    '比翼齐飞，生活更幸福！',
    '美满良缘，白首成约！',
    '愿你们相亲相爱，永结同心！',
    '和和美美，白头偕老！',
    '恭喜你们订婚达成，祝福你们盟结良缘！',
    '愿你们一直带着这喜悦和幸福走进人生的新篇章！',
    '祝你们山盟永在、海誓长存！',
    '祝天天恩恩爱爱！幸福快乐！',
    '露出幸福真面目，只缘身在祝福中。',
    '祝你们永远快乐、永远幸福！',
    '人生永美满，幸福在人间！恭喜恭喜！',
    '同心结已成，愿爱永同行！',
    '祝你们百年恩爱结连理，一生幸福永同心！',
    '甜甜蜜蜜，永结同心，幸福百年！',
    '祝你们相亲相爱一百年不动摇！',
    '海枯石烂同心永结，地阔天高比翼齐飞！',
    '恭喜恭喜！我们一起摇红包、做game、中大奖、沾喜气，嗨起来！',
  ],
  wl: [
    '今天来见到大家，真开心',
    '氛围太棒啦，超舒服',
    '愿咱们今天都有好收获',
    '终于来啦，满是期待',
    '和大家一起，感觉超棒',
    '盼今天每一刻都顺意',
    '精彩时刻，满心期待',
    '祝大家今天都尽兴呀',
    '这儿的感觉，太对味了',
    '希望今天满是小美好',
    '乘兴而来，兴尽而返',
    '美好时光与诸君共享',
    '感谢主办方的各项安排',
    '精彩不止一点点',
    '祝咱们都有难忘时刻',
    '就两个字：开心',
    '和朋友一起来的，真好',
    '能参与进来，真欢喜',
    '愿今天每个人都舒心',
    '一起度过这段好时光',
  ],
};
export const QUICKWISHES = {
  wedding: [
    '恭喜找到自己的长征伴侣。',
    '结完婚，生完孩子，赶紧回来开黑！',
    '中国首富祝你们婚快乐永结同心',
    '大小姐一定要开心幸福啊 来自你最牢靠的粉丝后援团',
    '祝各位吃好喝好!',
    '天生才子佳人配，只羡鸳鸯不羡仙。',
    '奥利给 我最美我最帅 我是人间小可爱',
    '今晚大奖花落谁家🌸 🌸',
    '郎才女貌，瓜瓞延绵',
    '主持人帅的滑丝',
    '美满良缘，白首成约！',
    '比翼齐飞，事业更昌盛！',
    '和和美美，白头偕老！',
    '嗨起来，艾瑞巴蒂',
    '珠连壁合，天作之美',
    '欢庆此日结佳偶，且喜今朝庆良缘',
    '露出幸福真面目，只缘身在祝福中。',
    '幸福一对，幸福一生。',
    '㊗️新婚快乐，百年好合，早生贵子',
    '早生三胞胎',
    '幸福永远哈',
    '新郎今天也太帅了，新娘也超级漂亮',
    '祝二位新人永结同心',
    '火箭🚀 🚀🚀🚀 ,走一个',
    '💗💗💗！幸福呦',
    'everybaby  high 起来！',
  ],
  zshl: [
    '恭喜找到自己的长征伴侣。',
    '结完婚，生完孩子，赶紧回来开黑！',
    '请喝趴我',
    '来了来了，干饭人，干酒人',
    '大家说说，新郎有我帅吗',
    '哥们,加油,以后工资上交,出门交代',
    '兄弟，早生贵子，百年好合，早生贵子',
    '要狠狠的幸福到白头^o^',
    '娶老婆咯！心里美滋滋',
    '我给你俩幸福加点糖',
    '你我共富贵！多生孩子多种树！',
    '哦耶，我不管我最帅！',
    '新娘太美了',
    '新婚快乐',
    '新郎今天有点帅',
    '恭喜你找到了今生唯一灵魂之伴侣。',
    '主持人今天很帅，但是和我兄弟新郎比，还差一点点',
    '新郎今天太帅了，发个大红包吧',
    '大家吃好喝好玩好，待会还有抢红包',
    '喝完喜酒，晚上麻将三缺一，来的扣666',
    '看你们大婚了，我也想找个对象',
    '明年这时候是不是该喝孩子的满月酒啦',
    '一切都是最好的安排！祝新婚快乐，一生欢喜！',
    '一生一世两情相悦，三世尘缘四世同喜，五谷丰登六六顺',
    '中国首富祝你们婚快乐永结同心',
    '大小姐一定要开心幸福啊 来自你最牢靠的粉丝后援团',
    '祝各位吃好喝好!',
    '天生才子佳人配，只羡鸳鸯不羡仙。',
    '奥利给 我最美我最帅 我是人间小可爱',
    '今晚大奖花落谁家🌸 🌸',
    '郎才女貌，瓜瓞延绵',
    '主持人帅的滑丝',
    '美满良缘，白首成约！',
    '比翼齐飞，事业更昌盛！',
    '和和美美，白头偕老！',
    '嗨起来，艾瑞巴蒂',
    '珠连壁合，天作之美',
    '欢庆此日结佳偶，且喜今朝庆良缘',
    '露出幸福真面目，只缘身在祝福中。',
    '幸福一对，幸福一生。',
    '㊗️新婚快乐，百年好合，早生贵子',
    '早生三胞胎',
    '幸福永远哈',
    '新郎今天也太帅了，新娘也超级漂亮',
    '祝二位新人永结同心',
    '火箭🚀 🚀🚀🚀 ,走一个',
    '💗💗💗！幸福呦',
    'everybaby  high 起来！',
  ],
  annualMeeting: [
    '祝公司蓬勃发展，生意兴隆，财源广进！',
    '祝我们企业的明天更加辉煌！',
    '祝公司在未来的发展中吉祥如意，大展宏图！',
    '祝愿我们公司再创辉煌，越来越好！',
    '祝愿公司生意兴隆通四海，财源茂盛达三江。',
    '我们会更加的努力，更加的奋进，迎接新的辉煌！',
    '一路有你，尽显雄风，携手共进，再创天地辉煌！',
    '根深叶茂无疆业，源远流长有道财！',
    '东风利市春来有象，生意兴隆日进无疆！',
    '祝愿公司未来创新不止、扬帆起航！',
    '一份耕耘，一份收获，风雨同舟，共创辉煌！',
    '展望未来，满怀信心，同心协力，积极进取！',
    '普天同庆艳阳天，霖霖甘露兆丰年！',
    '包打天下鸿图展，装潢华丽伟业坚！',
    '五十耕耘磨一剑，周全服务暖人间！',
    '年年好运财源广，庆语欢歌谱新篇！',
    '年年若得齐心处，庆功谈笑斩荆棘！',
    '福禄双收业兴旺，瑞气东来鸿运长！',
    '博大精深科技强，德厚载物美名扬！',
    '十全十美峥嵘榜，周天日月齐光芒！',
  ],
  birth: [
    '年年有今日，岁岁有今朝！',
    '祝你生日快乐！天天开心，身体健康！',
    '愿快乐、幸福永远围绕在你身边!生日快乐!',
    '衷心地祝愿你生日快乐!万事如意！',
    '生日快乐!你快乐所以我快乐！',
    '声声的祝福，深深的情谊，祝你生日快乐！',
    '祝你百事可乐，万事芬达，天天娃哈哈！',
    '祝你在新的一岁里事事顺利!生日快乐!',
    '愿健康快乐与你日夜相伴，祝你生日快乐!',
    '让我为你祝福，让我为你欢笑，祝你生日快乐！',
    '愿你天天快乐，年年好运，一生幸福！',
    '身体健康，心想事成，万事如意！',
    '快事长伴友，乐衔月下杯！',
    '快意人生勤登攀，乐娱生日庆华年！',
  ],
  bby: [
    '希望你身体强壮，快快长大，越长越可爱哦！',
    '宝宝，你的到来点亮了我们的生命，为我们的生活赋予了全新的意义，生日快乐！',
    '值得记念的日子，宝贝，世界因为有了你而更加美好，生日快乐!',
    '宝贝，生日快乐。记住，你生命的每一次扬帆出海。我的祝福都会伴你同行!',
    '祝福宝宝健康成长，前途无量，有一个美好的未来，快乐、成就、功名、财富应有尽有！。',
    '愿你像颗种子，勇敢地冲破泥沙，将嫩绿的幼芽伸出地面，指向天空。',
    '青春、阳光、欢笑，为这属于你的日子，舞出欢乐的节拍。祝宝贝生日快乐!',
    '祝你在每个成长的日子里都开开心心!生日快乐!',
    '宝贝，你的生日就在今天，祝你可爱依旧，快乐多多!',
    '以后要听妈妈的话，做个乖宝宝哦!',
    '祝福宝宝聪明伶俐、听话乖巧。',
    '送宝宝一份温馨，两份问候，三份美好，四份懵懂，五份高贵，六份前程，七份典雅，八份柔情，九份财运，十份真诚。生日快乐，幸福安康。',
    '希望未来的日子，你都能快乐的成长，有个快乐美好的童年!',
    '宝宝生日快乐，原所有的快乐，所有的幸福，所有的温馨，所有的好运永远围绕在你身边!生日快乐!',
    '祝福这个可爱的孩子，我祝福他健康成长，快乐幸福，将来一定事业有成。',
    '愿所有的幸福，所有的快乐，所有的温馨，所有的好运，永远围绕在宝宝身边。',
  ],
  bly: [
    '祝孩子像林间的仙子一样快乐幸福，歌声相伴，美满一生!',
    '百日宝宝百岁康，岁岁岁平安，祝您宝宝平安又健康!',
    '感谢你，宝贝。因为你，花朵开放，随你而来的满天希望!',
    '宝贝。你生命的每一次扬帆出海。我的祝福都会伴你同行!',
    '百年百月百天，长久长顺长安',
    '青春、阳光、欢笑，为这属于你的日子，舞出欢乐的节拍。',
  ],
  myy: [
    '祝愿宝宝，满月快乐，健康围绕！',
    '祝宝宝健康成长，平安快乐！',
    '长风相顺伴安康，命生不凡春秋畅！',
    '惟愿宝宝平安顺遂，一生喜乐！',
    '健生英俊神仙助，康硕聪明山海随！',
  ],
  sy: [
    '福如东海寿比南山;日月昌明松鹤长春;笑口常开天伦永享。',
    '嘉宾旨酒，笑指青山来献寿。愿百岁平安，人共梅花老岁寒。',
    '今天是个喜庆的日子，在您辛劳了几十年的今天，子孙欢聚一堂，同享天伦之乐，祝您寿与天齐',
    '岁月飞逝，青春不老， 愿快乐与您永随',
    '千里送蟠桃，福多寿多，祝您老福如东海',
    '麻姑献寿，松鹤同寿，祝您寿比南山不老松',
    '子孙绕膝福气多，日月增辉年寿长',
    '如月之恒，如日之升，如南山之寿，不骞不崩。如松柏之茂，无不尔或承',
    '恭祝老寿星，福如东海，日月昌明。',
    '松鹤长春，春秋不老，古稀重新，欢乐远长。',
    '恭祝老人增富增寿增富贵，添光添彩添吉祥，福如东海，寿比南山！',
    '祝福老人生活之树常绿，生命之水长流，寿诞快乐，春辉永绽！',
    '福寿安康，万寿无疆，健康如意，福乐绵绵，笑口常开，益寿延年！',
    '华龄老叟青春驻，鳞凤龟龙寿，期颐天赐，飞觞畅饮，祝虾千秋。',
    '立言立德，胸藏丘壑，泊浪章优，轮翻世纪，夕阳华美，比胜王侯。',
    '让我们一起恭祝寿星，福如东海，日月昌明；春秋不老，松鹤长青；欢乐远长，古稀重新。',
    '满脸皱纹，双手粗茧，岁月记载着您的辛劳，人们想念着您的善良；在这个特殊的日子里，祝您福同海阔、寿比南山，愿健康与快乐永远伴随着您！',
    '恭祝老寿星，福如东海，日月昌明。松鹤长春，春秋不老，古稀重新，欢乐远长。同时也祝愿在坐的的各位都幸福安康!',
    '安逸静谧的晚年，一种休息，一种愉悦，一种至高的享受!祝您福如东海长流水寿比南山不老松!',
  ],
  crl: [
    '成人礼，愿你的美梦都能成真，愿你的喜好都能触及。',
    '愿你在未来的日子里，在风雨中像个大人，成熟坚强；在阳光下像个孩子，快乐无忧，未来，望你保持最初的心[给你小心心]，拥有最初的快乐，越来越好，平安顺遂',
    '愿无忧 愿无愁 愿吾辈前程似锦',
    '愿你 有良善、有勇气、有梦想、有担当、有满满的爱。',
    '愿你如风般自由，如星般璀璨，如诗般绮丽，如梦般辽远，愿你走的每一条路都平坦，度过的每一天都艳阳满天，愿你生无忧怠，岁岁平安',
    '愿成为大人后的你可以保持对世界的好奇勇敢去挑战一切未知善良热情可爱',
    '愿你独立坚强，愿你所得皆你所想，愿你拥有成人的成熟却又不失纯真的美好。愿你一路披荆斩棘，也愿这一路繁花似锦！',
    '愿你三冬暖，愿你春不寒，愿你一路上有良人相伴，一生无忧！',
    '愿你的内心始终弘毅自强愿你的世界始终暖阳和煦愿你的路途始终平坦无忧愿最好的一切始终伴你左右',
    '愿你开启一段新的美丽人生!愿你真诚、美丽、善良。',
    '懵懂的成人礼，愿你的天空永远湛蓝，没有烦恼，顺顺利利的成长！',
    '走向成熟,克服依赖,走向独立，愿你今后的每一天万事顺意，不惧风雨，勇往直前。',
  ],
  bydl: [
    '我不想说再见,更不想说不见，我只想说您不要忘了朋友。',
    '毕业了我们不要哭好不好。',
    '毕业了，我怕连偷偷看你的机会都没有了。',
    '我不怕毕业，我怕毕业后的离别。',
    '毕业了，曾经那些不在意的人和事，现在想来多么珍贵。',
    '校服很丑但是我想陪你多穿几年。',
    '下一个夏天，教室里又坐满了人，可惜不再是我们。',
    '我不喜欢毕业，即使毕业没有作业。',
    '母校就是那个你一天骂它八遍，却不许别人骂的地方。',
    '同桌至上，这个夏天，我们不毕业。',
    '好好珍惜穿校服的日子吧，因为一脱就是一辈子。',
    '今天天气不错，明天没有课，以后都没有课了。',
    '我们和学校再见，却不跟青春道别。',
    '请再谱一支青春曲，伴随你我在明天的征途中继续奋进!',
    '不说难过，不说再见，我们后会有期。',
    '真正的毕业不是离开那所学校，而是那群人散了。',
    '让生命的书页，永远记住点燃过心灵的温暖阳光。',
    '毕业季。友情不毕业，青春不毕业。',
    '我们都是再快毕业的时候才爱上学校的。',
    '谁把光阴剪成了烟花，一瞬间，看尽繁华。',
    '离开的不是学校，而是教室里的那帮逗比。',
    '再遇见或许我们都不记得曾经的年少轻狂。',
    '时光不老，我们不散。',
    '有一种美好叫做青春，有一种离别叫做毕业。',
    '最初遇见羞了脸，如今离别却红了眼。',
    '几载青春，几载情谊，同学少年总相忆。',
    '毕业了，结束了！可是到底是结束，还是另一个新的开始？',
    '毕业，我说事结束，你却说是成熟。',
    '我们一起奋斗的日子，一起跑过的日子是最值得怀念的。',
    '毕业了，心中有太多太多的不舍！',
    '毕业了，懂得什么是友谊，懂得了什么是师生情。',
  ],
  xsy: [
    ' 举杯谢恩师,一日教诲一世情。',
    '桃李芬芳,师恩难忘。',
    '青云直上日,难忘教诲时。',
    '投之以桃,报之以李,老师,谢谢您!',
    '成功源自您的栽培，优秀出自您的耕耘，感谢老师！',
    '金榜题名时，师恩永难忘。',
    '师德高尚人敬仰，恩泽稚童情意长。',
    '祝前程似锦，贺金榜题名。',
    '今日金榜提名,明日鹏程万里。',
    '春风得意马蹄疾，一日看尽长安花。',
    '学业有成，美好未来。',
    '星光不负赶路人,时光不负有心人。',
    '远大前程已扬帆，乘风破浪在此刻。',
    '鸦反哺，羊跪乳，学子永记教师恩。',
    '师生情谊深似海，愿您生活美满，身体康泰！',
    '春风育桃李，秋果谢恩情。',
    '纸短情长，师恩难忘。',
    '十年树木百年人，老师恩情犹海深。',
    '师长恩情深似海,同学缘分高于天。',
    '厚谊常存魂梦里，深恩永志我心中。',
    '芬芳四溢,桃李天下。',
    '不惧风霜,宽厚弘毅，感谢您，老师。',
    '桃李满天下，春晖遍四方。',
    '点点滴滴，言传身教，悠然于心。',
    '好风凭借力，送我上青云。',
  ],
  jbtm: [
    '今日金榜提名,明日鹏程万里。',
    '学业有成，未来可期。',
    '祝前程似锦，贺金榜题名',
    '壮志凌云，妙笔生花，愿未来前程似锦。',
    '好风凭借力，送我上青云。',
    '披星戴月走过的路，终将会繁花遍地。',
    '一步登科，蟾宫稳步，桂香满袖。',
    '一鸣从此始，相望青云端。',
    '春风得意马蹄疾，一日看尽长安花。',
    '东风擢第上瑶京，金榜天门列姓名。',
    '鹰击天风壮，鹏飞海浪春。',
    '大鹏一日同风起，扶摇直上九万里。',
    '画凌烟，上甘泉，自古功名属少年。',
    '天道酬勤，力耕不欺。',
    '远大前程已扬帆，乘风破浪在此刻。',
    '向道是龙刚不信，果然夺得锦标归。',
    '知汝十年磨一剑，一朝飞出虹云端。',
    '金榜高悬姓字真，分明折得一枝春。',
    '桃花直透三层浪，桂子高攀第一枝。',
    '金榜题名，马到功成，不负韶华。',
    '须知少时凌云志，曾许人间第一流。',
    '乡里亲情相见日，一时携酒贺高堂。',
    '希君生羽翼，一化北溟鱼。',
    '知君志不小，一举凌鸿鹄。',
    '愿祝君如此山水，滔滔岌岌风云起。',
  ],
  txh: [
    '人生的幸福不是走平坦的路，而是在坎坷的路上有位患难与共的朋友;的快乐不是没有眼泪的生活，而是有位为你擦眼泪的知己。我亲爱的朋友，愿您拥有幸福和快乐!',
    '敬爱的老师，作为你们的学生，得到你们的谆谆教诲，终生受益，我们感到无比的骄傲!',
    '亲爱的同学，作为学子同窗共读，留存真挚无私的友情，我们倍感珍惜!',
    '不论是身居高位，还是一介布衣;不论是富甲一方，还是清贫如水，但是，师生情永在，同学谊永存!',
    '人和人相遇，靠的是一点缘分，人和人相处，靠的是一份诚意，人和人相爱，靠的是一颗真心，正因为人世间每段缘份都来之不易，我希望我们永远是的朋友!',
    '晚上笑笑睡个美满觉，早晨笑笑全天生活有情调，工作之余笑笑满堂欢喜又热闹，烦恼之时笑笑一切忧愁全抛掉，收到短信笑笑感受生活真美妙。',
    '你的美丽雅纯是子弹，会深深地击中我的心，让你的情话和动人在我心中一生美丽，一条短信却蕴含着我千千万万个心愿，祝你天天快乐高兴。',
    '我送你一颗忘忧草，再为你逮只幸福鸟，当幸福鸟含着忘忧草像你飞来时，请把你的心整理好，那是我对你的祝福，只希望你能快乐到老幸福到老!',
    '选对一个环境可以快乐一生!选对一个伴侣可以幸福一生!选对一个朋友可以智慧一生!选对一份事业可以成就一生!您是我一生最美丽的相遇!',
    '我不知道流星能飞多久，值不值得追求;我不知道樱花能开多久，值不值得等候;但我知道你我的友谊，能像樱花般美丽，像恒星般永恒，值得我用一生去保留。',
    '给回忆永不褪去的色彩，给思念自由飞翔的翅膀，给幸福永恒不朽的生命，给生活轻松灿烂的笑脸，给朋友诚挚美好的友谊，给你当然是一生一世的祝福!',
    '紧地握一握手。手有意，手有情，掌心中千言万语，也有我难言的秘密。',
    '忧他人之忧，乐他人之乐，你那善良热诚无私的品性，永远铭刻在我心怀。',
    '你珍惜今天，又以百倍的热情去拥抱明天，那未，未来就一定属于你!',
    '我们这一代，是跨世纪的青年。历史不允许我们愧对古人与后代。愿我们以卓越的智慧坚强的意志大无畏的精神，不断开拓，不断奋进!',
    '高尚的理想是人生的指路明灯。有了它，生活就有了方向;有了它，内心就感到充实。迈开坚定的步伐，走向既定的目标吧!',
    '不论从事哪种职业，要走向成功，首先应对职业感兴趣。',
    '当我走进你，本想获得一滴水，你却给了我整个海洋;本想采摘一片树叶，你却给了我整个森林;本想获得一缕春风，你却给了我整整一个春天。',
    '难忘今宵，今宵我们欢声笑语歌舞飞扬',
    '请再谱一支青春曲，伴随你我在明天的征途中继续奋进!',
    '我们曾是并肩的两棵小树，我们曾是二重唱的两个声部，我们曾是张课桌上的学友。当我们挥手告别的时候，请接受我深情的祝福。',
    '岁月的车轮即将驶出青春的校园，甚至来不及去想一想，我们就要走向生活的前方。这样匆匆，说些什么?――让我们的心间加固童年时架设起来的桥梁。',
    '我们相逢在陌生时，我们分手在熟悉后。明天，我们要到生活的星图上找寻自己的新位置，让我们用自己闪烁的星光相互问讯表情达意。',
    '大地上有五色土，海滩边有五彩贝，乐章里有五线谱，人生中有五彩路。',
    '今日同窗分手，说一声：珍重!明朝校友相逢，贺一句：成功!',
    '相聚的时光虽然短暂，同学情谊将远播四方',
    '一丝真情胜过千两黄金，一丝温暖能抵万里寒霜，一声问候送来温馨甜蜜，一条短信捎去我万般心意，忙碌的日子好好照顾自己。',
    '一份真诚的感动令我们常存心间，一份诚挚的祝福将陪伴我们直到永远，为了心中这份感情，我们在这里绽开笑颜。',
    '美酒传递着我们深深的祝福，友情让我们的心彼此相连，为了这份真挚的情感，我们在这里推杯换盏。',
    '关于相遇有一种解释叫缘分，关于生命有一种信念叫做轮回，而对于我有一种情感叫做思念，如果真有轮回，我希望每一次生命中有你这个永远不变的朋友!',
    '纵然岁月流逝，空间分隔了我们，时间冲散了你我，但关怀祝福之心却长伴左右。',
    '步入大学迎来一片新的天地，为了理想为了将来去拼搏去努力;海阔凭鱼跃，天高任鸟飞!祝福大一新生大展宏图，捷报连连!',
    '友情的延续来自心灵，不论联系有多少，只要内心留有彼此的一片天空，那么偶尔一声问侯就会带来会心的一笑。',
    '送上一份温馨的牵挂，赠予一腔火热的恋情。',
    '痛苦是别人的，快乐才是自己的;麻烦将是暂时的，朋友总是永恒的;爱情是用心经营的，世界上没有什么大不了的;祝今天，哈哈!',
    '相知是天意，相识是人意，相加便是友谊，有情便有意，我们能聚在一起，因为心有灵犀。',
    '心似乎不得休息，总是不停地想你，哪怕是夜深人静，但愿星星能送去我的万千祝福。',
    '星光依旧灿烂，激情仍然燃烧。因为有梦想，所以我存在。你在你的领域里不惜青春，我在我的道路上不知疲倦。',
    '夜色茫茫照四周，天边新月如钩。往事恍如梦，梦境何处求。人隔千里，路悠悠，请明月，代问候。',
    '一丝真情胜过千两黄金，一丝温暖能抵万里寒霜，一声问候送来温馨甜蜜，一条短信捎去我万般心意，忙碌的日子好好照顾自己。',
    '初遇你的心情是温馨的，和你交友的时候是真心的，与你在一起的时候是开心的，认识你这个朋友是无怨无悔的。',
    '春风得意马蹄疾。新年伊始，愿你乘着和煦的春风，朝着灿烂的前景，马不停蹄，奔腾捷进!',
    '当你成功时，喷嚏如歌;当你失败时，歌如喷嚏。',
    '当你早上开机时，能见到我对你的祝福，一朵心中的玫瑰，为你带来一天的好运。',
    '对你的思念像袅袅的轻烟不绝如缕，对你的祝福似潺潺的小溪伴随一生一世。',
    '方寸间，历数世上桑田沧海;时空里，细问人间暑往寒来;是朋友，星移斗转情不改;是知音，天涯海角记心怀。',
    '风吹走了祝福的心絮，雨模煳了期盼的视线，我扎紧了思念的情结，相信总有一天我们会再度重逢!',
    '不管工作有多么的繁忙，只要记得我时刻都在远方关望你祝福你就好。',
    '把生活酿成酒浆，用快乐作瓶，用微笑命名，用和谐构图，用舒畅着色，聘请看短信的你，做永远的品酒师。',
    '你好，我的朋友，你一定还在忙吧，注意保重身体，你的好朋友!',
  ],
  qqy: [
    '笑语声声，共庆乔迁喜！',
    '仁里莺迁崇四美，新居燕喜庆三春！',
    '乔宅喜，天地人共喜！',
    '乔迁之喜祝福你，真诚祝福做贺礼！',
    '良辰吉日，从此金银财宝滚进门！',
    '乔迁大喜拍拍手，祝福送到喝喜酒！',
    '鞭炮啪啪啪，锣鼓铛铛铛，新天新地新福绕，新宅新院新财罩！',
    '乔新迁，好运到，入金窝，福星照！',
  ],
  hx: [
    '祝愿贵公司蓬勃发展，日胜一日!明天展会圆满成功!',
    '机遇蕴含精彩，发展充满信心，号角催人奋进。',
    '惨淡经营历千辛，一举成名天下闻，虎啸龙吟展宏图，盘马弯弓创新功!',
    '团结，是一个重要的精神，一个人要想成功，要有能够同别人合作的精神！',
    '事业是连结我们的纽带，愿我们的事业旺发达，友谊之花也随之盛开！',
    '祝你一气呵成马到成功，一帆风顺事业有成，一鸣惊人大展宏图，一年到头和和美美快快乐乐',
    '成就是辉煌的，业绩是突出的，目标是超过的，心情是开心的，愿来大家再接再厉，再创辉煌，身体健康，万事如意。',
  ],
  dhy: [
    '恭喜找到自己的长征伴侣。',
    '订完婚，人生成就已达成，赶紧回来开黑！',
    '请喝趴我',
    '来了来了，干饭人，干酒人',
    '说好了，结婚我要当伴郎',
    '哥们,加油,以后工资上交,出门交代',
    '兄弟，恭喜你找到爱情的归宿',
    '要狠狠的幸福到白头^o^',
    '娶媳妇咯！心里美滋滋',
    '我给你俩幸福加点糖',
    '你我共富贵！多生孩子多种树！',
    '哦耶，我不管我最帅！',
    '今天的你们太美了',
    '恭喜你找到了今生唯一灵魂之伴侣。',
    '今天准新郎太帅了，发个大红包吧',
    '大家吃好喝好玩好，待会还有抢红包',
    '喝完喜酒，晚上麻将三缺一，来的扣666',
    '看你们订婚了，我也想找个对象',
    '已经等不及要参加你们的婚礼啦',
    '一切都是最好的安排！一定一定要幸福哦！',
    '中国首富祝你们幸福美满，永结同心',
    '大小姐一定要开心幸福啊 来自你最牢靠的粉丝后援团',
    '祝各位吃好喝好!',
    '天生才子佳人配，只羡鸳鸯不羡仙。',
    '奥利给 我最美我最帅 我是人间小可爱',
    '今晚大奖花落谁家🌸 🌸',
    '郎才女貌，瓜瓞延绵',
    '主持人帅的滑丝',
    '美满良缘，白首成约！',
    '比翼齐飞，生活更幸福！',
    '和和美美，白头偕老！',
    '嗨起来，艾瑞巴蒂',
    '珠连壁合，天作之美',
    '露出幸福真面目，只缘身在祝福中。',
    '幸福一对，幸福一生。',
    '㊗️白首成约，终身之盟，百年好合',
    '订婚快乐',
    '幸福永远哈',
    '准新郎今天也太帅了，准新娘也超级漂亮',
    '祝小郎君和小新娘永结同心',
    '火箭🚀 🚀🚀🚀 ,走一个',
    '💗💗💗！幸福呦',
    'everybaby  high 起来！',
  ],
  wl: [
    '今天来见到大家，真开心',
    '氛围太棒啦，超舒服',
    '愿咱们今天都有好收获',
    '终于来啦，满是期待',
    '和大家一起，感觉超棒',
    '盼今天每一刻都顺意',
    '精彩时刻，满心期待',
    '祝大家今天都尽兴呀',
    '这儿的感觉，太对味了',
    '希望今天满是小美好',
    '乘兴而来，兴尽而返',
    '美好时光与诸君共享',
    '感谢主办方的各项安排',
    '精彩不止一点点',
    '祝咱们都有难忘时刻',
    '就两个字：开心',
    '和朋友一起来的，真好',
    '能参与进来，真欢喜',
    '愿今天每个人都舒心',
    '一起度过这段好时光',
  ],
};
// 红包雨等待界面快捷用语
export const HBYWQUICKWISH = [
  '红包雨摇起来',
  '单身多年的手速终于排上用处了',
  '新郎官发个大红包呀',
  '红包下不停',
  '大家拿起手机，准备抢啊',
  '我的手气最旺~',
  '抢第一的再发一个，哈哈',
  '祝福阿，发红包了！',
  '红包雨走起',
  '永结同心，红包雨一直下',
  '大家赶紧扫码哦，下半场一起抢红包😝',
  '哇 发红包的老板好帅,祝老板生意兴隆',
  '不发红包雨就捣乱',
  '万水千山总是情 再发个红包行不行',
  '为红包雨而来',
  '主持人无敌帅，我要红包！',
  '坐等红包雨',
  '发红包了吗？快一点我等不及了👍👍👍',
  '司仪哥哥给个红包呗',
  '大吉大利，红包拿来',
  '大家快扫码 抢红包啦',
  '大家开开心心抢红包',
  '大家注意啦我要发大红包啦',
  '大红包是我的',
  '帅哥司仪给个红包 看看大屏幕',
  '恭喜恭喜，红包拿来',
  '感谢大家，抢红包积极参与呀！',
  '吃饭要积极，抢红包更要积极',
  '我是冲着红包来滴',
  '扫描二维码，签到，抢红包，so easy~',
  '新婚快乐红包拿来',
  '新郎官~今天的红包还不够',
  '新郎新娘红包走一圈。',
  '抢到红包开宝箱，哈哈',
  '有木有老板再来一波红包雨',
  '此地是我开，此树是我栽！红包嗖嗖到我口袋来~',
  '满月酒红包雨已准备好~',
  '盛大的婚礼必须下红包雨',
  '红包雨还不够，大家说对不对呀',
  '我要中第一名的红包，超开心🥳',
  '红包雨不要停',
  '抢个大红包，沾沾喜气',
  '红包红包我爱你、就象老鼠爱大米',
  '红包给我！伴娘送你！',
  '新郎官发红包的姿势最帅',
  '再来一次红包雨，我们不服',
  '请各位摇红包时慢点，让我体验中奖的感觉',
  '谢谢新郎新娘的红包',
  '霸气红包雨',
  '我也要大娃娃和红包',
  '帅哥司仪给个红包 祝你快点脱单',
  '快点发红包，手机没电了',
];
// 婚礼祝福语颜色
export const WISHCOLOR = [
  {
    color: '#bd38f4',
    backgroundColor: '#f4d8ff',
  },
  {
    color: '#f43838',
    backgroundColor: '#ffe5e5',
  },
  {
    color: '#f4ca38',
    backgroundColor: '#fbf7e8',
  },
];
// 弹出层模块
export const POPUP_MODULE = {
  giftModule: {
    key: 0,
    name: '礼物',
  },
  bapinModule: {
    key: 1,
    name: '祝福霸屏',
  },
  photoModule: {
    key: 2,
    name: '霸屏照片',
  },
  danmuModule: {
    key: 3,
    name: '霸气弹幕',
  },
  rechargeModule: {
    key: 4,
    name: '充值',
  },
  qrcodeModule: {
    key: 5,
    name: '二维码',
  },
  recommendGiftModule: {
    key: 6,
    name: '推荐礼物',
  },
  editInfoModule: {
    key: 7,
    name: '编辑信息',
  },
  superDanmuModule: {
    key: 8,
    name: '超级弹幕',
  },
  diamondHbModule: {
    key: 9,
    name: '喵钻红包',
  },
  diamondHbLuckyModule: {
    key: 10,
    name: '喵钻红包手气榜',
  },
  funcTipModule: {
    key: 11,
    name: '功能提示',
  },
  moreModule: {
    key: 12,
    name: '更多',
  },
  signHbModule: {
    key: 13,
    name: '签到红包',
  },
  seatModule: {
    key: 14,
    name: '席位表',
  },
  sendGiftGameModule: {
    key: 16,
    name: '送祝福游戏',
  },
  signRankModule: {
    key: 17,
    name: '签到排名',
  },
  chooseSongModule: {
    key: 18,
    name: '点歌',
  },
  relativesChooseModule: {
    key: 19,
    name: '亲友团',
  },
  lotteryNumModule: {
    key: 20,
    name: '抽奖次数',
  },
};
// 普通弹幕颜色
export const COMMON_DANMU_COLOR = ['#ef5378', '#70F0B8', '#febade'];

// 照片类型
export const PHOTO_TYPE = [
  {
    name: '小',
    size: 'small',
  },
  {
    name: '中',
    size: 'mid',
  },
  {
    name: '大',
    size: 'large',
  },
  {
    name: '霸',
    size: 'ba',
  },
];

// 弹幕类型
export const DANMU_TYPE = [
  {
    name: '蓝',
    size: 'small',
  },
  {
    name: '黄',
    size: 'mid',
  },
  {
    name: '红',
    size: 'large',
  },
];
// 超级弹幕类型
export const SUPERDANMU_TYPE = [
  {
    name: '唯美特效',
  },
  {
    name: '高贵特效',
  },
  {
    name: '至尊特效',
  },
];
// 霸屏类型
export const BAPIN_TYPE = [
  {
    color: '清新紫',
    colorCode: 'qx',
  },
  {
    color: '梦幻蓝',
    colorCode: 'mh',
  },
  {
    color: '土豪金',
    colorCode: 'yl',
  },
];
// webview容器页面(除了首页之外)
export const WEBVIEWH5 = [
  'photoWall',
  'photographerWall',
  'hotelReserve',
  'hotelDetail',
  'packageDetail',
  'menuDetail',
  'myPreferential',
  'preferentialDetail',
  'couponDetail',
  'msWeddingDressDetail',
];
// 聊天记录中的图标
export const CHATICON = {
  bapin: require('../image/hd2/bapinIconNew.png'),
  photo: require('../image/hd2/photoIconNew.png'),
  rocket: require('../image/hd2/danmuIconNew.png'),
  superDanmu: require('../image/hd2/superDanmuIcon.png'),
  hbkd: require('../image/hd2/hbkdIconNew.png'),
  photoWall: require('../image/hd2/photoWallIconNew.png'),
};
// 中式婚礼版聊天记中的图标
export const CHATICON_ZSHL = {
  bapin: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/zfhfIconEtry.png',
  photo: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/photoIcon.png',
  rocket: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/zsdm.png',
  superDanmu: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/allScreenIcon.png',
  hbkd: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/hbkdIcon.png',
  photoWall: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/photoInstant.png',
};
// 默认头像猫头
export const DEFAULTAVATAR = 'http://ustatic.joymew.com/emcee/common/b51d744c7b3f4f379d3f7f989c295daf';

// 亲友关系
export const RELATIVES = {
  0: '亲友',
  1: '父母',
  2: '舅舅',
  3: '叔叔',
  4: '伯伯',
  5: '阿姨',
  6: '姐妹',
  7: '兄弟',
  8: '朋友',
  9: '同学',
  10: '师长',
  11: '同事',
  12: '自定义',
};

/**
 * type取值格式 1(男方亲友),2(女方亲友),''或者1-1(表示男方父母)、2-1(表示女方父母)
 */
export const getRelativeTypeLabel = (type) => {
  if (type.includes('-')) {
    const tmpSubTypeInfos = type.split('-');
    const firstLevelType = tmpSubTypeInfos[0];
    const secondLevelType = tmpSubTypeInfos[1];
    const firstLevelTypeLabel = firstLevelType === '1' ? '男方' : '女方';
    let secondLevelTypeLabel;
    if (/^\d+$/.test(secondLevelType)) {
      secondLevelTypeLabel = RELATIVES[secondLevelType];
    } else {
      secondLevelTypeLabel = secondLevelType;
    }
    return `${firstLevelTypeLabel}${secondLevelTypeLabel}`;
  }
  if (type === '1') {
    return '男方亲友';
  }
  if (type === '2') {
    return '女方亲友';
  }
  return '';
};
```

## File: src/main.js
```javascript
import Vue from 'vue';
import toast from 'vue2-toast';
import vueTap from 'v-tap';
import vueScroll from 'vuescroll';
import SVGA from 'svgaplayerweb';
import {
  DatetimePicker,
  DropdownItem,
  DropdownMenu,
  Popup,
} from 'vant';
import App from './App.vue';
import router from './router';
import store from './store';
import giftDanmu from './components/Danmu/giftDanmu/main';
import rocketDanmu from './components/Danmu/rocket/main';
import bapin from './components/Bapin/main';
import enterEffect from './components/enterEffect/main';
import useTip from './components/useTip/main';
import '@/utils/hdOptimizationTmpPatch';

import './assets/styles/public.css';
import './assets/styles/toast.css';
import './assets/styles/animate.css';

Vue.use(Popup);
Vue.use(DatetimePicker);
Vue.use(DropdownItem);
Vue.use(DropdownMenu);
Vue.config.productionTip = false;
Vue.use(toast);
Vue.use(vueTap);
Vue.use(vueScroll);
Vue.use(giftDanmu);
Vue.use(rocketDanmu);
Vue.use(bapin);
Vue.use(enterEffect);
Vue.use(useTip);
Vue.prototype.$svgaParser = new SVGA.Parser();

const app = new Vue({
  router,
  store,
  render: (h) => h(App),
}).$mount('#app');

export default app;
```

## File: src/store/modules/app.js
```javascript
import { getUrlParam } from '@/utils/index';
import { getSceneInfoBySceneType } from '@/assets/constant/scene';
import live from './live';

const state = {
  loadingVisible: true,
  currentLoadingProgress: 0,
  popupAreaVisible: false,
  popupModuleKey: -1,
  token: '',
  chatAreaScrollId: '',
  previewImg: '', // 预览图片地址
  currentGiftType: '', // 当前选中的礼物类型(giftId)
  currentPhotoType: '', // 当前选中的照片类型(giftId)
  currentDanmuType: '', // 当前选中的霸气弹幕类型(giftId)
  currentBapinType: '', // 当前选中的霸屏类型(giftId)
  currentSuperDanmuType: '', // 当前选中的超级弹幕类型(giftId)
  gameBtnVisible: false, // game按钮出现与隐藏
  origin: '', // 设置进入场景 用于h5跳转小程序再返回的场景记忆(sendGift、sendBapin、sendPhoto、sendDanmu、sendRecommendGift)
  rcGiftGameCodes: [], // 每个game结束后只出现一次推荐礼物 并保存出现过的gameCode
  atText: '', // 推荐礼物的文字
  bapinCloseIconVisible: false, // 是否展示霸屏关闭按钮
  isCloseCurrentBapin: false, // 是否关闭当前霸屏
  giftSendVisible: false, // 礼物发送是否可见(礼物、霸屏、照片、霸气弹幕)
  hbkdVisible: false, // 红包口袋是否可见
  hbkdRemainVisible: false, // 红包口袋余额是否可见
  photographerVisible: false, // 摄影师照片墙是否可见
  photographerImgPrice: 0, // 摄影师照片墙照片价格
  needLogin: false,
  heartWallPrice: '0',
  editUserInfoPrice: '0',
  hotelReserveVisible: false, // 婚宴预定是否可见
  hotelReserveIcon: '', // 婚宴预定入口Icon
  isInOtherWeviewH5: false, // 是否在除了首页之外其他的webview h5
  enterEffectContainerMountedObserver: null, // 观察者对象(监听enterEffectContainer dom是否渲染完成)
  funcTipIndex: 0,
  loadAdVisible: false,
  env: 'miniProgram', // 取值miniProgram h5 tt
  inWeixinBrowse: true, // env = h5时判断是否在微信浏览器里
  bottom: 0, // 是否为全面屏
  enter: false, // 是否有导航栏
  userphone: '', // 用户电话
  isCloseCoin: false, // 取消喵币充值(直接支付)
  isGiftToHbkd: false, // 礼物进红包口袋
  inSeatQuery: false, // 席位查询中
  isHlt: '', // 定位具体的某个婚礼堂 取值39(云境)、x(xxx婚礼堂)、common ''(非婚礼堂的普通用户)
  hltHotelName: '',
  isBrideVote: false, // 打开伴郎伴娘入口
  miniProgramType: '', // 区分嗨喵和嗨猫小程序 取值hamiao(嗨喵互动)、haimao(嗨猫互动)、ledong(嗨喵乐动)、''(婚礼堂、同庆楼小程序)
  mpType: '', // 作用同miniProgramType 区别是前者用于重构前的互动小程序 后者用于重构后的互动小程序
  chooseSongVisible: false, // 点歌功能是否可见
  songSheetList: [], // 歌单列表
  // 签到红包的配置信息
  signHbConfig: {
    avator: '',
    organizer: '',
    bless: {
      lineOne: '',
      lineTwo: '',
    },
  },
  // 福利购广告是否可见
  switchFuligoAd: false,
  switchFuligoAdUrl: '',
  // 开关对象
  /**
   * {
   * switch_sgs_game: boolean,// 外场游戏开关
   * switch_sgs_game_param: string, // 外场游戏参数
   * }
   */
  switchContent: null,
  qiandaoleme: false,
};

const mutations = {
  // 保存签到红包的配置信息
  setSignHbConfig(state, data) {
    state.signHbConfig = data || {
      avator: '',
      organizer: '',
      bless: {
        lineOne: '',
        lineTwo: '',
      },
    };
  },
  setNeedLogin: (state, data) => {
    state.needLogin = data;
  },
  setLoading: (state, data) => {
    state.loadingVisible = data;
  },
  updateCurrentLoadingProgress: (state, data) => {
    state.currentLoadingProgress = `${data}%`;
  },
  setToken: (state, data) => {
    state.token = data;
  },
  setHotelConfig: (state, data) => {
    console.log('data', data);
    state.userphone = data.userphone || '';
    state.bottom = data.bottom || 0;
    if (data.enter) {
      state.enter = true;
    } else {
      state.enter = false;
    }
  },
  togglePopup: (state, data) => {
    if (!state.popupAreaVisible && data !== undefined) {
      state.popupAreaVisible = true;
      state.popupModuleKey = data;
    } else {
      state.popupModuleKey = -1;
      state.popupAreaVisible = false;
    }
  },
  setChatAreaScrollId: (state, data) => {
    state.chatAreaScrollId = data;
  },
  setPreviewImg: (state, data) => {
    state.previewImg = data;
  },
  resetPreviewImg: (state) => {
    state.previewImg = '';
  },
  setCurrentGiftType: (state, data) => {
    state.currentGiftType = data;
  },
  setCurrentPhotoType: (state, data) => {
    state.currentPhotoType = data;
  },
  setCurrentDanmuType: (state, data) => {
    state.currentDanmuType = data;
  },
  setCurrentBapinType: (state, data) => {
    state.currentBapinType = data;
  },
  setCurrentSuperDanmuType: (state, data) => {
    state.currentSuperDanmuType = data;
  },
  setGameBtnVisible: (state, data) => {
    state.gameBtnVisible = data;
  },
  setOrigin: (state, data) => {
    state.origin = data;
  },
  updateRcGiftGameCodes: (state, data) => {
    state.rcGiftGameCodes.push(data);
    state.atText = 'game结束啦送个祝福吧!';
  },
  initRcGiftAtText: (state) => {
    const tmpSceneObj = getSceneInfoBySceneType(live.state.sceneType);
    if (tmpSceneObj) {
      state.atText = tmpSceneObj.recommendGiftText;
    }
  },
  setIsCloseCurrentBapin: (state, data) => {
    state.isCloseCurrentBapin = data;
  },
  setBapinCloseIconVisible: (state, data) => {
    state.bapinCloseIconVisible = data;
  },
  setGiftSendVisible: (state, data) => {
    if (data === '0' || !data) {
      state.giftSendVisible = true;
    } else {
      state.giftSendVisible = false;
    }
  },
  setHbkdVisible: (state, data) => {
    if (data === '0' || !data) {
      state.hbkdVisible = true;
    } else {
      state.hbkdVisible = false;
    }
  },
  setHbkdRemainVisible: (state, data) => {
    if (data === '0' || !data) {
      state.hbkdRemainVisible = true;
    } else {
      state.hbkdRemainVisible = false;
    }
  },
  setHeartWallPrice: (state, data) => {
    state.heartWallPrice = data;
  },
  setEditUserInfoPrice: (state, data) => {
    state.editUserInfoPrice = data;
  },
  setPhotographerWallInfo: (state, data) => {
    state.photographerVisible = data.photo_shi_switch === '1';
    state.photographerImgPrice = parseFloat(data.photo_one_price);
  },
  setHotelReserveVisible: (state, data) => {
    state.hotelReserveVisible = data === '1';
  },
  setHotelReserveIcon: (state, data) => {
    state.hotelReserveIcon = data;
  },
  setIsInOtherWeviewH5: (state, data) => {
    state.isInOtherWeviewH5 = data;
  },
  initEnterEffectContainerMountedObserver: (state, data) => {
    state.enterEffectContainerMountedObserver = data;
  },
  updateEnterEffectContainerMountedObserver: (state, data) => {
    state.enterEffectContainerMountedObserver[data.key] = data.value;
  },
  setFuncTipIndex: (state, data) => {
    state.funcTipIndex = data;
  },
  updateLoadAd: (state) => {
    // loadAd: liveId
    if (live.state.sceneType !== '0') {
      return;
    }
    const loadAdLS = localStorage.getItem('loadAd');
    if (!loadAdLS) {
      state.loadAdVisible = true;
      localStorage.setItem('loadAd', live.state.liveId);
    } else {
      if (loadAdLS === live.state.liveId) {
        state.loadAdVisible = false;
        return;
      }
      localStorage.setItem('loadAd', live.state.liveId);
      state.loadAdVisible = true;
    }
  },
  setLoadAdVisible: (state, data) => {
    state.loadAdVisible = data;
  },
  setEnv: (state, data) => {
    state.env = data;
  },
  setInWeixinBrowse: (state, data) => {
    state.inWeixinBrowse = data;
  },
  setIsCloseCoin: (state, data) => {
    // 重构后的互动小程序默认关闭喵币支付
    if (state.mpType) {
      state.isCloseCoin = true;
    } else if (data && data === '1') {
      state.isCloseCoin = true;
    }
  },
  setIsBrideVote: (state, data) => {
    console.log('data', data);
    if (data && data === '1') {
      state.isBrideVote = true;
    } else {
      state.isBrideVote = false;
    }
  },
  setInSeatQuery: (state, data) => {
    state.inSeatQuery = data;
  },
  setIsGiftToHbkd: (state, data) => {
    if (!data || data === '0' || data === 0) {
      state.isGiftToHbkd = false;
    } else {
      state.isGiftToHbkd = true;
    }
  },
  setIsHlt: (state, data) => {
    if (data) {
      state.isHlt = data;
    }
  },
  setMiniProgramType: (state, data) => {
    if (data) {
      state.miniProgramType = data;
    }
  },
  setMpType: (state, data) => {
    if (data) {
      state.mpType = data;
    }
  },
  setHltHotelName: (state, data) => {
    state.hltHotelName = data;
    if (getUrlParam('hltHotelId') === '11') {
      state.hltHotelName = '米纱婚纱';
    }
  },
  setChooseSongVisible: (state, data) => {
    state.chooseSongVisible = data === '1';
  },
  setSongSheetList: (state, data) => {
    if (data?.list) {
      state.songSheetList = data.list;
      console.log('state.songSheetList', state.songSheetList);
    }
  },
  setSwitchFuligoAd: (state, data) => {
    const { fuliSwitch, url } = data;
    state.switchFuligoAd = fuliSwitch === true;
    state.switchFuligoAdUrl = url;
  },
  setSwitchContent: (state, data) => {
    state.switchContent = data || null;
  },
  setQiandaoleme: (state, data) => {
    state.qiandaoleme = data;
  },
};

const actions = {
  //   toggleSideBar({ commit }) {
  //     commit('TOGGLE_SIDEBAR')
  //   },
};

const getters = {
  isYj(state) {
    return state.isHlt === '39';
  },
  outerGameSwitch(state) {
    if (state.switchContent) {
      return state.switchContent.switch_sgs_game;
    }
    return false;
  },
  outerGameParam(state) {
    if (state.switchContent && state.switchContent.switch_sgs_game_param) {
      return JSON.parse(state.switchContent.switch_sgs_game_param);
    }
    return null;
  },
};

export default {
  namespaced: true,
  state,
  getters,
  mutations,
  actions,
};
```

## File: src/store/modules/chat/utils/index.js
```javascript
import { generateRandomId, getCurrentDate } from '@/utils/index';
import { getRelativeInfo, getGiftInfo } from './func';

/**
 * 格式化辅助方法——名字格式化
 */
const formatName = ({ name, sceneType }) => {
  const cutLen = sceneType === '0' ? 9 : 18;
  return name.length > cutLen ? `${name.slice(0, cutLen)}...` : name;
};

/**
 * 格式化辅助方法——某一条聊天消息格式化
 */
const formatChatItem = ({ chatItem, giftListAll, sceneType }) => {
  const chatMsg = {
    id: generateRandomId(),
    userName: formatName({ name: chatItem.miaoName, sceneType }),
    content: chatItem.miaoContent,
    headImg: chatItem.miaoTxUrl,
    photoUrl: chatItem.miaoTpUrl,
    vipLevel: chatItem.vipLevel,
    currentStatus: chatItem.miaoPosition,
    deskNum: chatItem.miaoTableNumber,
    sendDate: chatItem.sentTime,
    ...getRelativeInfo(chatItem.miaoType), // 获取亲友信息
    ...getGiftInfo({
      giftId: chatItem.miaoLiwuId,
      sceneType,
      giftListAll,
    }), // 获取发礼物信息
  };

  // 红包口袋特殊处理
  if (chatMsg.giftType === 'hbkd') {
    chatMsg.giftName = `${chatMsg.content}元${chatMsg.giftName}`;
    chatMsg.content = '';
  }

  return chatMsg;
};

/**
 * 格式化辅助方法——获取排名信息
 */
const getRankText = ({
  rank, rankCity, rankCountry, rankProvince,
}) => {
  const rankInfo = {
    city: `本市排名：${rankCity}`,
    country: `全国排名：${rankCountry}`,
    province: `本省排名: ${rankProvince}`,
  };
  return rankInfo[rank];
};

let cardChat = null;
/**
 * 获取卡片消息
 * cardJson: 与主持人相关的卡片数组，目前只有一项卡片 type为hostCard
 */
export const getCardChat = ({
  cardJson, avatar, name, rankCity, rankCountry, rankProvince,
}) => {
  if (cardChat) {
    return {
      ...cardChat,
      id: generateRandomId(),
    };
  }
  const {
    type, phone, introduce, rank, cardBg, textColor,
  } = cardJson[0];
  cardChat = {
    id: generateRandomId(),
    advertiseType: type,
    advertiseContent: {
      avatar,
      emcee_name: name,
      rank: getRankText({
        rank,
        rankCity,
        rankCountry,
        rankProvince,
      }),
      phone,
      introduce,
      cardBg,
      textColor,
    },
  };
  return cardChat;
};

/**
 * 格式化ws服务器传过来的聊天消息
 */
export const formatChat = ({ chat, giftListAll, sceneType }) => {
  const chatMsg = {
    id: generateRandomId(),
    userName: formatName({ name: chat.miaoName, sceneType }),
    content: chat.miaoBless,
    headImg: chat.miaoHeadUrl,
    photoUrl: chat.miaoTuUrl,
    vipLevel: chat.miaoVipLevel,
    currentStatus: chat.miaoPosition,
    deskNum: chat.miaoTableNumber,
    sendDate: getCurrentDate(),
    ...getRelativeInfo(chat.miaoType), // 获取亲友信息
    ...getGiftInfo({
      giftId: chat.miaoLwId,
      sceneType,
      giftListAll,
    }), // 获取发礼物信息
  };

  return chatMsg;
};

/**
 * 格式化服务端传过来的聊天记录
 */
export const formatChatList = ({ chatList, giftListAll, sceneType }) => {
  const formattedChatList = [];
  chatList.forEach((chatItem) => {
    // 格式化某一条聊天信息
    formattedChatList.push(
      formatChatItem({
        chatItem,
        giftListAll,
        sceneType,
      }),
    );
  });
  return formattedChatList;
};
```

## File: src/assets/constant/scene.js
```javascript
export const SCENE_INFO = [
  {
    sceneName: '婚礼版',
    sceneType: '0',
    // bg: require('../image/hd2/hunli-bg-new.png'),
    bg: 'https://static.hudongmiao.com/joymewH5/img/hlbg_compressed2.png',
    recommendGiftText: '送我们一个新婚祝福吧',
  },
  {
    sceneName: '中式婚礼版',
    sceneType: '91',
    bg: 'https://ustatic.joymew.com/joymewScreen/zshl/mobile/zsbgs.png',
    recommendGiftText: '送我们一个新婚祝福吧',
  },
  {
    sceneName: '年会版',
    sceneType: '1',
    bg:
      'https://static.hudongmiao.com/joymewH5/img/enterprise/bg.png',
    recommendGiftText: '送给企业一个未来祝福吧',
  },
  {
    sceneName: '生日版',
    sceneType: '2',
    bg: 'https://static.hudongmiao.com/joymewMp/joymewIndex/birthBg3.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '宝宝宴',
    sceneType: '21',
    bg: 'https://static.hudongmiao.com/joymewH5/img/birthPhoneBg2.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '寿宴',
    sceneType: '22',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/syMobileBg3.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '成人礼',
    sceneType: '23',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/crlMobileBg4.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '百露宴',
    sceneType: '24',
    bg: 'https://static.hudongmiao.com/joymewMp/bly/blyBg.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '满月宴',
    sceneType: '25',
    bg: 'https://static.hudongmiao.com/joymewMp/myyBg.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '圆锁宴',
    sceneType: '26',
    bg: 'https://static.hudongmiao.com/joymewMp/joymewIndex/birthBg3.png',
    recommendGiftText: '送我一个生日祝福吧',
  },
  {
    sceneName: '毕业礼',
    sceneType: '41',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/bydlMobileBg.png',
    recommendGiftText: '送我一个毕业祝福吧',
  },
  {
    sceneName: '谢师宴',
    sceneType: '42',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/xsyMobileBg.png',
    recommendGiftText: '送我一个祝福吧',
  },
  {
    sceneName: '金榜题名',
    sceneType: '43',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/jbtmMobileBg2.png',
    recommendGiftText: '送我一个祝福吧',
  },
  {
    sceneName: '同学会',
    sceneType: '51',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/txhBg.png',
    recommendGiftText: '送我一个祝福吧',
  },
  {
    sceneName: '乔迁宴',
    sceneType: '52',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/qqyBg.png',
    recommendGiftText: '送我一个祝福吧',
  },
  {
    sceneName: '会销',
    sceneType: '53',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/hxBg.png',
    recommendGiftText: '送我一个祝福吧',
  },
  {
    sceneName: '订婚宴',
    sceneType: '54',
    bg: 'https://static.joymew.com/joymewMp/joymewIndex/dhyMobileBg.png',
    recommendGiftText: '送我一个祝福吧',
  },
  {
    sceneName: '文旅版',
    sceneType: '55',
    bg: 'https://ustatic.hudongmiao.com/joymewMp/joymewIndex/wlInnerBg.png',
    recommendGiftText: '送我一个祝福吧',
  },
];
export const getSceneInfoBySceneType = (pSceneType) => {
  const tmpLen = SCENE_INFO.length;
  let tmpObj = null;
  for (let i = 0; i < tmpLen; i += 1) {
    if (SCENE_INFO[i].sceneType === pSceneType) {
      tmpObj = SCENE_INFO[i];
      break;
    }
  }
  return tmpObj;
};
```

## File: src/router/index.js
```javascript
import Vue from 'vue';
import VueRouter from 'vue-router';

const VueRouterPush = VueRouter.prototype.push;
const VueRouterReplace = VueRouter.prototype.replace;
VueRouter.prototype.push = function push(to) {
  return VueRouterPush.call(this, to).catch((err) => err);
};

VueRouter.prototype.replace = function replace(to) {
  return VueRouterReplace.call(this, to).catch((err) => err);
};
Vue.use(VueRouter);

export const routes = [
  {
    path: '/error',
    name: 'error',
    component: () => import('@/views/error/index.vue'),
    meta: {
      title: '错误提示',
    },
  },
  {
    path: '/',
    name: 'index2',
    component: () => import('@/views/index/index.vue'),
    meta: {
      title: '嗨喵悦动',
    },
  },
  {
    path: '/hby',
    name: 'hby',
    component: () => import('@/views/hby/index.vue'),
    meta: {
      title: '红包雨',
    },
  },
  {
    path: '/hbyWedding',
    name: 'hbyWedding',
    component: () => import('@/views/hby/wedding/index.vue'),
    meta: {
      title: '全场红包雨',
    },
  },
  {
    path: '/shake',
    name: 'shake',
    component: () => import('@/views/shake/v2/index.vue'),
    meta: {
      title: '摇一摇',
    },
  },
  {
    path: '/moneyTree',
    name: 'moneyTree',
    component: () => import('@/views/shake/moneyTree/index.vue'),
    meta: {
      title: '摇钱树',
    },
  },
  {
    path: '/shakeDragon',
    name: 'shakeDragon',
    component: () => import('@/views/shake/dragon/index.vue'),
    meta: {
      title: '飞龙在天',
    },
  },
  {
    path: '/cattleShake',
    name: 'cattleShake',
    component: () => import('@/views/cattleShake/index.vue'),
    meta: {
      title: '谁最牛',
    },
  },
  {
    path: '/dragonBoatTeamShake',
    name: 'dragonBoatTeamShake',
    component: () => import('@/views/dragonBoatTeamShake/index.vue'),
    meta: {
      title: '赛龙舟',
    },
  },
  {
    path: '/countMoney',
    name: 'countMoney',
    component: () => import('@/views/countMoney/index.vue'),
    meta: {
      title: '数钞票',
    },
  },
  {
    path: '/pigOut',
    name: 'pigOut',
    component: () => import('@/views/pigOut/index.vue'),
    meta: {
      title: '狼吞虎咽',
    },
  },
  {
    path: '/vote',
    name: 'vote',
    component: () => import('@/views/vote/voteNew.vue'),
    meta: {
      title: '投票',
    },
  },
  {
    path: '/cutfruit',
    name: 'cutfruit',
    component: () => import('@/views/cutfruit/index.vue'),
    meta: {
      title: '切水果',
    },
  },
  {
    path: '/photographerWall',
    name: 'photographerWall',
    component: () => import('@/views/photographerWall/index.vue'),
    meta: {
      title: '现场照片',
    },
  },
  {
    path: '/bubbleSign',
    name: 'bubbleSign',
    component: () => import('@/views/bubbleSign/index.vue'),
    meta: {
      title: '手写签到',
    },
  },
  {
    path: '/clickHb',
    name: 'clickHb',
    component: () => import('@/views/clickHb/index.vue'),
    meta: {
      title: '点红包',
    },
  },
  {
    path: '/hotelReserve',
    name: 'hotelReserve',
    component: () => import('@/views/hotelReserve/index.vue'),
    meta: {
      title: '婚宴预定',
    },
  },
  {
    path: '/hotelDetail',
    name: 'hotelDetail',
    component: () => import('@/views/hotelReserve/hotelDetail.vue'),
    meta: {
      title: '宴会厅',
    },
  },
  {
    path: '/packageDetail',
    name: 'packageDetail',
    component: () => import('@/views/hotelReserve/discountDetail.vue'),
    meta: {
      title: '优惠活动',
    },
  },
  {
    path: '/menuDetail',
    name: 'menuDetail',
    component: () => import('@/views/hotelReserve/menuDetail.vue'),
    meta: {
      title: '婚宴菜单',
    },
  },
  {
    path: '/couponDetail',
    name: 'couponDetail',
    component: () => import('@/views/hotelReserve/couponDetail.vue'),
    meta: {
      title: '优惠详情',
    },
  },
  {
    path: '/msWeddingDressDetail',
    name: 'msWeddingDressDetail',
    component: () => import('@/views/hotelReserve/packageDetail.vue'),
    meta: {
      title: '精品单品详情',
    },
  },
  {
    path: '/jumpBone',
    name: 'jumpBone',
    component: () => import('@/views/jumpBone/index.vue'),
    meta: {
      title: '跳一跳',
    },
  },
  {
    path: '/giveMark',
    name: 'giveMark',
    component: () => import('@/views/giveMark/index.vue'),
    meta: {
      title: '评分',
    },
  },
  {
    path: '/guessHbPay',
    name: 'guessHbPay',
    component: () => import('@/views/guessHbPay/index.vue'),
    meta: {
      title: '猜红包支付',
    },
  },
  {
    path: '/rechargeWedding',
    name: 'rechargeWedding',
    component: () => import('@/views/rechargeWedding/index.vue'),
    meta: {
      title: '充值中心',
    },
  },
  {
    path: '/rechargeOther',
    name: 'rechargeOther',
    component: () => import('@/views/rechargeOther/index.vue'),
    meta: {
      title: '充值中心',
    },
  },
  {
    path: '/hbkdRecharge',
    name: 'hbkdRecharge',
    component: () => import('@/views/hbkdRecharge/index.vue'),
    meta: {
      title: '红包口袋',
    },
  },
  {
    path: '/zyz',
    name: 'zyz',
    component: () => import('@/views/zyz/index.vue'),
    meta: {
      title: '转一转',
    },
  },
  {
    path: '/nyn',
    name: 'nyn',
    component: () => import('@/views/nyn/index.vue'),
    meta: {
      title: '扭一扭',
    },
  },
  {
    path: '/hbWall',
    name: 'hbWall',
    component: () => import('@/views/hbWall/index.vue'),
    meta: {
      title: '红包墙',
    },
  },
  {
    path: '/kbx',
    name: 'kbx',
    component: () => import('@/views/kbx/index.vue'),
    meta: {
      title: '开宝箱',
    },
  },
  {
    path: '/duiduipeng',
    name: 'duiduipeng',
    component: () => import('@/views/duiduipeng/index.vue'),
    meta: {
      title: '对对碰',
    },
  },
  {
    path: '/guessHb',
    name: 'guessHb',
    component: () => import('@/views/guessHb/index.vue'),
    meta: {
      title: '猜红包',
    },
  },
  {
    path: '/sign',
    name: 'sign',
    component: () => import('@/views/sign/index.vue'),
    meta: {
      title: '签到',
    },
  },
  {
    path: '/feedback',
    name: 'feedback',
    component: () => import('@/views/feedback/index.vue'),
    meta: {
      title: '反馈投诉',
    },
  },
  {
    path: '/couponRank',
    name: 'couponRank',
    component: () => import('@/components/gameRank/couponRank.vue'),
    meta: {
      title: '带优惠券的排行榜',
    },
  },
  {
    path: '/estimate',
    name: 'estimate',
    component: () => import('@/views/estimate/index.vue'),
    meta: {
      title: '主持评分',
    },
  },
  {
    path: '/clickTiger',
    name: 'clickTiger',
    component: () => import('@/views/clickTiger/index.vue'),
    meta: {
      title: '武松打虎',
    },
  },
  {
    path: '/seat',
    name: 'seat',
    component: () => import('@/views/seat/seat.vue'),
    meta: {
      title: '席位表',
    },
  },
  {
    path: '/brideVote',
    name: 'brideVote',
    component: () => import('@/views/brideVote/index.vue'),
    meta: {
      title: '伴郎伴娘',
    },
  },
  {
    path: '/playFootball',
    name: 'playFootball',
    component: () => import('@/views/playFootball/index.vue'),
    meta: {
      title: '谁是射手王',
    },
  },
  {
    path: '/myPreferential',
    name: 'MyPreferential',
    component: () => import('@/views/hotelReserve/MyPreferential.vue'),
    meta: {
      title: '我的优惠',
    },
  },
  {
    path: '/preferentialDetail',
    name: 'PreferentialDetail',
    component: () => import('@/views/hotelReserve/preferentialDetail.vue'),
    meta: {
      title: '奖品详情',
    },
  },
  {
    path: '/basketball-shoot',
    name: 'basketball-shoot',
    component: () => import('@/views/BasketballShoot.vue'),
    meta: {
      title: '篮球',
    },
  },
  {
    path: '/majiang',
    name: 'majiang',
    component: () => import('@/views/majiang/majiang.vue'),
    meta: {
      title: '雀神大赛',
    },
  },
  {
    path: '/happyQA',
    name: 'happyQA',
    component: () => import('@/views/happyQA/happyQA.vue'),
    meta: {
      title: '开心问答',
    },
  },
  {
    path: '/guessLanternRiddle',
    name: 'guessLanternRiddle',
    component: () => import('@/views/guessLanternRiddle/index.vue'),
    meta: {
      title: '猜灯谜',
    },
  },
  {
    path: '/dragonPlayBead',
    name: 'dragonPlayBead',
    component: () => import('@/views/dragonPlayBead/index.vue'),
    meta: {
      title: '游龙戏珠',
    },
  },
  {
    path: '/goldenSnake',
    name: 'goldenSnake',
    component: () => import('@/views/goldenSnake/index.vue'),
  },
  {
    path: '/playFireworks',
    name: 'playFireworks',
    component: () => import('@/views/playFireworks/index.vue'),
    meta: {
      title: '放鞭炮',
    },
  },
  {
    path: '/wishTreeLottery',
    name: 'wishTreeLottery',
    component: () => import('@/views/wishTreeLottery/index.vue'),
    meta: {
      title: '许愿树抽奖',
    },
  },
];

const router = new VueRouter({
  mode: 'hash',
  routes,
});

router.beforeEach((to, from, next) => {
  console.log(from);
  if (to.meta.title) {
    document.title = to.meta.title;
  }
  next();
});
export default router;
```

## File: src/utils/service.js
```javascript
// 业务相关的工具方法
import store from '@/store/index';
import {
  PHOTO_TYPE, DANMU_TYPE, SUPERDANMU_TYPE, POPUP_MODULE, WISH, QUICKWISHES,
} from '../assets/constant/index';
import { generateRandom } from './index';
import { tmpAdjustGameUrl } from './hdOptimizationTmpPatch';

// 格式化礼物列表
export const formatGiftList = (giftList = []) => {
  const result = [];
  let tempArr = [];

  for (let i = 0; i < giftList.length; i += 1) {
    tempArr.push({
      id: giftList[i].id,
      giftId: giftList[i].giftconst,
      name: giftList[i].giftname,
      giftImg: giftList[i].imglink,
      price: parseFloat(giftList[i].giftprice),
    });
    if ((i !== 0 && (i + 1) % 8 === 0) || i === giftList.length - 1) {
      result.push(tempArr);
      tempArr = [];
    }
  }
  return result;
};

// 格式化照片类型列表
export const formatPhotoTypeList = (photoTypeList) => {
  const result = [];
  for (let i = 0; i < photoTypeList.length; i += 1) {
    result.push({
      id: photoTypeList[i].id,
      giftId: photoTypeList[i].giftconst,
      name: PHOTO_TYPE[i].name,
      size: PHOTO_TYPE[i].size,
      price: parseFloat(photoTypeList[i].giftprice),
      time: photoTypeList[i].couponinfo,
    });
  }
  return result;
};

// 格式化霸气弹幕类型列表
export const formatDanmuTypeList = (danmuTypeList) => {
  const result = [];
  const DANMU_TYPE_ZSHL = ['龍', '鳳', '麒麟'];
  for (let i = 0; i < danmuTypeList.length; i += 1) {
    result.push({
      id: danmuTypeList[i].id,
      giftId: danmuTypeList[i].giftconst,
      name: store.state.live.sceneType !== '91' ? DANMU_TYPE[i].name : DANMU_TYPE_ZSHL[i],
      size: DANMU_TYPE[i].size,
      wish: danmuTypeList[i].giftname,
      price: parseFloat(danmuTypeList[i].giftprice),
    });
  }
  return result;
};
// 格式化超级弹幕类型列表
export const formatSuperDanmuTypeList = (superDanmuTypeList) => {
  const result = [];
  for (let i = 0; i < superDanmuTypeList.length; i += 1) {
    result.push({
      id: superDanmuTypeList[i].id,
      giftId: superDanmuTypeList[i].giftconst,
      price: parseFloat(superDanmuTypeList[i].giftprice),
      time: superDanmuTypeList[i].shijian,
      giftname: SUPERDANMU_TYPE[i].name,
    });
  }
  return result;
};
// 格式化霸屏类型列表
export const formatBapinTypeList = (bapinTypeList) => {
  const result = [];
  for (let i = 0; i < bapinTypeList.length; i += 1) {
    result.push({
      id: bapinTypeList[i].id,
      giftId: bapinTypeList[i].giftconst,
      giftname: bapinTypeList[i].giftname,
      price: parseFloat(bapinTypeList[i].giftprice),
      shijian: bapinTypeList[i].shijian,
    });
  }
  return result;
};
/** 通过gameCode获取game的一些常量
 * @param gameCode 游戏code
 * @parma wsData websocket数据
 * @return {{enterType: string, gameUrl: string, needShake: boolean}} gameInfo
 */
export const getGameInfoByGameCode = (gameCode, wsData = null) => {
  // TODO 后续改成从路由meta信息中获取并生成map，然后根据gameCode获取，
  // NOTENEW 后续这些数据直接在大屏初始化的时候就传过来，不需要再根据gameCode判断生成

  // 之所以使用in而不是wsData?.h5GameInfo?.属性名，是因为needShake可能为false导致判断不准确
  if (wsData?.h5GameInfo && 'enterType' in wsData?.h5GameInfo && 'gameUrl' in wsData?.h5GameInfo && 'needShake' in wsData?.h5GameInfo) {
    return {
      enterType: wsData.h5GameInfo.enterType,
      gameUrl: wsData.h5GameInfo.gameUrl,
      needShake: wsData.h5GameInfo.needShake,
    };
  }

  const gameInfo = {
    enterType: 'h5',
    gameUrl: '',
    needShake: false,
  };
  if (store.state.app.env === 'miniProgram' || store.state.app.env === 'tt') {
    switch (gameCode) {
      case 'hmPlay3':
        // 扭一扭
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/nyn/nyn?userId=${store.state.user.userId}&openId=${store.state.user.openId}&name=${store.state.user.name}&headImg=${store.state.user.headImg}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay4':
        // 转一转
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/zyz/zyz?userId=${store.state.user.userId}&openId=${store.state.user.openId}&zyzList=${store.state.live.zyzList}&name=${store.state.user.name}&headImg=${store.state.user.headImg}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay30':
      case 'hmPlay31':
        // 喊红包
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/shoutHb/index?userId=${store.state.user.userId}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay21':
        // 幸运小转盘
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/luckyWheel/luckyWheel?userId=${store.state.user.userId}&openId=${store.state.user.openId}&zyzList=${store.state.live.zyzList}&name=${store.state.user.name}&headImg=${store.state.user.headImg}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay1':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/hby';
        gameInfo.needShake = true;
        break;
      case 'hmPlay26':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/hbyWedding';
        gameInfo.needShake = true;
        break;
      case 'hmPlay6':
        // 摇一摇
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/shake';
        gameInfo.needShake = true;
        break;
      case 'hmPlay33':
        // 摇钱树
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/moneyTree';
        gameInfo.needShake = true;
        break;
      case 'hmPlay34':
        // 放鞭炮
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/playFireworks';
        gameInfo.needShake = true;
        break;
      case 'hmPlay8':
        // 谁最牛
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/cattleShake';
        gameInfo.needShake = true;
        break;
      case 'hmPlay27':
        // 飞龙在天
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/shakeDragon';
        gameInfo.needShake = true;
        break;
      case 'hmPlay28':
        // 游龙戏珠
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/dragonPlayBead';
        gameInfo.needShake = true;
        break;
      case 'hmPlay7':
        // 数钞票
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/countMoney';
        gameInfo.needShake = false;
        break;
      case 'hmPlay9':
        // 切水果
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/cutFruit';
        gameInfo.needShake = false;
        break;
      case 'hmPlay17':
        // 狼吞虎咽
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/pigOut';
        gameInfo.needShake = false;
        break;
      case 'hmPlay18':
        // 武松打虎
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/clickTiger';
        gameInfo.needShake = false;
        break;
      case 'hmPlay32':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/goldenSnake';
        gameInfo.needShake = false;
        break;
      case 'hmPlay35':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/wishTreeLottery';
        gameInfo.needShake = false;
        break;
      case 'hmPlay20':
        // 踢足球
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/playFootball';
        gameInfo.needShake = false;
        break;
      case 'hmPlay2':
        // 开宝箱
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/kbx/kbx?userId=${store.state.user.userId}&openId=${store.state.user.openId}&name=${store.state.user.name}&headImg=${store.state.user.headImg}&isForbidBuyHbq=${store.state.user.isForbidBuyHbq}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay5':
        // 红包墙
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/hbWall/hbWall?userId=${store.state.user.userId}&openId=${store.state.user.openId}&name=${store.state.user.name}&headImg=${store.state.user.headImg}&isForbidBuyHbq=${store.state.user.isForbidBuyHbq}`;
        gameInfo.needShake = false;
        break;
      case 'vote':
        // 投票
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/vote';
        gameInfo.needShake = false;
        break;
      case 'hmPlay10':
        // 手写签名
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/bubbleSign';
        gameInfo.needShake = false;
        break;
      case 'hmPlay11':
        // 点红包
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/clickHb';
        gameInfo.needShake = false;
        break;
      case 'hmPlay12':
        // 赛龙舟
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/dragonBoatTeamShake';
        gameInfo.needShake = true;
        break;
      case 'hmPlay13':
        // 跳一跳
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/jumpBone';
        gameInfo.needShake = false;
        // gameInfo.enterType = 'thirdParty';
        // gameInfo.gameUrl = `/miniGame/templeEscape/index.html?splid=${store.state
        //   .live.liveId}&userId=${store.state.user.userId}&token=${store.state.app
        //   .token}`;
        // gameInfo.needShake = false;
        break;
      case 'hmPlay14':
        // 评分
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/giveMark';
        gameInfo.needShake = false;
        break;
      case 'hmPlay15':
        // 猜红包
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/guessHb/guessHb?userId=${store.state.user.userId}&openId=${store.state.user.openId}&name=${store.state.user.name}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay16':
        // 争分夺秒
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/zfdm/zfdm?userId=${store.state.user.userId}&openId=${store.state.user.openId}&name=${store.state.user.name}&headImg=${store.state.user.headImg}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay19':
        // 送祝福
        gameInfo.enterType = 'popup';
        gameInfo.gameUrl = 16;
        gameInfo.needShake = false;
        break;
      case 'hmPlay22':
        // 对对碰
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/duiduipeng';
        gameInfo.needShake = false;
        break;
      case 'hmPlay23':
        // 兔子投篮
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/basketball-shoot';
        gameInfo.needShake = false;
        break;
      case 'hmPlay24':
        // 雀神大赛
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/majiang';
        gameInfo.needShake = false;
        break;
      case 'hmPlay25':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/happyQA';
        gameInfo.needShake = false;
        break;
      case 'hmPlay29':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/guessLanternRiddle';
        gameInfo.needShake = false;
        break;
      default:
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '我是默认地址';
        gameInfo.needShake = false;
    }
  } else if (store.state.app.env === 'h5') {
    switch (gameCode) {
      case 'hmPlay3':
        // 扭一扭
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/nyn';
        gameInfo.needShake = false;
        break;
      case 'hmPlay4':
        // 转一转
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/zyz';
        gameInfo.needShake = false;
        break;
      case 'hmPlay21':
        // 幸运小转盘
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/luckyWheel';
        gameInfo.needShake = false;
        break;
      case 'hmPlay1':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/hby';
        gameInfo.needShake = true;
        break;
      case 'hmPlay26':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/hbyWedding';
        gameInfo.needShake = true;
        break;
      case 'hmPlay6':
        // 摇一摇
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/shake';
        gameInfo.needShake = true;
        break;
      case 'hmPlay8':
        // 谁最牛
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/cattleShake';
        gameInfo.needShake = true;
        break;
      case 'hmPlay27':
        // 飞龙在天
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/shakeDragon';
        gameInfo.needShake = true;
        break;
      case 'hmPlay28':
        // 游龙戏珠
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/dragonPlayBead';
        gameInfo.needShake = true;
        break;
      case 'hmPlay33':
        // 摇钱树
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/moneyTree';
        gameInfo.needShake = true;
        break;
      case 'hmPlay34':
        // 放鞭炮
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/playFireworks';
        gameInfo.needShake = true;
        break;
      case 'hmPlay7':
        // 数钞票
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/countMoney';
        gameInfo.needShake = false;
        break;
      case 'hmPlay9':
        // 切水果
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/cutFruit';
        gameInfo.needShake = false;
        break;
      case 'hmPlay17':
        // 狼吞虎咽
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/pigOut';
        gameInfo.needShake = false;
        break;
      case 'hmPlay18':
        // 武松打虎
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/clickTiger';
        gameInfo.needShake = false;
        break;
      case 'hmPlay35':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/wishTreeLottery';
        gameInfo.needShake = false;
        break;
      case 'hmPlay32':
        // 金蛇纳福
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/goldenSnake';
        gameInfo.needShake = false;
        break;
      case 'hmPlay20':
        // 踢足球
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/playFootball';
        gameInfo.needShake = false;
        break;
      case 'hmPlay2':
        // 开宝箱
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/kbx';
        gameInfo.needShake = false;
        break;
      case 'hmPlay5':
        // 红包墙
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/hbWall';
        gameInfo.needShake = false;
        break;
      case 'vote':
        // 投票
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/vote';
        gameInfo.needShake = false;
        break;
      case 'hmPlay10':
        // 手写签名
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/bubbleSign';
        gameInfo.needShake = false;
        break;
      case 'hmPlay11':
        // 点红包
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/clickHb';
        gameInfo.needShake = false;
        break;
      case 'hmPlay12':
        // 赛龙舟
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/dragonBoatTeamShake';
        gameInfo.needShake = true;
        break;
      case 'hmPlay13':
        // 跳一跳
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/jumpBone';
        gameInfo.needShake = false;
        break;
      case 'hmPlay14':
        // 评分
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/giveMark';
        gameInfo.needShake = false;
        break;
      case 'hmPlay15':
        // 猜红包
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/guessHb';
        gameInfo.needShake = false;
        break;
      case 'hmPlay16':
        // 争分夺秒
        gameInfo.enterType = 'mp';
        gameInfo.gameUrl = `/pages/zfdm/zfdm?userId=${store.state.user.userId}&openId=${store.state.user.openId}`;
        gameInfo.needShake = false;
        break;
      case 'hmPlay19':
        // 送祝福
        gameInfo.enterType = 'popup';
        gameInfo.gameUrl = 16;
        gameInfo.needShake = false;
        break;
      case 'hmPlay22':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/duiduipeng';
        gameInfo.needShake = false;
        break;
      case 'hmPlay23':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/basketball-shoot';
        gameInfo.needShake = false;
        break;
      case 'hmPlay24':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/majiang';
        gameInfo.needShake = false;
        break;
      case 'hmPlay25':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/happyQA';
        gameInfo.needShake = false;
        break;
      case 'hmPlay29':
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '/guessLanternRiddle';
        gameInfo.needShake = false;
        break;
      default:
        gameInfo.enterType = 'h5';
        gameInfo.gameUrl = '我是默认地址';
        gameInfo.needShake = false;
    }
  }
  /**
   * 临时兼容的代码块
   * 互动小程序进行了分包优化，游戏地址发生了改变
   * 待其他小程序优化好后删除当前代码、并将gameUrl调整为新的地址
   */
  if (gameInfo.enterType === 'mp' && store.state.app.mpType) {
    tmpAdjustGameUrl(gameInfo);
  }
  return gameInfo;
};

// 推荐礼物自动弹出(无操作30s后自动弹出)
export const recommendGiftLogic = () => {
  let recommendCount = -1; // 推荐礼物弹出计时器
  const emptyOperateTime = process.env.NODE_ENV === 'production' ? 30 : 3; // 空操作时间
  // 重置弹出礼物定时器
  const resetRecommendInterval = () => {
    recommendCount = -1;
  };
  // 定时器
  const recommendInterval = setInterval(() => {
    recommendCount += 1;

    if (recommendCount >= emptyOperateTime) {
      // 被拉黑不弹出推荐礼物
      if (store.state.user.isForbidBuyHbq) {
        clearInterval(recommendInterval);
        return;
      }
      // 字节小程序不弹出推荐礼物
      if (store.state.app.env === 'tt') {
        clearInterval(recommendInterval);
        return;
      }
      // 如果设置了礼物发送不可见则不弹出推荐礼物
      if (!store.state.app.giftSendVisible) {
        clearInterval(recommendInterval);
        return;
      }
      // 弹出层正在展示中则重置定时器
      if (store.state.app.popupModuleKey > -1) {
        console.log('***弹出层正在展示中***');
        console.log(store.state.app.popupModuleKey);
        resetRecommendInterval();
        return;
      }

      // 当前在game中(不包括签到)则重置定时器
      if ((store.state.game.gameStatus === 1 || store.state.game.gameStatus === 2) && store.state.game.currentGameCode !== 'sign') {
        resetRecommendInterval();
        return;
      }
      // 限制每次进入只自动弹出1次
      let recommendGiftFlag = localStorage.getItem('recommendGiftFlag');
      if (recommendGiftFlag) {
        clearInterval(recommendInterval);
        localStorage.removeItem('recommendGiftFlag');
        console.log('***recommendGift auto popup one times***');
        return;
      }
      recommendGiftFlag = 1;
      localStorage.setItem('recommendGiftFlag', recommendGiftFlag);
      store.commit('app/togglePopup', 6);
    }
  }, 1000);
  return resetRecommendInterval;
};

// 功能提示自动弹出(无操作40s后自动弹出)
export const funcTipLogic = () => {
  let funcTipCount = -1; // 功能提示弹出计时器
  const emptyOperateTime = process.env.NODE_ENV === 'production' ? 40 : 10; // 空操作时间
  // 重置功能提示定时器
  const resetFuncTipInterval = () => {
    funcTipCount = -1;
  };
  // 获取带弹出功能提示的索引
  const getIndex = (cIndexs) => {
    const originIndexs = [0, 1, 2, 3, 4];
    let resultIndex = -1;
    if (!cIndexs) {
      resultIndex = generateRandom(0, 5);
    } else {
      const tempIndexs = [];
      for (let i = 0; i < 5; i += 1) {
        if (cIndexs.indexOf(originIndexs[i]) === -1) {
          tempIndexs.push(originIndexs[i]);
        }
      }
      const tempLen = tempIndexs.length;
      if (tempLen > 0) {
        resultIndex = tempIndexs[generateRandom(0, tempLen)];
      }
    }
    return resultIndex;
  };
  // 弹出提示
  const popupFuncTip = (fIndex) => {
    store.commit('app/setFuncTipIndex', fIndex);
    store.commit('app/togglePopup', POPUP_MODULE.funcTipModule.key);
  };
  // 定时器
  const funcTipInterval = setInterval(() => {
    funcTipCount += 1;

    if (funcTipCount >= emptyOperateTime) {
      // 被拉黑不弹出功能提示
      if (store.state.user.isForbidBuyHbq) {
        clearInterval(funcTipInterval);
        return;
      }
      // 字节小程序不弹出功能提示
      if (store.state.app.env === 'tt') {
        clearInterval(funcTipInterval);
        return;
      }
      // 非婚礼版、非中式婚礼版不弹出功能提示
      if (!['0', '91'].includes(store.state.live.sceneType)) {
        clearInterval(funcTipInterval);
        return;
      }
      // 如果设置了礼物发送不可见则不弹出功能提示
      if (!store.state.app.giftSendVisible) {
        clearInterval(funcTipInterval);
        return;
      }
      // 弹出层正在展示中则重置定时器
      if (store.state.app.popupModuleKey > -1) {
        console.log('***弹出层正在展示中***');
        console.log(store.state.app.popupModuleKey);
        resetFuncTipInterval();
        return;
      }

      // 当前在game中(不包括签到)则重置定时器
      if ((store.state.game.gameStatus === 1 || store.state.game.gameStatus === 2) && store.state.game.currentGameCode !== 'sign') {
        resetFuncTipInterval();
        return;
      }
      // 限制每场活动进入只自动弹出5次
      // funcTipInfo: {liveId,indexs:[0,1,2,3,4]}
      const funcTipInfoStr = localStorage.getItem('funcTipInfo');
      if (funcTipInfoStr) {
        const funcTipInfo = JSON.parse(funcTipInfoStr);
        if (funcTipInfo.liveId !== store.state.live.liveId) {
          // 新的活动
          localStorage.removeItem('funcTipInfo');
          const cIndex = getIndex();

          console.log(`弹出${cIndex}`);
          popupFuncTip(cIndex);
          const tempObjStr = JSON.stringify({
            liveId: store.state.live.liveId,
            indexs: [cIndex],
          });
          localStorage.setItem('funcTipInfo', tempObjStr);
          resetFuncTipInterval();
        } else {
          const cIndex = getIndex(funcTipInfo.indexs);
          if (cIndex === -1) {
            console.log('本场活动功能提示已全部弹出过啦!');
            clearInterval(funcTipInterval);
          } else {
            console.log(`弹出${cIndex}`);
            popupFuncTip(cIndex);
            funcTipInfo.indexs.push(cIndex);
            const tempObjStr = JSON.stringify({
              ...funcTipInfo,
            });
            localStorage.setItem('funcTipInfo', tempObjStr);
            resetFuncTipInterval();
          }
        }
      } else {
        const cIndex = getIndex();
        console.log(`弹出${cIndex}`);
        popupFuncTip(cIndex);
        const tempObjStr = JSON.stringify({
          liveId: store.state.live.liveId,
          indexs: [cIndex],
        });
        localStorage.setItem('funcTipInfo', tempObjStr);
        resetFuncTipInterval();
      }
    }
  }, 1000);
  return resetFuncTipInterval;
};

// 根据key查找弹出模块
export const getPopModuleByKey = (key) => {
  const moduleKeys = Object.keys(POPUP_MODULE);
  const tmpLen = moduleKeys.length;
  let tmpResult = null;
  for (let i = 0; i < tmpLen; i += 1) {
    if (POPUP_MODULE[moduleKeys[i]].key === key) {
      tmpResult = POPUP_MODULE[moduleKeys[i]];
      break;
    }
  }
  return tmpResult;
};

// hotelInfo存入localStorage
// tObj格式{key(所要保存的值的键名) value(所要保存的值)}
export const saveHotelInfoToLocal = (tObj) => {
  const hotelReserveInfoStr = localStorage.getItem('hotelReserveInfo');
  if (!hotelReserveInfoStr) {
    const tmpObj = {
      currentId: '',
      menuList: [],
      banquetList: [],
      setMealList: [],
      discountLIst: [],
      couponList: [],
    };
    tmpObj[tObj.key] = tObj.value;
    localStorage.setItem('hotelReserveInfo', JSON.stringify(tmpObj));
  } else {
    const tmpObj2 = JSON.parse(hotelReserveInfoStr);
    tmpObj2[tObj.key] = tObj.value;
    localStorage.setItem('hotelReserveInfo', JSON.stringify(tmpObj2));
  }
};
// 读取hotelInfo从localStorage
export const getHotelInfoFromLocal = (key) => {
  let result;
  const hotelReserveInfoStr = localStorage.getItem('hotelReserveInfo');
  if (hotelReserveInfoStr) {
    const tmpObj = JSON.parse(hotelReserveInfoStr);
    result = tmpObj[key];
  }
  return result;
};

// 根据sceneType获取祝福语
export const getWishBySceneType = (sceneType, returnType) => {
  let tmpWishList;
  if (sceneType === '0') {
    tmpWishList = WISH.wedding;
  } else if (sceneType === '1') {
    tmpWishList = WISH.annualMeeting;
  } else if (sceneType === '2' || sceneType === '26') {
    tmpWishList = WISH.birth;
  } else if (sceneType === '21') {
    tmpWishList = WISH.bby;
  } else if (sceneType === '22') {
    tmpWishList = WISH.sy;
  } else if (sceneType === '23') {
    tmpWishList = WISH.crl;
  } else if (sceneType === '24') {
    tmpWishList = WISH.bly;
  } else if (sceneType === '25') {
    tmpWishList = WISH.myy;
  } else if (sceneType === '41') {
    tmpWishList = WISH.bydl;
  } else if (sceneType === '42') {
    tmpWishList = WISH.xsy;
  } else if (sceneType === '43') {
    tmpWishList = WISH.jbtm;
  } else if (sceneType === '51') {
    tmpWishList = WISH.txh;
  } else if (sceneType === '52') {
    tmpWishList = WISH.qqy;
  } else if (sceneType === '53') {
    tmpWishList = WISH.hx;
  } else if (sceneType === '54') {
    tmpWishList = WISH.dhy;
  } else if (sceneType === '91') {
    tmpWishList = WISH.wedding;
  } else if (sceneType === '55') {
    tmpWishList = WISH.wl;
  }
  let tmpResult;
  if (returnType === 'list') {
    tmpResult = tmpWishList;
  } else {
    const tmpWishListLen = tmpWishList.length;
    tmpResult = tmpWishList[generateRandom(0, tmpWishListLen)];
  }
  return tmpResult;
};
// 根据sceneType获取快捷祝福语
export const generateQuickWishBySceneType = (sceneType, returnType) => {
  let tmpWishList;
  if (sceneType === '0') {
    tmpWishList = QUICKWISHES.wedding;
  } else if (sceneType === '1') {
    tmpWishList = QUICKWISHES.annualMeeting;
  } else if (sceneType === '2' || sceneType === '26') {
    tmpWishList = QUICKWISHES.birth;
  } else if (sceneType === '21') {
    tmpWishList = QUICKWISHES.bby;
  } else if (sceneType === '22') {
    tmpWishList = QUICKWISHES.sy;
  } else if (sceneType === '23') {
    tmpWishList = QUICKWISHES.crl;
  } else if (sceneType === '24') {
    tmpWishList = QUICKWISHES.bly;
  } else if (sceneType === '25') {
    tmpWishList = QUICKWISHES.myy;
  } else if (sceneType === '41') {
    tmpWishList = QUICKWISHES.bydl;
  } else if (sceneType === '42') {
    tmpWishList = QUICKWISHES.xsy;
  } else if (sceneType === '43') {
    tmpWishList = QUICKWISHES.jbtm;
  } else if (sceneType === '51') {
    tmpWishList = QUICKWISHES.txh;
  } else if (sceneType === '52') {
    tmpWishList = QUICKWISHES.qqy;
  } else if (sceneType === '53') {
    tmpWishList = QUICKWISHES.hx;
  } else if (sceneType === '54') {
    tmpWishList = QUICKWISHES.dhy;
  } else if (sceneType === '55') {
    tmpWishList = QUICKWISHES.wl;
  }
  let tmpResult;
  if (returnType === 'list') {
    tmpResult = tmpWishList;
  } else {
    const tmpWishListLen = tmpWishList.length;
    tmpResult = tmpWishList[generateRandom(0, tmpWishListLen)];
  }
  return tmpResult;
};

export const getSeatPopupFlag = () => {
  // seatPopup
  let seatPopup = localStorage.getItem('seatPopup');
  if (seatPopup && seatPopup !== store.state.live.liveId) {
    // 新的活动
    localStorage.removeItem('seatPopup');
    localStorage.removeItem('seatMy');
    localStorage.removeItem('seatSearchList');
    seatPopup = null;
  }
  return seatPopup;
};
export const updateSeatPopupFlag = () => {
  localStorage.setItem('seatPopup', store.state.live.liveId);
};

export const removeSeatPopupFlag = () => {
  localStorage.removeItem('seatPopup');
  localStorage.removeItem('seatMy');
  localStorage.removeItem('seatSearchList');
};
```
