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
- Only files matching these patterns are included: api, assets/constant, components, pages, utils, libs, app.js, app.json, package.json
- Files matching patterns in .gitignore are excluded
- Files matching default ignore patterns are excluded
- Files are sorted by Git change count (files with more changes are at the bottom)

# Directory Structure
```
api/index/index.js
api/login.js
api/system.js
app.js
app.json
assets/constant/default.js
assets/constant/host.js
components/authDialogNew/authDialogNew.js
components/authDialogNew/authDialogNew.json
components/authDialogNew/authDialogNew.ttml
components/authDialogNew/authDialogNew.ttss
components/sign/sign.js
components/sign/sign.json
components/sign/sign.ttml
components/sign/sign.ttss
components/signCustom/signCustom.js
components/signCustom/signCustom.json
components/signCustom/signCustom.ttml
components/signCustom/signCustom.ttss
components/signLz/signLz.js
components/signLz/signLz.json
components/signLz/signLz.ttml
components/signLz/signLz.ttss
libs/svgaplayer.weapp.js
package.json
pages/hotelReserve/couponDetail/couponDetail.js
pages/hotelReserve/couponDetail/couponDetail.json
pages/hotelReserve/couponDetail/couponDetail.ttml
pages/hotelReserve/couponDetail/couponDetail.ttss
pages/hotelReserve/hotelDetail/hotelDetail.js
pages/hotelReserve/hotelDetail/hotelDetail.json
pages/hotelReserve/hotelDetail/hotelDetail.ttml
pages/hotelReserve/hotelDetail/hotelDetail.ttss
pages/hotelReserve/hotelReserve.js
pages/hotelReserve/hotelReserve.json
pages/hotelReserve/hotelReserve.ttml
pages/hotelReserve/hotelReserve.ttss
pages/hotelReserve/menuDetail/menuDetail.js
pages/hotelReserve/menuDetail/menuDetail.json
pages/hotelReserve/menuDetail/menuDetail.ttml
pages/hotelReserve/menuDetail/menuDetail.ttss
pages/hotelReserve/packageDetail/packageDetail.js
pages/hotelReserve/packageDetail/packageDetail.json
pages/hotelReserve/packageDetail/packageDetail.ttml
pages/hotelReserve/packageDetail/packageDetail.ttss
pages/index/index.js
pages/index/index.json
pages/index/index.ttml
pages/index/index.ttss
pages/joymewIndex/joymewIndex.js
pages/joymewIndex/joymewIndex.json
pages/joymewIndex/joymewIndex.ttml
pages/joymewIndex/joymewIndex.ttss
pages/live/live.js
pages/live/live.json
pages/live/live.ttml
pages/live/live.ttss
utils/date.js
utils/index.js
utils/request.js
utils/storage.js
```

# Files

## File: api/index/index.js
```javascript
import {
request,
requestH5 } from
'../../utils/request';
import { getLiveId } from '../../utils/storage';

const app = getApp();
//验证司仪
export function validateEmcee() {
  return request('emceeUser/validate', 'POST', {});
}

//获取活动信息
export function getLiveInfo() {
  return request('wxScan/saiYaRen', 'POST', {
    splid: getLiveId()
  });
}

// 获取签到状态
export function getSignInState() {
  return request('hmScanReportController/getQianDaoInfo', 'GET', {
    splid: getLiveId()
  });
}
// 签到
export function signIn(paramObj) {
  return request('hmScanReportController/qianDao', 'POST', {
    avator: app.globalData.userInfo.avatarUrl,
    splid: getLiveId(),
    bless_str: paramObj.wish,
    wx_name: paramObj.name,
    phonenumber: paramObj.userPhone ? paramObj.userPhone : '',
    type: paramObj.role,
    birthDate: paramObj.birthDate,
    gender: paramObj.gender
  });
}

// 获取聊天记录
export function getMsgInfo() {
  return requestH5('wxScan/getMsgInfo', 'GET', {
    splid: getLiveId(),
    num: 1,
    size: 30
  });
}

// 发送聊天消息
export function sendChatMessage(message) {
  return requestH5('sendMsgController/msgGo6', 'POST', {
    splid: getLiveId(),
    content: message,
    color: 0
  });
}

// 保存签到信息(h5授权前调用)
export function saveSignInfo({
  splid = getLiveId(),
  bless_str = '',
  phonenumber = '',
  type = '',
  birthDate = '',
  gender = '',
  redirect_url = ''
}) {
  return request('hmScanReportController/saveQianDaoParam', 'POST', {
    splid,
    bless_str,
    phonenumber,
    type,
    birthDate,
    gender,
    redirect_url
  });
}
```

## File: api/login.js
```javascript
import { request } from '../utils/request.js';
/**
 * 抖音登录获取code
 */
export function wxLogin() {
  return new Promise((resolve, reject) => {
    tt.login({
      timeout: 10000,
      success: (result) => {
        resolve(result);
      },
      fail: () => {
        reject(1);
      }
    });
  });
}

// 用户授权new
export function authUserNew({
  dy_appid,
  code,
  anonymous_code,
}) {
  return request('dyScan/oauth_user', 'POST', {
    code,
    anonymous_code,
    dy_appid,
    // dy_appid: 'tt42b93404dd85d9cb01',
    cancelLoading: true
  });
}


export function wxGetUserInfoNew() {
  return new Promise((resolve, reject) => {
    tt.getUserProfile({
      force: true,
      success: (result) => {
        resolve(result);
      },
      fail: (err) => {
        reject(err);
      }
    });
  });
}


// 授权获取手机号(新版获取手机号,不需要提前login)
export function authGetPhoneByCode(paramObj) {
  return request('wxScan/getPhoneNumber', 'POST', {
    code: paramObj.code,
    type: paramObj.type // 4:嗨猫 3:婚礼堂 1:默认 2:婚礼人
  });
}


// 授权获取手机号(旧版获取手机号,需要提前login)
export function authGetPhoneMiaoShop(paramObj) {
  return request('wxScan/authPhoneMiao', 'POST', {
    encryptedData: paramObj.encryptedData,
    iv: paramObj.iv
  });
}

// 查看用户是否关注抖音号
export function checkFollowState(awemeId) {
  return new Promise((resolve, reject) => {
    tt.checkFollowAwemeState({
      awemeId,
      success: (res) => {
        resolve(res);
      },
      fail: (err) => {
        reject(err)
      },
    });
  })
}

// 引导关注抖音号
export function followAwemeUser(awemeId) {
  return new Promise((resolve, reject) => {
    tt.followAwemeUser({
      awemeId,
      success: (res) => {
        resolve(res);
      },
      fail: (err) => {
        reject(err);
      }
    });
  })
}
```

## File: api/system.js
```javascript
import { showWxToast } from '../utils/index';

const TEMPLATEID = 'RyXJFlmR_oSJfxaWTJ5Hgsq83n37Px_04FcCMwylFcE';

// 检查小程序更新
export function checkSystemUpdate() {
  const updateManager = tt.getUpdateManager();

  updateManager.onCheckForUpdate(function (res) {
    // 请求完新版本信息的回调
    console.log('onCheckForUpdate', res.hasUpdate);
  });

  updateManager.onUpdateReady(function () {
    tt.showModal({
      title: '更新提示',
      content: '新版本已经准备好，是否重启应用？',
      success: function (res) {
        if (res.confirm) {
          // 新的版本已经下载好，调用 applyUpdate 应用新版本并重启
          updateManager.applyUpdate();
        }
      }
    });
  });

  updateManager.onUpdateFailed(function () {
    // 新版本下载失败
    showWxToast('新版本下载失败!');
  });
}

//获取系统信息
export function getSystemInfo() {
  return new Promise((resolve, reject) => {
    tt.getSystemInfo({
      success: (result) => {
        resolve(result);
      },
      fail: () => {
        reject(1);
      }
    });
  });
}

//获取用户的当前设置(是否授权过等信息)
export function getSetting() {
  return new Promise((resolve, reject) => {
    tt.getSetting({
      success: (result) => {
        resolve(result);
      },
      fail: () => {
        reject(1);
      }
    });
  });
}


// 下载文件
export function wxDownloadFile(filePath) {
  return new Promise((resolve, reject) => {
    tt.downloadFile({
      url: filePath,
      success: (res) => {
        resolve(res);
      },
      fail: (err) => {
        reject(err);
      }
    });
  });
}

// 文件保存到相册
export function wxSaveFileToAlbum(tmpFilePath) {
  return new Promise((resolve, reject) => {
    tt.saveImageToPhotosAlbum({
      filePath: tmpFilePath,
      success: (res) => {
        resolve(res);
      },
      fail: (err) => {
        reject(err);
      }
    });
  });
}
```

## File: app.js
```javascript
import { checkSystemUpdate } from './api/system.js';
import {
  setUserInfo,
  getUserInfo,
  setUserPhone,
  getUserPhone
} from
  './utils/storage.js';

App({
  onLaunch: function (e) {
    //检查小程序更新
    checkSystemUpdate();
    console.log('场景值：', e.scene);
  },
  onHide: function () { },
  globalData: {
    // 授权登录后获取的用户基本信息
    userInfo: {
      // 测试用待修改
      // nickName: '汪元会',
      // avatarUrl: 'https://thirdwx.qlogo.cn/mmopen/vi_32/sw36m5OS67agMibBw1ulocBjr5Hmv0zOkylyq7HrG3UD2ERQ2ux9IrMT1v7AxTrCgFmMnnb9QKPFtLyR80picBFA/132',
      nickName: '',
      avatarUrl: ''
    },
    activityTitle: '', // 活动标题
    h5Url: '', // live h5地址
    isH5NeedRefresh: false, // live h5是否需要刷新
    nynRechargeIndex: 0, //索引 扭一扭充值列表的索引
    nynLuckyIndex: 0, //索引 扭一扭中奖列表的索引
    zfdmIndex: 0, // 索引 争分夺秒消息队列的索引
    zfdmId: '', // 争分夺秒轮次id
    sceneType: '0', // 活动版本
    nynList: [],
    luckyWheelPrizeItemList: [], // 幸运小转盘奖品列表
    userPhone: '',
    dy_appid: '',
    dy_bind_id: '69803373412', // 上小官抖音号
    // 测试用待修改
    // nynList: [{code:"0",desc:"谢谢参与"},{code:"4",desc:"18元"},{code:"5",desc:"58.8元"},{code:"6",desc:"88.8元"},{code:"7",desc:"28.8元"},{code:"8",desc:"68.8元"},{code:"9",desc:"38.8元"},{code:"10",desc:"谢谢参与"}],
  },
  setUserInfo(paramObj) {
    if (paramObj) {
      this.globalData.userInfo.nickName = paramObj.nickName;
      this.globalData.userInfo.avatarUrl = paramObj.avatarUrl;
      setUserInfo({
        nickName: paramObj.nickName,
        avatarUrl: paramObj.avatarUrl
      });
    } else {
      const stUserInfo = getUserInfo();
      this.globalData.userInfo.nickName = stUserInfo.nickName;
      this.globalData.userInfo.avatarUrl = stUserInfo.avatarUrl;
    }
  },
  setH5Url(url) {
    this.globalData.h5Url = url;
  },
  setUserPhone(phone) {
    if (phone) {
      this.globalData.userPhone = phone;
      setUserPhone(phone);
    } else {
      const stUserPhone = getUserPhone();
      this.globalData.userPhone = stUserPhone || '';
    }
  },
  updateNynRechargeIndex() {
    this.globalData.nynRechargeIndex += 1;
  },
  updateNynLuckyIndex() {
    this.globalData.nynLuckyIndex += 1;
  },
  initZfdmId(id) {
    if (!this.globalData.zfdmId) {
      // 首次玩
      this.globalData.zfdmId = id;
    } else if (this.globalData.zfdmId !== id) {
      // 新的一轮索引需要重置
      this.globalData.zfdmId = id;
      this.resetZfdmIndex();
    }
  },
  updateZfdmIndex() {
    this.globalData.zfdmIndex += 1;
  },
  resetZfdmIndex() {
    this.globalData.zfdmIndex = 0;
  },
  setDyappid(dyappid) {
    this.globalData.dy_appid = dyappid;
  },
  setDyBindId(dy_bind_id) {
    this.globalData.dy_bind_id = dy_bind_id;
  }
});
```

## File: app.json
```json
{
    "pages": [
        "pages/joymewIndex/joymewIndex",
        "pages/index/index",
        "pages/live/live",
        "pages/hotelReserve/hotelReserve",
        "pages/hotelReserve/packageDetail/packageDetail",
        "pages/hotelReserve/menuDetail/menuDetail",
        "pages/hotelReserve/hotelDetail/hotelDetail",
        "pages/hotelReserve/couponDetail/couponDetail"
    ],
    "window": {
        "backgroundTextStyle": "light",
        "navigationBarBackgroundColor": "#fff",
        "navigationBarTitleText": " 嗨喵悦动",
        "navigationBarTextStyle": "black",
        "onReachBottomDistance": 100
    },
    "sitemapLocation": "sitemap.json",
    "resolveAlias": {
        "@/*": "/*"
    }
}
```

## File: assets/constant/default.js
```javascript
export default {
  defaultHeadImg: 'https://ustatic.hudongmiao.com/joymewMp/defaultHeadImg2.png',
  wishesWedding: [
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
  '珠联壁合洞房春暖，花好月圆鱼水情深！'],

  wishesAnnualMeeting: [
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
  '十全十美峥嵘榜，周天日月齐光芒！'],

  wishesBirth: [
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
  '快意人生勤登攀，乐娱生日庆华年！'],

  wishesBBY: [
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
  '愿所有的幸福，所有的快乐，所有的温馨，所有的好运，永远围绕在宝宝身边。'],

  wishesSY: [
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
  '安逸静谧的晚年，一种休息，一种愉悦，一种至高的享受!祝您福如东海长流水寿比南山不老松!'],

  wishesCRL: [
  '愿此去前程似锦 再相逢依旧少年',
  '愿你走到哪里都不缺重头再来的勇气',
  '愿你的未来，要咩有咩，前程似锦，踮到飞起',
  '愿你出走半生 归来仍是少年',
  '愿你成为自己的太阳 不必凭借谁的光',
  '愿你 有良善、有勇气、有梦想、有担当、有满满的爱。',
  '愿你开启一段新的美丽人生!愿你真诚、美丽、善良',
  '成人告别幼稚走向成熟,克服依赖,走向独立，愿你今后的每一天万事顺意，不惧风雨，勇往直前',
  '成年了可以放心大胆谈恋爱了'],

  wishesBLY: [
  '祝孩子像林间的仙子一样快乐幸福，歌声相伴，美满一生!',
  '百日宝宝百岁康，岁岁岁平安，祝您宝宝平安又健康!',
  '感谢你，宝贝。因为你，花朵开放，随你而来的满天希望!',
  '宝贝。你生命的每一次扬帆出海。我的祝福都会伴你同行!',
  '百年百月百天，长久长顺长安',
  '青春、阳光、欢笑，为这属于你的日子，舞出欢乐的节拍。'],

  wishesMYY: [
  '一月已满，健康快乐，平安成长，更加欣喜，举杯同庆。',
  '满月宴，祝福满满，健康满满，幸福满满，快乐满满。',
  '美好到，得小宝。命运好，才情高。合家欢，父母笑。',
  '宝宝降临，全家欢笑，再无烦绕；宝宝一笑，万事变好。',
  '祝愿宝宝，满月快乐，健康围绕，乐得逍遥！',
  '宝宝满月到，幸福吹响集结号，喜鹊鸿雁传喜报，远亲近邻都请到！',
  '喜气伴绕；恭喜喜得宝宝，开心常绕',
  '宝宝满月，送去满满的祝愿：愿工资涨满，广开财源，多赚宝宝的奶粉钱！'],

  wishesBYDL: [
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
  '毕业了，懂得什么是友谊，懂得了什么是师生情。'],

  wishesXSY: [
  '这人生的旅途上，感谢有您的教诲。是您给了我无尽的信心和勇气，为我点燃了希望之灯，让我遨游在知识的海洋。谢谢您，亲爱的老师！',
  '鸦反哺，羊跪乳。学子永记教师恩。青山绕绿水，老师恩情长又长。路边花，雪中草，没有恩师都会倒山再高，水再深，没有老师恩情真！',
  '男老师，赛雄狮；女老师，赛西施。教我们求真务实，实事求是！祝老师们时时开心，事事顺心，世世代代受人爱戴尊敬！',
  '蜗居三尺天地，教鞭指扬文字，粉尘挥洒知识，育出满天桃李。笑容堆积，是您辛劳后的欣喜，开心依旧，是祝您幸福无比，祝老师万事如意。',
  '您工作在今朝，却建设着祖国的明天；您教学在课堂，成就却在祖国的四面八方',
  '不计辛勤一砚寒，桃熟流丹，李熟枝残。种花容易树人难，幽谷飞香不一般诗满人间，画满人间。英才济济笑开颜。',
  '恩师掠起心中责，传道授业向人间；不计辛勤播希望，浇灌未来育新苗；两袖清风任劳怨，桃李满园笑开颜。教师节来临，在此道一声，老师，您辛苦了，愿您幸福安康，快乐一生！',
  '在您关怀的目光之下，给予了我无尽的信心和勇气！您是我永远的老师！衷心祝您健康幸福！在教师节到来之际，祝我亲爱的老师，身体健康！永远快乐！',
  '现在，一切都过去了，可它变成为亲切的回忆了，我怀念着您带我们走过的分分秒秒！老师，祝福您：桃李满天下，春晖遍四方！',
  '在我们从幼稚走向成熟，从愚昧走向文明的路上，您用生命的.火炬，为我们开道。',
  '对于您教诲的苦心，我无比感激，并将铭记于心！',
  '老师，离别虽然久长，而您那形象仿佛是一个灿烂发亮的光点，一直在我的心中闪烁。',
  '一个个日子升起又降落，一届届学生走来又走过，不变的是您深沉的爱和灿烂的笑容。祝福您亲爱的老师。',
  '燃烧自己，照亮学生；人民教师，教书育人。春风化雨，塑造灵魂；茁壮成长，难忘师恩！',
  '你有父亲严厉的一面，有母亲慈祥的一面，有朋友知心的一面，感谢您的指引，感谢您的教诲，感谢您的关心。',
  '您的岗位永不调换，您的足迹却遍布四方；您的两鬓会有一天斑白，您的青春却百年不衰。',
  '有了你，我的一生才精彩！！谢谢你！我的老师！',
  '教师是火种，点燃了学生的心灵之火；教师是石级，承受着学生一步步踏实地向上攀登。',
  '真空、坚定、谦逊、朴素――这是您教给我唱的歌，这是您指引我走的人生之路。',
  '老师，您是我心中最重量级的人物，您的教导我记心上，您的教育我记心间，您的教诲我记心里',
  '师恩常常基于无声的关怀，往往耐人寻味；但只有感，才能懂得它的珍贵。',
  '亲情血浓于水；友情彼此安慰；爱情相依相偎；师生情如同亲朋，关爱教诲；愿您生活美满，身体康泰！',
  '老师您好！是您的心血撒遍了广大莘莘学子，您的辛劳培养了新一代天之骄子，祝您身体健康。',
  '老师，感谢您用自己的生命之光，照亮了我人生的旅途。',
  '三十岁而立，报父母含辛茹苦养育之恩；二十年成才，感老师辛勤耐心教导之德。'],

  wishesJBTM: [
  '考场凯旋心欢喜，捷报传来登金榜。父母一听心落定，笑容满面报讯忙。斟酌兴趣和爱好，填报志愿有主张。祝你心想事成人欢笑，学府深造创辉煌!',
  '满池荷花送清香，喜讯传来心荡漾。忧愁烦恼一扫光，笑容满面歌声扬。金榜题名愿得偿，再入学府知识长。祝你学成归来成栋梁，为国贡献做榜样！',
  '枝头喜鹊喳喳叫，金榜题名喜讯到。亲朋好友来祝贺，父母开心脸含笑。鲤鱼今日龙门跳，进入学府再深造。他日一展凌云志，事业成功成英豪。愿你前程多美好，实现梦想步步高！',
  '芬芳满园花枝俏，捷报传来心欢笑。如风似雨清凉到，合家开怀乐淘陶。设宴举杯同庆贺，笑语盈盈共欢乐。志向高远入学府，大步迈向成功路。愿你前途无限光明。',
  '多年的寒窗苦读，终于赢得了这一激动人心的时刻，真心地祝贺你，金榜题名！',
  '功夫不负苦心人，祝贺你，终于成功了！',
  '十年寒窗苦种种，只为一朝化作龙，今日得遂凌云志，青云路上九霄冲，知你高考得成功，诚心祝福在心中，愿你的人生一路顺风。',
  '水滴石穿业精不舍，海阔天高学贵有恒。祝，金榜题名！',
  '幸福的消息在金色的季节传出，诚心的祝福由灿烂的笑脸道出！',
  '度过黑色七月，经过蓝色八月，迎来了金色九月，一个属于莘莘学子的幸运之月，祝你学习更上一层楼！',
  '虽没悬梁刺股那么悲壮，也没凿壁取光那么刻苦，但曾挑灯夜读，题海奋斗。如今金榜题名，终可施才，报效祖国，恭喜!',
  '十年扬帆征战场，今朝姓名题金榜。亲友相闻看捷报，合家雀跃欢声笑。文字绽香醉心房，伴随家人话梦想。鱼跃龙门入名校，必将成才志向高。愿你明天更灿烂。',
  '辛苦的付出，终结出了硕果；汗水的灌溉，打开了喜悦的大门。即将迈入大学之门，人生之路又开启。愿你收拾好心情，迈开愉快的脚步，让大学生活丰富多彩。朋友，祝你如意!',
  '寒窗十载，风雨千百;书山行遍，航遍学海;千磨百炼，博大胸怀;水洗浪淘，题名应该。祝贺你金榜题名，心想事成!',
  '十数寒窗受尽累，不惜青春伴书随，翼羽渐丰展风采，金榜题名唯我最!笑看成败淡浮华，挥洒青春投社会!愿你激情永不退，向着理想勇敢追!',
  '昨夜喜鹊枝头叫，出门必定行大运。寒窗苦读十二载，金榜题名看今朝。千军万马齐冲锋，早把胜算握手中。酸甜苦辣都尝遍，荆棘踏破是坦途。',
  '有志不怕年纪小，英雄不惧出身低。激情点燃竖雄心，青春作伴逐梦忙。人生谷底上坡路，高峰更望高处行。踏遍青山人不老，一事能狂便少年。',
  '如果说鼓励是一朵云，我会让你的学业路上彩云满天;如果说祝福是一片雪，我会让你学业路中瑞雪纷飞;在云儿凝结成雪的气候，你已经是心仪已久那个学府的学生。',
  '宝剑锋自磨砺出，梅花香自苦寒来。',
  '朝为田舍郎，暮登天子堂。将相本无种，男儿当自强',
  '少年自有青云志，当许天下第一流。',
  '大学，不是你堕落的开始，而是你梦想的一个新起点！拼搏吧，奋斗吧，让你的大学时光在你的人生的篇章里，充实的，无悔的淌过！',
  '春天你撒下了汗水，用一片碧绿来换取金秋的黄金满地，收获的是成功的喜悦，迈入人生另一阶段，你的生命会更加精彩。恭喜高考成功！',
  '壮志凌云，大鹏展翅日'],

  wishesTXH: [
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
  '你好，我的朋友，你一定还在忙吧，注意保重身体，你的好朋友!'],

  wishesQQY: [
  '笑语声声，共庆乔迁喜！',
  '仁里莺迁崇四美，新居燕喜庆三春！',
  '乔宅喜，天地人共喜！',
  '乔迁之喜祝福你，真诚祝福做贺礼！',
  '良辰吉日，从此金银财宝滚进门！',
  '乔迁大喜拍拍手，祝福送到喝喜酒！',
  '鞭炮啪啪啪，锣鼓铛铛铛，新天新地新福绕，新宅新院新财罩！',
  '乔新迁，好运到，入金窝，福星照！'],

  wishesHX: [
  '祝愿贵公司蓬勃发展，日胜一日!明天展会圆满成功!',
  '机遇蕴含精彩，发展充满信心，号角催人奋进。',
  '惨淡经营历千辛，一举成名天下闻，虎啸龙吟展宏图，盘马弯弓创新功!',
  '团结，是一个重要的精神，一个人要想成功，要有能够同别人合作的精神！',
  '事业是连结我们的纽带，愿我们的事业旺发达，友谊之花也随之盛开！',
  '祝你一气呵成马到成功，一帆风顺事业有成，一鸣惊人大展宏图，一年到头和和美美快快乐乐',
  '成就是辉煌的，业绩是突出的，目标是超过的，心情是开心的，愿来大家再接再厉，再创辉煌，身体健康，万事如意。'],

  commentDanmu: [
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/7caf15e372604102aeee963d75b2768b',
    comment: '主持人普通话说滴杠杠滴，😄幽默风趣，很不错！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/be4285f66ab243bb868fac7ba4e4dc19',
    comment: '声音音好好听，气氛活跃互动精彩'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/46baed054d9649e4955dcc4fa9a56553',
    comment: '主持人真的太棒了风趣幽默可动精彩活跃多才多艺而且人长得太帅了和太酷了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/8f0dfeb8425144508e1139fed41f7388',
    comment: '主持人帅哥你太棒了，希望几年后我们也能够请您帮儿子主持婚礼'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/7a7b0d7763e2430595966d015369292b',
    comment: '主持人帅气，风趣幽默，多才多艺，有机会会推荐朋友'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/826189c5cabc4a0bbce00eb036164b12',
    comment: '非常难忘的一次婚礼，新娘太美了！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/e8fc93d922ce43c395a89e4e2872eebe',
    comment: '幽默风趣,举止文雅,优雅大方型,温暖阳光'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/95f5831d6a294298b05ad0925b4cb55d',
    comment: '主持小哥哥声音好听，主持氛围也很不错；互动较强。棒棒哒！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/e9c03d76d1f44bf2ad9f1ccab784fe9c',
    comment: ',主持人今天晚上说的非常棒，多才多艺'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/054dc1930af4434687cc56fedadd7db5',
    comment: '互动动精精彩气氛活、跃风趣幽默主持人辛苦了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/de0c871f15de4b91b53143b3a4dcb0a3',
    comment: '遇见的都是天意，拥有的都是幸运'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/a6e7486e3c684e26a832b62d54ce383b',
    comment: '主持人声音真的很赞'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/8db03d1957e84d16a2495c5e31c4881c',
    comment: '气氛很好，主持人很赞/:strong '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/42ee2ed12f06478b9065ed1d80df5477',
    comment: '有趣的一场婚宴'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/9e60e611b92c4668bb08d07d8f1474a7',
    comment: '气氛活跃！金牌主持！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/6bbcf56bb69b42779e1cdc5676366c98',
    comment: '主持人帅气且且多才多多艺风趣幽默，主持辛苦了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/ee6539d289464f85a79e6c0be44b254e',
    comment: '司仪气氛拿捏的相当可以，可是我没红包没奖品，没娃娃'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/ec85b975240b481d843bc5bc6f5c2690',
    comment: '互动做的很好，整个环节安排的环环相扣'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/c903f512edfd46358234f5446cce8a0f',
    comment: '主持人帅气多才多艺，现场气氛活跃，互动相当精彩，婚礼在欢快的氛围中圆满结束！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/3457b5391a3944bfa9b882d46358e597',
    comment: '主持好帅,牛，牛，牛'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d10c27b7250b4d24975d55dd6c036887',
    comment: '50块钱很开心哈哈哈哈哈'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/a91b2655840b45deb5e2008f13e82689',
    comment: '我很喜欢这的主持人'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/f29814ab9c6845018ddcf4a89a9c71a0',
    comment: '气氛搞的很嗨，主持人也很棒'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/b70536b6c16c4e0a9ce1b79668fde844',
    comment: '司仪小哥辛苦了！婚礼很棒'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/efe8e550a0b349a29d490f1dc3c1d407',
    comment: '额，又碰见了😆 😆 '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/9130a8326af945e9997dfa2b220ccf5a',
    comment: '辛苦啦，如果结婚，肯定是我的首选对象'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/85a406981e0c425f8e74938821e0a317',
    comment: '帅气十足主持人，气氛活跃精彩，体验感超好'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/dc69a13ce76c4ed2a0e9a730e28fd168',
    comment: '帅气十足主持人，气氛活跃精彩，体验感超好'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/3f6793bace83483c99c29ce01ceb5a47',
    comment: '主持人认真活跃且多才多艺，互动精彩，是个人才。'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/6bfd19867ffd4c689d18f7afc0dd793e',
    comment: '非常满意，非常多才多艺，气氛活跃，互动精彩，主持人辛苦啦！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/18e1c4dfaba1484b9ab5ece4241e5a53',
    comment: '多才多艺，太棒了。超喜欢你。666👍👍👍👍'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/afa8d092d8864b0b87d7f5b2220edc8f',
    comment: '主持人主持得太好了方为你点赞'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/b88d1bc61a474041b38e6f636d449312',
    comment: '优秀，才华与帅气于一身'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/53e0d99190da4abaa986de4b71308474',
    comment: '靓仔的歌声太动听了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/60f63fe1650948789fdf0ed76f5adadf',
    comment: '司仪小哥今天给了，为他点赞'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/c5307e264d494311aacd183bf7eeb139',
    comment: '整场一个人，嗨翻全场，点赞'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d59d1ff0f82b40f3bd0af22f4e6c7e8b',
    comment: '主持人太帅了 是不是单身啊'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/24538634bc36496590b550293a1e1804',
    comment: '帅哥主持人 ，口才好。带动全场氛围 ，气氛热烈 棒棒哒！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/737274a082e04f24bbf7d66b5c318cf6',
    comment: '司仪小哥们也很辛苦.谢谢你们啦'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d1ea0bf1211845ada3c1a1a80481e62f',
    comment: '不知道说什么，就说你好帅吧'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/eeb8733b8aa64223bb01b34c4a71d892',
    comment: '今天的婚宴很大气，气氛治跃，多才多艺，主持人帅，这家婚宴厅好。'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/dbc6a6e5d79d4ac4b832bcae96bcd796',
    comment: '司仪小哥帅气，有亲和力和感染力，全部棒棒哒'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/28be0f623f264d93bd5c8a06887fa9df',
    comment: '主持人幽默风趣，现场气氛搞的很活跃，漂亮'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/95be2fa6d35246329a2dd95bee69241b',
    comment: '口才惊人，喜庆连连，幽默风趣，阳光帅气'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/06b3b9a5e2594a8a930a5d49607e5dfd',
    comment: '祝福满满，金牌主持！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/1170b9843cd349ab8cd321caeaf3d8c7',
    comment: '司仪帅哥🤵‍♂️辛苦了，你的互动精神活跃气氛多才多艺的表演令人感受深刻。'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/6c0663970696460e81167e6f80f810e8',
    comment: '主持人我是你的小迷妹，哈哈哈'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/2a26b1c3aeff45c18d47262cb537e9bf',
    comment: '司仪很认真卖力 给👍 👍 👍 👍 👍 '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/fe269bc93d1a439c9426129a8a03fac4',
    comment: '喜欢你这风格'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/e16bba0fd96949b59c3667abc062848d',
    comment: '有声，有色，精彩绝伦，创意独新。'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/8ee2e4e7010a4d1d9bdf37294ca6eee0',
    comment: '主持人帅去声音效果棒气氛活跃产主持人辛苦啦！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/365f720d73db4ee5b7462e1d6edacc46',
    comment: '司仪小哥帅气爆棚，现场气氛棒棒的'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/fc53a06c05df4d4f836f542c061b3e46',
    comment: '主持的不错，可惜我没拿到奖😂 '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/1e83c099552d421398959025aa2695d8',
    comment: '司仪小哥真是多才多艺，有机会推荐给我的亲朋好友！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d9772c5871724f13b6c731806f3ec44a',
    comment: '主持很好，我家儿子结婚也选你家公司'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/6b57e181f666456e8f134ffb43baf815',
    comment: '不错不错，还有眼神示意'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/623d84fc9caa495fb5b3b73f2dd95d20',
    comment: '现场带动气氛，会场整个嗨起来啦，简直就是party 小王子。'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/63a3d4b04cea4fd48c2c8f57ac82ae58',
    comment: '完美，很喜欢这个主持人'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/c824ffa7586c4979b62f4f06f3fcfc0a',
    comment: '参加所有婚礼中最棒的主持'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/3aeb0adf007947cda011e4d9da8d9036,',
    comment: '司仪小哥哥帅气又多彩，必须五星好评！！！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/b5aad85f6d0b496bbb0ebb33b3db41dd',
    comment: '第一次遇到这么棒的主持人，祝事业蒸蒸日上'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/72e6885f0ad843ee9b4eafe36b1bb9cd',
    comment: '这是第二次遇见主持人了，实力派。'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/f6a16ba18b124898bcf5881c05d7bede',
    comment: '主持人很棒  能照顾到各个年龄段的朋友'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/72ba753c9a0a41218a06c288c1abf276',
    comment: '我的婚礼也是你主持哒 很好 '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/968842b689b84846be31506fc83b80ca',
    comment: '主持人很用心了 主持一场婚礼 '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/8383e05679074a4eaeae051518c32947',
    comment: '棒！就是办结婚早了半年，不然就选你啦'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/4b6bc47bc5684fbbb878f114cc08f5c2',
    comment: '你主持婚礼能感动全场，能把所有年龄段的人带动起来！效果杠杠的，期待你下次更精彩的场面！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/cde04dbc070b4615a037d31d1cb69683',
    comment: '果然厉害，是在下输了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d71738a2c5d34c08b40fd8423299ec75',
    comment: '这场婚礼是我目前看到的最棒的一场，气氛特别好'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/12fe9e9202cf4bb1aa2bd76abdc37143',
    comment: '下次结婚可以找你主持吗?'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/25df74f75bf64f00bc65a90d933e7556',
    comment: '下次见面多发几个红包，哈哈'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/a9e9ac9a22894ff6b6c0d4605fde7bf4',
    comment: '一个字帅，二个字特帅，三个字帅呆了！！！：五星级'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/2081aec05e714ea3aba0036ad45a5af1',
    comment: '主持人长的帅，声音好听，主要给我的小红包多多👍 '
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/52263a11a5bf44808687dcc55f41f4da',
    comment: '太棒了，参加过的婚礼当中最给力的一位主持人！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/650b2878e77049d5b8ab963f28ba2747',
    comment: '主持帅哥声音响亮，婚礼策划到位，气氛精彩幽默。为你点赞，值的五星好评'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/f6c74dca1d1e4d17b96da780f35b12aa',
    comment: '情商很高的帅哥主持'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/b796ab1e2e2f4011b54c9626f0f4e485',
    comment: '小哥哥很有礼貌 是我理想中的婚礼司仪'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/dcc05cb0a0124cb89e4f1dd797580a5a',
    comment: '给82分怕主持人骄傲，剩下的18分以666的形式给你…'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/37d6447e489f47648cb13fa31f4211d3',
    comment: '今天的婚礼让人难忘，主持人非常优秀，主持水平很高'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/383e367501394873bf03a22261b7765e',
    comment: '整场婚礼气氛非常热闹，主持人和嘉宾在互动环节合拍，最后说一句，主持人很帅！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/2963116d6c544f79a21639d3f970e6d9',
    comment: '第一次感受到什么样的婚礼叫做清新脱俗，很喜欢今天的主持人，多才多艺，礼貌友好，今天辛苦啦！希望以后结婚也能请他当主持'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/fccd0c18d27d42d99a2182865d6eabf1',
    comment: '超级有气场，活动主持的也挺棒，有是今天运气王，拿了两个大奖哦！！！'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/280df1261d5b48f6bd4f6f0febedadc0',
    comment: '主持人辛苦了，下次我儿子结婚有机会邀请你'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d7cf7d5eb8d54fe0b781c7d2c448b969',
    comment: '很6的Ck'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/6968d2f3ee94416c98e0f0ef80c7d10f',
    comment: '帅帅主持，婚礼现场气氛活跃，把控有方，希望有缘再见！为你点赞赞赞👍'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/9aca5214763348c58b2fdde0fa0aa1c0',
    comment: '主持人帅的一比'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/9aca5214763348c58b2fdde0fa0aa1c0',
    comment: '今天参加婚礼，是我第一次遇见主持人这么的帅气，多才多艺'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/5afee876c4cb4570a0ef705c363db011',
    comment: '挺棒的，接触过的这么多主持中是出类拔萃的了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/417257aa80134b9a930d4791c73c9093',
    comment: '主持人帅B了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/fac898fc909e47898570912dea8b72e6',
    comment: '说的太好了，都感动的哭了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/1a280c8e5e9f4eb7a1fa2ef984cf0332',
    comment: '加个微信我马上结婚了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/c4229f93572f43318e0a8b090b2de434',
    comment: '棒棒哒～下次结婚我也找你'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/8471484eadfc417caccd1318dcebd3b8',
    comment: '人帅声音棒，以后自己的孩子结婚也找他'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/73c32c96d380441ca6e3bf2a4cfcbdd3',
    comment: '司仪小哥绝绝子，等我结婚找你'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/aafe6fabe3c44f7d985e5916b2cf65da',
    comment: '主持人第二次遇见了，哈哈，第一次我叔叔儿子结婚，这次是舅舅儿子结婚，太有缘了，不错，互动精彩，主持人声音效果特棒，蛮好的'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/e1ba7b0ca085463ab7395899b0219c69',
    comment: '有机会的，我儿子明年也要结婚了，不晓得定的是哪家🥰🥰'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/f589128aa97e45fea0752df15838c9f3',
    comment: '可惜结婚早了'
  },
  {
    avator:
    'https://ustatic.hudongmiao.com/miao/comment/d7b7c167ace04f1fb264cb72546da461',
    comment: '留个电话，下回有活找你！'
  }],

  defaultAvatars: [
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/1.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/2.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/3.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/4.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/5.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/6.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/7.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/8.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/9.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/10.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/11.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/12.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/13.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/14.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/15.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/16.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/17.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/18.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/19.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/20.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/21.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/22.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/23.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/24.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/25.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/26.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/27.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/28.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/29.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/30.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/31.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/32.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/33.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/34.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/35.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/36.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/37.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/38.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/39.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/40.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/41.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/42.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/43.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/44.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/45.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/46.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/47.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/48.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/49.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/50.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/51.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/52.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/53.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/54.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/55.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/56.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/57.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/58.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/59.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/60.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/61.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/62.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/63.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/64.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/65.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/66.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/67.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/68.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/69.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/70.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/71.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/72.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/73.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/74.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/75.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/76.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/77.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/78.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/79.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/80.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/81.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/82.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/83.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/84.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/85.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/86.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/87.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/88.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/89.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/90.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/91.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/92.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/93.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/94.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/95.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/96.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/97.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/98.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/99.png',
  'https://ustatic.hudongmiao.com/joymewMp/defaultAvatar/100.png']

};
```

## File: assets/constant/host.js
```javascript
export const API_HOST = 'https://hm.hudongmiao.com/';
// export const API_HOST = 'http://192.168.66.8:8052/';
// export const PAGE_HOST = 'http://192.168.66.107/';
export const PAGE_HOST = 'https://shm.hudongmiao.com/';
// export const PAGE_HOST = 'http://dev.joymew.com/';
```

## File: components/authDialogNew/authDialogNew.js
```javascript
import { wxLogin, authUserNew, wxGetUserInfoNew } from '../../api/login';
import { setToken } from '../../utils/storage';
import { showWxToast, hideWxLoading } from '../../utils/index';

const app = getApp();

Component({
  /**
   * 组件的属性列表
   */
  properties: {
    dialogVisible: {
      value: false,
      type: Boolean
    }
  },
  observers: {
    'dialogVisible': function (dialogVisible) {
      if (dialogVisible) {
        // 授权的登录弹窗出现
        console.log(this.data.dialogVisible);
        this.loginSilence();
      }
    },
  },
  data: {
    needAuthGetAvatarName: false,
  },
  attached() {
  },
  /**
   * 组件的方法列表
   */
  methods: {
    loginSilence: function () {
      wxLogin().
        then((res) => {
          console.log('***wxLogin***');
          console.log(res);
          return authUserNew({
            code: res.code,
            anonymous_code: res.anonymousCode,
            dy_appid: app.globalData.dy_appid
          });
        }).then((res2) => {
          console.log('***静默授权结果***');
          console.log(res2);
          setToken(res2.data.token);
          const tmpUserInfo = res2.data.user;
          if (tmpUserInfo.avator && tmpUserInfo.wx_name) {
            app.setUserInfo({
              nickName: tmpUserInfo.wx_name,
              avatarUrl: tmpUserInfo.avator
            });
            this.triggerEvent('authSuccess');
          } else {
            // 头像昵称为空,需要授权获取
            this.setData({
              needAuthGetAvatarName: true
            });
          }
        }).
        catch((err) => {
          console.log(err);
          console.log('静默授权失败');
          this.closeAuth();
        });
    },
    closeAuth: function () {
      this.triggerEvent('authFail');
    },
    openAuthNew: function() {
      wxGetUserInfoNew().then((res) => {
        console.log('***wxGetUserInfoNew***');
        console.log(res);
        const { nickName, avatarUrl } = res.userInfo;
        app.setUserInfo({
          nickName,
          avatarUrl
        });
        this.triggerEvent('authSuccess');
      });
    }
  }
})
```

## File: components/authDialogNew/authDialogNew.json
```json
{
    "component": true
}
```

## File: components/authDialogNew/authDialogNew.ttml
```
<!-- 授权登陆 -->
<view class="authLogin {{needAuthGetAvatarName?'shade':''}}" wx:if="{{dialogVisible}}">
  <view class="authBox" wx:if="{{needAuthGetAvatarName}}">
    <image class="logoImg" src="https://ustatic.joymew.com/joymewMp/authDialog/hmLogo.png"></image>
    <view class="name"> 嗨喵悦动</view>
     <view class="btn" bindtap="openAuthNew">授权登录</view>
     <image class="closeImg" src="https://ustatic.joymew.com/joymewMp/authDialog/closeIcon.png" bindtap="closeAuth"></image>
  </view>
</view>
```

## File: components/authDialogNew/authDialogNew.ttss
```
.authLogin {
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}
.shade {
  background-color: rgba(32, 32, 32, 0.72);
}
.authLogin>.authBox {
  width: 520rpx;
  height: 600rpx;
  background-image: url('https://ustatic.joymew.com/joymewMp/authDialog/authBg.png');
  background-size: 100% 100%;
  position: absolute;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.authLogin>.authBox>.logoImg {
  width: 124rpx;
  height: 124rpx;
  position: absolute;
  top: 137rpx;
}

.authLogin>.authBox>.name {
  font-size: 36rpx;
  font-weight: bold;
  color: #313131;
  position: absolute;
  top: 288rpx;
}

.authLogin>.authBox>.btn {
  width: 300rpx;
  height: 80rpx;
  background: linear-gradient(-45deg, #FEB141, #FEC74D);
  box-shadow: 0px 12px 24px 0px rgba(254, 177, 65, 0.24);
  border-radius: 40rpx;
  font-size: 28rpx;
  font-weight: bold;
  color: #FFFFFF;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  bottom: 61rpx;
  letter-spacing: 0.5vw;
}

.authLogin>.authBox>.closeImg {
  width: 44rpx;
  height: 44rpx;
  position: absolute;
  bottom: -89rpx;
}
```

## File: components/sign/sign.js
```javascript
import { showWxToast } from '../../utils/index';
import { authGetPhoneMiaoShop } from '../../api/login';

Component({
  /**
   * 组件的属性列表
   */
  properties: {
    activityTitle: {
      value: '',
      type: String
    },
    userNameProp: {
      value: '',
      type: String
    },
    wishProp: {
      value: '',
      type: String
    },
    sceneType: {
      value: '',
      type: String
    },
    isExamine: {
      value: false,
      type: Boolean
    },
    isForcePhone: {
      value: false,
      type: Boolean
    },
    miaoShopId: {
      value: '',
      type: String
    }
  },
  observers: {
    userNameProp: function (userNameProp) {
      this.setData({
        userName: userNameProp
      });
    },
    wishProp: function (wishProp) {
      this.setData({
        wish: wishProp
      });
    },
    activityTitle: function (newVal) {
      if (newVal && newVal.indexOf('&') > -1) {
        this.setData({
          activityTitleArr: newVal.split('&')
        });
      }
    }
  },
  data: {
    role: '', // 亲友类型 1:男方亲友 2:女方亲友  '': 不选
    userName: '', // 姓名
    wish: '', // 祝福语
    gender: '0', // 性别 0:男 1:女 商城版独有
    phone: '', // 手机号 商城版
    birthDate: '', // 生日 商城版独有
    activityTitleArr: [] // 企业版标题 指定标识符&处换行
  },
  /**
   * 组件的方法列表
   */
  methods: {
    userNameBlur(e) {
      console.log('***userNameBlur***');
      this.setData({
        userName: e.detail.value
      });
    },
    wishesBlur(e) {
      console.log('***wishesBlur***');
      if (e.detail.value) {
        this.setData({
          wish: e.detail.value
        });
      }
    },
    // 选择亲友
    chooseRelatives(e) {
      console.log('***chooseRelatives***');
      console.log(e);
      this.setData({
        role: e.currentTarget.dataset.role
      });
    },
    sign() {
      if (this.data.miaoShopId) {
        this.signMiaoShop();
        return;
      }
      // if (!this.data.userName) {
      //   showWxToast('贵宾姓名不能为空!');
      //   return;
      // }
      if (!this.data.wish) {
        showWxToast('祝福语不能为空!');
        return;
      }
      // if (this.data.phone && this.data.phone.length !== 11) {
      //   showWxToast('请输入正确格式的手机号!');
      //   return;
      // }
      // 需要强制获取手机号
      // if (this.data.isForcePhone && !this.data.phone) {
      //   showWxToast('手机号不能为空!');
      //   return;
      // }
      console.log(this.data.userName);
      console.log(this.data.wish);
      console.log(this.data.role);
      this.triggerEvent('signEvent', {
        userName: this.data.userName,
        wish: this.data.wish,
        role: this.data.role,
        userPhone: this.data.phone
      });
    },
    refreshWish() {
      this.triggerEvent('refreshWishEvent');
    },
    chooseGender: function (e) {
      console.log(e.currentTarget.dataset.gender);
      this.setData({
        gender: e.currentTarget.dataset.gender
      });
    },
    getPhoneNumber: function (e) {
      console.log('*******getPhoneNumber方法内部*******');
      console.log(e.detail.iv);
      console.log(e.detail.encryptedData);
      if(!e.detail.encryptedData || !e.detail.iv) {
        console.log(e.detail.errMsg);
        return;
      }
      try {
        authGetPhoneMiaoShop({
          encryptedData: e.detail.encryptedData,
          iv: e.detail.iv
        }).
        then((res) => {
          console.log(res);
          if (res && res.phone_info && res.phone_info.phoneNumber) {
            this.setData({
              phone: res.phone_info.phoneNumber
            });
          } else {
            showWxToast('手机号获取失败!请删除小程序重新进入!');
          }
        }).
        catch((err) => {
          console.log(err);
          showWxToast(JSON.stringify(err));
        });
      } catch (err) {
        console.log(err);
        showWxToast(JSON.stringify(err));
      }
    },
    handleBirthDateChange: function (e) {
      console.log(e.detail.value);
      this.setData({
        birthDate: e.detail.value
      });
    },
    onOpenWebCastRoom(e) {
      console.log(e);
    },
    signMiaoShop: function () {
      console.log('signMiaoShop方法执行!');
      // if (!this.data.userName) {
      //   showWxToast('贵宾姓名不能为空!');
      //   return;
      // }
      if (!this.data.wish) {
        showWxToast('祝福语不能为空!');
        return;
      }
      if (!this.data.isExamine) {
        // if (!this.data.phone) {
        //   showWxToast('手机号不能为空!');
        //   return;
        // }
        // if (this.data.phone.length !== 11) {
        //   showWxToast('手机号格式错误!');
        //   return;
        // }
        // if (!this.data.birthDate) {
        //   showWxToast('请选择生日!');
        //   return;
        // }
      }
      console.log(this.data.userName);
      console.log(this.data.wish);
      console.log(this.data.phone);
      console.log(this.data.birthDate);
      console.log(this.data.gender);
      this.triggerEvent('signEvent', {
        userName: this.data.userName,
        wish: this.data.wish,
        userPhone: this.data.phone,
        birthDate: this.data.birthDate,
        gender: this.data.gender
      });
    }
  }
});
```

## File: components/sign/sign.json
```json
{"component":true}
```

## File: components/sign/sign.ttml
```
<view class="signNew">
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/weddingSignBg2022.png' class="bg" tt:if="{{sceneType === '0'}}"></image>
    <image src="https://ustatic.hudongmiao.com/joymewMp/joymewIndex/ballon2.png" class="ballon2" tt:if="{{sceneType === '0'}}"></image>
    <image src="https://ustatic.hudongmiao.com/joymewMp/joymewIndex/ballon3.png" class="ballon3" tt:if="{{sceneType === '0'}}"></image>
    <image src="https://ustatic.hudongmiao.com/joymewMp/joymewIndex/wel2022.png" class="welWedding" tt:if="{{sceneType === '0'}}"></image>
    <view class="annualBgBox" tt:if="{{sceneType === '1'}}">
        <image src='https://ustatic.hudongmiao.com/joymewMp/joymewIndex/bg-annualMeeting01.png' class="annualBg" mode="widthFix"></image>
    </view>
    <image src='https://ustatic.hudongmiao.com/joymewMp/joymewIndex/signTitle-annualMeeting03.png' class="annualSignTitle" tt:if="{{sceneType === '1'}}" mode="widthFix"></image>
    <view class="annualTitle" tt:if="{{sceneType === '1' && activityTitleArr.length === 0}}">{{activityTitle}}</view>
    <view class="annualTitle" tt:if="{{sceneType === '1' && activityTitleArr.length > 0}}">
        <view class="titleItem" tt:for="{{activityTitleArr}}" tt:for-item="item" tt:for-index="index" tt:key="index">{{item}}</view>
    </view>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/birthBg3.png' class="bg" tt:if="{{sceneType === '2'}}"></image>
    <view class="bbyBg" tt:if="{{sceneType === '21'}}"></view>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/bbyDeco02.png' class="bbyDeco02" tt:if="{{sceneType === '21'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/bbyDeco01.png' class="bbyDeco01" tt:if="{{sceneType === '21'}}"></image>
    <view class="syBgBox" tt:if="{{sceneType === '22'}}">
        <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/syMobileBg4.png' class="syBg" mode="widthFix"></image>
    </view>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/lantern.png' class="topLantern" tt:if="{{sceneType === '22'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/decoration.png' class="bottomDecoration" tt:if="{{sceneType === '22'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/crlMobileBg2.png' class="bg" tt:if="{{sceneType === '23'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/crlBottomCloud.png' class="crlBottomCloud" tt:if="{{sceneType === '23'}}"></image>
    <image src='https://ustatic.hudongmiao.com/joymewMp/bly/blyBg.png' class="bg" tt:if="{{sceneType === '24'}}"></image>
    <image src='https://ustatic.hudongmiao.com/joymewMp/myyBg.png' class="bg" tt:if="{{sceneType === '25'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/bydlBg.png' class="bg" tt:if="{{sceneType === '41'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/bydlDeco.png' class="cloud" tt:if="{{sceneType === '41'}}"></image>
    <view class="xsyBgBox" tt:if="{{sceneType === '42'}}">
        <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/xsyBg.png' class="xsyBg" mode="widthFix"></image>
    </view>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/xsyDeco.png' class="lantern" tt:if="{{sceneType === '42'}}"></image>
    <view class="jbtmBgBox" tt:if="{{sceneType === '43'}}">
        <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/jbtmBg.png' class="jbtmBg" mode="widthFix"></image>
    </view>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/jbtmCloud.png' class="jbtmCloud" tt:if="{{sceneType === '43'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/txhBg.png' class="bg" tt:if="{{sceneType === '51'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/qqyBg.png' class="bg" tt:if="{{sceneType === '52'}}"></image>
    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/hxBg.png' class="bg" tt:if="{{sceneType === '53'}}"></image>
    <view class="signBox signBox{{sceneType}}">
        <image src="https://ustatic.hudongmiao.com/joymewMp/joymewIndex/qima.gif" class="qima" tt:if="{{sceneType === '0'}}"></image>
        <image src="https://ustatic.hudongmiao.com/joymewMp/joymewIndex/ballon1.png" class="ballon1" tt:if="{{sceneType === '0'}}"></image>
        <view class="benifit" tt:if="{{sceneType === '0'}}">一起看美照、送祝福、玩游戏吧～</view>
        <!-- <view class="fItem">
            <text class="key key{{sceneType}}">姓名：</text>
            <input bindblur="userNameBlur" name="userName" placeholder='请输入您的姓名' maxlength="12" value="{{userName}}" placeholder-class="phcolor{{sceneType}}" class="ipt{{sceneType}}"></input>
        </view> -->
        <view class="fItem" tt:if="{{miaoShopId}}">
            <text class="key key{{sceneType}}">性别：</text>
            <view class="sexGroup">
                <view class="sexItem sexItem{{sceneType}}" bindtap="chooseGender" data-gender='0'>
                    <image src='https://ustatic.joymew.com/joymewMpTql/signWedding/male.png' class="sexIcon"></image>
                    男
                    <image src='https://ustatic.joymew.com/joymewMpTql/signWedding/tickedIcon.png' class="tickedIcon" tt:if="{{gender === '0'}}"></image>
                </view>
                <view class="sexItem sexItem{{sceneType}}" bindtap="chooseGender" data-gender='1'>
                    <image src='https://ustatic.joymew.com/joymewMpTql/signWedding/female.png' class="sexIcon"></image>
                    女
                    <image src='https://ustatic.joymew.com/joymewMpTql/signWedding/tickedIcon.png' class="tickedIcon" tt:if="{{gender === '1'}}"></image>
                </view>
            </view>
        </view>
        <view class="fItem" tt:if="{{!isExamine}}">
            <text class="key key{{sceneType}}">祝福语：</text>
            <input bindblur="wishesBlur" name="wishes" placeholder='祝福语' maxlength="20" value="{{wish}}" placeholder-class="phcolor{{sceneType}}" class="iptPad ipt{{sceneType}}"></input>
            <view class="refreshBtn refreshBtn{{sceneType}}" bindtap="refreshWish"></view>
        </view>
        <!-- 婚礼版独有 -->
        <view class="fItem" tt:if="{{!miaoShopId && sceneType === '0'}}">
            <text class="key key0">亲友团：</text>
            <view class="chooseGroup">
                <view class="chooseItem {{ role === '1'?'active':'' }}" catchtap="chooseRelatives" data-role="1">
                    <text>男方</text>
                </view>
                <view class="chooseItem {{ role === '2'?'active':'' }}" catchtap="chooseRelatives" data-role="2">
                    <text>女方</text>
                </view>
                <view class="chooseItem {{ role === ''?'active':'' }}" catchtap="chooseRelatives" data-role>
                    <text>不选</text>
                </view>
            </view>
        </view>
        <!-- <view class="fItem" tt:if="{{!isExamine && (isForcePhone || miaoShopId)}}">
            <text class="key key{{sceneType}}">手机号：</text>
            <view class="getPhoneIpt getPhoneIpt{{sceneType}}">
                {{phone ? phone: '获取手机号'}}
                <button open-type="getPhoneNumber" bindgetphonenumber="getPhoneNumber" class="getPhoneBtn" tt:if="{{!phone}}">
                    获取手机号
                </button>
            </view>
            <view class="phoneIconBox phoneIconBox{{sceneType}}"></view>
        </view> -->
        <!-- <view class="fItem" tt:if="{{miaoShopId}}">
            <text class="key key{{sceneType}}">生日：</text>
            <picker mode="date" bindchange="handleBirthDateChange" value="{{birthDate}}">
                <view class="birthDate">
                    <view class="val">{{birthDate === '' ? '请选择' : birthDate}}</view>
                    <image src='https://ustatic.joymew.com/joymewMp/joymewIndex/downArrow.png' class="downArrow"></image>
                </view>
            </picker>
        </view> -->
        <!-- TODO 待解开注释 -->
        <view class="signBtn signBtn{{sceneType}}" catchtap="sign">
            <text tt:if="{{sceneType !== '1'}}">点击进入</text>
        </view>
        <!-- <button open-type="openWebcastRoom" data-aweme-id="53444542032" class="signBtn signBtn{{sceneType}}" bindopenwebcastroom="onOpenWebCastRoom">跳转直播间</button> -->
        <!-- <aweme-data aweme-id="53444542032" type="avatar" style="position:fixed;top: 140rpx;left: 40rpx;"/> -->
    </view>
</view>
```

## File: components/sign/sign.ttss
```
.signNew {
  width: 100vw;
  height: 100vh;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  perspective: 4000rpx;
}
.annualBgBox {
  width: 100%;
  height: 100%;
  position: absolute;
  overflow: hidden;
}
.annualBg {
  width: 750rpx;
  position: absolute;
  top: -10rpx;
  left: 0;
}
.annualSignTitle {
  position: relative;
  width: 320rpx;
  margin-top: 80rpx;
}
.annualTitle {
  position: relative;
  color: transparent;
  background-image: linear-gradient(45deg, #e4af57, #fce688);
  font-size: 60rpx;
  padding: 0 20rpx;
  -webkit-background-clip: text;
}
.titleItem {
  color: transparent;
  background-image: linear-gradient(45deg, #e4af57, #fce688);
  font-size: 60rpx;
  padding: 0 20rpx;
  -webkit-background-clip: text;
}
.bg {
  width: 100%;
  height: 100%;
}
.bbyBg {
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: #e4c4c4;
}
.bbyDeco02 {
  width: 750rpx;
  height: 340rpx;
  position: absolute;
  top: 0;
}

.bbyDeco01 {
  width: 750rpx;
  height: 941rpx;
  position: absolute;
  top: 29rpx;
}
.syBgBox {
  width: 100%;
  height: 100%;
  position: absolute;
  overflow: hidden;
}
.syBg {
  width: 750rpx;
  position: absolute;
  top: -180rpx;
  left: 0;
}
.topLantern {
  width: 750rpx;
  height: 278rpx;
  position: absolute;
  top: 0;
}

.bottomDecoration {
  width: 750rpx;
  height: 70rpx;
  position: absolute;
  bottom: 0;
}
.crlBottomCloud {
  width: 750rpx;
  height: 198rpx;
  position: absolute;
  bottom: 0;
}
.cloud {
  width: 750rpx;
  height: 253rpx;
  position: absolute;
  bottom: 0;
}
.xsyBgBox {
  width: 100%;
  height: 100%;
  position: absolute;
  overflow: hidden;
}
.xsyBg {
  width: 835rpx;
  position: absolute;
  top: -10rpx;
  left: -12rpx;
}
.lantern {
  width: 750rpx;
  height: 151rpx;
  position: absolute;
  top: 0;
}
.jbtmBgBox {
  width: 100%;
  height: 100%;
  position: absolute;
  overflow: hidden;
}
.jbtmBg {
  width: 940rpx;
  position: absolute;
  top: -50rpx;
  left: -65rpx;
}
.jbtmCloud {
  width: 750rpx;
  height: 158rpx;
  position: absolute;
  bottom: -30rpx;
}
.signBox {
  width: 620rpx;
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: absolute;
  bottom: 80rpx;
  padding-top: 40rpx;
  padding-bottom: 40rpx;
}
/* differance */
.signBox0 {
  background-image: url('https://ustatic.joymew.com/joymewMp/joymewIndex/box-04.png');
  width: 678rpx;
}
.signBox1 {
  background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/boxQy01.png');
}
.signBox2 {
  background-color: #dbfafe;
}
.signBox21,
.signBox24,
.signBox25 {
  background-color: #f9eded;
}
.signBox22 {
  background-color: #cf1820;
}
.signBox23 {
  background-image: url('https://ustatic.joymew.com/joymewMp/joymewIndex/signBoxCrl.png');
}
.signBox41 {
  background: #d0efff;
}
.signBox42 {
  background: #fef188;
}
.signBox43 {
  background: #ffffd8;
}
.signBox51 {
  background: #2c3032;
}
.signBox52 {
  background: #ff9484;
}
.signBox53 {
  background-image: url('https://ustatic.joymew.com/joymewMp/joymewIndex/signBoxBgHX.png');
}
.benifit {
  font-size: 32rpx;
  font-weight: 400;
  color: #7a61e6;
  margin-top: 20rpx;
  margin-bottom: 30rpx;
}
.fItem {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 620rpx;
  padding: 0 40rpx;
  margin-bottom: 40rpx;
  position: relative;
}
.signBox0 .fItem {
  align-items: unset;
  flex-direction: column;
}
.key {
  font-size: 32rpx;
  font-weight: 600;
}
/* differance */
.key0 {
  color: #ee8b6b;
  margin-bottom: 20rpx;
  font-size: 28rpx;
}
.key2,
.key21,
.key23,
.key24,
.key25,
.key41,
.key42,
.key43,
.key52 {
  color: #333333;
}
.key1 {
  color: #facd7f;
}
.key22,
.key51,
.key53 {
  color: #ffffff;
}
input {
  width: 412rpx;
  height: 56rpx;
  box-sizing: border-box;
  font-size: 32rpx;
  font-weight: normal;
  border-top: none;
  border-left: none;
  border-right: none;
  outline: none;
}
/* differance */
.ipt0 {
  color: #333333;
  border-bottom: 2rpx solid #e8757e;
  width: 540rpx;
  font-size: 40rpx;
}
.ipt1,
.ipt53 {
  color: #ffffff;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.6);
}
.ipt2,
.ipt21,
.ipt24,
.ipt25 {
  color: #333333;
  border-bottom: 1rpx solid rgba(51, 51, 51, 0.6);
}
.ipt22 {
  color: #ffffff;
  border-bottom: 1rpx solid #cc8c8c;
}
.ipt23 {
  color: #333333;
  border-bottom: 1rpx solid #54d5e9;
}
.ipt41 {
  color: #333333;
  border-bottom: 1rpx solid #efd1ee;
}
.ipt42 {
  color: #333333;
  border-bottom: 1rpx solid #e20013;
}
.ipt43 {
  color: #333333;
  border-bottom: 1rpx solid #ea002a;
}
.ipt51 {
  color: #ffffff;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.6);
}
.ipt52 {
  color: #333333;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.6);
}
.phcolor0 {
  color: #000000;
}
.phcolor1,
.phcolor22,
.phcolor51 {
  color: #ffffff;
}
.phcolor2,
.phcolor23,
.phcolor25,
.phcolor41,
.phcolor42,
.phcolor43,
.phcolor52 {
  color: #333333;
}
.iptPad {
  padding-right: 70rpx;
}
.refreshBtn {
  width: 28rpx;
  height: 28rpx;
  background-size: 100% 100%;
  position: absolute;
  right: 35rpx;
  bottom: 17rpx;
}
.qima {
  width: 260rpx;
  height: 220rpx;
  position: absolute;
  top: -220rpx;
}
.welWedding {
  width: 660rpx;
  height: 336rpx;
  position: absolute;
  top: 30rpx;
  animation-name: pulse;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
.ballon1 {
  width: 68rpx;
  height: 164rpx;
  position: absolute;
  bottom: -10rpx;
  right: -34rpx;
  animation-name: swing;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  transform-origin: bottom center;
}
.ballon2 {
  width: 136rpx;
  height: 132rpx;
  position: absolute;
  right: 37rpx;
  top: 350rpx;
  animation-name: ballonAni;
  animation-duration: 10s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
.ballon3 {
  width: 148rpx;
  height: 160rpx;
  position: absolute;
  left: 37rpx;
  top: 350rpx;
  animation-name: ballonAni;
  animation-duration: 10s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
/* differance */
.refreshBtn0 {
  background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/refreshIconPink.png');
  right: 42rpx;
}
.refreshBtn1,
.refreshBtn2,
.refreshBtn21,
.refreshBtn22,
.refreshBtn23,
.refreshBtn24,
.refreshBtn25,
.refreshBtn41,
.refreshBtn42,
.refreshBtn43,
.refreshBtn51 {
  background-image: url('https://ustatic.joymew.com/joymewMp/joymewIndex/txhReloadIcon.png');
}
.refreshBtn52 {
  background-image: url('https://ustatic.joymew.com/joymewMp/joymewIndex/qqyReloadIcon.png');
}
.refreshBtn53 {
  background-image: url('https://ustatic.joymew.com/joymewMp/joymewIndex/bbyReloadIcon.png');
}
.phoneIconBox {
  width: 24rpx;
  height: 32rpx;
  position: absolute;
  right: 57rpx;
  bottom: 17rpx;
  background-size: 100% 100%;
}
/* differance */
.phoneIconBox0 {
  background-image: url('https://ustatic.joymew.com/joymewMpTql/signWedding/phoneIcon.png');
}
.phoneIconBox1,
.phoneIconBox2,
.phoneIconBox21,
.phoneIconBox22,
.phoneIconBox23,
.phoneIconBox24,
.phoneIconBox25,
.phoneIconBox41,
.phoneIconBox42,
.phoneIconBox43,
.phoneIconBox51,
.phoneIconBox52,
.phoneIconBox53 {
  background-image: url('https://ustatic.joymew.com/joymewMpTql/signTXH/phoneIcon.png');
}
.chooseGroup {
  width: 540rpx;
  height: 56rpx;
  box-sizing: border-box;
  display: flex;
  justify-content: space-around;
}
.chooseGroup > .chooseItem {
  width: 170rpx;
  height: 56rpx;
  background: rgba(122, 97, 230, 0.4);
  border-radius: 28rpx;
  font-size: 28rpx;
  font-weight: 400;
  text-align: center;
  line-height: 56rpx;
  color: #ffffff;
}
.chooseGroup > .chooseItem.active {
  background: #7a61e6;
}
.sexGroup {
  width: 412rpx;
  height: 59rpx;
  display: flex;
  justify-content: space-around;
}
.sexGroup > .sexItem {
  display: flex;
  align-items: center;
  position: relative;
  font-size: 32rpx;
  font-weight: 400;
  text-align: center;
}
/* differance */
.sexItem0,
.sexItem2,
.sexItem21,
.sexItem23,
.sexItem24,
.sexItem25,
.sexItem41,
.sexItem42,
.sexItem43,
.sexItem52 {
  color: #333333;
}
.sexItem1,
.sexItem22,
.sexItem51,
.sexItem53 {
  color: #ffffff;
}
.sexGroup .sexItem > .sexIcon {
  width: 59rpx;
  height: 59rpx;
  display: flex;
  align-items: center;
  margin-right: 17rpx;
}
.sexGroup .sexItem > .tickedIcon {
  position: absolute;
  width: 20rpx;
  height: 20rpx;
  top: 38rpx;
  left: 40rpx;
}
.getPhoneIpt {
  position: relative;
  z-index: 1;
  width: 412rpx;
  height: 56rpx;
  box-sizing: border-box;
  font-size: 32rpx;
  font-weight: normal;
  border-bottom: 2rpx solid #666666;
  padding-right: 68rpx;
}
/* differance */
.getPhoneIpt0 {
  width: 540rpx;
  border-bottom: 2rpx solid #e8757e;
  font-size: 40rpx;
}
.getPhoneIpt2,
.getPhoneIpt21 {
  color: #333333;
}
.getPhoneIpt1 {
  color: #ffffff;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.6);
}
.getPhoneIpt22 {
  color: #ffffff;
  border-bottom: 1rpx solid #cc8c8c;
}
.getPhoneIpt23 {
  color: #333333;
  border-bottom: 1rpx solid #54d5e9;
}
.getPhoneIpt24,
.getPhoneIpt25 {
  color: #333333;
  border-bottom: 1rpx solid rgba(51, 51, 51, 0.6);
}
.getPhoneIpt41 {
  color: #333333;
  border-bottom: 1rpx solid #efd1ee;
}
.getPhoneIpt42 {
  color: #333333;
  border-bottom: 1rpx solid #e20013;
}
.getPhoneIpt43 {
  color: #333333;
  border-bottom: 1rpx solid #ea002a;
}
.getPhoneIpt51,
.getPhoneIpt53 {
  color: #ffffff;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.6);
}
.getPhoneIpt52 {
  color: #333333;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.6);
}
.getPhoneIpt > .getPhoneBtn {
  width: 100%;
  height: 100%;
  opacity: 0;
  background-color: transparent;
  position: absolute;
  right: 0;
  top: 0;
}
.birthDate {
  width: 412rpx;
  height: 56rpx;
  background: #ffffff;
  border-radius: 4rpx;
  position: absolute;
  right: 55rpx;
  top: -8rpx;
}
.birthDate > .downArrow {
  width: 27rpx;
  height: 14rpx;
  position: absolute;
  right: 15rpx;
  bottom: 21rpx;
  transition: all 0.1s linear;
}
.birthDate > .val {
  width: 80%;
  height: 100%;
  position: absolute;
  font-size: 32rpx;
  font-weight: 400;
  color: #666666;
  line-height: 56rpx;
  padding-left: 18rpx;
}
.signBtn {
  width: 380rpx;
  height: 72rpx;
  border-radius: 36rpx;
  font-size: 32rpx;
  font-weight: 500;
  margin-top: 8rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}
/* differance */
.signBtn0 {
  background: linear-gradient(180deg, #e87080 0%, #ee8b6b 100%);
  color: #ffffff;
}
.signBtn1 {
  background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/signBtnQy01.png');
  background-size: 100% 100%;
}
.signBtn2,
.signBtn21,
.signBtn24,
.signBtn25 {
  background: #fab0ce;
  color: #ffffff;
}
.signBtn22 {
  background: #fddd97;
  color: #ffffff;
}
.signBtn23,
.signBtn41 {
  background: #54d5e9;
  color: #ffffff;
}
.signBtn42 {
  background: #e20013;
  color: #ffffff;
}
.signBtn43 {
  background: #ea002a;
  color: #ffffff;
}
.signBtn51 {
  background: #beb161;
  color: #ffffff;
}
.signBtn52 {
  background: #ef2152;
  color: #ffffff;
}
.signBtn53 {
  background: #b3e0ee;
  color: #ffffff;
}

@keyframes pulse {
  from {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }

  50% {
    -webkit-transform: scale3d(1.05, 1.05, 1.05);
    transform: scale3d(1.05, 1.05, 1.05);
  }

  to {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}
@keyframes swing {
  20% {
    -webkit-transform: rotate3d(0, 0, 1, 15deg);
    transform: rotate3d(0, 0, 1, 15deg);
  }

  40% {
    -webkit-transform: rotate3d(0, 0, 1, -10deg);
    transform: rotate3d(0, 0, 1, -10deg);
  }

  60% {
    -webkit-transform: rotate3d(0, 0, 1, 5deg);
    transform: rotate3d(0, 0, 1, 5deg);
  }

  80% {
    -webkit-transform: rotate3d(0, 0, 1, -5deg);
    transform: rotate3d(0, 0, 1, -5deg);
  }

  to {
    -webkit-transform: rotate3d(0, 0, 1, 0deg);
    transform: rotate3d(0, 0, 1, 0deg);
  }
}

@keyframes ballonAni {
  from {
    transform: translateZ(1000rpx);
    opacity: 1;
  }
  to {
    transform: translateZ(-5000rpx);
    opacity: 0;
  }
}
```

## File: components/signCustom/signCustom.js
```javascript
import { showWxToast } from '../../utils/index';
import { authGetPhoneByCode, authGetPhoneMiaoShop } from '../../api/login';

const tmpDeskList = [];
for (let i = 0; i < 90; i += 1) {
  if (i < 3) {
    tmpDeskList.push(i + 1);
  } else if (i < 12) {
    tmpDeskList.push(i + 2);
  } else if (i < 21) {
    tmpDeskList.push(i + 3);
  } else if (i < 30) {
    tmpDeskList.push(i + 4);
  } else if (i < 39) {
    tmpDeskList.push(i + 5);
  } else if (i < 48) {
    tmpDeskList.push(i + 6);
  } else if (i < 57) {
    tmpDeskList.push(i + 7);
  } else if (i < 66) {
    tmpDeskList.push(i + 8);
  } else if (i < 75) {
    tmpDeskList.push(i + 9);
  } else if (i < 84) {
    tmpDeskList.push(i + 10);
  } else {
    tmpDeskList.push(i + 11);
  }
}

Component({
  /**
   * 组件的属性列表
   */
  properties: {
    activityTitle: {
      value: '',
      type: String,
    },
    userNameProp: {
      value: '',
      type: String,
    },
    wishProp: {
      value: '',
      type: String,
    },
    isExamine: {
      value: false,
      type: Boolean,
    },
    sceneType: {
      value: '',
      type: String,
    },
    customBg: {
      value: '',
      type: String,
    }
  },
  observers: {
    userNameProp: function (userNameProp) {
      this.setData({
        userName: userNameProp,
      });
    },
    wishProp: function (wishProp) {
      this.setData({
        wish: wishProp,
      });
    }
  },
  attached() {
    console.log('attached');
  },
  data: {
    userName: '', // 姓名
    wish: '', // 祝福语
    phone: '', // 手机号
    deskNum: '', // 桌号
    deskList: tmpDeskList,
    role: '', // 亲友类型 1:男方亲友 2:女方亲友  '': 不选
  },
  /**
   * 组件的方法列表
   */
  methods: {
    userNameBlur(e) {
      console.log('***userNameBlur***');
      this.setData({
        userName: e.detail.value,
      });
    },
    wishesBlur(e) {
      console.log('***wishesBlur***');
      if (e.detail.value) {
        this.setData({
          wish: e.detail.value,
        });
      }
    },
    // 选择亲友
    chooseRelatives(e) {
      console.log('***chooseRelatives***');
      console.log(e);
      this.setData({
        role: e.currentTarget.dataset.role,
      });
    },
    handlePickerChange: function (e) {
      console.log(e.detail.value);
      let tmpDeskNum = this.data.deskNum;
      tmpDeskNum = this.data.deskList[e.detail.value];
      this.setData({
        deskNum: tmpDeskNum,
      });
    },
    sign() {
      // if (!this.data.userName) {
      //   showWxToast('贵宾姓名不能为空!');
      //   return;
      // }
      if (!this.data.isExamine) {
        if (!this.data.wish) {
          showWxToast('祝福语不能为空!');
          return;
        }
        // if (!this.data.phone) {
        //   showWxToast('手机号不能为空!');
        //   return;
        // }
        // if (this.data.phone.length !== 11) {
        //   showWxToast('手机号格式错误!');
        //   return;
        // }
      }
      console.log(this.data.userName);
      console.log(this.data.wish);
      console.log(this.data.phone);
      this.triggerEvent('signEvent', {
        userName: this.data.userName,
        wish: this.data.wish,
        userPhone: this.data.phone,
        role: this.data.role,
        deskNum: this.data.deskNum,
      });
    },
    refreshWish() {
      this.triggerEvent('refreshWishEvent');
    },
    getPhoneNumber: function (e) {
      console.log('******getPhoneNumber方法内部*******');
      console.log(e.detail.encryptedData);
      console.log(e.detail.iv);
      try {
        authGetPhoneMiaoShop({
          encryptedData: e.detail.encryptedData,
          iv: e.detail.iv
        })
          .then(res => {
            console.log(res);
            if (res && res.phone_info && res.phone_info.phoneNumber) {
              this.setData({
                phone: res.phone_info.phoneNumber,
              });
            } else {
              showWxToast('手机号获取失败!请删除小程序重新进入!');
            }
          })
          .catch(err => {
            console.log(err);
            showWxToast(JSON.stringify(err));
          });
      } catch (err) {
        console.log(err);
        showWxToast(JSON.stringify(err));
      }
    },
    handleStopMove(e) {
     return false;
    }
  },
});
```

## File: components/signCustom/signCustom.json
```json
{
    "component": true
}
```

## File: components/signCustom/signCustom.ttml
```
<!-- 云境定制 -->
<view class="signNew">
    <image src="{{customBg}}" class="customBg" mode="aspectFit"></image>
    <image src="https://ustatic.hudongmiao.com/joymewMpTql/signWedding/yjBgtite.png" class="yjBgtite" mode="widthFix"></image>
    <view class="signBox">
        <image src="https://ustatic.hudongmiao.com/joymewMpTql/signWedding/yjBgtit.png" class="yjBgtit" mode="widthFix"></image>
        <!-- <view class="fItem">
            <text class="key">姓名：</text>
            <input bindblur="userNameBlur" name="userName" placeholder='请输入您的姓名' maxlength="12" class="namIpt" value="{{userName}}"></input>
        </view> -->
        <!-- <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key">手机号：</text>
            <view class="getPhoneIpt {{phone ? 'hasPhone' : ''}}">
                {{phone ? phone: '获取手机号'}}
                <button open-type="getPhoneNumber" bindgetphonenumber="getPhoneNumber" class="getPhoneBtn" wx:if="{{!phone}}">
                    获取手机号
                </button>
                <image src="/assets/image/phone.png" class="phoneIcon"></image>
            </view>
        </view> -->
        <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key">祝福语：</text>
            <input bindblur="wishesBlur" name="wishes" placeholder='祝福语' maxlength="20" value="{{wish}}" class="iptPad"></input>
            <image class="refreshBtn" bindtap="refreshWish" src="/assets/image/refresh.png"></image>
        </view>
        <view class="fItem" wx:if="{{sceneType === '0'}}">
            <text class="key">亲友团：</text>
            <view class="chooseGroup">
                <view class="chooseItem {{ role === '1'?'active':'' }}" catchtap="chooseRelatives" data-role="1">
                    <text>男方</text>
                </view>
                <view class="chooseItem {{ role === '2'?'active':'' }}" catchtap="chooseRelatives" data-role="2">
                    <text>女方</text>
                </view>
                <view class="chooseItem {{ role === ''?'active':'' }}" catchtap="chooseRelatives" data-role="">
                    <text>不选</text>
                </view>
            </view>
        </view>
        <view class="fItem" wx:if="{{sceneType === '0'}}">
            <text class="key">桌号：</text>
            <picker value="{{deskNum}}" range="{{deskList}}" bindchange="handlePickerChange" style="height: 40rpx">
                <view class="deskNum">
                    <view class="val">{{deskNum === '' ? '请选择' : deskNum}}</view>
                    <image src='https://static.joymew.com/joymewMp/joymewIndex/downArrow.png' class="downArrow"></image>
                </view>
            </picker>
        </view>
        <!-- <button open-type="getPhoneNumber" bindgetphonenumber="getPhoneNumber" class="signBtn" wx:if="{{!phone}}" data-type="signBtn">
            点击进入
        </button>
        <view class="signBtn" catchtap="sign" wx:if="{{phone}}">点击进入</view> -->
        <view class="signBtn" catchtap="sign">点击进入</view>
    </view>
</view>
```

## File: components/signCustom/signCustom.ttss
```
.signNew {
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url('https://ustatic.hudongmiao.com/joymewMpTql/signWedding/yunjinBg2.png');
  background-color: #0f1019;
}
.customBg {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
.yjBgtite {
  width: 320rpx;
  height: 125rpx;
  position: absolute;
  top: 40rpx;
}
.yjBgtit {
  width: 380rpx;
  height: 134rpx;
}
.signBox {
  width: 680rpx;
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: absolute;
  top: 148rpx;
  padding: 40rpx 0;
  border-bottom: 2rpx solid #deac81;
  border-right: 2rpx solid #deac81;
  border-left: 2rpx solid #deac81;
}
.fItem {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  width: 586rpx;
  margin-bottom: 20rpx;
  position: relative;
}
.key {
  font-size: 36rpx;
  font-weight: 600;
  color: #deac81;
}
input {
  width: 382rpx;
  height: 54rpx;
  border-radius: 4rpx;
  box-sizing: border-box;
  font-size: 32rpx;
  font-weight: normal;
  outline: none;
  color: #333333;
}
.iptPad {
  padding-right: 60rpx;
  padding-left: 20rpx;
  width: 586rpx;
  height: 62rpx;
  margin-top: 10rpx;
  font-size: 36rpx;
  background-color: #ffffff;
}
.namIpt {
  width: 586rpx;
  height: 62rpx;
  font-size: 36rpx;
  margin-top: 10rpx;
  padding-right: 20rpx;
  padding-left: 20rpx;
  background-color: #ffffff;
}
.refreshBtn {
  width: 30rpx;
  height: 30rpx;
  position: absolute;
  right: 12rpx;
  bottom: 12rpx;
}
.phoneIconBox {
  width: 24rpx;
  height: 30rpx;
  position: absolute;
  right: 57rpx;
  bottom: 17rpx;
  background-size: 100% 100%;
}
.chooseGroup {
  width: 586rpx;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  margin-top: 10rpx;
}
.chooseGroup > .chooseItem {
  width: 105rpx;
  height: 54rpx;
  background: #ffffff;
  border-radius: 10rpx;
  font-size: 32rpx;
  font-weight: 400;
  text-align: center;
  line-height: 52rpx;
  color: #000000;
}
.chooseGroup > .chooseItem.active {
  background: #deac81;
}
.sexGroup {
  width: 412rpx;
  height: 54rpx;
  display: flex;
  justify-content: space-around;
}
.sexGroup > .sexItem {
  display: flex;
  align-items: center;
  position: relative;
  font-size: 32rpx;
  font-weight: 400;
  text-align: center;
  color: #333333;
}
.sexGroup .sexItem > .sexIcon {
  width: 59rpx;
  height: 59rpx;
  display: flex;
  align-items: center;
  margin-right: 17rpx;
}
.sexGroup .sexItem > .tickedIcon {
  position: absolute;
  width: 20rpx;
  height: 20rpx;
  top: 38rpx;
  left: 40rpx;
}
.getPhoneIpt {
  position: relative;
  z-index: 1;
  width: 586rpx;
  height: 62rpx;
  font-size: 36rpx;
  font-weight: normal;
  background-color: #ffffff;
  padding-right: 68rpx;
  padding-left: 20rpx;
  color: #333333;
  margin-top: 10rpx;
  display: flex;
  align-items: center;
}
.getPhoneIpt.hasPhone {
  color: #333333;
}
.getPhoneIpt > .getPhoneBtn {
  width: 100%;
  height: 100%;
  opacity: 0;
  background-color: transparent;
  position: absolute;
  right: 0;
  top: 0;
}
.getPhoneIpt > .phoneIcon {
  width: 48rpx;
  height: 48rpx;
  position: absolute;
  right: 0;
}

.deskNum {
  width: 586rpx;
  height: 62rpx;
  background: #ffffff;
  border-radius: 4rpx;
  position: relative;
  margin-top: 10rpx;
}
.deskNum > .downArrow {
  width: 22rpx;
  height: 12rpx;
  position: absolute;
  right: 12rpx;
  bottom: 21rpx;
  transition: all 0.1s linear;
}
.deskNum > .val {
  width: 80%;
  height: 100%;
  position: absolute;
  font-size: 32rpx;
  font-weight: 400;
  color: #333333;
  line-height: 54rpx;
  padding-left: 10rpx;
}
.signBtn {
  width: 586rpx;
  height: 78rpx;
  border-radius: 12rpx;
  font-size: 32rpx;
  font-weight: 500;
  margin-top: 35rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #deac81;
  color: #333333;
}
@media screen and (min-height: 720px) {
  .yjBgtite {
    top: 80rpx;
  }
  .signBox {
    top: 320rpx;
  }
}
```

## File: components/signLz/signLz.js
```javascript
import { showWxToast } from '../../utils/index';
import { authGetPhoneByCode } from '../../api/login';

const tmpDeskList = [];
for (let i = 0; i < 90; i += 1) {
  if (i < 3) {
    tmpDeskList.push(i + 1);
  } else if (i < 12) {
    tmpDeskList.push(i + 2);
  } else if (i < 21) {
    tmpDeskList.push(i + 3);
  } else if (i < 30) {
    tmpDeskList.push(i + 4);
  } else if (i < 39) {
    tmpDeskList.push(i + 5);
  } else if (i < 48) {
    tmpDeskList.push(i + 6);
  } else if (i < 57) {
    tmpDeskList.push(i + 7);
  } else if (i < 66) {
    tmpDeskList.push(i + 8);
  } else if (i < 75) {
    tmpDeskList.push(i + 9);
  } else if (i < 84) {
    tmpDeskList.push(i + 10);
  } else {
    tmpDeskList.push(i + 11);
  }
}

Component({
  /**
   * 组件的属性列表
   */
  properties: {
    activityTitle: {
      value: '',
      type: String,
    },
    userNameProp: {
      value: '',
      type: String,
    },
    wishProp: {
      value: '',
      type: String,
    },
    isExamine: {
      value: false,
      type: Boolean,
    },
    sceneType: {
      value: '',
      type: String,
    }
  },
  observers: {
    userNameProp: function (userNameProp) {
      this.setData({
        userName: userNameProp,
      });
    },
    wishProp: function (wishProp) {
      this.setData({
        wish: wishProp,
      });
    }
  },
  attached() {
    console.log('attached');
  },
  data: {
    userName: '', // 姓名
    wish: '', // 祝福语
    phone: '', // 手机号
    deskNum: '', // 桌号
    deskList: tmpDeskList,
    role: '', // 亲友类型 1:男方亲友 2:女方亲友  '': 不选
  },
  /**
   * 组件的方法列表
   */
  methods: {
    userNameBlur(e) {
      console.log('***userNameBlur***');
      this.setData({
        userName: e.detail.value,
      });
    },
    wishesBlur(e) {
      console.log('***wishesBlur***');
      if (e.detail.value) {
        this.setData({
          wish: e.detail.value,
        });
      }
    },
    phoneBlur(e) {
      console.log('***phoneBlur***');
      if (e.detail.value) {
        this.setData({
          phone: e.detail.value,
        });
      }
    },
    // 选择亲友
    chooseRelatives(e) {
      console.log('***chooseRelatives***');
      console.log(e);
      this.setData({
        role: e.currentTarget.dataset.role,
      });
    },
    handlePickerChange: function (e) {
      console.log(e.detail.value);
      let tmpDeskNum = this.data.deskNum;
      tmpDeskNum = this.data.deskList[e.detail.value];
      this.setData({
        deskNum: tmpDeskNum,
      });
    },
    sign() {
      // if (!this.data.userName) {
      //   showWxToast('贵宾姓名不能为空!');
      //   return;
      // }
      if (!this.data.isExamine) {
        if (!this.data.wish) {
          showWxToast('祝福语不能为空!');
          return;
        }
        if (!this.data.phone) {
          showWxToast('手机号不能为空!');
          return;
        }
        if (this.data.phone.length !== 11) {
          showWxToast('手机号格式错误!');
          return;
        }
      }
      console.log(this.data.userName);
      console.log(this.data.wish);
      console.log(this.data.phone);
      this.triggerEvent('signEvent', {
        userName: this.data.userName,
        wish: this.data.wish,
        userPhone: this.data.phone,
        role: this.data.role,
        deskNum: this.data.deskNum,
      });
    },
    refreshWish() {
      this.triggerEvent('refreshWishEvent');
    },
    getPhoneNumber: function (e) {
      console.log('******getPhoneNumber方法内部*******');
      console.log(e.detail.code);
      try {
        authGetPhoneByCode({
          code: e.detail.code
        })
          .then(res => {
            console.log(res);
            if (res && res.phone_info && res.phone_info.phoneNumber) {
              this.setData({
                phone: res.phone_info.phoneNumber,
              });
            } else {
              showWxToast('手机号获取失败!请删除小程序重新进入!');
            }
          })
          .catch(err => {
            console.log(err);
            showWxToast(JSON.stringify(err));
          });
      } catch (err) {
        console.log(err);
        showWxToast(JSON.stringify(err));
      }
    }
  },
});
```

## File: components/signLz/signLz.json
```json
{
    "component": true
}
```

## File: components/signLz/signLz.ttml
```
<!-- 狼尊定制 -->
<view class="signNew">
    <image src="https://ustatic.hudongmiao.com/joymewMpTql/hk_slogan.png" class="hk_slogan" mode="widthFix"></image>
    <image src="https://ustatic.hudongmiao.com/joymewMpTql/hk_title.png" class="hk_title" mode="widthFix"></image>
    <image src="https://ustatic.hudongmiao.com/joymewMpTql/hk_benifit.png" class="hk_benifit" mode="widthFix"></image>
    <view class="newdate-slogan">— 开启婚庆获客2.0时代 —</view>
    <view class="signBox">
        <view class="welcom-eng">Welcome to join us</view>
        <view class="welcom-cn">欢迎加入我们</view>

        <!-- <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key">手机号：</text>
            <view class="getPhoneIpt {{phone ? 'hasPhone' : ''}}">
                {{phone ? phone: '获取手机号'}}
                <button open-type="getPhoneNumber" bindgetphonenumber="getPhoneNumber" class="getPhoneBtn"
                    wx:if="{{!phone}}">
                    获取手机号
                </button>
                <image src="https://ustatic.hudongmiao.com/joymewMpTql/phone_icon.png" class="phoneIcon"></image>
            </view>
        </view> -->
        <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key">手机号：</text>
            <input bindblur="phoneBlur" name="phone" placeholder='请输入手机号' maxlength="20" value="{{phone}}"
                class="iptPad"></input>
            <image src="https://ustatic.hudongmiao.com/joymewMpTql/phone_icon.png" class="refreshBtn"></image>
        </view>
        <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key">签到语：</text>
            <input bindblur="wishesBlur" name="wishes" placeholder='祝福语' maxlength="20" value="{{wish}}"
                class="iptPad"></input>
            <image src="https://ustatic.hudongmiao.com/joymewMpTql/refresh_icon.png" class="refreshBtn"
                bindtap="refreshWish"></image>
        </view>
        <!-- <button open-type="getPhoneNumber" bindgetphonenumber="getPhoneNumber" class="signBtn" wx:if="{{!phone}}"
            data-type="signBtn">
            点击进入
        </button> -->
        <view class="signBtn" catchtap="sign">点击进入</view>
    </view>
    <view class="bottom-slogan-wrap">
        <view class="slogan-strong">嗨喵 让获客更简单</view>
        <view class="slogan-common">欢聚时刻 嗨喵相伴</view>
    </view>
</view>
```

## File: components/signLz/signLz.ttss
```
.signNew {
  width: 100vw;
  height: 100vh;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url('https://ustatic.hudongmiao.com/joymewMpTql/lz-bg.png');
  background-color: #0f1019;
}

.hk_slogan {
  width: 216rpx;
  height: 60rpx;
}

.hk_title {
  width: 552rpx;
  height: 132rpx;
  margin-top: 8rpx;
}

.hk_benifit {
  width: 520rpx;
  height: 48rpx;
  margin-top: 16rpx;
}

.newdate-slogan {
  font-size: 32rpx;
  font-weight: 500;
  color: #ffffff;
  margin-top: 34rpx;
}

.signBox {
  width: 654rpx;
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 32rpx;
  padding-bottom: 56rpx;
  background-color: rgba(255, 255, 255, 0.30);
  border: 2rpx solid;
  border-image: linear-gradient(145deg, #ffffff 0%, rgba(255, 255, 255, 0.00) 100%, #ffffff 100%) 1 1;
  border-radius: 8rpx;
  margin-top: 64rpx;
}

.welcom-eng {
  font-size: 24rpx;
  font-weight: 400;
  color: #ffffff;
}

.welcom-cn {
  font-size: 36rpx;
  font-family: PingFang SC, PingFang SC-Medium;
  font-weight: 500;
  text-align: LEFT;
  color: #ffffff;
  line-height: 48rpx;
}

.fItem {
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  width: 586rpx;
  margin-bottom: 48rpx;
  position: relative;
}

.key {
  font-size: 32rpx;
  font-weight: 600;
  color: #FFFFFF;
}

input {
  width: 382rpx;
  height: 54rpx;
  border-radius: 4rpx;
  box-sizing: border-box;
  font-size: 32rpx;
  font-weight: normal;
  outline: none;
  color: #333333;
}

.iptPad {
  padding-right: 60rpx;
  padding-left: 20rpx;
  width: 586rpx;
  height: 62rpx;
  margin-top: 10rpx;
  font-size: 36rpx;
  background-color: #ffffff;
}

.namIpt {
  width: 586rpx;
  height: 62rpx;
  font-size: 36rpx;
  margin-top: 10rpx;
  padding-right: 20rpx;
  padding-left: 20rpx;
  background-color: #ffffff;
}

.refreshBtn {
  width: 40rpx;
  height: 40rpx;
  position: absolute;
  right: 12rpx;
  bottom: 12rpx;
}

.phoneIconBox {
  width: 24rpx;
  height: 30rpx;
  position: absolute;
  right: 57rpx;
  bottom: 17rpx;
  background-size: 100% 100%;
}

.chooseGroup {
  width: 586rpx;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  margin-top: 10rpx;
}

.chooseGroup>.chooseItem {
  width: 158rpx;
  height: 72rpx;
  background: #ffffff;
  border-radius: 58rpx;
  font-size: 28rpx;
  font-weight: 400;
  text-align: center;
  line-height: 72rpx;
  color: #ECC697;
}

.chooseGroup>.chooseItem.active {
  background: #deac81;
  color: #ffffff;
}

.sexGroup {
  width: 412rpx;
  height: 54rpx;
  display: flex;
  justify-content: space-around;
}

.sexGroup>.sexItem {
  display: flex;
  align-items: center;
  position: relative;
  font-size: 32rpx;
  font-weight: 400;
  text-align: center;
  color: #333333;
}

.sexGroup .sexItem>.sexIcon {
  width: 59rpx;
  height: 59rpx;
  display: flex;
  align-items: center;
  margin-right: 17rpx;
}

.sexGroup .sexItem>.tickedIcon {
  position: absolute;
  width: 20rpx;
  height: 20rpx;
  top: 38rpx;
  left: 40rpx;
}

.getPhoneIpt {
  position: relative;
  z-index: 1;
  width: 586rpx;
  height: 62rpx;
  font-size: 36rpx;
  font-weight: normal;
  background-color: #ffffff;
  padding-right: 68rpx;
  padding-left: 20rpx;
  color: #333333;
  margin-top: 10rpx;
  display: flex;
  align-items: center;
}

.getPhoneIpt.hasPhone {
  color: #333333;
}

.getPhoneIpt>.getPhoneBtn {
  width: 100%;
  height: 100%;
  opacity: 0;
  background-color: transparent;
  position: absolute;
  right: 0;
  top: 0;
}

.getPhoneIpt>.phoneIcon {
  width: 44rpx;
  height: 44rpx;
  position: absolute;
  right: 0;
}

.deskNum {
  width: 586rpx;
  height: 62rpx;
  background: #ffffff;
  border-radius: 4rpx;
  position: relative;
  margin-top: 10rpx;
}

.deskNum>.downArrow {
  width: 22rpx;
  height: 12rpx;
  position: absolute;
  right: 12rpx;
  bottom: 21rpx;
  transition: all 0.1s linear;
}

.deskNum>.val {
  width: 80%;
  height: 100%;
  position: absolute;
  font-size: 32rpx;
  font-weight: 400;
  color: #333333;
  line-height: 54rpx;
  padding-left: 10rpx;
}

.signBtn {
  width: 578rpx;
  height: 72rpx;
  border-radius: 58rpx;
  font-size: 28rpx;
  font-weight: 500;
  margin-top: 48rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #ECC697;
  color: #FFFFFF;
}

.bottom-slogan-wrap {
  position: absolute;
  bottom: 54rpx;
}

.slogan-strong {
  font-size: 28rpx;
  font-weight: 500;
  color: #ffffff;
  text-align: center;
}

.slogan-common {
  font-size: 24rpx;
  font-weight: 400;
  color: #ffffff;
  margin-top: 14rpx;
  text-align: center;
}

@media screen and (max-height: 720px) {
  .newdate-slogan {
    margin-top: 20rpx;
  }
  .signBox {
    margin-top: 20rpx;
  }

  .bottom-slogan-wrap {
    bottom: 20rpx;
  }
}
```

## File: libs/svgaplayer.weapp.js
```javascript
!function (t) {if ("object" == typeof exports && "undefined" != typeof module) module.exports = t();else if ("function" == typeof define && define.amd) define([], t);else {("undefined" != typeof window ? window : "undefined" != typeof global ? global : "undefined" != typeof self ? self : this).SVGA = t();}}(function () {return function t(e, r, i) {function n(s, a) {if (!r[s]) {if (!e[s]) {var u = "function" == typeof require && require;if (!a && u) return u(s, !0);if (o) return o(s, !0);var h = new Error("Cannot find module '" + s + "'");throw h.code = "MODULE_NOT_FOUND", h;}var l = r[s] = { exports: {} };e[s][0].call(l.exports, function (t) {return n(e[s][1][t] || t);}, l, l.exports, t, e, r, i);}return r[s].exports;}for (var o = "function" == typeof require && require, s = 0; s < i.length; s++) n(i[s]);return n;}({ 1: [function (t, e, r) {"use strict";e.exports = function () {var e = {};function r() {e.converter._configure(), e.decoder._configure(), e.Field._configure(), e.MapField._configure(), e.Message._configure(), e.Namespace._configure(), e.Method._configure(), e.ReflectionObject._configure(), e.OneOf._configure(), e.parse._configure(), e.Reader._configure(), e.Root._configure(), e.Service._configure(), e.verifier._configure(), e.Type._configure(), e.types._configure(), e.wrappers._configure(), e.Writer._configure();}if (e.build = "minimal", e.Writer = t(34), e.Reader = t(22), e.util = t(31), e.rpc = t(25), e.roots = t(24), e.verifier = t(32), e.tokenize = t(27), e.parse = t(19), e.common = t(5), e.ReflectionObject = t(17), e.Namespace = t(16), e.Root = t(23), e.Enum = t(8), e.Type = t(28), e.Field = t(9), e.OneOf = t(18), e.MapField = t(13), e.Service = t(26), e.Method = t(15), e.converter = t(6), e.decoder = t(7), e.Message = t(14), e.wrappers = t(33), e.types = t(29), e.util = t(31), e.configure = r, e.load = function (t, r, i) {return "function" == typeof r ? (i = r, r = new e.Root()) : r || (r = new e.Root()), r.load(t, i);}, e.loadSync = function (t, r) {return r || (r = new e.Root()), r.loadSync(t);}, e.parseFromPbString = function (t, r, i) {return "function" == typeof r ? (i = r, r = new e.Root()) : r || (r = new e.Root()), r.parseFromPbString(t, i);}, r(), arguments && arguments.length) for (var i = 0; i < arguments.length; i++) {var n = arguments[i];if (n.hasOwnProperty("exports")) return void (n.exports = e);}return e;}();}, { 13: 13, 14: 14, 15: 15, 16: 16, 17: 17, 18: 18, 19: 19, 22: 22, 23: 23, 24: 24, 25: 25, 26: 26, 27: 27, 28: 28, 29: 29, 31: 31, 32: 32, 33: 33, 34: 34, 5: 5, 6: 6, 7: 7, 8: 8, 9: 9 }], 24: [function (t, e, r) {"use strict";e.exports = {};}, {}], 27: [function (t, e, r) {"use strict";e.exports = d;var i = /[\s{}=;:[\],'"()<>]/g,n = /(?:"([^"\\]*(?:\\.[^"\\]*)*)")/g,o = /(?:'([^'\\]*(?:\\.[^'\\]*)*)')/g,s = /^ *[*/]+ */,a = /^\s*\*?\/*/,u = /\n/g,h = /\s/,l = /\\(.?)/g,f = { 0: "\0", r: "\r", n: "\n", t: "\t" };function c(t) {return t.replace(l, function (t, e) {switch (e) {case "\\":case "":return e;default:return f[e] || "";}});}function d(t, e) {t = t.toString();var r = 0,l = t.length,f = 1,d = null,p = null,y = 0,m = !1,v = [],g = null;function b(t) {return Error("illegal " + t + " (line " + f + ")");}function w(e) {return t.charAt(e);}function _(r, i) {d = t.charAt(r++), y = f, m = !1;var n,o = r - (e ? 2 : 3);do {if (--o < 0 || "\n" === (n = t.charAt(o))) {m = !0;break;}} while (" " === n || "\t" === n);for (var h = t.substring(r, i).split(u), l = 0; l < h.length; ++l) h[l] = h[l].replace(e ? a : s, "").trim();p = h.join("\n").trim();}function x(e) {var r = k(e),i = t.substring(e, r);return /^\s*\/{1,2}/.test(i);}function k(t) {for (var e = t; e < l && "\n" !== w(e);) e++;return e;}function A() {if (v.length > 0) return v.shift();if (g) return function () {var e = "'" === g ? o : n;e.lastIndex = r - 1;var i = e.exec(t);if (!i) throw b("string");return r = e.lastIndex, O(g), g = null, c(i[1]);}();var s, a, u, d, p;do {if (r === l) return null;for (s = !1; h.test(u = w(r));) if ("\n" === u && ++f, ++r === l) return null;if ("/" === w(r)) {if (++r === l) throw b("comment");if ("/" === w(r)) {if (e) {if (d = r, p = !1, x(r)) {p = !0;do {if ((r = k(r)) === l) break;r++;} while (x(r));} else r = Math.min(l, k(r) + 1);p && _(d, r), f++, s = !0;} else {for (p = "/" === w(d = r + 1); "\n" !== w(++r);) if (r === l) return null;++r, p && _(d, r - 1), ++f, s = !0;}} else {if ("*" !== (u = w(r))) return "/";d = r + 1, p = e || "*" === w(d);do {if ("\n" === u && ++f, ++r === l) throw b("comment");a = u, u = w(r);} while ("*" !== a || "/" !== u);++r, p && _(d, r - 2), s = !0;}}} while (s);var y = r;if (i.lastIndex = 0, !i.test(w(y++))) for (; y < l && !i.test(w(y));) ++y;var m = t.substring(r, r = y);return '"' !== m && "'" !== m || (g = m), m;}function O(t) {v.push(t);}function S() {if (!v.length) {var t = A();if (null === t) return null;O(t);}return v[0];}return Object.defineProperty({ next: A, peek: S, push: O, skip: function (t, e) {var r = S();if (r === t) return A(), !0;if (!e) throw b("token '" + r + "', '" + t + "' expected");return !1;}, cmnt: function (t) {var r = null;return void 0 === t ? y === f - 1 && (e || "*" === d || m) && (r = p) : (y < t && S(), y !== t || m || !e && "/" !== d || (r = p)), r;} }, "line", { get: function () {return f;} });}d.unescape = c;}, {}], 5: [function (t, e, r) {"use strict";e.exports = o;var i,n = /\/|\./;function o(t, e) {n.test(t) || (t = "google/protobuf/" + t + ".proto", e = { nested: { google: { nested: { protobuf: { nested: e } } } } }), o[t] = e;}o("any", { Any: { fields: { type_url: { type: "string", id: 1 }, value: { type: "bytes", id: 2 } } } }), o("duration", { Duration: i = { fields: { seconds: { type: "int64", id: 1 }, nanos: { type: "int32", id: 2 } } } }), o("timestamp", { Timestamp: i }), o("empty", { Empty: { fields: {} } }), o("struct", { Struct: { fields: { fields: { keyType: "string", type: "Value", id: 1 } } }, Value: { oneofs: { kind: { oneof: ["nullValue", "numberValue", "stringValue", "boolValue", "structValue", "listValue"] } }, fields: { nullValue: { type: "NullValue", id: 1 }, numberValue: { type: "double", id: 2 }, stringValue: { type: "string", id: 3 }, boolValue: { type: "bool", id: 4 }, structValue: { type: "Struct", id: 5 }, listValue: { type: "ListValue", id: 6 } } }, NullValue: { values: { NULL_VALUE: 0 } }, ListValue: { fields: { values: { rule: "repeated", type: "Value", id: 1 } } } }), o("wrappers", { DoubleValue: { fields: { value: { type: "double", id: 1 } } }, FloatValue: { fields: { value: { type: "float", id: 1 } } }, Int64Value: { fields: { value: { type: "int64", id: 1 } } }, UInt64Value: { fields: { value: { type: "uint64", id: 1 } } }, Int32Value: { fields: { value: { type: "int32", id: 1 } } }, UInt32Value: { fields: { value: { type: "uint32", id: 1 } } }, BoolValue: { fields: { value: { type: "bool", id: 1 } } }, StringValue: { fields: { value: { type: "string", id: 1 } } }, BytesValue: { fields: { value: { type: "bytes", id: 1 } } } }), o("field_mask", { FieldMask: { fields: { paths: { rule: "repeated", type: "string", id: 1 } } } }), o.get = function (t) {return o[t] || null;};}, {}], 22: [function (t, e, r) {"use strict";e.exports = a;var i,n,o = t(31);function s(t, e) {return RangeError("index out of range: " + t.pos + " + " + (e || 1) + " > " + t.len);}function a(t) {this.buf = t, this.pos = 0, this.len = t.length;}var u,h = "undefined" != typeof Uint8Array ? function (t) {if (t instanceof Uint8Array || Array.isArray(t)) return new a(t);if ("undefined" != typeof ArrayBuffer && t instanceof ArrayBuffer) return new a(new Uint8Array(t));throw Error("illegal buffer");} : function (t) {if (Array.isArray(t)) return new a(t);throw Error("illegal buffer");};function l() {var t = new i(0, 0),e = 0;if (!(this.len - this.pos > 4)) {for (; e < 3; ++e) {if (this.pos >= this.len) throw s(this);if (t.lo = (t.lo | (127 & this.buf[this.pos]) << 7 * e) >>> 0, this.buf[this.pos++] < 128) return t;}return t.lo = (t.lo | (127 & this.buf[this.pos++]) << 7 * e) >>> 0, t;}for (; e < 4; ++e) if (t.lo = (t.lo | (127 & this.buf[this.pos]) << 7 * e) >>> 0, this.buf[this.pos++] < 128) return t;if (t.lo = (t.lo | (127 & this.buf[this.pos]) << 28) >>> 0, t.hi = (t.hi | (127 & this.buf[this.pos]) >> 4) >>> 0, this.buf[this.pos++] < 128) return t;if (e = 0, this.len - this.pos > 4) {for (; e < 5; ++e) if (t.hi = (t.hi | (127 & this.buf[this.pos]) << 7 * e + 3) >>> 0, this.buf[this.pos++] < 128) return t;} else for (; e < 5; ++e) {if (this.pos >= this.len) throw s(this);if (t.hi = (t.hi | (127 & this.buf[this.pos]) << 7 * e + 3) >>> 0, this.buf[this.pos++] < 128) return t;}throw Error("invalid varint encoding");}function f(t, e) {return (t[e - 4] | t[e - 3] << 8 | t[e - 2] << 16 | t[e - 1] << 24) >>> 0;}function c() {if (this.pos + 8 > this.len) throw s(this, 8);return new i(f(this.buf, this.pos += 4), f(this.buf, this.pos += 4));}a.create = o.Buffer ? function (t) {return (a.create = function (t) {return o.Buffer.isBuffer(t) ? new (void 0)(t) : h(t);})(t);} : h, a.prototype._slice = o.Array.prototype.subarray || o.Array.prototype.slice, a.prototype.uint32 = (u = 4294967295, function () {if (u = (127 & this.buf[this.pos]) >>> 0, this.buf[this.pos++] < 128) return u;if (u = (u | (127 & this.buf[this.pos]) << 7) >>> 0, this.buf[this.pos++] < 128) return u;if (u = (u | (127 & this.buf[this.pos]) << 14) >>> 0, this.buf[this.pos++] < 128) return u;if (u = (u | (127 & this.buf[this.pos]) << 21) >>> 0, this.buf[this.pos++] < 128) return u;if (u = (u | (15 & this.buf[this.pos]) << 28) >>> 0, this.buf[this.pos++] < 128) return u;if ((this.pos += 5) > this.len) throw this.pos = this.len, s(this, 10);return u;}), a.prototype.int32 = function () {return 0 | this.uint32();}, a.prototype.sint32 = function () {var t = this.uint32();return t >>> 1 ^ -(1 & t) | 0;}, a.prototype.bool = function () {return 0 !== this.uint32();}, a.prototype.fixed32 = function () {if (this.pos + 4 > this.len) throw s(this, 4);return f(this.buf, this.pos += 4);}, a.prototype.sfixed32 = function () {if (this.pos + 4 > this.len) throw s(this, 4);return 0 | f(this.buf, this.pos += 4);}, a.prototype.float = function () {if (this.pos + 4 > this.len) throw s(this, 4);var t = o.float.readFloatLE(this.buf, this.pos);return this.pos += 4, t;}, a.prototype.double = function () {if (this.pos + 8 > this.len) throw s(this, 4);var t = o.float.readDoubleLE(this.buf, this.pos);return this.pos += 8, t;}, a.prototype.bytes = function () {var t = this.uint32(),e = this.pos,r = this.pos + t;if (r > this.len) throw s(this, t);return this.pos += t, Array.isArray(this.buf) ? this.buf.slice(e, r) : e === r ? new this.buf.constructor(0) : this._slice.call(this.buf, e, r);}, a.prototype.string = function () {var t = this.bytes();return n.read(t, 0, t.length);}, a.prototype.skip = function (t) {if ("number" == typeof t) {if (this.pos + t > this.len) throw s(this, t);this.pos += t;} else do {if (this.pos >= this.len) throw s(this);} while (128 & this.buf[this.pos++]);return this;}, a.prototype.skipType = function (t) {switch (t) {case 0:this.skip();break;case 1:this.skip(8);break;case 2:this.skip(this.uint32());break;case 3:for (; 4 != (t = 7 & this.uint32());) this.skipType(t);break;case 5:this.skip(4);break;default:throw Error("invalid wire type " + t + " at offset " + this.pos);}return this;}, a._configure = function () {i = t(12), n = t(30);var e = o.Long ? "toLong" : "toNumber";o.merge(a.prototype, { int64: function () {return l.call(this)[e](!1);}, uint64: function () {return l.call(this)[e](!0);}, sint64: function () {return l.call(this).zzDecode()[e](!1);}, fixed64: function () {return c.call(this)[e](!0);}, sfixed64: function () {return c.call(this)[e](!1);} });};}, { 12: 12, 30: 30, 31: 31 }], 32: [function (t, e, r) {"use strict";var i, n;function o(t, e) {return t.name + ": " + e + (t.repeated && "array" !== e ? "[]" : t.map && "object" !== e ? "{k:" + t.keyType + "}" : "") + " expected";}function s(t, e, r, s) {var a = s.types;if (t.resolvedType) {if (t.resolvedType instanceof i) {if (Object.keys(t.resolvedType.values).indexOf(r) < 0) return o(t, "enum value");} else {var u = a[e].verify(r);if (u) return t.name + "." + u;}} else switch (t.type) {case "int32":case "uint32":case "sint32":case "fixed32":case "sfixed32":if (!n.isInteger(r)) return o(t, "integer");break;case "int64":case "uint64":case "sint64":case "fixed64":case "sfixed64":if (!(n.isInteger(r) || r && n.isInteger(r.low) && n.isInteger(r.high))) return o(t, "integer|Long");break;case "float":case "double":if ("number" != typeof r) return o(t, "number");break;case "bool":if ("boolean" != typeof r) return o(t, "boolean");break;case "string":if (!n.isString(r)) return o(t, "string");break;case "bytes":if (!(r && "number" == typeof r.length || n.isString(r))) return o(t, "buffer");}}function a(t, e) {switch (t.keyType) {case "int32":case "uint32":case "sint32":case "fixed32":case "sfixed32":if (!n.key32Re.test(e)) return o(t, "integer key");break;case "int64":case "uint64":case "sint64":case "fixed64":case "sfixed64":if (!n.key64Re.test(e)) return o(t, "integer|Long key");break;case "bool":if (!n.key2Re.test(e)) return o(t, "boolean key");}}function u(t) {return function (e) {return function (r) {var i;if ("object" != typeof r || null === r) return "object expected";var u,h = {};t.oneofsArray.length && (u = {});for (var l = 0; l < t.fieldsArray.length; ++l) {var f,c = t._fieldsArray[l].resolve(),d = r[c.name];if (!c.optional || null != d && r.hasOwnProperty(c.name)) if (c.map) {if (!n.isObject(d)) return o(c, "object");var p = Object.keys(d);for (f = 0; f < p.length; ++f) {if (i = a(c, p[f])) return i;if (i = s(c, l, d[p[f]], e)) return i;}} else if (c.repeated) {if (!Array.isArray(d)) return o(c, "array");for (f = 0; f < d.length; ++f) if (i = s(c, l, d[f], e)) return i;} else {if (c.partOf) {var y = c.partOf.name;if (1 === h[c.partOf.name] && 1 === u[y]) return c.partOf.name + ": multiple values";u[y] = 1;}if (i = s(c, l, d, e)) return i;}}};};}e.exports = u, u._configure = function () {i = t(8), n = t(31);};}, { 31: 31, 8: 8 }], 19: [function (t, e, r) {"use strict";var i, n, o, s, a, u, h, l, f, c, d;e.exports = A, A.filename = null, A.defaults = { keepCase: !1 };var p = /^[1-9][0-9]*$/,y = /^-?[1-9][0-9]*$/,m = /^0[x][0-9a-fA-F]+$/,v = /^-?0[x][0-9a-fA-F]+$/,g = /^0[0-7]+$/,b = /^-?0[0-7]+$/,w = /^(?![eE])[0-9]*(?:\.[0-9]*)?(?:[eE][+-]?[0-9]+)?$/,_ = /^[a-zA-Z_][a-zA-Z_0-9]*$/,x = /^(?:\.?[a-zA-Z_][a-zA-Z_0-9]*)+$/,k = /^(?:\.[a-zA-Z][a-zA-Z_0-9]*)+$/;function A(t, e, r) {e instanceof n || (r = e, e = new n()), r || (r = A.defaults);var O,S,E,N,T,j = i(t, r.alternateCommentMode || !1),R = j.next,F = j.push,I = j.peek,B = j.skip,P = j.cmnt,C = !0,M = !1,D = e,L = r.keepCase ? function (t) {return t;} : d.camelCase;function z(t, e, r) {var i = A.filename;return r || (A.filename = null), Error("illegal " + (e || "token") + " '" + t + "' (" + (i ? i + ", " : "") + "line " + j.line + ")");}function V() {var t,e = [];do {if ('"' !== (t = R()) && "'" !== t) throw z(t);e.push(R()), B(t), t = I();} while ('"' === t || "'" === t);return e.join("");}function Z(t) {var e = R();switch (e) {case "'":case '"':return F(e), V();case "true":case "TRUE":return !0;case "false":case "FALSE":return !1;}try {return function (t, e) {var r = 1;switch ("-" === t.charAt(0) && (r = -1, t = t.substring(1)), t) {case "inf":case "INF":case "Inf":return r * (1 / 0);case "nan":case "NAN":case "Nan":case "NaN":return NaN;case "0":return 0;}if (p.test(t)) return r * parseInt(t, 10);if (m.test(t)) return r * parseInt(t, 16);if (g.test(t)) return r * parseInt(t, 8);if (w.test(t)) return r * parseFloat(t);throw z(t, "number", !0);}(e);} catch (r) {if (t && x.test(e)) return e;throw z(e, "value");}}function U(t, e) {var r, i;do {!e || '"' !== (r = I()) && "'" !== r ? t.push([i = q(R()), B("to", !0) ? q(R()) : i]) : t.push(V());} while (B(",", !0));B(";");}function q(t, e) {switch (t) {case "max":case "MAX":case "Max":return 536870911;case "0":return 0;}if (!e && "-" === t.charAt(0)) throw z(t, "id");if (y.test(t)) return parseInt(t, 10);if (v.test(t)) return parseInt(t, 16);if (b.test(t)) return parseInt(t, 8);throw z(t, "id");}function J() {if (void 0 !== O) throw z("package");if (O = R(), !x.test(O)) throw z(O, "name");D = D.define(O), B(";");}function $() {var t,e = I();switch (e) {case "weak":t = E || (E = []), R();break;case "public":R();default:t = S || (S = []);}e = V(), B(";"), t.push(e);}function K() {if (B("="), N = V(), !(M = "proto3" === N) && "proto2" !== N) throw z(N, "syntax");B(";");}function H(t, e) {switch (e) {case "option":return G(t, e), B(";"), !0;case "message":return function (t, e) {if (!_.test(e = R())) throw z(e, "type name");var r = new o(e);W(r, function (t) {if (!H(r, t)) switch (t) {case "map":!function (t) {B("<");var e = R();if (void 0 === c.mapKey[e]) throw z(e, "type");B(",");var r = R();if (!x.test(r)) throw z(r, "type");B(">");var i = R();if (!_.test(i)) throw z(i, "name");B("=");var n = new a(L(i), q(R()), e, r);W(n, function (t) {if ("option" !== t) throw z(t);G(n, t), B(";");}, function () {tt(n);}), t.add(n);}(r);break;case "required":case "optional":case "repeated":X(r, t);break;case "oneof":!function (t, e) {if (!_.test(e = R())) throw z(e, "name");var r = new u(L(e));W(r, function (t) {"option" === t ? (G(r, t), B(";")) : (F(t), X(r, "optional"));}), t.add(r);}(r, t);break;case "extensions":U(r.extensions || (r.extensions = []));break;case "reserved":U(r.reserved || (r.reserved = []), !0);break;default:if (!M || !x.test(t)) throw z(t);F(t), X(r, "optional");}}), t.add(r);}(t, e), !0;case "enum":return function (t, e) {if (!_.test(e = R())) throw z(e, "name");var r = new h(e);W(r, function (t) {switch (t) {case "option":G(r, t), B(";");break;case "reserved":U(r.reserved || (r.reserved = []), !0);break;default:!function (t, e) {if (!_.test(e)) throw z(e, "name");B("=");var r = q(R(), !0),i = {};W(i, function (t) {if ("option" !== t) throw z(t);G(i, t), B(";");}, function () {tt(i);}), t.add(e, r, i.comment);}(r, t);}}), t.add(r);}(t, e), !0;case "service":return function (t, e) {if (!_.test(e = R())) throw z(e, "service name");var r = new l(e);W(r, function (t) {if (!H(r, t)) {if ("rpc" !== t) throw z(t);!function (t, e) {var r = e;if (!_.test(e = R())) throw z(e, "name");var i,n,o,s,a = e;if (B("("), B("stream", !0) && (n = !0), !x.test(e = R())) throw z(e);if (i = e, B(")"), B("returns"), B("("), B("stream", !0) && (s = !0), !x.test(e = R())) throw z(e);o = e, B(")");var u = new f(a, r, i, o, n, s);W(u, function (t) {if ("option" !== t) throw z(t);G(u, t), B(";");}), t.add(u);}(r, t);}}), t.add(r);}(t, e), !0;case "extend":return function (t, e) {if (!x.test(e = R())) throw z(e, "reference");var r = e;W(null, function (e) {switch (e) {case "required":case "repeated":case "optional":X(t, e, r);break;default:if (!M || !x.test(e)) throw z(e);F(e), X(t, "optional", r);}});}(t, e), !0;}return !1;}function W(t, e, r) {var i = j.line;if (t && (t.comment = P(), t.filename = A.filename), B("{", !0)) {for (var n; "}" !== (n = R());) e(n);B(";", !0);} else r && r(), B(";"), t && "string" != typeof t.comment && (t.comment = P(i));}function X(t, e, r) {var i = R();if ("group" !== i) {if (!x.test(i)) throw z(i, "type");var n = R();if (!_.test(n)) throw z(n, "name");n = L(n), B("=");var a = new s(n, q(R()), i, e, r);W(a, function (t) {if ("option" !== t) throw z(t);G(a, t), B(";");}, function () {tt(a);}), t.add(a), M || !a.repeated || void 0 === c.packed[i] && void 0 !== c.basic[i] || a.setOption("packed", !1, !0);} else !function (t, e) {var r = R();if (!_.test(r)) throw z(r, "name");var i = d.lcFirst(r);r === i && (r = d.ucFirst(r)), B("=");var n = q(R()),a = new o(r);a.group = !0;var u = new s(i, n, r, e);u.filename = A.filename, W(a, function (t) {switch (t) {case "option":G(a, t), B(";");break;case "required":case "optional":case "repeated":X(a, t);break;default:throw z(t);}}), t.add(a).add(u);}(t, e);}function G(t, e) {var r = B("(", !0);if (!x.test(e = R())) throw z(e, "name");var i = e;r && (B(")"), i = "(" + i + ")", e = I(), k.test(e) && (i += e, R())), B("="), Y(t, i);}function Y(t, e) {if (B("{", !0)) do {if (!_.test(T = R())) throw z(T, "name");"{" === I() ? Y(t, e + "." + T) : (B(":"), "{" === I() ? Y(t, e + "." + T) : Q(t, e + "." + T, Z(!0)));} while (!B("}", !0));else Q(t, e, Z(!0));}function Q(t, e, r) {t.setOption && t.setOption(e, r);}function tt(t) {if (B("[", !0)) {do {G(t, "option");} while (B(",", !0));B("]");}return t;}for (; null !== (T = R());) switch (T) {case "package":if (!C) throw z(T);J();break;case "import":if (!C) throw z(T);$();break;case "syntax":if (!C) throw z(T);K();break;case "option":if (!C) throw z(T);G(D, T), B(";");break;default:if (H(D, T)) {C = !1;continue;}throw z(T);}return A.filename = null, { package: O, imports: S, weakImports: E, syntax: N, root: e };}A._configure = function () {i = t(27), n = t(23), o = t(28), s = t(9), a = t(13), u = t(18), h = t(8), l = t(26), f = t(15), c = t(29), d = t(31);};}, { 13: 13, 15: 15, 18: 18, 23: 23, 26: 26, 27: 27, 28: 28, 29: 29, 31: 31, 8: 8, 9: 9 }], 17: [function (t, e, r) {"use strict";var i, n;function o(t, e) {if (!i.isString(t)) throw TypeError("name must be a string");if (e && !i.isObject(e)) throw TypeError("options must be an object");this.options = e, this.name = t, this.parent = null, this.resolved = !1, this.comment = null, this.filename = null;}e.exports = o, o.className = "ReflectionObject", Object.defineProperties(o.prototype, { root: { get: function () {for (var t = this; null !== t.parent;) t = t.parent;return t;} }, fullName: { get: function () {for (var t = [this.name], e = this.parent; e;) t.unshift(e.name), e = e.parent;return t.join(".");} } }), o.prototype.toJSON = function () {throw Error();}, o.prototype.onAdd = function (t) {this.parent && this.parent !== t && this.parent.remove(this), this.parent = t, this.resolved = !1;var e = t.root;e instanceof n && e._handleAdd(this);}, o.prototype.onRemove = function (t) {var e = t.root;e instanceof n && e._handleRemove(this), this.parent = null, this.resolved = !1;}, o.prototype.resolve = function () {return this.resolved || this.root instanceof n && (this.resolved = !0), this;}, o.prototype.getOption = function (t) {if (this.options) return this.options[t];}, o.prototype.setOption = function (t, e, r) {return r && this.options && void 0 !== this.options[t] || ((this.options || (this.options = {}))[t] = e), this;}, o.prototype.setOptions = function (t, e) {if (t) for (var r = Object.keys(t), i = 0; i < r.length; ++i) this.setOption(r[i], t[r[i]], e);return this;}, o.prototype.toString = function () {var t = this.constructor.className,e = this.fullName;return e.length ? t + " " + e : t;}, o._configure = function (e) {n = t(23), i = t(31);};}, { 23: 23, 31: 31 }], 16: [function (t, e, r) {"use strict";e.exports = l;var i,n,o,s,a,u = t(17);function h(t, e) {if (t && t.length) {for (var r = {}, i = 0; i < t.length; ++i) r[t[i].name] = t[i].toJSON(e);return r;}}function l(t, e) {u.call(this, t, e), this.nested = void 0, this._nestedArray = null;}function f(t) {return t._nestedArray = null, t;}((l.prototype = Object.create(u.prototype)).constructor = l).className = "Namespace", l.fromJSON = function (t, e) {return new l(t, e.options).addJSON(e.nested);}, l.arrayToJSON = h, l.isReservedId = function (t, e) {if (t) for (var r = 0; r < t.length; ++r) if ("string" != typeof t[r] && t[r][0] <= e && t[r][1] >= e) return !0;return !1;}, l.isReservedName = function (t, e) {if (t) for (var r = 0; r < t.length; ++r) if (t[r] === e) return !0;return !1;}, Object.defineProperty(l.prototype, "nestedArray", { get: function () {return this._nestedArray || (this._nestedArray = o.toArray(this.nested));} }), l.prototype.toJSON = function (t) {return o.toObject(["options", this.options, "nested", h(this.nestedArray, t)]);}, l.prototype.addJSON = function (t) {if (t) for (var e, r = Object.keys(t), o = 0; o < r.length; ++o) e = t[r[o]], this.add((void 0 !== e.fields ? s.fromJSON : void 0 !== e.values ? i.fromJSON : void 0 !== e.methods ? a.fromJSON : void 0 !== e.id ? n.fromJSON : l.fromJSON)(r[o], e));return this;}, l.prototype.get = function (t) {return this.nested && this.nested[t] || null;}, l.prototype.getEnum = function (t) {if (this.nested && this.nested[t] instanceof i) return this.nested[t].values;throw Error("no such enum: " + t);}, l.prototype.add = function (t) {if (!(t instanceof n && void 0 !== t.extend || t instanceof s || t instanceof i || t instanceof a || t instanceof l)) throw TypeError("object must be a valid nested object");if (this.nested) {var e = this.get(t.name);if (e) {if (!(e instanceof l && t instanceof l) || e instanceof s || e instanceof a) throw Error("duplicate name '" + t.name + "' in " + this);for (var r = e.nestedArray, o = 0; o < r.length; ++o) t.add(r[o]);this.remove(e), this.nested || (this.nested = {}), t.setOptions(e.options, !0);}} else this.nested = {};return this.nested[t.name] = t, t.onAdd(this), f(this);}, l.prototype.remove = function (t) {if (!(t instanceof u)) throw TypeError("object must be a ReflectionObject");if (t.parent !== this) throw Error(t + " is not a member of " + this);return delete this.nested[t.name], Object.keys(this.nested).length || (this.nested = void 0), t.onRemove(this), f(this);}, l.prototype.define = function (t, e) {if (o.isString(t)) t = t.split(".");else if (!Array.isArray(t)) throw TypeError("illegal path");if (t && t.length && "" === t[0]) throw Error("path must be relative");for (var r = this; t.length > 0;) {var i = t.shift();if (r.nested && r.nested[i]) {if (!((r = r.nested[i]) instanceof l)) throw Error("path conflicts with non-namespace objects");} else r.add(r = new l(i));}return e && r.addJSON(e), r;}, l.prototype.resolveAll = function () {for (var t = this.nestedArray, e = 0; e < t.length;) t[e] instanceof l ? t[e++].resolveAll() : t[e++].resolve();return this.resolve();}, l.prototype.lookup = function (t, e, r) {if ("boolean" == typeof e ? (r = e, e = void 0) : e && !Array.isArray(e) && (e = [e]), o.isString(t) && t.length) {if ("." === t) return this.root;t = t.split(".");} else if (!t.length) return this;if ("" === t[0]) return this.root.lookup(t.slice(1), e);var i = this.get(t[0]);if (i) {if (1 === t.length) {if (!e || e.indexOf(i.constructor) > -1) return i;} else if (i instanceof l && (i = i.lookup(t.slice(1), e, !0))) return i;} else for (var n = 0; n < this.nestedArray.length; ++n) if (this._nestedArray[n] instanceof l && (i = this._nestedArray[n].lookup(t, e, !0))) return i;return null === this.parent || r ? null : this.parent.lookup(t, e);}, l.prototype.lookupType = function (t) {var e = this.lookup(t, [s]);if (!e) throw Error("no such type: " + t);return e;}, l.prototype.lookupEnum = function (t) {var e = this.lookup(t, [i]);if (!e) throw Error("no such Enum '" + t + "' in " + this);return e;}, l.prototype.lookupTypeOrEnum = function (t) {var e = this.lookup(t, [s, i]);if (!e) throw Error("no such Type or Enum '" + t + "' in " + this);return e;}, l.prototype.lookupService = function (t) {var e = this.lookup(t, [a]);if (!e) throw Error("no such Service '" + t + "' in " + this);return e;}, l._configure = function () {i = t(8), n = t(9), o = t(31), s = t(28), a = t(26);};}, { 17: 17, 26: 26, 28: 28, 31: 31, 8: 8, 9: 9 }], 8: [function (t, e, r) {"use strict";e.exports = o;var i = t(17);((o.prototype = Object.create(i.prototype)).constructor = o).className = "Enum";var n = t(16);function o(t, e, r, n, o) {if (i.call(this, t, r), e && "object" != typeof e) throw TypeError("values must be an object");if (this.valuesById = {}, this.values = Object.create(this.valuesById), this.comment = n, this.comments = o || {}, this.reserved = void 0, e) for (var s = Object.keys(e), a = 0; a < s.length; ++a) "number" == typeof e[s[a]] && (this.valuesById[this.values[s[a]] = e[s[a]]] = s[a]);}o.fromJSON = function (t, e) {var r = new o(t, e.values, e.options, e.comment, e.comments);return r.reserved = e.reserved, r;}, o.prototype.toJSON = function (t) {var e = !!t && Boolean(t.keepComments);return util.toObject(["options", this.options, "values", this.values, "reserved", this.reserved && this.reserved.length ? this.reserved : void 0, "comment", e ? this.comment : void 0, "comments", e ? this.comments : void 0]);}, o.prototype.add = function (t, e, r) {if (!util.isString(t)) throw TypeError("name must be a string");if (!util.isInteger(e)) throw TypeError("id must be an integer");if (void 0 !== this.values[t]) throw Error("duplicate name '" + t + "' in " + this);if (this.isReservedId(e)) throw Error("id " + e + " is reserved in " + this);if (this.isReservedName(t)) throw Error("name '" + t + "' is reserved in " + this);if (void 0 !== this.valuesById[e]) {if (!this.options || !this.options.allow_alias) throw Error("duplicate id " + e + " in " + this);this.values[t] = e;} else this.valuesById[this.values[t] = e] = t;return this.comments[t] = r || null, this;}, o.prototype.remove = function (t) {if (!util.isString(t)) throw TypeError("name must be a string");var e = this.values[t];if (null == e) throw Error("name '" + t + "' does not exist in " + this);return delete this.valuesById[e], delete this.values[t], delete this.comments[t], this;}, o.prototype.isReservedId = function (t) {return n.isReservedId(this.reserved, t);}, o.prototype.isReservedName = function (t) {return n.isReservedName(this.reserved, t);};}, { 16: 16, 17: 17 }], 23: [function (t, e, r) {"use strict";e.exports = f;var i = t(16);((f.prototype = Object.create(i.prototype)).constructor = f).className = "Root";var n,o,s,a = t(9),u = t(8),h = t(18),l = t(31);function f(t) {i.call(this, "", t), this.deferred = [], this.files = [], this.names = [];}function c() {}f.fromJSON = function (t, e) {return t = "string" == typeof t ? JSON.parse(t) : t, e || (e = new f()), t.options && e.setOptions(t.options), e.addJSON(t.nested);}, f.prototype.resolvePath = l.path.resolve, f.prototype.parseFromPbString = function t(e, r, i) {"function" == typeof r && (i = r, r = void 0);var n = this;if (!i) return l.asPromise(t, n, e, r);var a = null;if ("string" == typeof e) a = JSON.parse(e);else {if ("object" != typeof e) return void console.log("pb\u683c\u5f0f\u8f6c\u5316\u5931\u8d25");a = e;}function u(t, e) {if (i) {var r = i;i = null, r(t, e);}}function h(t, e) {try {if (l.isString(e) && "{" === e.charAt(0) && (e = JSON.parse(e)), l.isString(e)) {o.filename = t;var i,s = o(e, n, r),a = 0;if (s.imports) for (; a < s.imports.length; ++a) f(i = s.imports[a]);if (s.weakImports) {for (a = 0; a < s.weakImports.length; ++a) i = s.weakImports[a];f(i);}} else n.setOptions(e.options).addJSON(e.nested);} catch (h) {u(h);}u(null, n);}function f(t) {n.names.indexOf(t) > -1 || (n.names.push(t), t in s && h(t, s[t]));}h(a.name, a.pbJsonStr);}, f.prototype.load = function t(e, r, i) {"function" == typeof r && (i = r, r = void 0);var n = this;if (!i) return l.asPromise(t, n, e, r);var a = i === c;function u(t, e) {if (i) {var r = i;if (i = null, a) throw t;r(t, e);}}function h(t, e) {try {if (l.isString(e) && "{" === e.charAt(0) && (e = JSON.parse(e)), l.isString(e)) {o.filename = t;var i,s = o(e, n, r),h = 0;if (s.imports) for (; h < s.imports.length; ++h) (i = n.resolvePath(t, s.imports[h])) && f(i);if (s.weakImports) for (h = 0; h < s.weakImports.length; ++h) (i = n.resolvePath(t, s.weakImports[h])) && f(i, !0);} else n.setOptions(e.options).addJSON(e.nested);} catch (c) {u(c);}a || d || u(null, n);}function f(t, e) {var r = t.lastIndexOf("google/protobuf/");if (r > -1) {var o = t.substring(r);o in s && (t = o);}if (!(n.files.indexOf(t) > -1)) if (n.files.push(t), t in s) a ? h(t, s[t]) : (++d, setTimeout(function () {--d, h(t, s[t]);}));else if (a) {var f;try {f = l.fs.readFileSync(t).toString("utf8");} catch (c) {return void (e || u(c));}h(t, f);} else ++d, l.fetch(t, function (r, o) {--d, i && (r ? e ? d || u(null, n) : u(r) : h(t, o));});}var d = 0;l.isString(e) && (e = [e]);for (var p, y = 0; y < e.length; ++y) (p = n.resolvePath("", e[y])) && f(p);if (a) return n;d || u(null, n);}, f.prototype.loadSync = function (t, e) {if (!l.isNode) throw Error("not supported");return this.load(t, e, c);}, f.prototype.resolveAll = function () {if (this.deferred.length) throw Error("unresolvable extensions: " + this.deferred.map(function (t) {return "'extend " + t.extend + "' in " + t.parent.fullName;}).join(", "));return i.prototype.resolveAll.call(this);};var d = /^[A-Z]/;function p(t, e) {var r = e.parent.lookup(e.extend);if (r) {var i = new a(e.fullName, e.id, e.type, e.rule, void 0, e.options);return i.declaringField = e, e.extensionField = i, r.add(i), !0;}return !1;}f.prototype._handleAdd = function (t) {if (t instanceof a) void 0 === t.extend || t.extensionField || p(0, t) || this.deferred.push(t);else if (t instanceof u) d.test(t.name) && (t.parent[t.name] = t.values);else if (!(t instanceof h)) {if (t instanceof n) for (var e = 0; e < this.deferred.length;) p(0, this.deferred[e]) ? this.deferred.splice(e, 1) : ++e;for (var r = 0; r < t.nestedArray.length; ++r) this._handleAdd(t._nestedArray[r]);d.test(t.name) && (t.parent[t.name] = t);}}, f.prototype._handleRemove = function (t) {if (t instanceof a) {if (void 0 !== t.extend) if (t.extensionField) t.extensionField.parent.remove(t.extensionField), t.extensionField = null;else {var e = this.deferred.indexOf(t);e > -1 && this.deferred.splice(e, 1);}} else if (t instanceof u) d.test(t.name) && delete t.parent[t.name];else if (t instanceof i) {for (var r = 0; r < t.nestedArray.length; ++r) this._handleRemove(t._nestedArray[r]);d.test(t.name) && delete t.parent[t.name];}}, f._configure = function () {n = t(28), o = t(19), s = t(5), a = t(9), u = t(8), h = t(18), l = t(31);};}, { 16: 16, 18: 18, 19: 19, 28: 28, 31: 31, 5: 5, 8: 8, 9: 9 }], 28: [function (t, e, r) {"use strict";e.exports = m;var i,n,o,s,a,u,h,l,f,c,d,p,y = t(16);function m(t, e) {y.call(this, t, e), this.fields = {}, this.oneofs = void 0, this.extensions = void 0, this.reserved = void 0, this.group = void 0, this._fieldsById = null, this._fieldsArray = null, this._oneofsArray = null, this._ctor = null;}function v(t) {return t._fieldsById = t._fieldsArray = t._oneofsArray = null, delete t.encode, delete t.decode, delete t.verify, t;}((m.prototype = Object.create(y.prototype)).constructor = m).className = "Type", Object.defineProperties(m.prototype, { fieldsById: { get: function () {if (this._fieldsById) return this._fieldsById;this._fieldsById = {};for (var t = Object.keys(this.fields), e = 0; e < t.length; ++e) {var r = this.fields[t[e]],i = r.id;if (this._fieldsById[i]) throw Error("duplicate id " + i + " in " + this);this._fieldsById[i] = r;}return this._fieldsById;} }, fieldsArray: { get: function () {return this._fieldsArray || (this._fieldsArray = u.toArray(this.fields));} }, oneofsArray: { get: function () {return this._oneofsArray || (this._oneofsArray = u.toArray(this.oneofs));} }, ctor: { get: function () {return this._ctor || (this.ctor = m.generateConstructor(this));}, set: function (t) {var e = t.prototype;e instanceof o || ((t.prototype = new o()).constructor = t, u.merge(t.prototype, e)), t.$type = t.prototype.$type = this, u.merge(t, o, !0), u.merge(t.prototype, o, !0), this._ctor = t;for (var r = 0; r < this.fieldsArray.length; ++r) this._fieldsArray[r].resolve();var i = {};for (r = 0; r < this.oneofsArray.length; ++r) {var n = this._oneofsArray[r].resolve().name,s = function (t) {for (var e = {}, r = 0; r < t.length; ++r) e[t[r]] = 0;return { setter: function (r) {if (!(t.indexOf(r) < 0)) {e[r] = 1;for (var i = 0; i < t.length; ++i) t[i] !== r && delete this[t[i]];}}, getter: function () {for (var t = Object.keys(this), r = t.length - 1; r > -1; --r) if (1 === e[t[r]] && void 0 !== this[t[r]] && null !== this[t[r]]) return t[r];} };}(this._oneofsArray[r].oneof);i[n] = { get: s.getter, set: s.setter };}r && Object.defineProperties(t.prototype, i);} } }), m.generateConstructor = function (t) {return function (e) {for (var r, i = 0; i < t.fieldsArray.length; i++) (r = t._fieldsArray[i]).map ? this[r.name] = {} : r.repeated && (this[r.name] = []);if (e) for (var n = Object.keys(e), o = 0; o < n.length; ++o) null != e[n[o]] && (this[n[o]] = e[n[o]]);};}, m.fromJSON = function (t, e) {var r = new m(t, e.options);r.extensions = e.extensions, r.reserved = e.reserved;for (var o = Object.keys(e.fields), a = 0; a < o.length; ++a) r.add((void 0 !== e.fields[o[a]].keyType ? p.fromJSON : n.fromJSON)(o[a], e.fields[o[a]]));if (e.oneofs) for (o = Object.keys(e.oneofs), a = 0; a < o.length; ++a) r.add(s.fromJSON(o[a], e.oneofs[o[a]]));if (e.nested) for (o = Object.keys(e.nested), a = 0; a < o.length; ++a) {var u = e.nested[o[a]];r.add((void 0 !== u.id ? n.fromJSON : void 0 !== u.fields ? m.fromJSON : void 0 !== u.values ? i.fromJSON : void 0 !== u.methods ? f.fromJSON : y.fromJSON)(o[a], u));}return e.extensions && e.extensions.length && (r.extensions = e.extensions), e.reserved && e.reserved.length && (r.reserved = e.reserved), e.group && (r.group = !0), e.comment && (r.comment = e.comment), r;}, m.prototype.toJSON = function (t) {var e = y.prototype.toJSON.call(this, t),r = !!t && Boolean(t.keepComments);return { options: e && e.options || void 0, oneofs: y.arrayToJSON(this.oneofsArray, t), fields: y.arrayToJSON(this.fieldsArray.filter(function (t) {return !t.declaringField;}), t) || {}, extensions: this.extensions && this.extensions.length ? this.extensions : void 0, reserved: this.reserved && this.reserved.length ? this.reserved : void 0, group: this.group || void 0, nested: e && e.nested || void 0, comment: r ? this.comment : void 0 };}, m.prototype.resolveAll = function () {for (var t = this.fieldsArray, e = 0; e < t.length;) t[e++].resolve();var r = this.oneofsArray;for (e = 0; e < r.length;) r[e++].resolve();return y.prototype.resolveAll.call(this);}, m.prototype.get = function (t) {return this.fields[t] || this.oneofs && this.oneofs[t] || this.nested && this.nested[t] || null;}, m.prototype.add = function (t) {if (this.get(t.name)) throw Error("duplicate name '" + t.name + "' in " + this);if (t instanceof n && void 0 === t.extend) {if (this._fieldsById && this._fieldsById[t.id]) throw Error("duplicate id " + t.id + " in " + this);if (this.isReservedId(t.id)) throw Error("id " + t.id + " is reserved in " + this);if (this.isReservedName(t.name)) throw Error("name '" + t.name + "' is reserved in " + this);return t.parent && t.parent.remove(t), this.fields[t.name] = t, t.message = this, t.onAdd(this), v(this);}return t instanceof s ? (this.oneofs || (this.oneofs = {}), this.oneofs[t.name] = t, t.onAdd(this), v(this)) : y.prototype.add.call(this, t);}, m.prototype.remove = function (t) {if (t instanceof n && void 0 === t.extend) {if (!this.fields || this.fields[t.name] !== t) throw Error(t + " is not a member of " + this);return delete this.fields[t.name], t.parent = null, t.onRemove(this), v(this);}if (t instanceof s) {if (!this.oneofs || this.oneofs[t.name] !== t) throw Error(t + " is not a member of " + this);return delete this.oneofs[t.name], t.parent = null, t.onRemove(this), v(this);}return y.prototype.remove.call(this, t);}, m.prototype.isReservedId = function (t) {return y.isReservedId(this.reserved, t);}, m.prototype.isReservedName = function (t) {return y.isReservedName(this.reserved, t);}, m.prototype.create = function (t) {return new this.ctor(t);}, m.prototype.setup = function () {for (var t = this.fullName, e = [], r = 0; r < this.fieldsArray.length; ++r) e.push(this._fieldsArray[r].resolve().resolvedType);this.decode = l(this)({ Reader: a, types: e, util: u }), this.verify = h(this)({ types: e, util: u }), this.fromObject = d.fromObject(this)({ types: e, util: u }), this.toObject = d.toObject(this)({ types: e, util: u });var i = c[t];if (i) {var n = Object.create(this);n.fromObject = this.fromObject, this.fromObject = i.fromObject.bind(n), n.toObject = this.toObject, this.toObject = i.toObject.bind(n);}return this;}, m.prototype.encode = function (t, e) {return this.setup().encode(t, e);}, m.prototype.encodeDelimited = function (t, e) {return this.encode(t, e && e.len ? e.fork() : e).ldelim();}, m.prototype.decode = function (t, e) {return this.setup().decode(t, e);}, m.prototype.decodeDelimited = function (t) {return t instanceof a || (t = a.create(t)), this.decode(t, t.uint32());}, m.prototype.verify = function (t) {return this.setup().verify(t);}, m.prototype.fromObject = function (t) {return this.setup().fromObject(t);}, m.prototype.toObject = function (t, e) {return this.setup().toObject(t, e);}, m.d = function (t) {return function (e) {u.decorateType(e, t);};}, m._configure = function () {i = t(8), n = t(9), o = t(14), s = t(18), t(34), a = t(22), u = t(31), h = t(32), l = t(7), f = t(26), c = t(33), d = t(6), p = t(13);};}, { 13: 13, 14: 14, 16: 16, 18: 18, 22: 22, 26: 26, 31: 31, 32: 32, 33: 33, 34: 34, 6: 6, 7: 7, 8: 8, 9: 9 }], 18: [function (t, e, r) {"use strict";e.exports = s;var i,n,o = t(17);function s(t, e, r, i) {if (Array.isArray(e) || (r = e, e = void 0), o.call(this, t, r), void 0 !== e && !Array.isArray(e)) throw TypeError("fieldNames must be an Array");this.oneof = e || [], this.fieldsArray = [], this.comment = i;}function a(t) {if (t.parent) for (var e = 0; e < t.fieldsArray.length; ++e) t.fieldsArray[e].parent || t.parent.add(t.fieldsArray[e]);}((s.prototype = Object.create(o.prototype)).constructor = s).className = "OneOf", s.fromJSON = function (t, e) {return new s(t, e.oneof, e.options, e.comment);}, s.prototype.toJSON = function (t) {var e = !!t && Boolean(t.keepComments);return n.toObject(["options", this.options, "oneof", this.oneof, "comment", e ? this.comment : void 0]);}, s.prototype.add = function (t) {if (!(t instanceof i)) throw TypeError("field must be a Field");return t.parent && t.parent !== this.parent && t.parent.remove(t), this.oneof.push(t.name), this.fieldsArray.push(t), t.partOf = this, a(this), this;}, s.prototype.remove = function (t) {if (!(t instanceof i)) throw TypeError("field must be a Field");var e = this.fieldsArray.indexOf(t);if (e < 0) throw Error(t + " is not a member of " + this);return this.fieldsArray.splice(e, 1), (e = this.oneof.indexOf(t.name)) > -1 && this.oneof.splice(e, 1), t.partOf = null, this;}, s.prototype.onAdd = function (t) {o.prototype.onAdd.call(this, t);for (var e = 0; e < this.oneof.length; ++e) {var r = t.get(this.oneof[e]);r && !r.partOf && (r.partOf = this, this.fieldsArray.push(r));}a(this);}, s.prototype.onRemove = function (t) {for (var e, r = 0; r < this.fieldsArray.length; ++r) (e = this.fieldsArray[r]).parent && e.parent.remove(e);o.prototype.onRemove.call(this, t);}, s.d = function () {for (var t = new Array(arguments.length), e = 0; e < arguments.length;) t[e] = arguments[e++];return function (e, r) {n.decorateType(e.constructor).add(new s(r, t)), Object.defineProperty(e, r, { get: n.oneOfGetter(t), set: n.oneOfSetter(t) });};}, s._configure = function () {i = t(9), n = t(31);};}, { 17: 17, 31: 31, 9: 9 }], 9: [function (t, e, r) {"use strict";e.exports = h;var i,n,o,s,a = t(17);((h.prototype = Object.create(a.prototype)).constructor = h).className = "Field";var u = /^required|optional|repeated$/;function h(t, e, r, i, s, h, l) {if (o.isObject(i) ? (l = s, h = i, i = s = void 0) : o.isObject(s) && (l = h, h = s, s = void 0), a.call(this, t, h), !o.isInteger(e) || e < 0) throw TypeError("id must be a non-negative integer");if (!o.isString(r)) throw TypeError("type must be a string");if (void 0 !== i && !u.test(i = i.toString().toLowerCase())) throw TypeError("rule must be a string rule");if (void 0 !== s && !o.isString(s)) throw TypeError("extend must be a string");this.rule = i && "optional" !== i ? i : void 0, this.type = r, this.id = e, this.extend = s || void 0, this.required = "required" === i, this.optional = !this.required, this.repeated = "repeated" === i, this.map = !1, this.message = null, this.partOf = null, this.typeDefault = null, this.defaultValue = null, this.long = !!o.Long && void 0 !== n.long[r], this.bytes = "bytes" === r, this.resolvedType = null, this.extensionField = null, this.declaringField = null, this._packed = null, this.comment = l;}h.fromJSON = function (t, e) {return new h(t, e.id, e.type, e.rule, e.extend, e.options, e.comment);}, Object.defineProperty(h.prototype, "packed", { get: function () {return null === this._packed && (this._packed = !1 !== this.getOption("packed")), this._packed;} }), h.prototype.setOption = function (t, e, r) {return "packed" === t && (this._packed = null), a.prototype.setOption.call(this, t, e, r);}, h.prototype.toJSON = function (t) {var e = !!t && Boolean(t.keepComments);return o.toObject(["rule", "optional" !== this.rule && this.rule || void 0, "type", this.type, "id", this.id, "extend", this.extend, "options", this.options, "comment", e ? this.comment : void 0]);}, h.prototype.resolve = function () {if (this.resolved) return this;if (void 0 === (this.typeDefault = n.defaults[this.type]) && (this.resolvedType = (this.declaringField ? this.declaringField.parent : this.parent).lookupTypeOrEnum(this.type), this.resolvedType instanceof s ? this.typeDefault = null : this.typeDefault = this.resolvedType.values[Object.keys(this.resolvedType.values)[0]]), this.options && null != this.options.default && (this.typeDefault = this.options.default, this.resolvedType instanceof i && "string" == typeof this.typeDefault && (this.typeDefault = this.resolvedType.values[this.typeDefault])), this.options && (!0 !== this.options.packed && (void 0 === this.options.packed || !this.resolvedType || this.resolvedType instanceof i) || delete this.options.packed, Object.keys(this.options).length || (this.options = void 0)), this.long) this.typeDefault = o.Long.fromNumber(this.typeDefault, "u" === this.type.charAt(0)), Object.freeze && Object.freeze(this.typeDefault);else if (this.bytes && "string" == typeof this.typeDefault) {var t;o.utf8.write(this.typeDefault, t = o.newBuffer(o.utf8.length(this.typeDefault)), 0), this.typeDefault = t;}return this.map ? this.defaultValue = o.emptyObject : this.repeated ? this.defaultValue = o.emptyArray : this.defaultValue = this.typeDefault, this.parent instanceof s && (this.parent.ctor.prototype[this.name] = this.defaultValue), a.prototype.resolve.call(this);}, h.d = function (t, e, r, i) {return "function" == typeof e ? e = o.decorateType(e).name : e && "object" == typeof e && (e = o.decorateEnum(e).name), function (n, s) {o.decorateType(n.constructor).add(new h(s, t, e, r, { default: i }));};}, h._configure = function () {s = t(28), i = t(8), n = t(29), o = t(31);};}, { 17: 17, 28: 28, 29: 29, 31: 31, 8: 8 }], 13: [function (t, e, r) {"use strict";e.exports = s;var i,n,o = t(9);function s(t, e, r, i, s, a) {if (o.call(this, t, e, i, void 0, void 0, s, a), !n.isString(r)) throw TypeError("keyType must be a string");this.keyType = r, this.resolvedKeyType = null, this.map = !0;}((s.prototype = Object.create(o.prototype)).constructor = s).className = "MapField", s.fromJSON = function (t, e) {return new s(t, e.id, e.keyType, e.type, e.options, e.comment);}, s.prototype.toJSON = function (t) {var e = !!t && Boolean(t.keepComments);return n.toObject(["keyType", this.keyType, "type", this.type, "id", this.id, "extend", this.extend, "options", this.options, "comment", e ? this.comment : void 0]);}, s.prototype.resolve = function () {if (this.resolved) return this;if (void 0 === i.mapKey[this.keyType]) throw Error("invalid key type: " + this.keyType);return o.prototype.resolve.call(this);}, s.d = function (t, e, r) {return "function" == typeof r ? r = n.decorateType(r).name : r && "object" == typeof r && (r = n.decorateEnum(r).name), function (i, o) {n.decorateType(i.constructor).add(new s(o, t, e, r));};}, s._configure = function () {i = t(29), n = t(31);};}, { 29: 29, 31: 31, 9: 9 }], 15: [function (t, e, r) {"use strict";e.exports = o;var i,n = t(17);function o(t, e, r, o, s, a, u, h) {if (i.isObject(s) ? (u = s, s = a = void 0) : i.isObject(a) && (u = a, a = void 0), void 0 !== e && !i.isString(e)) throw TypeError("type must be a string");if (!i.isString(r)) throw TypeError("requestType must be a string");if (!i.isString(o)) throw TypeError("responseType must be a string");n.call(this, t, u), this.type = e || "rpc", this.requestType = r, this.requestStream = !!s || void 0, this.responseType = o, this.responseStream = !!a || void 0, this.resolvedRequestType = null, this.resolvedResponseType = null, this.comment = h;}((o.prototype = Object.create(n.prototype)).constructor = o).className = "Method", o.fromJSON = function (t, e) {return new o(t, e.type, e.requestType, e.responseType, e.requestStream, e.responseStream, e.options, e.comment);}, o.prototype.toJSON = function (t) {var e = !!t && Boolean(t.keepComments);return i.toObject(["type", "rpc" !== this.type && this.type || void 0, "requestType", this.requestType, "requestStream", this.requestStream, "responseType", this.responseType, "responseStream", this.responseStream, "options", this.options, "comment", e ? this.comment : void 0]);}, o.prototype.resolve = function () {return this.resolved ? this : (this.resolvedRequestType = this.parent.lookupType(this.requestType), this.resolvedResponseType = this.parent.lookupType(this.responseType), n.prototype.resolve.call(this));}, o._configure = function () {i = t(31);};}, { 17: 17, 31: 31 }], 7: [function (t, e, r) {"use strict";var i, n, o;function s(t) {return "missing required '" + t.name + "'";}function a(t) {return function (e) {var r = e.Reader,a = e.types,u = e.util;return function (e, h) {e instanceof r || (e = r.create(e));for (var l, f = void 0 === h ? e.len : e.pos + h, c = new this.ctor(); e.pos < f;) {var d = e.uint32();if (t.group && 4 == (7 & d)) break;for (var p = d >>> 3, y = 0, m = !1; y < t.fieldsArray.length; ++y) {var v = t._fieldsArray[y].resolve(),g = v.name,b = v.resolvedType instanceof i ? "int32" : v.type;if (p == v.id) {if (m = !0, v.map) e.skip().pos++, c[g] === u.emptyObject && (c[g] = {}), l = e[v.keyType](), e.pos++, n.long[v.keyType], null == n.basic[b] ? c[g]["object" == typeof l ? u.longToHash(l) : l] = a[y].decode(e, e.uint32()) : c[g]["object" == typeof l ? u.longToHash(l) : l] = e[b]();else if (v.repeated) {if (c[g] && c[g].length || (c[g] = []), null != n.packed[b] && 2 == (7 & d)) for (var w = e.uint32() + e.pos; e.pos < w;) c[g].push(e[b]());else null == n.basic[b] ? v.resolvedType.group ? c[g].push(a[y].decode(e)) : c[g].push(a[y].decode(e, e.uint32())) : c[g].push(e[b]());} else null == n.basic[b] ? v.resolvedType.group ? c[g] = a[y].decode(e) : c[g] = a[y].decode(e, e.uint32()) : c[g] = e[b]();break;}}m || (console.log("t", d), e.skipType(7 & d));}for (y = 0; y < t._fieldsArray.length; ++y) {var _ = t._fieldsArray[y];if (_.required && !c.hasOwnProperty(_.name)) throw o.ProtocolError(s(_), { instance: c });}return c;};};}e.exports = a, a._configure = function () {i = t(8), n = t(29), o = t(31);};}, { 29: 29, 31: 31, 8: 8 }], 14: [function (t, e, r) {"use strict";var i;function n(t) {if (t) for (var e = Object.keys(t), r = 0; r < e.length; ++r) this[e[r]] = t[e[r]];}e.exports = n, n.create = function (t) {return this.$type.create(t);}, n.encode = function (t, e) {return arguments.length ? 1 == arguments.length ? this.$type.encode(arguments[0]) : this.$type.encode(arguments[0], arguments[1]) : this.$type.encode(this);}, n.encodeDelimited = function (t, e) {return this.$type.encodeDelimited(t, e);}, n.decode = function (t) {return this.$type.decode(t);}, n.decodeDelimited = function (t) {return this.$type.decodeDelimited(t);}, n.verify = function (t) {return this.$type.verify(t);}, n.fromObject = function (t) {return this.$type.fromObject(t);}, n.toObject = function (t, e) {return t = t || this, this.$type.toObject(t, e);}, n.prototype.toJSON = function () {return this.$type.toObject(this, i.toJSONOptions);}, n.set = function (t, e) {n[t] = e;}, n.get = function (t) {return n[t];}, n._configure = function () {i = t(31);};}, { 31: 31 }], 29: [function (t, e, r) {"use strict";var i = e.exports,n = t(31),o = ["double", "float", "int32", "uint32", "sint32", "fixed32", "sfixed32", "int64", "uint64", "sint64", "fixed64", "sfixed64", "bool", "string", "bytes"];function s(t, e) {var r = 0,i = {};for (e |= 0; r < t.length;) i[o[r + e]] = t[r++];return i;}i.basic = s([1, 5, 0, 0, 0, 5, 5, 0, 0, 0, 1, 1, 0, 2, 2]), i.defaults = s([0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, !1, "", n.emptyArray, null]), i.long = s([0, 0, 0, 1, 1], 7), i.mapKey = s([0, 0, 0, 5, 5, 0, 0, 0, 1, 1, 0, 2], 2), i.packed = s([1, 5, 0, 0, 0, 5, 5, 0, 0, 0, 1, 1, 0]), i._configure = function () {n = t(31);};}, { 31: 31 }], 33: [function (t, e, r) {"use strict";var i,n = r;n[".google.protobuf.Any"] = { fromObject: function (t) {if (t && t["@type"]) {var e = this.lookup(t["@type"]);if (e) {var r = "." === t["@type"].charAt(0) ? t["@type"].substr(1) : t["@type"];return this.create({ type_url: "/" + r, value: e.encode(e.fromObject(t)).finish() });}}return this.fromObject(t);}, toObject: function (t, e) {if (e && e.json && t.type_url && t.value) {var r = t.type_url.substring(t.type_url.lastIndexOf("/") + 1),n = this.lookup(r);n && (t = n.decode(t.value));}if (!(t instanceof this.ctor) && t instanceof i) {var o = t.$type.toObject(t, e);return o["@type"] = t.$type.fullName, o;}return this.toObject(t, e);} }, n._configure = function () {i = t(14);};}, { 14: 14 }], 6: [function (t, e, r) {"use strict";var i,n,o = e.exports;function s(t, e, r, o) {var s = o.m,a = o.d,u = o.types,h = o.ksi,l = void 0 !== h;if (t.resolvedType) {if (t.resolvedType instanceof i) {for (var f = l ? a[r][h] : a[r], c = t.resolvedType.values, d = Object.keys(c), p = 0; p < d.length; p++) if (!(t.repeated && c[d[p]] === t.typeDefault || d[p] != f && c[d[p]] != f)) {l ? s[r][h] = c[d[p]] : s[r] = c[d[p]];break;}} else {if ("object" != typeof (l ? a[r][h] : a[r])) throw TypeError(t.fullName + ": object expected");l ? s[r][h] = u[e].fromObject(a[r][h]) : s[r] = u[e].fromObject(a[r]);}} else {var y = !1;switch (t.type) {case "double":case "float":l ? s[r][h] = Number(a[r][h]) : s[r] = Number(a[r]);break;case "uint32":case "fixed32":l ? s[r][h] = a[r][h] >>> 0 : s[r] = a[r] >>> 0;break;case "int32":case "sint32":case "sfixed32":l ? s[r][h] = 0 | a[r][h] : s[r] = 0 | a[r];break;case "uint64":y = !0;case "int64":case "sint64":case "fixed64":case "sfixed64":n.Long ? l ? s[r][h] = n.Long.fromValue(a[r][h]).unsigned = y : s[r] = n.Long.fromValue(a[r]).unsigned = y : "string" == typeof (l ? a[r][h] : a[r]) ? l ? s[r][h] = parseInt(a[r][h], 10) : s[r] = parseInt(a[r], 10) : "number" == typeof (l ? a[r][h] : a[r]) ? l ? s[r][h] = a[r][h] : s[r] = a[r] : "object" == typeof (l ? a[r][h] : a[r]) && (l ? s[r][h] = new n.LongBits(a[r][h].low >>> 0, a[r][h].high >>> 0).toNumber(y) : s[r] = new n.LongBits(a[r].low >>> 0, a[r].high >>> 0).toNumber(y));break;case "bytes":"string" == typeof (l ? a[r][h] : a[r]) ? l ? n.base64.decode(a[r][h], s[r][h] = n.newBuffer(n.base64.length(a[r][h])), 0) : n.base64.decode(a[r], s[r] = n.newBuffer(n.base64.length(a[r])), 0) : (l ? a[r][h] : a[r]).length && (l ? s[r][h] = a[r][h] : s[r] = a[r]);break;case "string":l ? s[r][h] = String(a[r][h]) : s[r] = String(a[r]);break;case "bool":l ? s[r][h] = Boolean(a[r][h]) : s[r] = Boolean(a[r]);}}}function a(t, e, r, o) {var s = o.m,a = o.d,u = o.types,h = o.ksi,l = o.o,f = void 0 !== h;if (t.resolvedType) t.resolvedType instanceof i ? f ? a[r][h] = l.enums === String ? u[e].values[s[r][h]] : s[r][h] : a[r] = l.enums === String ? u[e].values[s[r]] : s[r] : f ? a[r][h] = u[e].toObject(s[r][h], l) : a[r] = u[e].toObject(s[r], l);else {var c = !1;switch (t.type) {case "double":case "float":f ? a[r][h] = l.json && !isFinite(s[r][h]) ? String(s[r][h]) : s[r][h] : a[r] = l.json && !isFinite(s[r]) ? String(s[r]) : s[r];break;case "uint64":c = !0;case "int64":case "sint64":case "fixed64":case "sfixed64":"number" == typeof s[r][h] ? f ? a[r][h] = l.longs === String ? String(s[r][h]) : s[r][h] : a[r] = l.longs === String ? String(s[r]) : s[r] : f ? a[r][h] = l.longs === String ? n.Long.prototype.toString.call(s[r][h]) : l.longs === Number ? new n.LongBits(s[r][h].low >>> 0, s[r][h].high >>> 0).toNumber(c) : s[r][h] : a[r] = l.longs === String ? n.Long.prototype.toString.call(s[r]) : l.longs === Number ? new n.LongBits(s[r].low >>> 0, s[r].high >>> 0).toNumber(c) : s[r];break;case "bytes":f ? a[r][h] = l.bytes === String ? n.base64.encode(s[r][h], 0, s[r][h].length) : l.bytes === Array ? Array.prototype.slice.call(s[r][h]) : s[r][h] : a[r] = l.bytes === String ? n.base64.encode(s[r], 0, s[r].length) : l.bytes === Array ? Array.prototype.slice.call(s[r]) : s[r];break;default:f ? a[r][h] = s[r][h] : a[r] = s[r];}}}o._configure = function () {i = t(8), n = t(31);}, o.fromObject = function (t) {var e = t.fieldsArray;return function (t) {return function (r) {if (r instanceof this.ctor) return r;if (!e.length) return new this.ctor();for (var o = new this.ctor(), a = 0; a < e.length; ++a) {var u,h = e[a].resolve(),l = h.name;if (h.map) {if (r[l]) {if ("object" != typeof r[l]) throw TypeError(h.fullName + ": object expected");o[l] = {};}var f = Object.keys(r[l]);for (u = 0; u < f.length; ++u) s(h, a, l, n.merge(n.copy(t), { m: o, d: r, ksi: f[u] }));} else if (h.repeated) {if (r[l]) {if (!Array.isArray(r[l])) throw TypeError(h.fullName + ": array expected");for (o[l] = [], u = 0; u < r[l].length; ++u) s(h, a, l, n.merge(n.copy(t), { m: o, d: r, ksi: u }));}} else (h.resolvedType instanceof i || null != r[l]) && s(h, a, l, n.merge(n.copy(t), { m: o, d: r }));}return o;};};}, o.toObject = function (t) {var e = t.fieldsArray.slice().sort(n.compareFieldsById);return function (r) {return e.length ? function (o, s) {s = s || {};for (var u, h, l = {}, f = [], c = [], d = [], p = 0; p < e.length; ++p) e[p].partOf || (e[p].resolve().repeated ? f : e[p].map ? c : d).push(e[p]);if (f.length && (s.arrays || s.defaults)) for (p = 0; p < f.length; ++p) l[f[p].name] = [];if (c.length && (s.objects || s.defaults)) for (p = 0; p < c.length; ++p) l[c[p].name] = {};if (d.length && s.defaults) for (p = 0; p < d.length; ++p) if (h = (u = d[p]).name, u.resolvedType instanceof i) l[h] = s.enums = String ? u.resolvedType.valuesById[u.typeDefault] : u.typeDefault;else if (u.long) {if (n.Long) {var y = new n.Long(u.typeDefault.low, u.typeDefault.high, u.typeDefault.unsigned);l[h] = s.longs === String ? y.toString() : s.longs === Number ? y.toNumber() : y;} else l[h] = s.longs === String ? u.typeDefault.toString() : u.typeDefault.toNumber();} else u.bytes ? l[h] = s.bytes === String ? String.fromCharCode.apply(String, u.typeDefault) : Array.prototype.slice.call(u.typeDefault).join("*..*").split("*..*") : l[h] = u.typeDefault;var m = !1;for (p = 0; p < e.length; ++p) {h = (u = e[p]).name;var v,g,b = t._fieldsArray.indexOf(u);if (u.map) {if (m || (m = !0), o[h] && (v = Object.keys(o[h]).length)) for (l[h] = {}, g = 0; g < v.length; ++g) a(u, b, h, n.merge(n.copy(r), { m: o, d: l, ksi: v[g], o: s }));} else if (u.repeated) {if (o[h] && o[h].length) for (l[h] = [], g = 0; g < o[h].length; ++g) a(u, b, h, n.merge(n.copy(r), { m: o, d: l, ksi: g, o: s }));} else null != o[h] && o.hasOwnProperty(h) && a(u, b, h, n.merge(n.copy(r), { m: o, d: l, o: s })), u.partOf && s.oneofs && (l[u.partOf.name] = h);}return l;} : function () {return {};};};};}, { 31: 31, 8: 8 }], 26: [function (t, e, r) {"use strict";e.exports = a;var i,n,o,s = t(16);function a(t, e) {s.call(this, t, e), this.methods = {}, this._methodsArray = null;}function u(t) {return t._methodsArray = null, t;}((a.prototype = Object.create(s.prototype)).constructor = a).className = "Service", a.fromJSON = function (t, e) {var r = new a(t, e.options);if (e.methods) for (var n = Object.keys(e.methods), o = 0; o < n.length; ++o) r.add(i.fromJSON(n[o], e.methods[n[o]]));return e.nested && r.addJSON(e.nested), r.comment = e.comment, r;}, a.prototype.toJSON = function (t) {var e = s.prototype.toJSON.call(this, t),r = !!t && Boolean(t.keepComments);return n.toObject(["options", e && e.options || void 0, "methods", s.arrayToJSON(this.methodsArray, t) || {}, "nested", e && e.nested || void 0, "comment", r ? this.comment : void 0]);}, Object.defineProperty(a.prototype, "methodsArray", { get: function () {return this._methodsArray || (this._methodsArray = n.toArray(this.methods));} }), a.prototype.get = function (t) {return this.methods[t] || s.prototype.get.call(this, t);}, a.prototype.resolveAll = function () {for (var t = this.methodsArray, e = 0; e < t.length; ++e) t[e].resolve();return s.prototype.resolve.call(this);}, a.prototype.add = function (t) {if (this.get(t.name)) throw Error("duplicate name '" + t.name + "' in " + this);return t instanceof i ? (this.methods[t.name] = t, t.parent = this, u(this)) : s.prototype.add.call(this, t);}, a.prototype.remove = function (t) {if (t instanceof i) {if (this.methods[t.name] !== t) throw Error(t + " is not a member of " + this);return delete this.methods[t.name], t.parent = null, u(this);}return s.prototype.remove.call(this, t);}, a.prototype.create = function (t, e, r) {for (var i, s = new o.Service(t, e, r), a = 0; a < this.methodsArray.length; ++a) {var u = n.lcFirst((i = this._methodsArray[a]).resolve().name).replace(/[^$\w_]/g, "");s[u] = n.codegen(["r", "c"], n.isReserved(u) ? u + "_" : u)("return this.rpcCall(m,q,s,r,c)")({ m: i, q: i.resolvedRequestType.ctor, s: i.resolvedResponseType.ctor });}return s;}, a._configure = function () {i = t(15), n = t(31), o = t(25);};}, { 15: 15, 16: 16, 25: 25, 31: 31 }], 34: [function (t, e, r) {"use strict";e.exports = h;var i,n = t(31),o = t(30);function s(t, e, r) {this.fn = t, this.len = e, this.next = void 0, this.val = r;}function a() {}function u(t) {this.head = t.head, this.tail = t.tail, this.len = t.len, this.next = t.states;}function h() {this.len = 0, this.head = new s(a, 0, 0), this.tail = this.head, this.states = null;}function l(t, e, r) {e[r] = 255 & t;}function f(t, e) {this.len = t, this.next = void 0, this.val = e;}function c(t, e, r) {for (; t.hi;) e[r++] = 127 & t.lo | 128, t.lo = (t.lo >>> 7 | t.hi << 25) >>> 0, t.hi >>>= 7;for (; t.lo > 127;) e[r++] = 127 & t.lo | 128, t.lo = t.lo >>> 7;e[r++] = t.lo;}function d(t, e, r) {e[r] = 255 & t, e[r + 1] = t >>> 8 & 255, e[r + 2] = t >>> 16 & 255, e[r + 3] = t >>> 24;}h.create = n.Buffer ? function () {return (h.create = function () {return new (void 0)();})();} : function () {return new h();}, h.alloc = function (t) {return new n.Array(t);}, n.Array !== Array && (h.alloc = n.pool(h.alloc, n.Array.prototype.subarray)), h.prototype._push = function (t, e, r) {return this.tail = this.tail.next = new s(t, e, r), this.len += e, this;}, f.prototype = Object.create(s.prototype), f.prototype.fn = function (t, e, r) {for (; t > 127;) e[r++] = 127 & t | 128, t >>>= 7;e[r] = t;}, h.prototype.uint32 = function (t) {return this.len += (this.tail = this.tail.next = new f((t >>>= 0) < 128 ? 1 : t < 16384 ? 2 : t < 2097152 ? 3 : t < 268435456 ? 4 : 5, t)).len, this;}, h.prototype.int32 = function (t) {return t < 0 ? this._push(c, 10, i.fromNumber(t)) : this.uint32(t);}, h.prototype.sint32 = function (t) {return this.uint32((t << 1 ^ t >> 31) >>> 0);}, h.prototype.uint64 = function (t) {var e = i.from(t);return this._push(c, e.length(), e);}, h.prototype.int64 = h.prototype.uint64, h.prototype.sint64 = function (t) {var e = i.from(t).zzEncode();return this._push(c, e.length(), e);}, h.prototype.bool = function (t) {return this._push(l, 1, t ? 1 : 0);}, h.prototype.fixed32 = function (t) {return this._push(d, 4, t >>> 0);}, h.prototype.sfixed32 = h.prototype.fixed32, h.prototype.fixed64 = function (t) {var e = i.from(t);return this._push(d, 4, e.lo)._push(d, 4, e.hi);}, h.prototype.sfixed64 = h.prototype.fixed64, h.prototype.float = function (t) {return this._push(n.float.writeFloatLE, 4, t);}, h.prototype.double = function (t) {return this._push(n.float.writeDoubleLE, 8, t);};var p = n.Array.prototype.set ? function (t, e, r) {e.set(t, r);} : function (t, e, r) {for (var i = 0; i < t.length; ++i) e[r + i] = t[i];};h.prototype.bytes = function (t) {var e = t.length >>> 0;if (!e) return this._push(l, 1, 0);if (n.isString(t)) {var r = h.alloc(e = o.length(t));o.write(t, r, 0), t = r;}return this.uint32(e)._push(p, e, t);}, h.prototype.string = function (t) {var e = o.length(t);return e ? this.uint32(e)._push(o.write, e, t) : this._push(l, 1, 0);}, h.prototype.fork = function () {return this.states = new u(this), this.head = this.tail = new s(a, 0, 0), this.len = 0, this;}, h.prototype.reset = function () {return this.states ? (this.head = this.states.head, this.tail = this.states.tail, this.len = this.states.len, this.states = this.states.next) : (this.head = this.tail = new s(a, 0, 0), this.len = 0), this;}, h.prototype.ldelim = function () {var t = this.head,e = this.tail,r = this.len;return this.reset().uint32(r), r && (this.tail.next = t.next, this.tail = e, this.len += r), this;}, h.prototype.finish = function () {for (var t = this.head.next, e = this.constructor.alloc(this.len), r = 0; t;) t.fn(t.val, e, r), r += t.len, t = t.next;return e;}, h._configure = function () {i = t(12), t(4), o = t(30);};}, { 12: 12, 30: 30, 31: 31, 4: 4 }], 31: [function (t, e, r) {"use strict";var i = e.exports,n = t(24);i.LongBits = t(12), i.Long = t(11), i.pool = t(21), i.float = t(10), i.asPromise = t(3), i.EventEmitter = t(2), i.path = t(20), i.base64 = t(4), i.utf8 = t(30), i.compareFieldsById = function (t, e) {return t.id - e.id;}, i.toArray = function (t) {if (t) {for (var e = Object.keys(t), r = new Array(e.length), i = 0; i < e.length;) r[i] = t[e[i++]];return r;}return [];}, i.toObject = function (t) {for (var e = {}, r = 0; r < t.length;) {var i = t[r++],n = t[r++];void 0 !== n && (e[i] = n);}return e;}, i.isString = function (t) {return "string" == typeof t || t instanceof String;}, i.isReserved = function (t) {return /^(?:do|if|in|for|let|new|try|var|case|else|enum|eval|false|null|this|true|void|with|break|catch|class|const|super|throw|while|yield|delete|export|import|public|return|static|switch|typeof|default|extends|finally|package|private|continue|debugger|function|arguments|interface|protected|implements|instanceof)$/.test(t);}, i.isObject = function (t) {return t && "object" == typeof t;}, i.Array = "undefined" != typeof Uint8Array ? Uint8Array : Array, i.oneOfGetter = function (t) {for (var e = {}, r = 0; r < t.length; ++r) e[t[r]] = 1;return function () {for (var t = Object.keys(this), r = t.length - 1; r > -1; --r) if (1 === e[t[r]] && void 0 !== this[t[r]] && null !== this[t[r]]) return t[r];};}, i.oneOfSetter = function (t) {return function (e) {for (var r = 0; r < t.length; ++r) t[r] !== e && delete this[t[r]];};}, i.merge = function (t, e, r) {for (var i = Object.keys(e), n = 0; n < i.length; ++n) void 0 !== t[i[n]] && r || (t[i[n]] = e[i[n]]);return t;}, i.decorateType = function (e, r) {if (e.$type) return r && e.$type.name !== r && (i.decorateRoot.remove(e.$type), e.$type.name = r, i.decorateRoot.add(e.$type)), e.$type;Type || (Type = t(28));var n = new Type(r || e.name);return i.decorateRoot.add(n), n.ctor = e, Object.defineProperty(e, "$type", { value: n, enumerable: !1 }), Object.defineProperty(e.prototype, "$type", { value: n, enumerable: !1 }), n;}, i.emptyArray = Object.freeze ? Object.freeze([]) : [], i.emptyObject = Object.freeze ? Object.freeze({}) : {}, i.longToHash = function (t) {return t ? i.LongBits.from(t).toHash() : i.LongBits.zeroHash;}, i.copy = function (t) {if ("object" != typeof t) return t;var e = {};for (var r in t) e[r] = t[r];return e;}, i.deepCopy = function t(e) {if ("object" != typeof e) return e;var r = {};for (var i in e) r[i] = t(e[i]);return r;}, i.ProtocolError = function (t) {function e(t, r) {if (!(this instanceof e)) return new e(t, r);Object.defineProperty(this, "message", { get: function () {return t;} }), Error.captureStackTrace ? Error.captureStackTrace(this, e) : Object.defineProperty(this, "stack", { value: new Error().stack || "" }), r && merge(this, r);}return (e.prototype = Object.create(Error.prototype)).constructor = e, Object.defineProperty(e.prototype, "name", { get: function () {return t;} }), e.prototype.toString = function () {return this.name + ": " + this.message;}, e;}, i.toJSONOptions = { longs: String, enums: String, bytes: String, json: !0 }, i.Buffer = null, i.newBuffer = function (t) {return "number" == typeof t ? new i.Array(t) : "undefined" == typeof Uint8Array ? t : new Uint8Array(t);}, i.stringToBytes = function (t) {var e,r,i = [];e = t.length;for (var n = 0; n < e; n++) (r = t.charCodeAt(n)) >= 65536 && r <= 1114111 ? (i.push(r >> 18 & 7 | 240), i.push(r >> 12 & 63 | 128), i.push(r >> 6 & 63 | 128), i.push(63 & r | 128)) : r >= 2048 && r <= 65535 ? (i.push(r >> 12 & 15 | 224), i.push(r >> 6 & 63 | 128), i.push(63 & r | 128)) : r >= 128 && r <= 2047 ? (i.push(r >> 6 & 31 | 192), i.push(63 & r | 128)) : i.push(255 & r);return i;}, i.byteToString = function (t) {if ("string" == typeof t) return t;for (var e = "", r = t, i = 0; i < r.length; i++) {var n = r[i].toString(2),o = n.match(/^1+?(?=0)/);if (o && 8 == n.length) {for (var s = o[0].length, a = r[i].toString(2).slice(7 - s), u = 1; u < s; u++) a += r[u + i].toString(2).slice(2);e += String.fromCharCode(parseInt(a, 2)), i += s - 1;} else e += String.fromCharCode(r[i]);}return e;}, i.isInteger = Number.isInteger || function (t) {return "number" == typeof t && isFinite(t) && Math.floor(t) === t;}, Object.defineProperty(i, "decorateRoot", { get: function () {return n.decorated || (n.decorated = new (t(23))());} });}, { 10: 10, 11: 11, 12: 12, 2: 2, 20: 20, 21: 21, 23: 23, 24: 24, 28: 28, 3: 3, 30: 30, 4: 4 }], 25: [function (t, e, r) {"use strict";e.exports = n;var i = t(31);function n(t, e, r) {if ("function" != typeof t) throw TypeError("rpcImpl must be a function");i.EventEmitter.call(this), this.rpcImpl = t, this.requestDelimited = Boolean(e), this.responseDelimited = Boolean(r);}(n.prototype = Object.create(i.EventEmitter.prototype)).constructor = n, n.prototype.rpcCall = function t(e, r, n, o, s) {if (!o) throw TypeError("request must be specified");var a = this;if (!s) return i.asPromise(t, a, e, r, n, o);if (a.rpcImpl) try {return a.rpcImpl(e, r[a.requestDelimited ? "encodeDelimited" : "encode"](o).finish(), function (t, r) {if (t) return a.emit("error", t, e), s(t);if (null !== r) {if (!(r instanceof n)) try {r = n[a.responseDelimited ? "decodeDelimited" : "decode"](r);} catch (t) {return a.emit("error", t, e), s(t);}return a.emit("data", r, e), s(null, r);}a.end(!0);});} catch (u) {return a.emit("error", u, e), void setTimeout(function () {s(u);}, 0);} else setTimeout(function () {s(Error("already ended"));}, 0);}, n.prototype.end = function (t) {return this.rpcImpl && (t || this.rpcImpl(null, null, null), this.rpcImpl = null, this.emit("end").off()), this;};}, { 31: 31 }], 2: [function (t, e, r) {"use strict";function i() {this._listeners = {};}e.exports = i, i.prototype.on = function (t, e, r) {return (this._listeners[t] || (this._listeners[t] = [])).push({ fn: e, ctx: r || this }), this;}, i.prototype.off = function (t, e) {if (void 0 === t) this._listeners = {};else if (void 0 === e) this._listeners[t] = [];else for (var r = this._listeners[t], i = 0; i < r.length;) r[i].fn === e ? r.splice(i, 1) : ++i;return this;}, i.prototype.emit = function (t) {var e = this._listeners[t];if (e) {for (var r = [], i = 1; i < arguments.length;) r.push(arguments[i++]);for (i = 0; i < e.length;) e[i].fn.apply(e[i++].ctx, r);}return this;};}, {}], 3: [function (t, e, r) {"use strict";e.exports = function (t, e) {for (var r = new Array(arguments.length - 1), i = 0, n = 2, o = !0; n < arguments.length;) r[i++] = arguments[n++];return new Promise(function (n, s) {r[i] = function (t) {if (o) if (o = !1, t) s(t);else {for (var e = new Array(arguments.length - 1), r = 0; r < e.length;) e[r++] = arguments[r];n.apply(null, e);}};try {t.apply(e || null, r);} catch (a) {o && (o = !1, s(a));}});};}, {}], 4: [function (t, e, r) {"use strict";var i = e.exports;i.length = function (t) {var e = t.length;if (!e) return 0;for (var r = 0; --e % 4 > 1 && "=" === t.charAt(e);) ++r;return Math.ceil(3 * t.length) / 4 - r;};for (var n = new Array(64), o = new Array(123), s = 0; s < 64;) o[n[s] = s < 26 ? s + 65 : s < 52 ? s + 71 : s < 62 ? s - 4 : s - 59 | 43] = s++;i.encode = function (t, e, r) {for (var i, o = null, s = [], a = 0, u = 0; e < r;) {var h = t[e++];switch (u) {case 0:s[a++] = n[h >> 2], i = (3 & h) << 4, u = 1;break;case 1:s[a++] = n[i | h >> 4], i = (15 & h) << 2, u = 2;break;case 2:s[a++] = n[i | h >> 6], s[a++] = n[63 & h], u = 0;}a > 8191 && ((o || (o = [])).push(String.fromCharCode.apply(String, s)), a = 0);}return u && (s[a++] = n[i], s[a++] = 61, 1 === u && (s[a++] = 61)), o ? (a && o.push(String.fromCharCode.apply(String, s.slice(0, a))), o.join("")) : String.fromCharCode.apply(String, s.slice(0, a));}, i.decode = function (t, e, r) {for (var i, n = r, s = 0, a = 0; a < t.length;) {var u = t.charCodeAt(a++);if (61 === u && s > 1) break;if (void 0 === (u = o[u])) throw Error("invalid encoding");switch (s) {case 0:i = u, s = 1;break;case 1:e[r++] = i << 2 | (48 & u) >> 4, i = u, s = 2;break;case 2:e[r++] = (15 & i) << 4 | (60 & u) >> 2, i = u, s = 3;break;case 3:e[r++] = (3 & i) << 6 | u, s = 0;}}if (1 === s) throw Error("invalid encoding");return r - n;}, i.test = function (t) {return /^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==|[A-Za-z0-9+/]{3}=)?$/.test(t);};}, {}], 10: [function (t, e, r) {"use strict";function i(t) {return "undefined" != typeof Float32Array ? function () {var e = new Float32Array([-0]),r = new Uint8Array(e.buffer),i = 128 === r[3];function n(t, i, n) {e[0] = t, i[n] = r[0], i[n + 1] = r[1], i[n + 2] = r[2], i[n + 3] = r[3];}function o(t, i, n) {e[0] = t, i[n] = r[3], i[n + 1] = r[2], i[n + 2] = r[1], i[n + 3] = r[0];}function s(t, i) {return r[0] = t[i], r[1] = t[i + 1], r[2] = t[i + 2], r[3] = t[i + 3], e[0];}function a(t, i) {return r[3] = t[i], r[2] = t[i + 1], r[1] = t[i + 2], r[0] = t[i + 3], e[0];}t.writeFloatLE = i ? n : o, t.writeFloatBE = i ? o : n, t.readFloatLE = i ? s : a, t.readFloatBE = i ? a : s;}() : function () {function e(t, e, r, i) {var n = e < 0 ? 1 : 0;if (n && (e = -e), 0 === e) t(1 / e > 0 ? 0 : 2147483648, r, i);else if (isNaN(e)) t(2143289344, r, i);else if (e > 34028234663852886e22) t((n << 31 | 2139095040) >>> 0, r, i);else if (e < 11754943508222875e-54) t((n << 31 | Math.round(e / 1401298464324817e-60)) >>> 0, r, i);else {var o = Math.floor(Math.log(e) / Math.LN2);t((n << 31 | o + 127 << 23 | 8388607 & Math.round(e * Math.pow(2, -o) * 8388608)) >>> 0, r, i);}}function r(t, e, r) {var i = t(e, r),n = 2 * (i >> 31) + 1,o = i >>> 23 & 255,s = 8388607 & i;return 255 === o ? s ? NaN : n * (1 / 0) : 0 === o ? 1401298464324817e-60 * n * s : n * Math.pow(2, o - 150) * (s + 8388608);}t.writeFloatLE = e.bind(null, n), t.writeFloatBE = e.bind(null, o), t.readFloatLE = r.bind(null, s), t.readFloatBE = r.bind(null, a);}(), "undefined" != typeof Float64Array ? function () {var e = new Float64Array([-0]),r = new Uint8Array(e.buffer),i = 128 === r[7];function n(t, i, n) {e[0] = t, i[n] = r[0], i[n + 1] = r[1], i[n + 2] = r[2], i[n + 3] = r[3], i[n + 4] = r[4], i[n + 5] = r[5], i[n + 6] = r[6], i[n + 7] = r[7];}function o(t, i, n) {e[0] = t, i[n] = r[7], i[n + 1] = r[6], i[n + 2] = r[5], i[n + 3] = r[4], i[n + 4] = r[3], i[n + 5] = r[2], i[n + 6] = r[1], i[n + 7] = r[0];}function s(t, i) {return r[0] = t[i], r[1] = t[i + 1], r[2] = t[i + 2], r[3] = t[i + 3], r[4] = t[i + 4], r[5] = t[i + 5], r[6] = t[i + 6], r[7] = t[i + 7], e[0];}function a(t, i) {return r[7] = t[i], r[6] = t[i + 1], r[5] = t[i + 2], r[4] = t[i + 3], r[3] = t[i + 4], r[2] = t[i + 5], r[1] = t[i + 6], r[0] = t[i + 7], e[0];}t.writeDoubleLE = i ? n : o, t.writeDoubleBE = i ? o : n, t.readDoubleLE = i ? s : a, t.readDoubleBE = i ? a : s;}() : function () {function e(t, e, r, i, n, o) {var s = i < 0 ? 1 : 0;if (s && (i = -i), 0 === i) t(0, n, o + e), t(1 / i > 0 ? 0 : 2147483648, n, o + r);else if (isNaN(i)) t(0, n, o + e), t(2146959360, n, o + r);else if (i > 17976931348623157e292) t(0, n, o + e), t((s << 31 | 2146435072) >>> 0, n, o + r);else {var a;if (i < 22250738585072014e-324) t((a = i / 5e-324) >>> 0, n, o + e), t((s << 31 | a / 4294967296) >>> 0, n, o + r);else {var u = Math.floor(Math.log(i) / Math.LN2);1024 === u && (u = 1023), t(4503599627370496 * (a = i * Math.pow(2, -u)) >>> 0, n, o + e), t((s << 31 | u + 1023 << 20 | 1048576 * a & 1048575) >>> 0, n, o + r);}}}function r(t, e, r, i, n) {var o = t(i, n + e),s = t(i, n + r),a = 2 * (s >> 31) + 1,u = s >>> 20 & 2047,h = 4294967296 * (1048575 & s) + o;return 2047 === u ? h ? NaN : a * (1 / 0) : 0 === u ? 5e-324 * a * h : a * Math.pow(2, u - 1075) * (h + 4503599627370496);}t.writeDoubleLE = e.bind(null, n, 0, 4), t.writeDoubleBE = e.bind(null, o, 4, 0), t.readDoubleLE = r.bind(null, s, 0, 4), t.readDoubleBE = r.bind(null, a, 4, 0);}(), t;}function n(t, e, r) {e[r] = 255 & t, e[r + 1] = t >>> 8 & 255, e[r + 2] = t >>> 16 & 255, e[r + 3] = t >>> 24;}function o(t, e, r) {e[r] = t >>> 24, e[r + 1] = t >>> 16 & 255, e[r + 2] = t >>> 8 & 255, e[r + 3] = 255 & t;}function s(t, e) {return (t[e] | t[e + 1] << 8 | t[e + 2] << 16 | t[e + 3] << 24) >>> 0;}function a(t, e) {return (t[e] << 24 | t[e + 1] << 16 | t[e + 2] << 8 | t[e + 3]) >>> 0;}e.exports = i(i);}, {}], 11: [function (t, e, r) {"use strict";e.exports = n;var i = null;try {i = new WebAssembly.Instance(new WebAssembly.Module(new Uint8Array([0, 97, 115, 109, 1, 0, 0, 0, 1, 13, 2, 96, 0, 1, 127, 96, 4, 127, 127, 127, 127, 1, 127, 3, 7, 6, 0, 1, 1, 1, 1, 1, 6, 6, 1, 127, 1, 65, 0, 11, 7, 50, 6, 3, 109, 117, 108, 0, 1, 5, 100, 105, 118, 95, 115, 0, 2, 5, 100, 105, 118, 95, 117, 0, 3, 5, 114, 101, 109, 95, 115, 0, 4, 5, 114, 101, 109, 95, 117, 0, 5, 8, 103, 101, 116, 95, 104, 105, 103, 104, 0, 0, 10, 191, 1, 6, 4, 0, 35, 0, 11, 36, 1, 1, 126, 32, 0, 173, 32, 1, 173, 66, 32, 134, 132, 32, 2, 173, 32, 3, 173, 66, 32, 134, 132, 126, 34, 4, 66, 32, 135, 167, 36, 0, 32, 4, 167, 11, 36, 1, 1, 126, 32, 0, 173, 32, 1, 173, 66, 32, 134, 132, 32, 2, 173, 32, 3, 173, 66, 32, 134, 132, 127, 34, 4, 66, 32, 135, 167, 36, 0, 32, 4, 167, 11, 36, 1, 1, 126, 32, 0, 173, 32, 1, 173, 66, 32, 134, 132, 32, 2, 173, 32, 3, 173, 66, 32, 134, 132, 128, 34, 4, 66, 32, 135, 167, 36, 0, 32, 4, 167, 11, 36, 1, 1, 126, 32, 0, 173, 32, 1, 173, 66, 32, 134, 132, 32, 2, 173, 32, 3, 173, 66, 32, 134, 132, 129, 34, 4, 66, 32, 135, 167, 36, 0, 32, 4, 167, 11, 36, 1, 1, 126, 32, 0, 173, 32, 1, 173, 66, 32, 134, 132, 32, 2, 173, 32, 3, 173, 66, 32, 134, 132, 130, 34, 4, 66, 32, 135, 167, 36, 0, 32, 4, 167, 11])), {}).exports;} catch (E) {}function n(t, e, r) {this.low = 0 | t, this.high = 0 | e, this.unsigned = !!r;}function o(t) {return !0 === (t && t.__isLong__);}n.prototype.__isLong__, Object.defineProperty(n.prototype, "__isLong__", { value: !0 }), n.isLong = o;var s = {},a = {};function u(t, e) {var r, i, n;return e ? (n = 0 <= (t >>>= 0) && t < 256) && (i = a[t]) ? i : (r = l(t, (0 | t) < 0 ? -1 : 0, !0), n && (a[t] = r), r) : (n = -128 <= (t |= 0) && t < 128) && (i = s[t]) ? i : (r = l(t, t < 0 ? -1 : 0, !1), n && (s[t] = r), r);}function h(t, e) {if (isNaN(t)) return e ? b : g;if (e) {if (t < 0) return b;if (t >= y) return A;} else {if (t <= -m) return O;if (t + 1 >= m) return k;}return t < 0 ? h(-t, e).neg() : l(t % p | 0, t / p | 0, e);}function l(t, e, r) {return new n(t, e, r);}n.fromInt = u, n.fromNumber = h, n.fromBits = l;var f = Math.pow;function c(t, e, r) {if (0 === t.length) throw Error("empty string");if ("NaN" === t || "Infinity" === t || "+Infinity" === t || "-Infinity" === t) return g;if ("number" == typeof e ? (r = e, e = !1) : e = !!e, (r = r || 10) < 2 || 36 < r) throw RangeError("radix");var i;if ((i = t.indexOf("-")) > 0) throw Error("interior hyphen");if (0 === i) return c(t.substring(1), e, r).neg();for (var n = h(f(r, 8)), o = g, s = 0; s < t.length; s += 8) {var a = Math.min(8, t.length - s),u = parseInt(t.substring(s, s + a), r);if (a < 8) {var l = h(f(r, a));o = o.mul(l).add(h(u));} else o = (o = o.mul(n)).add(h(u));}return o.unsigned = e, o;}function d(t, e) {return "number" == typeof t ? h(t, e) : "string" == typeof t ? c(t, e) : l(t.low, t.high, "boolean" == typeof e ? e : t.unsigned);}n.fromString = c, n.fromValue = d;var p = 4294967296,y = p * p,m = y / 2,v = u(1 << 24),g = u(0);n.ZERO = g;var b = u(0, !0);n.UZERO = b;var w = u(1);n.ONE = w;var _ = u(1, !0);n.UONE = _;var x = u(-1);n.NEG_ONE = x;var k = l(-1, 2147483647, !1);n.MAX_VALUE = k;var A = l(-1, -1, !0);n.MAX_UNSIGNED_VALUE = A;var O = l(0, -2147483648, !1);n.MIN_VALUE = O;var S = n.prototype;S.toInt = function () {return this.unsigned ? this.low >>> 0 : this.low;}, S.toNumber = function () {return this.unsigned ? (this.high >>> 0) * p + (this.low >>> 0) : this.high * p + (this.low >>> 0);}, S.toString = function (t) {if ((t = t || 10) < 2 || 36 < t) throw RangeError("radix");if (this.isZero()) return "0";if (this.isNegative()) {if (this.eq(O)) {var e = h(t),r = this.div(e),i = r.mul(e).sub(this);return r.toString(t) + i.toInt().toString(t);}return "-" + this.neg().toString(t);}for (var n = h(f(t, 6), this.unsigned), o = this, s = "";;) {var a = o.div(n),u = (o.sub(a.mul(n)).toInt() >>> 0).toString(t);if ((o = a).isZero()) return u + s;for (; u.length < 6;) u = "0" + u;s = "" + u + s;}}, S.getHighBits = function () {return this.high;}, S.getHighBitsUnsigned = function () {return this.high >>> 0;}, S.getLowBits = function () {return this.low;}, S.getLowBitsUnsigned = function () {return this.low >>> 0;}, S.getNumBitsAbs = function () {if (this.isNegative()) return this.eq(O) ? 64 : this.neg().getNumBitsAbs();for (var t = 0 != this.high ? this.high : this.low, e = 31; e > 0 && 0 == (t & 1 << e); e--);return 0 != this.high ? e + 33 : e + 1;}, S.isZero = function () {return 0 === this.high && 0 === this.low;}, S.eqz = S.isZero, S.isNegative = function () {return !this.unsigned && this.high < 0;}, S.isPositive = function () {return this.unsigned || this.high >= 0;}, S.isOdd = function () {return 1 == (1 & this.low);}, S.isEven = function () {return 0 == (1 & this.low);}, S.equals = function (t) {return o(t) || (t = d(t)), (this.unsigned === t.unsigned || this.high >>> 31 != 1 || t.high >>> 31 != 1) && this.high === t.high && this.low === t.low;}, S.eq = S.equals, S.notEquals = function (t) {return !this.eq(t);}, S.neq = S.notEquals, S.ne = S.notEquals, S.lessThan = function (t) {return this.comp(t) < 0;}, S.lt = S.lessThan, S.lessThanOrEqual = function (t) {return this.comp(t) <= 0;}, S.lte = S.lessThanOrEqual, S.le = S.lessThanOrEqual, S.greaterThan = function (t) {return this.comp(t) > 0;}, S.gt = S.greaterThan, S.greaterThanOrEqual = function (t) {return this.comp(t) >= 0;}, S.gte = S.greaterThanOrEqual, S.ge = S.greaterThanOrEqual, S.compare = function (t) {if (o(t) || (t = d(t)), this.eq(t)) return 0;var e = this.isNegative(),r = t.isNegative();return e && !r ? -1 : !e && r ? 1 : this.unsigned ? t.high >>> 0 > this.high >>> 0 || t.high === this.high && t.low >>> 0 > this.low >>> 0 ? -1 : 1 : this.sub(t).isNegative() ? -1 : 1;}, S.comp = S.compare, S.negate = function () {return !this.unsigned && this.eq(O) ? O : this.not().add(w);}, S.neg = S.negate, S.add = function (t) {o(t) || (t = d(t));var e = this.high >>> 16,r = 65535 & this.high,i = this.low >>> 16,n = 65535 & this.low,s = t.high >>> 16,a = 65535 & t.high,u = t.low >>> 16,h = 0,f = 0,c = 0,p = 0;return c += (p += n + (65535 & t.low)) >>> 16, f += (c += i + u) >>> 16, h += (f += r + a) >>> 16, h += e + s, l((c &= 65535) << 16 | (p &= 65535), (h &= 65535) << 16 | (f &= 65535), this.unsigned);}, S.subtract = function (t) {return o(t) || (t = d(t)), this.add(t.neg());}, S.sub = S.subtract, S.multiply = function (t) {if (this.isZero()) return g;if (o(t) || (t = d(t)), i) return l(i.mul(this.low, this.high, t.low, t.high), i.get_high(), this.unsigned);if (t.isZero()) return g;if (this.eq(O)) return t.isOdd() ? O : g;if (t.eq(O)) return this.isOdd() ? O : g;if (this.isNegative()) return t.isNegative() ? this.neg().mul(t.neg()) : this.neg().mul(t).neg();if (t.isNegative()) return this.mul(t.neg()).neg();if (this.lt(v) && t.lt(v)) return h(this.toNumber() * t.toNumber(), this.unsigned);var e = this.high >>> 16,r = 65535 & this.high,n = this.low >>> 16,s = 65535 & this.low,a = t.high >>> 16,u = 65535 & t.high,f = t.low >>> 16,c = 65535 & t.low,p = 0,y = 0,m = 0,b = 0;return m += (b += s * c) >>> 16, y += (m += n * c) >>> 16, m &= 65535, y += (m += s * f) >>> 16, p += (y += r * c) >>> 16, y &= 65535, p += (y += n * f) >>> 16, y &= 65535, p += (y += s * u) >>> 16, p += e * c + r * f + n * u + s * a, l((m &= 65535) << 16 | (b &= 65535), (p &= 65535) << 16 | (y &= 65535), this.unsigned);}, S.mul = S.multiply, S.divide = function (t) {if (o(t) || (t = d(t)), t.isZero()) throw Error("division by zero");var e, r, n;if (i) return this.unsigned || -2147483648 !== this.high || -1 !== t.low || -1 !== t.high ? l((this.unsigned ? i.div_u : i.div_s)(this.low, this.high, t.low, t.high), i.get_high(), this.unsigned) : this;if (this.isZero()) return this.unsigned ? b : g;if (this.unsigned) {if (t.unsigned || (t = t.toUnsigned()), t.gt(this)) return b;if (t.gt(this.shru(1))) return _;n = b;} else {if (this.eq(O)) return t.eq(w) || t.eq(x) ? O : t.eq(O) ? w : (e = this.shr(1).div(t).shl(1)).eq(g) ? t.isNegative() ? w : x : (r = this.sub(t.mul(e)), n = e.add(r.div(t)));if (t.eq(O)) return this.unsigned ? b : g;if (this.isNegative()) return t.isNegative() ? this.neg().div(t.neg()) : this.neg().div(t).neg();if (t.isNegative()) return this.div(t.neg()).neg();n = g;}for (r = this; r.gte(t);) {e = Math.max(1, Math.floor(r.toNumber() / t.toNumber()));for (var s = Math.ceil(Math.log(e) / Math.LN2), a = s <= 48 ? 1 : f(2, s - 48), u = h(e), c = u.mul(t); c.isNegative() || c.gt(r);) c = (u = h(e -= a, this.unsigned)).mul(t);u.isZero() && (u = w), n = n.add(u), r = r.sub(c);}return n;}, S.div = S.divide, S.modulo = function (t) {return o(t) || (t = d(t)), i ? l((this.unsigned ? i.rem_u : i.rem_s)(this.low, this.high, t.low, t.high), i.get_high(), this.unsigned) : this.sub(this.div(t).mul(t));}, S.mod = S.modulo, S.rem = S.modulo, S.not = function () {return l(~this.low, ~this.high, this.unsigned);}, S.and = function (t) {return o(t) || (t = d(t)), l(this.low & t.low, this.high & t.high, this.unsigned);}, S.or = function (t) {return o(t) || (t = d(t)), l(this.low | t.low, this.high | t.high, this.unsigned);}, S.xor = function (t) {return o(t) || (t = d(t)), l(this.low ^ t.low, this.high ^ t.high, this.unsigned);}, S.shiftLeft = function (t) {return o(t) && (t = t.toInt()), 0 == (t &= 63) ? this : t < 32 ? l(this.low << t, this.high << t | this.low >>> 32 - t, this.unsigned) : l(0, this.low << t - 32, this.unsigned);}, S.shl = S.shiftLeft, S.shiftRight = function (t) {return o(t) && (t = t.toInt()), 0 == (t &= 63) ? this : t < 32 ? l(this.low >>> t | this.high << 32 - t, this.high >> t, this.unsigned) : l(this.high >> t - 32, this.high >= 0 ? 0 : -1, this.unsigned);}, S.shr = S.shiftRight, S.shiftRightUnsigned = function (t) {if (o(t) && (t = t.toInt()), 0 == (t &= 63)) return this;var e = this.high;return t < 32 ? l(this.low >>> t | e << 32 - t, e >>> t, this.unsigned) : l(32 === t ? e : e >>> t - 32, 0, this.unsigned);}, S.shru = S.shiftRightUnsigned, S.shr_u = S.shiftRightUnsigned, S.toSigned = function () {return this.unsigned ? l(this.low, this.high, !1) : this;}, S.toUnsigned = function () {return this.unsigned ? this : l(this.low, this.high, !0);}, S.toBytes = function (t) {return t ? this.toBytesLE() : this.toBytesBE();}, S.toBytesLE = function () {var t = this.high,e = this.low;return [255 & e, e >>> 8 & 255, e >>> 16 & 255, e >>> 24, 255 & t, t >>> 8 & 255, t >>> 16 & 255, t >>> 24];}, S.toBytesBE = function () {var t = this.high,e = this.low;return [t >>> 24, t >>> 16 & 255, t >>> 8 & 255, 255 & t, e >>> 24, e >>> 16 & 255, e >>> 8 & 255, 255 & e];}, n.fromBytes = function (t, e, r) {return r ? n.fromBytesLE(t, e) : n.fromBytesBE(t, e);}, n.fromBytesLE = function (t, e) {return new n(t[0] | t[1] << 8 | t[2] << 16 | t[3] << 24, t[4] | t[5] << 8 | t[6] << 16 | t[7] << 24, e);}, n.fromBytesBE = function (t, e) {return new n(t[4] << 24 | t[5] << 16 | t[6] << 8 | t[7], t[0] << 24 | t[1] << 16 | t[2] << 8 | t[3], e);};}, {}], 12: [function (t, e, r) {"use strict";function i(t, e) {this.lo = t >>> 0, this.hi = e >>> 0;}e.exports = i;var n = i.zero = new i(0, 0);n.toNumber = function () {return 0;}, n.zzEncode = n.zzDecode = function () {return this;}, n.length = function () {return 1;};var o = i.zeroHash = "\0\0\0\0\0\0\0\0";i.fromNumber = function (t) {if (0 === t) return n;var e = t < 0;e && (t = -t);var r = t >>> 0,o = (t - r) / 4294967296 >>> 0;return e && (o = ~o >>> 0, r = ~r >>> 0, ++r > 4294967295 && (r = 0, ++o > 4294967295 && (o = 0))), new i(r, o);}, i.from = function (t) {return "number" == typeof t ? i.fromNumber(t) : "string" == typeof t || t instanceof String ? i.fromNumber(parseInt(t, 10)) : t.low || t.high ? new i(t.low >>> 0, t.high >>> 0) : n;}, i.prototype.toNumber = function (t) {if (!t && this.hi >>> 31) {var e = 1 + ~this.lo >>> 0,r = ~this.hi >>> 0;return e || (r = r + 1 >>> 0), -(e + 4294967296 * r);}return this.lo + 4294967296 * this.hi;}, i.prototype.toLong = function (t) {return { low: 0 | this.lo, high: 0 | this.hi, unsigned: Boolean(t) };};var s = String.prototype.charCodeAt;i.fromHash = function (t) {return t === o ? n : new i((s.call(t, 0) | s.call(t, 1) << 8 | s.call(t, 2) << 16 | s.call(t, 3) << 24) >>> 0, (s.call(t, 4) | s.call(t, 5) << 8 | s.call(t, 6) << 16 | s.call(t, 7) << 24) >>> 0);}, i.prototype.toHash = function () {return String.fromCharCode(255 & this.lo, this.lo >>> 8 & 255, this.lo >>> 16 & 255, this.lo >>> 24, 255 & this.hi, this.hi >>> 8 & 255, this.hi >>> 16 & 255, this.hi >>> 24);}, i.prototype.zzEncode = function () {var t = this.hi >> 31;return this.hi = ((this.hi << 1 | this.lo >>> 31) ^ t) >>> 0, this.lo = (this.lo << 1 ^ t) >>> 0, this;}, i.prototype.zzDecode = function () {var t = -(1 & this.lo);return this.lo = ((this.lo >>> 1 | this.hi << 31) ^ t) >>> 0, this.hi = (this.hi >>> 1 ^ t) >>> 0, this;}, i.prototype.length = function () {var t = this.lo,e = (this.lo >>> 28 | this.hi << 4) >>> 0,r = this.hi >>> 24;return 0 === r ? 0 === e ? t < 16384 ? t < 128 ? 1 : 2 : t < 2097152 ? 3 : 4 : e < 16384 ? e < 128 ? 5 : 6 : e < 2097152 ? 7 : 8 : r < 128 ? 9 : 10;};}, {}], 20: [function (t, e, r) {"use strict";var i = e.exports,n = i.isAbsolute = function (t) {return /^(?:\/|\w+:)/.test(t);},o = i.normalize = function (t) {var e = (t = t.replace(/\\/g, "/").replace(/\/{2,}/g, "/")).split("/"),r = n(t),i = "";r && (i = e.shift() + "/");for (var o = 0; o < e.length;) ".." === e[o] ? o > 0 && ".." !== e[o - 1] ? e.splice(--o, 2) : r ? e.splice(o, 1) : ++o : "." === e[o] ? e.splice(o, 1) : ++o;return i + e.join("/");};i.resolve = function (t, e, r) {return r || (e = o(e)), n(e) ? e : (r || (t = o(t)), (t = t.replace(/(?:\/|^)[^/]+$/, "")).length ? o(t + "/" + e) : e);};}, {}], 21: [function (t, e, r) {"use strict";e.exports = function (t, e, r) {var i = r || 8192,n = i >>> 1,o = null,s = i;return function (r) {if (r < 1 || r > n) return t(r);s + r > i && (o = t(i), s = 0);var a = e.call(o, s, s += r);return 7 & s && (s = 1 + (7 | s)), a;};};}, {}], 30: [function (t, e, r) {"use strict";var i = e.exports;i.length = function (t) {for (var e = 0, r = 0, i = 0; i < t.length; ++i) (r = t.charCodeAt(i)) < 128 ? e += 1 : r < 2048 ? e += 2 : 55296 == (64512 & r) && 56320 == (64512 & t.charCodeAt(i + 1)) ? (++i, e += 4) : e += 3;return e;}, i.read = function (t, e, r) {if (r - e < 1) return "";for (var i, n = null, o = [], s = 0; e < r;) (i = t[e++]) < 128 ? o[s++] = i : i > 191 && i < 224 ? o[s++] = (31 & i) << 6 | 63 & t[e++] : i > 239 && i < 365 ? (i = ((7 & i) << 18 | (63 & t[e++]) << 12 | (63 & t[e++]) << 6 | 63 & t[e++]) - 65536, o[s++] = 55296 + (i >> 10), o[s++] = 56320 + (1023 & i)) : o[s++] = (15 & i) << 12 | (63 & t[e++]) << 6 | 63 & t[e++], s > 8191 && ((n || (n = [])).push(String.fromCharCode.apply(String, o)), s = 0);return n ? (s && n.push(String.fromCharCode.apply(String, o.slice(0, s))), n.join("")) : String.fromCharCode.apply(String, o.slice(0, s));}, i.write = function (t, e, r) {for (var i, n, o = r, s = 0; s < t.length; ++s) (i = t.charCodeAt(s)) < 128 ? e[r++] = i : i < 2048 ? (e[r++] = i >> 6 | 192, e[r++] = 63 & i | 128) : 55296 == (64512 & i) && 56320 == (64512 & (n = t.charCodeAt(s + 1))) ? (i = 65536 + ((1023 & i) << 10) + (1023 & n), ++s, e[r++] = i >> 18 | 240, e[r++] = i >> 12 & 63 | 128, e[r++] = i >> 6 & 63 | 128, e[r++] = 63 & i | 128) : (e[r++] = i >> 12 | 224, e[r++] = i >> 6 & 63 | 128, e[r++] = 63 & i | 128);return r - o;};}, {}], 35: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.getMiniBridge = void 0, r.getMiniBridge = function () {return "undefined" == typeof wx && "undefined" != typeof my ? my : wx;};}, {}], 36: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.BezierPath = void 0;var i = function (t, e, r) {this.d = t, this.transform = e, this.styles = r, this._d = t, this._transform = e, this._styles = r;};r.BezierPath = i;}, {}], 37: [function (t, e, r) {"use strict";var i,n = this && this.__extends || (i = function (t, e) {return (i = Object.setPrototypeOf || { __proto__: [] } instanceof Array && function (t, e) {t.__proto__ = e;} || function (t, e) {for (var r in e) Object.prototype.hasOwnProperty.call(e, r) && (t[r] = e[r]);})(t, e);}, function (t, e) {if ("function" != typeof e && null !== e) throw new TypeError("Class extends value " + String(e) + " is not a constructor or null");function r() {this.constructor = t;}i(t, e), t.prototype = null === e ? Object.create(e) : (r.prototype = e.prototype, new r());});Object.defineProperty(r, "__esModule", { value: !0 }), r.EllipsePath = void 0;var o = function (t) {function e(e, r, i, n, o, s) {var a = t.call(this, "", o, s) || this;return a._x = e, a._y = r, a._radiusX = i, a._radiusY = n, a._transform = o, a._styles = s, a;}return n(e, t), e;}(t(36).BezierPath);r.EllipsePath = o;}, { 36: 36 }], 38: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.FrameEntity = void 0;var i = t(36),n = function t(e) {this.alpha = 0, this.transform = { a: 1, b: 0, c: 0, d: 1, tx: 0, ty: 0 }, this.layout = { x: 0, y: 0, width: 0, height: 0 }, this.nx = 0, this.ny = 0, this.shapes = [], this.alpha = parseFloat(e.alpha) || 0, e.layout && (this.layout.x = parseFloat(e.layout.x) || 0, this.layout.y = parseFloat(e.layout.y) || 0, this.layout.width = parseFloat(e.layout.width) || 0, this.layout.height = parseFloat(e.layout.height) || 0), e.transform && (this.transform.a = parseFloat(e.transform.a) || 1, this.transform.b = parseFloat(e.transform.b) || 0, this.transform.c = parseFloat(e.transform.c) || 0, this.transform.d = parseFloat(e.transform.d) || 1, this.transform.tx = parseFloat(e.transform.tx) || 0, this.transform.ty = parseFloat(e.transform.ty) || 0), e.clipPath && e.clipPath.length > 0 && (this.maskPath = new i.BezierPath(e.clipPath, void 0, { fill: "#000000" })), e.shapes && (e.shapes instanceof Array && e.shapes.forEach(function (t) {switch (t.pathArgs = t.args, t.type) {case 0:t.type = "shape", t.pathArgs = t.shape;break;case 1:t.type = "rect", t.pathArgs = t.rect;break;case 2:t.type = "ellipse", t.pathArgs = t.ellipse;break;case 3:t.type = "keep";}if (t.styles) {t.styles.fill && ("number" == typeof t.styles.fill.r && (t.styles.fill[0] = t.styles.fill.r), "number" == typeof t.styles.fill.g && (t.styles.fill[1] = t.styles.fill.g), "number" == typeof t.styles.fill.b && (t.styles.fill[2] = t.styles.fill.b), "number" == typeof t.styles.fill.a && (t.styles.fill[3] = t.styles.fill.a)), t.styles.stroke && ("number" == typeof t.styles.stroke.r && (t.styles.stroke[0] = t.styles.stroke.r), "number" == typeof t.styles.stroke.g && (t.styles.stroke[1] = t.styles.stroke.g), "number" == typeof t.styles.stroke.b && (t.styles.stroke[2] = t.styles.stroke.b), "number" == typeof t.styles.stroke.a && (t.styles.stroke[3] = t.styles.stroke.a));var e = t.styles.lineDash || [];switch (t.styles.lineDashI > 0 && e.push(t.styles.lineDashI), t.styles.lineDashII > 0 && (e.length < 1 && e.push(0), e.push(t.styles.lineDashII), e.push(0)), t.styles.lineDashIII > 0 && (e.length < 2 && (e.push(0), e.push(0)), e[2] = t.styles.lineDashIII), t.styles.lineDash = e, t.styles.lineJoin) {case 0:t.styles.lineJoin = "miter";break;case 1:t.styles.lineJoin = "round";break;case 2:t.styles.lineJoin = "bevel";}switch (t.styles.lineCap) {case 0:t.styles.lineCap = "butt";break;case 1:t.styles.lineCap = "round";break;case 2:t.styles.lineCap = "square";}}}), e.shapes[0] && "keep" === e.shapes[0].type ? this.shapes = t.lastShapes : (this.shapes = e.shapes, t.lastShapes = e.shapes));var r = this.transform.a * this.layout.x + this.transform.c * this.layout.y + this.transform.tx,n = this.transform.a * (this.layout.x + this.layout.width) + this.transform.c * this.layout.y + this.transform.tx,o = this.transform.a * this.layout.x + this.transform.c * (this.layout.y + this.layout.height) + this.transform.tx,s = this.transform.a * (this.layout.x + this.layout.width) + this.transform.c * (this.layout.y + this.layout.height) + this.transform.tx,a = this.transform.b * this.layout.x + this.transform.d * this.layout.y + this.transform.ty,u = this.transform.b * (this.layout.x + this.layout.width) + this.transform.d * this.layout.y + this.transform.ty,h = this.transform.b * this.layout.x + this.transform.d * (this.layout.y + this.layout.height) + this.transform.ty,l = this.transform.b * (this.layout.x + this.layout.width) + this.transform.d * (this.layout.y + this.layout.height) + this.transform.ty;this.nx = Math.min(Math.min(o, s), Math.min(r, n)), this.ny = Math.min(Math.min(h, l), Math.min(a, u));};r.FrameEntity = n;}, { 36: 36 }], 39: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.Player = r.Parser = void 0;var i = t(41),n = t(42);r.Parser = i.Parser, r.Player = n.Player;}, { 41: 41, 42: 42 }], 42: [function (t, e, r) {"use strict";var i = this && this.__awaiter || function (t, e, r, i) {return new (r || (r = Promise))(function (n, o) {function s(t) {try {u(i.next(t));} catch (e) {o(e);}}function a(t) {try {u(i.throw(t));} catch (e) {o(e);}}function u(t) {var e;t.done ? n(t.value) : (e = t.value, e instanceof r ? e : new r(function (t) {t(e);})).then(s, a);}u((i = i.apply(t, e || [])).next());});},n = this && this.__generator || function (t, e) {var r,i,n,o,s = { label: 0, sent: function () {if (1 & n[0]) throw n[1];return n[1];}, trys: [], ops: [] };return o = { next: a(0), throw: a(1), return: a(2) }, "function" == typeof Symbol && (o[Symbol.iterator] = function () {return this;}), o;function a(o) {return function (a) {return function (o) {if (r) throw new TypeError("Generator is already executing.");for (; s;) try {if (r = 1, i && (n = 2 & o[0] ? i.return : o[0] ? i.throw || ((n = i.return) && n.call(i), 0) : i.next) && !(n = n.call(i, o[1])).done) return n;switch (i = 0, n && (o = [2 & o[0], n.value]), o[0]) {case 0:case 1:n = o;break;case 4:return s.label++, { value: o[1], done: !1 };case 5:s.label++, i = o[1], o = [0];continue;case 7:o = s.ops.pop(), s.trys.pop();continue;default:if (!(n = (n = s.trys).length > 0 && n[n.length - 1]) && (6 === o[0] || 2 === o[0])) {s = 0;continue;}if (3 === o[0] && (!n || o[1] > n[0] && o[1] < n[3])) {s.label = o[1];break;}if (6 === o[0] && s.label < n[1]) {s.label = n[1], n = o;break;}if (n && s.label < n[2]) {s.label = n[2], s.ops.push(o);break;}n[2] && s.ops.pop(), s.trys.pop();continue;}o = e.call(t, s);} catch (a) {o = [6, a], i = 0;} finally {r = n = 0;}if (5 & o[0]) throw o[1];return { value: o[0] ? o[1] : void 0, done: !0 };}([o, a]);};}};Object.defineProperty(r, "__esModule", { value: !0 }), r.Player = void 0;var o = t(45),s = t(47),a = t(35).getMiniBridge(),u = function () {function t() {this.loops = 0, this.clearsAfterStop = !0, this.fillMode = "Forward", this._contentMode = "AspectFit", this._animator = new s.ValueAnimator(), this._forwardAnimating = !1, this._currentFrame = 0, this._dynamicImage = {}, this._dynamicText = {};}return t.prototype.setCanvas = function (t, e) {return i(this, void 0, void 0, function () {var r = this;return n(this, function (i) {return [2, new Promise(function (i, n) {var o = a.createSelectorQuery();e && (o = o.in(e)), o.select(t).fields({ node: !0, size: !0 }).exec(function (t) {var e;if (r.canvas = null === (e = null == t ? void 0 : t[0]) || void 0 === e ? void 0 : e.node, r.canvas) {if (r.ctx = r.canvas.getContext("2d"), r.ctx) {var o = a.getSystemInfoSync().pixelRatio;r.canvas.width = t[0].width * o, r.canvas.height = t[0].height * o, i(void 0);} else n("canvas context not found.");} else n("canvas not found.");});})];});});}, t.prototype.setVideoItem = function (t) {return i(this, void 0, void 0, function () {var e,r,s = this;return n(this, function (a) {switch (a.label) {case 0:return this._currentFrame = 0, this._videoItem = t, t ? [4, Promise.all(Object.keys(t.spec.images).map(function (e) {return i(s, void 0, void 0, function () {var r;return n(this, function (i) {switch (i.label) {case 0:return i.trys.push([0, 2,, 3]), [4, this.loadWXImage(t.spec.images[e])];case 1:return r = i.sent(), [2, { key: e, value: r }];case 2:return i.sent(), [2, { key: e, value: void 0 }];case 3:return [2];}});});}))] : [3, 2];case 1:return e = a.sent(), r = {}, e.forEach(function (t) {r[t.key] = t.value;}), t.decodedImages = r, this._renderer = new o.Renderer(this._videoItem, this.ctx, this.canvas), [3, 3];case 2:this._renderer = void 0, a.label = 3;case 3:return this.clear(), this._update(), [2];}});});}, t.prototype.loadWXImage = function (t) {var e = this;if (!this.canvas) throw "no canvas";return new Promise(function (r, i) {var n = e.canvas.createImage();n.onload = function () {r(n);}, n.onerror = function (t) {console.log(t), i("image decoded fail.");}, n.src = "string" == typeof t ? t : "data:image/png;base64," + a.arrayBufferToBase64(t);});}, t.prototype.setContentMode = function (t) {this._contentMode = t, this._update();}, t.prototype.startAnimation = function (t) {void 0 === t && (t = !1), this.stopAnimation(!1), this._doStart(void 0, t, void 0);}, t.prototype.startAnimationWithRange = function (t, e) {void 0 === e && (e = !1), this.stopAnimation(!1), this._doStart(t, e, void 0);}, t.prototype.pauseAnimation = function () {this.stopAnimation(!1);}, t.prototype.stopAnimation = function (t) {this._forwardAnimating = !1, void 0 !== this._animator && this._animator.stop(), void 0 === t && (t = this.clearsAfterStop), t && this.clear();}, t.prototype.clear = function () {var t;null === (t = this._renderer) || void 0 === t || t.clear();}, t.prototype.stepToFrame = function (t, e) {void 0 === e && (e = !1);var r = this._videoItem;r && (t >= r.frames || t < 0 || (this.pauseAnimation(), this._currentFrame = t, this._update(), e && this._doStart(void 0, !1, this._currentFrame)));}, t.prototype.stepToPercentage = function (t, e) {void 0 === e && (e = !1);var r = this._videoItem;if (r) {var i = t * r.frames;i >= r.frames && i > 0 && (i = r.frames - 1), this.stepToFrame(i, e);}}, t.prototype.setImage = function (t, e) {return i(this, void 0, void 0, function () {var r;return n(this, function (i) {switch (i.label) {case 0:return [4, this.loadWXImage(t)];case 1:return r = i.sent(), this._dynamicImage[e] = r, [2];}});});}, t.prototype.setText = function (t, e) {this._dynamicText[e] = t;}, t.prototype.clearDynamicObjects = function () {this._dynamicImage = {}, this._dynamicText = {};}, t.prototype.onFinished = function (t) {this._onFinished = t;}, t.prototype.onFrame = function (t) {this._onFrame = t;}, t.prototype.onPercentage = function (t) {this._onPercentage = t;}, t.prototype._doStart = function (t, e, r) {var i = this;void 0 === e && (e = !1), void 0 === r && (r = 0);var n = this._videoItem;n && (this._animator = new s.ValueAnimator(), this._animator.canvas = this.canvas, void 0 !== t ? (this._animator.startValue = Math.max(0, t.location), this._animator.endValue = Math.min(n.frames - 1, t.location + t.length), this._animator.duration = (this._animator.endValue - this._animator.startValue + 1) * (1 / n.FPS) * 1e3) : (this._animator.startValue = 0, this._animator.endValue = n.frames - 1, this._animator.duration = n.frames * (1 / n.FPS) * 1e3), this._animator.loops = this.loops <= 0 ? 1 / 0 : this.loops, this._animator.fillRule = "Backward" === this.fillMode ? 1 : 0, this._animator.onUpdate = function (t) {i._currentFrame !== Math.floor(t) && (i._forwardAnimating && (i._currentFrame, Math.floor(t)), i._currentFrame = Math.floor(t), i._update(), "function" == typeof i._onFrame && i._onFrame(i._currentFrame), "function" == typeof i._onPercentage && i._onPercentage((i._currentFrame + 1) / n.frames));}, this._animator.onEnd = function () {i._forwardAnimating = !1, !0 === i.clearsAfterStop && i.clear(), "function" == typeof i._onFinished && i._onFinished();}, !0 === e ? (this._animator.reverse(r), this._forwardAnimating = !1) : (this._animator.start(r), this._forwardAnimating = !0), this._currentFrame = this._animator.startValue, this._update());}, t.prototype._resize = function () {var t = this.ctx,e = this._videoItem;if (t && e) {var r = 1,i = 1,n = 0,o = 0,s = this.canvas.width,a = this.canvas.height,u = e.videoSize;if ("Fill" === this._contentMode) r = s / u.width, i = a / u.height;else if ("AspectFit" === this._contentMode || "AspectFill" === this._contentMode) {var h = u.width / u.height,l = s / a;h >= l && "AspectFit" === this._contentMode || h <= l && "AspectFill" === this._contentMode ? (r = i = s / u.width, o = (a - u.height * i) / 2) : (h < l && "AspectFit" === this._contentMode || h > l && "AspectFill" === this._contentMode) && (r = i = a / u.height, n = (s - u.width * r) / 2);}this._renderer && (this._renderer.globalTransform = { a: r, b: 0, c: 0, d: i, tx: n, ty: o });}}, t.prototype._update = function () {this._resize(), this._renderer && (this._renderer._dynamicImage = this._dynamicImage, this._renderer._dynamicText = this._dynamicText, this._renderer.drawFrame(this._currentFrame), this._renderer.playAudio(this._currentFrame));}, t;}();r.Player = u;}, { 35: 35, 45: 45, 47: 47 }], 41: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.Parser = void 0;var i = t(48),n = t(35),o = t(40).inflate,s = t(43).ProtoMovieEntity,a = n.getMiniBridge(),u = function () {function t() {}return t.prototype.load = function (t) {return new Promise(function (e, r) {0 === t.indexOf("http://") || 0 === t.indexOf("https://") ? a.request({ url: t, dataType: "arraybuffer", responseType: "arraybuffer", success: function (t) {try {var n = o(t.data),a = s.decode(n);e(new i.VideoEntity(a));} catch (u) {r(u);}}, fail: function (t) {r(t);} }) : a.getFileSystemManager().readFile({ filePath: t, success: function (t) {try {var n = o(t.data),a = s.decode(n);e(new i.VideoEntity(a));} catch (u) {r(u);}}, fail: function (t) {r(t);} });});}, t;}();r.Parser = u;}, { 35: 35, 40: 40, 43: 43, 48: 48 }], 40: [function (t, e, r) {"use strict";var i;i = this, function (t) {var e = function (t, e, r, i) {for (var n = 65535 & t | 0, o = t >>> 16 & 65535 | 0, s = 0; 0 !== r;) {r -= s = r > 2e3 ? 2e3 : r;do {o = o + (n = n + e[i++] | 0) | 0;} while (--s);n %= 65521, o %= 65521;}return n | o << 16 | 0;},r = new Uint32Array(function () {for (var t, e = [], r = 0; r < 256; r++) {t = r;for (var i = 0; i < 8; i++) t = 1 & t ? 3988292384 ^ t >>> 1 : t >>> 1;e[r] = t;}return e;}()),i = function (t, e, i, n) {var o = r,s = n + i;t ^= -1;for (var a = n; a < s; a++) t = t >>> 8 ^ o[255 & (t ^ e[a])];return -1 ^ t;},n = function (t, e) {var r,i,n,o,s,a,u,h,l,f,c,d,p,y,m,v,g,b,w,_,x,k,A,O,S = t.state;r = t.next_in, A = t.input, i = r + (t.avail_in - 5), n = t.next_out, O = t.output, o = n - (e - t.avail_out), s = n + (t.avail_out - 257), a = S.dmax, u = S.wsize, h = S.whave, l = S.wnext, f = S.window, c = S.hold, d = S.bits, p = S.lencode, y = S.distcode, m = (1 << S.lenbits) - 1, v = (1 << S.distbits) - 1;t: do {d < 15 && (c += A[r++] << d, d += 8, c += A[r++] << d, d += 8), g = p[c & m];e: for (;;) {if (c >>>= b = g >>> 24, d -= b, 0 == (b = g >>> 16 & 255)) O[n++] = 65535 & g;else {if (!(16 & b)) {if (0 == (64 & b)) {g = p[(65535 & g) + (c & (1 << b) - 1)];continue e;}if (32 & b) {S.mode = 12;break t;}t.msg = "invalid literal/length code", S.mode = 30;break t;}w = 65535 & g, (b &= 15) && (d < b && (c += A[r++] << d, d += 8), w += c & (1 << b) - 1, c >>>= b, d -= b), d < 15 && (c += A[r++] << d, d += 8, c += A[r++] << d, d += 8), g = y[c & v];r: for (;;) {if (c >>>= b = g >>> 24, d -= b, !(16 & (b = g >>> 16 & 255))) {if (0 == (64 & b)) {g = y[(65535 & g) + (c & (1 << b) - 1)];continue r;}t.msg = "invalid distance code", S.mode = 30;break t;}if (_ = 65535 & g, d < (b &= 15) && (c += A[r++] << d, (d += 8) < b && (c += A[r++] << d, d += 8)), (_ += c & (1 << b) - 1) > a) {t.msg = "invalid distance too far back", S.mode = 30;break t;}if (c >>>= b, d -= b, _ > (b = n - o)) {if ((b = _ - b) > h && S.sane) {t.msg = "invalid distance too far back", S.mode = 30;break t;}if (x = 0, k = f, 0 === l) {if (x += u - b, b < w) {w -= b;do {O[n++] = f[x++];} while (--b);x = n - _, k = O;}} else if (l < b) {if (x += u + l - b, (b -= l) < w) {w -= b;do {O[n++] = f[x++];} while (--b);if (x = 0, l < w) {w -= b = l;do {O[n++] = f[x++];} while (--b);x = n - _, k = O;}}} else if (x += l - b, b < w) {w -= b;do {O[n++] = f[x++];} while (--b);x = n - _, k = O;}for (; w > 2;) O[n++] = k[x++], O[n++] = k[x++], O[n++] = k[x++], w -= 3;w && (O[n++] = k[x++], w > 1 && (O[n++] = k[x++]));} else {x = n - _;do {O[n++] = O[x++], O[n++] = O[x++], O[n++] = O[x++], w -= 3;} while (w > 2);w && (O[n++] = O[x++], w > 1 && (O[n++] = O[x++]));}break;}}break;}} while (r < i && n < s);r -= w = d >> 3, c &= (1 << (d -= w << 3)) - 1, t.next_in = r, t.next_out = n, t.avail_in = r < i ? i - r + 5 : 5 - (r - i), t.avail_out = n < s ? s - n + 257 : 257 - (n - s), S.hold = c, S.bits = d;},o = new Uint16Array([3, 4, 5, 6, 7, 8, 9, 10, 11, 13, 15, 17, 19, 23, 27, 31, 35, 43, 51, 59, 67, 83, 99, 115, 131, 163, 195, 227, 258, 0, 0]),s = new Uint8Array([16, 16, 16, 16, 16, 16, 16, 16, 17, 17, 17, 17, 18, 18, 18, 18, 19, 19, 19, 19, 20, 20, 20, 20, 21, 21, 21, 21, 16, 72, 78]),a = new Uint16Array([1, 2, 3, 4, 5, 7, 9, 13, 17, 25, 33, 49, 65, 97, 129, 193, 257, 385, 513, 769, 1025, 1537, 2049, 3073, 4097, 6145, 8193, 12289, 16385, 24577, 0, 0]),u = new Uint8Array([16, 16, 16, 16, 17, 17, 18, 18, 19, 19, 20, 20, 21, 21, 22, 22, 23, 23, 24, 24, 25, 25, 26, 26, 27, 27, 28, 28, 29, 29, 64, 64]),h = function (t, e, r, i, n, h, l, f) {var c,d,p,y,m,v,g,b,w,_ = f.bits,x = 0,k = 0,A = 0,O = 0,S = 0,E = 0,N = 0,T = 0,j = 0,R = 0,F = null,I = 0,B = new Uint16Array(16),P = new Uint16Array(16),C = null,M = 0;for (x = 0; x <= 15; x++) B[x] = 0;for (k = 0; k < i; k++) B[e[r + k]]++;for (S = _, O = 15; O >= 1 && 0 === B[O]; O--);if (S > O && (S = O), 0 === O) return n[h++] = 20971520, n[h++] = 20971520, f.bits = 1, 0;for (A = 1; A < O && 0 === B[A]; A++);for (S < A && (S = A), T = 1, x = 1; x <= 15; x++) if (T <<= 1, (T -= B[x]) < 0) return -1;if (T > 0 && (0 === t || 1 !== O)) return -1;for (P[1] = 0, x = 1; x < 15; x++) P[x + 1] = P[x] + B[x];for (k = 0; k < i; k++) 0 !== e[r + k] && (l[P[e[r + k]]++] = k);if (0 === t ? (F = C = l, v = 19) : 1 === t ? (F = o, I -= 257, C = s, M -= 257, v = 256) : (F = a, C = u, v = -1), R = 0, k = 0, x = A, m = h, E = S, N = 0, p = -1, y = (j = 1 << S) - 1, 1 === t && j > 852 || 2 === t && j > 592) return 1;for (;;) {g = x - N, l[k] < v ? (b = 0, w = l[k]) : l[k] > v ? (b = C[M + l[k]], w = F[I + l[k]]) : (b = 96, w = 0), c = 1 << x - N, A = d = 1 << E;do {n[m + (R >> N) + (d -= c)] = g << 24 | b << 16 | w | 0;} while (0 !== d);for (c = 1 << x - 1; R & c;) c >>= 1;if (0 !== c ? (R &= c - 1, R += c) : R = 0, k++, 0 == --B[x]) {if (x === O) break;x = e[r + l[k]];}if (x > S && (R & y) !== p) {for (0 === N && (N = S), m += A, T = 1 << (E = x - N); E + N < O && !((T -= B[E + N]) <= 0);) E++, T <<= 1;if (j += 1 << E, 1 === t && j > 852 || 2 === t && j > 592) return 1;n[p = R & y] = S << 24 | E << 16 | m - h | 0;}}return 0 !== R && (n[m + R] = x - N << 24 | 64 << 16 | 0), f.bits = S, 0;},l = { Z_NO_FLUSH: 0, Z_PARTIAL_FLUSH: 1, Z_SYNC_FLUSH: 2, Z_FULL_FLUSH: 3, Z_FINISH: 4, Z_BLOCK: 5, Z_TREES: 6, Z_OK: 0, Z_STREAM_END: 1, Z_NEED_DICT: 2, Z_ERRNO: -1, Z_STREAM_ERROR: -2, Z_DATA_ERROR: -3, Z_MEM_ERROR: -4, Z_BUF_ERROR: -5, Z_NO_COMPRESSION: 0, Z_BEST_SPEED: 1, Z_BEST_COMPRESSION: 9, Z_DEFAULT_COMPRESSION: -1, Z_FILTERED: 1, Z_HUFFMAN_ONLY: 2, Z_RLE: 3, Z_FIXED: 4, Z_DEFAULT_STRATEGY: 0, Z_BINARY: 0, Z_TEXT: 1, Z_UNKNOWN: 2, Z_DEFLATED: 8 },f = l.Z_FINISH,c = l.Z_BLOCK,d = l.Z_TREES,p = l.Z_OK,y = l.Z_STREAM_END,m = l.Z_NEED_DICT,v = l.Z_STREAM_ERROR,g = l.Z_DATA_ERROR,b = l.Z_MEM_ERROR,w = l.Z_BUF_ERROR,_ = l.Z_DEFLATED,x = 12,k = 30,A = function (t) {return (t >>> 24 & 255) + (t >>> 8 & 65280) + ((65280 & t) << 8) + ((255 & t) << 24);};function O() {this.mode = 0, this.last = !1, this.wrap = 0, this.havedict = !1, this.flags = 0, this.dmax = 0, this.check = 0, this.total = 0, this.head = null, this.wbits = 0, this.wsize = 0, this.whave = 0, this.wnext = 0, this.window = null, this.hold = 0, this.bits = 0, this.length = 0, this.offset = 0, this.extra = 0, this.lencode = null, this.distcode = null, this.lenbits = 0, this.distbits = 0, this.ncode = 0, this.nlen = 0, this.ndist = 0, this.have = 0, this.next = null, this.lens = new Uint16Array(320), this.work = new Uint16Array(288), this.lendyn = null, this.distdyn = null, this.sane = 0, this.back = 0, this.was = 0;}var S,E,N = function (t) {if (!t || !t.state) return v;var e = t.state;return t.total_in = t.total_out = e.total = 0, t.msg = "", e.wrap && (t.adler = 1 & e.wrap), e.mode = 1, e.last = 0, e.havedict = 0, e.dmax = 32768, e.head = null, e.hold = 0, e.bits = 0, e.lencode = e.lendyn = new Int32Array(852), e.distcode = e.distdyn = new Int32Array(592), e.sane = 1, e.back = -1, p;},T = function (t) {if (!t || !t.state) return v;var e = t.state;return e.wsize = 0, e.whave = 0, e.wnext = 0, N(t);},j = function (t, e) {var r;if (!t || !t.state) return v;var i = t.state;return e < 0 ? (r = 0, e = -e) : (r = 1 + (e >> 4), e < 48 && (e &= 15)), e && (e < 8 || e > 15) ? v : (null !== i.window && i.wbits !== e && (i.window = null), i.wrap = r, i.wbits = e, T(t));},R = function (t, e) {if (!t) return v;var r = new O();t.state = r, r.window = null;var i = j(t, e);return i !== p && (t.state = null), i;},F = !0,I = function (t) {if (F) {S = new Int32Array(512), E = new Int32Array(32);for (var e = 0; e < 144;) t.lens[e++] = 8;for (; e < 256;) t.lens[e++] = 9;for (; e < 280;) t.lens[e++] = 7;for (; e < 288;) t.lens[e++] = 8;for (h(1, t.lens, 0, 288, S, 0, t.work, { bits: 9 }), e = 0; e < 32;) t.lens[e++] = 5;h(2, t.lens, 0, 32, E, 0, t.work, { bits: 5 }), F = !1;}t.lencode = S, t.lenbits = 9, t.distcode = E, t.distbits = 5;},B = function (t, e, r, i) {var n,o = t.state;return null === o.window && (o.wsize = 1 << o.wbits, o.wnext = 0, o.whave = 0, o.window = new Uint8Array(o.wsize)), i >= o.wsize ? (o.window.set(e.subarray(r - o.wsize, r), 0), o.wnext = 0, o.whave = o.wsize) : ((n = o.wsize - o.wnext) > i && (n = i), o.window.set(e.subarray(r - i, r - i + n), o.wnext), (i -= n) ? (o.window.set(e.subarray(r - i, r), 0), o.wnext = i, o.whave = o.wsize) : (o.wnext += n, o.wnext === o.wsize && (o.wnext = 0), o.whave < o.wsize && (o.whave += n))), 0;},P = T,C = R,M = function (t, r) {var o,s,a,u,l,O,S,E,N,T,j,R,F,P,C,M,D,L,z,V,Z,U,q,J,$ = 0,K = new Uint8Array(4),H = new Uint8Array([16, 17, 18, 0, 8, 7, 9, 6, 10, 5, 11, 4, 12, 3, 13, 2, 14, 1, 15]);if (!t || !t.state || !t.output || !t.input && 0 !== t.avail_in) return v;(o = t.state).mode === x && (o.mode = 13), l = t.next_out, a = t.output, S = t.avail_out, u = t.next_in, s = t.input, O = t.avail_in, E = o.hold, N = o.bits, T = O, j = S, U = p;t: for (;;) switch (o.mode) {case 1:if (0 === o.wrap) {o.mode = 13;break;}for (; N < 16;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (2 & o.wrap && 35615 === E) {o.check = 0, K[0] = 255 & E, K[1] = E >>> 8 & 255, o.check = i(o.check, K, 2, 0), E = 0, N = 0, o.mode = 2;break;}if (o.flags = 0, o.head && (o.head.done = !1), !(1 & o.wrap) || (((255 & E) << 8) + (E >> 8)) % 31) {t.msg = "incorrect header check", o.mode = k;break;}if ((15 & E) !== _) {t.msg = "unknown compression method", o.mode = k;break;}if (N -= 4, Z = 8 + (15 & (E >>>= 4)), 0 === o.wbits) o.wbits = Z;else if (Z > o.wbits) {t.msg = "invalid window size", o.mode = k;break;}o.dmax = 1 << o.wbits, t.adler = o.check = 1, o.mode = 512 & E ? 10 : x, E = 0, N = 0;break;case 2:for (; N < 16;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (o.flags = E, (255 & o.flags) !== _) {t.msg = "unknown compression method", o.mode = k;break;}if (57344 & o.flags) {t.msg = "unknown header flags set", o.mode = k;break;}o.head && (o.head.text = E >> 8 & 1), 512 & o.flags && (K[0] = 255 & E, K[1] = E >>> 8 & 255, o.check = i(o.check, K, 2, 0)), E = 0, N = 0, o.mode = 3;case 3:for (; N < 32;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}o.head && (o.head.time = E), 512 & o.flags && (K[0] = 255 & E, K[1] = E >>> 8 & 255, K[2] = E >>> 16 & 255, K[3] = E >>> 24 & 255, o.check = i(o.check, K, 4, 0)), E = 0, N = 0, o.mode = 4;case 4:for (; N < 16;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}o.head && (o.head.xflags = 255 & E, o.head.os = E >> 8), 512 & o.flags && (K[0] = 255 & E, K[1] = E >>> 8 & 255, o.check = i(o.check, K, 2, 0)), E = 0, N = 0, o.mode = 5;case 5:if (1024 & o.flags) {for (; N < 16;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}o.length = E, o.head && (o.head.extra_len = E), 512 & o.flags && (K[0] = 255 & E, K[1] = E >>> 8 & 255, o.check = i(o.check, K, 2, 0)), E = 0, N = 0;} else o.head && (o.head.extra = null);o.mode = 6;case 6:if (1024 & o.flags && ((R = o.length) > O && (R = O), R && (o.head && (Z = o.head.extra_len - o.length, o.head.extra || (o.head.extra = new Uint8Array(o.head.extra_len)), o.head.extra.set(s.subarray(u, u + R), Z)), 512 & o.flags && (o.check = i(o.check, s, R, u)), O -= R, u += R, o.length -= R), o.length)) break t;o.length = 0, o.mode = 7;case 7:if (2048 & o.flags) {if (0 === O) break t;R = 0;do {Z = s[u + R++], o.head && Z && o.length < 65536 && (o.head.name += String.fromCharCode(Z));} while (Z && R < O);if (512 & o.flags && (o.check = i(o.check, s, R, u)), O -= R, u += R, Z) break t;} else o.head && (o.head.name = null);o.length = 0, o.mode = 8;case 8:if (4096 & o.flags) {if (0 === O) break t;R = 0;do {Z = s[u + R++], o.head && Z && o.length < 65536 && (o.head.comment += String.fromCharCode(Z));} while (Z && R < O);if (512 & o.flags && (o.check = i(o.check, s, R, u)), O -= R, u += R, Z) break t;} else o.head && (o.head.comment = null);o.mode = 9;case 9:if (512 & o.flags) {for (; N < 16;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (E !== (65535 & o.check)) {t.msg = "header crc mismatch", o.mode = k;break;}E = 0, N = 0;}o.head && (o.head.hcrc = o.flags >> 9 & 1, o.head.done = !0), t.adler = o.check = 0, o.mode = x;break;case 10:for (; N < 32;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}t.adler = o.check = A(E), E = 0, N = 0, o.mode = 11;case 11:if (0 === o.havedict) return t.next_out = l, t.avail_out = S, t.next_in = u, t.avail_in = O, o.hold = E, o.bits = N, m;t.adler = o.check = 1, o.mode = x;case x:if (r === c || r === d) break t;case 13:if (o.last) {E >>>= 7 & N, N -= 7 & N, o.mode = 27;break;}for (; N < 3;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}switch (o.last = 1 & E, N -= 1, 3 & (E >>>= 1)) {case 0:o.mode = 14;break;case 1:if (I(o), o.mode = 20, r === d) {E >>>= 2, N -= 2;break t;}break;case 2:o.mode = 17;break;case 3:t.msg = "invalid block type", o.mode = k;}E >>>= 2, N -= 2;break;case 14:for (E >>>= 7 & N, N -= 7 & N; N < 32;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if ((65535 & E) != (E >>> 16 ^ 65535)) {t.msg = "invalid stored block lengths", o.mode = k;break;}if (o.length = 65535 & E, E = 0, N = 0, o.mode = 15, r === d) break t;case 15:o.mode = 16;case 16:if (R = o.length) {if (R > O && (R = O), R > S && (R = S), 0 === R) break t;a.set(s.subarray(u, u + R), l), O -= R, u += R, S -= R, l += R, o.length -= R;break;}o.mode = x;break;case 17:for (; N < 14;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (o.nlen = 257 + (31 & E), E >>>= 5, N -= 5, o.ndist = 1 + (31 & E), E >>>= 5, N -= 5, o.ncode = 4 + (15 & E), E >>>= 4, N -= 4, o.nlen > 286 || o.ndist > 30) {t.msg = "too many length or distance symbols", o.mode = k;break;}o.have = 0, o.mode = 18;case 18:for (; o.have < o.ncode;) {for (; N < 3;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}o.lens[H[o.have++]] = 7 & E, E >>>= 3, N -= 3;}for (; o.have < 19;) o.lens[H[o.have++]] = 0;if (o.lencode = o.lendyn, o.lenbits = 7, q = { bits: o.lenbits }, U = h(0, o.lens, 0, 19, o.lencode, 0, o.work, q), o.lenbits = q.bits, U) {t.msg = "invalid code lengths set", o.mode = k;break;}o.have = 0, o.mode = 19;case 19:for (; o.have < o.nlen + o.ndist;) {for (; M = ($ = o.lencode[E & (1 << o.lenbits) - 1]) >>> 16 & 255, D = 65535 & $, !((C = $ >>> 24) <= N);) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (D < 16) E >>>= C, N -= C, o.lens[o.have++] = D;else {if (16 === D) {for (J = C + 2; N < J;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (E >>>= C, N -= C, 0 === o.have) {t.msg = "invalid bit length repeat", o.mode = k;break;}Z = o.lens[o.have - 1], R = 3 + (3 & E), E >>>= 2, N -= 2;} else if (17 === D) {for (J = C + 3; N < J;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}N -= C, Z = 0, R = 3 + (7 & (E >>>= C)), E >>>= 3, N -= 3;} else {for (J = C + 7; N < J;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}N -= C, Z = 0, R = 11 + (127 & (E >>>= C)), E >>>= 7, N -= 7;}if (o.have + R > o.nlen + o.ndist) {t.msg = "invalid bit length repeat", o.mode = k;break;}for (; R--;) o.lens[o.have++] = Z;}}if (o.mode === k) break;if (0 === o.lens[256]) {t.msg = "invalid code -- missing end-of-block", o.mode = k;break;}if (o.lenbits = 9, q = { bits: o.lenbits }, U = h(1, o.lens, 0, o.nlen, o.lencode, 0, o.work, q), o.lenbits = q.bits, U) {t.msg = "invalid literal/lengths set", o.mode = k;break;}if (o.distbits = 6, o.distcode = o.distdyn, q = { bits: o.distbits }, U = h(2, o.lens, o.nlen, o.ndist, o.distcode, 0, o.work, q), o.distbits = q.bits, U) {t.msg = "invalid distances set", o.mode = k;break;}if (o.mode = 20, r === d) break t;case 20:o.mode = 21;case 21:if (O >= 6 && S >= 258) {t.next_out = l, t.avail_out = S, t.next_in = u, t.avail_in = O, o.hold = E, o.bits = N, n(t, j), l = t.next_out, a = t.output, S = t.avail_out, u = t.next_in, s = t.input, O = t.avail_in, E = o.hold, N = o.bits, o.mode === x && (o.back = -1);break;}for (o.back = 0; M = ($ = o.lencode[E & (1 << o.lenbits) - 1]) >>> 16 & 255, D = 65535 & $, !((C = $ >>> 24) <= N);) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (M && 0 == (240 & M)) {for (L = C, z = M, V = D; M = ($ = o.lencode[V + ((E & (1 << L + z) - 1) >> L)]) >>> 16 & 255, D = 65535 & $, !(L + (C = $ >>> 24) <= N);) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}E >>>= L, N -= L, o.back += L;}if (E >>>= C, N -= C, o.back += C, o.length = D, 0 === M) {o.mode = 26;break;}if (32 & M) {o.back = -1, o.mode = x;break;}if (64 & M) {t.msg = "invalid literal/length code", o.mode = k;break;}o.extra = 15 & M, o.mode = 22;case 22:if (o.extra) {for (J = o.extra; N < J;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}o.length += E & (1 << o.extra) - 1, E >>>= o.extra, N -= o.extra, o.back += o.extra;}o.was = o.length, o.mode = 23;case 23:for (; M = ($ = o.distcode[E & (1 << o.distbits) - 1]) >>> 16 & 255, D = 65535 & $, !((C = $ >>> 24) <= N);) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (0 == (240 & M)) {for (L = C, z = M, V = D; M = ($ = o.distcode[V + ((E & (1 << L + z) - 1) >> L)]) >>> 16 & 255, D = 65535 & $, !(L + (C = $ >>> 24) <= N);) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}E >>>= L, N -= L, o.back += L;}if (E >>>= C, N -= C, o.back += C, 64 & M) {t.msg = "invalid distance code", o.mode = k;break;}o.offset = D, o.extra = 15 & M, o.mode = 24;case 24:if (o.extra) {for (J = o.extra; N < J;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}o.offset += E & (1 << o.extra) - 1, E >>>= o.extra, N -= o.extra, o.back += o.extra;}if (o.offset > o.dmax) {t.msg = "invalid distance too far back", o.mode = k;break;}o.mode = 25;case 25:if (0 === S) break t;if (R = j - S, o.offset > R) {if ((R = o.offset - R) > o.whave && o.sane) {t.msg = "invalid distance too far back", o.mode = k;break;}R > o.wnext ? (R -= o.wnext, F = o.wsize - R) : F = o.wnext - R, R > o.length && (R = o.length), P = o.window;} else P = a, F = l - o.offset, R = o.length;R > S && (R = S), S -= R, o.length -= R;do {a[l++] = P[F++];} while (--R);0 === o.length && (o.mode = 21);break;case 26:if (0 === S) break t;a[l++] = o.length, S--, o.mode = 21;break;case 27:if (o.wrap) {for (; N < 32;) {if (0 === O) break t;O--, E |= s[u++] << N, N += 8;}if (j -= S, t.total_out += j, o.total += j, j && (t.adler = o.check = o.flags ? i(o.check, a, j, l - j) : e(o.check, a, j, l - j)), j = S, (o.flags ? E : A(E)) !== o.check) {t.msg = "incorrect data check", o.mode = k;break;}E = 0, N = 0;}o.mode = 28;case 28:if (o.wrap && o.flags) {for (; N < 32;) {if (0 === O) break t;O--, E += s[u++] << N, N += 8;}if (E !== (4294967295 & o.total)) {t.msg = "incorrect length check", o.mode = k;break;}E = 0, N = 0;}o.mode = 29;case 29:U = y;break t;case k:U = g;break t;case 31:return b;case 32:default:return v;}return t.next_out = l, t.avail_out = S, t.next_in = u, t.avail_in = O, o.hold = E, o.bits = N, (o.wsize || j !== t.avail_out && o.mode < k && (o.mode < 27 || r !== f)) && B(t, t.output, t.next_out, j - t.avail_out), T -= t.avail_in, j -= t.avail_out, t.total_in += T, t.total_out += j, o.total += j, o.wrap && j && (t.adler = o.check = o.flags ? i(o.check, a, j, t.next_out - j) : e(o.check, a, j, t.next_out - j)), t.data_type = o.bits + (o.last ? 64 : 0) + (o.mode === x ? 128 : 0) + (20 === o.mode || 15 === o.mode ? 256 : 0), (0 === T && 0 === j || r === f) && U === p && (U = w), U;},D = function (t) {if (!t || !t.state) return v;var e = t.state;return e.window && (e.window = null), t.state = null, p;},L = function (t, e) {if (!t || !t.state) return v;var r = t.state;return 0 == (2 & r.wrap) ? v : (r.head = e, e.done = !1, p);},z = function (t, r) {var i,n = r.length;return t && t.state ? 0 !== (i = t.state).wrap && 11 !== i.mode ? v : 11 === i.mode && e(1, r, n, 0) !== i.check ? g : B(t, r, n, n) ? (i.mode = 31, b) : (i.havedict = 1, p) : v;},V = function (t, e) {return Object.prototype.hasOwnProperty.call(t, e);},Z = !0;try {String.fromCharCode.apply(null, new Uint8Array(1));} catch (t) {Z = !1;}for (var U = new Uint8Array(256), q = 0; q < 256; q++) U[q] = q >= 252 ? 6 : q >= 248 ? 5 : q >= 240 ? 4 : q >= 224 ? 3 : q >= 192 ? 2 : 1;U[254] = U[254] = 1;var J = function (t, e) {var r,i,n = e || t.length,o = new Array(2 * n);for (i = 0, r = 0; r < n;) {var s = t[r++];if (s < 128) o[i++] = s;else {var a = U[s];if (a > 4) o[i++] = 65533, r += a - 1;else {for (s &= 2 === a ? 31 : 3 === a ? 15 : 7; a > 1 && r < n;) s = s << 6 | 63 & t[r++], a--;a > 1 ? o[i++] = 65533 : s < 65536 ? o[i++] = s : (s -= 65536, o[i++] = 55296 | s >> 10 & 1023, o[i++] = 56320 | 1023 & s);}}}return function (t, e) {if (e < 65534 && t.subarray && Z) return String.fromCharCode.apply(null, t.length === e ? t : t.subarray(0, e));for (var r = "", i = 0; i < e; i++) r += String.fromCharCode(t[i]);return r;}(o, i);},$ = function (t, e) {(e = e || t.length) > t.length && (e = t.length);for (var r = e - 1; r >= 0 && 128 == (192 & t[r]);) r--;return r < 0 || 0 === r ? e : r + U[t[r]] > e ? r : e;},K = { 2: "need dictionary", 1: "stream end", 0: "", "-1": "file error", "-2": "stream error", "-3": "data error", "-4": "insufficient memory", "-5": "buffer error", "-6": "incompatible version" },H = function () {this.input = null, this.next_in = 0, this.avail_in = 0, this.total_in = 0, this.output = null, this.next_out = 0, this.avail_out = 0, this.total_out = 0, this.msg = "", this.state = null, this.data_type = 2, this.adler = 0;},W = function () {this.text = 0, this.time = 0, this.xflags = 0, this.os = 0, this.extra = null, this.extra_len = 0, this.name = "", this.comment = "", this.hcrc = 0, this.done = !1;},X = Object.prototype.toString,G = l.Z_NO_FLUSH,Y = l.Z_FINISH,Q = l.Z_OK,tt = l.Z_STREAM_END,et = l.Z_NEED_DICT,rt = l.Z_STREAM_ERROR,it = l.Z_DATA_ERROR,nt = l.Z_MEM_ERROR;function ot(t) {this.options = function (t) {for (var e = Array.prototype.slice.call(arguments, 1); e.length;) {var r = e.shift();if (r) {if ("object" != typeof r) throw new TypeError(r + "must be non-object");for (var i in r) V(r, i) && (t[i] = r[i]);}}return t;}({ chunkSize: 65536, windowBits: 15, to: "" }, t || {});var e = this.options;e.raw && e.windowBits >= 0 && e.windowBits < 16 && (e.windowBits = -e.windowBits, 0 === e.windowBits && (e.windowBits = -15)), !(e.windowBits >= 0 && e.windowBits < 16) || t && t.windowBits || (e.windowBits += 32), e.windowBits > 15 && e.windowBits < 48 && 0 == (15 & e.windowBits) && (e.windowBits |= 15), this.err = 0, this.msg = "", this.ended = !1, this.chunks = [], this.strm = new H(), this.strm.avail_out = 0;var r = C(this.strm, e.windowBits);if (r !== Q) throw new Error(K[r]);if (this.header = new W(), L(this.strm, this.header), e.dictionary && ("string" == typeof e.dictionary ? e.dictionary = function (t) {var e,r,i,n,o,s = t.length,a = 0;for (n = 0; n < s; n++) 55296 == (64512 & (r = t.charCodeAt(n))) && n + 1 < s && 56320 == (64512 & (i = t.charCodeAt(n + 1))) && (r = 65536 + (r - 55296 << 10) + (i - 56320), n++), a += r < 128 ? 1 : r < 2048 ? 2 : r < 65536 ? 3 : 4;for (e = new Uint8Array(a), o = 0, n = 0; o < a; n++) 55296 == (64512 & (r = t.charCodeAt(n))) && n + 1 < s && 56320 == (64512 & (i = t.charCodeAt(n + 1))) && (r = 65536 + (r - 55296 << 10) + (i - 56320), n++), r < 128 ? e[o++] = r : r < 2048 ? (e[o++] = 192 | r >>> 6, e[o++] = 128 | 63 & r) : r < 65536 ? (e[o++] = 224 | r >>> 12, e[o++] = 128 | r >>> 6 & 63, e[o++] = 128 | 63 & r) : (e[o++] = 240 | r >>> 18, e[o++] = 128 | r >>> 12 & 63, e[o++] = 128 | r >>> 6 & 63, e[o++] = 128 | 63 & r);return e;}(e.dictionary) : "[object ArrayBuffer]" === X.call(e.dictionary) && (e.dictionary = new Uint8Array(e.dictionary)), e.raw && (r = z(this.strm, e.dictionary)) !== Q)) throw new Error(K[r]);}function st(t, e) {var r = new ot(e);if (r.push(t), r.err) throw r.msg || K[r.err];return r.result;}ot.prototype.push = function (t, e) {var r,i,n,o = this.strm,s = this.options.chunkSize,a = this.options.dictionary;if (this.ended) return !1;for (i = e === ~~e ? e : !0 === e ? Y : G, "[object ArrayBuffer]" === X.call(t) ? o.input = new Uint8Array(t) : o.input = t, o.next_in = 0, o.avail_in = o.input.length;;) {for (0 === o.avail_out && (o.output = new Uint8Array(s), o.next_out = 0, o.avail_out = s), (r = M(o, i)) === et && a && ((r = z(o, a)) === Q ? r = M(o, i) : r === it && (r = et)); o.avail_in > 0 && r === tt && o.state.wrap > 0 && 0 !== t[o.next_in];) P(o), r = M(o, i);switch (r) {case rt:case it:case et:case nt:return this.onEnd(r), this.ended = !0, !1;}if (n = o.avail_out, o.next_out && (0 === o.avail_out || r === tt)) if ("string" === this.options.to) {var u = $(o.output, o.next_out),h = o.next_out - u,l = J(o.output, u);o.next_out = h, o.avail_out = s - h, h && o.output.set(o.output.subarray(u, u + h), 0), this.onData(l);} else this.onData(o.output.length === o.next_out ? o.output : o.output.subarray(0, o.next_out));if (r !== Q || 0 !== n) {if (r === tt) return r = D(this.strm), this.onEnd(r), this.ended = !0, !0;if (0 === o.avail_in) break;}}return !0;}, ot.prototype.onData = function (t) {this.chunks.push(t);}, ot.prototype.onEnd = function (t) {t === Q && ("string" === this.options.to ? this.result = this.chunks.join("") : this.result = function (t) {for (var e = 0, r = 0, i = t.length; r < i; r++) e += t[r].length;for (var n = new Uint8Array(e), o = 0, s = 0, a = t.length; o < a; o++) {var u = t[o];n.set(u, s), s += u.length;}return n;}(this.chunks)), this.chunks = [], this.err = t, this.msg = this.strm.msg;};var at = ot,ut = st,ht = function (t, e) {return (e = e || {}).raw = !0, st(t, e);},lt = st,ft = l,ct = { Inflate: at, inflate: ut, inflateRaw: ht, ungzip: lt, constants: ft };t.Inflate = at, t.constants = ft, t.default = ct, t.inflate = ut, t.inflateRaw = ht, t.ungzip = lt, Object.defineProperty(t, "__esModule", { value: !0 });}("object" == typeof r && void 0 !== e ? r : (i = "undefined" != typeof globalThis ? globalThis : i || self).pako = {});}, {}], 48: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.VideoEntity = void 0;var i = t(46),n = function (t) {var e, r;this.spec = t, this.version = "2.0.0", this.decodedImages = {}, this.version = t.ver, this.videoSize = { width: t.params.viewBoxWidth || 0, height: t.params.viewBoxHeight || 0 }, this.FPS = t.params.fps || 20, this.frames = t.params.frames || 0, this.sprites = null !== (r = null === (e = t.sprites) || void 0 === e ? void 0 : e.map(function (t) {return new i.SpriteEntity(t);})) && void 0 !== r ? r : [], this.audios = [];};r.VideoEntity = n;}, { 46: 46 }], 43: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.ProtoMovieEntity = r.proto = void 0;var i = t(1),n = JSON.parse('{"nested":{"com":{"nested":{"opensource":{"nested":{"svga":{"options":{"objc_class_prefix":"SVGAProto","java_package":"com.opensource.svgaplayer.proto"},"nested":{"MovieParams":{"fields":{"viewBoxWidth":{"type":"float","id":1},"viewBoxHeight":{"type":"float","id":2},"fps":{"type":"int32","id":3},"frames":{"type":"int32","id":4}}},"SpriteEntity":{"fields":{"imageKey":{"type":"string","id":1},"frames":{"rule":"repeated","type":"FrameEntity","id":2},"matteKey":{"type":"string","id":3}}},"AudioEntity":{"fields":{"audioKey":{"type":"string","id":1},"startFrame":{"type":"int32","id":2},"endFrame":{"type":"int32","id":3},"startTime":{"type":"int32","id":4},"totalTime":{"type":"int32","id":5}}},"Layout":{"fields":{"x":{"type":"float","id":1},"y":{"type":"float","id":2},"width":{"type":"float","id":3},"height":{"type":"float","id":4}}},"Transform":{"fields":{"a":{"type":"float","id":1},"b":{"type":"float","id":2},"c":{"type":"float","id":3},"d":{"type":"float","id":4},"tx":{"type":"float","id":5},"ty":{"type":"float","id":6}}},"ShapeEntity":{"oneofs":{"args":{"oneof":["shape","rect","ellipse"]}},"fields":{"type":{"type":"ShapeType","id":1},"shape":{"type":"ShapeArgs","id":2},"rect":{"type":"RectArgs","id":3},"ellipse":{"type":"EllipseArgs","id":4},"styles":{"type":"ShapeStyle","id":10},"transform":{"type":"Transform","id":11}},"nested":{"ShapeType":{"values":{"SHAPE":0,"RECT":1,"ELLIPSE":2,"KEEP":3}},"ShapeArgs":{"fields":{"d":{"type":"string","id":1}}},"RectArgs":{"fields":{"x":{"type":"float","id":1},"y":{"type":"float","id":2},"width":{"type":"float","id":3},"height":{"type":"float","id":4},"cornerRadius":{"type":"float","id":5}}},"EllipseArgs":{"fields":{"x":{"type":"float","id":1},"y":{"type":"float","id":2},"radiusX":{"type":"float","id":3},"radiusY":{"type":"float","id":4}}},"ShapeStyle":{"fields":{"fill":{"type":"RGBAColor","id":1},"stroke":{"type":"RGBAColor","id":2},"strokeWidth":{"type":"float","id":3},"lineCap":{"type":"LineCap","id":4},"lineJoin":{"type":"LineJoin","id":5},"miterLimit":{"type":"float","id":6},"lineDashI":{"type":"float","id":7},"lineDashII":{"type":"float","id":8},"lineDashIII":{"type":"float","id":9}},"nested":{"RGBAColor":{"fields":{"r":{"type":"float","id":1},"g":{"type":"float","id":2},"b":{"type":"float","id":3},"a":{"type":"float","id":4}}},"LineCap":{"values":{"LineCap_BUTT":0,"LineCap_ROUND":1,"LineCap_SQUARE":2}},"LineJoin":{"values":{"LineJoin_MITER":0,"LineJoin_ROUND":1,"LineJoin_BEVEL":2}}}}}},"FrameEntity":{"fields":{"alpha":{"type":"float","id":1},"layout":{"type":"Layout","id":2},"transform":{"type":"Transform","id":3},"clipPath":{"type":"string","id":4},"shapes":{"rule":"repeated","type":"ShapeEntity","id":5}}},"MovieEntity":{"fields":{"version":{"type":"string","id":1},"params":{"type":"MovieParams","id":2},"images":{"keyType":"string","type":"bytes","id":3},"sprites":{"rule":"repeated","type":"SpriteEntity","id":4},"audios":{"rule":"repeated","type":"AudioEntity","id":5}}}}}}}}}}}');r.proto = i.Root.fromJSON(n), r.ProtoMovieEntity = r.proto.lookupType("com.opensource.svga.MovieEntity");}, { 1: 1 }], 47: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.ValueAnimator = void 0;var i = function () {function t() {this.startValue = 0, this.endValue = 0, this.duration = 0, this.loops = 1, this.fillRule = 0, this.mRunning = !1, this.mStartTime = 0, this.mCurrentFrication = 0, this.mReverse = !1, this.onStart = function () {}, this.onUpdate = function (t) {}, this.onEnd = function () {};}return t.prototype.start = function (t) {this.doStart(!1, t);}, t.prototype.reverse = function (t) {this.doStart(!0, t);}, t.prototype.stop = function () {this.doStop();}, t.prototype.animatedValue = function () {return (this.endValue - this.startValue) * this.mCurrentFrication + this.startValue;}, t.prototype.doStart = function (e, r) {void 0 === r && (r = void 0), this.mReverse = e, this.mRunning = !0, this.mStartTime = t.currentTimeMillsecond(), r && (this.mStartTime -= e ? (1 - r / (this.endValue - this.startValue)) * this.duration : r / (this.endValue - this.startValue) * this.duration), this.mCurrentFrication = 0, this.onStart(), this.doFrame();}, t.prototype.doStop = function () {this.mRunning = !1;}, t.prototype.doFrame = function () {var e,r = this,i = function () {var e;r.mRunning && (r.doDeltaTime(t.currentTimeMillsecond() - r.mStartTime), null === (e = r.canvas) || void 0 === e || e.requestAnimationFrame(i));};null === (e = this.canvas) || void 0 === e || e.requestAnimationFrame(i);}, t.prototype.doDeltaTime = function (t) {var e = !1;t >= this.duration * this.loops ? (this.mCurrentFrication = 1 === this.fillRule ? 0 : 1, this.mRunning = !1, e = !0) : (this.mCurrentFrication = t % this.duration / this.duration, this.mReverse && (this.mCurrentFrication = 1 - this.mCurrentFrication)), this.onUpdate(this.animatedValue()), !1 === this.mRunning && e && this.onEnd();}, t.currentTimeMillsecond = function () {return "undefined" == typeof performance ? new Date().getTime() : performance.now();}, t;}();r.ValueAnimator = i;}, {}], 45: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.Renderer = void 0;var i = t(36),n = t(37),o = t(44),s = function () {function t(t, e, r) {this.videoItem = t, this.ctx = e, this.canvas = r, this._dynamicImage = {}, this._dynamicText = {};}return t.prototype.clear = function () {var t = this.ctx,e = { x: 0, y: 0, width: this.canvas.width, height: this.canvas.height };t.clearRect(e.x, e.y, e.width, e.height);}, t.prototype.drawFrame = function (t) {var e = this,r = this.ctx,i = { x: 0, y: 0, width: this.canvas.width, height: this.canvas.height };r.clearRect(i.x, i.y, i.width, i.height);var n = {},o = !1,s = this.videoItem.sprites;s.forEach(function (i, a) {var u, h;if (-1 != (null === (u = s[0].imageKey) || void 0 === u ? void 0 : u.indexOf(".matte"))) {if (-1 == (null === (h = i.imageKey) || void 0 === h ? void 0 : h.indexOf(".matte"))) {var l = s[a - 1];if (o && (!i.matteKey || 0 == i.matteKey.length || i.matteKey != l.matteKey)) {o = !1;var f = n[i.matteKey];r.globalCompositeOperation = "destination-in", e.drawSprite(f, t), r.globalCompositeOperation = "source-over", r.restore();}null == i.matteKey || null != l.matteKey && 0 != l.matteKey.length && l.matteKey == i.matteKey || (o = !0, r.save()), e.drawSprite(i, t), o && a == s.length - 1 && (f = n.get(i.matteKey), r.globalCompositeOperation = "destination-in", e.drawSprite(f, t), r.globalCompositeOperation = "source-over", r.restore());} else f[i.imageKey] = i;} else e.drawSprite(i, t);});}, t.prototype.drawSprite = function (t, e) {var r,s,a,u = this,h = t.frames[e];if (!(h.alpha < .05)) {var l = this.ctx;l.save(), this.globalTransform && l.transform(this.globalTransform.a, this.globalTransform.b, this.globalTransform.c, this.globalTransform.d, this.globalTransform.tx, this.globalTransform.ty), l.globalAlpha = h.alpha, l.transform(h.transform.a, h.transform.b, h.transform.c, h.transform.d, h.transform.tx, h.transform.ty);var f = null === (r = t.imageKey) || void 0 === r ? void 0 : r.replace(".matte", "");if (f) {var c = null !== (s = this._dynamicImage[f]) && void 0 !== s ? s : this.videoItem.decodedImages[f];void 0 !== h.maskPath && null !== h.maskPath && (h.maskPath._styles = void 0, this.drawBezier(h.maskPath), l.clip()), c && l.drawImage(c, 0, 0, c.width, c.height, 0, 0, h.layout.width, h.layout.height), h.shapes && h.shapes.forEach(function (t) {"shape" === t.type && t.pathArgs && t.pathArgs.d && u.drawBezier(new i.BezierPath(t.pathArgs.d, t.transform, t.styles)), "ellipse" === t.type && t.pathArgs && u.drawEllipse(new n.EllipsePath(parseFloat(t.pathArgs.x) || 0, parseFloat(t.pathArgs.y) || 0, parseFloat(t.pathArgs.radiusX) || 0, parseFloat(t.pathArgs.radiusY) || 0, t.transform, t.styles)), "rect" === t.type && t.pathArgs && u.drawRect(new o.RectPath(parseFloat(t.pathArgs.x) || 0, parseFloat(t.pathArgs.y) || 0, parseFloat(t.pathArgs.width) || 0, parseFloat(t.pathArgs.height) || 0, parseFloat(t.pathArgs.cornerRadius) || 0, t.transform, t.styles));});var d = this._dynamicText[f];if (void 0 !== d) {l.font = d.size + "px " + (null !== (a = d.family) && void 0 !== a ? a : "Arial");var p = l.measureText(d.text).width;l.fillStyle = d.color;var y = void 0 !== d.offset && void 0 !== d.offset.x ? isNaN(d.offset.x) ? 0 : d.offset.x : 0,m = void 0 !== d.offset && void 0 !== d.offset.y ? isNaN(d.offset.y) ? 0 : d.offset.y : 0;l.fillText(d.text, (h.layout.width - p) / 2 + y, h.layout.height / 2 + m);}l.restore();}}}, t.prototype.playAudio = function (t) {}, t.prototype.resetShapeStyles = function (t) {var e = this.ctx,r = t._styles;r && (r && r.stroke ? e.strokeStyle = "rgba(" + (255 * r.stroke[0]).toFixed(0) + ", " + (255 * r.stroke[1]).toFixed(0) + ", " + (255 * r.stroke[2]).toFixed(0) + ", " + r.stroke[3] + ")" : e.strokeStyle = "transparent", r && (e.lineWidth = r.strokeWidth || void 0, e.lineCap = r.lineCap || void 0, e.lineJoin = r.lineJoin || void 0, e.miterLimit = r.miterLimit || void 0), r && r.fill ? e.fillStyle = "rgba(" + (255 * r.fill[0]).toFixed(0) + ", " + (255 * r.fill[1]).toFixed(0) + ", " + (255 * r.fill[2]).toFixed(0) + ", " + r.fill[3] + ")" : e.fillStyle = "transparent", r && r.lineDash && e.setLineDash([r.lineDash[0], r.lineDash[1]], r.lineDash[2]));}, t.prototype.drawBezier = function (t) {var e = this,r = this.ctx;r.save(), this.resetShapeStyles(t), void 0 !== t._transform && null !== t._transform && r.transform(t._transform.a, t._transform.b, t._transform.c, t._transform.d, t._transform.tx, t._transform.ty);var i = { x: 0, y: 0, x1: 0, y1: 0, x2: 0, y2: 0 };r.beginPath(), t._d.replace(/([a-zA-Z])/g, "|||$1 ").replace(/,/g, " ").split("|||").forEach(function (t) {if (0 != t.length) {var r = t.substr(0, 1);if ("MLHVCSQRZmlhvcsqrz".indexOf(r) >= 0) {var n = t.substr(1).trim().split(" ");e.drawBezierElement(i, r, n);}}}), t._styles && t._styles.fill && r.fill(), t._styles && t._styles.stroke && r.stroke(), r.restore();}, t.prototype.drawBezierElement = function (t, e, r) {var i = this.ctx;switch (e) {case "M":t.x = Number(r[0]), t.y = Number(r[1]), i.moveTo(t.x, t.y);break;case "m":t.x += Number(r[0]), t.y += Number(r[1]), i.moveTo(t.x, t.y);break;case "L":t.x = Number(r[0]), t.y = Number(r[1]), i.lineTo(t.x, t.y);break;case "l":t.x += Number(r[0]), t.y += Number(r[1]), i.lineTo(t.x, t.y);break;case "H":t.x = Number(r[0]), i.lineTo(t.x, t.y);break;case "h":t.x += Number(r[0]), i.lineTo(t.x, t.y);break;case "V":t.y = Number(r[0]), i.lineTo(t.x, t.y);break;case "v":t.y += Number(r[0]), i.lineTo(t.x, t.y);break;case "C":t.x1 = Number(r[0]), t.y1 = Number(r[1]), t.x2 = Number(r[2]), t.y2 = Number(r[3]), t.x = Number(r[4]), t.y = Number(r[5]), i.bezierCurveTo(t.x1, t.y1, t.x2, t.y2, t.x, t.y);break;case "c":t.x1 = t.x + Number(r[0]), t.y1 = t.y + Number(r[1]), t.x2 = t.x + Number(r[2]), t.y2 = t.y + Number(r[3]), t.x += Number(r[4]), t.y += Number(r[5]), i.bezierCurveTo(t.x1, t.y1, t.x2, t.y2, t.x, t.y);break;case "S":t.x1 && t.y1 && t.x2 && t.y2 ? (t.x1 = t.x - t.x2 + t.x, t.y1 = t.y - t.y2 + t.y, t.x2 = Number(r[0]), t.y2 = Number(r[1]), t.x = Number(r[2]), t.y = Number(r[3]), i.bezierCurveTo(t.x1, t.y1, t.x2, t.y2, t.x, t.y)) : (t.x1 = Number(r[0]), t.y1 = Number(r[1]), t.x = Number(r[2]), t.y = Number(r[3]), i.quadraticCurveTo(t.x1, t.y1, t.x, t.y));break;case "s":t.x1 && t.y1 && t.x2 && t.y2 ? (t.x1 = t.x - t.x2 + t.x, t.y1 = t.y - t.y2 + t.y, t.x2 = t.x + Number(r[0]), t.y2 = t.y + Number(r[1]), t.x += Number(r[2]), t.y += Number(r[3]), i.bezierCurveTo(t.x1, t.y1, t.x2, t.y2, t.x, t.y)) : (t.x1 = t.x + Number(r[0]), t.y1 = t.y + Number(r[1]), t.x += Number(r[2]), t.y += Number(r[3]), i.quadraticCurveTo(t.x1, t.y1, t.x, t.y));break;case "Q":t.x1 = Number(r[0]), t.y1 = Number(r[1]), t.x = Number(r[2]), t.y = Number(r[3]), i.quadraticCurveTo(t.x1, t.y1, t.x, t.y);break;case "q":t.x1 = t.x + Number(r[0]), t.y1 = t.y + Number(r[1]), t.x += Number(r[2]), t.y += Number(r[3]), i.quadraticCurveTo(t.x1, t.y1, t.x, t.y);break;case "A":case "a":break;case "Z":case "z":i.closePath();}}, t.prototype.drawEllipse = function (t) {var e = this.ctx;e.save(), this.resetShapeStyles(t), void 0 !== t._transform && null !== t._transform && e.transform(t._transform.a, t._transform.b, t._transform.c, t._transform.d, t._transform.tx, t._transform.ty);var r = t._x - t._radiusX,i = t._y - t._radiusY,n = 2 * t._radiusX,o = 2 * t._radiusY,s = n / 2 * .5522848,a = o / 2 * .5522848,u = r + n,h = i + o,l = r + n / 2,f = i + o / 2;e.beginPath(), e.moveTo(r, f), e.bezierCurveTo(r, f - a, l - s, i, l, i), e.bezierCurveTo(l + s, i, u, f - a, u, f), e.bezierCurveTo(u, f + a, l + s, h, l, h), e.bezierCurveTo(l - s, h, r, f + a, r, f), t._styles && t._styles.fill && e.fill(), t._styles && t._styles.stroke && e.stroke(), e.restore();}, t.prototype.drawRect = function (t) {var e = this.ctx;e.save(), this.resetShapeStyles(t), void 0 !== t._transform && null !== t._transform && e.transform(t._transform.a, t._transform.b, t._transform.c, t._transform.d, t._transform.tx, t._transform.ty);var r = t._x,i = t._y,n = t._width,o = t._height,s = t._cornerRadius;n < 2 * s && (s = n / 2), o < 2 * s && (s = o / 2), e.beginPath(), e.moveTo(r + s, i), e.arcTo(r + n, i, r + n, i + o, s), e.arcTo(r + n, i + o, r, i + o, s), e.arcTo(r, i + o, r, i, s), e.arcTo(r, i, r + n, i, s), e.closePath(), t._styles && t._styles.fill && e.fill(), t._styles && t._styles.stroke && e.stroke(), e.restore();}, t;}();r.Renderer = s;}, { 36: 36, 37: 37, 44: 44 }], 44: [function (t, e, r) {"use strict";var i,n = this && this.__extends || (i = function (t, e) {return (i = Object.setPrototypeOf || { __proto__: [] } instanceof Array && function (t, e) {t.__proto__ = e;} || function (t, e) {for (var r in e) Object.prototype.hasOwnProperty.call(e, r) && (t[r] = e[r]);})(t, e);}, function (t, e) {if ("function" != typeof e && null !== e) throw new TypeError("Class extends value " + String(e) + " is not a constructor or null");function r() {this.constructor = t;}i(t, e), t.prototype = null === e ? Object.create(e) : (r.prototype = e.prototype, new r());});Object.defineProperty(r, "__esModule", { value: !0 }), r.RectPath = void 0;var o = function (t) {function e(e, r, i, n, o, s, a) {var u = t.call(this, "", s, a) || this;return u._x = e, u._y = r, u._width = i, u._height = n, u._cornerRadius = o, u._transform = s, u._styles = a, u;}return n(e, t), e;}(t(36).BezierPath);r.RectPath = o;}, { 36: 36 }], 46: [function (t, e, r) {"use strict";Object.defineProperty(r, "__esModule", { value: !0 }), r.SpriteEntity = void 0;var i = t(38),n = function (t) {var e, r;this.matteKey = t.matteKey, this.imageKey = t.imageKey, this.frames = null !== (r = null === (e = t.frames) || void 0 === e ? void 0 : e.map(function (t) {return new i.FrameEntity(t);})) && void 0 !== r ? r : [];};r.SpriteEntity = n;}, { 38: 38 }] }, {}, [39])(39);});
```

## File: package.json
```json
{
    "name": "joymew-mp2",
    "version": "1.0.0",
    "description": "",
    "main": "app.js",
    "dependencies": {},
    "devDependencies": {},
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "license": "ISC"
}
```

## File: pages/hotelReserve/couponDetail/couponDetail.js
```javascript
import { getToken, getLiveId, setLiveId } from '../../../utils/storage';
import { getCurrentTimestamp } from '../../../utils/date';
import  { PAGE_HOST } from '../../../assets/constant/host';
const app = getApp();

Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: ' 优惠详情',
    token: ''
  },
  onLoad: function (options) {
    if (options.liveId && options.token) {
      // 分享进入
      setLiveId(options.liveId);
      app.setH5Url(`${PAGE_HOST}?liveId=${options.liveId}&token=${options.token}&time=${getCurrentTimestamp()}#/couponDetail`);
    } else {
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/couponDetail`);
    }
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/couponDetail`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: ` 优惠详情(${app.globalData.activityTitle})`
    });
  },
  onShow: function () {
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: `/pages/couponDetail/couponDetail?liveId=${getLiveId()}&token=${getToken()}`,
    };
  },
})
```

## File: pages/hotelReserve/couponDetail/couponDetail.json
```json
{
    "navigationBarTitleText": "优惠详情"
  }
```

## File: pages/hotelReserve/couponDetail/couponDetail.ttml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/couponDetail/couponDetail.ttss
```
page {
    background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/hotelReserve/hotelDetail/hotelDetail.js
```javascript
import { getToken, getLiveId, setLiveId } from '../../../utils/storage';
import { getCurrentTimestamp } from '../../../utils/date';
import  { PAGE_HOST } from '../../../assets/constant/host';
const app = getApp();
Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: '宴会厅',
    token: ''
  },
  onLoad: function (options) {
    if (options.liveId && options.token) {
      // 分享进入
      setLiveId(options.liveId);
      app.setH5Url(`${PAGE_HOST}?liveId=${options.liveId}&token=${options.token}&time=${getCurrentTimestamp()}#/hotelDetail`);
    } else {
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/hotelDetail`);
    }
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/hotelDetail`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: `宴会厅(${app.globalData.activityTitle})`
    });
  },
  onShow: function () {
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: `/pages/hotelDetail/hotelDetail?liveId=${getLiveId()}&token=${getToken()}`,
    };
  },
})
```

## File: pages/hotelReserve/hotelDetail/hotelDetail.json
```json
{
    "navigationBarTitleText": "宴会厅"
  }
```

## File: pages/hotelReserve/hotelDetail/hotelDetail.ttml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/hotelDetail/hotelDetail.ttss
```
page {
    background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
  }
```

## File: pages/hotelReserve/hotelReserve.js
```javascript
import { getToken, getLiveId, setLiveId } from '../../utils/storage';
import { getCurrentTimestamp } from '../../utils/date';
import  { PAGE_HOST } from '../../assets/constant/host';
const app = getApp();

Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: '婚宴预定',
    token: ''
  },
  onLoad: function (options) {
    if (options.liveId && options.token) {
      // 分享进入
      setLiveId(options.liveId);
      app.setH5Url(`${PAGE_HOST}?liveId=${options.liveId}&token=${options.token}&time=${getCurrentTimestamp()}#/hotelReserve`);
    } else {
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/hotelReserve`);
    }
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/hotelReserve`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: `婚宴预定(${app.globalData.activityTitle})`
    });
  },
  onShow: function () {
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: `/pages/hotelReserve/hotelReserve?liveId=${getLiveId()}&token=${getToken()}`,
    };
  }
})
```

## File: pages/hotelReserve/hotelReserve.json
```json
{
  "navigationBarTitleText": "婚宴预定"
}
```

## File: pages/hotelReserve/hotelReserve.ttml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/hotelReserve.ttss
```
page {
  background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/hotelReserve/menuDetail/menuDetail.js
```javascript
import { getToken, getLiveId, setLiveId } from '../../../utils/storage';
import { getCurrentTimestamp } from '../../../utils/date';
import  { PAGE_HOST } from '../../../assets/constant/host';
const app = getApp();

Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: '婚宴菜单',
    token: ''
  },
  onLoad: function (options) {
    if (options.liveId && options.token) {
      // 分享进入
      setLiveId(options.liveId);
      app.setH5Url(`${PAGE_HOST}?liveId=${options.liveId}&token=${options.token}&time=${getCurrentTimestamp()}#/menuDetail`);
    } else {
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/menuDetail`);
    }
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/menuDetail`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: `婚宴菜单(${app.globalData.activityTitle})`
    });
  },
  onShow: function () {
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: `/pages/menuDetail/menuDetail?liveId=${getLiveId()}&token=${getToken()}`,
    };
  },
})
```

## File: pages/hotelReserve/menuDetail/menuDetail.json
```json
{
    "navigationBarTitleText": "婚宴菜单"
  }
```

## File: pages/hotelReserve/menuDetail/menuDetail.ttml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/menuDetail/menuDetail.ttss
```
page {
    background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/hotelReserve/packageDetail/packageDetail.js
```javascript
import { getToken, getLiveId, setLiveId } from '../../../utils/storage';
import { getCurrentTimestamp } from '../../../utils/date';
import  { PAGE_HOST } from '../../../assets/constant/host';
const app = getApp();

Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: '精品套餐',
    token: ''
  },
  onLoad: function (options) {
    if (options.liveId && options.token) {
      // 分享进入
      setLiveId(options.liveId);
      app.setH5Url(`${PAGE_HOST}?liveId=${options.liveId}&token=${options.token}&time=${getCurrentTimestamp()}#/packageDetail`);
    } else {
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/packageDetail`);
    }
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/packageDetail`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: `精品套餐(${app.globalData.activityTitle})`
    });
  },
  onShow: function () {
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: `/pages/packageDetail/packageDetail?liveId=${getLiveId()}&token=${getToken()}`,
    };
  },
})
```

## File: pages/hotelReserve/packageDetail/packageDetail.json
```json
{
    "navigationBarTitleText": "精品套餐"
  }
```

## File: pages/hotelReserve/packageDetail/packageDetail.ttml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/packageDetail/packageDetail.ttss
```
page {
    background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/index/index.js
```javascript
import {
  getMsgInfo,
  sendChatMessage
} from '../../api/index/index';
import {
  newDateTransform,
  getCurrentDate
} from '../../utils/date';
import {
  getRandom,
  showWxToast
} from '../../utils/index';
import {
  getUserInfo
} from '../../utils/storage';

const WISH = [
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
  '新婚快乐！我们一起摇红包、做game、中大奖、沾喜气，嗨起来！'
];

const QUICKWISH = [
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
  'everybaby  high 起来！'
];

Page({
  data: {
    autoFocus: false,
    sendDanmuVisible: false,
    message: '',
    quickWishes: [],
    defaultWishes: [],
    chatList: [],
    chatTop: 0,
    scrollTop: 0
  },
  onLoad: function () {
    this.initWishes();
    this.requestMsgInfo();
  },
  sendDanmu() {
    sendChatMessage(this.data.message).then((res) => {
      console.log(res);
      const {
        nickName,
        avatarUrl
      } = getUserInfo();
      const tmpChatList = this.data.chatList;
      tmpChatList.push({
        miaoContent: this.data.message,
        sendTime: getCurrentDate(),
        miaoName: nickName,
        miaoTxUrl: avatarUrl
      });
      this.setData({
        chatList: tmpChatList,
        message: '',
        sendDanmuVisible: false,
        scrollTop: tmpChatList.length * 200
      });
    });
  },
  initWishes() {
    // WISH
    const tmpWishLen = WISH.length;
    const tmpWish = [];
    for (let i = 0; i < 5; i += 1) {
      tmpWish.push(WISH[getRandom(0, tmpWishLen)]);
    }
    const tmpQuickWishLen = QUICKWISH.length;
    const tmpQuickWish = [];
    for (let i = 0; i < 3; i += 1) {
      tmpQuickWish.push(QUICKWISH[getRandom(0, tmpQuickWishLen)]);
    }
    this.setData({
      defaultWishes: tmpWish,
      quickWishes: tmpQuickWish
    });
  },
  handleInput(e) {
    console.log(e.detail.value);
    this.setData({
      message: e.detail.value
    });
  },
  chooseDefaultWish(e) {
    console.log(e.currentTarget.dataset.index);
    this.setData({
      message: this.data.defaultWishes[e.currentTarget.dataset.index],
      autoFocus: true
    });
  },
  showSendDanmu() {
    this.setData({
      sendDanmuVisible: true,
      autoFocus: true
    });
  },
  closeSendDanmu() {
    this.setData({
      sendDanmuVisible: false
    });
  },
  requestMsgInfo() {
    getMsgInfo().then((res) => {
      if (
        res &&
        res.data &&
        res.data.chat_list &&
        res.data.chat_list.length > 0) {
        const list = res.data.chat_list.
        filter((item) => !item.miaoLiwuId).
        map((item) => ({
          ...item,
          sendTime: newDateTransform(item.sendTime, 16)
        }));
        console.log(list);
        this.setData({
          chatList: list,
          scrollTop: list.length * 200
        });
      }
    });
  },
  chooseQuickWish(e) {
    console.log(e.currentTarget.dataset.index);
    let tmpQuickWish = this.data.quickWishes;
    sendChatMessage(tmpQuickWish[e.currentTarget.dataset.index]).then((res) => {
      console.log(res);
      const {
        nickName,
        avatarUrl
      } = getUserInfo();
      const tmpChatList = this.data.chatList;
      tmpChatList.push({
        miaoContent: tmpQuickWish[e.currentTarget.dataset.index],
        sendTime: getCurrentDate(),
        miaoName: nickName,
        miaoTxUrl: avatarUrl
      });
      tmpQuickWish.splice(e.currentTarget.dataset.index, 1);
      this.setData({
        chatList: tmpChatList,
        quickWishes: tmpQuickWish,
        scrollTop: tmpChatList.length * 200
      });
    });
  }
});
```

## File: pages/index/index.json
```json
{"navigationBarTitleText":" 嗨喵互动","backgroundColor":"#305068","disableScroll":false}
```

## File: pages/index/index.ttml
```
<view class="index-wrap">
    <view class="bg"></view>
    <view class="chatArea">
        <view class="weddingChatList">
            <scroll-view class="newsContainer" scroll-y="true" style="height:502rpx" scrollTop="{{scrollTop}}">
                <view class="messageItem" tt:for="{{chatList}}" tt:key="index">
                    <view class="top">
                        <image class="headImg" src="{{item.miaoTxUrl}}"></image>
                        <view class="nickname">{{item.miaoName}}</view>
                    </view>
                    <view class="content">
                        <view class="common">{{item.miaoContent}}</view>
                    </view>
                    <view class="bottom">
                        <view class="date">{{item.sendTime}}</view>
                    </view>
                </view>
            </scroll-view>
        </view>
    </view>
    <view class="bottomArea">
        <view class="wedding">
            <view class="quickWish">
                <view class="quickWishCt">
                    <view class="item" tt:for="{{quickWishes}}" tt:key="index" bindtap="chooseQuickWish" data-index="{{index}}">
                        <view class="itemCt">
                            {{item}}
                        </view>
                    </view>
                </view>
            </view>
            <view class="bottomMain {{sendDanmuVisible ? 'show' : ''}}">
                <view class="bottomEmptyArea" bindtap="closeSendDanmu" tt:if="{{sendDanmuVisible}}"></view>
                <view class="default" tt:if="{{sendDanmuVisible}}">
                    <view class="defaultCt">
                        <view class="item" tt:for="{{defaultWishes}}" data-index="{{index}}" tt:key="index" bindtap="chooseDefaultWish">
                            <view class="itemCt">{{item}}</view>
                        </view>
                    </view>
                </view>
                <view class="iptArea">
                    <image src="/assets/image/hd2/messageIcon.png" class="msgIcon"></image>
                    <view class="inputBoxVitual" tt:if="{{!sendDanmuVisible}}" bindtap="showSendDanmu">送上祝福...</view>
                    <input class="inputBox" placeholder="送上祝福..." bindinput="handleInput" value="{{message}}" tt:if="{{sendDanmuVisible}}" focus="{{autoFocus}}" placeholder-style="font-size:16px" disabled />
                    <view class="sendBtn {{message ? 'active' : ''}}" tt:if="{{sendDanmuVisible}}" bindtap="sendDanmu">
                        发送</view>
                </view>
            </view>
        </view>
    </view>
</view>
```

## File: pages/index/index.ttss
```
view {
    box-sizing: border-box;
}
.index-wrap {
    position: relative;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
}
.bg {
    background-image: url('https://ustatic.hudongmiao.com/h5/bg.png');
    background-size: 100% 100%;
    position: absolute;
    width: 100%;
    height: 100%;
    background-size: cover;
    background-position: 50%;
    z-index: 0;
}

.chatArea {
    position: absolute;
    width: 530rpx;
    height: 502rpx;
    bottom: 290rpx;
    color: #fff;
    z-index: 0;
}
.chatArea .weddingChatList {
    position: absolute;
    width: 100%;
    height: 100%;
    padding-left: 20rpx;
}
.messageItem {
    background-color: rgba(0, 0, 0, 0.2);
    border-radius: 0px 32rpx 32rpx 32rpx;
    color: #ffffff;
    padding: 20rpx 18rpx;
    position: relative;
    width: 490rpx;
    margin: 18rpx 0;
}
.messageItem .top {
    display: flex;
    align-items: center;
}
.messageItem .top .headImg{
    width: 40rpx;
    height: 40rpx;
    border-radius: 50%;
}
.messageItem .top .nickname{
    font-size: 20rpx;
    font-weight: 300;
    color: #ffffff;
    margin-left: 10rpx;
}
.messageItem .content {
    font-size: 28rpx;
    margin-top: 18rpx;
}
.messageItem .content .common {
    margin-top: 23rpx;
}
.messageItem .bottom {
    justify-content: space-between;
    margin-top: 23rpx;
    display: flex;
    align-items: center;
}
.messageItem .bottom .date{
    font-size: 20rpx;
    font-weight: 400;
    color: rgba(255, 255, 255, 0.4);
}

.bottomArea {
    width: 100%;
    height: 140rpx;
    position: absolute;
    bottom: 0;
    z-index: 2;
}
.bottomArea .wedding .quickWish{
    height: 69rpx;
    width: 100%;
    position: absolute;
    left: 0;
    top: -69rpx;
    border-radius: 24rpx 24rpx 0 0;
    overflow-x: scroll;
}
.bottomArea .wedding .quickWish .quickWishCt {
    white-space: nowrap;
}
.bottomArea .wedding .quickWish .quickWishCt .item{
    font-size: 20rpx;
    color: #ffffff;
    align-items: center;
    margin: 0px 20rpx;
    display: inline-block;
    background: linear-gradient(135deg, #ee9bff, #5560f5);
    border-radius: 27rpx;
    padding: 4rpx;
}
.bottomArea .wedding .quickWish .quickWishCt .item .itemCt{
    border-radius: 27rpx;
    background: linear-gradient(135deg, #183a6a, #1351a3);
    padding: 4rpx 12rpx;
}
.bottomArea .wedding .bottomMain{
    width: 100%;
    padding: 0 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.bottomArea .wedding .bottomMain .bottomEmptyArea {
    position: absolute;
    width: 100vw;
    height: 100vh;
    top: -100vh;
}
.bottomArea .wedding .bottomMain.show {
    flex-direction: column;
    justify-content: center;
    background: linear-gradient(135deg, #183a6a, #1351a3);
    height: 260rpx;
    position: absolute;
    bottom: 0;
    border-top-left-radius: 20rpx;
    border-top-right-radius: 20rpx;
}
.bottomArea .wedding .bottomMain .iptArea {
    width: 292rpx;
    height: 72rpx;
    background: rgba(0, 0, 0, 0.19);
    border-radius: 36rpx;
    padding-left: 24rpx;
    padding-right: 14rpx;
    position: relative;
    display: flex;
    align-items: center;
}
.bottomArea .wedding .bottomMain .iptArea::after {
    content: '';
    display: block;
    width: 2rpx;
    height: 32rpx;
    background-color: rgba(251, 213, 111, 0.3);
    position: absolute;
    left: 68rpx;
}
.bottomArea .wedding .bottomMain .iptArea .msgIcon{
    width: 36rpx;
    height: 36rpx;
}
.bottomArea .wedding .bottomMain .iptArea .inputBox{
    width: 212rpx;
    height: 72rpx;
    background-color: transparent;
    border-radius: 36rpx;
    border: none;
    font-size: 20rpx;
    padding: 0 10rpx 0 10rpx;
    color: #fff;
    position: absolute;
    left: 80rpx;
    outline: none;
    box-sizing: border-box;
}
.bottomArea .wedding .bottomMain .iptArea .inputBoxVitual{
    width: 212rpx;
    height: 72rpx;
    background-color: transparent;
    border-radius: 36rpx;
    border: none;
    font-size: 20rpx;
    padding: 0 10rpx 0 10rpx;
    color: #fff;
    position: absolute;
    left: 80rpx;
    outline: none;
    box-sizing: border-box;
    display: flex;
    align-items: center;
}
.bottomArea .wedding .bottomMain .iptArea .sendBtn {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100rpx;
    height: 45rpx;
    font-size: 24rpx;
    color: rgba(255, 255, 255, 0.6);
    background-color: rgba(0, 0, 0, 0.6);
    position: absolute;
    right: 10rpx;
    border-radius: 34rpx;
}
.bottomArea .wedding .bottomMain .iptArea .sendBtn.active {
    background-color: #e4156a;
    color: #fff;
}
.bottomArea .wedding .bottomMain .default {
    height: 90rpx;
    width: 100%;
    border-radius: 24rpx 24rpx 0 0;
}
.bottomArea .wedding .bottomMain .default .defaultCt{
    white-space: nowrap;
    overflow-x: scroll;
}
.bottomArea .wedding .bottomMain .default .item{
    font-size: 20rpx;
    color: #ffffff;
    align-items: center;
    margin: 0rpx 20rpx;
    display: inline-block;
    background: linear-gradient(135deg, #ee9bff, #5560f5);
    border-radius: 27rpx;
    padding: 4rpx;
}
.bottomArea .wedding .bottomMain .default .item .itemCt{
    border-radius: 27rpx;
    background: linear-gradient(135deg, #183a6a, #1351a3);
    padding: 4rpx 12rpx;
}
/* bottomMain active状态下的子元素样式 */
.bottomArea .wedding .bottomMain.show .iptArea {
    width: 700rpx;
}
.bottomArea .wedding .bottomMain.show .iptArea::after {
    display: none;
}
.bottomArea .wedding .bottomMain.show .iptArea .msgIcon{
   display: none;
}
.bottomArea .wedding .bottomMain.show .iptArea .inputBox{
    width: 563rpx;
    left: 28rpx;
 }
```

## File: pages/joymewIndex/joymewIndex.js
```javascript
import {
  getSignInState,
  signIn,
  getLiveInfo
} from '../../api/index/index';
import {
  checkFollowState,
  followAwemeUser
} from '../../api/login';
import {
  getToken,
  setLiveId,
  getLiveId,
  getUserInfo,
  clearStorage,
  setToken,
  setUserInfo,
  setIsHlt,
  getIsHlt,
} from '../../utils/storage';
import {
  getCurrentTimestamp,
  dateCompare
} from '../../utils/date';
import defaultContent from '../../assets/constant/default';
import {
  getRandom,
  showWxToast,
  timeoutTask
} from '../../utils/index';
import {
  PAGE_HOST
} from '../../assets/constant/host';

const app = getApp();
// 观察者模式 监听活动信息是否获取到
const Observer = {};
// 作为应付审核的liveId token
const LIVEID = 'afb94fa7142f43adb3c5dc8bc61d2d9b';
const DEFAULTAVATOR =
  'https://ustatic.joymew.com/joymewScreen/defaultHeadImg2.png';
const EXAMINETOKEN =
  'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHQiOjE3MDQ3MDY2NjY3MzMsInVpZCI6ImY2MGNjMWE4MmJiMzQ4Njk4MjYwNTU4MjBjMmYwY2M3IiwiaWF0IjoxNzA0MzU2MjA4ODc3fQ.ZfS0A_Qqmil-HaSMfn-usFB433qkLPJVM50rIW0SXmQ';
Page({
  data: {
    sceneType: '', // 场景类型 0: 婚礼版 1:企业版 2:生日版
    role: '', // 亲友类型 1:男方亲友 2:女方亲友 ''：不选
    userName: '', // 姓名
    wish: '', // 祝福语
    userPhone: '', // 手机号
    activityTitle: '',
    liveId: '',
    needAuth: false, // 是否需要授权登录
    isOverdate: false, // 活动是否过期
    isValid: true, // 活动是否有效
    customSignWishList: [], // 自定义签到语列表
    isForcePhone: false, // 企业版是否强制获取手机号
    isExamine: false, // 是否是isExamine live
    userIdParam: '', // 二维码中携带的userId参数
    miaoShopId: '', // 是否是婚礼堂 取值5(婚礼堂)、''(非婚礼堂的普通用户)
    isHlt: '', // 定位具体的某个婚礼堂 取值39(云境)、x(xxx婚礼堂)、common ''(非婚礼堂的普通用户)
    followAwemeState: 2, // 是否关注小程序所绑定的抖音号 0:未关注 1:已关注 2:功能不可用
    checkFollowStateFuncResult: '', // ''表示未执行该方法 '1'表示成功获取到关注状态 '0'表示未获取到关注状态
  },
  onLoad: function (options) {
    console.log('options:', options);
    let that = this;
    let tmpLiveId = '';
    let stLiveId = getLiveId(); // 缓存中的liveId

    // 观察者模式 监听活动信息是否获取到
    Object.defineProperty(Observer, 'liveInfoGetted', {
      configurable: true,
      enumerable: true,
      get() {
        return false;
      },
      set(val) {
        if (val) {
          console.log('***liveInfoGetted***');
          // 活动信息获取到后 执行主逻辑
          that.mainLogic();
        }
      }
    });
    // 获取liveId
    if (options.q) {
      // 扫码进入
      this.decodeQrcodeParam(decodeURIComponent(options.q));
    } else if (options.liveId) {
      if (!this.validateExamineLive(options.liveId)) {
        this.setExamine();
        return;
      }
      // 分享带参进入
      tmpLiveId = options.liveId;
      this.setData({
        liveId: tmpLiveId
      });
    } else if (stLiveId) {
      if (!this.validateExamineLive(stLiveId)) {
        this.setExamine();
        return;
      }

      // 直接进入
      this.setData({
        liveId: stLiveId
      });
    } else {
      this.setExamine();
    }
    this.checkClearStorage(options.liveId, stLiveId);
    setLiveId(this.data.liveId);
  },

  onShow: function () {
    if (this.data.needAuth) {
      return;
    }
    this.getLiveInfoDirect();
  },
  onShareAppMessage: function () {
    let tmpShareObj;
    if (this.data.sceneType === '0') {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
        imageUrl: '/assets/image/shareCard.png'
      };
    } else if (this.data.sceneType === '1') {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
        imageUrl: '/assets/image/shareCard-annualMeeting01.png'
      };
    } else if (this.data.sceneType === '2') {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
        imageUrl: '/assets/image/birthBg02.png'
      };
    } else {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId
      };
    }
    console.log('***onShareAppMessage***');
    console.log(tmpShareObj);
    return tmpShareObj;
  },
  mainLogic() {
    console.log('***执行主逻辑***');
    const stToken = getToken();
    const stUserInfo = getUserInfo();
    if (
      !stToken ||
      !stUserInfo.nickName ||
      !stUserInfo.avatarUrl ||
      stUserInfo.avatarUrl === DEFAULTAVATOR && this.data.liveId !== LIVEID) {
      this.setData({
        needAuth: true
      });
      return;
    }
    // 初始化用户信息
    app.setUserInfo();
    this.setData({
      userName: app.globalData.userInfo.nickName
    });
    // 判断是否签到
    getSignInState().
    then((res) => {
      console.log('***签到状态***');
      console.log(res);
      if (res.data.isNeddReload === '1') {
        throw '401';
      }
      if (this.data.isOverdate) {
        showWxToast('活动已结束!');
        return;
      }
      const isSign = res.data.qian_dao_le_me;
      if (isSign && !this.data.isExamine) {
        console.log('***不需要签到***');
        // 不需要签到
        this.toLive();
      } else if (!isSign && !this.data.isExamine) {
        // 检查是否关注抖音号
        this.checkFollowAwemeStateLogic();
      }
    }).
    catch((err) => {
      console.log(err);
      // token过期需要授权登录
      this.setData({
        needAuth: true
      });
    });
  },
  // 判断是否签到--->签到逻辑
  sign(e) {
    console.log(e);
    this.setData({
      userName: e.detail.userName,
      wish: e.detail.wish,
      role: e.detail.role || '',
      userPhone: e.detail.userPhone || '',
      birthDate: e.detail.birthDate || '',
      gender: e.detail.gender || ''
    });
    if (this.data.isOverdate) {
      showWxToast('活动已结束!');
      return;
    }
    if (!this.data.isValid) {
      showWxToast('活动信息错误，请重新进入!');
      return;
    }
    if (this.data.followAwemeState === 0 && !this.data.isExamine) {
      followAwemeUser(app.globalData.dy_bind_id).then((res) => {
        console.log(res);
        this.setData({
          followAwemeState: 1
        });
        this.signLogic();
      }).catch((err) => {
        console.log(err);
        const {
          errNo
        } = err;
        this.handleFollowErrNo(errNo);
      });
    } else if (this.data.followAwemeState === 1 && !this.data.isExamine) {
      showWxToast('关注成功!可以进入互动啦!');
      this.signLogic();
    } else if (this.data.followAwemeState === 2 && !this.data.isExamine) {
      showWxToast(`checkFollowStateFuncResult:${this.data.checkFollowStateFuncResult}`);
      this.checkFollowAwemeStateLogic();
    } else if (this.data.isExamine) {
      this.signLogic();
    }
  },
  // 跳转live页面
  toLive() {
    console.log('***app globalData中的数据***');
    console.log(app.globalData);
    console.log('***跳转live***');
    if (this.data.isExamine) {
      tt.navigateTo({
        url: '/pages/index/index'
      });
      return;
    }
    app.setUserPhone(this.data.userPhone);
    // h5是否提示过的标识 缓存中有值说明提示过 没有值说明没有提示过
    const tmpIsHlt = getIsHlt();
    const staicUrl = `${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}`;
    let variableUrl = '';
    if (tmpIsHlt) {
      variableUrl += `&isHlt=${tmpIsHlt}`;
    }
    if (app.globalData.userPhone) {
      variableUrl += `&userPhone=${app.globalData.userPhone}`;
    }
    if (variableUrl) {
      app.setH5Url(staicUrl + variableUrl);
      console.log(staicUrl + variableUrl);
    } else {
      app.setH5Url(staicUrl);
      console.log(staicUrl);
    }
    tt.redirectTo({
      url: '/pages/live/live'
    });
  },
  // 刷新祝福语
  refreshWish() {
    // 设置自定义签到语
    let customSignLen = this.data.customSignWishList.length;
    if (customSignLen > 0) {
      this.setData({
        wish: this.data.customSignWishList[getRandom(0, customSignLen)]
      });
      return;
    }
    // 设置默认祝福语
    if (this.data.sceneType === '0') {
      this.setData({
        wish: defaultContent.wishesWedding[getRandom(0, 20)]
      });
    } else if (this.data.sceneType === '1') {
      this.setData({
        wish: defaultContent.wishesAnnualMeeting[getRandom(0, 20)]
      });
    } else if (this.data.sceneType === '2') {
      this.setData({
        wish: defaultContent.wishesBirth[getRandom(0, 14)]
      });
    } else if (this.data.sceneType === '21') {
      this.setData({
        wish: defaultContent.wishesBBY[getRandom(0, 10)]
      });
    } else if (this.data.sceneType === '22') {
      this.setData({
        wish: defaultContent.wishesSY[getRandom(0, 8)]
      });
    } else if (this.data.sceneType === '23') {
      this.setData({
        wish: defaultContent.wishesCRL[getRandom(0, 9)]
      });
    } else if (this.data.sceneType === '24') {
      this.setData({
        wish: defaultContent.wishesBLY[getRandom(0, 6)]
      });
    } else if (this.data.sceneType === '25') {
      this.setData({
        wish: defaultContent.wishesMYY[getRandom(0, 8)]
      });
    } else if (this.data.sceneType === '41') {
      this.setData({
        wish: defaultContent.wishesBYDL[getRandom(0, 31)]
      });
    } else if (this.data.sceneType === '42') {
      this.setData({
        wish: defaultContent.wishesXSY[getRandom(0, 25)]
      });
    } else if (this.data.sceneType === '43') {
      this.setData({
        wish: defaultContent.wishesJBTM[getRandom(0, 24)]
      });
    } else if (this.data.sceneType === '51') {
      this.setData({
        wish: defaultContent.wishesTXH[getRandom(0, 50)]
      });
    } else if (this.data.sceneType === '52') {
      this.setData({
        wish: defaultContent.wishesQQY[getRandom(0, 8)]
      });
    } else if (this.data.sceneType === '53') {
      this.setData({
        wish: defaultContent.wishesHX[getRandom(0, 7)]
      });
    }
  },
  // 授权登录成功后的回调
  handleAuthSuccess(e) {
    // 用户名赋值
    console.log('***用户名赋值 关闭授权框***');
    this.setData({
      userName: app.globalData.userInfo.nickName,
      needAuth: false
    });
    // 获取签到状态
    getSignInState().
    then((res) => {
      console.log('***handleAuthSuccess 获取签到状态***');
      console.log(res);
      if (this.data.isOverdate) {
        showWxToast('活动已结束!');
        timeoutTask(() => {
          tt.navigateTo({
            url: `/pages/estimate/estimate?splid=${this.data.liveId}`
          });
        }, 1500);
        return;
      }
      if (res.data.qian_dao_le_me) {
        // 不需要签到
        this.toLive();
      } else {
        this.checkFollowAwemeStateLogic();
      }
    }).
    catch((err) => {
      console.log(err);
      // token过期需要重新授权登录
      if (err === '401') {
        this.setData({
          needAuth: true
        });
      }
    });
  },
  // 授权登录失败的回调
  handleAuthFail() {
    clearStorage();
    this.setData({
      needAuth: false
    });
  },
  validateExamineLive(pLiveId) {
    let tFlag = true;
    if (pLiveId === LIVEID) {
      tFlag = false;
    }
    return tFlag;
  },
  setExamine() {
    setLiveId(LIVEID);
    setToken(EXAMINETOKEN);
    setUserInfo({
      nickName: '默认用户',
      avatarUrl: DEFAULTAVATOR
    });
    this.setData({
      liveId: LIVEID,
      isExamine: true
    });
  },
  getLiveInfoDirect() {
    getLiveInfo().then((res) => {
      console.log('活动信息:', res);
      if (res && res.data && res.data.splid) {
        this.setData({
          activityTitle: res.data.splid.theme,
          sceneType: res.data.splid.scenario
        });
        app.globalData.sceneType = this.data.sceneType;
        app.globalData.activityTitle = this.data.activityTitle;
        // 设置扭一扭奖项列表
        const tmpNynPrizeArray = [];
        const tmpNynList = res.data.nynList.split(',');
        for (let i = 0; i < tmpNynList.length; i += 1) {
          if (tmpNynList[i] === '0') {
            tmpNynPrizeArray.push({
              desc: '谢谢参与',
              endIndex: i
            });
          } else if (tmpNynList[i] !== '-1') {
            tmpNynPrizeArray.push({
              desc: tmpNynList[i] + '元',
              endIndex: i
            });
          }
        }
        app.globalData.nynList = tmpNynPrizeArray;
        // 设置幸运小转盘奖项列表
        app.globalData.luckyWheelPrizeItemList = res.data.luckySmallList.split(',');
        if (res.data.signWish && res.data.signWish.length > 0) {
          let tmpSignWishList = res.data.signWish.map((item) => {
            return item.bless_str;
          });
          this.setData({
            customSignWishList: tmpSignWishList
          });
        }
        // 设置默认祝福语
        this.refreshWish();
        // 是否强制获取手机号
        this.setData({
          isForcePhone: res.data.splid.forcephone === '1'
        });

        if (res.data.siyiInfo) {
          // 判断是否是婚礼堂用户
          if (res.data.siyiInfo.high_privilege === 5) {
            this.setData({
              miaoShopId: '5',
            });
            // 婚礼堂用户再区分：云境或其他酒店用户
            if (res.data.siyiInfo.tql_store_id === '39') {
              // 云境
              setIsHlt('39');
              this.setData({
                isHlt: '39',
              });
            } else if (res.data.siyiInfo.tql_store_id) {
              // 其他酒店用户
              setIsHlt(res.data.siyiInfo.tql_store_id);
              this.setData({
                isHlt: res.data.siyiInfo.tql_store_id,
              });
            } else {
              // 特殊情况 无酒店id
              setIsHlt('common');
              this.setData({
                isHlt: '',
              });
            }
          } else {
            this.setData({
              miaoShopId: '',
              isHlt: '',
            });
            setIsHlt('common');
          }
        }

        // 活动是否过期
        if (
          dateCompare(res.data.splid.using_date) ||
          res.data.splid.is_end_wedding === '1') {
          this.setData({
            isOverdate: true
          });
        }
        // 抖音appId
        if (res.data.siyiInfo.dy_appid) {
          app.setDyappid(res.data.siyiInfo.dy_appid);
        }
        // 绑定的抖音号
        if (res.data.siyiInfo.dy_bind_id) {
          app.setDyBindId(res.data.siyiInfo.dy_bind_id);
        }

        // 通知活动信息已经获取到可以执行主逻辑了
        Observer.liveInfoGetted = true;
      } else {
        showWxToast('活动信息获取错误，请重新进入!');
        this.setData({
          isValid: false
        });
      }
    });
  },
  decodeQrcodeParam(qrcodeParamStr) {
    const paramKey = qrcodeParamStr.split('?')[1].split('=')[0];
    const paramVal = qrcodeParamStr.split('?')[1].split('=')[1];
    if (!paramKey || !paramVal) {
      showWxToast('抖音版本过低!');
      return;
    }
    if (!this.validateExamineLive(paramVal)) {
      this.setExamine();
    }
    this.setData({
      liveId: paramVal
    });
  },
  signLogic() {
    getSignInState().
    then((res) => {
      console.log('***sign 获取签到状态***');
      console.log(res);
      return res.data.qian_dao_le_me;
    }).
    then((res2) => {
      console.log(res2);
      if (!res2) {
        // 需要签到
        return signIn({
          wish: this.data.wish,
          name: this.data.userName,
          role: this.data.role,
          userPhone: this.data.isForcePhone || this.data.miaoShopId ?
            this.data.userPhone : '',
          birthDate: this.data.birthDate,
          gender: this.data.gender
        });
      } else {
        // 不需要签到
        this.toLive();
      }
    }).
    then((res3) => {
      if (res3 && res3.success) {
        console.log('***签到接口返回***');
        console.log(res3);
        this.toLive();
      }
    }).
    catch((err) => {
      console.log(err);
      // token过期需要重新授权登录
      if (err === '401') {
        this.setData({
          needAuth: true
        });
      }
    });
  },
  showAuth() {
    this.setData({
      needAuth: true
    });
  },
  checkFollowAwemeStateLogic() {
    checkFollowState(app.globalData.dy_bind_id).then((res) => {
      console.log('抖音号关注情况:', res);
      this.setData({
        followAwemeState: res.hasFollowed ? 1 : 0,
        checkFollowStateFuncResult: '1'
      });
    }).catch((err) => {
      console.log(err);
      this.setData({
        followAwemeState: 2,
        checkFollowStateFuncResult: '0'
      });
    });
    // 强制弹出关注弹窗
    //  this.setData({
    //   followAwemeState: 0,
    //   checkFollowStateFuncResult: '1'
    // });
  },
  handleFollowErrNo(errNo) {
    console.log('关注抖音号失败的状态码:', errNo);
    if (errNo === 10301 || errNo === 21101 || errNo === 21103 || errNo === 21104) {
      // 系统的原因导致关注失败
      this.setData({
        followAwemeState: 2
      });
      showWxToast(`异常${errNo},请重新进入小程序!`);
    } else if (errNo === 10601) {
      showWxToast('请先登录抖音号!');
    } else if (errNo === 10502) {
      // 用户取消操作
      this.setData({
        followAwemeState: 0
      });
    } else {
      showWxToast('未知情况,请重新进入小程序!');
    }
  },
  checkClearStorage(liveId, storageLiveId) {
    if (storageLiveId && liveId && LIVEID !== storageLiveId && liveId !== storageLiveId) {
      tt.clearStorageSync();
    }
  }
});
```

## File: pages/joymewIndex/joymewIndex.json
```json
{
    "navigationBarTitleText": " 嗨喵悦动",
    "usingComponents": {
        "signNew": "../../components/sign/sign",
        "signCustom": "../../components/signCustom/signCustom",
        "authDialogNew": "../../components/authDialogNew/authDialogNew",
        "signLz": "../../components/signLz/signLz"
    },
    "disableScroll": true
}
```

## File: pages/joymewIndex/joymewIndex.ttml
```
<view class="joymewIndex">
    <!-- 云境定制签到 -->
    <signCustom sceneType="{{sceneType}}" activityTitle="{{activityTitle}}" userNameProp="{{userName}}"
        isExamine="{{isExamine}}" wishProp="{{wish}}" bind:refreshWishEvent="refreshWish" bind:signEvent="sign"
        bind:needAuthEvent="showAuth" tt:if="{{isHlt === '39'}}"></signCustom>
        <!-- 公司婚礼堂定制签到 -->
    <signLz sceneType="{{sceneType}}" activityTitle="{{activityTitle}}" userNameProp="{{userName}}" isExamine="{{isExamine}}" wishProp="{{wish}}"  bind:refreshWishEvent="refreshWish" bind:signEvent="sign" bind:needAuthEvent="showAuth" tt:elif="{{isHlt === '38' || isHlt === '41'}}"></signLz>
    <!-- 签到模块 -->
    <signNew sceneType="{{sceneType}}" activityTitle="{{activityTitle}}" userNameProp="{{userName}}"
        isExamine="{{isExamine}}" wishProp="{{wish}}" isForcePhone="{{isForcePhone}}" miaoShopId="{{miaoShopId}}"
        bind:refreshWishEvent="refreshWish" bind:signEvent="sign" bind:needAuthEvent="showAuth" tt:else></signNew>
    <!-- 授权登录弹窗 -->
    <authDialogNew dialogVisible="{{needAuth}}" bind:authSuccess="handleAuthSuccess" bind:authFail="handleAuthFail">
    </authDialogNew>
</view>
```

## File: pages/joymewIndex/joymewIndex.ttss
```
.joymewIndex {
    width: 100vw;
    height: 150vh;
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.joymewIndex>.bg {
    width: 750rpx;
    height: 1624rpx;
    background: radial-gradient(circle, #E94D67, #A81E24);
    position: absolute;
}

.joymewIndex>.title2Img {
    width: 501rpx;
    height: 387rpx;
    position: absolute;
    top: -39rpx;
    left: 129rpx;
}

.joymewIndex>.loveImg {
    width: 65rpx;
    height: 60rpx;
    position: absolute;
    left: 37rpx;
    top: 98rpx;
}

.joymewIndex>.love2Img {
    width: 51rpx;
    height: 46rpx;
    position: absolute;
    left: 89rpx;
    top: 21rpx;
}

.joymewIndex>.love3Img {
    width: 60rpx;
    height: 51rpx;
    position: absolute;
    top: 106rpx;
    right: 60rpx;
}

.joymewIndex>.pearImg {
    position: absolute;
    width: 188rpx;
    height: 189rpx;
    top: -60rpx;
    right: -19rpx;
}

.joymewIndex>.ribbonImg {
    width: 203rpx;
    height: 164rpx;
    position: absolute;
    top: 250rpx;
    left: -81rpx;
}

.joymewIndex>.ribbonImg2 {
    width: 180rpx;
    height: 145rpx;
    position: absolute;
    top: 218rpx;
    right: -79rpx;
}

.joymewIndex>.pearImg2 {
    position: absolute;
    width: 188rpx;
    height: 189rpx;
    top: 120rpx;
    right: -93rpx;
}

.joymewIndex>.weddingTitle {
    width: 705rpx;
    height: 319rpx;
    background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/box2-01.png');
    background-size: 100% 100%;
    position: absolute;
    top: 345rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.joymewIndex>.weddingTitle>.happyImg {
    width: 183rpx;
    height: 147rpx;
    position: absolute;
    left: 28rpx;
    top: -60rpx;
}

.joymewIndex>.weddingTitle>.title {
    font-size: 48rpx;
    font-weight: 400;
    color: #848484;
    background: linear-gradient(43deg, #FAE4A7 3.1494140625%, #F4CA71 29.0771484375%, #FADC9D 76.3671875%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: absolute;
    bottom: 66rpx;
    width: 100%;
    text-align: center;
    overflow: hidden;
    white-space: nowrap;
}

.joymewIndex>.weddingTitle>.welcome {
    font-size: 24rpx;
    font-weight: 400;
    color: #848484;
    position: absolute;
    top: 46rpx;
    background: linear-gradient(43deg, #FAE4A7 3.1494140625%, #F4CA71 29.0771484375%, #FADC9D 76.3671875%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    letter-spacing: 7rpx;
}

.joymewIndex>.weddingTitle>.engWelcome1 {
    font-size: 27rpx;
    font-family: zihun160hao;
    color: #848484;
    position: absolute;
    top: 99rpx;
    background: linear-gradient(43deg, #FAE4A7 3.1494140625%, #F4CA71 29.0771484375%, #FADC9D 76.3671875%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.joymewIndex>.weddingTitle>.engWelcome2 {
    font-size: 35rpx;
    font-weight: normal;
    color: #848484;
    position: absolute;
    top: 127rpx;
    background: linear-gradient(43deg, #FAE4A7 3.1494140625%, #F4CA71 29.0771484375%, #FADC9D 76.3671875%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.joymewIndex>.signTitleImg {
    width: 274rpx;
    height: 65rpx;
    position: absolute;
    top: 700rpx;
}

.joymewIndex>.signBox {
    width: 783rpx;
    height: 671rpx;
    position: absolute;
    top: 720rpx;
    background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/box-01.png');
    background-size: 100% 100%;
    left: 16rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.joymewIndex>.love4Img {
    position: absolute;
    width: 726rpx;
    height: 574rpx;
    bottom: -34rpx;
}

.joymewIndex>.signBox>.userName {
    position: absolute;
    top: 160rpx;
    width: 73%;
    left: 11%
}

.joymewIndex>.signBox .lineImg {
    /* width: 416rpx; */
    width: 100%;
    height: 3rpx;
    position: absolute;
    bottom: 0;
}

.joymewIndex>.signBox>.wishes {
    position: absolute;
    top: 281rpx;
    width: 73%;
    left: 11%;
    display: flex;
    align-items: center;
}

.joymewIndex>.signBox>.wishes>input {
    width: 66%;
    height: 91rpx;
    padding: 22rpx 0rpx;
    box-sizing: border-box;
    font-size: 32rpx;
    font-weight: normal;
    color: #FFFFFF;
    border: none;
    outline: none;
    margin-left: 7%;
}

.joymewIndex>.signBox>.wishes>.refreshBtn {
    width: 123rpx;
    height: 44rpx;
    background: rgba(255, 255, 255, 0.14);
    border: 0rpx solid #FFC6AB;
    border-radius: 16rpx;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    right: 3%;
}

.joymewIndex>.signBox>.wishes>.refreshBtn>.refreshIcon {
    width: 30rpx;
    height: 30rpx;
}

.joymewIndex>.signBox>.wishes>.refreshBtn>text {
    font-size: 24rpx;
    font-weight: normal;
    color: #FACD7F;
    margin-left: 7rpx;
}

.joymewIndex>.signBox>.userName>.iptWrap {
    display: flex;
    align-items: center;
    width: 100%;
}

.joymewIndex>.signBox>.userName>.iptWrap>text {
    font-size: 36rpx;
    font-weight: normal;
    color: #FFFFFF;
    margin-left: 7%;
    margin-right: 4%;
}

.joymewIndex>.signBox>.userName>.iptWrap>input {
    /* width: 416rpx; */
    width: 60%;
    height: 91rpx;
    padding: 22rpx 0rpx;
    box-sizing: border-box;
    font-size: 30rpx;
    font-weight: normal;
    color: #FFFFFF;
    border: none;
    outline: none;
}

.joymewIndex>.signBox>.chooseGroup {
    width: 52%;
    display: flex;
    justify-content: space-around;
    position: absolute;
    top: 420rpx;
    left: 15%;
}

.joymewIndex>.signBox>.chooseGroup>.chooseItem {
    width: 225rpx;
    height: 63rpx;
}

.joymewIndex>.signBox>.chooseGroup>.chooseItem {
    background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/round.png');
    background-size: 100% 100%;
    width: 34rpx;
    height: 34rpx;
    position: relative;
}

.joymewIndex>.signBox>.chooseGroup>.chooseItem>text {
    font-size: 28rpx;
    font-weight: normal;
    color: #FFFFFF;
    position: absolute;
    display: block;
    white-space: nowrap;
    left: 48rpx;
    top: -3rpx;
}

.joymewIndex>.signBox>.chooseGroup>.chooseItem.active {
    background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/roundActive.png');
    background-size: 100% 100%;
    width: 34rpx;
    height: 34rpx;
}

.joymewIndex>.signBox>.signBtn {
    background-image: url('https://ustatic.hudongmiao.com/joymewMp/joymewIndex/btn.png');
    background-size: 100% 100%;
    width: 445rpx;
    height: 87rpx;
    position: absolute;
    top: 500rpx;
}

.joymewIndex>.signBox>.authBtn {
    width: 445rpx;
    height: 87rpx;
    position: absolute;
    top: 500rpx;
    opacity: 0;
}

@media screen and (max-height: 720px) {
    .joymewIndex>.title2Img {
        top: -94rpx;
    }

    .joymewIndex>.weddingTitle {
        top: 241rpx;
    }

    .joymewIndex>.signTitleImg {
        top: 584rpx;
    }

    .joymewIndex>.signBox {
        top: 584rpx;
        background-size: 100% 90%;
        background-repeat: no-repeat;
    }

    .joymewIndex>.signBox>.userName {
        top: 120rpx;
    }

    .joymewIndex>.signBox>.wishes {
        top: 234rpx;
    }

    .joymewIndex>.signBox>.chooseGroup {
        top: 387rpx;
    }

    .joymewIndex>.signBox>.signBtn {
        top: 467rpx;
    }

    .joymewIndex>.signBox>.authBtn {
        top: 467rpx;
    }
}
```

## File: pages/live/live.js
```javascript
import { getToken, getLiveId } from '../../utils/storage';
import { getCurrentTimestamp } from '../../utils/date';
import { getOrigin, removeOrigin } from '../../utils/storage';
import { PAGE_HOST } from '../../assets/constant/host';

const app = getApp();

Page({
  data: {
    h5Url: '',
    activityTitle: '欢迎进入 嗨喵悦动',
    liveId: ''
  },
  onLoad: function (options) {
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: app.globalData.activityTitle,
      liveId: getLiveId()
    });
    console.log('***h5Url***');
    console.log(this.data.h5Url);
    console.log('***activityTitle***');
    console.log(this.data.activityTitle);
  },
  onShow: function () {
    if (app.globalData.isH5NeedRefresh) {
      console.log('***h5 needRefresh***');
      app.globalData.isH5NeedRefresh = false;
      this.updateH5Url();
      removeOrigin();
      this.setData({
        h5Url: app.globalData.h5Url,
        activityTitle: app.globalData.activityTitle,
        liveId: getLiveId()
      });
    }
    console.log('***h5Url***');
    console.log(this.data.h5Url);
    console.log('***activityTitle***');
    console.log(this.data.activityTitle);
  },
  updateH5Url() {
    const staicUrl = `${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}`;
    let variableUrl = '';
    if (app.globalData.userPhone) {
      variableUrl += `&userPhone=${app.globalData.userPhone}`;
    }
    const tmpOrigin = getOrigin();
    switch (tmpOrigin) {
      case 'sendGift':
        variableUrl += '&origin=sendGift';
        break;
      case 'purchaseEnterEffect':
        variableUrl += '&origin=purchaseEnterEffect';
        break;
      case 'sendBapin':
        variableUrl += '&origin=sendBapin';
        break;
      case 'sendPhoto':
        variableUrl += '&origin=sendPhoto';
        break;
      case 'sendDanmu':
        variableUrl += '&origin=sendDanmu';
        break;
      case 'sendDanmuHby':
        variableUrl += '&origin=sendDanmuHby';
        break;
      case 'editInfo':
        variableUrl += '&origin=editInfo';
        break;
      case 'sendDiamondHb':
        variableUrl += '&origin=sendDiamondHb';
        break;
      case 'adRewardGift':
        variableUrl += '&origin=adRewardGift';
        break;
      case 'sendGiftCarnival':
        variableUrl += '&origin=sendGiftCarnival';
        break;
      default:
        variableUrl = '';}


    if (variableUrl) {
      app.setH5Url(staicUrl + variableUrl);
      console.log(staicUrl + variableUrl);
    } else {
      app.setH5Url(staicUrl);
      console.log(staicUrl);
    }
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId
    };
  }
});
```

## File: pages/live/live.json
```json
{"navigationBarTitleText":" 嗨喵悦动","backgroundColor":"#305068","disableScroll":true}
```

## File: pages/live/live.ttml
```
<web-view tt:if="{{h5Url}}" src="{{h5Url}}">
</web-view>
```

## File: pages/live/live.ttss
```
page {
  background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: utils/date.js
```javascript
/** 
 * 日期比较大小 
 * compareDateString大于dateString，返回1； 
 * 等于返回0； 
 * compareDateString小于dateString，返回-1 
 * @param {日期字符串} dateString
 * @param {比较的日期} compareDateString  
 */
// export function dateCompare(dateString, compareDateString) {
//     var dateTime = dateParse(dateString).getTime();
//     var compareDateTime = dateParse(compareDateString).getTime();
//     if (compareDateTime > dateTime) {
//       return true;
//     } else if (compareDateTime == dateTime) {
//       return false;
//     } else {
//       return false;
//     }
//   };
export function dateCompare(dateString) {
  const dateTime = dateParse(dateString).getTime();

  // 减去24小时
  const compareDateTime = new Date().getTime() - 24 * 60 * 60 * 1000;
  if (compareDateTime > dateTime) {
    return true;
  }if (compareDateTime === dateTime) {
    return false;
  }
  return false;
}

/**
 * 将日期字符串转换为Date
 * @param {日期字符串} dateString 
 */
export function dateParse(dateString) {
  var SEPARATOR_BAR = "-";
  var SEPARATOR_SLASH = "/";
  var SEPARATOR_DOT = ".";
  var dateArray;
  if (dateString.indexOf(SEPARATOR_BAR) > -1) {
    dateArray = dateString.split(SEPARATOR_BAR);
  } else if (dateString.indexOf(SEPARATOR_SLASH) > -1) {
    dateArray = dateString.split(SEPARATOR_SLASH);
  } else {
    dateArray = dateString.split(SEPARATOR_DOT);
  }
  return new Date(dateArray[0], dateArray[1] - 1, dateArray[2]);
};

// 获取当前时间戳
export function getCurrentTimestamp() {
  return new Date().getTime();
}

export const newDateTransform = (timedata, t) => {
  let target = t;
  const date = new Date(timedata.substr(0, 19));
  const currentTime = date.getTime();
  const offset = date.getTimezoneOffset() * 60000;
  const utcTime = currentTime + offset;
  const newDate = new Date(utcTime + target * 3600000);
  const Year = newDate.getFullYear();
  const Month = newDate.getMonth() + 1 < 10 ?
  `0${newDate.getMonth() + 1}` :
  newDate.getMonth() + 1;
  const d = newDate.getDate() < 10 ? `0${newDate.getDate()}` : newDate.getDate();
  const Hours = newDate.getHours() < 10 ? `0${newDate.getHours()}` : newDate.getHours();
  const Minutes = newDate.getMinutes() < 10 ?
  `0${newDate.getMinutes()}` :
  newDate.getMinutes();
  const Seconds = newDate.getSeconds() < 10 ?
  `0${newDate.getSeconds()}` :
  newDate.getSeconds();
  const overTime = `${Year}/${Month}/${d} ${Hours}:${Minutes}:${Seconds}`;
  return overTime;
};

// 获取当前年月日时分秒
export function getCurrentDate() {
  let d = new Date();
  let year = d.getFullYear();
  let month = d.getMonth();
  month = month + 1 > 12 ? 1 : month + 1;
  month = month > 9 ? month : '0' + month.toString();
  let day = d.getDate();
  let hour = d.getHours();
  hour = hour > 9 ? hour : '0' + hour.toString();
  let minute = d.getMinutes();
  minute = minute > 9 ? minute : '0' + minute.toString();
  let second = d.getSeconds();
  return `${year}-${month}-${day} ${hour}:${minute}:${second}`;
}
```

## File: utils/index.js
```javascript
let wxToastLock = false;
let wxLoadingLock = false;
export function timeoutTask(task, time) {
  let tmpTimeout = setTimeout(() => {
    task();
    clearTimeout(tmpTimeout);
  }, time);
}
export function isNumber(val) {
  const regPos = /^\d+(\.\d+)?$/; //非负浮点数

  const regNeg = /^(-(([0-9]+\.[0-9]*[1-9][0-9]*)|([0-9]*[1-9][0-9]*\.[0-9]+)|([0-9]*[1-9][0-9]*)))$/; //负浮点数

  let flag = false;

  if (regPos.test(val) || regNeg.test(val)) {
    flag = true;
  }
  return flag;
}
// 获取随机值  min<= num < max
export const getRandom = (min, max) =>
Math.floor(Math.random() * (max - min)) + min;

export const showWxToast = (pTip) => {
  if (!wxToastLock && !wxLoadingLock) {
    wxToastLock = true;
    tt.showToast({
      title: pTip,
      icon: 'none'
    });
    timeoutTask(() => {
      hideWxToast();
    }, 1500);
  } else if (!wxToastLock && wxLoadingLock) {
    hideWxLoading();
    showWxToast(pTip);
  } else if (wxToastLock && !wxLoadingLock) {
    hideWxToast();
    showWxToast(pTip);
  } else {
    console.log('两个锁都是锁住状态 showWxToast');
  }
};

export const showWxLoading = (pTip) => {
  if (!wxToastLock && !wxLoadingLock) {
    wxLoadingLock = true;
    tt.showLoading({
      title: pTip,
      mask: true
    });
  } else if (!wxToastLock && wxLoadingLock) {
    hideWxLoading();
    showWxLoading(pTip);
  } else if (wxToastLock && !wxLoadingLock) {
    hideWxToast();
    showWxLoading(pTip);
  } else {
    console.log('两个锁都是锁住状态 showWxLoading');
  }
};

export const hideWxLoading = () => {
  if (wxLoadingLock) {
    tt.hideLoading();
    wxLoadingLock = false;
  } else {
    console.log('特殊情况hideWxLoading');
  }
};
const hideWxToast = () => {
  if (wxToastLock) {
    tt.hideToast();
    wxToastLock = false;
  } else {
    console.log('特殊情况hideWxToast');
  }
};

export const converNumToText = (numStr) => {
  let text = '';
  switch (numStr) {
    case '1':
      text = '一';
      break;
    case '2':
      text = '二';
      break;
    case '3':
      text = '三';
      break;
    case '4':
      text = '四';
      break;
    case '5':
      text = '五';
      break;
    case '6':
      text = '六';
      break;
    case '7':
      text = '七';
      break;
    case '8':
      text = '八';
      break;
    case '9':
      text = '九';
      break;
    case '10':
      text = '十';
      break;
    case '11':
      text = '十一';
      break;
    case '12':
      text = '十二';
      break;
    case '13':
      text = '十三';
      break;
    case '14':
      text = '十四';
      break;
    case '15':
      text = '十五';
      break;
    case '16':
      text = '十六';
      break;
    case '17':
      text = '十七';
      break;
    case '18':
      text = '十八';
      break;
    case '19':
      text = '十九';
      break;
    case '20':
      text = '二十';
      break;
    default:
      text = '';}

  return text;
};

// 获取当前年月日
export const getCurrentDate = (dateType) => {
  let tmpResultDate;
  const date = new Date();
  if (dateType === 'date') {
    const year = date.getFullYear();
    const tmpMonth = date.getMonth() + 1;
    const month = tmpMonth < 10 ? "0" + tmpMonth : tmpMonth;
    const day = date.getDate() < 10 ? "0" + date.getDate() : date.getDate();
    const hour = date.getHours() < 10 ? "0" + date.getHours() : date.getHours();
    const minute = date.getMinutes() < 10 ? "0" + date.getMinutes() : date.getMinutes();
    const second = date.getSeconds() < 10 ? "0" + date.getSeconds() : date.getSeconds();
    tmpResultDate = `${year}-${month}-${day} ${hour}:${minute}:${second}`;
  } else if (dateType === 'timestamp') {
    tmpResultDate = date.getTime();
  }
  return tmpResultDate;
};

// 比较版本号
export const compareVersion = (v1, v2) => {
  v1 = v1.split('.');
  v2 = v2.split('.');
  const len = Math.max(v1.length, v2.length);

  while (v1.length < len) {
    v1.push('0');
  }
  while (v2.length < len) {
    v2.push('0');
  }

  for (let i = 0; i < len; i++) {
    const num1 = parseInt(v1[i]);
    const num2 = parseInt(v2[i]);

    if (num1 > num2) {
      return 1;
    } else if (num1 < num2) {
      return -1;
    }
  }

  return 0;
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
```

## File: utils/request.js
```javascript
import {
API_HOST,
PAGE_HOST } from
'../assets/constant/host.js';
import {
getToken,
clearStorage } from
'./storage.js';
import {
showWxToast,
showWxLoading,
hideWxLoading } from
'./index.js';

export function request(url, method = 'GET', data) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    if (!data.cancelLoading) {
      showWxLoading('请求中');
    }
    const header = {

      'Content-Type': 'application/x-www-form-urlencoded'
    };
    if (tmpToken) {
      header.token = tmpToken;
    }
    tt.request({
      url: API_HOST + url,
      method,
      data,
      header,
      success: (res) => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        if (res.statusCode === 200) {
          if (res.data.success) {
            resolve(res.data);
          } else {
            if (res.data.message === '401') {
              showWxToast('登录已过期!');
              clearStorage();
              reject('401');
            } else {
              resolve(res.data);
            }
          }
        } else {
          showWxToast('网络异常');
          reject('网络异常');
        }
      },
      fail: (err) => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        showWxToast('网络异常');
        reject('网络异常');
      }
    });
  });
}

export function requestUpload(url, path) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    const header = {

      'Content-Type': 'application/x-www-form-urlencoded'
    };
    if (tmpToken) {
      header.token = tmpToken;
    }
    tt.uploadFile({
      url: 'https://www.hudongmiao.com/' + url,
      filePath: path,
      name: 'file',
      header,
      formData: {
        prefix: 'wechat-complaints'
      },
      success: function (res) {
        resolve(res);
      },
      fail: function (err) {
        reject(err);
      }
    });
  });
}

export function requestHMUpload(url, path, token) {
  return new Promise((resolve, reject) => {
    // const tmpToken = getToken();
    tt.uploadFile({
      url: 'https://hm.hudongmiao.com/' + url,
      filePath: path,
      name: 'file',
      header: {
        'token': token,
        'Content-Type': 'application/x-www-form-urlencoded'
      },
      formData: {
        prefix: 'wechat-complaints'
      },
      success: function (res) {
        resolve(res);
      },
      fail: function (err) {
        reject(err);
      }
    });
  });
}

export function $request(url, method = 'GET', data) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    if (!data.cancelLoading) {
      showWxLoading('请求中');
    }
    let header = {

      'Content-Type': 'application/x-www-form-urlencoded'
    };
    if (tmpToken) {
      header.token = tmpToken;
    }
    tt.request({
      url: 'https://www.hudongmiao.com/' + url,
      method,
      data,
      header,
      success: (res) => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        if (res.statusCode === 200) {
          if (res.data.success) {
            resolve(res.data);
          } else {
            if (res.data.message === '401') {
              showWxToast('登录已过期!');
              clearStorage();
              reject('401');
            } else {
              resolve(res.data);
            }
          }
        } else {
          showWxToast('网络异常');
          reject('网络异常');
        }
      },
      fail: (err) => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        showWxToast('网络异常');
        reject('网络异常');
      }
    });
  });
}

export function requestUploadAudio(url, path) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    tt.uploadFile({
      url: 'https://www.hudongmiao.com/' + url,
      filePath: path,
      name: 'file',
      header: {
        'token': tmpToken,
        'Content-Type': 'application/x-www-form-urlencoded'
      },
      formData: {
        prefix: 'audioAI'
      },
      success: function (res) {
        resolve(res);
      },
      fail: function (err) {
        reject(err);
      }
    });
  });
}

export function requestH5(url, method = 'GET', data) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    if (!data.cancelLoading) {
      showWxLoading('请求中');
    }
    tt.request({
      url: PAGE_HOST + url,
      method,
      data,
      header: {
        token: tmpToken,
        'Content-Type': 'application/x-www-form-urlencoded'
      },
      success: (res) => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        if (res.statusCode === 200) {
          if (res.data.success) {
            resolve(res.data);
          } else {
            if (res.data.message === '401') {
              showWxToast('登录已过期!');
              clearStorage();
              reject('401');
            } else {
              resolve(res.data);
            }
          }
        } else {
          showWxToast('网络异常');
          reject('网络异常');
        }
      },
      fail: (err) => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        showWxToast('网络异常');
        reject('网络异常');
      }
    });
  });
}
```

## File: utils/storage.js
```javascript
export function setToken(token) {
  tt.setStorageSync('token', token);
}
export function getToken() {
  return tt.getStorageSync('token');
}
export function setLiveId(liveId) {
  tt.setStorageSync('liveId', liveId);
}
export function getLiveId() {
  return tt.getStorageSync('liveId');
}
export function clearStorage() {
  //  wx.removeStorageSync('liveId');
  tt.removeStorageSync('token');
  tt.removeStorageSync('nickName');
  tt.removeStorageSync('avatarUrl');
  tt.removeStorageSync('userPhone');
}
export function setUseTipFlag() {
  tt.setStorageSync('useTipFlag', 1);
}
export function getUseTipFlag() {
  return tt.getStorageSync('useTipFlag');
}
export function setAdPopFlag() {
  tt.setStorageSync('adPopFlag', 1);
}
export function getAdPopFlag() {
  return tt.getStorageSync('adPopFlag');
}
export function setUserInfo(paramObj) {
  tt.setStorageSync('nickName', paramObj.nickName);
  tt.setStorageSync('avatarUrl', paramObj.avatarUrl);
}
export function getUserInfo() {
  return {
    nickName: tt.getStorageSync('nickName'),
    avatarUrl: tt.getStorageSync('avatarUrl')
  };
}
export function setOrigin(origin) {
  tt.setStorageSync('origin', origin);
}
export function getOrigin() {
  return tt.getStorageSync('origin');
}
export function removeOrigin() {
  tt.removeStorageSync('origin');
}
export function setUserPhone(userPhone) {
  tt.setStorageSync('userPhone', userPhone);
}
export function getUserPhone() {
  return tt.getStorageSync('userPhone');
}

export function setAllGiftList(allGiftList) {
  tt.setStorageSync('allGiftList', allGiftList);
}
export function getAllGiftList() {
  return tt.getStorageSync('allGiftList');
}
export function setIsHlt(val) {
  tt.setStorageSync('isHlt', val);
}
export function getIsHlt() {
  return tt.getStorageSync('isHlt');
}
```
