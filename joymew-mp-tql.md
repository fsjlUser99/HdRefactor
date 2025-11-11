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
- Only files matching these patterns are included: api, components, pages, utils/qiniu/index.js, utils/date.js, utils/index.js, utils/request.js, utils/storage.js, app.js, app.json
- Files matching patterns in .gitignore are excluded
- Files matching default ignore patterns are excluded
- Files are sorted by Git change count (files with more changes are at the bottom)

# Directory Structure
```
api/comment/comment.js
api/comment/draw.js
api/feedback/feedback.js
api/guessHb/guessHb.js
api/hbkdRecharge/hbkdRecharge.js
api/index/index.js
api/kbx/kbx.js
api/login.js
api/nyn/nyn.js
api/pay.js
api/recharge/recharge.js
api/system.js
api/zfdm/zfdm.js
api/zyz/zyz.js
app.js
app.json
components/authDialogNew/authDialogNew.js
components/authDialogNew/authDialogNew.json
components/authDialogNew/authDialogNew.wxml
components/authDialogNew/authDialogNew.wxss
components/authDialogNew/cropper/cropper.js
components/authDialogNew/cropper/cropper.json
components/authDialogNew/cropper/cropper.wxml
components/authDialogNew/cropper/cropper.wxss
components/feedbackEntry/feedbackEntry.js
components/feedbackEntry/feedbackEntry.json
components/feedbackEntry/feedbackEntry.wxml
components/feedbackEntry/feedbackEntry.wxss
components/image-cropper/image-cropper.js
components/image-cropper/image-cropper.json
components/image-cropper/image-cropper.wxml
components/image-cropper/image-cropper.wxss
components/privacyAuthorize/privacyAuthorize.js
components/privacyAuthorize/privacyAuthorize.json
components/privacyAuthorize/privacyAuthorize.wxml
components/privacyAuthorize/privacyAuthorize.wxss
components/rateStar/rateStar.js
components/rateStar/rateStar.json
components/rateStar/rateStar.wxml
components/rateStar/rateStar.wxss
components/sign/sign.js
components/sign/sign.json
components/sign/sign.wxml
components/sign/sign.wxss
pages/agreement/agreement.js
pages/agreement/agreement.json
pages/agreement/agreement.wxml
pages/agreement/agreement.wxss
pages/feedback/feedback.js
pages/feedback/feedback.json
pages/feedback/feedback.wxml
pages/feedback/feedback.wxss
pages/guessHb/guessHb.js
pages/guessHb/guessHb.json
pages/guessHb/guessHb.wxml
pages/guessHb/guessHb.wxss
pages/hbkdRecharge/hbkdRecharge.js
pages/hbkdRecharge/hbkdRecharge.json
pages/hbkdRecharge/hbkdRecharge.wxml
pages/hbkdRecharge/hbkdRecharge.wxss
pages/hbWall/hbWall.js
pages/hbWall/hbWall.json
pages/hbWall/hbWall.wxml
pages/hbWall/hbWall.wxss
pages/hotelReserve/couponDetail/couponDetail.js
pages/hotelReserve/couponDetail/couponDetail.json
pages/hotelReserve/couponDetail/couponDetail.wxml
pages/hotelReserve/couponDetail/couponDetail.wxss
pages/hotelReserve/hotelDetail/hotelDetail.js
pages/hotelReserve/hotelDetail/hotelDetail.json
pages/hotelReserve/hotelDetail/hotelDetail.wxml
pages/hotelReserve/hotelDetail/hotelDetail.wxss
pages/hotelReserve/hotelReserve.js
pages/hotelReserve/hotelReserve.json
pages/hotelReserve/hotelReserve.wxml
pages/hotelReserve/hotelReserve.wxss
pages/hotelReserve/menuDetail/menuDetail.js
pages/hotelReserve/menuDetail/menuDetail.json
pages/hotelReserve/menuDetail/menuDetail.wxml
pages/hotelReserve/menuDetail/menuDetail.wxss
pages/hotelReserve/packageDetail/packageDetail.js
pages/hotelReserve/packageDetail/packageDetail.json
pages/hotelReserve/packageDetail/packageDetail.wxml
pages/hotelReserve/packageDetail/packageDetail.wxss
pages/index/index.js
pages/index/index.json
pages/index/index.wxml
pages/index/index.wxss
pages/joymewIndex/joymewIndex.js
pages/joymewIndex/joymewIndex.json
pages/joymewIndex/joymewIndex.wxml
pages/joymewIndex/joymewIndex.wxss
pages/kbx/kbx.js
pages/kbx/kbx.json
pages/kbx/kbx.wxml
pages/kbx/kbx.wxss
pages/live/live.js
pages/live/live.json
pages/live/live.wxml
pages/live/live.wxss
pages/nyn/nyn.js
pages/nyn/nyn.json
pages/nyn/nyn.wxml
pages/nyn/nyn.wxss
pages/pay/pay.js
pages/pay/pay.json
pages/pay/pay.wxml
pages/photographerWall/photographerWall.js
pages/photographerWall/photographerWall.json
pages/photographerWall/photographerWall.wxml
pages/photographerWall/photographerWall.wxss
pages/photoWall/photoWall.js
pages/photoWall/photoWall.json
pages/photoWall/photoWall.wxml
pages/photoWall/photoWall.wxss
pages/recharge/recharge.js
pages/recharge/recharge.json
pages/recharge/recharge.wxml
pages/recharge/recharge.wxss
pages/recharge2/recharge2.js
pages/recharge2/recharge2.json
pages/recharge2/recharge2.wxml
pages/recharge2/recharge2.wxss
pages/test/index/index.js
pages/test/index/index.json
pages/test/index/index.wxml
pages/test/index/index.wxss
pages/test/login/login.js
pages/test/login/login.json
pages/test/login/login.wxml
pages/test/login/login.wxss
pages/test/pay/pay.js
pages/test/pay/pay.json
pages/test/pay/pay.wxml
pages/test/pay/pay.wxss
pages/zfdm/zfdm.js
pages/zfdm/zfdm.json
pages/zfdm/zfdm.wxml
pages/zfdm/zfdm.wxss
pages/zyz/zyz.js
pages/zyz/zyz.json
pages/zyz/zyz.wxml
pages/zyz/zyz.wxss
utils/date.js
utils/index.js
utils/qiniu/index.js
utils/request.js
utils/storage.js
```

# Files

## File: api/comment/comment.js
```javascript
import { $request, request } from "../../utils/request";

// 获取我的评价 及主持人信息
export function getHostInfo({ splid }) {
  return $request("splidComment/getMyComment", "POST", {
    splid,
  });
}

// 进行评价
export function commitComment({
  splid,
  // nickname,
  // avatar,
  content,
  label,
  satisfaction,
}) {
  return $request("splidComment/saveUserComment", "POST", {
    splid,
    // nickname,
    // avatar,
    content,
    type: "3", //场次评论
    label,
    satisfaction,
  });
}

// 获取评价汇总信息，
export function getHostCommentBase({ splid }) {
  return $request("splidComment/getUserComment", "POST", {
    splid,
  });
}

// 获取所欲评价用户评价列表
export function getHostCommentList({ splid, currentPage, showCount }) {
  return $request("splidComment/getCommentList", "POST", {
    splid,
    type: "3", //场次评价
    currentPage,
    showCount,
  });
}

// 打赏主持
export function Reward({ splid, totalfee}) {
  return request("hmWxmoney/chongzhiReward", "POST", {
    splid,
    totalfee,    
    // USER_ID,
    // openid,
  });
}
```

## File: api/comment/draw.js
```javascript
import { $request } from "../../utils/request";

// 获取抽奖列表
export function getLotteryInfo() {
  return $request("kpComment/getLotteryInfo", "POST", {
    lotteryId: '1',
  });
}
// 获取抽奖详情
export function getLotteryDetail({lotteryId}) {
  return $request("/kpComment/getLotteryInfoById", "POST", {
    lotteryId,
  });
}

// 参与抽奖
export function saveLotteryInfo({lotteryId}) {
  // const now = new Date()
  // const hours = now.getHours()
  // const minutes = now.getMinutes()
  // const add0 = (num) => num>9?num:'0'+ String(num)
  // const time = `${add0(hours)}:${add0(minutes)}`
  return $request("kpComment/saveLotteryInfo", "POST", {
    // lotteryId: '1',
    lotteryId,
    // time,
  });
}
```

## File: api/feedback/feedback.js
```javascript
import { request,requestUpload } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 提交反馈
export function submitFeedback(paramObj) {
    return request('wxScan/commandInfo6', 'POST', {
        userId: paramObj.userId,
        content: paramObj.desc,
        phone_number: paramObj.phone,
        reason: paramObj.type,
        splid: getLiveId(),
        piclink: paramObj.imgurl,
    });
}

// 上传反馈图片
export function uploadFeedbackImg(path) {
    return requestUpload('beiJing/shangchuanTomcat', path);
}

// 选择图片
export function wxChooseImage(uploaderNum) {
    return new Promise((resolve, reject) => {
        wx.chooseImage({
            count: 3 - uploaderNum,
            sizeType: ['original', 'compressed'], // 可以指定是原图还是压缩图，默认二者都有
            sourceType: ['album', 'camera'], // 可以指定来源是相册还是相机，默认二者都有
            success: (res) => {
                resolve(res);
            },
            fail: (err) => {
                reject(err);
            },
        })
    });
}
```

## File: api/guessHb/guessHb.js
```javascript
import { request } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 获取猜红包状态
export function getGuessInfo(cancelLoading) {
    return request('guessRedPackage/getGuessInfo', 'POST', {
        splid: getLiveId(),
        cancelLoading,
    });
}

// 参与猜红包
export function attendGuess(pObj) {
    return request('guessRedPackage/robRedPackage', 'POST', {
        splid: getLiveId(),
        sort: pObj.sort,
        rob_sort: pObj.robSort,
        guess_money: pObj.guessMoney,
        red_package_id: pObj.hbId,
    });
}

// 猜红包充值
export function guessHbRecharge(paramObj) {
    return request('hmWxmoney/chongzhiKbx', 'POST', {
        splid: getLiveId(),
        giftId: 'guess',
        userId: paramObj.userId,
        openid: paramObj.openid,
        total: paramObj.money,
    });
}
```

## File: api/hbkdRecharge/hbkdRecharge.js
```javascript
import { request } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 红包口袋充值
export function rechageHbkd(paramObj) {
    return request('hmWxmoney/chongZhiRedB', 'POST', {
        splid: getLiveId(),
        totalfee: paramObj.total,
        USER_ID: paramObj.userId,
        openid: paramObj.openId,
    });
}
// 红包口袋列表
export function getHbkdList() {
    return request('hbkd/shenLuoTianZheng6', 'POST', {
        splid: getLiveId(),
    });
}
```

## File: api/index/index.js
```javascript
import { request, $request, requestH5 } from '../../utils/request';
import { getLiveId } from '../../utils/storage';

const app = getApp();
//验证司仪
export function validateEmcee() {
  return request('emceeUser/validate', 'POST', {});
}

//获取活动信息
export function getLiveInfo() {
  return request('wxScan/saiYaRen', 'POST', {
    splid: getLiveId(),
  });
}

//充值(测试方法)
export function recharge(money) {
  return new Promise((resolve, reject) => {
    request('hmWxmoney/chongzhiMiao', 'post', {
      total: money,
      userId: wx.getStorageSync('userId'),
      openid: wx.getStorageSync('openId'),
    })
      .then(res1 => {
        return pay(res1);
      })
      .then(res2 => {
        resolve(res2);
      })
      .catch(err => {
        console.log(err);
        reject(err);
      });
  });
}

//支付(测试方法)
export function pay(param) {
  return new Promise((resolve, reject) => {
    wx.requestPayment({
      timeStamp: param.obj.timeStamp,
      nonceStr: param.obj.nonceStr,
      package: param.obj.package,
      signType: 'MD5',
      paySign: param.obj.paySign,
      success: function(res) {
        console.log(res);
        resolve(res);
      },
      fail: function(res) {
        reject(res);
      },
    });
  });
}

// 获取签到状态
export function getSignInState() {
  return request('hmScanReportController/getQianDaoInfo', 'GET', {
    splid: getLiveId(),
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
    gender: paramObj.gender,
  });
}

// 订阅消息
export function addSubscribeSize() {
  return request('subscribeController/addSubscribeSize', 'POST', {});
}

// userId换取liveId
export function getLiveIdByUserId(userId) {
  return $request('fixed/getQrcode', 'POST', {
    userId,
  });
}

// 获取聊天记录
export function getMsgInfo() {
  return requestH5('wxScan/getMsgInfo', 'GET', {
    splid: getLiveId(),
    num: 1,
    size: 30,
  });
}

// 发送聊天消息
export function sendChatMessage(message) {
  return requestH5('sendMsgController/msgGo6', 'POST', {
    splid: getLiveId(),
    content: message,
    color: 0,
  });
}

  // 保存签到信息(h5授权前调用)
  export function saveSignInfo({
    splid = getLiveId(),
    bless_str = '',
    phonenumber = '',
    type = '', // 角色
    birthDate = '',
    gender = '',
    redirect_url = '',
  }) {
    return request('hmScanReportController/saveQianDaoParam', 'POST', {
      splid,
      bless_str,
      phonenumber,
      type,
      birthDate,
      gender,
      redirect_url,
    });
  }
```

## File: api/kbx/kbx.js
```javascript
import { request } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 开宝箱充值
export function kbxRecharge(paramObj) {
    return request('hmWxmoney/chongzhiKbx', 'POST', {
        splid: getLiveId(),
        giftId: 'kbx',
        userId: paramObj.userId,
        openid: paramObj.openid,
        total: paramObj.money,
    });
}

// 抢宝箱
export function robBox(paramObj) {
    return request('kakaluote/guipaiqigong6', 'POST', {
        splid: getLiveId(),
        boxIdList: paramObj.boxIds,
        order_by: paramObj.sort,
    });
}

// 获取宝箱列表
export function getBoxesList() {
    return request('kakaluote/chaojisaiyaren6', 'GET', {
        splid: getLiveId(),
    });
}

// 发送广播
export function sendBroadCast(paramObj) {
    return request('sendMsgController/duxin6', 'POST', {
        splid: getLiveId(),
        ykq_info: paramObj.c
    });
}

// 获取game状态
export function getGameState(userId) {
    return request('play/baiyan6', 'GET', {
        splid: getLiveId(),
        userId,
    });
}

// 获取我的宝箱
export function getMyBoxes() {
    return request('kakaluote/jianlai6', 'GET', {
        splid: getLiveId(),
    });
}

// 获取红包列表
export function getHbList(cancelLoading) {
    return request('hbqController/showHbqList6', 'GET', {
        splid: getLiveId(),
        cancelLoading,
    });
}

// 买红包
export function buyHb(paramObj) {
    return request('hbqController/hbqPay6', 'POST', {
        splid: getLiveId(),
        eggIdList: paramObj.hbIds,
        order_by: paramObj.sort,
    });
}

// 红包墙充值
export function hbqRecharge(paramObj) {
    return request('hmWxmoney/chongzhiKbx', 'POST', {
        splid: getLiveId(),
        giftId: 'hbq',
        userId: paramObj.userId,
        openid: paramObj.openid,
        total: paramObj.money,
    });
}

// 获取红包排行榜
export function getHbRankList() {
    return request('hbqController/hbqRankList6', 'GET', {
        splid: getLiveId(),
    });
}
```

## File: api/login.js
```javascript
import { request } from '../utils/request.js';
import { getLiveId } from '../utils/storage';
/**
 * 微信登录获取code
 */
export function wxLogin() {
  return new Promise((resolve, reject) => {
    wx.login({
      timeout: 10000,
      success: result => {
        resolve(result);
      },
      fail: () => {
        reject(1);
      },
    });
  });
}
/**
 * 用户授权
 */
export function authUser(paramObj) {
  let param;
  if (paramObj.userInfo) {
    param = {
      code: paramObj.code,
      userInfo: paramObj.userInfo,
      splid: getLiveId(),
    };
  } else {
    param = {
      code: paramObj.code,
      encryptedData: paramObj.encryptedData,
      iv: paramObj.iv,
      splid: getLiveId(),
    };
  }
  return request('wxScan/oauth_user6', 'POST', param);
}

// 用户授权new
export function authUserNew(code) {
  return request('wxScan/oauth_user7', 'POST', {
      code,
      cancelLoading: true
  });
}
/**
 * 获取用户信息
 * 
 */
export function wxGetUserInfo() {
  return new Promise((resolve, reject) => {
    wx.getUserInfo({
      lang: 'zh_CN',
      success: result => {
        resolve(result);
      },
      fail: () => {
        reject(1);
      },
    });
  });
}

export function wxGetUserInfoNew() {
  return new Promise((resolve, reject) => {
    wx.getUserProfile({
      lang: 'zh_CN',
      desc: '业务需要',
      success: result => {
        resolve(result);
      },
      fail: err => {
        reject(err);
      },
    });
  });
}
// 授权获取手机号(同庆楼专用，后台会多查询一次)(废弃)
export function authGetPhone(paramObj) {
  return request('wxScan/authPhone', 'POST', {
    encryptedData: paramObj.encryptedData,
    iv: paramObj.iv,
  });
}

// 新版获取手机号 
export function authGetPhoneNew(paramObj) {
  const { code } = paramObj;
  const targetObj = {
    splid: getLiveId(),
    code,
  }
  if(!code) {
    delete targetObj.code
  }
  console.log(targetObj);
  return request('wxScan/authPhone2', 'POST', targetObj);
}
```

## File: api/nyn/nyn.js
```javascript
import { request } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 获取奖池金额
export function getPoolMoney() {
    return request('jianLai/luckyDbList6', 'GET', {
        splid: getLiveId(),
        cancelLoading: true,
    });
}
// 获取奖项列表
// export function getPrizeList() {
//     return request('jianLai/startData6', 'GET', {});
// }
// 获取扭一扭相关信息
export function getNynInfo() {
    return request('jianLai/getLuckyId6', 'GET', {
        splid: getLiveId(),
        playInfo: 'hdGame88',
    });
}
// 获取扭一扭排行榜列表
export function getNynRank() {
    return request('jianLai/luckyDbRank6', 'GET', {
        splid: getLiveId(),
    });
}
// 扭一扭充值
export function nynRecharge(paramObj) {
    return request('hmWxmoney/chongzhiNyn', 'POST', {
        splid: getLiveId(),
        giftId: 'one',
        USER_ID: paramObj.userId,
        openid: paramObj.openId,
    });
}
// 扭一扭开始
export function startNyn(paramObj) {
    return request('jianLai/niuyiniu6', 'POST', {
        splid: getLiveId(),
        playInfo: 'hdGame88',
        id: paramObj.turnId,
    });
}
// 扭一扭发送中奖信息
export function sendPrizeInfo(paramObj) {
    return request('jianLai/luoXuanWan6', 'POST', {
        type: '2',
        gold: paramObj.gold,
        balance: paramObj.remainCoin,
        splid: getLiveId(),
        id: paramObj.turnId,
    });
}
// 发送广播
export function sendBroadCast(paramObj) {
    return request('sendMsgController/duxin6', 'POST', {
        splid: getLiveId(),
        ykq_info: paramObj.c
    });
}
```

## File: api/pay.js
```javascript
// 微信支付
export function wxPay(param) {
    return new Promise((resolve, reject) => {
        wx.requestPayment({
            'timeStamp': param.obj.timeStamp,
            'nonceStr': param.obj.nonceStr,
            'package': param.obj.package,
            'signType': 'MD5',
            'paySign': param.obj.paySign,
            'success': function (res) {
                console.log(res);
                resolve(res)
            },
            'fail': function (res) {
                reject(res)
            }
        })
    });
}
```

## File: api/recharge/recharge.js
```javascript
import { request, requestUpload } from '../../utils/request';
import { getLiveId } from '../../utils/storage';

// 获取发送礼物排行榜
export function getGiftRankList() {
    return request('hmGiftController/findGiftRankList6', 'GET', {
        splid: getLiveId(),
    });
}
// 获取男女方发送礼物排行榜
export function getRoleGiftRankList() {
    return request('hmGiftController/findGiftRankList7', 'GET', {
        splid: getLiveId(),
    });
}
// 发送礼物
export function sendGift(paramObj) {
    return request('hmGiftController/sendGift6', 'POST', {
        splid: getLiveId(),
        giftconst: paramObj.giftId,
    });
}
// 发送霸气弹幕礼物
export function sendDanmuGift(paramObj) {
    return request('hmGiftController/sendGift6', 'POST', {
        splid: getLiveId(),
        giftconst: paramObj.giftId,
        content: paramObj.giftWish,
        gift_source: paramObj.giftSource,
    });
}

// 发送礼物广播
export function sendGiftBroadCast(paramObj) {
    return request('sendMsgController/liwuGo6', 'POST', {
        splid: getLiveId(),
        liwuId: paramObj.giftId,
        content: paramObj.content || '',
    });
}
// 支付
export function diamondRecharge(paramObj) {
    return request('hmWxmoney/chongzhiMiao', 'POST', {
        total: paramObj.total,
        userId: paramObj.userId,
        openid: paramObj.openId,
    });
}

// 领取vip头像框
export function becomeVip() {
    return request('wxScan/becomeVip', 'POST', {
        miao_vip: 'vip1',
        splid: getLiveId(),
    });
}

// 选择图片
export function wxChooseImage() {
    return new Promise((resolve, reject) => {
        wx.chooseImage({
            count: 1,
            sizeType: ['original', 'compressed'], // 可以指定是原图还是压缩图，默认二者都有
            sourceType: ['album', 'camera'], // 可以指定来源是相册还是相机，默认二者都有
            success: (res) => {
                resolve(res);
            },
            fail: (err) => {
                reject(err);
            },
        })
    });
}

// 上传图片
export function uploadHeadImg(path) {
    return requestUpload('beiJing/shangchuanTomcat', path);
}

// 修改个人信息
export function editUserInfo(paramObj) {
    return request('hmGiftController/editUserInfo', 'POST', {
        wx_name: paramObj.wx_name,
        avator: paramObj.avator,
        table_number: paramObj.table_number,
        position: paramObj.position,
        type: paramObj.type,
        splid: getLiveId(),
    });
}

export function buyLivePhoto(livePhotoId) {
    return request('hmGiftController/buyPhoto', 'POST', {
        id: livePhotoId,
        splid: getLiveId(),
    });
}


// 送礼物游戏支付并发送
export function sendGiftGameRecharge({giftconst,openid, userId, content}) {
    return request('hmWxmoney/sendWishPay', 'POST', {
        giftconst,
        openid,
        userId,
        content,
        splid: getLiveId(),
    });
}

// 全屏特效支付并发送
export function sendSuperDanmuRecharge({giftconst,openid, userId, content}) {
    return request('hmWxmoney/sendSuperGift', 'POST', {
        giftconst,
        openid,
        userId,
        content,
        splid: getLiveId(),
    });
}
```

## File: api/system.js
```javascript
import { showWxToast } from '../utils/index'

const TEMPLATEID = 'uDvjb_IqKELTI2NFD2uwyXze9pMDAxda1go-uFjQzqY';
const TEMPLATEID2 = 'smK_K6cNxrFRgSPW_YPDzMedFBZa6DfxAqv2inEsYvU';
// 检查小程序更新
export function checkSystemUpdate() {
    const updateManager = wx.getUpdateManager()

    updateManager.onCheckForUpdate(function (res) {
        // 请求完新版本信息的回调
        console.log('onCheckForUpdate',res.hasUpdate)
    })

    updateManager.onUpdateReady(function () {
        wx.showModal({
            title: '更新提示',
            content: '新版本已经准备好，是否重启应用？',
            success: function (res) {
                if (res.confirm) {
                    // 新的版本已经下载好，调用 applyUpdate 应用新版本并重启
                    updateManager.applyUpdate()
                }
            }
        })
    })

    updateManager.onUpdateFailed(function () {
        // 新版本下载失败
        showWxToast('新版本下载失败!');
    })
}

//获取系统信息
export function getSystemInfo() {
    return new Promise((resolve, reject) => {
        wx.getSystemInfo({
            success: (result) => {
                resolve(result);
            },
            fail: () => {
                reject(1);
            }
        });
    })
}

//获取用户的当前设置(是否授权过等信息)
export function getSetting() {
    return new Promise((resolve, reject) => {
        wx.getSetting({
            success: (result) => {
                resolve(result);
            },
            fail: () => {
                reject(1);
            }
        });
    })
}

//询问订阅消息
export function getSubscribeMessage() {
    return new Promise((resolve, reject) => {
        wx.requestSubscribeMessage({
            tmplIds: [TEMPLATEID,TEMPLATEID2],
            success: (result) => {
                resolve(result[TEMPLATEID,TEMPLATEID2]);
            },
            fail: () => {
                reject(1);
            }
        });
    })
}

// 下载文件
export function wxDownloadFile(filePath) {
    return new Promise((resolve,reject) => {
        wx.downloadFile({
            url: filePath,
            success: (res) => {
                resolve(res);
            },
            fail: (err) => {
                reject(err);
            },
        });
    });
}

// 文件保存到相册
export function wxSaveFileToAlbum(tmpFilePath) {
    return new Promise((resolve,reject) => {
        wx.saveImageToPhotosAlbum({
            filePath: tmpFilePath,
            success: (res) => {
                resolve(res);
            },
            fail: (err) => {
                reject(err);
            },
        });
    });
}
```

## File: api/zfdm/zfdm.js
```javascript
import { request } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 争分夺秒充值
export function zfdmRecharge(paramObj) {
    return request('hmWxmoney/chongzhiRace', 'POST', {
        splid: getLiveId(),
        USER_ID: paramObj.userId,
        openid: paramObj.openId,
    });
}

// 获取争分夺秒信息
export function getZfdmInfo(isLoop) {
    return request('race/getRaceInfo', 'GET', {
        splid: getLiveId(),
        cancelLoading: isLoop ? isLoop : '',
    });
}

// 争分夺秒开始游戏
export function startZfdm(paramObj) {
    return request('race/robRace', 'POST', {
        splid: getLiveId(),
        guess_info_id: paramObj.guessInfoId,
        raceTime: paramObj.raceTime,
    });
}

// 获取排行榜
export function getZfdmRankList(redpackageId) {
    return request('race/getRaceRankList', 'GET', {
        splid: getLiveId(),
        red_package_id: redpackageId,
    });
}
```

## File: api/zyz/zyz.js
```javascript
import { request } from '../../utils/request'
import { getLiveId } from '../../utils/storage'

// 获取奖池金额
export function getPoolMoney() {
    return request('jianLai/luckyDbList6', 'GET', {
        splid: getLiveId(),
        cancelLoading: true,
    });
}
// 获取转一转相关信息W
export function getZyzInfo() {
    return request('jianLai/getLuckyId6', 'GET', {
        splid: getLiveId(),
        playInfo: 'hdGame89',
    });
}
// 获取转一转排行榜列表
export function getZyzRank() {
    return request('jianLai/luckyDbRank6', 'GET', {
        splid: getLiveId(),
    });
}
// 转一转充值
export function zyzRecharge(paramObj) {
    return request('hmWxmoney/chongzhiNyn', 'POST', {
        splid: getLiveId(),
        giftId: 'one',
        USER_ID: paramObj.userId,
        openid: paramObj.openId,
    });
}
// 转一转开始
export function startZyz(paramObj) {
    return request('jianLai/luckyDb6', 'POST', {
        splid: getLiveId(),
        playInfo: 'hdGame89',
        id: paramObj.turnId,
    });
}
// 转一转发送中奖信息
export function sendPrizeInfo(paramObj) {
    return request('jianLai/luoXuanWan6', 'POST', {
        type: '2',
        gold: paramObj.gold,
        balance: paramObj.remainCoin,
        splid: getLiveId(),
        id: paramObj.turnId,
    });
}
// 发送广播
export function sendBroadCast(paramObj) {
    return request('sendMsgController/duxin6', 'POST', {
        splid: getLiveId(),
        ykq_info: paramObj.c
    });
}
```

## File: app.js
```javascript
import { checkSystemUpdate } from './api/system.js';
import { setUserInfo, getUserInfo } from './utils/storage.js';

App({
  onLaunch: function() {
    //检查小程序更新
    checkSystemUpdate();
  },
  onHide: function() {},
  globalData: {
    // 授权登录后获取的用户基本信息
    userInfo: {
      // 测试用待修改
      // nickName: '汪元会',
      // avatarUrl: 'https://thirdwx.qlogo.cn/mmopen/vi_32/sw36m5OS67agMibBw1ulocBjr5Hmv0zOkylyq7HrG3UD2ERQ2ux9IrMT1v7AxTrCgFmMnnb9QKPFtLyR80picBFA/132',
      nickName: '',
      avatarUrl: '',
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
    // 测试用待修改
    // nynList: [{code:"0",desc:"谢谢参与"},{code:"4",desc:"18元"},{code:"5",desc:"58.8元"},{code:"6",desc:"88.8元"},{code:"7",desc:"28.8元"},{code:"8",desc:"68.8元"},{code:"9",desc:"38.8元"},{code:"10",desc:"谢谢参与"}],
  },
  setUserInfo(paramObj) {
    if (paramObj) {
      this.globalData.userInfo.nickName = paramObj.nickName;
      this.globalData.userInfo.avatarUrl = paramObj.avatarUrl;
      setUserInfo({
        nickName: paramObj.nickName,
        avatarUrl: paramObj.avatarUrl,
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
});
```

## File: app.json
```json
{
  "pages": [
    "pages/joymewIndex/joymewIndex",
    "pages/index/index",
    "pages/live/live",
    "pages/test/pay/pay",
    "pages/nyn/nyn",
    "pages/zyz/zyz",
    "pages/kbx/kbx",
    "pages/test/login/login",
    "pages/recharge/recharge",
    "pages/recharge2/recharge2",
    "pages/hbkdRecharge/hbkdRecharge",
    "pages/test/index/index",
    "pages/pay/pay",
    "pages/agreement/agreement",
    "pages/feedback/feedback",
    "pages/photoWall/photoWall",
    "pages/hbWall/hbWall",
    "pages/photographerWall/photographerWall",
    "pages/hotelReserve/hotelReserve",
    "pages/hotelReserve/hotelDetail/hotelDetail",
    "pages/hotelReserve/packageDetail/packageDetail",
    "pages/hotelReserve/menuDetail/menuDetail",
    "pages/hotelReserve/couponDetail/couponDetail",
    "pages/guessHb/guessHb",
    "pages/zfdm/zfdm"
  ],
  "window": {
    "backgroundTextStyle": "light",
    "navigationBarBackgroundColor": "#fff",
    "navigationBarTitleText": " 嗨喵悦动",
    "navigationBarTextStyle": "black",
    "onReachBottomDistance": 100
  },
  "usingComponents": {
    "authDialogNew": "/components/authDialogNew/authDialogNew",
    "image-cropper": "/components/image-cropper/image-cropper",
    "privacyAuthorize": "/components/privacyAuthorize/privacyAuthorize"
  },
  "sitemapLocation": "sitemap.json",
  "resolveAlias": {
    "@/*": "/*"
  },
  "__usePrivacyCheck__": true
}
```

## File: components/authDialogNew/authDialogNew.js
```javascript
import {
    wxLogin,
    authUserNew
  } from '../../api/login';
  import qiniu from '../../utils/qiniu/index';
  import { setToken } from '../../utils/storage';
  import { showWxToast, getRandom } from '../../utils/index';
  import defaultContent from '../../assets/constant/default';
  
  const app = getApp();
  
  const DEFAULTAVATAR = 'https://ustatic.hudongmiao.com/joymewMp/grayAvator.png';
  Component({
    /**
     * 组件的属性列表
     */
    properties: {
      dialogVisible: {
        value: false,
        type: Boolean,
      },
      isJoymewIndex: {
        // 是否是首页调用
        value: true,
        type: Boolean,
      },
    },
    observers: {
      dialogVisible: function(dialogVisible) {
        if (dialogVisible) {
          // 授权的登录弹窗出现
          console.log(this.data.dialogVisible);
          this.loginSilence();
        }
      },
      avatarCropped: function(newVal) {
        if (newVal) {
          this.setData({
            avatarUrl: newVal,
          });
          console.log('上传服务器前的图片地址:', this.data.avatarUrl);
          this.uploadAvatar(this.data.avatarUrl);
        }
      },
    },
    data: {
      isNewAuthBox: false,
      avatarUrl: DEFAULTAVATAR,
      avatarUncropped: '',
      avatarCropped: '',
      nickName: '',
    },
    attached() {},
    /**
     * 组件的方法列表
     */
    methods: {
      openAuthNew: function() {
        let that = this;
        if (!this.data.avatarUrl || this.data.avatarUrl === DEFAULTAVATAR) {
          wx.showModal({
            title: '提示',
            content: '请上传头像!',
            cancelText: '默认头像',
            confirmText: '知道了',
            success: function(sm) {
              if (sm.confirm) {
                console.log('用户点击确认');
              } else if (sm.cancel) {
                // 设置默认头像
                const AVATARS = defaultContent.defaultAvatars;
                const tmpLen = AVATARS.length;
                that.setData({
                  avatarUrl: AVATARS[getRandom(0, tmpLen)],
                });
              }
            },
          });
          return;
        }
        if (!this.data.nickName) {
          // showWxToast('请填写姓名!');
          wx.showModal({
            title: '提示',
            content: '请填写姓名!',
            cancelText: '默认姓名',
            confirmText: '知道了',
            success: function(sm) {
              if (sm.confirm) {
                console.log('用户点击取消');
              } else if (sm.cancel) {
                // 设置默认姓名
                that.setData({
                  nickName: `嗨喵用户${getRandom(0, 9999)}`,
                });
              }
            },
          });
          return;
        }
        const tmpUserInfo = {
          nickName: this.data.nickName,
          avatarUrl: this.data.avatarUrl,
        };
        app.setUserInfo(tmpUserInfo);
        this.triggerEvent('authSuccess');
      },
      loginSilence: function() {
        wxLogin()
          .then(res => {
            console.log('***wxLogin***');
            console.log(res);
            return authUserNew(res.code);
          })
          .then(res2 => {
            console.log('***静默授权结果***');
            console.log(res2);
            setToken(res2.data.token);
            const tmpUserInfo = res2.data.user;
            if (tmpUserInfo.avator && tmpUserInfo.wx_name) {
              // 后台存有用户头像昵称
              app.setUserInfo({
                nickName: tmpUserInfo.wx_name,
                avatarUrl: tmpUserInfo.avator,
              });
              this.triggerEvent('authSuccess');
            } else if (this.data.isJoymewIndex) {
              // 首页调用authDialogNew组件
              this.triggerEvent('authSuccess', 'needH5Auth');
            } else {
              this.initQiniuInfo();
              // 后台没有保存过用户头像昵称
              this.setData({
                isNewAuthBox: true,
              });
            }
          })
          .catch(err => {
            console.log('静默授权失败', err);
            this.closeAuth();
          });
      },
      closeAuth: function() {
        this.triggerEvent('authFail');
      },
      onChooseAvatar: function(e) {
        const { avatarUrl } = e.detail;
        this.setData({
          avatarUrl,
          avatarUncropped: avatarUrl,
        });
      },
      handleCancelCropper() {
        this.setData({
          avatarUncropped: '',
          avatarUrl: '',
        });
      },
      handleConfirmCropper(e) {
        this.setData({
          avatarUncropped: '',
          avatarCropped: e.detail,
        });
      },
      userNameBlur: function(e) {
        if (wx.requirePrivacyAuthorize) {
          wx.requirePrivacyAuthorize({});
        }
        this.setData({
          nickName: e.detail.value,
        });
      },
      uploadAvatar: function(avatarPath) {
        qiniu
          .qiniuUpload(avatarPath)
          .then(res => {
            console.log(res);
            this.setData({
              avatarUrl: res.imageURL,
            });
          })
          .catch(err => {
            console.log(err);
            showWxToast('头像上传失败!请重新进入小程序!');
          });
      },
      initQiniuInfo: function() {
        qiniu
          .getQiniuToken()
          .then(res => {
            console.log(res.data.token);
            qiniu.initQiniu(res.data.token);
          })
          .catch(err => {
            console.log(err);
          });
      },
    },
  });
```

## File: components/authDialogNew/authDialogNew.json
```json
{
    "component": true,
    "usingComponents": {
      "cropper": "./cropper/cropper"
    }
  }
```

## File: components/authDialogNew/authDialogNew.wxml
```
<!-- 新授权登陆 -->
<view class="authLogin {{isNewAuthBox?'shade':''}}" wx:if="{{dialogVisible}}">
  <view class="authBox" wx:if="{{isNewAuthBox}}">
    <button class="avatar-wrapper" open-type="chooseAvatar" bind:chooseavatar="onChooseAvatar">
      <image class="avatar" src="{{avatarUrl}}"></image>
    </button>
    <view class="nameIpt">
      <text class="key">昵称</text>
      <input type="nickname" class="weui-input" value="{{nickName}}" bindblur="userNameBlur" maxlength="12" placeholder="请输入昵称" placeholder-class="phcolor" />
    </view>
    <view class="btn" bindtap="openAuthNew">授权登录</view>
    <image class="closeImg" src="https://static.joymew.com/joymewMp/authDialog/closeIcon.png" bindtap="closeAuth"></image>
    <cropper avatarUncropped="{{avatarUncropped}}" bind:cancelEvent="handleCancelCropper" bind:confirmEvent="handleConfirmCropper"></cropper>
  </view>
</view>
<!-- 隐私授权弹窗 -->
<privacyAuthorize></privacyAuthorize>
```

## File: components/authDialogNew/authDialogNew.wxss
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
  .authLogin > .authBox {
    width: 520rpx;
    height: 600rpx;
    background-image: url('https://static.joymew.com/joymewMp/authDialog/authBg.png');
    background-size: 100% 100%;
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .authLogin > .authBox > .logoImg {
    width: 124rpx;
    height: 124rpx;
    position: absolute;
    top: 137rpx;
  }
  
  .authLogin > .authBox > .name {
    font-size: 36rpx;
    font-weight: bold;
    color: #313131;
    position: absolute;
    top: 288rpx;
  }
  
  .authLogin > .authBox > .btn {
    width: 300rpx;
    height: 80rpx;
    background: linear-gradient(-45deg, #feb141, #fec74d);
    box-shadow: 0px 12px 24px 0px rgba(254, 177, 65, 0.24);
    border-radius: 40rpx;
    font-size: 28rpx;
    font-weight: bold;
    color: #ffffff;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    bottom: 61rpx;
    letter-spacing: 0.5vw;
  }
  
  .authLogin > .authBox > .closeImg {
    width: 44rpx;
    height: 44rpx;
    position: absolute;
    bottom: -89rpx;
  }
  
  .authBox > .avatar-wrapper {
    width: 200rpx;
    height: 200rpx;
    margin-top: 40rpx;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .authBox > .avatar-wrapper > .avatar {
    width: 120rpx;
    height: 120rpx;
  }
  .authBox > .nameIpt {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    margin-top: 40rpx;
    border-top: 2rpx solid rgba(0, 0, 0, 0.1);
    border-bottom: 2rpx solid rgba(0, 0, 0, 0.1);
    width: 100%;
    height: 85rpx;
    padding: 0 20rpx;
  }
  .authBox > .nameIpt > .key {
    color: #333333;
    font-size: 38rpx;
  }
  .authBox > .nameIpt > .weui-input {
    width: 380rpx;
    font-size: 38rpx;
  }
  .phcolor {
    color: #333333;
  }
```

## File: components/authDialogNew/cropper/cropper.js
```javascript
Component({
    /**
     * 组件的属性列表
     */
    properties: {
      avatarUncropped: {
        type: String,
        value: '',
      },
    },
    observers: {
      avatarUncropped: function(newVal) {
        if (newVal) {
          wx.nextTick(() => {
            this.cropper = this.selectComponent('#image-cropper');
            this.setData({
              src: newVal,
            });
            console.log('1111111111111');
            console.log(this.cropper);
          });
        }
      },
    },
    /**
     * 组件的初始数据
     */
    data: {
      src: '',
      width: 250, //宽度
      height: 250, //高度
      max_width: 300,
      max_height: 300,
      disable_rotate: true, //是否禁用旋转
      disable_ratio: false, //锁定比例
      limit_move: true, //是否限制移动
    },
    lifetimes: {
      attached() {},
    },
    /**
     * 组件的方法列表
     */
    methods: {
      cropperload(e) {
        console.log('cropper加载完成');
      },
      loadimage(e) {
        wx.hideLoading();
        console.log('图片');
        this.cropper.imgReset();
      },
      clickcut(e) {
        console.log(e.detail);
        //图片预览
        wx.previewImage({
          current: e.detail.url, // 当前显示图片的http链接
          urls: [e.detail.url], // 需要预览的图片http链接列表
        });
      },
      cancelCropper() {
        this.triggerEvent('cancelEvent');
      },
      confirmCropper() {
        this.cropper.getImg(obj => {
          this.triggerEvent('confirmEvent', obj.url);
        });
      },
      rotate() {
        //在用户旋转的基础上旋转90°
        this.cropper.setAngle((this.cropper.data.angle += 90));
      },
    },
  });
```

## File: components/authDialogNew/cropper/cropper.json
```json
{
    "component": true,
    "usingComponents": {}
  }
```

## File: components/authDialogNew/cropper/cropper.wxml
```
<view class="cropperContainer" wx:if="{{avatarUncropped}}">
  <view style="width:100%;height:500rpx;">
    <image-cropper id="image-cropper" bindload="cropperload" bindimageload="loadimage" bindtapcut="clickcut" limit_move="{{false}}" disable_rotate="{{true}}" width="{{width}}" height="{{height}}" imgSrc="{{src}}" angle="{{angle}}" disable_width="{{true}}" max_width="{{max_width}}" max_height="{{max_height}}" disable_height="{{true}}" disable_ratio="{{true}}"></image-cropper>
  </view>
  <text class="hint">点击中间裁剪框可查看裁剪后的图片</text>
  <view class='bottom'>
    <text class="btnText" catchtap='cancelCropper'>取消</text>
    <text class="btnText" catchtap='rotate'>旋转</text>
    <text class="btnText" catchtap='confirmCropper'>确认</text>
  </view>
</view>
```

## File: components/authDialogNew/cropper/cropper.wxss
```
.cropperContainer {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: black;
    z-index: 99999;
  }
  .top {
    position: absolute;
    width: 100%;
    top: 10rpx;
    display: flex;
    flex-flow: wrap;
    z-index: 10;
    color: white;
    justify-content: space-around;
  }
  
  .hint {
    position: absolute;
    top: 10rpx;
    width: 100%;
    font-size: 33rpx;
    text-align: center;
    color: white;
    z-index: 10;
  }
  
  page {
    background: white;
  }
  
  view {
    font-size: 30rpx;
  }
  
  .bottom {
    position: absolute;
    width: 100%;
    bottom: 50rpx;
    display: flex;
    z-index: 10;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
    height: 120rpx;
  }
  
  button {
    font-size: 27rpx;
    z-index: 2;
    padding: 0 20rpx;
    height: 60rpx;
    min-width: 70rpx;
    margin: 0 4rpx;
  }
  
  .input {
    display: flex;
    height: 50rpx;
    width: 50%;
  }
  
  .input>.label {
    min-width: 150rpx;
    font-size: 30rpx;
    height: 50rpx;
    line-height: 50rpx;
  }
  
  .input>input {
    margin-left: 10rpx;
    text-align: center;
    max-width: 160rpx;
    border: 1px solid rgb(255, 255, 255);
    height: 50rpx;
    line-height: 50rpx;
    min-height: 50rpx;
    box-sizing: border-box;
  }
  .btnText {
    font-size: 42rpx;
    color: #ffffff;
  }
```

## File: components/feedbackEntry/feedbackEntry.js
```javascript
Component({
    /**
     * 组件的属性列表
     */
    properties: {
        userId: {
            value: '',
            type: String
        },
    },
    observers: {
    },
    data: {
    },
    /**
     * 组件的方法列表
     */
    methods: {
        // 跳转到反馈页面
        toFeedback() {
            wx.navigateTo({
                url: '/pages/feedback/feedback?userId=' + this.properties.userId,
            });
        },
    }
})
```

## File: components/feedbackEntry/feedbackEntry.json
```json
{
    "component": true
}
```

## File: components/feedbackEntry/feedbackEntry.wxml
```
<view class="feedbackEntry" bindtap="toFeedback">
    <image src="../../assets/image/icon/kefuIcon.png" class="kefuIcon" />
    反馈投诉
</view>
```

## File: components/feedbackEntry/feedbackEntry.wxss
```
.feedbackEntry {
    width: 147rpx;
    height: 58rpx;
    background-color: rgba(0, 0, 0, 0.6);
    display: flex;
    align-items: center;
    border-top-left-radius: 25rpx;
    border-bottom-left-radius: 25rpx;
    position: fixed;
    top: 48rpx;
    right: 0;
    font-size: 24rpx;
    color: #ffe2ce;
    padding: 0 8rpx 0 13rpx;
    /* 最高层级 */
    z-index: 9999;
}

.feedbackEntry>.kefuIcon {
    width: 24rpx;
    height: 24rpx;
    margin-right: 4rpx;
}
```

## File: components/image-cropper/image-cropper.js
```javascript
Component({
    properties: {
        /**     
         * 图片路径
         */
        'imgSrc': {
            type: String
        },
        /**
         * 裁剪框高度
         */
        'height': {
            type: Number,
            value: 200
        },
        /**
         * 裁剪框宽度
         */
        'width': {
            type: Number,
            value: 200
        },
        /**
         * 裁剪框最小尺寸
         */
        'min_width': {
            type: Number,
            value: 100
        },
        'min_height': {
            type: Number,
            value: 100
        },
        /**
         * 裁剪框最大尺寸
         */
        'max_width': {
            type: Number,
            value: 300
        },
        'max_height': {
            type: Number,
            value: 300
        },
        /**
         * 裁剪框禁止拖动
         */
        'disable_width': {
            type: Boolean,
            value: false
        },
        'disable_height': {
            type: Boolean,
            value: false
        },
        /**
         * 锁定裁剪框比例
         */
        'disable_ratio': {
            type: Boolean,
            value: false
        },
        /**
         * 生成的图片尺寸相对剪裁框的比例
         */
        'export_scale': {
            type: Number,
            value: 3
        },
        /**
         * 生成的图片质量0-1
         */
        'quality': {
            type: Number,
            value: 1
        },
        'cut_top': {
            type: Number,
            value: null
        },
        'cut_left': {
            type: Number,
            value: null
        },
        /**
         * canvas上边距（不设置默认不显示）
         */
        'canvas_top': {
            type: Number,
            value: null
        },
        /**
         * canvas左边距（不设置默认不显示）
         */
        'canvas_left': {
            type: Number,
            value: null
        },
        /**
         * 图片宽度
         */
        'img_width': {
            type: null,
            value: null
        },
        /**
         * 图片高度
         */
        'img_height': {
            type: null,
            value: null
        },
        /**
         * 图片缩放比
         */
        'scale': {
            type: Number,
            value: 1
        },
        /**
         * 图片旋转角度
         */
        'angle': {
            type: Number,
            value: 0
        },
        /**
         * 最小缩放比
         */
        'min_scale': {
            type: Number,
            value: 0.5
        },
        /**
         * 最大缩放比
         */
        'max_scale': {
            type: Number,
            value: 2
        },
        /**
         * 是否禁用旋转
         */
        'disable_rotate': {
            type: Boolean,
            value: false
        },
        /**
         * 是否限制移动范围(剪裁框只能在图片内)
         */
        'limit_move': {
            type: Boolean,
            value: false
        }
    },
    data: {
        el: 'image-cropper', //暂时无用
        info: wx.getSystemInfoSync(),
        MOVE_THROTTLE: null, //触摸移动节流settimeout
        MOVE_THROTTLE_FLAG: true, //节流标识
        INIT_IMGWIDTH: 0, //图片设置尺寸,此值不变（记录最初设定的尺寸）
        INIT_IMGHEIGHT: 0, //图片设置尺寸,此值不变（记录最初设定的尺寸）
        TIME_BG: null, //背景变暗延时函数
        TIME_CUT_CENTER: null,
        _touch_img_relative: [{
            x: 0,
            y: 0
        }], //鼠标和图片中心的相对位置
        _flag_cut_touch: false, //是否是拖动裁剪框
        _hypotenuse_length: 0, //双指触摸时斜边长度
        _flag_img_endtouch: false, //是否结束触摸
        _flag_bright: true, //背景是否亮
        _canvas_overflow: true, //canvas缩略图是否在屏幕外面
        _canvas_width: 200,
        _canvas_height: 200,
        origin_x: 0.5, //图片旋转中心
        origin_y: 0.5, //图片旋转中心
        _cut_animation: false, //是否开启图片和裁剪框过渡
        _img_top: wx.getSystemInfoSync().windowHeight / 2, //图片上边距
        _img_left: wx.getSystemInfoSync().windowWidth / 2, //图片左边距
        watch: {
            //监听截取框宽高变化
            width(value, that) {
                    if (value < that.data.min_width) {
                        that.setData({
                            width: that.data.min_width
                        });
                    }
                    that._computeCutSize();
                },
                height(value, that) {
                    if (value < that.data.min_height) {
                        that.setData({
                            height: that.data.min_height
                        });
                    }
                    that._computeCutSize();
                },
                angle(value, that) {
                    //停止居中裁剪框，继续修改图片位置
                    that._moveStop();
                    if (that.data.limit_move) {
                        if (that.data.angle % 90) {
                            that.setData({
                                angle: Math.round(that.data.angle / 90) * 90
                            });
                            return;
                        }
                    }
                },
                _cut_animation(value, that) {
                    //开启过渡300毫秒之后自动关闭
                    clearTimeout(that.data._cut_animation_time);
                    if (value) {
                        that.data._cut_animation_time = setTimeout(() => {
                            that.setData({
                                _cut_animation: false
                            });
                        }, 300)
                    }
                },
                limit_move(value, that) {
                    if (value) {
                        if (that.data.angle % 90) {
                            that.setData({
                                angle: Math.round(that.data.angle / 90) * 90
                            });
                        }
                        that._imgMarginDetectionScale();
                        !that.data._canvas_overflow && that._draw();
                    }
                },
                canvas_top(value, that) {
                    that._canvasDetectionPosition();
                },
                canvas_left(value, that) {
                    that._canvasDetectionPosition();
                },
                imgSrc(value, that) {
                    that.pushImg();
                },
                cut_top(value, that) {
                    that._cutDetectionPosition();
                    if (that.data.limit_move) {
                        !that.data._canvas_overflow && that._draw();
                    }
                },
                cut_left(value, that) {
                    that._cutDetectionPosition();
                    if (that.data.limit_move) {
                        !that.data._canvas_overflow && that._draw();
                    }
                }
        }
    },
    attached() {
        this.data.info = wx.getSystemInfoSync();
        //启用数据监听
        this._watcher();
        this.data.INIT_IMGWIDTH = this.data.img_width;
        this.data.INIT_IMGHEIGHT = this.data.img_height;
        this.setData({
            _canvas_height: this.data.height,
            _canvas_width: this.data.width,
        });
        this._initCanvas();
        this.data.imgSrc && (this.data.imgSrc = this.data.imgSrc);
        //根据开发者设置的图片目标尺寸计算实际尺寸
        this._initImageSize();
        //设置裁剪框大小>设置图片尺寸>绘制canvas
        this._computeCutSize();
        //检查裁剪框是否在范围内
        this._cutDetectionPosition();
        //检查canvas是否在范围内
        this._canvasDetectionPosition();
        //初始化完成
        this.triggerEvent('load', {
            cropper: this
        });
    },
    methods: {
        /**
         * 上传图片
         */
        upload() {
                let that = this;
                wx.chooseImage({
                    count: 1,
                    sizeType: ['original', 'compressed'],
                    sourceType: ['album', 'camera'],
                    success(res) {
                        const tempFilePaths = res.tempFilePaths[0];
                        that.pushImg(tempFilePaths);
                        wx.showLoading({
                            title: '加载中...'
                        })
                    }
                })
            },
            /**
             * 返回图片信息
             */
            getImg(getCallback) {
                this._draw(() => {
                    wx.canvasToTempFilePath({
                        width: this.data.width * this.data.export_scale,
                        height: Math.round(this.data.height * this.data.export_scale),
                        destWidth: this.data.width * this.data.export_scale,
                        destHeight: Math.round(this.data.height) * this.data.export_scale,
                        fileType: 'png',
                        quality: this.data.quality,
                        canvasId: this.data.el,
                        success: (res) => {
                            getCallback({
                                url: res.tempFilePath,
                                width: this.data.width * this.data.export_scale,
                                height: this.data.height * this.data.export_scale
                            });
                        }
                    }, this)
                });
            },
            /**
             * 设置图片动画
             * {
             *    x:10,//图片在原有基础上向下移动10px
             *    y:10,//图片在原有基础上向右移动10px
             *    angle:10,//图片在原有基础上旋转10deg
             *    scale:0.5,//图片在原有基础上增加0.5倍
             * }
             */
            setTransform(transform) {
                if (!transform) return;
                if (!this.data.disable_rotate) {
                    this.setData({
                        angle: transform.angle ? this.data.angle + transform.angle : this.data.angle
                    });
                }
                var scale = this.data.scale;
                if (transform.scale) {
                    scale = this.data.scale + transform.scale;
                    scale = scale <= this.data.min_scale ? this.data.min_scale : scale;
                    scale = scale >= this.data.max_scale ? this.data.max_scale : scale;
                }
                this.data.scale = scale;
                let cutX = this.data.cut_left;
                let cutY = this.data.cut_top;
                if (transform.cutX) {
                    this.setData({
                        cut_left: cutX + transform.cutX
                    });
                    this.data.watch.cut_left(null, this);
                }
                if (transform.cutY) {
                    this.setData({
                        cut_top: cutY + transform.cutY
                    });
                    this.data.watch.cut_top(null, this);
                }
                this.data._img_top = transform.y ? this.data._img_top + transform.y : this.data._img_top;
                this.data._img_left = transform.x ? this.data._img_left + transform.x : this.data._img_left;
                //图像边缘检测,防止截取到空白
                this._imgMarginDetectionScale();
                //停止居中裁剪框，继续修改图片位置
                this._moveDuring();
                this.setData({
                    scale: this.data.scale,
                    _img_top: this.data._img_top,
                    _img_left: this.data._img_left
                });
                !this.data._canvas_overflow && this._draw();
                //可以居中裁剪框了
                this._moveStop(); //结束操作
            },
            /**
             * 设置剪裁框位置
             */
            setCutXY(x, y) {
                this.setData({
                    cut_top: y,
                    cut_left: x
                });
            },
            /**
             * 设置剪裁框尺寸
             */
            setCutSize(w, h) {
                this.setData({
                    width: w,
                    height: h
                });
                this._computeCutSize();
            },
            /**
             * 设置剪裁框和图片居中
             */
            setCutCenter() {
                let cut_top = (this.data.info.windowHeight - this.data.height) * 0.5;
                let cut_left = (this.data.info.windowWidth - this.data.width) * 0.5;
                //顺序不能变
                this.setData({
                    _img_top: this.data._img_top - this.data.cut_top + cut_top,
                    cut_top: cut_top, //截取的框上边距
                    _img_left: this.data._img_left - this.data.cut_left + cut_left,
                    cut_left: cut_left, //截取的框左边距
                });
            },
            _setCutCenter() {
                let cut_top = (this.data.info.windowHeight - this.data.height) * 0.5;
                let cut_left = (this.data.info.windowWidth - this.data.width) * 0.5;
                this.setData({
                    cut_top: cut_top, //截取的框上边距
                    cut_left: cut_left, //截取的框左边距
                });
            },
            /**
             * 设置剪裁框宽度-即将废弃
             */
            setWidth(width) {
                this.setData({
                    width: width
                });
                this._computeCutSize();
            },
            /**
             * 设置剪裁框高度-即将废弃
             */
            setHeight(height) {
                this.setData({
                    height: height
                });
                this._computeCutSize();
            },
            /**
             * 是否锁定旋转
             */
            setDisableRotate(value) {
                this.data.disable_rotate = value;
            },
            /**
             * 是否限制移动
             */
            setLimitMove(value) {
                this.setData({
                    _cut_animation: true,
                    limit_move: !!value
                });
            },
            /**
             * 初始化图片，包括位置、大小、旋转角度
             */
            imgReset() {
                this.setData({
                    scale: 1,
                    angle: 0,
                    _img_top: wx.getSystemInfoSync().windowHeight / 2,
                    _img_left: wx.getSystemInfoSync().windowWidth / 2,
                })
            },
            /**
             * 加载（更换）图片
             */
            pushImg(src) {
                if (src) {
                    this.setData({
                        imgSrc: src
                    });
                    //发现是手动赋值直接返回，交给watch处理
                    return;
                }

                // getImageInfo接口传入 src: '' 会导致内存泄漏

                if (!this.data.imgSrc) return;
                wx.getImageInfo({
                    src: this.data.imgSrc,
                    success: (res) => {
                            this.data.imageObject = res;
                            //图片非本地路径需要换成本地路径
                            if (this.data.imgSrc.search(/tmp/) == -1) {
                                this.setData({
                                    imgSrc: res.path
                                });
                            }
                            //计算最后图片尺寸
                            this._imgComputeSize();
                            if (this.data.limit_move) {
                                //限制移动，不留空白处理
                                this._imgMarginDetectionScale();
                            }
                            this._draw();
                        },
                        fail: (err) => {
                            this.setData({
                                imgSrc: ''
                            });
                        }
                });
            },
            imageLoad(e) {
                setTimeout(() => {
                    this.triggerEvent('imageload', this.data.imageObject);

                }, 1000)
            },
            /**
             * 设置图片放大缩小
             */
            setScale(scale) {
                if (!scale) return;
                this.setData({
                    scale: scale
                });
                !this.data._canvas_overflow && this._draw();
            },
            /**
             * 设置图片旋转角度
             */
            setAngle(angle) {
                if (!angle) return;
                this.setData({
                    _cut_animation: true,
                    angle: angle
                });
                this._imgMarginDetectionScale();
                !this.data._canvas_overflow && this._draw();
            },
            _initCanvas() {
                //初始化canvas
                if (!this.data.ctx) {
                    this.data.ctx = wx.createCanvasContext("image-cropper", this);
                }
            },
            /**
             * 根据开发者设置的图片目标尺寸计算实际尺寸
             */
            _initImageSize() {
                //处理宽高特殊单位 %>px
                if (this.data.INIT_IMGWIDTH && typeof this.data.INIT_IMGWIDTH == "string" && this.data.INIT_IMGWIDTH.indexOf("%") != -1) {
                    let width = this.data.INIT_IMGWIDTH.replace("%", "");
                    this.data.INIT_IMGWIDTH = this.data.img_width = this.data.info.windowWidth / 100 * width;
                }
                if (this.data.INIT_IMGHEIGHT && typeof this.data.INIT_IMGHEIGHT == "string" && this.data.INIT_IMGHEIGHT.indexOf("%") != -1) {
                    let height = this.data.img_height.replace("%", "");
                    this.data.INIT_IMGHEIGHT = this.data.img_height = this.data.info.windowHeight / 100 * height;
                }
            },
            /**
             * 检测剪裁框位置是否在允许的范围内(屏幕内)
             */
            _cutDetectionPosition() {
                let _cutDetectionPositionTop = () => {
                        //检测上边距是否在范围内
                        if (this.data.cut_top < 0) {
                            this.setData({
                                cut_top: 0
                            });
                        }
                        if (this.data.cut_top > this.data.info.windowHeight - this.data.height) {
                            this.setData({
                                cut_top: this.data.info.windowHeight - this.data.height
                            });
                        }
                    },
                    _cutDetectionPositionLeft = () => {
                        //检测左边距是否在范围内
                        if (this.data.cut_left < 0) {
                            this.setData({
                                cut_left: 0
                            });
                        }
                        if (this.data.cut_left > this.data.info.windowWidth - this.data.width) {
                            this.setData({
                                cut_left: this.data.info.windowWidth - this.data.width
                            });
                        }
                    };
                //裁剪框坐标处理（如果只写一个参数则另一个默认为0，都不写默认居中）
                if (this.data.cut_top == null && this.data.cut_left == null) {
                    this._setCutCenter();
                } else if (this.data.cut_top != null && this.data.cut_left != null) {
                    _cutDetectionPositionTop();
                    _cutDetectionPositionLeft();
                } else if (this.data.cut_top != null && this.data.cut_left == null) {
                    _cutDetectionPositionTop();
                    this.setData({
                        cut_left: (this.data.info.windowWidth - this.data.width) / 2
                    });
                } else if (this.data.cut_top == null && this.data.cut_left != null) {
                    _cutDetectionPositionLeft();
                    this.setData({
                        cut_top: (this.data.info.windowHeight - this.data.height) / 2
                    });
                }
            },
            /**
             * 检测canvas位置是否在允许的范围内(屏幕内)如果在屏幕外则不开启实时渲染
             * 如果只写一个参数则另一个默认为0，都不写默认超出屏幕外
             */
            _canvasDetectionPosition() {
                if (this.data.canvas_top == null && this.data.canvas_left == null) {
                    this.data._canvas_overflow = false;
                    this.setData({
                        canvas_top: -5000,
                        canvas_left: -5000
                    });
                } else if (this.data.canvas_top != null && this.data.canvas_left != null) {
                    if (this.data.canvas_top < -this.data.height || this.data.canvas_top > this.data.info.windowHeight) {
                        this.data._canvas_overflow = true;
                    } else {
                        this.data._canvas_overflow = false;
                    }
                } else if (this.data.canvas_top != null && this.data.canvas_left == null) {
                    this.setData({
                        canvas_left: 0
                    });
                } else if (this.data.canvas_top == null && this.data.canvas_left != null) {
                    this.setData({
                        canvas_top: 0
                    });
                    if (this.data.canvas_left < -this.data.width || this.data.canvas_left > this.data.info.windowWidth) {
                        this.data._canvas_overflow = true;
                    } else {
                        this.data._canvas_overflow = false;
                    }
                }
            },
            /**
             * 图片边缘检测-位置
             */
            _imgMarginDetectionPosition(scale) {
                if (!this.data.limit_move) return;
                let left = this.data._img_left;
                let top = this.data._img_top;
                var scale = scale || this.data.scale;
                let img_width = this.data.img_width;
                let img_height = this.data.img_height;
                if (this.data.angle / 90 % 2) {
                    img_width = this.data.img_height;
                    img_height = this.data.img_width;
                }
                left = this.data.cut_left + img_width * scale / 2 >= left ? left : this.data.cut_left + img_width * scale / 2;
                left = this.data.cut_left + this.data.width - img_width * scale / 2 <= left ? left : this.data.cut_left + this.data.width - img_width * scale / 2;
                top = this.data.cut_top + img_height * scale / 2 >= top ? top : this.data.cut_top + img_height * scale / 2;
                top = this.data.cut_top + this.data.height - img_height * scale / 2 <= top ? top : this.data.cut_top + this.data.height - img_height * scale / 2;
                this.setData({
                    _img_left: left,
                    _img_top: top,
                    scale: scale
                })
            },
            /**
             * 图片边缘检测-缩放
             */
            _imgMarginDetectionScale() {
                if (!this.data.limit_move) return;
                let scale = this.data.scale;
                let img_width = this.data.img_width;
                let img_height = this.data.img_height;
                if (this.data.angle / 90 % 2) {
                    img_width = this.data.img_height;
                    img_height = this.data.img_width;
                }
                if (img_width * scale < this.data.width) {
                    scale = this.data.width / img_width;
                }
                if (img_height * scale < this.data.height) {
                    scale = Math.max(scale, this.data.height / img_height);
                }
                this._imgMarginDetectionPosition(scale);
            },
            _setData(obj) {
                let data = {};
                for (var key in obj) {
                    if (this.data[key] != obj[key]) {
                        data[key] = obj[key];
                    }
                }
                this.setData(data);
                return data;
            },
            /**
             * 计算图片尺寸
             */
            _imgComputeSize() {
                let img_width = this.data.img_width,
                    img_height = this.data.img_height;
                if (!this.data.INIT_IMGHEIGHT && !this.data.INIT_IMGWIDTH) {
                    //默认按图片最小边 = 对应裁剪框尺寸
                    img_width = this.data.imageObject.width;
                    img_height = this.data.imageObject.height;
                    if (img_width / img_height > this.data.width / this.data.height) {
                        img_height = this.data.height;
                        img_width = this.data.imageObject.width / this.data.imageObject.height * img_height;
                    } else {
                        img_width = this.data.width;
                        img_height = this.data.imageObject.height / this.data.imageObject.width * img_width;
                    }
                } else if (this.data.INIT_IMGHEIGHT && !this.data.INIT_IMGWIDTH) {
                    img_width = this.data.imageObject.width / this.data.imageObject.height * this.data.INIT_IMGHEIGHT;
                } else if (!this.data.INIT_IMGHEIGHT && this.data.INIT_IMGWIDTH) {
                    img_height = this.data.imageObject.height / this.data.imageObject.width * this.data.INIT_IMGWIDTH;
                }
                this.setData({
                    img_width: img_width,
                    img_height: img_height
                });
            },
            //改变截取框大小
            _computeCutSize() {
                if (this.data.width > this.data.info.windowWidth) {
                    this.setData({
                        width: this.data.info.windowWidth,
                    });
                } else if (this.data.width + this.data.cut_left > this.data.info.windowWidth) {
                    this.setData({
                        cut_left: this.data.info.windowWidth - this.data.cut_left,
                    });
                };
                if (this.data.height > this.data.info.windowHeight) {
                    this.setData({
                        height: this.data.info.windowHeight,
                    });
                } else if (this.data.height + this.data.cut_top > this.data.info.windowHeight) {
                    this.setData({
                        cut_top: this.data.info.windowHeight - this.data.cut_top,
                    });
                }!this.data._canvas_overflow && this._draw();
            },
            //开始触摸
            _start(event) {
                this.data._flag_img_endtouch = false;
                if (event.touches.length == 1) {
                    //单指拖动
                    this.data._touch_img_relative[0] = {
                        x: (event.touches[0].clientX - this.data._img_left),
                        y: (event.touches[0].clientY - this.data._img_top)
                    }
                } else {
                    //双指放大
                    let width = Math.abs(event.touches[0].clientX - event.touches[1].clientX);
                    let height = Math.abs(event.touches[0].clientY - event.touches[1].clientY);
                    this.data._touch_img_relative = [{
                        x: (event.touches[0].clientX - this.data._img_left),
                        y: (event.touches[0].clientY - this.data._img_top)
                    }, {
                        x: (event.touches[1].clientX - this.data._img_left),
                        y: (event.touches[1].clientY - this.data._img_top)
                    }];
                    this.data._hypotenuse_length = Math.sqrt(Math.pow(width, 2) + Math.pow(height, 2));
                }!this.data._canvas_overflow && this._draw();
            },
            _move_throttle() {
                //安卓需要节流
                if (this.data.info.platform == 'android') {
                    clearTimeout(this.data.MOVE_THROTTLE);
                    this.data.MOVE_THROTTLE = setTimeout(() => {
                        this.data.MOVE_THROTTLE_FLAG = true;
                    }, 1000 / 40)
                    return this.data.MOVE_THROTTLE_FLAG;
                } else {
                    this.data.MOVE_THROTTLE_FLAG = true;
                }
            },
            _move(event) {
                if (this.data._flag_img_endtouch || !this.data.MOVE_THROTTLE_FLAG) return;
                this.data.MOVE_THROTTLE_FLAG = false;
                this._move_throttle();
                this._moveDuring();
                if (event.touches.length == 1) {
                    //单指拖动
                    let left = (event.touches[0].clientX - this.data._touch_img_relative[0].x),
                        top = (event.touches[0].clientY - this.data._touch_img_relative[0].y);
                    //图像边缘检测,防止截取到空白
                    this.data._img_left = left;
                    this.data._img_top = top;
                    this._imgMarginDetectionPosition();
                    this.setData({
                        _img_left: this.data._img_left,
                        _img_top: this.data._img_top
                    });
                } else {
                    //双指放大
                    let width = (Math.abs(event.touches[0].clientX - event.touches[1].clientX)),
                        height = (Math.abs(event.touches[0].clientY - event.touches[1].clientY)),
                        hypotenuse = Math.sqrt(Math.pow(width, 2) + Math.pow(height, 2)),
                        scale = this.data.scale * (hypotenuse / this.data._hypotenuse_length),
                        current_deg = 0;
                    scale = scale <= this.data.min_scale ? this.data.min_scale : scale;
                    scale = scale >= this.data.max_scale ? this.data.max_scale : scale;
                    //图像边缘检测,防止截取到空白
                    this.data.scale = scale;
                    this._imgMarginDetectionScale();
                    //双指旋转(如果没禁用旋转)
                    let _touch_img_relative = [{
                        x: (event.touches[0].clientX - this.data._img_left),
                        y: (event.touches[0].clientY - this.data._img_top)
                    }, {
                        x: (event.touches[1].clientX - this.data._img_left),
                        y: (event.touches[1].clientY - this.data._img_top)
                    }];
                    if (!this.data.disable_rotate) {
                        let first_atan = 180 / Math.PI * Math.atan2(_touch_img_relative[0].y, _touch_img_relative[0].x);
                        let first_atan_old = 180 / Math.PI * Math.atan2(this.data._touch_img_relative[0].y, this.data._touch_img_relative[0].x);
                        let second_atan = 180 / Math.PI * Math.atan2(_touch_img_relative[1].y, _touch_img_relative[1].x);
                        let second_atan_old = 180 / Math.PI * Math.atan2(this.data._touch_img_relative[1].y, this.data._touch_img_relative[1].x);
                        //当前旋转的角度
                        let first_deg = first_atan - first_atan_old,
                            second_deg = second_atan - second_atan_old;
                        if (first_deg != 0) {
                            current_deg = first_deg;
                        } else if (second_deg != 0) {
                            current_deg = second_deg;
                        }
                    }
                    this.data._touch_img_relative = _touch_img_relative;
                    this.data._hypotenuse_length = Math.sqrt(Math.pow(width, 2) + Math.pow(height, 2));
                    //更新视图
                    this.setData({
                        angle: this.data.angle + current_deg,
                        scale: this.data.scale
                    });
                }!this.data._canvas_overflow && this._draw();
            },
            //结束操作
            _end(event) {
                this.data._flag_img_endtouch = true;
                this._moveStop();
            },
            //点击中间剪裁框处理
            _click(event) {
                if (!this.data.imgSrc) {
                    //调起上传
                    this.upload();
                    return;
                }
                this._draw(() => {
                    let x = event.detail ? event.detail.x : event.touches[0].clientX;
                    let y = event.detail ? event.detail.y : event.touches[0].clientY;
                    if ((x >= this.data.cut_left && x <= (this.data.cut_left + this.data.width)) && (y >= this.data.cut_top && y <= (this.data.cut_top + this.data.height))) {
                        //生成图片并回调
                        wx.canvasToTempFilePath({
                            width: this.data.width * this.data.export_scale,
                            height: Math.round(this.data.height * this.data.export_scale),
                            destWidth: this.data.width * this.data.export_scale,
                            destHeight: Math.round(this.data.height) * this.data.export_scale,
                            fileType: 'png',
                            quality: this.data.quality,
                            canvasId: this.data.el,
                            success: (res) => {
                                this.triggerEvent('tapcut', {
                                    url: res.tempFilePath,
                                    width: this.data.width * this.data.export_scale,
                                    height: this.data.height * this.data.export_scale
                                });
                            }
                        }, this)
                    }
                });
            },
            //渲染
            _draw(callback) {
                if (!this.data.imgSrc) return;
                let draw = () => {
                    //图片实际大小
                    let img_width = this.data.img_width * this.data.scale * this.data.export_scale;
                    let img_height = this.data.img_height * this.data.scale * this.data.export_scale;
                    //canvas和图片的相对距离
                    var xpos = this.data._img_left - this.data.cut_left;
                    var ypos = this.data._img_top - this.data.cut_top;
                    //旋转画布
                    this.data.ctx.translate(xpos * this.data.export_scale, ypos * this.data.export_scale);
                    this.data.ctx.rotate(this.data.angle * Math.PI / 180);
                    this.data.ctx.drawImage(this.data.imgSrc, -img_width / 2, -img_height / 2, img_width, img_height);
                    this.data.ctx.draw(false, () => {
                        callback && callback();
                    });
                }
                if (this.data.ctx.width != this.data.width || this.data.ctx.height != this.data.height) {
                    //优化拖动裁剪框，所以必须把宽高设置放在离用户触发渲染最近的地方
                    this.setData({
                        _canvas_height: this.data.height,
                        _canvas_width: this.data.width,
                    }, () => {
                        //延迟40毫秒防止点击过快出现拉伸或裁剪过多
                        setTimeout(() => {
                            draw();
                        }, 40);
                    });
                } else {
                    draw();
                }
            },
            //裁剪框处理
            _cutTouchMove(e) {
                if (this.data._flag_cut_touch && this.data.MOVE_THROTTLE_FLAG) {
                    if (this.data.disable_ratio && (this.data.disable_width || this.data.disable_height)) return;
                    //节流
                    this.data.MOVE_THROTTLE_FLAG = false;
                    this._move_throttle();
                    let width = this.data.width,
                        height = this.data.height,
                        cut_top = this.data.cut_top,
                        cut_left = this.data.cut_left,
                        size_correct = () => {
                            width = width <= this.data.max_width ? width >= this.data.min_width ? width : this.data.min_width : this.data.max_width;
                            height = height <= this.data.max_height ? height >= this.data.min_height ? height : this.data.min_height : this.data.max_height;
                        },
                        size_inspect = () => {
                            if ((width > this.data.max_width || width < this.data.min_width || height > this.data.max_height || height < this.data.min_height) && this.data.disable_ratio) {
                                size_correct();
                                return false;
                            } else {
                                size_correct();
                                return true;
                            }
                        };
                    height = this.data.CUT_START.height + ((this.data.CUT_START.corner > 1 && this.data.CUT_START.corner < 4 ? 1 : -1) * (this.data.CUT_START.y - e.touches[0].clientY));
                    switch (this.data.CUT_START.corner) {
                    case 1:
                        width = this.data.CUT_START.width + this.data.CUT_START.x - e.touches[0].clientX;
                        if (this.data.disable_ratio) {
                            height = width / (this.data.width / this.data.height)
                        }
                        if (!size_inspect()) return;
                        cut_left = this.data.CUT_START.cut_left - (width - this.data.CUT_START.width);
                        break
                    case 2:
                        width = this.data.CUT_START.width + this.data.CUT_START.x - e.touches[0].clientX;
                        if (this.data.disable_ratio) {
                            height = width / (this.data.width / this.data.height)
                        }
                        if (!size_inspect()) return;
                        cut_top = this.data.CUT_START.cut_top - (height - this.data.CUT_START.height)
                        cut_left = this.data.CUT_START.cut_left - (width - this.data.CUT_START.width)
                        break
                    case 3:
                        width = this.data.CUT_START.width - this.data.CUT_START.x + e.touches[0].clientX;
                        if (this.data.disable_ratio) {
                            height = width / (this.data.width / this.data.height)
                        }
                        if (!size_inspect()) return;
                        cut_top = this.data.CUT_START.cut_top - (height - this.data.CUT_START.height);
                        break
                    case 4:
                        width = this.data.CUT_START.width - this.data.CUT_START.x + e.touches[0].clientX;
                        if (this.data.disable_ratio) {
                            height = width / (this.data.width / this.data.height)
                        }
                        if (!size_inspect()) return;
                        break
                    }
                    if (!this.data.disable_width && !this.data.disable_height) {
                        this.setData({
                            width: width,
                            cut_left: cut_left,
                            height: height,
                            cut_top: cut_top,
                        })
                    } else if (!this.data.disable_width) {
                        this.setData({
                            width: width,
                            cut_left: cut_left
                        })
                    } else if (!this.data.disable_height) {
                        this.setData({
                            height: height,
                            cut_top: cut_top
                        })
                    }
                    this._imgMarginDetectionScale();
                }
            },
            _cutTouchStart(e) {
                let currentX = e.touches[0].clientX;
                let currentY = e.touches[0].clientY;
                let cutbox_top4 = this.data.cut_top + this.data.height - 30;
                let cutbox_bottom4 = this.data.cut_top + this.data.height + 20;
                let cutbox_left4 = this.data.cut_left + this.data.width - 30;
                let cutbox_right4 = this.data.cut_left + this.data.width + 30;

                let cutbox_top3 = this.data.cut_top - 30;
                let cutbox_bottom3 = this.data.cut_top + 30;
                let cutbox_left3 = this.data.cut_left + this.data.width - 30;
                let cutbox_right3 = this.data.cut_left + this.data.width + 30;

                let cutbox_top2 = this.data.cut_top - 30;
                let cutbox_bottom2 = this.data.cut_top + 30;
                let cutbox_left2 = this.data.cut_left - 30;
                let cutbox_right2 = this.data.cut_left + 30;

                let cutbox_top1 = this.data.cut_top + this.data.height - 30;
                let cutbox_bottom1 = this.data.cut_top + this.data.height + 30;
                let cutbox_left1 = this.data.cut_left - 30;
                let cutbox_right1 = this.data.cut_left + 30;
                if (currentX > cutbox_left4 && currentX < cutbox_right4 && currentY > cutbox_top4 && currentY < cutbox_bottom4) {
                    this._moveDuring();
                    this.data._flag_cut_touch = true;
                    this.data._flag_img_endtouch = true;
                    this.data.CUT_START = {
                        width: this.data.width,
                        height: this.data.height,
                        x: currentX,
                        y: currentY,
                        corner: 4
                    }
                } else if (currentX > cutbox_left3 && currentX < cutbox_right3 && currentY > cutbox_top3 && currentY < cutbox_bottom3) {
                    this._moveDuring();
                    this.data._flag_cut_touch = true;
                    this.data._flag_img_endtouch = true;
                    this.data.CUT_START = {
                        width: this.data.width,
                        height: this.data.height,
                        x: currentX,
                        y: currentY,
                        cut_top: this.data.cut_top,
                        cut_left: this.data.cut_left,
                        corner: 3
                    }
                } else if (currentX > cutbox_left2 && currentX < cutbox_right2 && currentY > cutbox_top2 && currentY < cutbox_bottom2) {
                    this._moveDuring();
                    this.data._flag_cut_touch = true;
                    this.data._flag_img_endtouch = true;
                    this.data.CUT_START = {
                        width: this.data.width,
                        height: this.data.height,
                        cut_top: this.data.cut_top,
                        cut_left: this.data.cut_left,
                        x: currentX,
                        y: currentY,
                        corner: 2
                    }
                } else if (currentX > cutbox_left1 && currentX < cutbox_right1 && currentY > cutbox_top1 && currentY < cutbox_bottom1) {
                    this._moveDuring();
                    this.data._flag_cut_touch = true;
                    this.data._flag_img_endtouch = true;
                    this.data.CUT_START = {
                        width: this.data.width,
                        height: this.data.height,
                        cut_top: this.data.cut_top,
                        cut_left: this.data.cut_left,
                        x: currentX,
                        y: currentY,
                        corner: 1
                    }
                }
            },
            _cutTouchEnd(e) {
                this._moveStop();
                this.data._flag_cut_touch = false;
            },
            //停止移动时需要做的操作
            _moveStop() {
                //清空之前的自动居中延迟函数并添加最新的
                clearTimeout(this.data.TIME_CUT_CENTER);
                this.data.TIME_CUT_CENTER = setTimeout(() => {
                        //动画启动
                        if (!this.data._cut_animation) {
                            this.setData({
                                _cut_animation: true
                            });
                        }
                        this.setCutCenter();
                    }, 1000)
                    //清空之前的背景变化延迟函数并添加最新的
                clearTimeout(this.data.TIME_BG);
                this.data.TIME_BG = setTimeout(() => {
                    if (this.data._flag_bright) {
                        this.setData({
                            _flag_bright: false
                        });
                    }
                }, 2000)
            },
            //移动中
            _moveDuring() {
                //清空之前的自动居中延迟函数
                clearTimeout(this.data.TIME_CUT_CENTER);
                //清空之前的背景变化延迟函数
                clearTimeout(this.data.TIME_BG);
                //高亮背景
                if (!this.data._flag_bright) {
                    this.setData({
                        _flag_bright: true
                    });
                }
            },
            //监听器
            _watcher() {
                Object.keys(this.data).forEach(v => {
                    this._observe(this.data, v, this.data.watch[v]);
                })
            },
            _observe(obj, key, watchFun) {
                var val = obj[key];
                Object.defineProperty(obj, key, {
                    configurable: true,
                    enumerable: true,
                    set: (value) => {
                            val = value;
                            watchFun && watchFun(val, this);
                        },
                        get() {
                            if (val && '_img_top|img_left||width|height|min_width|max_width|min_height|max_height|export_scale|cut_top|cut_left|canvas_top|canvas_left|img_width|img_height|scale|angle|min_scale|max_scale'.indexOf(key) != -1) {
                                let ret = parseFloat(parseFloat(val).toFixed(3));
                                if (typeof val == "string" && val.indexOf("%") != -1) {
                                    ret += '%';
                                }
                                return ret;
                            }
                            return val;
                        }
                })
            },
            _preventTouchMove() {}
    }
})
```

## File: components/image-cropper/image-cropper.json
```json
{
	"component": true
}
```

## File: components/image-cropper/image-cropper.wxml
```
<view class='image-cropper' catchtouchmove='_preventTouchMove'>
    <view class='main' bindtouchend="_cutTouchEnd" bindtouchstart="_cutTouchStart" bindtouchmove="_cutTouchMove" bindtap="_click">
        <view class='content'>
            <view class='content_top bg_gray {{_flag_bright?"":"bg_black"}}' style="height:{{cut_top}}px;transition-property:{{_cut_animation?'':'background'}}"></view>
            <view class='content_middle' style="height:{{height}}px;">
                <view class='content_middle_left bg_gray {{_flag_bright?"":"bg_black"}}' style="width:{{cut_left}}px;transition-property:{{_cut_animation?'':'background'}}"></view>
                <view class='content_middle_middle' style="width:{{width}}px;height:{{height}}px;transition-duration: .3s;transition-property:{{_cut_animation?'':'background'}};">
                    <view class="border border-top-left"></view>
                    <view class="border border-top-right"></view>
                    <view class="border border-right-top"></view>
                    <view class="border border-right-bottom"></view>
                    <view class="border border-bottom-right"></view>
                    <view class="border border-bottom-left"></view>
                    <view class="border border-left-bottom"></view>
                    <view class="border border-left-top"></view>
                </view>
                <view class='content_middle_right bg_gray {{_flag_bright?"":"bg_black"}}' style="transition-property:{{_cut_animation?'':'background'}}"></view>
            </view>
            <view class='content_bottom bg_gray {{_flag_bright?"":"bg_black"}}' style="transition-property:{{_cut_animation?'':'background'}}"></view>
        </view>
        <image bindload="imageLoad" bindtouchstart="_start" bindtouchmove="_move" bindtouchend="_end" style="width:{{img_width ? img_width + 'px' : 'auto'}};height:{{img_height ? img_height + 'px' : 'auto'}};transform:translate3d({{_img_left-img_width/2}}px,{{_img_top-img_height/2}}px,0) scale({{scale}}) rotate({{angle}}deg);transition-duration:{{_cut_animation?.4:0}}s;" class='img' src='{{imgSrc}}'></image>
    </view>
    <canvas canvas-id='image-cropper' disable-scroll="true" style="width:{{_canvas_width * export_scale}}px;height:{{_canvas_height * export_scale}}px;left:{{canvas_left}}px;top:{{canvas_top}}px" class='image-cropper-canvas'></canvas>
</view>
```

## File: components/image-cropper/image-cropper.wxss
```
.image-cropper {
    background: rgba(14, 13, 13, .8);
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    z-index: 1;
}

.image-cropper .main {
    position: absolute;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
}

.image-cropper .content {
    z-index: 9;
    position: absolute;
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    pointer-events: none;
}

.image-cropper .bg_black {
    background: rgba(0, 0, 0, 0.8) !important;
}

.image-cropper .bg_gray {
    background: rgba(0, 0, 0, 0.45);
    transition-duration: .35s;
}

.image-cropper .content>.content_top {
    pointer-events: none;
}

.image-cropper .content>.content_middle {
    display: flex;
    height: 200px;
    width: 100%;
}

.image-cropper .content_middle_middle {
    width: 200px;
    box-sizing: border-box;
    position: relative;
    transition-duration: .3s;
}

.image-cropper .content_middle_right {
    flex: auto;
}

.image-cropper .content>.content_bottom {
    flex: auto;
}

.image-cropper .img {
    z-index: 2;
    top: 0;
    left: 0;
    position: absolute;
    border: none;
    width: 100%;
    backface-visibility: hidden;
    transform-origin: center;
}

.image-cropper .image-cropper-canvas {
    position: fixed;
    background: white;
    width: 150px;
    height: 150px;
    z-index: 10;
    top: -200%;
    pointer-events: none;
}

.image-cropper .border {
    background: white;
    pointer-events: auto;
    position: absolute;
}

.image-cropper .border-top-left {
    left: -2.5px;
    top: -2.5px;
    height: 2.5px;
    width: 33rpx;
}

.image-cropper .border-top-right {
    right: -2.5px;
    top: -2.5px;
    height: 2.5px;
    width: 33rpx;
}

.image-cropper .border-right-top {
    top: -1px;
    width: 2.5px;
    height: 30rpx;
    right: -2.5px;
}

.image-cropper .border-right-bottom {
    width: 2.5px;
    height: 30rpx;
    right: -2.5px;
    bottom: -1px;
}

.image-cropper .border-bottom-left {
    height: 2.5px;
    width: 33rpx;
    bottom: -2.5px;
    left: -2.5px;
}

.image-cropper .border-bottom-right {
    height: 2.5px;
    width: 33rpx;
    bottom: -2.5px;
    right: -2.5px;
}

.image-cropper .border-left-top {
    top: -1px;
    width: 2.5px;
    height: 30rpx;
    left: -2.5px;
}

.image-cropper .border-left-bottom {
    width: 2.5px;
    height: 30rpx;
    left: -2.5px;
    bottom: -1px;
}
```

## File: components/privacyAuthorize/privacyAuthorize.js
```javascript
const PRIVACYNAME = '《嗨猫互动小程序隐私保护指引》';

Component({
  properties: {
    needAutoShow: { // 是否需要弹窗自动弹出(条件满足的时候)
      value: false,
      type: Boolean
    }
  },
  data: {
    privacyAuthorizeVisible: false,
    privacyContractName: '',
  },
  lifetimes: {
    async attached() {
      try {
        this.watchNeedPrivacyAuthEvent();
        const needAuthorization = await this.getPrivacyAuthInfo();
        console.log(typeof needAuthorization, needAuthorization);
        this.autoShowLogic(needAuthorization);
      } catch (err) {
        console.log(err);
      }
    },
    detached() {}
  },
  methods: {
    // 打开隐私协议具体内容
    onPrivacyContractOpen() {
      wx.openPrivacyContract({
        success: () => {}, // 打开成功
        fail: () => {}, // 打开失败
        complete: () => {}
      });
    },
    // 同意授权
    onAgree() {
      this.privacyAuthResolve({
        event: 'agree',
        buttonId: 'agree-btn'
      });
      this.setData({
        privacyAuthorizeVisible: false
      });
    },
    // 拒绝授权
    onDisagree() {
      this.privacyAuthResolve({
        event: 'disagree'
      });
      this.setData({
        privacyAuthorizeVisible: false
      });
    },
    // 监听“需要隐私授权”事件
    watchNeedPrivacyAuthEvent() {
      wx.onNeedPrivacyAuthorization((resolve) => {
        // 打开隐私授权弹窗
        this.setData({
          privacyAuthorizeVisible: true
        });
        // 暂存resolve(授权上报函数)
        this.privacyAuthResolve = resolve;
      });
    },
    // 查询隐私名称、是否需要隐私授权
    getPrivacyAuthInfo() {
      return new Promise((resolve, reject) => {
        wx.getPrivacySetting({
          success: (res) => {
            console.log("是否需要授权：", res.needAuthorization, "隐私协议的名称为：", res.privacyContractName);
            if (res.needAuthorization) {
              this.setData({
                privacyContractName: res.privacyContractName || PRIVACYNAME
              });
              resolve(res.needAuthorization);
            }
          },
          fail: (err) => {
            console.log(err);
            reject(err);
          },
        })
      })
    },
    // 自动弹出隐私授权窗(条件满足的情况)的逻辑
    // 条件：需要隐私授权并且需要自动弹出
    autoShowLogic(needPrivacyAuth) {
      if (needPrivacyAuth === true && this.data.needAutoShow) {
        wx.requirePrivacyAuthorize({});
      }
    }
  },
});
```

## File: components/privacyAuthorize/privacyAuthorize.json
```json
{
  "component": true
}
```

## File: components/privacyAuthorize/privacyAuthorize.wxml
```
<!-- 隐私授权弹窗 -->
<view class="privacyAuthorize" wx:if="{{privacyAuthorizeVisible}}">
  <view class="shade"></view>
  <view class="box">
   <view class="platformInfo">
    <image src="https://static.hudongmiao.com/joymewMp/defaultHeadImg2.png" class="avatar" />
    嗨喵现场互动
   </view>
    <view class="content">在你使用【嗨喵现场互动】服务之前，请仔细阅读<text class="link" bindtap="onPrivacyContractOpen">{{privacyContractName}}</text>。如你同意{{privacyContractName}}，请点击"同意"开始使用【嗨喵现场互动】</view>
    <view class="btnGroup">
      <button class="btn refuseBtn" bindtap="onDisagree">拒绝</button>
      <button id="agree-btn" open-type="agreePrivacyAuthorization" bindagreeprivacyauthorization="onAgree" class="btn agreeBtn">同意</button>
    </view>
  </view>
</view>
```

## File: components/privacyAuthorize/privacyAuthorize.wxss
```
.privacyAuthorize {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: 99999;
  display: flex;
  justify-content: center;
  align-items: center;
}

.shade {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
}

.box {
  width: 480rpx;
  min-height: 450rpx;
  position: relative;
  background-color: #ffffff;
  border-radius: 20rpx;
  padding: 20rpx;
}

.box .platformInfo {
  display: flex;
  align-items: center;
  font-size: 32rpx;
  color: #000000;
}

.box .platformInfo .avatar {
  width: 80rpx;
  height: 80rpx;
  border-radius: 50%;
  margin-right: 20rpx;
}

.box .content {
  margin-top: 20rpx;
  font-size: 28rpx;
  color: #000000;
  line-height: 45rpx;
}
.box .content .link {
  color: rgba(10,142,238, 1);
}

.box .btnGroup {
  display: flex;
  margin-top: 40rpx;
  gap: 20rpx;
}

.box .btnGroup .btn {
  width: 200rpx;
  height: 80rpx;
  font-size: 28rpx;
  border-radius: 20rpx;
  display: flex;
  align-items: center;
  justify-content: center;
}
.box .btnGroup .btn::after {
  border: none;
}
.box .btnGroup .refuseBtn {
  background-color: rgba(242,242,242,1);
  color: rgba(83,190,107,1);
}

.box .btnGroup .agreeBtn {
  background-color: rgba(83,190,107,1);
  color: #ffffff;
}
```

## File: components/rateStar/rateStar.js
```javascript
// components/rateStar/rateStar.js
Component({
  /**
   * 组件的属性列表
   */
  properties: {
    rate: {
      type: [Number, String],
      default: 0
    },
    size: {
      type: [Number, String],
      default: 0
    },    
    edit: {
      type:Boolean,
      default: false
    }
  },

  /**
   * 组件的初始数据
   */
  data: {

  },

  /**
   * 组件的方法列表
   */
  methods: {
    setRate(e){
      if(!this.data.edit){
        return 
      }
      let rate = e.currentTarget.dataset.rate
			this.triggerEvent('change', rate)
    }
  }
})
```

## File: components/rateStar/rateStar.json
```json
{
  "component": true,
  "usingComponents": {}
}
```

## File: components/rateStar/rateStar.wxml
```
<view class="wrapper">
  <block wx:for="{{[1,2,3,4,5]}}" wx:for-item="item" wx:for-index="index" wx:key="index" >
    <image class="star-icon {{size}}" src="/assets/image/comment/unstar.png" data-rate="{{item}}" bindtap="setRate" wx:if="{{rate<item}}"></image>
    <image class="star-icon {{size}}" src="/assets/image/comment/star.png" data-rate="{{item}}" bindtap="setRate" wx:if="{{rate>=item}}"></image>
  </block>
</view>
```

## File: components/rateStar/rateStar.wxss
```
/* components/rateStar/rateStar.wxss */
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.star-icon{
  width: 28rpx;
  height: 28rpx;
  margin-left: 12rpx;
}
.big{
  width: 42rpx;
  height: 42rpx;
  margin-left: 12rpx;
}
```

## File: components/sign/sign.js
```javascript
import {
  showWxToast,
  timeoutTask
} from '../../utils/index';
import {
  authGetPhoneNew
} from '../../api/login';

Component({
  /**
   * 组件的属性列表
   */
  properties: {
    activityTitle: {
      value: '',
      type: String,
    },
    wishProp: {
      value: '',
      type: String,
    },
    sceneType: {
      value: '',
      type: String,
    },
    isExamine: {
      value: false,
      type: Boolean,
    },
    wxGetPhoneButtonVisible: {
      value: false,
      type: Boolean,
    },
  },
  observers: {
    wishProp: function (wishProp) {
      this.setData({
        wish: wishProp,
      });
    },
    // wxGetPhoneButtonVisible: function(newVal) {
    //   this.setData({
    //     needInputPhone: !newVal
    //   });
    // },
  },
  data: {
    wish: '', // 祝福语
    gender: '0', // 性别 0:男 1:女 商城版独有
    phone: '', // 手机号 商城版
    birthDate: '', // 生日 商城版独有
    needInputPhone: false,
    phoneInputFocus: false,
  },
  /**
   * 组件的方法列表
   */
  methods: {
    wishesBlur(e) {
      console.log('***wishesBlur***');
      if (e.detail.value) {
        this.setData({
          wish: e.detail.value,
        });
      }
    },
    sign() {
      if (!this.data.wish) {
        showWxToast('祝福语不能为空!');
        return;
      }
      if (this.data.phone && this.data.phone.length !== 11) {
        showWxToast('请输入正确格式的手机号!');
        return;
      }
      if (!this.data.isExamine) {
        if (!this.data.phone) {
          showWxToast('手机号不能为空!');
          this.setData({
            needInputPhone: true,
            phoneInputFocus: true
          });
          return;
        }
        if (this.data.phone.length !== 11) {
          showWxToast('手机号格式错误!');
          return;
        }
        if (!this.data.birthDate) {
          showWxToast('请选择生日!');
          return;
        }
      }
      console.log(this.data.wish);
      console.log(this.data.phone);
      console.log(this.data.birthDate);
      console.log(this.data.gender);
      this.triggerEvent('signEvent', {
        wish: this.data.wish,
        userPhone: this.data.phone,
        birthDate: this.data.birthDate,
        gender: this.data.gender,
      });
    },
    refreshWish() {
      this.triggerEvent('refreshWishEvent');
    },
    phoneBlur(e) {
      console.log('***phoneBlur***');
      if (e.detail.value) {
        this.setData({
          phone: e.detail.value,
          phoneInputFocus: false,
        });
      }
    },
    chooseGender: function (e) {
      console.log(e.currentTarget.dataset.gender);
      this.setData({
        gender: e.currentTarget.dataset.gender,
      });
    },
    personInputPhone() {
      showWxToast('请输入手机号!');
      // 手机输入框显示
      this.setData({
        needInputPhone: true,
      })
      // 延迟0.3s输入框聚焦
      timeoutTask(() => {
        this.setData({
          phoneInputFocus: true
        })
      }, 300);
    },
    getPhoneNumber: function (e) {
      console.log('*******getPhoneNumber方法内部*******');
      console.log(e.detail.code);
      console.log(e.detail.errno);
      if (e.detail.errno === 1400001 || !e.detail.code) {
        this.personInputPhone();
        return;
      }
      // 没有微信获取手机号能力的情况下不传code
      authGetPhoneNew({
          code: this.data.wxGetPhoneButtonVisible ? e.detail.code : '', 
        })
        .then(res => {
          console.log(res);
          if (res && res.phoneNumber) {
            this.setData({
              phone: res.phoneNumber,
            });
          } else {
            this.personInputPhone();
          }
        })
        .catch(err => {
          console.log(err);
          this.personInputPhone();
        });
    },
    handleBirthDateChange: function (e) {
      console.log(e.detail.value);
      this.setData({
        birthDate: e.detail.value,
      });
    },
  },
});
```

## File: components/sign/sign.json
```json
{
    "component": true
}
```

## File: components/sign/sign.wxml
```
<view class="signNew">
    <image src='https://static.joymew.com/joymewMp/joymewIndex/tqlLogo.png' class="tqlLogo"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/weddingSignBg2022.png' class="bg" wx:if="{{sceneType === '0'}}"></image>
    <image src="https://static.hudongmiao.com/joymewMp/joymewIndex/ballon2.png" class="ballon2" wx:if="{{sceneType === '0'}}"></image>
    <image src="https://static.hudongmiao.com/joymewMp/joymewIndex/ballon3.png" class="ballon3" wx:if="{{sceneType === '0'}}"></image>
    <image src="https://static.hudongmiao.com/joymewMp/joymewIndex/wel2022.png" class="welWedding" wx:if="{{sceneType === '0'}}"></image>
    <view class="annualBgBox" wx:if="{{sceneType === '1'}}">
        <image src='https://static.hudongmiao.com/joymewMp/joymewIndex/bg-annualMeeting01.png' class="annualBg" mode="widthFix"></image>
    </view>
    <image src='https://static.hudongmiao.com/joymewMp/joymewIndex/signTitle-annualMeeting03.png' class="annualSignTitle" wx:if="{{sceneType === '1'}}" mode="widthFix"></image>
    <view class="annualTitle" wx:if="{{sceneType === '1'}}">{{activityTitle}}</view>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/birthBg3.png' class="bg" wx:if="{{sceneType === '2'}}"></image>
    <view class="bbyBg" wx:if="{{sceneType === '21'}}"></view>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/bbyDeco02.png' class="bbyDeco02" wx:if="{{sceneType === '21'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/bbyDeco01.png' class="bbyDeco01" wx:if="{{sceneType === '21'}}"></image>
    <view class="syBgBox" wx:if="{{sceneType === '22'}}">
        <image src='https://static.joymew.com/joymewMp/joymewIndex/syMobileBg4.png' class="syBg" mode="widthFix"></image>
    </view>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/lantern.png' class="topLantern" wx:if="{{sceneType === '22'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/decoration.png' class="bottomDecoration" wx:if="{{sceneType === '22'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/crlMobileBg2.png' class="bg" wx:if="{{sceneType === '23'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/crlBottomCloud.png' class="crlBottomCloud" wx:if="{{sceneType === '23'}}"></image>
    <image src='https://static.hudongmiao.com/joymewMp/bly/blyBg.png' class="bg" wx:if="{{sceneType === '24'}}"></image>
    <image src='https://static.hudongmiao.com/joymewMp/myyBg.png' class="bg" wx:if="{{sceneType === '25'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/bydlBg.png' class="bg" wx:if="{{sceneType === '41'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/bydlDeco.png' class="cloud" wx:if="{{sceneType === '41'}}"></image>
    <view class="xsyBgBox" wx:if="{{sceneType === '42'}}">
        <image src='https://static.joymew.com/joymewMp/joymewIndex/xsyBg.png' class="xsyBg" mode="widthFix"></image>
    </view>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/xsyDeco.png' class="lantern" wx:if="{{sceneType === '42'}}"></image>
    <view class="jbtmBgBox" wx:if="{{sceneType === '43'}}">
        <image src='https://static.joymew.com/joymewMp/joymewIndex/jbtmBg.png' class="jbtmBg" mode="widthFix"></image>
    </view>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/jbtmCloud.png' class="jbtmCloud" wx:if="{{sceneType === '43'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/txhBg.png' class="bg" wx:if="{{sceneType === '51'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/qqyBg.png' class="bg" wx:if="{{sceneType === '52'}}"></image>
    <image src='https://static.joymew.com/joymewMp/joymewIndex/hxBg.png' class="bg" wx:if="{{sceneType === '53'}}"></image>
    <view class="signBox signBox{{sceneType}}">
        <image src="https://static.hudongmiao.com/joymewMp/joymewIndex/qima.gif" class="qima" wx:if="{{sceneType === '0'}}"></image>
        <image src="https://static.hudongmiao.com/joymewMp/joymewIndex/ballon1.png" class="ballon1" wx:if="{{sceneType === '0'}}"></image>
        <view class="benifit" wx:if="{{sceneType === '0'}}">一起看美照、送祝福、玩游戏吧～</view>
        <view class="fItem">
            <text class="key key{{sceneType}}">性别：</text>
            <view class="sexGroup">
                <view class="sexItem sexItem{{sceneType}}" bindtap="chooseGender" data-gender='0'>
                    <image src='https://static.joymew.com/joymewMpTql/signWedding/male.png' class="sexIcon"></image>
                    男
                    <image src='https://static.joymew.com/joymewMpTql/signWedding/tickedIcon.png' class="tickedIcon" wx:if="{{gender === '0'}}"></image>
                </view>
                <view class="sexItem sexItem{{sceneType}}" bindtap="chooseGender" data-gender='1'>
                    <image src='https://static.joymew.com/joymewMpTql/signWedding/female.png' class="sexIcon"></image>
                    女
                    <image src='https://static.joymew.com/joymewMpTql/signWedding/tickedIcon.png' class="tickedIcon" wx:if="{{gender === '1'}}"></image>
                </view>
            </view>
        </view>
        <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key key{{sceneType}}">祝福语：</text>
            <input bindblur="wishesBlur" name="wishes" placeholder='祝福语' maxlength="20" value="{{wish}}" placeholder-class="phcolor{{sceneType}}" class="iptPad ipt{{sceneType}}"></input>
            <view class="refreshBtn refreshBtn{{sceneType}}" bindtap="refreshWish"></view>
        </view>
        <view class="fItem" wx:if="{{!isExamine}}">
            <text class="key key{{sceneType}}">手机号：</text>
            <view class="getPhoneIpt getPhoneIpt{{sceneType}}" wx:if="{{!needInputPhone}}">
                {{phone ? phone: '获取手机号'}}
                <button open-type="getPhoneNumber" bindgetphonenumber="getPhoneNumber" class="getPhoneBtn" wx:if="{{!phone}}">
                    获取手机号
                </button>
            </view>
            <input bindblur="phoneBlur" name="phone" placeholder='请输入手机号' maxlength="11" value="{{phone}}" placeholder-class="phcolor{{sceneType}}" class="iptPad ipt{{sceneType}}" wx:else focus="{{phoneInputFocus}}" type="number"></input>
            <view class="phoneIconBox phoneIconBox{{sceneType}}"></view>
        </view>
        <view class="fItem">
            <text class="key key{{sceneType}}">生日：</text>
            <picker mode="date" bindchange="handleBirthDateChange" value="{{birthDate}}">
                <view class="birthDate">
                    <view class="val">{{birthDate === '' ? '请选择' : birthDate}}</view>
                    <image src='https://static.joymew.com/joymewMp/joymewIndex/downArrow.png' class="downArrow"></image>
                </view>
            </picker>
        </view>
        <view class="signBtn signBtn{{sceneType}}" catchtap="sign">
            <text wx:if="{{sceneType !== '1'}}">点击进入</text>
        </view>
    </view>
</view>
```

## File: components/sign/sign.wxss
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
.tqlLogo {
  width: 110rpx;
  height: 148rpx;
  position: absolute;
  left: 8rpx;
  top: 53rpx;
  z-index: 1;
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
  background-image: url('https://static.joymew.com/joymewMp/joymewIndex/box-04.png');
  width: 678rpx;
}
.signBox1 {
  background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/boxQy01.png');
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
  background-image: url('https://static.joymew.com/joymewMp/joymewIndex/signBoxCrl.png');
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
  background-image: url('https://static.joymew.com/joymewMp/joymewIndex/signBoxBgHX.png');
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
  background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/refreshIconPink.png');
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
  background-image: url('https://static.joymew.com/joymewMp/joymewIndex/txhReloadIcon.png');
}
.refreshBtn52 {
  background-image: url('https://static.joymew.com/joymewMp/joymewIndex/qqyReloadIcon.png');
}
.refreshBtn53 {
  background-image: url('https://static.joymew.com/joymewMp/joymewIndex/bbyReloadIcon.png');
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
  background-image: url('https://static.joymew.com/joymewMpTql/signWedding/phoneIcon.png');
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
  background-image: url('https://static.joymew.com/joymewMpTql/signTXH/phoneIcon.png');
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
  background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/signBtnQy01.png');
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

## File: pages/agreement/agreement.js
```javascript
import { PAGE_HOST } from '../../assets/constant/host';
import { getCurrentTimestamp } from '../../utils/date';
const app = getApp();

Page({
  data: {
    h5Url: '',
  },
  onLoad: function(options) {
    this.setData({
      h5Url: `${PAGE_HOST}agreement/index.html?time=${getCurrentTimestamp()}`,
    });
  },
  onShow: function() {},
  onUnload: function() {},
});
```

## File: pages/agreement/agreement.json
```json
{
    "navigationBarTitleText": "充值服务协议"
}
```

## File: pages/agreement/agreement.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}">
</web-view>
```

## File: pages/agreement/agreement.wxss
```
view {
    margin: 20rpx 0;
}
```

## File: pages/feedback/feedback.js
```javascript
import { submitFeedback, uploadFeedbackImg, wxChooseImage } from '../../api/feedback/feedback';
import { timeoutTask, showWxToast, showWxLoading, hideWxLoading } from '../../utils/index';
// 投诉页面需要传userId
let btnLock = false;
Page({

  /**
   * 页面的初始数据
   */
  data: {
    txtVal: 0,
    typeList: [{
      name: "支付未到账",
      isActive: false
    }, {
      name: "误点击支付",
      isActive: false
    }, {
      name: "不明的扣款",
      isActive: false
    }, {
      name: "红包未到账",
      isActive: false
    }, {
      name: "其他原因",
      isActive: false
    }],
    activeTypeStr: "",
    desc: "",
    phone: "",
    uploaderList: [],
    uploadImgUrlList: [],
    uploaderNum: 0,
    showUpload: true,
    userId: '',
  },

  onLoad: function (options) {
    console.log(options.userId);
    this.setData({
      userId: options.userId,
    });
  },
  phoneInput: function (e) {
    this.setData({
      phone: e.detail.value
    })
  },
  descInput: function (e) {
    this.setData({
      txtVal: e.detail.value.length,
      desc: e.detail.value
    })
    if (this.data.txtVal >= 120) {
      showWxToast('问题内容不能超过120字哦!');
      this.setData({
        desc: this.data.desc.slice(0, 120)
      })
    }
  },
  chooseType(e) {
    if (e.currentTarget.dataset.active) {
      this.resetTypeList();
    } else {
      let tmpCount = this.getTypeListActiveNum();
      if (tmpCount == 0) {
        this.updateTypeList(e.currentTarget.dataset.name);
      } else {
        this.resetTypeList();
        this.updateTypeList(e.currentTarget.dataset.name);
      }
    }
  },
  getTypeListActiveNum() {
    let tmpTypeList = this.data.typeList;
    let tmpCount = 0;
    for (let i = 0; i < tmpTypeList.length; i++) {
      if (tmpTypeList[i].isActive) {
        tmpCount++;
      }
    }
    return tmpCount;
  },
  updateTypeList(name) {
    let tmpTypeList = this.data.typeList;
    for (let i = 0; i < tmpTypeList.length; i++) {
      if (tmpTypeList[i].name == name) {
        tmpTypeList[i].isActive = !tmpTypeList[i].isActive
        break;
      }
    }
    this.setData({
      typeList: tmpTypeList
    })
  },
  resetTypeList() {
    let tmpTypeList = this.data.typeList;
    for (let i = 0; i < tmpTypeList.length; i++) {
      if (tmpTypeList[i].isActive) {
        tmpTypeList[i].isActive = false;
      }
    }
    this.setData({
      typeList: tmpTypeList
    })
  },

  submit() {
    if (btnLock) {
      return;
    }
    this.setData({
      activeTypeStr: ""
    })
    let tmpActiveTypeStr = "";
    let tmpImgUrlStr = "";
    let tmpImgUrlList = this.data.uploadImgUrlList;
    let tmpImgUrlListSub = [];
    let tmpTypeList = this.data.typeList;
    for (let i = 0; i < tmpImgUrlList.length; i++) {
      tmpImgUrlListSub.push(tmpImgUrlList[i].value);
    }
    for (let i = 0; i < tmpTypeList.length; i++) {
      if (tmpTypeList[i].isActive) {
        tmpActiveTypeStr += (tmpTypeList[i].name + " ");
      }
    }
    this.setData({
      activeTypeStr: tmpActiveTypeStr
    })
    if (!this.data.activeTypeStr) {
      showWxToast('至少选择一个问题类型哦!');
      return;
    }
    if (!this.data.desc) {
      showWxToast('请填写问题描述!');
      return;
    }
    if (!this.data.phone) {
      showWxToast('请填写手机号!');
      return;
    }

    if (!(this.data.phone.length == 11)) {
      showWxToast('手机号格式不正确!');
      return;
    }
    if (tmpImgUrlListSub.length > 0) {
      tmpImgUrlStr = tmpImgUrlListSub.join(',');
    }

    console.log(this.data.desc);
    console.log(this.data.phone);
    console.log(this.data.activeTypeStr);
    console.log(tmpImgUrlStr);
    btnLock = true;
    submitFeedback({
      desc: this.data.desc,
      phone: this.data.phone,
      type: this.data.activeTypeStr,
      imgurl: tmpImgUrlStr,
    }).then((res) => {
      console.log(res);
      showWxToast('投诉信息提交成功');
      timeoutTask(() => {
        btnLock = false;
        wx.navigateBack();
      }, 1000);
    }).catch((err) => {
      console.log(err);
      btnLock = false;
      showWxToast('投诉信息提交失败');
    });
  },
  // 删除图片
  clearImg: function (e) {
    var nowList = []; //新数据

    var uploaderList = this.data.uploaderList; //原数据
    for (let i = 0; i < uploaderList.length; i++) {
      if (i == e.currentTarget.dataset.index) {
        this.deleteImgUrlByKey(uploaderList[i])
        continue;
      } else {
        nowList.push(uploaderList[i])
        continue;
      }
    }
    this.setData({
      uploaderNum: this.data.uploaderNum - 1,
      uploaderList: nowList,
      showUpload: true
    })
  },
  deleteImgUrlByKey(key) {
    let tmpImgUrlList = this.data.uploadImgUrlList;
    for (let i = 0; i < tmpImgUrlList.length; i++) {
      if (tmpImgUrlList[i].key == key) {
        tmpImgUrlList.splice(i, 1);
        break;
      }
    }
    this.setData({
      uploadImgUrlList: tmpImgUrlList
    })
  },
  //展示图片
  showImg: function (e) {
    var that = this;
    wx.previewImage({
      urls: that.data.uploaderList,
      current: that.data.uploaderList[e.currentTarget.dataset.index]
    })
  },
  //上传图片
  upload: function (e) {
    let tempFilePaths;
    wxChooseImage(this.data.uploaderNum).then((res) => {
      console.log(res);
      showWxLoading('上传图片中...');
      tempFilePaths = res.tempFilePaths;
      return uploadFeedbackImg(tempFilePaths[0]);
    }).then((res2) => {
      hideWxLoading();
      console.log(res2);
      let tmpRes = JSON.parse(res2.data);
      console.log(tmpRes.data.filePath);
      let tmpImgUrlList = this.data.uploadImgUrlList;
      let uploaderList = this.data.uploaderList.concat(tempFilePaths);
      tmpImgUrlList.push({
        key: tempFilePaths[0],
        value: tmpRes.data.filePath
      })
      if (uploaderList.length == 3) {
        this.setData({
          showUpload: false
        });
      }
      this.setData({
        uploaderList: uploaderList,
        uploaderNum: uploaderList.length,
        uploadImgUrlList: tmpImgUrlList
      })
    }).catch((err) => {
      console.log(err);
      hideWxLoading();
    })
  },
  /**
   * 生命周期函数--监听页面初次渲染完成
   */
  onReady: function () {

  },

  /**
   * 生命周期函数--监听页面显示
   */
  onShow: function () {

  }

})
```

## File: pages/feedback/feedback.json
```json
{
  "navigationBarTitleText": "反馈投诉"
}
```

## File: pages/feedback/feedback.wxml
```
<view class="container">
  <view class="complaints-form">
    <view class="type-wrap">
      <view wx:for="{{typeList}}" wx:key="index" class="type-item">
        <view class="my-radio" style="{{item.isActive?'background-image:url(https://img.hidongtv.com/hidong-wechat/complaints-tick.png)':''}}" catchtap="chooseType" data-name="{{item.name}}" data-active="{{item.isActive}}"></view>
        <view class="radio-value">{{item.name}}</view>
      </view>
    </view>
    <view class="description-wrap">
      <view class="key">问题描述</view>
      <view class="desc-wrap">
        <textarea placeholder="请填写描述以便我们提供更好的帮助" maxlength="120" bindinput="descInput" />
        <view class="numberV">{{txtVal}}/120</view>
      </view>
    </view>
    <view class="img-wrap">
      <view class="key">相关截图</view>
      <view class="panel-title">{{title}}</view>
      <view class="{{uploaderList.length === 0 ? 'ui-uploader-cell':'ui-uploader-cell-other'}}">
        <!-- 根据已选择的图片临时路径数组展示图片-->
        <view class='ui-uploader-item' wx:for="{{uploaderList}}" wx:key="index">
          <!-- 删除-->
          <icon class='ui-uploader-item-icon' bindtap='clearImg' data-index="{{index}}" type="clear" size="20" color="#666666" />
          <!-- 图片-->
          <image bindtap='showImg' data-index="{{index}}" src='{{item}}'></image>
        </view>
        <!-- 上传按钮+框 -->
        <view class='ui-uploader' bindtap='upload' wx:if="{{showUpload}}">
          +
        </view>
      </view>
    </view>
    <view class="contact-wrap">
      <view class="phone-key">联系方式</view>
      <input bindinput='phoneInput' placeholder='请输入手机号' type="number" maxlength="11" />
    </view>
    <view class="contact-way">
      <view class="phoneItem">客服电话：19512368757</view>
      <view class="phoneItem">投诉电话：400-082-2298</view>
    </view>
    <view class="submit-btn-wrap">
        <view class="btn" catchtap="submit">提交</view>
    </view>
  </view>
</view>
```

## File: pages/feedback/feedback.wxss
```
.container {
  width: 100vw;
  background-color: #fff;
  position: relative;
  overflow: hidden;
}
.complaints-form>.type-wrap>.type-item {
  margin-left: 30rpx;
  height: 88rpx;
  border-bottom: 1rpx solid #e5e5e5;
  display: flex;
  align-items: center;
}

.complaints-form>.type-wrap>.type-item>.my-radio {
  width: 46rpx;
  height: 46rpx;
  border: 2rpx solid #c9c9c9;
  border-radius: 50%;
  margin-right: 20rpx;
  background-size: 100% 100%;
}

.complaints-form>.type-wrap>.type-item>.radio-value {
  color: #000;
  font-size: 34rpx;
}

.complaints-form>.description-wrap {
  margin-top: 20rpx;
}

.complaints-form>.description-wrap>.key {
  box-sizing: border-box;
  padding-left: 29rpx;
  font-size: 34rpx;
  color: #000;
}

.complaints-form>.description-wrap>.desc-wrap {
  display: flex;
  justify-content: center;
  position: relative;
  margin-top: 20rpx;
}

.complaints-form>.description-wrap>.desc-wrap>textarea {
  width: 690rpx;
  height: 140rpx;
  outline: none;
  border-radius: 4rpx;
  border: 1rpx solid #979797;
  box-sizing: border-box;
  padding: 12rpx;
}

.complaints-form>.description-wrap>.desc-wrap>.numberV {
  position: absolute;
  right: 5vw;
  bottom: 1vw;
  font-size: 3.2vw;
}

.complaints-form>.img-wrap {
  margin-top: 20rpx;
}

.complaints-form>.img-wrap>.key {
  box-sizing: border-box;
  padding-left: 29rpx;
  font-size: 34rpx;
  color: #000;
}

.complaints-form>.img-wrap .panel-title {
  margin-bottom: 20rpx;
}

.complaints-form>.img-wrap .ui-uploader-cell-other {
  width: 690rpx;
  /* padding: 40rpx 0; */
  display: flex;
  flex-wrap: wrap;
  align-content: flex-start;
  margin-left: 30rpx;
}

.complaints-form>.img-wrap .ui-uploader-cell {
  width: 690rpx;
  display: flex;
  flex-wrap: wrap;
  align-content: flex-start;
  margin-left: 30rpx;
}

.complaints-form>.img-wrap .ui-uploader-item {
  width: 118rpx;
  height: 118rpx;
  margin-right: 18rpx;
  margin-bottom: 18rpx;
  padding-bottom: 2rpx;
  padding-right: 2rpx;
  position: relative;
}

.complaints-form>.img-wrap .ui-uploader-item-icon {
  position: absolute;
  right: 0;
}

.complaints-form>.img-wrap .ui-uploader-item image {
  width: 100%;
  height: 100%;
}

.complaints-form>.img-wrap .ui-uploader {
  width: 135rpx;
  height: 135rpx;
  margin-right: 20rpx;
  background: #efefef;
  border-radius: 4rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #878787;
  font-size: 72rpx;
}

.complaints-form>.contact-wrap {
  margin-top: 20rpx;
  display: flex;
  align-items: center;
  margin-left: 29rpx;
}

.complaints-form>.contact-wrap>.phone-key {
  font-size: 34rpx;
  color: #000;
  margin-right: 17rpx;
}

.complaints-form>.contact-wrap>input {
  outline: none;
  width: 42vw;
  height: 9vw;
  border-radius: 1.067vw;
  border: 1px solid #dedede;
  box-sizing: border-box;
  padding: 2vw;
  font-size: 4vw;
  letter-spacing: 0.2vw;
}
.complaints-form>.contact-way {
  display: flex;
  width: 100%;
  justify-content: space-around;
  padding: 32rpx 12rpx;
}

.complaints-form>.contact-way>.phoneItem {
  font-size: 3.2vw;
  color: #878787;
}

.complaints-form>.submit-btn-wrap {
  display: flex;
  justify-content: center;
  position: fixed;
  bottom: -5rpx;
  width: 100%;
}

.complaints-form>.submit-btn-wrap>.btn {
  width: 100%;
  height: 94rpx;
  background: #1aad19;
  border-radius: 10rpx;
  font-size: 4vw;
  font-weight: 700;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## File: pages/guessHb/guessHb.js
```javascript
import { timeoutTask, showWxToast, converNumToText } from '../../utils/index';
import { wxPay } from '../../api/pay';
import {
  getGuessInfo,
  attendGuess,
  guessHbRecharge,
} from '../../api/guessHb/guessHb';

let robLock = false;
let endLoop = false;
const app = getApp();
const IDENTITYLIST = [
  {
    id: '1',
    name: '新郎',
  },
  {
    id: '2',
    name: '新娘',
  },
  {
    id: '3',
    name: '亲友',
  },
];
let DMLIST = [];
let shineIndex = 0;
let danmuIndex = 0;
Page({
  data: {
    inputVal: '', // 输入的最终值
    interArray: [], // 整数
    decimalArray: [], // 小数
    resultNum: '',
    targetVal: '', // 答案
    hbVisible: false,
    hasHbPop: false, // 限制红包每轮只弹出一次
    // 红包动画控制
    isHbOpen: false,
    isLidUpAniStart: false,
    isLidDownAniStart: false,
    isPShowAniStart: false,
    isRobBtnAniStart: false,
    // 0: 等待 1：game界面
    guessStatus: 0,
    hbId: '',
    sort: '',
    sortUnuse: '',
    sortText: '',
    guessMoney: '',
    attendNum: 0,
    remainNum: 0,
    purchaseMoney: 0,
    userId: '',
    openId: '',
    isAnnounce: false, // 是否可以揭晓
    hasPrize: false, // 是否猜中
    prizeMoney: '', // 中奖金额
    hasPrizeRounds: false, // 本轮是否有猜中的人
    rankList: [],
    rankListVisible: false,
    isFocus: false,
    gapMax: '',
    gapMin: '',
    boxShowAni: false,
    boxShow: false,
    textShowAni: false,
    iptShowAni: false,
    activeShine: '',
    shineShow: false,
    danmuAniShow: false,
    activeDanmuCt: '',
    payUser: {
      avator: '',
      identity: '',
    },
    hasClickGoOn: false,
    hasClickShow: false,
    hasAutoPopHb: false,
  },
  onLoad: function(options) {
    robLock = false;
    this.setData({
      userId: options.userId,
      openId: options.openId,
    });
    this.initGuessInfo();
  },
  onShow: function() {},
  onUnload: function() {
    endLoop = true;
  },
  robHb: function() {
    if (robLock) {
      return;
    }
    robLock = true;
    this.openHbAniStart().then(() => {
      timeoutTask(() => {
        robLock = false;
      }, 1500);
      this.setData({
        isHbOpen: true,
      });
    });
  },
  openHbAniStart() {
    return new Promise((resolve, reject) => {
      try {
        // 按钮动画开始
        this.setData({
          isRobBtnAniStart: true,
        });
        timeoutTask(() => {
          // 按钮动画结束
          this.setData({
            isRobBtnAniStart: false,
          });
          // 红包盖子打开
          this.setData({
            isLidUpAniStart: true,
          });
          resolve(1);
          timeoutTask(() => {
            // 奖项露出
            this.setData({
              isPShowAniStart: true,
            });
            // 红包盖子关闭
            this.setData({
              isLidDownAniStart: true,
            });
          }, 500);
        }, 1000);
      } catch (err) {
        reject(err);
      }
    });
  },
  handleInterDecimalInput(e) {
    const tmpInterArray = this.data.interArray;
    const tmpDecimalArray = this.data.decimalArray;
    const InterArrayLen = tmpInterArray.length;
    const DecimalArrayLen = tmpDecimalArray.length;
    for (let i = 0; i < InterArrayLen; i += 1) {
      tmpInterArray[i] = e.detail.value.charAt(i) || '';
    }
    for (let i = 0; i < DecimalArrayLen; i += 1) {
      tmpDecimalArray[i] = e.detail.value.charAt(i + InterArrayLen) || '';
    }

    this.setData({
      interArray: tmpInterArray,
      decimalArray: tmpDecimalArray,
    });
  },
  convertEmptyToZero() {
    const tmpInterArray = this.data.interArray;
    const tmpDecimalArray = this.data.decimalArray;
    const InterArrayLen = tmpInterArray.length;
    const DecimalArrayLen = tmpDecimalArray.length;
    for (let i = 0; i < InterArrayLen; i += 1) {
      if (tmpInterArray[i] === '') {
        tmpInterArray[i] = 0;
      }
    }
    for (let i = 0; i < DecimalArrayLen; i += 1) {
      if (tmpDecimalArray[i] === '') {
        tmpDecimalArray[i] = 0;
      }
    }
    this.setData({
      interArray: tmpInterArray,
      decimalArray: tmpDecimalArray,
    });
  },
  removeHeadZero() {
    let tmpResultNum = this.data.resultNum;
    tmpResultNum = '';
    let firstUnZeroInterIndex = -1; // 记录第一个非0数字的整数数组索引
    const tmpInterArray = this.data.interArray;
    const tmpDecimalArray = this.data.decimalArray;
    const InterArrayLen = tmpInterArray.length;
    const DecimalArrayLen = tmpDecimalArray.length;
    for (let i = 0; i < InterArrayLen; i += 1) {
      if (tmpInterArray[i] !== 0 && tmpInterArray[i] !== '0') {
        firstUnZeroInterIndex = i;
        break;
      }
    }
    console.log(firstUnZeroInterIndex);
    if (firstUnZeroInterIndex === -1) {
      // 整数都为0
      tmpResultNum += '0';
    } else {
      tmpResultNum += tmpInterArray
        .slice(firstUnZeroInterIndex, InterArrayLen)
        .join('');
    }
    if (tmpDecimalArray.length === 2) {
      if (tmpDecimalArray[0] !== 0 && tmpDecimalArray[1] === 0) {
        tmpResultNum += `.${tmpDecimalArray[0]}`;
      } else if (tmpDecimalArray[0] === 0 && tmpDecimalArray[1] !== 0) {
        tmpResultNum += `.0${tmpDecimalArray[1]}`;
      } else if (tmpDecimalArray[0] !== 0 && tmpDecimalArray[1] !== 0) {
        tmpResultNum += `.${tmpDecimalArray[0]}${tmpDecimalArray[1]}`;
      }
    } else if (tmpDecimalArray.length === 1) {
      if (tmpDecimalArray[0] !== 0) {
        tmpResultNum += `.${tmpDecimalArray[0]}`;
      }
    }
    this.setData({
      resultNum: tmpResultNum,
    });
  },
  Tap(e) {
    console.log(e);
    this.setData({
      isFocus: true,
    });
  },
  parseTargetVal(targetVal) {
    let tmpInterArray = [];
    let tmpDecimalArray = [];
    if (targetVal.indexOf('.') > -1) {
      tmpInterArray = targetVal.split('.')[0].split('');
      tmpDecimalArray = targetVal.split('.')[1].split('');
    } else {
      tmpInterArray = targetVal.split('');
    }
    tmpInterArray = tmpInterArray.map(() => {
      return '';
    });
    tmpDecimalArray = tmpDecimalArray.map(() => {
      return '';
    });
    this.setData({
      interArray: tmpInterArray,
      decimalArray: tmpDecimalArray,
    });
  },
  parseMyVal(myVal) {
    let tmpInterArray = [];
    let tmpDecimalArray = [];
    if (myVal.indexOf('.') > -1) {
      tmpInterArray = myVal.split('.')[0].split('');
      tmpDecimalArray = myVal.split('.')[1].split('');
    } else {
      tmpInterArray = myVal.split('');
    }
    this.setData({
      interArray: tmpInterArray,
      decimalArray: tmpDecimalArray,
    });
  },
  handleAttend() {
    // 空字符串转成0
    this.convertEmptyToZero();
    // 整数前面，小数后面去0
    this.removeHeadZero();
    if (this.data.resultNum === '0') {
      showWxToast('金额不能为0');
      return;
    }
    console.log(this.data.resultNum);
    if (robLock) {
      return;
    }
    robLock = true;
    attendGuess({
      sort: this.data.sortUnuse,
      robSort: this.data.sort,
      guessMoney: this.data.resultNum,
      hbId: this.data.hbId,
    })
      .then(res => {
        console.log(res);
        if (res.data.code === '200') {
          showWxToast('购买成功!');
          robLock = false;
          this.updateGuessInfo();
        } else if (res.data.code === '202') {
          showWxToast('已经购买过啦!');
          robLock = false;
          this.updateGuessInfo();
        } else if (res.data.code === '203') {
          showWxToast('32个名额已经没啦!等待下一轮!');
          robLock = false;
        } else if (res.data.code === '204') {
          console.log('喵币不足');
          this.recharge();
        } else if (res.data.code === '201') {
          console.log('未开始或已结束');
          robLock = false;
          showWxToast('猜红包尚未开始或已经结束!');
        } else if (res.data.code === '205') {
          robLock = false;
          showWxToast('本轮已经揭晓!等待下一轮!');
        }
      })
      .catch(err => {
        console.log(res);
        robLock = false;
      });
  },
  initGuessInfo() {
    if (robLock) {
      return;
    }
    robLock = true;
    getGuessInfo()
      .then(res => {
        console.log(res);
        robLock = false;
        if (res.data.code === '201') {
          showWxToast('猜红包尚未开始或已经结束!');
        } else if (
          res.data.code === '200' ||
          res.data.code === '202' ||
          res.data.code === '203' ||
          res.data.code === '204' ||
          res.data.code === '205'
        ) {
          let tmpPayUser = this.data.payUser;
          let tmpPayUser2 = JSON.parse(res.data.guess_data_json);
          tmpPayUser.avator = tmpPayUser2.headimgurl;
          tmpPayUser.identity = IDENTITYLIST.find(
            item => item.id === tmpPayUser2.shen_fen
          ).name;
          this.setData({
            guessStatus: 1,
            sort: res.data.rob_sort,
            sortUnuse: res.data.sort,
            sortText: converNumToText(res.data.rob_sort),
            hbId: res.data.red_package_id,
            guessMoney:
              res.data.guess_status === '0' ? '' : res.data.guess_status,
            targetVal: res.data.guess_balance,
            attendNum: res.data.CanYuSize,
            remainNum: res.data.RemainCanYuSize,
            purchaseMoney: res.data.purchase_amount_val,
            payUser: tmpPayUser,
          });
          if (res.data.guess_status === '0') {
            // 还没猜
            // 标准答案解析为整数数组和小数数组
            this.parseTargetVal(this.data.targetVal);
            this.resetBoxAni();
            this.showBoxAni();
          } else {
            // 已经猜过了
            // 自己猜的金额解析为整数数组和小数数组
            this.parseMyVal(this.data.guessMoney);
          }
          endLoop = false;
          // 轮询获取信息
          this.loopGetGuessInfo();
        }
      })
      .catch(err => {
        console.log(err);
        robLock = false;
      });
  },
  updateGuessInfo() {
    getGuessInfo()
      .then(res => {
        console.log(res);
        if (
          res.data.code === '200' ||
          res.data.code === '202' ||
          res.data.code === '203' ||
          res.data.code === '204' ||
          res.data.code === '205'
        ) {
          this.setData({
            sort: res.data.rob_sort,
            sortUnuse: res.data.sort,
            sortText: converNumToText(res.data.rob_sort),
            hbId: res.data.red_package_id,
            guessMoney:
              res.data.guess_status === '0' ? '' : res.data.guess_status,
            targetVal: res.data.guess_balance,
            attendNum: res.data.CanYuSize,
            remainNum: res.data.RemainCanYuSize,
            purchaseMoney: res.data.purchase_amount_val,
          });
          if (this.data.guessMoney === '0') {
            // 还没猜
            // 标准答案解析为整数数组和小数数组
            this.parseTargetVal(this.data.targetVal);
          } else {
            // 已经猜过了
            // 自己猜的金额解析为整数数组和小数数组
            this.parseMyVal(this.data.guessMoney);
          }
        }
      })
      .catch(err => {
        console.log(err);
      });
  },
  // 轮询获取参与者信息
  loopGetGuessInfo() {
    if (endLoop) {
      return;
    }
    getGuessInfo(true)
      .then(res => {
        console.log(res);
        if (
          res.data.code === '200' ||
          res.data.code === '202' ||
          res.data.code === '203' ||
          res.data.code === '204' ||
          res.data.code === '205'
        ) {
          if (res.data.rob_sort !== this.data.sort) {
            // 新的一轮
            this.setData({
              isLidUpAniStart: false,
              isLidDownAniStart: false,
              isPShowAniStart: false,
              isRobBtnAniStart: false,
              hasHbPop: false,
              isHbOpen: false,
              hbVisible: false,
              rankListVisible: false,
              hasClickGoOn: false,
              hasClickShow: false,
              interArray: [],
              decimalArray: [],
              hasAutoPopHb: false,
            });
            danmuIndex = 0;
            DMLIST = [];
            if (res.data.guess_status === '0') {
              // 还没猜
              // 标准答案解析为整数数组和小数数组
              this.resetBoxAni();
              this.showBoxAni();
              this.parseTargetVal(this.data.targetVal);
            } else {
              // 已经猜过了
              // 自己猜的金额解析为整数数组和小数数组
              this.parseMyVal(this.data.guessMoney);
            }
          }
          if (this.data.hasClickGoOn) {
            this.setData({
              guessMoney: '',
            });
            if (!this.data.hasClickShow) {
              this.setData({
                hasClickShow: true,
              });
              this.resetBoxAni();
              this.showBoxAni();
            }

            timeoutTask(() => {
              this.loopGetGuessInfo();
            }, 2000);
            return;
          }
          if (res.data.robRecordList) {
            console.log('showDanmuAni');
            console.log(danmuIndex);
            DMLIST = res.data.robRecordList.list.map(item => {
              let tmpName =
                item.wx_name.length > 4
                  ? item.wx_name.slice(0, 4) + '......'
                  : item.wx_name;
              return tmpName + '猜' + item.guess_money;
            });
            this.showDanmuAni();
          }
          this.setData({
            sort: res.data.rob_sort,
            sortUnuse: res.data.sort,
            sortText: converNumToText(res.data.rob_sort),
            hbId: res.data.red_package_id,
            guessMoney:
              res.data.guess_status === '0' ? '' : res.data.guess_status,
            targetVal: res.data.guess_balance,
            attendNum: res.data.CanYuSize,
            remainNum: res.data.RemainCanYuSize,
            isAnnounce: res.data.play_status === '1' ? true : false,
            purchaseMoney: res.data.purchase_amount_val,
          });

          this.gapHandle(res.data.min_max_json);
          if (res.data.code === '205') {
            if (res.data.robInfo.luckyJson[this.data.userId]) {
              // 猜中
              this.setData({
                hasPrize: true,
                prizeMoney: res.data.robInfo.luckyJson.luckyLotteryMoney,
              });
            } else {
              // 没猜中
              this.setData({
                hasPrize: false,
                prizeMoney: '',
              });
            }
            // 明细列表
            this.setData({
              rankList: res.data.robInfo.infoList,
              hasPrizeRounds: res.data.robInfo.luckyJson.lottery_size >= 1,
            });
          }
          if (this.data.isAnnounce) {
            this.autoAnnounceHb();
          }
        } else if (res.data.code === '201') {
          this.setData({
            guessStatus: 0,
            isLidUpAniStart: false,
            isLidDownAniStart: false,
            isPShowAniStart: false,
            isRobBtnAniStart: false,
            hasHbPop: false,
            isHbOpen: false,
          });
          endLoop = true;
        }
        timeoutTask(() => {
          this.loopGetGuessInfo();
        }, 2000);
      })
      .catch(err => {
        console.log(err);
        endLoop = true;
      });
  },
  recharge() {
    guessHbRecharge({
      money: this.data.purchaseMoney,
      userId: this.data.userId,
      openid: this.data.openId,
    })
      .then(res => {
        console.log(res);
        if (res.status === 'success') {
          wxPay(res)
            .then(res2 => {
              console.log(res2);
              showWxToast('充值成功!');
              robLock = false;
              app.globalData.isH5NeedRefresh = true;
              //充值完成 等待后台加喵钻逻辑完成后 去猜红包
              timeoutTask(() => {
                this.handleAttend();
              }, 500);
            })
            .catch(err => {
              console.log(err);
              robLock = false;
              showWxToast('充值失败!');
            });
        }
      })
      .catch(err => {
        console.log(err);
        reject(err);
      });
  },
  // 自动揭晓红包
  autoAnnounceHb() {
    if (this.data.hasAutoPopHb) {
      return;
    }
    this.setData({
      hasAutoPopHb: true,
    });
    if (!this.data.hasHbPop) {
      this.setData({
        hbVisible: true,
      });
    } else {
      this.setData({
        rankListVisible: true,
      });
    }
  },
  // 揭晓红包
  announceHb() {
    if (!this.data.isAnnounce) {
      showWxToast('等待揭晓！');
      return;
    }
    if (!this.data.hasHbPop) {
      this.setData({
        hbVisible: true,
      });
    } else {
      this.setData({
        rankListVisible: true,
      });
    }
  },
  // 继续参与
  contiAttend() {
    this.resetBoxAni();
    this.setData({
      rankListVisible: false,
      hbVisible: false,
      hasHbPop: true,
      hasClickGoOn: true,
    });
  },
  checkResult() {
    this.setData({
      hbVisible: false,
      hasHbPop: true,
      rankListVisible: true,
    });
  },
  closeHb() {
    this.setData({
      hbVisible: false,
      hasHbPop: true,
    });
  },
  closeRank() {
    this.setData({
      rankListVisible: false,
    });
  },
  gapHandle(gapStr) {
    if (!gapStr) {
      return;
    }
    const gapObj = JSON.parse(gapStr);
    Object.keys(gapObj).forEach(item => {
      if (
        parseInt(item.split('_')[1], 10) ===
        parseInt(this.data.sort, 10) - 1
      ) {
        if (item.split('_')[0] === 'shang') {
          this.setData({
            gapMax: gapObj[item] === '0' ? '5000' : gapObj[item],
          });
        } else if (item.split('_')[0] === 'xia') {
          this.setData({
            gapMin: gapObj[item] === '0' ? '0' : gapObj[item],
          });
        }
      }
    });
  },
  showBoxAni() {
    this.setData({
      boxShowAni: true,
    });
    timeoutTask(() => {
      this.setData({
        boxShowAni: false,
        boxShow: true,
        iptShowAni: true,
      });
      timeoutTask(() => {
        this.shineAni();
        timeoutTask(() => {
          this.setData({
            isFocus: true,
          });
        }, 2000);
      }, 500);
    }, 2000);
    timeoutTask(() => {
      this.setData({
        textShowAni: true,
      });
    }, 1000);
  },
  resetBoxAni() {
    this.setData({
      boxShowAni: false,
      boxShow: false,
      textShowAni: false,
      iptShowAni: false,
      isFocus: false,
    });
  },
  shineAni() {
    this.setData({
      shineShow: true,
    });
    timeoutTask(() => {
      this.setData({
        shineShow: false,
      });
    }, 1000);
  },
  showDanmuAni() {
    if (danmuIndex >= DMLIST.length) {
      return;
    }
    console.log(DMLIST[danmuIndex]);
    this.setData({
      activeDanmuCt: DMLIST[danmuIndex],
      danmuAniShow: true,
    });
    timeoutTask(() => {
      this.setData({
        danmuAniShow: false,
      });
      timeoutTask(() => {
        danmuIndex += 1;
        this.showDanmuAni();
      }, 1000);
    }, 3000);
  },
});
```

## File: pages/guessHb/guessHb.json
```json
{
    "navigationBarTitleText": "猜红包",
    "disableScroll": true
  }
```

## File: pages/guessHb/guessHb.wxml
```
<view class="guessHbContainer">
    <!-- 等待界面 -->
    <view class="waitMod" wx:if="{{guessStatus === 0}}">
        <view class="mainBox">
            <image src="https://static.hudongmiao.com/joymewMp/guessHb/guessHbRuleTitle.png" class="guessHbRuleTitle"></image>
            <view class="ruleList">
                <view class="ruleItem">
                    <view class="num">1.</view>
                    等待新人充值红包才可开启猜红包
                </view>
                <view class="ruleItem">
                    <view class="num">2.</view>
                    每轮参与人数最多为32名来宾
                </view>
                <view class="ruleItem">
                    <view class="num">3.</view>
                    每轮参与金额不同，越往后参与金额越高
                </view>
                <view class="ruleItem">
                    <view class="num">4.</view>
                    每轮竞猜都会显示猜中或未猜中，如本轮 未猜中会显示最接近的区间范围
                </view>
                <view class="ruleItem">
                    <view class="num">5.</view>
                    如果本轮有多名来宾猜中，将平分红包
                </view>
                <view class="ruleItem">
                    <view class="num">6.</view>
                    猜中红包直接到账您的微信零钱
                </view>
            </view>
            <view class="attendBtn" bindtap="initGuessInfo">立即参与</view>
        </view>
    </view>
    <!-- 竞猜界面 -->
    <view class="guessMod" wx:if="{{guessStatus === 1 && !guessMoney}}">
        <!-- 竞猜弹幕模块 -->
        <view class="danmuModule">
            <view class="danmu {{danmuAniShow ? 'danmuAni' : ''}}">{{activeDanmuCt}}</view>
        </view>
        <image src="{{payUser.avator}}" class="avator"></image>
        <view class="gameTip">{{payUser.identity}}邀请你竞猜红包</view>
        <view class="mainBox {{boxShowAni ? 'boxShowAni' : ''}} {{boxShow ? 'boxShow' : ''}} {{textShowAni ? 'textShowAni' : ''}} {{iptShowAni ? 'iptShowAni' : ''}}">
            <image src="https://static.joymew.com/joymewMp/guessHb/shineAni.webp" class="shineImg {{shineShow ? 'active' : ''}}" />
            <view class="roundsNum">第{{sortText}}轮</view>
            <view class="guessTip" wx:if="{{sort === '1'}}">小提示：有几个框即为几位数字</view>
            <view class="guessTip" wx:if="{{sort !== '1'}}">上一轮竞猜区间为：{{gapMin}}~{{gapMax}}</view>
            <view class="iptGroup {{interArray.length + decimalArray.length === 1 || interArray.length + decimalArray.length === 2 || interArray.length + decimalArray.length === 3 || interArray.length + decimalArray.length === 4 ? 'one': ''}} {{interArray.length + decimalArray.length === 5? 'two': ''}}" wx:if="{{!hbVisible && !rankListVisible}}">
                <input type="number" value="{{item}}" wx:for="{{interArray}}" wx:key="index" data-index="{{index}}" catchtap='Tap' disabled="{{true}}" />
                <view class="dot" wx:if="{{decimalArray.length > 0}}"></view>
                <input type="number" value="{{item}}" wx:for="{{decimalArray}}" wx:key="index" data-index="{{index}}" catchtap='Tap' disabled="{{true}}" />
            </view>
            <input class="hideIpt" focus="{{isFocus}}" bindinput="handleInterDecimalInput" maxlength="{{interArray.length + decimalArray.length}}" type="number"/>
            <view class="attendInfo">
                本轮已有
                <view class="num">{{attendNum}}</view>
                人参与，剩余
                <view class="num">{{remainNum - attendNum}}</view>
                个名额
            </view>
            <view class="attendTip">抓紧时间参与吧~</view>
            <view class="confirmBtn" bindtap="handleAttend">立即参与</view>
            <view class="price">本轮竞猜金额：{{purchaseMoney}}元</view>
        </view>
    </view>
    <!-- 竞猜结束，等待揭晓界面 -->
    <view class="guessResultWaitMod" wx:if="{{guessStatus === 1 && guessMoney}}">
        <!-- 竞猜弹幕模块 -->
        <view class="danmuModule">
            <view class="danmu {{danmuAniShow ? 'danmuAni' : ''}}">{{activeDanmuCt}}</view>
        </view>
        <image src="{{payUser.avator}}" class="avator"></image>
        <view class="gameTip">{{payUser.identity}}邀请你竞猜红包</view>
        <view class="mainBox">
            <view class="myGuessTitle">我的竞猜数字</view>
            <view class="iptGroup {{interArray.length + decimalArray.length === 1 || interArray.length + decimalArray.length === 2 || interArray.length + decimalArray.length === 3 || interArray.length + decimalArray.length === 4 ? 'one': ''}} {{interArray.length + decimalArray.length === 5? 'two': ''}}" wx:if="{{!hbVisible && !rankListVisible}}" wx:if="{{!hbVisible && !rankListVisible}}">
                <input type="number" value="{{item}}" wx:for="{{interArray}}" wx:key="index" data-index="{{index}}" disabled="{{true}}" />
                <view class="dot" wx:if="{{decimalArray.length > 0}}"></view>
                <input type="number" value="{{item}}" wx:for="{{decimalArray}}" wx:key="index" data-index="{{index}}" disabled="{{true}}" />
            </view>
            <view class="waitResultTip">竞猜结果等待主持人揭晓</view>
            <view class="attendInfo">
                已竞猜人数：
                <view class="num">{{attendNum}}/{{remainNum}}</view>
                人
            </view>
            <view class="waitOpenBtn {{isAnnounce?'active':''}}" bindtap="announceHb">
                {{isAnnounce ? '查看结果' : '等待揭晓'}}
            </view>
        </view>
    </view>
    <!-- 弹出红包模块 -->
    <view class="hbModule" wx:if="{{hbVisible}}">
        <view class="shade" bindtap="closeHb"></view>
        <view class="hbBox">
            <view class="lidArea {{isLidUpAniStart?'up':''}} {{isLidDownAniStart?'down':''}}">
                <view class="wish">大吉大利</view>
                <view class="wish2">祝您一猜就对～</view>
            </view>
            <view class="prizeArea {{isPShowAniStart?'show':'' }}">
                <view class="prized" wx:if="{{hasPrize}}">
                    <view class="guessNum">精准数字{{targetVal}}</view>
                    <view class="congratuTip">恭喜您获得竞猜红包</view>
                    <view class="money">
                        {{prizeMoney}}
                        <view class="unit">元</view>
                    </view>
                    <view class="getMoneyTip1">红包已到账您的微信零钱</view>
                    <view class="getMoneyTip2">感谢您的参与</view>
                    <view class="continueBtn" bindtap="contiAttend">继续参与</view>
                    <view class="checkDetail" bindtap="checkResult">查看竞猜结果</view>
                </view>
                <view class="unprized" wx:if="{{!hasPrize}}">
                    <view class="pityTip">很遗憾</view>
                    <view class="pityTip2">只差一点点，本轮没有猜中</view>
                    <view class="continueBtn" bindtap="contiAttend">继续参与</view>
                    <view class="checkDetail" bindtap="checkResult">查看竞猜结果</view>
                </view>
            </view>
            <view class="openBtn {{!isRobBtnAniStart?'commonActive':''}} {{isRobBtnAniStart?'active':''}}" wx:if="{{!isHbOpen}}" bindtap="robHb">
                开
            </view>
        </view>
    </view>
    <!-- 弹出竞猜结果模块 -->
    <view class="resultModule" wx:if="{{rankListVisible}}">
        <view class="shade" bindtap="closeRank"></view>
        <view class="resultBox">
            <image src="https://static.hudongmiao.com/joymewMp/guessHb/guessResultTitle.png" class="guessResultTitle"></image>
            <view class="resultTip">{{hasPrizeRounds ? '本轮红包已被猜中' : '本轮无人猜中，排名按最接近展示'}}</view>
            <view class="guessList">
                <view class="guessItem" wx:for="{{rankList}}" wx:key="index">
                    <view class="num">{{index + 1}}</view>
                    <view class="avator">
                        <image class="avatorImg" src="{{item.avator}}"></image>
                    </view>
                    <view class="nickname">{{item.wx_name}}</view>
                    <view class="guessVal">{{item.guess_money}}</view>
                    <view class="guessRt {{item.lucky_dog === '1' ? 'right' : ''}}">
                        {{item.lucky_dog === '1' ? '已猜中' : '未猜中'}}
                    </view>
                </view>
            </view>
            <view class="continueBtn" bindtap="contiAttend">继续参与</view>
        </view>
    </view>
</view>
```

## File: pages/guessHb/guessHb.wxss
```
.guessHbContainer {
  position: absolute;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/guessHbBg2.png');
  background-size: 100% 100%;
}
/* 等待界面 */
.waitMod {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.waitMod > .mainBox {
  width: 630rpx;
  height: 1000rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/guessHbBox2.png');
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 66rpx;
}
.waitMod > .mainBox > .guessHbRuleTitle {
  width: 422rpx;
  height: 88rpx;
}
.waitMod > .mainBox > .ruleList {
  width: 528rpx;
  font-size: 28rpx;
  font-weight: 400;
  color: #ffffff;
  line-height: 60rpx;
  margin-top: 40rpx;
}
.waitMod > .mainBox > .ruleList > .ruleItem {
  width: 100%;
  position: relative;
  padding-left: 32rpx;
}
.waitMod > .mainBox > .ruleList > .ruleItem > .num {
  position: absolute;
  left: 0rpx;
}
.waitMod > .mainBox > .attendBtn {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 462rpx;
  height: 80rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/confirmBg.png');
  background-size: 100% 100%;
  margin-top: 164rpx;
  font-size: 32rpx;
  font-weight: 400;
  color: #8d592f;
}
/* 竞猜界面 */
.guessMod {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 40rpx;
}
.guessMod > .danmuModule {
  width: 100%;
  height: 16%;
  position: absolute;
  top: 0;
  left: 0;
}
.guessMod > .danmuModule > .danmu {
  border-radius: 35rpx;
  text-align: center;
  width: 237rpx;
  padding: 0 20rpx;
  height: 65rpx;
  line-height: 65rpx;
  font-size: 23rpx;
  font-weight: 400;
  color: #ffffff;
  position: absolute;
  left: -235rpx;
  top: 50rpx;
  background-color: rgba(0, 0, 0, 0.6);
}
.guessMod > .danmuModule > .danmu.danmuAni {
  animation-name: danmuShowAni;
  animation-duration: 3s;
  animation-iteration-count: 1;
  animation-timing-function: ease-in;
}
.guessMod > .avator {
  width: 138rpx;
  height: 138rpx;
  border-radius: 50%;
}
.guessMod > .gameTip {
  font-size: 36rpx;
  font-weight: 500;
  color: #ffffff;
  margin-top: 16rpx;
}
.guessMod > .mainBox {
  width: 630rpx;
  height: 1000rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/guessHbBox2.png');
  background-size: 100% 100%;
  margin-top: 28rpx;
  padding-top: 40rpx;
  transform: scale(0.4) translateY(3056rpx);
  position: relative;
}
.guessMod > .mainBox > .shineImg {
  position: absolute;
  width: 119%;
  height: 136%;
  bottom: -4%;
  left: -10%;
  opacity: 0;
}
.guessMod > .mainBox > .shineImg.active {
  opacity: 1;
}
.guessMod > .mainBox > .roundsNum {
  width: 100%;
  text-align: center;
  font-size: 48rpx;
  color: #fdf1ac;
  font-weight: 500;
  opacity: 0;
  transition: all 1s ease-out;
}
.guessMod > .mainBox > .guessTip {
  width: 100%;
  text-align: center;
  font-size: 24rpx;
  color: #ffffff;
  margin-top: 32rpx;
  opacity: 0;
  transition: all 1s ease-out;
}
.guessMod > .mainBox > .iptGroup {
  width: 95%;
  margin: 0 auto;
  margin-top: 60rpx;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  opacity: 0;
  transition: all 1s ease-out;
}
.guessMod > .mainBox > .iptGroup > input {
  width: 72rpx;
  height: 72rpx;
  background-color: #ffffff;
  border: none;
  outline: none;
  font-size: 32rpx;
  font-weight: 400;
  color: #8d592f;
  text-align: center;
  margin: 0 12rpx;
}
.guessMod > .mainBox > .iptGroup.one > input {
  width: 119rpx;
  height: 119rpx;
  font-size: 72rpx;
}
.guessMod > .mainBox > .iptGroup.two > input {
  width: 88rpx;
  height: 88rpx;
  font-size: 36rpx;
}
.guessMod > .mainBox > .hideIpt {
  width: 0;
  height: 0;
}
.guessMod > .mainBox > .iptGroup > .dot {
  width: 8rpx;
  height: 8rpx;
  background: #ffffff;
  border-radius: 50%;
}
.guessMod > .mainBox > .attendInfo {
  width: 100%;
  margin-top: 114rpx;
  font-size: 28rpx;
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  opacity: 0;
  transition: all 1s ease-out;
}
.guessMod > .mainBox > .attendInfo > .num {
  font-size: 48rpx;
  color: #fdf1ac;
  margin: 0 6rpx;
}
.guessMod > .mainBox > .attendTip {
  font-size: 28rpx;
  color: #ffffff;
  margin-top: 24rpx;
  padding-left: 102rpx;
  opacity: 0;
  transition: all 1s ease-out;
}
.guessMod > .mainBox > .confirmBtn {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 462rpx;
  height: 80rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/confirmBg.png');
  background-size: 100% 100%;
  margin: 0 auto;
  margin-top: 190rpx;
  font-size: 32rpx;
  font-weight: 400;
  color: #8d592f;
  opacity: 0;
  transition: all 1s ease-out;
  position: relative;
  z-index: 1;
}
.guessMod > .mainBox > .price {
  width: 100%;
  text-align: center;
  font-size: 28rpx;
  color: #ffffff;
  font-weight: 400;
  margin-top: 26rpx;
  opacity: 0;
  transition: all 1s ease-out;
}
.guessMod > .mainBox.boxShowAni {
  animation-name: boxShowAni;
  animation-duration: 2s;
  animation-iteration-count: 1;
  animation-timing-function: ease-in;
}
.guessMod > .mainBox.textShowAni > .roundsNum {
  opacity: 1;
}
.guessMod > .mainBox.textShowAni > .guessTip {
  opacity: 1;
}
.guessMod > .mainBox.textShowAni > .attendInfo {
  opacity: 1;
}
.guessMod > .mainBox.textShowAni > .attendTip {
  opacity: 1;
}
.guessMod > .mainBox.textShowAni > .confirmBtn {
  opacity: 1;
}
.guessMod > .mainBox.textShowAni > .price {
  opacity: 1;
}
.guessMod > .mainBox.iptShowAni > .iptGroup {
  opacity: 1;
}
.guessMod > .mainBox.boxShow {
  transform: scale(1) translateY(0rpx);
}
/* 竞猜结束，等待揭晓界面 */
.guessResultWaitMod {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 40rpx;
}
.guessResultWaitMod > .danmuModule {
  width: 100%;
  height: 16%;
  position: absolute;
  top: 0;
  left: 0;
}
.guessResultWaitMod > .danmuModule > .danmu {
  border-radius: 35rpx;
  text-align: center;
  width: 237rpx;
  padding: 0 20rpx;
  height: 65rpx;
  line-height: 65rpx;
  font-size: 23rpx;
  font-weight: 400;
  color: #ffffff;
  position: absolute;
  left: -235rpx;
  top: 50rpx;
  background-color: rgba(0, 0, 0, 0.6);
}
.guessResultWaitMod > .danmuModule > .danmu.danmuAni {
  animation-name: danmuShowAni;
  animation-duration: 3s;
  animation-iteration-count: 1;
  animation-timing-function: ease-in;
}
.guessResultWaitMod > .avator {
  width: 138rpx;
  height: 138rpx;
  border-radius: 50%;
}
.guessResultWaitMod > .gameTip {
  font-size: 36rpx;
  font-weight: 500;
  color: #ffffff;
  margin-top: 16rpx;
}
.guessResultWaitMod > .mainBox {
  width: 630rpx;
  height: 1000rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/guessHbBox2.png');
  background-size: 100% 100%;
  margin-top: 28rpx;
  padding-top: 112rpx;
}
.guessResultWaitMod > .mainBox > .shineImg {
  position: absolute;
  width: 119%;
  height: 136%;
  bottom: -4%;
  left: -10%;
  opacity: 0;
}
.guessResultWaitMod > .mainBox > .shineImg.active {
  opacity: 1;
}
.guessResultWaitMod > .mainBox > .myGuessTitle {
  width: 100%;
  text-align: center;
  font-size: 48rpx;
  color: #ffffff;
}
.guessResultWaitMod > .mainBox > .iptGroup {
  width: 90%;
  margin: 0 auto;
  margin-top: 109rpx;
  display: flex;
  align-items: flex-end;
  justify-content: center;
}
.guessResultWaitMod > .mainBox > .iptGroup.one > input {
  width: 119rpx;
  height: 119rpx;
  font-size: 72rpx;
}
.guessResultWaitMod > .mainBox > .iptGroup.two > input {
  width: 88rpx;
  height: 88rpx;
  font-size: 36rpx;
}
.guessResultWaitMod > .mainBox > .iptGroup > input {
  width: 72rpx;
  height: 72rpx;
  background-color: #ffffff;
  border: none;
  outline: none;
  font-size: 32rpx;
  font-weight: 400;
  color: #8d592f;
  text-align: center;
  margin: 0 12rpx;
}
.guessResultWaitMod > .mainBox > .iptGroup > .dot {
  width: 8rpx;
  height: 8rpx;
  background: #ffffff;
  border-radius: 50%;
}
.guessResultWaitMod > .mainBox > .waitResultTip {
  font-size: 28rpx;
  color: #ffffff;
  margin-top: 118rpx;
  width: 100%;
  text-align: center;
}
.guessResultWaitMod > .mainBox > .attendInfo {
  width: 100%;
  margin-top: 40rpx;
  font-size: 28rpx;
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}
.guessResultWaitMod > .mainBox > .attendInfo > .num {
  font-size: 48rpx;
  color: #fdf1ac;
  margin: 0 6rpx;
}
.guessResultWaitMod > .mainBox > .waitOpenBtn {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 462rpx;
  height: 80rpx;
  background-color: #a0a0a0;
  margin: 0 auto;
  margin-top: 158rpx;
  font-size: 32rpx;
  font-weight: 400;
  color: #ffffff;
  border-radius: 8rpx;
}
.guessResultWaitMod > .mainBox > .waitOpenBtn.active {
  background-color: #fadaab;
  color: #8d592f;
}
.guessResultWaitMod > .mainBox.boxShowAni {
  animation-name: boxShowAni;
  animation-duration: 2s;
  animation-iteration-count: 1;
  animation-timing-function: ease-in;
}
.guessResultWaitMod > .mainBox.textShowAni > .myGuessTitle {
  opacity: 1;
}
.guessResultWaitMod > .mainBox.textShowAni > .waitResultTip {
  opacity: 1;
}
.guessResultWaitMod > .mainBox.textShowAni > .attendInfo {
  opacity: 1;
}
.guessResultWaitMod > .mainBox.textShowAni > .waitOpenBtn {
  opacity: 1;
}
.guessResultWaitMod > .mainBox.iptShowAni > .iptGroup {
  opacity: 1;
}
.guessResultWaitMod > .mainBox.boxShow {
  transform: scale(1) translateY(0rpx);
}
/* 弹出红包模块 */
.hbModule {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  background-color: rgba(0, 0, 0, 0.6);
}
.hbModule > .shade {
  position: absolute;
  width: 100%;
  height: 100%;
}
.hbModule > .hbBox {
  width: 560rpx;
  height: 734rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/hbBg.png');
  background-size: 100% 100%;
  position: absolute;
  top: 320rpx;
  perspective: 400rpx;
}
.hbModule > .hbBox > .lidArea {
  width: 560rpx;
  height: 548rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/hbLid.png');
  background-size: 100% 100%;
  transition: all linear 0.5s;
  transform: translateY(0rpx);
  z-index: 2;
  padding-top: 94rpx;
}
.hbModule > .hbBox > .lidArea.up {
  transform: translateY(-240rpx);
  z-index: 1;
}
.hbModule > .hbBox > .lidArea.down {
  transform: translateY(0rpx);
  z-index: 1;
}
.hbModule > .hbBox > .lidArea > .wish {
  width: 100%;
  text-align: center;
  font-size: 48rpx;
  font-weight: 400;
  color: #ffffff;
}
.hbModule > .hbBox > .lidArea > .wish2 {
  width: 100%;
  text-align: center;
  font-size: 48rpx;
  font-weight: 400;
  color: #ffffff;
  margin-top: 126rpx;
}
.hbModule > .hbBox > .openBtn {
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/openBtnBg.png');
  background-size: 100% 100%;
  width: 328rpx;
  height: 320rpx;
  position: absolute;
  left: 112.5rpx;
  top: 390rpx;
  font-size: 88rpx;
  font-weight: 500;
  color: #9a5804;
  padding-top: 12vw;
  z-index: 2;
  display: flex;
  justify-content: center;
}
.hbModule > .hbBox > .openBtn.active {
  animation-name: rotateY;
  animation-duration: 1s;
  animation-timing-function: ease-out;
  animation-fill-mode: forwards;
}
.hbModule > .hbBox > .openBtn.commonActive {
  animation-name: scaleAni;
  animation-duration: 2s;
  animation-timing-function: ease-out;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
}
.hbModule > .hbBox > .prizeArea {
  width: 528rpx;
  height: 620rpx;
  position: absolute;
  top: -70rpx;
  left: 15rpx;
  z-index: 1;
  transition: all linear 0.1s;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/prizeBg.png');
  background-size: 100% 100%;
  opacity: 0;
}
.hbModule > .hbBox > .prizeArea.show {
  opacity: 1;
}
.hbModule > .hbBox > .prizeArea > .unprized {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 178rpx;
}
.hbModule > .hbBox > .prizeArea > .unprized > .pityTip {
  font-size: 56rpx;
  color: #c87a3a;
  font-weight: 500;
}
.hbModule > .hbBox > .prizeArea > .unprized > .pityTip2 {
  font-size: 36rpx;
  color: #c87a3a;
  font-weight: 500;
  margin-top: 36rpx;
}

.hbModule > .hbBox > .prizeArea > .unprized > .continueBtn {
  width: 320rpx;
  height: 68rpx;
  background: linear-gradient(90deg, #fffeec, #ffde8d 100%);
  border-radius: 54rpx;
  font-size: 36rpx;
  font-weight: 500;
  color: #ca2e1b;
  position: absolute;
  bottom: -100rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}
.hbModule > .hbBox > .prizeArea > .unprized > .checkDetail {
  position: absolute;
  font-size: 28rpx;
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  bottom: -155rpx;
  left: 200rpx;
  padding-bottom: 4rpx;
}
.hbModule > .hbBox > .prizeArea > .unprized > .checkDetail::after {
  content: '';
  display: block;
  width: 100%;
  height: 2px;
  background-color: #ffffff;
  position: absolute;
  bottom: 0;
}

.hbModule > .hbBox > .prizeArea > .prized {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 94rpx;
}
.hbModule > .hbBox > .prizeArea > .prized > .guessNum {
  font-size: 36rpx;
  color: #c87a3a;
  font-weight: 500;
}
.hbModule > .hbBox > .prizeArea > .prized > .congratuTip {
  font-size: 36rpx;
  color: #c87a3a;
  font-weight: 500;
  margin-top: 64rpx;
}
.hbModule > .hbBox > .prizeArea > .prized > .money {
  margin-top: 28rpx;
  font-size: 56rpx;
  color: #f61e28;
  font-weight: 500;
  display: flex;
  align-items: flex-end;
}
.hbModule > .hbBox > .prizeArea > .prized > .money > .unit {
  font-size: 36rpx;
  color: #c87a3a;
  margin-left: 6rpx;
}
.hbModule > .hbBox > .prizeArea > .prized > .getMoneyTip1 {
  font-size: 28rpx;
  font-weight: 500;
  color: #c87a3a;
  margin-top: 106rpx;
}
.hbModule > .hbBox > .prizeArea > .prized > .getMoneyTip2 {
  font-size: 28rpx;
  font-weight: 500;
  color: #c87a3a;
}
.hbModule > .hbBox > .prizeArea > .prized > .continueBtn {
  width: 320rpx;
  height: 68rpx;
  background: linear-gradient(90deg, #fffeec, #ffde8d 100%);
  border-radius: 54rpx;
  font-size: 36rpx;
  font-weight: 500;
  color: #ca2e1b;
  position: absolute;
  bottom: -100rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}
.hbModule > .hbBox > .prizeArea > .prized > .checkDetail {
  position: absolute;
  font-size: 28rpx;
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  bottom: -155rpx;
  left: 200rpx;
  padding-bottom: 4rpx;
}
.hbModule > .hbBox > .prizeArea > .prized > .checkDetail::after {
  content: '';
  display: block;
  width: 100%;
  height: 2px;
  background-color: #ffffff;
  position: absolute;
  bottom: 0;
}
/* 弹出竞猜结果模块 */
.resultModule {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  background-color: rgba(0, 0, 0, 0.6);
}
.resultModule > .shade {
  position: absolute;
  width: 100%;
  height: 100%;
}
.resultModule > .resultBox {
  width: 630rpx;
  height: 1000rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/guessHb/guessHbBox2.png');
  background-size: 100% 100%;
  position: absolute;
  top: 148rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 32rpx;
}
.resultModule > .resultBox > .continueBtn {
  width: 320rpx;
  height: 68rpx;
  background: linear-gradient(90deg, #fffeec, #ffde8d 100%);
  border-radius: 54rpx;
  font-size: 36rpx;
  font-weight: 500;
  color: #ca2e1b;
  position: absolute;
  bottom: -24rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}
.resultModule > .resultBox > .guessResultTitle {
  width: 140rpx;
  height: 36rpx;
}
.resultModule > .resultBox > .resultTip {
  font-size: 32rpx;
  font-weight: 400;
  color: #fdf1ac;
  margin-top: 22rpx;
}
.resultModule > .resultBox > .guessList {
  width: 100%;
  margin-top: 30rpx;
  height: 809rpx;
  overflow-y: scroll;
}
.resultModule > .resultBox > .guessList > .guessItem {
  display: flex;
  align-items: center;
  padding: 0 32rpx;
  margin-bottom: 18rpx;
}
.resultModule > .resultBox > .guessList > .guessItem > .num {
  width: 49rpx;
  font-size: 36rpx;
  font-weight: 400;
  color: #ffffff;
}
.resultModule > .resultBox > .guessList > .guessItem > .avator {
  width: 64rpx;
  height: 64rpx;
  border-radius: 50%;
  background-color: #f8d9b5;
  margin-left: 15rpx;
}
.resultModule > .resultBox > .guessList > .guessItem > .avator > .avatorImg {
  width: 100%;
  height: 100%;
  border-radius: 50%;
}
.resultModule > .resultBox > .guessList > .guessItem > .nickname {
  width: 167rpx;
  font-size: 28rpx;
  font-weight: 400;
  color: #ffffff;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin-left: 14rpx;
}
.resultModule > .resultBox > .guessList > .guessItem > .guessVal {
  width: 112rpx;
  font-size: 28rpx;
  font-weight: 400;
  color: #ffffff;
  margin-left: 15rpx;
}
.resultModule > .resultBox > .guessList > .guessItem > .guessRt {
  font-size: 28rpx;
  font-weight: 400;
  color: #ffffff;
  margin-left: 30rpx;
}
.resultModule > .resultBox > .guessList > .guessItem > .guessRt.right {
  color: #26e900;
}
.resultModule > .resultBox > .guessList > .guessItem.meInfo > .nickname {
  color: #fdf1ac;
}
.resultModule > .resultBox > .guessList > .guessItem.meInfo > .guessVal {
  color: #fdf1ac;
}
.resultModule > .resultBox > .guessList > .guessItem.meInfo > .guessRt {
  color: #fdf1ac;
}
@keyframes rotateY {
  0% {
    transform: rotateY(0deg) translateZ(10px);
    opacity: 1;
  }

  70% {
    transform: rotateY(720deg) translateZ(10px);
    opacity: 1;
  }

  100% {
    transform: rotateY(720deg) translateZ(-400px);
    opacity: 0;
  }
}
@keyframes scaleAni {
  0% {
    transform: scale(1);
  }

  70% {
    transform: scale(0.8);
  }

  100% {
    transform: scale(1);
  }
}
@keyframes boxShowAni {
  0% {
    transform: scale(0.4) translateY(6112.5px);
  }
  60% {
    transform: scale(0.4) translateY(120px);
  }
  100% {
    transform: scale(1) translateY(0px);
  }
}

@keyframes danmuShowAni {
  0% {
    transform: translate(0, 0);
    opacity: 1;
  }
  10% {
    transform: translate(292rpx, 0);
    opacity: 1;
  }
  80% {
    transform: translate(292rpx, 0);
    opacity: 1;
  }
  100% {
    transform: translate(292rpx, -80rpx);
    opacity: 0;
  }
}
```

## File: pages/hbkdRecharge/hbkdRecharge.js
```javascript
import { rechageHbkd, getHbkdList } from '../../api/hbkdRecharge/hbkdRecharge';
import { wxPay } from '../../api/pay';
import { sendGiftBroadCast } from '../../api/recharge/recharge';
import { timeoutTask, showWxToast } from '../../utils/index';

const app = getApp();
const rechargeLocatInfo = [
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon6.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon5.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon1.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon2.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon3.png',
  },
  {
    price: '',
    txt: '自定义金额',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon4.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon6.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon5.png',
  },
  {
    price: 0,
    txt: '充值',
    bg: 'https://static.hudongmiao.com/joymewMp/hbkdRecharge/coupon1.png',
  },
];
let requestLock = false;
Page({
  data: {
    userId: '',
    openId: '',
    remainMoney: 0,
    hbkdRechargeList: [],
    hbkdList: [],
    moneyInput: '',
    inputVisible: false,
    isFocus: false,
    prizeSize: 0,
    hbkdRemainVisible: true,
  },
  onLoad: function(options) {
    this.setData({
      userId: options.userId,
      openId: options.openId,
      remainMoney: options.remainMoney,
      hbkdRemainVisible: options.hbkdRemainVisible === 'false' ? false : true,
    });
    this.handleHbkdRechargeList(options.hbkdRechargeListStr);
    this.getHbkdList();
  },
  onShow: function() {},
  onUnload: function() {},
  handleHbkdRechargeList: function(arrStr) {
    const arr = arrStr.split(',');
    const tmpHbkdRechargeList = [];
    const len = rechargeLocatInfo.length;
    if (!arr || arr.length === 0) {
      showWxToast('参数异常!');
      timeoutTask(() => {
        wx.navigateBack();
      }, 500);
    }
    for (let i = 0; i < len; i += 1) {
      if (i <= 4) {
        tmpHbkdRechargeList.push({
          price: arr[i],
          bg: rechargeLocatInfo[i].bg,
          txt: rechargeLocatInfo[i].txt,
          isCustom: false,
        });
      } else if (i === 5) {
        tmpHbkdRechargeList.push({
          price: '土豪随意',
          bg: rechargeLocatInfo[i].bg,
          txt: rechargeLocatInfo[i].txt,
          isCustom: true,
        });
      } else {
        tmpHbkdRechargeList.push({
          price: arr[i - 1],
          bg: rechargeLocatInfo[i].bg,
          txt: rechargeLocatInfo[i].txt,
          isCustom: false,
        });
      }
    }

    this.setData({
      hbkdRechargeList: tmpHbkdRechargeList,
    });
  },
  handleTap: function(e) {
    if (e.currentTarget.dataset.custom) {
      // 自定义价格 input显现
      this.setData({
        isFocus: true,
        inputVisible: true,
      });
      console.log(e);
    } else {
      // 固定价格 input隐藏 直接调用支付
      this.setData({
        inputVisible: false,
      });
      this.pay(e.currentTarget.dataset.money);
    }
  },
  handleMoneyInput: function(e) {
    let tmpMoneyStr = e.detail.value;
    let r = /^\+?[1-9][0-9]*$/; //正整数
    let flag = r.test(tmpMoneyStr);
    if (flag || tmpMoneyStr === '0.01') {
      // 只能是正整数或者是0.01
      this.setData({
        moneyInput: tmpMoneyStr,
      });
    } else {
      this.setData({
        moneyInput: '',
      });
    }
  },
  handleMoneyBlur: function(e) {
    if (!this.data.moneyInput) {
      showWxToast('请输入或者选择充值金额!');
      return;
    }
    if (this.data.moneyInput === '0') {
      showWxToast('充值金额不能为0!');
      return;
    }
    this.pay(this.data.moneyInput);
  },
  pay: function(choosedMoney) {
    if (!requestLock) {
      requestLock = true;
      rechageHbkd({
        total: choosedMoney,
        userId: this.data.userId,
        openId: this.data.openId,
      })
        .then(res => {
          console.log(res);
          return wxPay(res);
        })
        .then(res2 => {
          console.log(res2);
          // 前端处理红包口袋余额增加
          const tmpMoney =
            parseFloat(this.data.remainMoney) + parseFloat(choosedMoney);
          this.setData({
            remainMoney: tmpMoney,
          });
          showWxToast('充值成功!');
          requestLock = false;
          app.globalData.isH5NeedRefresh = true;
          return sendGiftBroadCast({
            giftId: 'hbkd',
            content: choosedMoney,
          });
          timeoutTask(() => {
            wx.navigateBack();
          }, 500);
        })
        .catch(err => {
          console.log(err);
          showWxToast('充值失败!');
          requestLock = false;
        });
    }
  },
  getHbkdList: function() {
    getHbkdList()
      .then(res => {
        console.log('***getHbkdList***');
        console.log(res);
        const tmpList = res.data.list;
        const tmpLen = tmpList.length;
        for (let i = 0; i < tmpLen; i += 1) {
          tmpList[i].num = i + 1 < 10 ? '0' + (i + 1) : i + 1;
          tmpList[i].wx_name =
            tmpList[i].wx_name.length <= 6
              ? tmpList[i].wx_name
              : tmpList[i].wx_name.substr(0, 6) + '...';
        }
        this.setData({
          hbkdList: tmpList,
          prizeSize: tmpLen,
          remainMoney: res.data.money,
        });
      })
      .catch(err => {
        console.log(err);
      });
  },
  toAgreement: function() {
    wx.navigateTo({
      url: '/pages/agreement/agreement',
    });
  },
});
```

## File: pages/hbkdRecharge/hbkdRecharge.json
```json
{
  "navigationBarTitleText": "红包口袋",
  "usingComponents": {
    "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
  }
}
```

## File: pages/hbkdRecharge/hbkdRecharge.wxml
```
<view class="hbkdRechargeContainer">
    <image src="https://static.hudongmiao.com/joymewMp/hbkdRecharge/bg2-01.png" class="bg" mode="widthFix"></image>
    <view class="remainArea {{hbkdRemainVisible ? '' : 'spec'}}">
        <view class="hbkdTitle">红包口袋</view>
        <view class="remainMoney" wx:if="{{hbkdRemainVisible}}">{{remainMoney}}元</view>
        <view class="tip">
            <view>口袋内金额将用于红包雨等全场互动</view>
        </view>
    </view>
    <view class="rechargeArea">
        <view class="rechargeListWrap">
            <view class="rechargeItem" style="background-image:url('{{item.bg}}')" wx:for="{{hbkdRechargeList}}" wx:key="index" bindtap="handleTap" data-money="{{item.price}}" data-custom="{{item.isCustom}}">
                <view class="price" wx:if="{{!item.isCustom}}">{{item.price}}元</view>
                <view class="price" wx:if="{{item.isCustom && !inputVisible}}">{{item.price}}</view>
                <input type="number" maxlength="4" value="{{moneyInput}}" bindinput="handleMoneyInput" bindblur="handleMoneyBlur" wx:if="{{item.isCustom && inputVisible}}" focus="{{isFocus}}" />
                <view class="unit" wx:if="{{item.isCustom && inputVisible}}">元</view>
                <view class="tip" wx:if="{{item.isCustom && !inputVisible}}">{{item.txt}}</view>
            </view>
        </view>
    </view>
    <view class="agreement" bindtap='toAgreement'>阅读并同意《充值服务协议》</view>
    <view class="rewardSheetTitle">
        <image src="https://static.hudongmiao.com/joymewMp/recharge/loveIcon.png" class="loveIcon"></image>
        <view class="title">{{prizeSize}}次赞赏</view>
        <image src="https://static.hudongmiao.com/joymewMp/recharge/loveIcon.png" class="loveIcon"></image>
    </view>
    <view class="rewardSheetList">
        <view class="item" wx:for="{{hbkdList}}" wx:key="index">
            <view class="leftCt">
                <image src="https://static.hudongmiao.com/joymewMp/recharge/firstMedal.png" class="medalImg" wx:if="{{index === 0}}"></image>
                <image src="https://static.hudongmiao.com/joymewMp/recharge/secondMedal.png" class="medalImg" wx:if="{{index === 1}}"></image>
                <image src="https://static.hudongmiao.com/joymewMp/recharge/thirdMedal.png" class="medalImg" wx:if="{{index === 2}}"></image>
                <view class="num" wx:if="{{index > 2}}">{{item.num}}</view>
                <image src="{{item.avator}}" class="headImg"></image>
                <view class="name">{{item.wx_name}}</view>
            </view>
            <view class="wish">累计打赏{{item.allGold}}元</view>
        </view>
    </view>
    <!-- 反馈入口 -->
    <feedbackEntry userId="{{userId}}"></feedbackEntry>
</view>
```

## File: pages/hbkdRecharge/hbkdRecharge.wxss
```
.hbkdRechargeContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.hbkdRechargeContainer>.bg {
    position: absolute;
    width: 100%;
}

.hbkdRechargeContainer>.remainArea {
    width: 100%;
    height: 435rpx;
    background-image: url('https://static.hudongmiao.com/joymewMp/hbkdRecharge/rainbow-01.png');
    background-size: 100% 100%;
    position: absolute;
    top: 83rpx;
    color: #FFFFFF;
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 1;
}

.hbkdRechargeContainer>.remainArea>.hbkdTitle {
    font-size: 34rpx;
    font-weight: 400;
    margin-top: 73rpx;
}

.hbkdRechargeContainer>.remainArea>.remainMoney {
    font-size: 66rpx;
    font-weight: bold;
}

.hbkdRechargeContainer>.remainArea>.tip {
    font-size: 20rpx;
    font-weight: 400;
    margin-top: 5rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.hbkdRechargeContainer>.remainArea.spec>.hbkdTitle {
    font-size: 62rpx;
    margin-top: 96rpx;
}
.hbkdRechargeContainer>.remainArea.spec>.tip {
    font-size: 32rpx;
    margin-top: 27rpx;
}
.hbkdRechargeContainer>.rechargeArea {
    width: 660rpx;
    height: 746rpx;
    background: #FFFFFF;
    border-radius: 72rpx;
    position: absolute;
    top: 288rpx;
}

.hbkdRechargeContainer>.rechargeArea>.rechargeListWrap {
    width: 100%;
    position: absolute;
    top: 191rpx;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.hbkdRechargeContainer>.rechargeArea>.rechargeListWrap>.rechargeItem {
    width: 191rpx;
    height: 124rpx;
    background-size: 100% 100%;
    color: #FFFFFF;
    font-weight: 400;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 23rpx 0;
    position: relative;
}
.hbkdRechargeContainer>.rechargeArea>.rechargeListWrap>.rechargeItem>input {
    width: 95rpx;
    height: 80rpx;
    color: #FFFFFF;
    font-size: 34rpx;
    margin-right: 25rpx;
}
.hbkdRechargeContainer>.rechargeArea>.rechargeListWrap>.rechargeItem>.price {
    font-size: 34rpx;
    text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2);
}

.hbkdRechargeContainer>.rechargeArea>.rechargeListWrap>.rechargeItem>.tip {
    font-size: 19rpx;
}
.hbkdRechargeContainer>.rechargeArea>.rechargeListWrap>.rechargeItem>.unit {
    font-size: 32rpx;
    position: absolute;
    color: #FFFFFF;
    right: 23rpx;
}
.hbkdRechargeContainer>.rewardSheetTitle {
    display: flex;
    align-items: center;
    position: absolute;
    top: 1288rpx;
    font-size: 36rpx;
    font-weight: 500;
    color: #FFFFFF;
    top: 1137rpx;
}

.hbkdRechargeContainer>.rewardSheetTitle>.loveIcon {
    width: 30rpx;
    height: 26rpx;
    margin: 0 30rpx;
}

.hbkdRechargeContainer>.rewardSheetList {
    position: absolute;
    top: 1223rpx;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #8A1DD3;
}

.hbkdRechargeContainer>.rewardSheetList>.item {
    width: 695rpx;
    height: 114rpx;
    background: rgba(84, 59, 144, 0.3);
    border-radius: 8rpx;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 35rpx 0 28rpx;
}

.hbkdRechargeContainer>.rewardSheetList>.item>.leftCt {
    display: flex;
    align-items: center;
}

.hbkdRechargeContainer>.rewardSheetList>.item>.leftCt>.medalImg {
    width: 39rpx;
    height: 50rpx;
}

.hbkdRechargeContainer>.rewardSheetList>.item>.leftCt>.headImg {
    width: 64rpx;
    height: 64rpx;
    border-radius: 50%;
    margin: 0 22rpx 0 17rpx;
}

.hbkdRechargeContainer>.rewardSheetList>.item>.leftCt>.name {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFFFFF;
}

.hbkdRechargeContainer>.rewardSheetList>.item>.wish {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFF32E;
}
.hbkdRechargeContainer>.agreement {
    font-size: 24rpx;
    font-weight: 400;
    color: #FFD027;
    position: absolute;
    top: 1069rpx;
}
```

## File: pages/hbWall/hbWall.js
```javascript
import {
  timeoutTask,
  getRandom,
  showWxToast,
  showWxLoading,
  hideWxLoading,
} from '../../utils/index';
import {
  getGameState,
  sendBroadCast,
  getHbList,
  buyHb,
  hbqRecharge,
  getHbRankList,
} from '../../api/kbx/kbx';
import { wxPay } from '../../api/pay';
import defaultContent from '../../assets/constant/default';

const app = getApp();

// 礼物数组
const giftList = [
  {
    id: 1,
    gift: 'rocket1',
    name: '小号火箭',
    imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket1.png',
  },
  {
    id: 2,
    gift: 'rocket2',
    name: '中号火箭',
    imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket2.png',
  },
  {
    id: 3,
    gift: 'rocket3',
    name: '大号火箭',
    imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket3.png',
  },
];
const wishList = ['醉酒饱德，不胜感激', '美酒佳肴,不甚荣幸', '感谢招待,祝愿安康', '小小红包,感谢招待'];
let requestLock = false;
// 限制只有一个轮询存在
let tmpInterval = null; // 刚进入红包墙的轮询
let tmpInterval2 = null; // 点击开始红包墙中的轮询
let baseMoney = 0;
Page({
  data: {
    gameStatus: 1, // 红包墙状态(控制页面显示)
    myHbsVisible: false,
    isLuckyShow: false,
    luckyAni: '',
    hbs: [],
    chooseHbIds: [],
    remain: 3,
    activeGiftIndex: -1,
    gift_show: {
      //当前显示的礼物
      id: 3,
      gift: 'rocket3',
      name: '大号火箭',
      imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket3.png',
      price: 0,
    },
    userId: '',
    openId: '',
    name: '',
    headImg: '',
    isForbidBuyHbq: false,
    luckyHbs: [],
    sort: '',
    rankList1: [],
    rankList2: [],
    defaultHeadImg: defaultContent.defaultHeadImg,
  },
  onLoad: function(options) {
    requestLock = false;
    tmpInterval = null;
    tmpInterval2 = null;
    baseMoney = 0;
    this.setData({
      userId: options.userId,
      openId: options.openId,
      name: options.name,
      headImg: options.headImg,
      isForbidBuyHbq: options.isForbidBuyHbq === 'true' ? true : false,
    });
  },
  onShow: function() {
    getGameState(this.data.userId).then(res => {
      console.log(res);
      if (res.success) {
        if (res.data.status === '1') {
          if (this.data.hbs.length === 0) {
            this.getHbs();
          }
          clearInterval(tmpInterval2);
          tmpInterval2 = null;
          if (!tmpInterval) {
            // 轮询更新红包列表
            tmpInterval = setInterval(() => {
              this.updateHbs(true);
            }, 4000);
          }
        } else if (res.data.status === '2') {
          showWxToast('本轮红包墙已经结束');
          timeoutTask(() => {
            wx.navigateBack();
          }, 1500);
        }
      }
    });
  },
  onHide: function() {
    //清除定时器
    clearInterval(tmpInterval);
    clearInterval(tmpInterval2);
    tmpInterval = null;
    tmpInterval2 = null;
  },
  onUnload: function() {
    //清除定时器
    clearInterval(tmpInterval);
    clearInterval(tmpInterval2);
    tmpInterval = null;
    tmpInterval2 = null;
  },
  enterGame: function() {
    getGameState(this.data.userId)
      .then(res => {
        console.log('***获取红包墙状态***');
        console.log(res);
        if (res.success) {
          if (res.data.status === '0') {
            showWxToast('请等待大屏开启红包墙');
          } else if (res.data.status === '1') {
            // 红包墙进行中
            console.log('***获取红包列表***');
            this.getHbs();
            clearInterval(tmpInterval);
            tmpInterval = null;
            if (!tmpInterval2) {
              // 轮询更新红包列表
              tmpInterval2 = setInterval(() => {
                this.updateHbs(true);
              }, 4000);
            }
          } else if (res.data.status === '2') {
            showWxToast('本轮开红包已经结束');
            timeoutTask(() => {
              wx.navigateBack();
            }, 1500);
          } else {
            showWxToast('请等待大屏开启红包墙');
          }
        }
      })
      .catch(err => {
        console.log(err);
      });
  },
  chooseHbs: function(e) {
    const index = this.findHbIndexByHbId(e.currentTarget.dataset.id);
    const hbs = this.data.hbs;
    if (hbs[index].isOpen) {
      showWxToast('这个红包已经被拆开啦！');
      return;
    }
    if (hbs[index].isBuyed) {
      showWxToast('这个红包已经被抢走啦！');
      return;
    }
    if (hbs[index].canBuy) {
      // 如果选中 取消选中
      if (hbs[index].isChoosed) {
        hbs[index].isChoosed = false;
        this.setData({
          hbs,
        });
        this.updateGift();
        return;
      }
      // 最多3个红包 包括已经购买的
      const hasChoosedNum = this.getChoosedHbsNum(true);
      if (hasChoosedNum >= 3) {
        showWxToast('最多只能选择三个红包哦');
        return;
      }
      if (!hbs[index].isChoosed) {
        hbs[index].isChoosed = true;
        this.setData({
          hbs,
        });
        this.updateGift();
      }
    }
  },
  // 获取红包列表
  getHbs: function() {
    getHbList(false).then(res => {
      if (res.success) {
        console.log('***红包列表***');
        console.log(res);
        const tmpLen = res.data.list.length;
        const tmpHbs = [];
        let tmpNum = -1;
        let tmpState;
        let tmpIsOpen;
        let tmpIsBuyed;
        let tmpCanBuy;
        let tmpUserId;
        let tmpName;
        let tmpHeadImg;
        for (let i = 0; i < tmpLen; i += 1) {
          if (i < 3) {
            // +1
            tmpNum = i + 1;
          } else if (i < 12) {
            // +2
            tmpNum = i + 2;
          } else if (i < 21) {
            // +3
            tmpNum = i + 3;
          } else {
            // +4
            tmpNum = i + 4;
          }
          tmpIsOpen = false;
          tmpIsBuyed = false;
          tmpCanBuy = false;
          tmpState = res.data.list[i].userId;
          tmpUserId = '';
          tmpName = '';
          tmpHeadImg = '';
          if (tmpState === '0') {
            if (res.data.list[i].userInfo) {
              // 未打开已购买
              tmpIsBuyed = true;
              tmpUserId = res.data.list[i].userInfo.USER_ID;
              tmpName = res.data.list[i].userInfo.wx_name;
              tmpHeadImg = res.data.list[i].userInfo.avator;
            } else {
              // 未打开未购买
              tmpCanBuy = true;
            }
          } else if (tmpState === '100') {
            // 红包已经在大屏被拆开
            tmpIsOpen = true;
            // 且被人购买
            if (res.data.list[i].userInfo) {
              tmpIsBuyed = true;
              tmpUserId = res.data.list[i].userInfo.USER_ID;
              tmpName = res.data.list[i].userInfo.wx_name;
              tmpHeadImg = res.data.list[i].userInfo.avator;
            }
          } else {
            // 红包已经被别人购买
            tmpIsBuyed = true;
            tmpUserId = res.data.list[i].userInfo.USER_ID;
            tmpName = res.data.list[i].userInfo.wx_name;
            tmpHeadImg = res.data.list[i].userInfo.avator;
          }
          tmpHbs.push({
            id: res.data.list[i].eggId,
            gold: res.data.list[i].money,
            isOpen: tmpIsOpen,
            isBuyed: tmpIsBuyed,
            canBuy: tmpCanBuy,
            isChoosed: false,
            userId: tmpUserId,
            name: tmpName,
            headImg: tmpHeadImg,
            num: tmpNum,
          });
        }
        baseMoney = parseFloat(res.data.hbqMoney);
        this.setData({
          hbs: tmpHbs,
          gameStatus: 2,
          sort: res.data.sort,
        });
        this.updateGift();
      } else {
        showWxToast('获取红包信息失败');
      }
    });
  },
  // 更新红包列表
  updateHbs: function(cancelLoading) {
    return new Promise((resolve, reject) => {
      getHbList(cancelLoading).then(res => {
        if (res.success && res.data) {
          console.log('***红包列表***');
          console.log(res);
          if (res.data.finished === '1') {
            console.log('***结束递归***');
            clearInterval(tmpInterval2);
            clearInterval(tmpInterval);
            tmpInterval2 = null;
            tmpInterval = null;
            this.handleGameEnd();
            resolve();
            return;
          }
          const tmpLen = res.data.list.length;
          const tmpHbs = this.data.hbs;
          let tmpNum = -1;
          let tmpState;
          let tmpIsOpen;
          let tmpIsBuyed;
          let tmpCanBuy;
          let tmpUserId;
          let tmpName;
          let tmpHeadImg;
          for (let i = 0; i < tmpLen; i += 1) {
            if (i < 3) {
              // +1
              tmpNum = i + 1;
            } else if (i < 12) {
              // +2
              tmpNum = i + 2;
            } else if (i < 21) {
              // +3
              tmpNum = i + 3;
            } else {
              // +4
              tmpNum = i + 4;
            }
            tmpIsOpen = false;
            tmpIsBuyed = false;
            tmpCanBuy = false;
            tmpState = res.data.list[i].userId;
            tmpUserId = '';
            tmpName = '';
            tmpHeadImg = '';
            if (tmpState === '0') {
              if (res.data.list[i].userInfo) {
                // 未打开已购买
                tmpIsBuyed = true;
                tmpUserId = res.data.list[i].userInfo.USER_ID;
                tmpName = res.data.list[i].userInfo.wx_name;
                tmpHeadImg = res.data.list[i].userInfo.avator;
              } else {
                // 未打开未购买
                tmpCanBuy = true;
              }
            } else if (tmpState === '100') {
              tmpIsOpen = true;
              if (res.data.list[i].userInfo) {
                // 打开已购买
                tmpIsBuyed = true;
                tmpUserId = res.data.list[i].userInfo.USER_ID;
                tmpName = res.data.list[i].userInfo.wx_name;
                tmpHeadImg = res.data.list[i].userInfo.avator;
              } else {
                // 打开未购买
                // 空操作
              }
            }
            if (tmpHbs[i]) {
              tmpHbs[i].isOpen = tmpIsOpen;
              tmpHbs[i].isBuyed = tmpIsBuyed;
              tmpHbs[i].canBuy = tmpCanBuy;
              if (!tmpCanBuy && tmpHbs[i].isChoosed) {
                // 选中的红包已经不可以购买了
                tmpHbs[i].isChoosed = false;
                this.updateGift();
              }
              tmpHbs[i].userId = tmpUserId;
              tmpHbs[i].name = tmpName;
              tmpHbs[i].headImg = tmpHeadImg;
            }
          }
          this.setData({
            hbs: tmpHbs,
            sort: res.data.sort,
          });
          console.log(this.data.hbs);
          resolve();
        } else {
          reject();
        }
      });
    });
  },
  // 结束红包墙获取排行榜
  handleGameEnd: function() {
    getHbRankList()
      .then(res2 => {
        console.log('***排行榜****', res2);
        let tmpResultList = res2.data.list;
        let rankList1 = tmpResultList.slice(0, 3);
        let rankList2 = tmpResultList.slice(3, 10);
        // 红包墙已经结束
        this.setData({
          gameStatus: 3,
          rankList1,
          rankList2,
        });
      })
      .catch(err => {
        console.log(err);
      });
  },
  // 获取选择的红包数目时更新祝福列表
  updateGift: function() {
    const hasChoosedNum = this.getChoosedHbsNum(false);
    this.hbsMapGift(hasChoosedNum);
  },
  // 获取已经选择的红包id数组
  getChoosedHbIds: function() {
    const hbs = this.data.hbs;
    const len = hbs.length;
    const tmpChoosedHbIds = [];
    for (let i = 0; i < len; i += 1) {
      if (hbs[i].isChoosed) {
        tmpChoosedHbIds.push(hbs[i].id);
      }
    }
    return tmpChoosedHbIds;
  },
  // 获取选好的红包数目
  getChoosedHbsNum: function(isIncludeBuyed) {
    let tmpHbList = this.data.hbs;
    let tmpLen = tmpHbList.length;
    let tmpCount = 0;
    if (isIncludeBuyed) {
      for (let i = 0; i < tmpLen; i += 1) {
        if (
          tmpHbList[i].isChoosed ||
          tmpHbList[i].userId === this.data.userId
        ) {
          tmpCount += 1;
        }
      }
    } else {
      for (let i = 0; i < tmpLen; i += 1) {
        if (tmpHbList[i].isChoosed) {
          tmpCount += 1;
        }
      }
    }
    return tmpCount;
  },
  // 打开我的红包页面
  toMyHbs: function() {
    this.setData({
      myHbsVisible: true,
    });
  },
  // 打开红包购买页面
  toBuyHbs: function() {
    this.setData({
      myHbsVisible: false,
    });
  },
  // 红包选择个数映射礼物
  hbsMapGift: function(choosedNum) {
    const tmpMoney = baseMoney;
    giftList[0].price = tmpMoney.toFixed(2);
    giftList[1].price = (tmpMoney * 2).toFixed(2);
    giftList[2].price = (tmpMoney * 3).toFixed(2);
    if (choosedNum == 3) {
      //选了3个红包<--->大火箭
      this.setData({
        gift_show: giftList[2],
      });
    } else if (choosedNum == 2) {
      //选了2个红包<--->中火箭
      this.setData({
        gift_show: giftList[1],
      });
    } else {
      //选了1个红包或者还没有选红包<--->小火箭
      this.setData({
        gift_show: giftList[0],
      });
    }
  },
  // 通过hbId查找红包所在数组的索引
  findHbIndexByHbId: function(hbId) {
    let tmpIndex = -1;
    const tmpLen = this.data.hbs.length;
    for (let i = 0; i < tmpLen; i += 1) {
      if (this.data.hbs[i].id === hbId) {
        tmpIndex = i;
        break;
      }
    }
    return tmpIndex;
  },
  showLucky() {
    this.setData({
      luckyAni: 'showLuckyAni',
      isLuckyShow: true,
    });
    // 4s后消失
    timeoutTask(() => {
      this.setData({
        luckyAni: 'hideLuckyAni',
      });
      timeoutTask(() => {
        this.setData({
          isLuckyShow: false,
        });
      }, 100);
    }, 4000);
  },
  // 买红包
  buy: function() {
    if (this.data.isForbidBuyHbq) {
      showWxToast('您没有权限买红包!');
      return;
    }
    let choosed;
    this.updateHbs(false)
      .then(() => {
        // 获取选中的红包
        choosed = this.getChoosedHbIds();
        console.log('***choosed***');
        console.log(choosed);
        if (choosed.length == 0) {
          showWxToast('请先选一个红包');
          return;
        }
        if (requestLock) {
          return;
        }
        requestLock = true;
        const chooseIdsStr = choosed.join(',');
        return this.robHb(chooseIdsStr, this.data.sort);
      })
      .then(res => {
        console.log(res);
        if (!res) {
          return;
        }
        if (res.code === '200') {
          // 喵钻足正常抢红包
          if (res.resultList.length == 0) {
            // 一个红包都没抢到
            wx.showModal({
              showCancel: false,
              title: '温馨提示',
              content: '很遗憾您选择的红包都被抢走了\r\n已退回至您的账户中',
              confirmText: '确定',
              success: () => {
                this.updateHbs(false);
              },
            });
          } else {
            // 至少抢到了一个
            if (choosed.length > res.resultList.length) {
              wx.showModal({
                showCancel: false,
                title: '温馨提示',
                content:
                  '恭喜您,成功抢到了' +
                  res.resultList.length +
                  '个红包！ \r\n 未抢到的红包，已退回至您的账户中',
                confirmText: '确定',
                success: () => {
                  this.updateHbs(false);
                },
              });
            } else {
              wx.showModal({
                showCancel: false,
                title: '温馨提示',
                content: '恭喜您,成功抢到了' + res.resultList.length + '个红包!',
                confirmText: '确定',
                success: () => {
                  this.updateHbs(false);
                },
              });
            }
            console.log(res.resultList);
            let tmpCode = '';
            if (this.data.gift_show.id === 3) {
              tmpCode = 7002;
            } else if (this.data.gift_show.id === 2) {
              tmpCode = 6002;
            } else if (this.data.gift_show.id === 1) {
              tmpCode = 5002;
            }
            let c = JSON.stringify({
              code: tmpCode,
              param: {
                headImg: this.data.headImg,
                nickname: this.data.name,
                wish: wishList[getRandom(0, 4)],
              },
            });
            // 发送广播
            sendBroadCast({
              c,
            });
            app.globalData.isH5NeedRefresh = true;
          }
          requestLock = false;
        } else if (res.code === '304') {
          // 喵钻不足
          if (res.NeedMoney) {
            // 调起支付
            return this.recharge(res.NeedMoney);
          } else {
            showWxToast('购买失败');
          }
        } else if (res.code === '303') {
          // 用户信息异常
          showWxToast('用户信息异常');
          requestLock = false;
        } else if (res.code === '302') {
          // 一个人最多抢到3个红包
          showWxToast('一个人最多抢到3个红包');
          requestLock = false;
        } else if (res.code === '301') {
          // 不是最新的轮次
          showWxToast('不是最新的轮次');
          requestLock = false;
        } else {
          showWxToast('购买失败');
          requestLock = false;
        }
      })
      .catch(err => {
        console.log(err);
        requestLock = false;
      });
  },
  // 抢红包
  robHb: function(pHbIdStr, pSort) {
    return new Promise((resolve, reject) => {
      showWxLoading('奋力争抢中...');
      buyHb({
        hbIds: pHbIdStr,
        sort: pSort,
      })
        .then(res => {
          console.log(res);
          hideWxLoading();
          resolve(res);
        })
        .catch(err => {
          console.log(err);
          reject(err);
          hideWxLoading();
          showWxToast('抢购失败');
        });
    });
  },
  // 支付
  recharge: function(money) {
    return new Promise((resolve, reject) => {
      hbqRecharge({
        userId: this.data.userId,
        openid: this.data.openId,
        money,
      })
        .then(res => {
          console.log(res);
          if (res.status === 'success') {
            wxPay(res)
              .then(res2 => {
                console.log(res2);
                showWxToast('充值成功');
                resolve(res2);
                requestLock = false;
                app.globalData.isH5NeedRefresh = true;
                // 充值完成 等待后台加嗨币逻辑完成后 去买红包
                timeoutTask(() => {
                  this.buy();
                }, 500);
              })
              .catch(err => {
                console.log(err);
                showWxToast('充值失败');
                requestLock = false;
                reject(err);
              });
          }
        })
        .catch(err => {
          console.log(err);
          reject(err);
        });
    });
  },
  toAgreement: function() {
    wx.navigateTo({
      url: '/pages/agreement/agreement',
    });
  },
});
```

## File: pages/hbWall/hbWall.json
```json
{
    "navigationBarTitleText": "红包墙",
    "usingComponents": {
      "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
    },
    "disableScroll":true
  }
```

## File: pages/hbWall/hbWall.wxml
```
<view class="hbWallContainer">
    <view class="bgArea">
        <image src="https://static.hudongmiao.com/joymewMp/hbWall/waitBg.png" class="waitBg" mode="widthFix" wx:if="{{gameStatus === 1}}"></image>
        <image src="https://static.hudongmiao.com/joymewMp/zyz/zyzBg2.png" class="bg" mode="widthFix" wx:if="{{gameStatus === 2}}"></image>
        <image src="https://static.joymew.com/joymewMp/hbWall/rankBg.png" class="bg" mode="widthFix" wx:if="{{gameStatus === 3}}"></image>
        <image src="https://static.joymew.com/joymewMp/hbWall/shine.png" class="shine" mode="widthFix" wx:if="{{gameStatus === 3}}"></image>
        <view class="shade" wx:if="{{gameStatus === 2}}"></view>
    </view>
    <!-- 等待界面 -->
    <view class="waitContainer" wx:if="{{gameStatus === 1}}">
        <view class="ruleBox">
            <view class="title">
                <image src="https://static.hudongmiao.com/joymewMp/hbWall/cs.png" class="csImg" mode="widthFix"></image>
                <view class="text">活动规则</view>
            </view>
            <view class="ruleContent">
                <view class="para">1、只需送出弹幕礼物，免费获得一次夺取宝箱的机会；</view>
                <view class="para">2、送出小火箭：获取一个红包;送出中火箭：获取二个红包;送出大火箭：获取三个红包。</view>
                <view class="para">3、如果红包被抢完，您支付得金额将原路退回您得账户</view>
            </view>
        </view>
        <view class="startBtn" bindtap="enterGame"></view>
    </view>
    <!-- 红包墙界面 -->
    <view class="gameContainer" wx:if="{{gameStatus === 2}}">
        <view class="wall">
            <view class="hbListWrap">
                <view class="hbItem {{item.isChoosed?'choosed':''}} {{item.isOpen?'reverse':''}}" wx:for="{{hbs}}" data-id="{{item.id}}" wx:key="index" bindtap="chooseHbs">
                    <view class="FM">
                        <view class="num">{{ item.num}}</view>
                        <image src="{{item.headImg}}" class="headImg" wx-if="{{item.isBuyed}}"></image>
                    </view>
                    <view class="ZM">
                        <view class="headImgBox">
                            <image src="{{item.headImg}}" class="headImg" wx-if="{{item.isBuyed}}"></image>
                            <image src="{{defaultHeadImg}}" class="headImg" wx-if="{{!item.isBuyed}}"></image>
                        </view>
                        <view class="name" wx-if="{{item.isBuyed}}">{{item.name}}</view>
                        <view class="name" wx-if="{{!item.isBuyed}}">虚位以待</view>
                        <view class="money">￥{{item.gold}}</view>
                    </view>
                </view>
            </view>
        </view>
        <view class="agreement" bindtap='toAgreement'>阅读并同意《充值服务协议》</view>
        <!-- <view class="csTip">
            <image src="https://static.hudongmiao.com/joymewMp/hbWall/cs.png" class="csImg" mode="widthFix"></image>
            <view class="text">送出小火箭:获取一个红包;送出中火箭:获取二个红包;送出大火箭:获取三个红包。</view>
        </view> -->
        <!-- 中奖结果 -->
        <view class="luckyWrap {{luckyAni}}" wx:if="{{isLuckyShow}}">
            <view class="tit">中奖啦</view>
            <view class="congragulations">
                恭喜你! 获得
                <text>{{luckyMoney}}</text>
                元红包!
            </view>
            <view class="wechatTip">微信已实时到账</view>
            <view class="money">{{luckyMoney}}元</view>
        </view>
        <view class="giftListWrap">
            <view class="giftItem">
                <view class="fudai"></view>
                <image src="{{gift_show.imgUrl}}" class="giftImg g{{gift_show.id}}"></image>
            </view>
            <view class="money">￥{{gift_show.price}}</view>
        </view>
        <view class="startBtn">
            <view class="text" bindtap='buy'>获取红包</view>
        </view>
    </view>
    <!-- 排行榜界面 -->
    <view class="rankContainer" wx:if="{{gameStatus === 3}}">
        <view class="rankTitle">福运榜</view>
        <view class="first" wx:if="{{rankList1[0]}}">
            <view class="num">第一名</view>
            <view class="headImgBox">
                <image src="{{rankList1[0].avator}}" class="headImg"></image>
                <view class="leftDesc"></view>
                <view class="rightDesc"></view>
            </view>
            <view class="name">
                <view class="text">{{rankList1[0].wx_name}}</view>
            </view>
            <view class="money">{{rankList1[0].totalGold}}元</view>
        </view>
        <view class="topThree">
            <view class="ttItem" wx:if="{{rankList1[0]}}">
                <image src="https://static.joymew.com/joymewMp/hbWall/gold.png" class="goldImg"></image>
                <view class="headImgBox">
                    <image src="{{rankList1[0].avator}}" class="headImg"></image>
                </view>
                <view class="name">{{rankList1[0].wx_name}}</view>
                <view class="money">{{rankList1[0].totalGold}}元</view>
            </view>
            <view class="ttItem" wx:if="{{rankList1[1]}}">
                <image src="https://static.joymew.com/joymewMp/hbWall/silver.png" class="silverImg"></image>
                <view class="headImgBox">
                    <image src="{{rankList1[1].avator}}" class="headImg"></image>
                </view>
                <view class="name">{{rankList1[1].wx_name}}</view>
                <view class="money">{{rankList1[1].totalGold}}元</view>
            </view>
            <view class="ttItem" wx:if="{{rankList1[2]}}">
                <image src="https://static.joymew.com/joymewMp/hbWall/cron.png" class="cronImg"></image>
                <view class="headImgBox">
                    <image src="{{rankList1[2].avator}}" class="headImg"></image>
                </view>
                <view class="name">{{rankList1[2].wx_name}}</view>
                <view class="money">{{rankList1[2].totalGold}}元</view>
            </view>
        </view>
        <view class="otherLuckyList">
            <view class="item" wx:for="{{rankList2}}" wx:key="index">
                <view class="headImgBox">
                    <image src="{{item.avator}}" class="headImg"></image>
                    <view class="num">{{ index + 4}}</view>
                </view>
                <view class="name">
                    <view class="text">{{item.wx_name}}</view>
                </view>
                <view class="money">{{item.totalGold}}元</view>
            </view>
        </view>
    </view>
</view>
```

## File: pages/hbWall/hbWall.wxss
```
.hbWallContainer {
    position: relative;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
}

/* 公共背景区域 */
.hbWallContainer>.bgArea {
    position: absolute;
    width: 100%;
    height: 100%;
}

.hbWallContainer>.bgArea>.waitBg {
    position: absolute;
    width: 100%;
}

.hbWallContainer>.bgArea>.bg {
    position: absolute;
    width: 105%;
    height: 100%;
    position: absolute;
    left: -2%;
}

.hbWallContainer>.bgArea>.shade {
    width: 100vw;
    height: 100vh;
    opacity: 0.6;
    background-color: #000000;
    position: absolute;
    top: 0;
    left: 0;
}

.hbWallContainer>.bgArea>.shine {
    width: 595rpx;
    height: 691rpx;
    position: absolute;
    left: 78rpx;
    z-index: 1;
}

/* 等待界面 */
.hbWallContainer>.waitContainer {
    position: absolute;
    width: 100%;
    height: 100%;
}

.waitContainer>.ruleBox {
    width: 389rpx;
    height: 689rpx;
    position: absolute;
    top: 307rpx;
    left: 320rpx;
}

.waitContainer>.ruleBox>.title {
    width: 258rpx;
    height: 64rpx;
    background: #C41321;
    border-radius: 32rpx;
    position: absolute;
    left: 20rpx;
    top: -36rpx;
    display: flex;
    align-items: center;
    padding-left: 98rpx;
}

.waitContainer>.ruleBox>.title>.text {
    font-size: 30rpx;
    font-weight: normal;
    color: #7A0A0E;
    text-shadow: 0px 5rpx 5rpx rgba(132, 0, 15, 0.75);
    background: linear-gradient(0deg, #EFD178 0%, #FBF9B8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.waitContainer>.ruleBox>.title>.csImg {
    width: 123rpx;
    height: 103rpx;
    position: absolute;
    left: -27rpx;
    top: -39rpx;
}

.waitContainer>.ruleBox>.ruleContent {
    position: absolute;
    width: 100%;
    top: 65rpx;
}

.waitContainer>.ruleBox>.ruleContent>.para {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFFFDA;
    width: 100%;
    margin: 20rpx 0;
    line-height: 44rpx;
}

.waitContainer>.startBtn {
    width: 390rpx;
    height: 114rpx;
    background-image: url('https://static.joymew.com/joymewMp/zyz/startBtn.png');
    background-size: 100% 100%;
    position: absolute;
    bottom: 0rpx;
    left: 322rpx;
}

/* 红包墙界面 */
.hbWallContainer>.gameContainer {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.gameContainer>.wall {
    position: absolute;
    width: 100%;
    height: 785rpx;
    top: 0rpx;
    background-image: url('https://static.joymew.com/joymewMp/hbWall/wall.png');
    background-size: 100% 100%;
    display: flex;
    justify-content: center;
}

.gameContainer>.wall>.hbListWrap {
    width: 660rpx;
    height: 650rpx;
    position: absolute;
    top: 100rpx;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.hbListWrap>.hbItem {
    position: relative;
    width: 90rpx;
    height: 131rpx;
    cursor: pointer;
}

.hbListWrap>.hbItem>.FM,
.hbListWrap>.hbItem>.ZM {
    position: absolute;
    width: 100%;
    height: 100%;
    transition: transform 0.8s ease-in-out;
    backface-visibility: hidden;
}

.hbListWrap>.hbItem>.FM {
    transform: rotateY(0deg);
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url('https://static.hudongmiao.com/joymewMp/hbWall/hbF.png');
    background-size: 100% 100%;
}

.hbListWrap>.hbItem>.FM>.headImg {
    left: 0;
    width: 58rpx;
    height: 58rpx;
    border-radius: 50%;
    position: absolute;
    top: 25rpx;
}

.hbListWrap>.hbItem>.FM>.num {
    font-size: 28rpx;
    font-weight: bold;
    color: #EDD890;
    position: absolute;
    right: 12rpx;
    top: 6rpx;
}

.hbListWrap>.hbItem>.ZM {
    transform: rotateY(-180deg);
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url('https://static.hudongmiao.com/joymewMp/hbWall/hbZ.png');
    background-size: 100% 100%;
}

.hbListWrap>.hbItem.reverse>.FM {
    transform: rotateY(180deg);
}

.hbListWrap>.hbItem.reverse>.ZM {
    transform: rotateY(0deg);
}

.hbListWrap>.hbItem.reverse>.ZM>.headImgBox {
    width: 61rpx;
    height: 61rpx;
    background: #650C15;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.hbListWrap>.hbItem.reverse>.ZM>.headImgBox>.headImg {
    width: 58rpx;
    height: 58rpx;
    border-radius: 50%;
}

.hbListWrap>.hbItem.reverse>.ZM>.name {
    font-size: 18rpx;
    font-weight: bold;
    color: #870F18;
    margin-top: 5rpx;
}

.hbListWrap>.hbItem.reverse>.ZM>.money {
    font-size: 18rpx;
    font-weight: bold;
    color: #870F18;
    margin-top: 5rpx;
}

.hbListWrap>.hbItem.choosed {
    transform: translateY(-40rpx) scale(1.1);
    z-index: 1;
}

.gameContainer>.agreement {
    font-size: 24rpx;
    font-weight: 400;
    color: #ffffff;
    position: absolute;
    bottom: 150rpx;
}

.gameContainer>.csTip {
    position: absolute;
    top: 824rpx;
    width: 584rpx;
    height: 78rpx;
    background: rgba(255, 238, 202, 0);
    border: 2rpx solid #D16239;
    border-radius: 10rpx;
    display: flex;
    align-items: center;
}

.gameContainer>.csTip>.csImg {
    width: 144rpx;
    position: absolute;
    top: -43rpx;
    left: -82rpx;
}

.gameContainer>.csTip>.text {
    font-size: 24rpx;
    font-weight: normal;
    color: #D96744;
    padding-left: 63rpx;
}

.gameContainer>.luckyWrap {
    width: 548rpx;
    height: 607rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    top: 176rpx;
    left: 85rpx;
    background-image: url('https://static.joymew.com/joymewMp/hbWall/result.png');
    background-size: 100% 100%;
}

.gameContainer>.luckyWrap>.tit {
    font-size: 60rpx;
    font-weight: 400;
    color: #D5261D;
    -webkit-text-stroke: 1px #D32F10;
    text-stroke: 1px #D32F10;
    position: absolute;
    top: 85rpx;
}

.gameContainer>.luckyWrap>.congragulations {
    font-size: 30rpx;
    font-weight: 400;
    color: #5E493D;
    position: absolute;
    top: 188rpx;
}

.gameContainer>.luckyWrap>.congragulations>text {
    color: #D5261D;
    font-size: 48rpx;
}

.gameContainer>.luckyWrap>.wechatTip {
    font-size: 24rpx;
    font-weight: normal;
    color: #8C7E77;
    position: absolute;
    top: 251rpx;
}

.gameContainer>.luckyWrap>.money {
    font-size: 36rpx;
    font-weight: 400;
    color: #FBA140;
    position: absolute;
    bottom: 105rpx;
}

.showLuckyAni {
    animation: zoomIn 0.1s linear;
}

.hideLuckyAni {
    animation: zoomOut 0.1s linear;
}

@keyframes zoomIn {
    from {
        opacity: 0;
        -webkit-transform: scale3d(0.3, 0.3, 0.3);
        transform: scale3d(0.3, 0.3, 0.3);
    }

    50% {
        opacity: 1;
    }
}

@keyframes zoomOut {
    from {
        opacity: 1;
    }

    50% {
        opacity: 0;
        -webkit-transform: scale3d(0.3, 0.3, 0.3);
        transform: scale3d(0.3, 0.3, 0.3);
    }

    to {
        opacity: 0;
    }
}

.gameContainer>.giftListWrap {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 826rpx;
}

.gameContainer>.giftListWrap>.giftItem {
    width: 135rpx;
    height: 158rpx;
    position: relative;
    display: flex;
    justify-content: center;
    opacity: 1;
}

.gameContainer>.giftListWrap>.giftItem>.fudai {
    width: 100%;
    height: 100%;
    position: absolute;
    background-image: url('https://static.joymew.com/joymewMp/zyz/fd1.png');
    background-size: 100% 100%;
}

.gameContainer>.giftListWrap>.giftItem>.giftImg {
    position: absolute;
    top: 41rpx;
}

.gameContainer>.giftListWrap>.giftItem>.giftImg.g1 {
    width: 45rpx;
    height: 108rpx;
}

.gameContainer>.giftListWrap>.giftItem>.giftImg.g2 {
    width: 38rpx;
    height: 109rpx;
}

.gameContainer>.giftListWrap>.giftItem>.giftImg.g3 {
    width: 43rpx;
    height: 110rpx;
}

.gameContainer>.giftListWrap>.money {
    font-size: 48rpx;
    font-weight: bold;
    color: #EDD890;
    position: relative;
}

.gameContainer>.startBtn {
    width: 390rpx;
    height: 114rpx;
    background-image: url('https://static.joymew.com/joymewMp/zyz/startBtn2.png');
    background-size: 100% 100%;
    position: absolute;
    bottom: 0rpx;
    display: flex;
    justify-content: center;
    align-items: center;
}

.gameContainer>.startBtn>.text {
    position: absolute;
    top: 19rpx;
    font-size: 48rpx;
    font-weight: 400;
    color: #C14532;
    background: linear-gradient(177deg, #FCD58E 0%, #F8A65D 99.31640625%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.hbWallContainer>.myHbs {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.hbWallContainer>.myHbs>.myHbTitle {
    font-size: 38rpx;
    font-weight: normal;
    color: #7A0A0E;
    text-shadow: 0px 5rpx 5rpx rgba(132, 0, 15, 0.75);
    background: linear-gradient(0deg, #EFD178 0%, #FBF9B8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: absolute;
    top: 211rpx;
    letter-spacing: 16rpx;
}

.hbWallContainer>.myHbs>.myHbList {
    display: flex;
    width: 80%;
    position: absolute;
    top: 358rpx;
    justify-content: space-around;
}

.myHbList>.hbItem {
    position: relative;
    width: 90rpx;
    height: 131rpx;
    cursor: pointer;
}

.myHbList>.hbItem>.FM,
.myHbList>.hbItem>.ZM {
    position: absolute;
    width: 100%;
    height: 100%;
    transition: transform 0.8s ease-in-out;
    backface-visibility: hidden;
}

.myHbList>.hbItem>.FM {
    transform: rotateY(0deg);
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url('https://static.hudongmiao.com/joymewMp/hbWall/hbF.png');
    background-size: 100% 100%;
}

.myHbList>.hbItem>.FM>.num {
    font-size: 28rpx;
    font-weight: bold;
    color: #EDD890;
    position: absolute;
    right: 12rpx;
    top: 6rpx;
}

.myHbList>.hbItem>.ZM {
    transform: rotateY(-180deg);
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url('https://static.hudongmiao.com/joymewMp/hbWall/hbZ.png');
    background-size: 100% 100%;
    padding-top: 8rpx;
}

.myHbList>.hbItem>.ZM>.headImgBox {
    width: 61rpx;
    height: 61rpx;
    background: #650C15;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.myHbList>.hbItem>.ZM>.headImgBox>.headImg {
    width: 58rpx;
    height: 58rpx;
    border-radius: 50%;
}

.myHbList>.hbItem>.ZM>.name {
    font-size: 18rpx;
    font-weight: bold;
    color: #870F18;
    margin-top: 5rpx;
}

.myHbList>.hbItem>.ZM>.money {
    font-size: 18rpx;
    font-weight: bold;
    color: #870F18;
    margin-top: 5rpx;
}

.myHbList>.hbItem.reverse>.FM {
    transform: rotateY(180deg);
}

.myHbList>.hbItem.reverse>.ZM {
    transform: rotateY(0deg);
}

.myHbList>.hbItem.choosed {
    transform: translate3d(0rpx, -11rpx, 100rpx);
}

.myHbs>.recordList {
    width: 702rpx;
    position: absolute;
    top: 570rpx;
}

.recordList>.recordItem {
    position: relative;
    width: 100%;
    height: 130rpx;
    background-image: url('https://static.joymew.com/joymewMp/hbWall/jx.png');
    background-size: 100% 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 88rpx;
    padding-left: 48rpx;
}

.recordList>.recordItem>.name {
    font-size: 29rpx;
    font-weight: 400;
    color: #FFC683;
}

.recordList>.recordItem>.result {
    font-size: 29rpx;
    font-weight: 400;
    color: #FC2C3D;
    text-shadow: 3rpx 5rpx 9rpx #E13120;
    background: linear-gradient(0deg, #FFFBC6 0%, #FFFFFF 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.myHbs>.backBtn {
    width: 390rpx;
    height: 114rpx;
    background-image: url('https://static.joymew.com/joymewMp/zyz/startBtn2.png');
    background-size: 100% 100%;
    position: absolute;
    bottom: 0rpx;
    display: flex;
    justify-content: center;
    align-items: center;
}

.myHbs>.backBtn>.text {
    position: absolute;
    top: 19rpx;
    font-size: 48rpx;
    font-weight: 400;
    color: #C14532;
    background: linear-gradient(177deg, #FCD58E 0%, #F8A65D 99.31640625%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

@keyframes scaleAni {

    0%,
    100% {
        transform: scale(1.1);
    }

    50% {
        transform: scale(1.3);
    }
}

.rankContainer {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.rankContainer>.rankTitle {
    font-size: 62rpx;
    font-weight: normal;
    color: #7A0A0E;
    text-shadow: 0px 5rpx 5rpx rgba(132, 0, 15, 0.75);
    background: linear-gradient(0deg, #EFD178 0%, #FBF9B8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: absolute;
    top: 199rpx;
    letter-spacing: 16rpx;
}

.rankContainer>.first {
    width: 349rpx;
    height: 409rpx;
    position: absolute;
    top: 190rpx;
    background-image: url('https://static.joymew.com/joymewMp/hbWall/firstBg.png');
    background-size: 100% 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.rankContainer>.first>.num {
    font-size: 28rpx;
    font-weight: 400;
    color: #fc2c3d;
    text-shadow: 3rpx 5rpx 9rpx #e13120;
    background: linear-gradient(0deg, #fffbc6 0%, #ffffff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: absolute;
    top: 54rpx;
}

.rankContainer>.first>.headImgBox {
    position: absolute;
    width: 108rpx;
    height: 108rpx;
    background: #fff0ce;
    border: 4rpx solid;
    border-image: linear-gradient(3deg, #d16f39, #fff1ae, #d16f39) 4 4;
    transform: rotate(45deg);
    top: 123rpx;
}

.rankContainer>.first>.headImgBox>.headImg {
    width: 106rpx;
    height: 103rpx;
    position: absolute;
    top: -2rpx;
    left: -1rpx;
}

.rankContainer>.first>.headImgBox>.leftDesc {
    position: absolute;
    width: 36rpx;
    height: 36rpx;
    background: rgba(255, 240, 206, 0);
    border: 4rpx solid;
    border-image: linear-gradient(3deg, #d16f39, #fff1ae, #d16f39) 4 4;
    left: -17rpx;
    top: 86rpx;
}

.rankContainer>.first>.headImgBox>.rightDesc {
    position: absolute;
    width: 36rpx;
    height: 36rpx;
    background: rgba(255, 240, 206, 0);
    border: 4rpx solid;
    border-image: linear-gradient(3deg, #d16f39, #fff1ae, #d16f39) 4 4;
    right: -19rpx;
    top: -21rpx;
}

.rankContainer>.first>.name {
    position: absolute;
    top: 248rpx;
    width: 212rpx;
    height: 88rpx;
    font-size: 30rpx;
    font-weight: 400;
    background-image: url('https://static.joymew.com/joymewMp/hbWall/nameBox.png');
    background-size: 100% 100%;
    color: #ffc683;
    text-shadow: #b53b48 1rpx 0 0, #b53b48 0 1rpx 0, #b53b48 -1rpx 0 0, #b53b48 0 -1rpx 0, #b53b48 2rpx 0 0, #b53b48 0 2rpx 0,
        #b53b48 -2rpx 0 0, #b53b48 0 -2rpx 0, #b53b48 3rpx 0 0, #b53b48 0 3rpx 0, #b53b48 -3rpx 0 0, #b53b48 0 -3rpx 0;
    display: flex;
    justify-content: center;
    align-items: center;
}

.rankContainer>.first>.name>.text {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.rankContainer>.first>.money {
    font-size: 36rpx;
    font-weight: 400;
    color: #fc2c3d;
    text-shadow: 3rpx 5rpx 9rpx #e13120;
    background: linear-gradient(0deg, #fffbc6 0%, #ffffff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: absolute;
    top: 325rpx;
}

.rankContainer>.topThree {
    width: 702rpx;
    height: 360rpx;
    position: absolute;
    top: 597rpx;
}

.rankContainer>.topThree>.ttItem {
    position: relative;
    width: 100%;
    height: 130rpx;
    background-image: url('https://static.joymew.com/joymewMp/hbWall/jx.png');
    background-size: 100% 100%;
    display: flex;
    align-items: center;
}

.rankContainer>.topThree>.ttItem>.goldImg {
    width: 86rpx;
    height: 75rpx;
    position: absolute;
    left: 59rpx;
}

.rankContainer>.topThree>.ttItem>.silverImg {
    width: 84rpx;
    height: 76rpx;
    position: absolute;
    left: 59rpx;
}

.rankContainer>.topThree>.ttItem>.cronImg {
    width: 83rpx;
    height: 82rpx;
    position: absolute;
    left: 59rpx;
}

.rankContainer>.topThree>.ttItem>.headImgBox {
    width: 83rpx;
    height: 83rpx;
    background: #fff0ce;
    border: 4rpx solid;
    border-image: linear-gradient(3deg, #d16f39, #fff1ae, #d16f39) 4 4;
    position: absolute;
    left: 173rpx;
}

.rankContainer>.topThree>.ttItem>.headImgBox>.headImg {
    width: 79rpx;
    height: 79rpx;
}

.rankContainer>.topThree>.ttItem>.name {
    font-size: 29rpx;
    font-weight: 400;
    color: #ffc683;
    text-shadow: #b53b48 1rpx 0 0, #b53b48 0 1rpx 0, #b53b48 -1rpx 0 0, #b53b48 0 -1rpx 0, #b53b48 2rpx 0 0, #b53b48 0 2rpx 0,
        #b53b48 -2rpx 0 0, #b53b48 0 -2rpx 0, #b53b48 3rpx 0 0, #b53b48 0 3rpx 0, #b53b48 -3rpx 0 0, #b53b48 0 -3rpx 0;
    position: absolute;
    left: 301rpx;
    width: 174rpx;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.rankContainer>.topThree>.ttItem>.money {
    font-size: 29rpx;
    font-weight: 400;
    color: #fc2c3d;
    text-shadow: 3rpx 5rpx 9rpx #e13120;
    background: linear-gradient(0deg, #fffbc6 0%, #ffffff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: absolute;
    left: 491rpx;
    width: 171rpx;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.rankContainer>.otherLuckyList {
    position: absolute;
    top: 1002rpx;
    width: 100%;
    display: flex;
    justify-content: space-around;
}

.rankContainer>.otherLuckyList>.item {
    width: 93rpx;
    flex-direction: column;
    position: relative;
    display: flex;
    align-items: center;
}

.rankContainer>.otherLuckyList>.item>.headImgBox {
    width: 80rpx;
    height: 80rpx;
    border-radius: 50%;
}

.rankContainer>.otherLuckyList>.item>.headImgBox>.headImg {
    width: 100%;
    height: 100%;
    border-radius: 50%;
}

.rankContainer>.otherLuckyList>.item>.headImgBox>.num {
    width: 34rpx;
    height: 34rpx;
    background: #682b1f;
    border-image: linear-gradient(125deg, #b24816, #762e22) 2 2;
    border-radius: 50%;
    font-size: 30rpx;
    font-weight: normal;
    color: #fded9e;
    position: absolute;
    left: -2rpx;
    top: -2rpx;
}

.rankContainer>.otherLuckyList>.item>.name {
    width: 90rpx;
    margin-top: 4rpx;
}

.rankContainer>.otherLuckyList>.item>.name>.text {
    color: #fee4de;
    font-size: 26rpx;
    font-weight: normal;
    background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    overflow: hidden;
    text-overflow: ellipsis;
    width: 90rpx;
    white-space: nowrap;
    text-align: center;
}

.rankContainer>.otherLuckyList>.item>.money {
    font-size: 30rpx;
    font-weight: normal;
    color: #fded9e;
    white-space: nowrap;
}

@media screen and (min-height: 720px) {
    .gameContainer>.wall {
        top: 93rpx;
    }

    .gameContainer>.csTip {
        top: 957rpx;
    }

    .gameContainer>.giftListWrap {
        top: 1086rpx;
    }

    .gameContainer>.dec01 {
        top: 619rpx;
    }
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

## File: pages/hotelReserve/couponDetail/couponDetail.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/couponDetail/couponDetail.wxss
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

## File: pages/hotelReserve/hotelDetail/hotelDetail.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/hotelDetail/hotelDetail.wxss
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
  },
})
```

## File: pages/hotelReserve/hotelReserve.json
```json
{
  "navigationBarTitleText": "婚宴预定"
}
```

## File: pages/hotelReserve/hotelReserve.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/hotelReserve.wxss
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

## File: pages/hotelReserve/menuDetail/menuDetail.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/menuDetail/menuDetail.wxss
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

## File: pages/hotelReserve/packageDetail/packageDetail.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/hotelReserve/packageDetail/packageDetail.wxss
```
page {
    background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/index/index.js
```javascript
import { getMsgInfo, sendChatMessage } from '../../api/index/index';
import { newDateTransform, getCurrentDate } from '../../utils/date';
import { getRandom, showWxToast } from '../../utils/index';
import { getUserInfo } from '../../utils/storage';

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
  '新婚快乐！我们一起摇红包、做game、中大奖、沾喜气，嗨起来！',
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
  'everybaby  high 起来！',
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
    scrollTop: 0,
  },
  onLoad: function() {
    this.initWishes();
    this.requestMsgInfo();
  },
  sendDanmu() {
    sendChatMessage(this.data.message).then(res => {
      console.log(res);
      const { nickName, avatarUrl } = getUserInfo();
      const tmpChatList = this.data.chatList;
      tmpChatList.push({
        miaoContent: this.data.message,
        sendTime: getCurrentDate(),
        miaoName: nickName,
        miaoTxUrl: avatarUrl,
      });
      this.setData({
        chatList: tmpChatList,
        message: '',
        sendDanmuVisible: false,
        scrollTop: tmpChatList.length * 200,
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
      quickWishes: tmpQuickWish,
    });
  },
  handleInput(e) {
    console.log(e.detail.value);
    this.setData({
      message: e.detail.value,
    });
  },
  chooseDefaultWish(e) {
    console.log(e.currentTarget.dataset.index);
    this.setData({
      message: this.data.defaultWishes[e.currentTarget.dataset.index],
      autoFocus: true,
    });
  },
  showSendDanmu() {
    this.setData({
      sendDanmuVisible: true,
      autoFocus: true,
    });
  },
  closeSendDanmu() {
    this.setData({
      sendDanmuVisible: false,
    });
  },
  requestMsgInfo() {
    getMsgInfo().then(res => {
      if (
        res &&
        res.data &&
        res.data.chat_list &&
        res.data.chat_list.length > 0
      ) {
        const list = res.data.chat_list
          .filter(item => !item.miaoLiwuId)
          .map(item => ({
            ...item,
            sendTime: newDateTransform(item.sendTime, 16),
          }));
        console.log(list);
        this.setData({
          chatList: list,
          scrollTop: list.length * 200,
        });
      }
    });
  },
  chooseQuickWish(e) {
    console.log(e.currentTarget.dataset.index);
    let tmpQuickWish = this.data.quickWishes;
    sendChatMessage(tmpQuickWish[e.currentTarget.dataset.index]).then(res => {
      console.log(res);
      const { nickName, avatarUrl } = getUserInfo();
      const tmpChatList = this.data.chatList;
      tmpChatList.push({
        miaoContent: tmpQuickWish[e.currentTarget.dataset.index],
        sendTime: getCurrentDate(),
        miaoName: nickName,
        miaoTxUrl: avatarUrl,
      });
      tmpQuickWish.splice(e.currentTarget.dataset.index, 1);
      this.setData({
        chatList: tmpChatList,
        quickWishes: tmpQuickWish,
        scrollTop: tmpChatList.length * 200,
      });
    });
  },
});
```

## File: pages/index/index.json
```json
{
    "navigationBarTitleText": " 嗨喵互动",
    "backgroundColor": "#305068",
    "disableScroll": false
}
```

## File: pages/index/index.wxml
```
<view class="index-wrap">
    <view class="bg"></view>
    <view class="chatArea">
        <view class="weddingChatList">
            <scroll-view class="newsContainer" scroll-y="true" style="height:502rpx" scrollTop="{{scrollTop}}">
                <view class="messageItem" wx:for="{{chatList}}" wx:key="index">
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
                    <view class="item" wx:for="{{quickWishes}}" wx:key="index" bindtap="chooseQuickWish"
                        data-index="{{index}}">
                        <view class="itemCt">
                            {{item}}
                        </view>
                    </view>
                </view>
            </view>
            <view class="bottomMain {{sendDanmuVisible ? 'show' : ''}}">
                <view class="bottomEmptyArea" bindtap="closeSendDanmu" wx:if="{{sendDanmuVisible}}"></view>
                <view class="default" wx:if="{{sendDanmuVisible}}">
                    <view class="defaultCt">
                        <view class="item" wx:for="{{defaultWishes}}" data-index="{{index}}" wx:key="index"
                            bindtap="chooseDefaultWish">
                            <view class="itemCt">{{item}}</view>
                        </view>
                    </view>
                </view>
                <view class="iptArea">
                    <image src="/assets/image/hd2/messageIcon.png" class="msgIcon"></image>
                    <view class="inputBoxVitual" wx:if="{{!sendDanmuVisible}}" bindtap="showSendDanmu">送上祝福...</view>
                    <input class="inputBox" placeholder="送上祝福..." bindinput="handleInput" value="{{message}}"
                        wx:if="{{sendDanmuVisible}}" focus="{{autoFocus}}" placeholder-style="font-size:16px" disabled/>
                    <view class="sendBtn {{message ? 'active' : ''}}" wx:if="{{sendDanmuVisible}}" bindtap="sendDanmu">
                        发送</view>
                </view>
            </view>
        </view>
    </view>
</view>
```

## File: pages/index/index.wxss
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
  getLiveInfo,
  getLiveIdByUserId,
  saveSignInfo,
} from '../../api/index/index';
import {
  getToken,
  setLiveId,
  getLiveId,
  setUseTipFlag,
  getUseTipFlag,
  getUserInfo,
  clearStorage,
  setToken,
  setUserInfo,
} from '../../utils/storage';
import {
  getCurrentTimestamp,
  dateCompare
} from '../../utils/date';
import defaultContent from '../../assets/constant/default';
import {
  getRandom,
  showWxToast
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
  'https://static.joymew.com/joymewScreen/defaultHeadImg2.png';
const EXAMINETOKEN =
  'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHQiOjE2OTczMzQ1MDI4NzYsInVpZCI6ImRmMTUwZjZlNGFlMDQ4NjA5NmQyZmYyNGNjNGFlYWVjIiwiaWF0IjoxNjk2NzI5NzAyODc2fQ.Wawo2rUZMyeLbmUP1hC9IDZC-8JF3UQQojr29S4xDcc';
Page({
  data: {
    sceneType: '', // 场景类型 0: 婚礼版 1:企业版 2:生日版
    role: '', // 亲友类型 1:男方亲友 2:女方亲友 ''：不选
    userName: '', // 姓名
    wish: '', // 祝福语
    userPhone: '', // 手机号
    birthDate: '',
    gender: '0',
    activityTitle: '',
    liveId: '',
    needAuth: false, // 是否需要授权登录
    isOverdate: false, // 活动是否过期
    isValid: true, // 活动是否有效
    customSignWishList: [], // 自定义签到语列表
    isExamine: false, // 是否是isExamine live
    isContantQrcode: false, // 是否是固定二维码 live
    userIdParam: '', // 二维码中携带的userId参数
    needH5Auth: false, // 是否需要H5授权(新用户需要启用H5授权获取头像昵称)
    wxGetPhoneButtonVisible: false,
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
      },
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
        liveId: tmpLiveId,
      });
    } else if (stLiveId) {
      if (!this.validateExamineLive(stLiveId)) {
        this.setExamine();
        return;
      }
      // 直接进入
      this.setData({
        liveId: stLiveId,
      });
    } else {
      this.setExamine();
    }
    if (!this.data.isContantQrcode) {
      setLiveId(this.data.liveId);
    }
  },

  onShow: function () {
    if (this.data.needAuth) {
      return;
    }
    if (this.data.isContantQrcode) {
      // 通过userId换取liveId后再获取活动信息
      this.getLiveInfoIndirect();
    } else {
      this.getLiveInfoDirect();
    }
  },
  onShareAppMessage: function () {
    let tmpShareObj;
    if (this.data.sceneType === '0') {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
        imageUrl: '/assets/image/shareCard.png',
      };
    } else if (this.data.sceneType === '1') {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
        imageUrl: '/assets/image/shareCard-annualMeeting01.png',
      };
    } else if (this.data.sceneType === '2') {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
        imageUrl: '/assets/image/birthBg02.png',
      };
    } else {
      tmpShareObj = {
        title: this.data.activityTitle,
        path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
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
      (stUserInfo.avatarUrl === DEFAULTAVATOR && this.data.liveId !== LIVEID)
    ) {
      this.setData({
        needAuth: true,
      });
      return;
    }
    // 初始化用户信息
    app.setUserInfo();
    this.setData({
      userName: app.globalData.userInfo.nickName,
    });
    // 判断是否签到
    getSignInState()
      .then(res => {
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
        if (isSign) {
          console.log('***不需要签到***');
          // 不需要签到
          this.toLive();
        }
      })
      .catch(err => {
        console.log(err);
        // token过期需要授权登录
        this.setData({
          needAuth: true,
        });
      });
  },

  // 判断是否签到--->签到逻辑
  sign(e) {
    console.log(e);
    this.setData({
      userName: this.data.userName,
      wish: e.detail.wish,
      role: e.detail.role || '',
      userPhone: e.detail.userPhone || '',
      birthDate: e.detail.birthDate || '',
      gender: e.detail.gender,
    });
    if (this.data.isOverdate) {
      showWxToast('活动已结束!');
      return;
    }
    if (!this.data.isValid) {
      showWxToast('活动信息错误，请重新进入!');
      return;
    }
    console.log('needH5Auth:', this.data.needH5Auth);
    if (this.data.needH5Auth) {
      this.signLogicNeedH5Auth();
    } else {
      this.signLogic();
    }
  },
  // 跳转live页面
  toLive() {
    console.log('***app globalData中的数据***');
    console.log(app.globalData);
    console.log('***跳转live***');
    if (this.data.isExamine) {
      wx.navigateTo({
        url: '/pages/index/index',
      });
      return;
    }
    console.log('***needH5Auth***');
    console.log(this.data.needH5Auth);
    if (this.data.needH5Auth) {
      app.setH5Url(
        `https://shm.hudongmiao.com/hmScanReportController/method1?token=${getToken()}`,
      );
    } else {
      // h5是否提示过的标识 缓存中有值说明提示过 没有值说明没有提示过
      const useTipFlag = getUseTipFlag();
      const staicUrl = `${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}`;
      let variableUrl = '';
      if (!useTipFlag) {
        variableUrl += '&useTipFlag=1';
      }
      if (variableUrl) {
        app.setH5Url(staicUrl + variableUrl);
        // 缓存中标记已经提示过
        setUseTipFlag();
        console.log(staicUrl + variableUrl);
      } else {
        app.setH5Url(staicUrl);
        console.log(staicUrl);
      }
    }
    wx.redirectTo({
      url: '/pages/live/live',
    });
  },
  // 刷新祝福语
  refreshWish() {
    // 设置自定义签到语
    let customSignLen = this.data.customSignWishList.length;
    if (customSignLen > 0) {
      this.setData({
        wish: this.data.customSignWishList[getRandom(0, customSignLen)],
      });
      return;
    }
    // 设置默认祝福语
    if (this.data.sceneType === '0') {
      this.setData({
        wish: defaultContent.wishesWedding[getRandom(0, 20)],
      });
    } else if (this.data.sceneType === '1') {
      this.setData({
        wish: defaultContent.wishesAnnualMeeting[getRandom(0, 20)],
      });
    } else if (this.data.sceneType === '2') {
      this.setData({
        wish: defaultContent.wishesBirth[getRandom(0, 14)],
      });
    } else if (this.data.sceneType === '21') {
      this.setData({
        wish: defaultContent.wishesBBY[getRandom(0, 10)],
      });
    } else if (this.data.sceneType === '22') {
      this.setData({
        wish: defaultContent.wishesSY[getRandom(0, 8)],
      });
    } else if (this.data.sceneType === '23') {
      this.setData({
        wish: defaultContent.wishesCRL[getRandom(0, 9)],
      });
    } else if (this.data.sceneType === '24') {
      this.setData({
        wish: defaultContent.wishesBLY[getRandom(0, 6)],
      });
    } else if (this.data.sceneType === '25') {
      this.setData({
        wish: defaultContent.wishesMYY[getRandom(0, 8)],
      });
    } else if (this.data.sceneType === '41') {
      this.setData({
        wish: defaultContent.wishesBYDL[getRandom(0, 31)],
      });
    } else if (this.data.sceneType === '42') {
      this.setData({
        wish: defaultContent.wishesXSY[getRandom(0, 25)],
      });
    } else if (this.data.sceneType === '43') {
      this.setData({
        wish: defaultContent.wishesJBTM[getRandom(0, 24)],
      });
    } else if (this.data.sceneType === '51') {
      this.setData({
        wish: defaultContent.wishesTXH[getRandom(0, 50)],
      });
    } else if (this.data.sceneType === '52') {
      this.setData({
        wish: defaultContent.wishesQQY[getRandom(0, 8)],
      });
    } else if (this.data.sceneType === '53') {
      this.setData({
        wish: defaultContent.wishesHX[getRandom(0, 7)],
      });
    }
  },
  // 授权登录成功后的回调
  handleAuthSuccess(e) {
    // 用户名赋值
    console.log('***用户名赋值 关闭授权框***');
    this.setData({
      userName: app.globalData.userInfo.nickName,
      needAuth: false,
    });
    if (e.detail === 'needH5Auth') {
      this.setData({
        needH5Auth: true,
      });
    }
    // 获取签到状态
    getSignInState()
      .then(res => {
        console.log('***handleAuthSuccess 获取签到状态***');
        console.log(res);
        if (this.data.isOverdate) {
          showWxToast('活动已结束!');
          return;
        }
        if (res.data.qian_dao_le_me) {
          // 不需要签到
          this.toLive();
        }
      })
      .catch(err => {
        console.log(err);
        // token过期需要重新授权登录
        if (err === '401') {
          this.setData({
            needAuth: true,
          });
        }
      });
  },
  // 授权登录失败的回调
  handleAuthFail() {
    clearStorage();
    this.setData({
      needAuth: false,
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
      avatarUrl: DEFAULTAVATOR,
    });
    this.setData({
      liveId: LIVEID,
      isExamine: true,
    });
  },
  getLiveInfoDirect() {
    getLiveInfo().then(res => {
      console.log('活动信息:', res);
      if (res && res.data && res.data.splid) {
        this.setData({
          activityTitle: res.data.splid.theme,
          sceneType: res.data.splid.scenario,
        });
        app.globalData.sceneType = this.data.sceneType;
        app.globalData.activityTitle = this.data.activityTitle;
        // 设置扭一扭奖项列表
        const tmpNynPrizeArray = [];
        const tmpNynList = res.data.nynList.split(',');
        for (let i = 0; i < tmpNynList.length; i++) {
          if (tmpNynList[i] !== '-1') {
            if (tmpNynList[i] === '0') {
              tmpNynPrizeArray.push({
                desc: '谢谢参与',
                endIndex: i,
              });
            } else {
              tmpNynPrizeArray.push({
                desc: tmpNynList[i] + '元',
                endIndex: i,
              });
            }
          }
        }
        app.globalData.nynList = tmpNynPrizeArray;
        if (res.data.signWish && res.data.signWish.length > 0) {
          let tmpSignWishList = res.data.signWish.map(item => {
            return item.bless_str;
          });
          this.setData({
            customSignWishList: tmpSignWishList,
          });
        }
        // 设置默认祝福语
        this.refreshWish();
        // 活动是否过期
        if (
          dateCompare(res.data.splid.using_date) ||
          res.data.splid.is_end_wedding === '1'
        ) {
          this.setData({
            isOverdate: true,
          });
        }
        if (res.data.siyiInfo) {
          // 是否展示微信获取手机号组件
          this.setData({
            wxGetPhoneButtonVisible: res.data.siyiInfo.isOpenWxPhone === '1'
          });
        }
        // 通知活动信息已经获取到可以执行主逻辑了
        Observer.liveInfoGetted = true;
      } else {
        showWxToast('活动信息获取错误，请重新进入!');
        this.setData({
          isValid: false,
        });
      }
    });
  },
  getLiveInfoIndirect() {
    getLiveIdByUserId(this.data.userIdParam)
      .then(res => {
        this.setData({
          liveId: res.data.splid,
        });
        setLiveId(res.data.splid);
      })
      .then(() => {
        this.getLiveInfoDirect();
      })
      .catch(err => {
        console.log(err);
      });
  },
  decodeQrcodeParam(qrcodeParamStr) {
    const paramKey = qrcodeParamStr.split('?')[1].split('=')[0];
    const paramVal = qrcodeParamStr.split('?')[1].split('=')[1];
    if (!paramKey || !paramVal) {
      showWxToast('微信版本过低!');
      return;
    }
    if (paramKey === 'userId') {
      this.setData({
        isContantQrcode: true,
        userIdParam: paramVal,
      });
      return;
    }
    if (!this.validateExamineLive(paramVal)) {
      this.setExamine();
    }
    this.setData({
      liveId: paramVal,
    });
  },
  // 需要H5授权的签到逻辑(需要H5授权说明一定没有签到过)
  signLogicNeedH5Auth() {
    // h5是否提示过的标识 缓存中有值说明提示过 没有值说明没有提示过
    const useTipFlag = getUseTipFlag();
    const staicUrl = `${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}`;
    let variableUrl = '';
    if (!useTipFlag) {
      variableUrl += '&useTipFlag=1';
    }
    if (variableUrl) {
      app.setH5Url(staicUrl + variableUrl);
      // 缓存中标记已经提示过
      setUseTipFlag();
      console.log(staicUrl + variableUrl);
    } else {
      app.setH5Url(staicUrl);
      console.log(staicUrl);
    }
    saveSignInfo({
        bless_str: this.data.wish,
        phonenumber: this.data.userPhone,
        type: this.data.role,
        birthDate: this.data.birthDate,
        gender: this.data.gender,
        redirect_url: app.globalData.h5Url,
      })
      .then(() => {
        // 后台完成签到
        this.toLive();
      })
      .catch(err => {
        console.log(err);
        // token过期需要重新授权登录
        if (err === '401') {
          this.setData({
            needAuth: true,
          });
        }
      });
  },
  signLogic() {
    getSignInState()
      .then(res => {
        console.log('***sign 获取签到状态***');
        console.log(res);
        return res.data.qian_dao_le_me;
      })
      .then(res2 => {
        console.log(res2);
        if (!res2) {
          // 需要签到
          return signIn({
            wish: this.data.wish,
            name: this.data.userName,
            role: this.data.role,
            userPhone: this.data.userPhone,
            birthDate: this.data.birthDate,
            gender: this.data.gender,
          });
        } else {
          // 不需要签到
          this.toLive();
        }
      })
      .then(res3 => {
        if (res3 && res3.success) {
          console.log('***签到接口返回***');
          console.log(res3);
          this.toLive();
        }
      })
      .catch(err => {
        console.log(err);
        // token过期需要重新授权登录
        if (err === '401') {
          this.setData({
            needAuth: true,
          });
        }
      });
  },
});
```

## File: pages/joymewIndex/joymewIndex.json
```json
{
    "navigationBarTitleText": " 嗨喵悦动",
    "usingComponents": {
        "signNew": "../../components/sign/sign"
    },
    "disableScroll": true
}
```

## File: pages/joymewIndex/joymewIndex.wxml
```
<view class="joymewIndex">
    <!-- 签到模块 -->
    <signNew id="signNew" sceneType="{{sceneType}}" activityTitle="{{activityTitle}}" isExamine="{{isExamine}}" wishProp="{{wish}}" wxGetPhoneButtonVisible="{{wxGetPhoneButtonVisible}}" bind:refreshWishEvent="refreshWish" bind:signEvent="sign" ></signNew>
    <!-- 授权登录弹窗 -->
    <authDialogNew dialogVisible="{{needAuth}}" bind:authSuccess="handleAuthSuccess" bind:authFail="handleAuthFail"></authDialogNew>
</view>
```

## File: pages/joymewIndex/joymewIndex.wxss
```
.joymewIndex {
    width: 100vw;
    height: 100vh;
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
    background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/box2-01.png');
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
    background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/box-01.png');
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
    background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/round.png');
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
    background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/roundActive.png');
    background-size: 100% 100%;
    width: 34rpx;
    height: 34rpx;
}

.joymewIndex>.signBox>.signBtn {
    background-image: url('https://static.hudongmiao.com/joymewMp/joymewIndex/btn.png');
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

## File: pages/kbx/kbx.js
```javascript
import { getGameState, sendBroadCast, getBoxesList, robBox, kbxRecharge, getMyBoxes } from '../../api/kbx/kbx';
import { wxPay } from '../../api/pay';
import { timeoutTask, getRandom, showWxToast, showWxLoading, hideWxLoading } from '../../utils/index';

const app = getApp();
const BX = [
    {
        num: '01',
        left: 129,
        top: 168,
    }, {
        num: '02',
        left: 281,
        top: 168,
    }, {
        num: '03',
        left: 444,
        top: 168,
    }, {
        num: '05',
        left: 62,
        top: 330,
    }, {
        num: '06',
        left: 213,
        top: 330,
    }, {
        num: '07',
        left: 365,
        top: 330,
    }, {
        num: '08',
        left: 521,
        top: 330,
    }, {
        num: '09',
        left: 37,
        top: 508,
    }, {
        num: '10',
        left: 201,
        top: 508,
    }, {
        num: '11',
        left: 364,
        top: 508,
    }, {
        num: '12',
        left: 521,
        top: 508,
    }, {
        num: '13',
        left: 42,
        top: 662,
    }, {
        num: '15',
        left: 206,
        top: 662,
    }, {
        num: '16',
        left: 360,
        top: 662,
    }, {
        num: '17',
        left: 526,
        top: 662,
    }, {
        num: '18',
        left: 117,
        top: 814,
    }, {
        num: '19',
        left: 279,
        top: 814,
    }, {
        num: '20',
        left: 444,
        top: 814,
    },
];
const giftList = [
    {
        id: 1,
        gift: 'rocket1',
        name: '小号火箭',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket1.png',
    }, {
        id: 2,
        gift: 'rocket2',
        name: '中号火箭',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket2.png',
    }, {
        id: 3,
        gift: 'rocket3',
        name: '大号火箭',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket3.png',
    }
];
const wishList = [
    '醉酒饱德，不胜感激',
    '美酒佳肴,不甚荣幸',
    '感谢招待,祝愿安康',
    '小小红包,感谢招待'
];
let requestLock = false;
Page({
    data: {
        gameStatus: 1, // 开宝箱状态(控制页面显示)
        myBoxesVisible: false,
        boxes: [],
        chooseBoxIds: [],
        remain: 3,
        money: 0,
        gift_show: { //当前显示的礼物
            id: 3,
            gift: 'rocket3',
            name: '大号火箭',
            imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket3.png',
            price: 0,
        },
        userId: '',
        openId: '',
        name: '',
        headImg: '',
        isForbidBuyHbq: false,
        luckyBoxes: [],
    },
    onLoad: function (options) {
        requestLock = false;
        this.setData({
            userId: options.userId,
            openId: options.openId,
            name: options.name,
            headImg: options.headImg,
            isForbidBuyHbq: options.isForbidBuyHbq === 'true' ? true : false,
        });
        getGameState(this.data.userId).then((res) => {
            if (res.success) {
                if (res.data.status === '1') {
                    this.setData({
                        gameStatus: 2,
                    });
                    this.getBoxes();
                } else if (res.data.status === '2') {
                    showWxToast('本轮开宝箱已经结束');
                    timeoutTask(() => {
                        wx.navigateBack();
                    }, 1500);
                }
            }
        })

    },
    onShow: function () {

    },
    onUnload: function () {
    },
    // 获取宝箱列表
    getBoxes: function () {
        getBoxesList().then((res) => {
            if (res.success && res.data) {
                const tmpLen = res.data.length;
                const tmpBoxes = [];
                for (let i = 0; i < tmpLen; i += 1) {
                    tmpBoxes.push({
                        id: res.data[i].eggId,
                        isBuyed: res.data[i].userId === '0' ? false : true,
                        isChoosed: false,
                        buyerId: res.data[i].userId,
                        num: BX[i].num,
                        left: BX[i].left,
                        top: BX[i].top,
                    });
                }
                this.setData({
                    boxes: tmpBoxes,
                    money: parseFloat(res.message),
                });
                this.setRemain();
                this.updateGift();
                console.log('宝箱列表:', this.data.boxes);
            } else {
                showWxToast('获取宝箱信息失败');
            }
        })
    },
    // 获取已经选择宝箱的数目
    getChoosedBoxesNum: function (isIncludeBuyed) {
        const boxes = this.data.boxes;
        const len = boxes.length;
        let tmpNum = 0;
        if (isIncludeBuyed) {
            for (let i = 0; i < len; i += 1) {
                if (boxes[i].isChoosed || boxes[i].buyerId === this.data.userId) {
                    tmpNum += 1;
                }
            }
        } else {
            for (let i = 0; i < len; i += 1) {
                if (boxes[i].isChoosed) {
                    tmpNum += 1;
                }
            }
        }
        return tmpNum;
    },
    // 获取已经选择的宝箱列表
    getChoosedBoxesList: function () {
        const boxes = this.data.boxes;
        const len = boxes.length;
        const tmpChoosedBoxes = [];
        for (let i = 0; i < len; i += 1) {
            if (boxes[i].isChoosed) {
                tmpChoosedBoxes.push(boxes[i]);
            }
        }
        return tmpChoosedBoxes;
    },
    // 设置还可以购买的宝箱个数(一共可购买三个)
    setRemain: function () {
        let tmpRemain = 0;
        const tmpLen = this.data.boxes.length;
        for (let i = 0; i < tmpLen; i += 1) {
            if (this.data.boxes[i].buyerId === this.data.userId) {
                tmpRemain += 1;
            }
        }
        this.setData({
            remain: tmpRemain,
        });
    },
    // 获取选择的宝箱数目时更新祝福列表
    updateGift: function () {
        const hasChoosedNum = this.getChoosedBoxesNum(false);
        this.boxesMapGift(hasChoosedNum);
    },
    // 祝福和已选择的宝箱数的映射
    boxesMapGift: function (choosedNum) {
        const tmpMoney = this.data.money;
        giftList[0].price = tmpMoney.toFixed(2);
        giftList[1].price = (tmpMoney * 2).toFixed(2);
        giftList[2].price = (tmpMoney * 3).toFixed(2);
        if (choosedNum == 3) {
            //选了3个宝箱<---> 大火箭
            this.setData({
                gift_show: giftList[2],
            })
        } else if (choosedNum == 2) {
            //选了2个宝箱<---> 中火箭
            this.setData({
                gift_show: giftList[1],
            })
        } else {
            //选了1个宝箱或者还没有选蛋<--->小火箭
            this.setData({
                gift_show: giftList[0],
            })
        }
    },
    enterGame: function () {
        getGameState(this.data.userId).then((res) => {
            console.log('***获取开宝箱状态***');
            console.log(res);
            if (res.success) {
                if (res.data.status === '0') {
                    showWxToast('请等待大屏开启开宝箱');
                } else if (res.data.status === '1') {
                    // 开宝箱进行中
                    this.getBoxes();
                    this.setData({
                        gameStatus: 2,
                    })
                } else if (res.data.status === '2') {
                    showWxToast('本轮开宝箱已经结束');
                    timeoutTask(() => {
                        wx.navigateBack();
                    }, 1500);
                } else {
                    showWxToast('请等待大屏开启开宝箱');
                }
            }
        }).catch((err) => {
            console.log(err);
        });
    },
    // 选择宝箱
    chooseBoxes: function (e) {
        const index = this.findBoxIndexByBoxId(e.currentTarget.dataset.id);
        const boxes = this.data.boxes;
        if (boxes[index].isBuyed) {
            showWxToast('这个宝箱已经被抢走啦');
            return;
        }
        // 如果选中 取消选中
        if (boxes[index].isChoosed) {
            boxes[index].isChoosed = false;
            this.setData({
                boxes,
            });
            this.updateGift();
            return;
        }
        // 最多3个宝箱 包括已经购买的
        const hasChoosedNum = this.getChoosedBoxesNum(true);
        if (hasChoosedNum >= 3) {
            showWxToast('最多只能选择三个宝箱哦');
            return;
        }
        if (!boxes[index].isChoosed) {
            boxes[index].isChoosed = true;
            this.setData({
                boxes,
            })
            this.updateGift();
        }
    },
    // 通过boxesId查找宝箱所在数组的索引
    findBoxIndexByBoxId: function (boxId) {
        let tmpIndex = -1;
        const tmpLen = this.data.boxes.length;
        for (let i = 0; i < tmpLen; i += 1) {
            if (this.data.boxes[i].id === boxId) {
                tmpIndex = i;
                break;
            }
        }
        return tmpIndex;
    },
    // 打开我的宝箱页面
    toMyBoxes: function () {
        this.getLuckyBoxes();
        this.setData({
            myBoxesVisible: true,
        });
    },
    // 打开宝箱购买页面
    toBuyBoxes: function () {
        this.setData({
            myBoxesVisible: false,
        });
    },
    // 买宝箱
    buy: function () {
        // 获取选中的宝箱
        const choosed = this.getChoosedBoxesList();
        if (choosed.length == 0) {
            showWxToast('请先选一个宝箱');
            return;
        }
        if (requestLock) {
            return;
        }
        console.log(typeof this.data.isForbidBuyHbq);
        if(this.data.isForbidBuyHbq) {
            showWxToast('您没有权限买宝箱!');
            return;
        }
        requestLock = true;
        let choosedStr = choosed.map((item) => {
            return item.id;
        }).join(',');
        this.robBox(choosedStr, 0).then((res) => {
            console.log(res);
            if (res.code === 'success') {
                requestLock = false;
                if (res.resultList.length == 0) {
                    wx.showModal({
                        showCancel: false,
                        title: '温馨提示',
                        content: '很遗憾您选择的宝箱都被抢走了\r\n已退回至您的账户中',
                        confirmText: '确定',
                        success: () => {
                        }
                    });
                } else {
                    if (choosed.length > res.resultList.length) {
                        wx.showModal({
                            showCancel: false,
                            title: '温馨提示',
                            content: '恭喜您,成功抢到了' + res.resultList.length + '个宝箱！ \r\n 未抢到的宝箱，已退回至您的账户中',
                            confirmText: '查看宝箱',
                            success: () => {
                                this.getLuckyBoxes();
                                this.setData({
                                    myBoxesVisible: true,
                                });
                            }
                        })
                    } else {
                        wx.showModal({
                            showCancel: false,
                            title: '温馨提示',
                            content: '恭喜您,成功抢到了' + res.resultList.length + '个宝箱!',
                            confirmText: '查看宝箱',
                            success: () => {
                                this.getLuckyBoxes();
                                this.setData({
                                    myBoxesVisible: true,
                                });
                            }
                        })
                    }
                    console.log(res.resultList);
                    let tmpCode = '';
                    if (this.data.gift_show.id === 3) {
                        tmpCode = 7002;
                    } else if (this.data.gift_show.id === 2) {
                        tmpCode = 6002;
                    } else if (this.data.gift_show.id === 1) {
                        tmpCode = 5002;
                    }
                    let c = JSON.stringify({
                        code: tmpCode,
                        param: {
                            headImg: this.data.headImg,
                            nickname: this.data.name,
                            wish: wishList[getRandom(0, 4)],
                        }
                    });
                    // 发送广播
                    sendBroadCast({
                        c,
                    });
                    app.globalData.isH5NeedRefresh = true;
                }
                this.getBoxes();
            } else if (res.code === 'error3') {
                if (res.NeedMoney) {
                    // 调起支付
                    return this.recharge(res.NeedMoney);
                } else {
                    showWxToast('购买失败!');
                }
            } else if (res.code === 'error4') {
                    showWxToast('开宝箱已经结束!');
                    requestLock = false;
            } else {
                showWxToast('购买失败');
                requestLock = false;
            }
        }).catch((err) => {
            console.log(err);
        })
    },
    // 抢宝箱
    robBox: function (boxId, sort) {
        return new Promise((resolve, reject) => {
            showWxLoading('奋力争抢中...');
            robBox({
                boxIds: boxId,
                sort: 0,
            }).then((res) => {
                console.log(res);
                hideWxLoading();
                resolve(res);
            }).catch((err) => {
                console.log(err);
                reject(err);
                hideWxLoading();
                showWxToast('抢购失败!');
            })
        });
    },
    // 支付
    recharge: function (money) {
        return new Promise((resolve, reject) => {
            kbxRecharge({
                userId: this.data.userId,
                openid: this.data.openId,
                money,
            }).then((res) => {
                console.log(res);
                if (res.status === 'success') {
                    wxPay(res).then((res2) => {
                        console.log(res2);
                        resolve(res2);
                        showWxToast('充值成功!');
                        requestLock = false;
                        app.globalData.isH5NeedRefresh = true;
                        //充值完成 等待后台加喵钻逻辑完成后 去买宝箱
                        timeoutTask(() => {
                            this.buy();
                        }, 500);
                    }).catch((err) => {
                        console.log(err);
                        showWxToast('充值失败!');
                        requestLock = false;
                        reject(err);
                    })
                }
            }).catch((err) => {
                console.log(err);
                reject(err);
            })
        });
    },
    // 获取我的宝箱
    getLuckyBoxes: function () {
        getMyBoxes().then((res) => {
            console.log(res);
            if (res.success) {
                if (res.data && res.data.length > 0) {
                    const tmpBoxes = [];
                    const tmpLen = res.data.length;
                    for (let i = 0; i < tmpLen; i += 1) {
                        if (res.data[i].eggId) {
                            let tmpEggId = parseInt(res.data[i].eggId);
                            if (tmpEggId <= 3) {
                                res.data[i].num = `0${tmpEggId}`;
                            } else if (tmpEggId >= 4 && tmpEggId <= 8) {
                                res.data[i].num = `0${tmpEggId + 1}`;
                            } else if (tmpEggId >= 9 && tmpEggId <= 12) {
                                res.data[i].num = `${tmpEggId + 1}`;
                            } else {
                                res.data[i].num = `${tmpEggId + 2}`;
                            }
                            tmpBoxes.push(res.data[i]);
                        }
                    }
                    this.setData({
                        luckyBoxes: tmpBoxes
                    });
                }
            } else {
                showWxToast('获取宝箱信息失败!');
            }
        }).catch((err) => {
            console.log(err);
            showWxToast('获取宝箱信息失败!');
        })
    },
    toAgreement: function () {
        wx.navigateTo({
            url: '/pages/agreement/agreement'
        });
    },
});
```

## File: pages/kbx/kbx.json
```json
{
  "navigationBarTitleText": "开宝箱",
  "usingComponents": {
    "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
  },
  "disableScroll": true
}
```

## File: pages/kbx/kbx.wxml
```
<view class="kbxContainer">
    <!-- 等待界面 -->
    <view class="waitContainer" wx:if="{{gameStatus === 1}}">
        <image src="https://static.hudongmiao.com/joymewMp/img/kbx/kbxWaitBg.png" class="bg"></image>
        <image src="https://static.hudongmiao.com/joymewMp/img/kbx/kbxWaitBx.png" class="kbxWaitBx"></image>
        <view class="tip2">只需送出弹幕礼物，免费获得一次夺取宝箱的机会</view>
        <view class="sendGiftItem item1">送出小号火箭：获取一个宝箱</view>
        <view class="sendGiftItem item2">送出中号火箭：获取二个宝箱</view>
        <view class="sendGiftItem item3">送出大号火箭：获取三个宝箱</view>
        <view class="tip3">ps:如果宝箱被抢完，您支付得金额将原路退回您得账户</view>
        <view class="btn" bindtap="enterGame">开始</view>
    </view>
    <!-- 开宝箱界面 -->
    <view class="gameContainer" wx:if="{{gameStatus === 2 && !myBoxesVisible}}">
        <image src="https://static.hudongmiao.com/joymewMp/kbx/bg3-01.png" class="bg"></image>
        <image src="https://static.hudongmiao.com/joymewMp/kbx/title3-01.png" class="title"></image>
        <image src="https://static.hudongmiao.com/joymewMp/kbx/ribbonLeft.png" class="ribbonLeft"></image>
        <image src="https://static.hudongmiao.com/joymewMp/kbx/ribbonRigth.png" class="ribbonRight"></image>
        <view class="bx {{item.isChoosed?'active':''}}" data-id="{{item.id}}" wx:for="{{boxes}}" wx:key="index" style="left:{{item.left}}rpx;top:{{item.top}}rpx" bindtap="chooseBoxes">
            <image src="https://static.hudongmiao.com/joymewMp/kbx/bx3.png" class="bxImg {{item.isBuyed?'buyed':''}}"></image>
            <view class="num">{{item.num}}</view>
        </view>
        <view class="giftListWrap">
            <view class="giftItem">
                <image src="{{gift_show.imgUrl}}" class="giftImg g{{gift_show.id}}"></image>
            </view>
            <view class="money">￥{{gift_show.price}}</view>
        </view>
        <view class="btn" bindtap='buy'>获取宝箱</view>
        <view class="myBoxBtn" bindtap="toMyBoxes"></view>
        <view class="agreement" bindtap='toAgreement'>阅读并同意《充值服务协议》</view>
    </view>
    <!-- 我的宝箱界面 -->
    <view class="myBoxes" wx:if="{{gameStatus === 2 && myBoxesVisible}}">
        <image src="https://static.hudongmiao.com/joymewMp/kbx/bg4-01.png" class="bg"></image>
        <image src="https://static.hudongmiao.com/joymewMp/kbx/title2-01.png" class="title"></image>
        <view class="myBxList">
            <view class="bx" wx:for="{{luckyBoxes}}" key="index">
                <image src="{{item.open==='0'?'https://static.hudongmiao.com/joymewMp/kbx/bx3.png':'https://static.hudongmiao.com/joymewMp/kbx/bxOpen3.png'}}" class="bxImg"></image>
                <view class="num {{item.open==='0'?'':'active'}}">{{item.num}}</view>
            </view>
        </view>
        <view class="myWinRecord">
            <image src="https://static.hudongmiao.com/joymewMp/kbx/loveIcon.png" class="loveIcon"></image>
            <text>我的中奖记录</text>
            <image src="https://static.hudongmiao.com/joymewMp/kbx/loveIcon.png" class="loveIcon"></image>
        </view>
        <view class="winItem item{{index+1}}" wx:for="{{luckyBoxes}}" key="index">
            <view class="bxName">{{item.num}}号宝箱</view>
            <view class="bxStatus">
                {{item.open==='0'?'未开启':(item.money==='0'?'谢谢参与':item.money)}}
            </view>
        </view>
        <view class="btn" bindtap="toBuyBoxes">返回</view>
    </view>
    <!-- 反馈入口 -->
    <feedbackEntry userId="{{userId}}"></feedbackEntry>
</view>
```

## File: pages/kbx/kbx.wxss
```
/* 等待界面 */
.kbxContainer>.waitContainer {
    position: absolute;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: all 0.3s ease-out;
}

.kbxContainer>.waitContainer>.bg {
    width: 100%;
    height: 100%;
    position: absolute;
}

.kbxContainer>.waitContainer>.kbxWaitBx {
    width: 750rpx;
    height: 780rpx;
    position: absolute;
    top: -102rpx;
    left: 0;
}

.kbxContainer>.waitContainer>.bx {
    width: 536rpx;
    height: 361rpx;
    position: absolute;
    top: 584rpx;
}

.kbxContainer>.waitContainer>.tip2 {
    font-size: 22rpx;
    font-weight: 400;
    color: #FFFFFF;
    position: absolute;
    top: 680rpx;
}

.kbxContainer>.waitContainer>.tip3 {
    font-size: 24rpx;
    font-weight: 400;
    color: #FEFEFE;
    position: absolute;
    top: 1009rpx;
}

.kbxContainer>.waitContainer>.sendGiftItem {
    width: 618rpx;
    height: 70rpx;
    border-radius: 8rpx;
    position: absolute;
    font-size: 28rpx;
    font-weight: 400;
    color: #FFFFFF;
    text-align: center;
    line-height: 70rpx;
}

.kbxContainer>.waitContainer>.btn {
    width: 439rpx;
    height: 106rpx;
    background-image: url('https://static.hudongmiao.com/joymewMp/kbx/btn2.png');
    background-size: 100% 100%;
    position: absolute;
    top: 1060rpx;
    text-align: center;
    font-size: 40rpx;
    font-weight: 400;
    color: #FFFFFF;
    text-shadow: 0px 2px 1px #880C0C;
    line-height: 83rpx;
}

.kbxContainer>.waitContainer>.sendGiftItem.item1 {
    top: 737rpx;
    background: #D1000E;
}

.kbxContainer>.waitContainer>.sendGiftItem.item2 {
    top: 820rpx;
    background: #FCAB0F;
}

.kbxContainer>.waitContainer>.sendGiftItem.item3 {
    top: 909rpx;
    background: #63A8FF;
}

/* 开宝箱界面 */
.kbxContainer>.gameContainer {
    position: absolute;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: all 0.3s ease-out;
}

.kbxContainer>.gameContainer>.bg {
    width: 100%;
    height: 100vh;
    position: absolute;
}

.kbxContainer>.gameContainer>.title {
    width: 327rpx;
    height: 89rpx;
    position: absolute;
    top: 43rpx;
}

.kbxContainer>.gameContainer>.ribbonLeft {
    width: 117rpx;
    height: 124rpx;
    position: absolute;
    left: 51rpx;
    top: 225rpx;
}

.kbxContainer>.gameContainer>.ribbonRight {
    width: 117rpx;
    height: 124rpx;
    position: absolute;
    right: 51rpx;
    top: 225rpx;
}

.kbxContainer>.gameContainer>.bx {
    width: 200rpx;
    height: 139rpx;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all 0.3s linear;
}

.kbxContainer>.gameContainer>.bx.active {
    animation-name: bounce;
    transform-origin: center bottom;
    animation-duration: 1s;
    transform: scale(1.2);
}

.kbxContainer>.gameContainer>.bx>.bxImg {
    position: absolute;
    width: 100%;
    height: 100%;
}

.kbxContainer>.gameContainer>.bx>.bxImg.buyed {
    filter: grayscale(100%);
}

.kbxContainer>.gameContainer>.bx>.num {
    font-size: 20rpx;
    color: #B97601;
    position: relative;
    left: -21rpx;
    top: -21rpx;
    font-weight: bold;
}

.kbxContainer>.gameContainer>.giftListWrap {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 937rpx;
}

.kbxContainer>.gameContainer>.giftListWrap>.giftItem {
    width: 78rpx;
    height: 92rpx;
    position: relative;
    display: flex;
    justify-content: center;
    opacity: 1;
}

.kbxContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg {
    position: absolute;
}

.kbxContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg.g1 {
    width: 45rpx;
    height: 92rpx;
}

.kbxContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg.g2 {
    width: 39rpx;
    height: 92rpx;
}

.kbxContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg.g3 {
    width: 43rpx;
    height: 92rpx;
}

.kbxContainer>.gameContainer>.giftListWrap>.money {
    font-size: 48rpx;
    font-weight: bold;
    color: #EDD890;
    position: relative;
}

.kbxContainer>.gameContainer>.btn {
    width: 439rpx;
    height: 106rpx;
    background-image: url('https://static.hudongmiao.com/joymewMp/kbx/btn2.png');
    background-size: 100% 100%;
    position: absolute;
    top: 1037rpx;
    text-align: center;
    font-size: 40rpx;
    font-weight: 400;
    color: #FFFFFF;
    text-shadow: 0px 2px 1px #880C0C;
    line-height: 83rpx;
}

.kbxContainer>.gameContainer>.myBoxBtn {
    width: 103rpx;
    height: 103rpx;
    background-image: url('https://static.hudongmiao.com/joymewMp/kbx/myBoxBtn.png');
    background-size: 100% 100%;
    position: absolute;
    right: 43rpx;
    top: 1037rpx;
    /* animation-name: scaleAni;
    animation-duration: 1s;
    animation-timing-function: ease-out;
    animation-iteration-count: infinite; */
    /* transform-origin: top center;
    animation-name: swing;
    animation-duration: 1s;
    animation-iteration-count: infinite; */
}

.kbxContainer>.gameContainer>.agreement {
    font-size: 24rpx;
    font-weight: 400;
    color: #FFD027;
    position: absolute;
    top: 1143rpx;
}

/* 我的宝箱界面 */
.kbxContainer>.myBoxes {
    position: absolute;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: all 0.3s ease-out;
}

.kbxContainer>.myBoxes>.bg {
    position: absolute;
    width: 100%;
    height: 100%;
}

.kbxContainer>.myBoxes>.title {
    position: absolute;
    width: 458rpx;
    height: 244rpx;
    top: 37rpx;
}

.kbxContainer>.myBoxes>.myBxList {
    position: absolute;
    width: 100%;
    display: flex;
    justify-content: center;
    top: 420rpx;
}

.kbxContainer>.myBoxes>.myBxList>.bx {
    width: 200rpx;
    height: 139rpx;
    position: relative;
}

.kbxContainer>.myBoxes>.myBxList>.bx>.bxImg {
    width: 100%;
    height: 100%;
}

.kbxContainer>.myBoxes>.myBxList>.bx>.num {
    font-size: 20rpx;
    color: #B97601;
    position: absolute;
    left: 69rpx;
    font-weight: bold;
    top: 36rpx;
}

.kbxContainer>.myBoxes>.myBxList>.bx>.num.active {
    top: 46rpx;
    left: 62rpx;
}

.kbxContainer>.myBoxes>.myWinRecord {
    position: absolute;
    top: 571rpx;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 36rpx;
    font-weight: 500;
    color: #FFFFFF;
}

.kbxContainer>.myBoxes>.myWinRecord>.loveIcon {
    width: 29rpx;
    height: 25rpx;
    margin: 20rpx;
}

.kbxContainer>.myBoxes>.winItem {
    width: 596rpx;
    height: 114rpx;
    background: rgba(255, 109, 119, 0.3);
    border-radius: 8rpx;
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 60rpx 0 35rpx;
}

.kbxContainer>.myBoxes>.winItem.item1 {
    top: 716rpx;
}

.kbxContainer>.myBoxes>.winItem.item2 {
    top: 858rpx;
}

.kbxContainer>.myBoxes>.winItem.item3 {
    top: 1002rpx;
}


.kbxContainer>.myBoxes>.winItem>.bxName {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFFFFF;
}

.kbxContainer>.myBoxes>.winItem>.bxStatus {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFF32E;
}

.kbxContainer>.myBoxes>.btn {
    width: 439rpx;
    height: 106rpx;
    background-image: url('https://static.hudongmiao.com/joymewMp/kbx/btn2.png');
    background-size: 100% 100%;
    position: absolute;
    bottom: 12rpx;
    text-align: center;
    font-size: 40rpx;
    font-weight: 400;
    color: #FFFFFF;
    text-shadow: 0px 2px 1px #880C0C;
    line-height: 83rpx;
}


@keyframes bounce {

    from,
    20%,
    53%,
    80%,
    to {
        -webkit-animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
        animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
        -webkit-transform: translate3d(0, 0, 0);
        transform: translate3d(0, 0, 0);
    }

    40%,
    43% {
        -webkit-animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
        animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
        -webkit-transform: translate3d(0, -30px, 0);
        transform: translate3d(0, -30px, 0);
    }

    70% {
        -webkit-animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
        animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
        -webkit-transform: translate3d(0, -15px, 0);
        transform: translate3d(0, -15px, 0);
    }

    90% {
        -webkit-transform: translate3d(0, -4px, 0);
        transform: translate3d(0, -4px, 0);
    }
}

@keyframes scaleAni {

    0%,
    100% {
        transform: scale(1.1);
    }

    50% {
        transform: scale(1.3);
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
    liveId: '',
  },
  onLoad: function(options) {
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: app.globalData.activityTitle,
      liveId: getLiveId(),
    });
    console.log('***h5Url***');
    console.log(this.data.h5Url);
    console.log('***activityTitle***');
    console.log(this.data.activityTitle);
  },
  onShow: function() {
    if (app.globalData.isH5NeedRefresh) {
      console.log('***h5 needRefresh***');
      app.globalData.isH5NeedRefresh = false;
      this.updateH5Url();
      removeOrigin();
      this.setData({
        h5Url: app.globalData.h5Url,
        activityTitle: app.globalData.activityTitle,
        liveId: getLiveId(),
      });
      console.log('***h5Url***');
      console.log(this.data.h5Url);
      console.log('***activityTitle***');
      console.log(this.data.activityTitle);
    }
  },
  updateH5Url() {
    const staicUrl = `${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}`;
    let variableUrl = '';
    const tmpOrigin = getOrigin();
    switch (tmpOrigin) {
      case 'sendGift':
        variableUrl = '&origin=sendGift';
        break;
      case 'purchaseEnterEffect':
        variableUrl = '&origin=purchaseEnterEffect';
        break;
      case 'sendBapin':
        variableUrl = '&origin=sendBapin';
        break;
      case 'sendPhoto':
        variableUrl = '&origin=sendPhoto';
        break;
      case 'sendDanmu':
        variableUrl = '&origin=sendDanmu';
        break;
      case 'sendDanmuHby':
        variableUrl = '&origin=sendDanmuHby';
        break;
      case 'editInfo':
        variableUrl = '&origin=editInfo';
        break;
      case 'sendDiamondHb':
        variableUrl = '&origin=sendDiamondHb';
        break;
      default:
        variableUrl = '';
    }

    if (variableUrl) {
      app.setH5Url(staicUrl + variableUrl);
      console.log(staicUrl + variableUrl);
    } else {
      app.setH5Url(staicUrl);
      console.log(staicUrl);
    }
  },
  onShareAppMessage: function() {
    return {
      title: this.data.activityTitle,
      path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
    };
  },
});
```

## File: pages/live/live.json
```json
{
  "navigationBarTitleText": " 嗨喵悦动",
  "backgroundColor": "#305068",
  "disableScroll": true
}
```

## File: pages/live/live.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/live/live.wxss
```
page {
  background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/nyn/nyn.js
```javascript
import { timeoutTask, getRandom, showWxToast } from '../../utils/index';
import { getPoolMoney, getNynInfo, getNynRank, nynRecharge, startNyn, sendPrizeInfo, sendBroadCast } from '../../api/nyn/nyn';
import { wxPay } from '../../api/pay';
import defaultContent from '../../assets/constant/default';

const app = getApp();
// 蛋位置信息
const locatInfo = [
    {
        x: 118,
        y: 0,
        fallAniDelay: 0.2,
        rotateAniDelay: 0.1,
        upAniDelay: 1.6,
        rotateAniDelay2: 1.5,
    },
    {
        x: 258,
        y: 26,
        fallAniDelay: 0.4,
        rotateAniDelay: 0.3,
        upAniDelay: 1.4,
        rotateAniDelay2: 1.3,
    },
    {
        x: 392,
        y: 62,
        fallAniDelay: 0.6,
        rotateAniDelay: 0.5,
        upAniDelay: 1.2,
        rotateAniDelay2: 1.1,
    },
    {
        x: 0,
        y: 80,
        fallAniDelay: 0.8,
        rotateAniDelay: 0.7,
        upAniDelay: 1,
        rotateAniDelay2: 0.9,
    },
    {
        x: 124,
        y: 128,
        fallAniDelay: 1,
        rotateAniDelay: 0.9,
        upAniDelay: 0.8,
        rotateAniDelay2: 0.7,
    },
    {
        x: 264,
        y: 162,
        fallAniDelay: 1.2,
        rotateAniDelay: 1.1,
        upAniDelay: 0.6,
        rotateAniDelay2: 0.5,
    },
    {
        x: 412,
        y: 192,
        fallAniDelay: 1.4,
        rotateAniDelay: 1.3,
        upAniDelay: 0.4,
        rotateAniDelay2: 0.3,
    },
    {
        x: 8,
        y: 212,
        fallAniDelay: 1.6,
        rotateAniDelay: 1.5,
        upAniDelay: 0.2,
        rotateAniDelay2: 0.1,
    },
]
// 蛋类型
const eggType = [
    {
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/egg1-01.png',
        width: 141,
        height: 155,
        luckyBeginY: -148,
    }, {
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/egg2.png',
        width: 141,
        height: 140,
        luckyBeginY: -136,
    }, {
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/egg3.png',
        width: 141,
        height: 140,
        luckyBeginY: -136,
    }, {
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/egg4-01.png',
        width: 141,
        height: 141,
        luckyBeginY: -140,
    },
];
// 礼物数组
const giftList = [
    {
        id: 1,
        gift: 'rocket1',
        name: '小号火箭',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/rocket1.png',
        isChoosed: true
    }, {
        id: 2,
        gift: 'rocket2',
        name: '中号火箭',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/rocket2.png',
        isChoosed: false
    }, {
        id: 3,
        gift: 'rocket3',
        name: '大号火箭',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/nyn/rocket3.png',
        isChoosed: false
    }
];
const wishList = [
    '醉酒饱德，不胜感激',
    '美酒佳肴,不甚荣幸',
    '感谢招待,祝愿安康',
    '小小红包,感谢招待'
];

let tmpInterval; //用于倒计时
let tmpInterval2; //用于轮询
let lock = false; //锁，用于确保 倒计时方法 一轮只调用一次
let lock2 = false;//锁，用于确保 执行动画的过程中不可以点按钮
let lock3 = false;//锁，用于确保 开始按钮不能连续点击
Page({
    data: {
        gameStatus: 1, // 扭一扭状态(控制页面显示)
        eggList: [], // 扭蛋列表
        prizeItemList: [],// 奖项列表
        poolMoney: 0, //奖池金额
        countDownNum: 0,// 倒计时
        isEntry: false,// 充值入口
        rechargeTipList: [], //充值提示列表
        luckyTipList: [], //中奖提示列表
        topRankList: [],// 排行榜列表
        otherRankList: [],
        isRechargeTipShow: false, //控制充值提示显示隐藏
        isResultTipShow: false, //控制扭一扭结果提示显示隐藏
        user: {
            nickname: 'player',
            money: 0
        }, //充值用户
        resultTipContent: {
            resultImgSrc: '',
            para1: '',
            para2: '',
            result: '',
            ptVal: 44,
        }, //充值结果内容
        btnText: '发送礼物',
        userId: '',
        openId: '',
        name: '',
        headImg: '',
        turnId: '', //一场扭一扭的id 0代表要充值 否则代表这场扭一扭的id
        giftList: giftList,
        giftListShow: true,
        rechargeTipAni: '',
        resultTipAni: '',
        luckyEgg: {
            imgUrl: '',
            width: '',
            height: '',
            luckyBeginY: 0,
            luckyEndY: 0,
            isFallLuckyAni: false,
            isRotateAni: false,
            left: 22,
            top: -124,
        },
    },
    onLoad: function (options) {
        tmpInterval = null;
        tmpInterval2 = null;
        lock = false;
        lock2 = false;
        lock3 = false;
        this.setData({
            userId: options.userId,
            openId: options.openId,
            name: options.name,
            headImg: options.headImg,
            prizeItemList: app.globalData.nynList,
        });
        this.requestPoolMoney();
        this.initEggList();
    },
    onShow: function () {
        this.toGame();
    },
    onHide: function () {
        //清除定时器
        clearInterval(tmpInterval);
        clearInterval(tmpInterval2);
        tmpInterval = null;
        tmpInterval2 = null;
        lock = false;
    },
    onUnload: function () {
        //清除定时器
        clearInterval(tmpInterval);
        clearInterval(tmpInterval2);
        tmpInterval = null;
        tmpInterval2 = null;
    },
    initEggList() {
        let tmpEggList = [];
        const len = this.data.prizeItemList.length;
        console.log(this.data.prizeItemList);
        for (let i = 0; i < len; i += 1) {
            this.createEgg(tmpEggList, i);
        }
        this.setData({
            eggList: tmpEggList,
        });
    },
    createEgg(tmArr, num) {
        let typeIndex = num > 3 ? num - 4 : num;
        let tmpDesc;
        if (this.data.prizeItemList[num]) {
            tmpDesc = this.data.prizeItemList[num].desc;
        } else {
            tmpDesc = '谢谢参与';
        }
        console.log(eggType, typeIndex);
        const egg = {
            num: num + 1,
            imgUrl: eggType[typeIndex].imgUrl,
            width: eggType[typeIndex].width,
            height: eggType[typeIndex].height,
            left: locatInfo[num].x,
            bottom: locatInfo[num].y,
            fallAniDelay: locatInfo[num].fallAniDelay,
            rotateAniDelay: locatInfo[num].rotateAniDelay,
            isFallAni: false,
            aroundAni: '',
            isRotateAni: false,
            prize: tmpDesc,
        };
        tmArr.push(egg);
    },
    fallEgg() {
        let tmpEggList = this.data.eggList;
        for (let i = 0; i < 8; i += 1) {
            tmpEggList[i].isFallAni = true;
            tmpEggList[i].isRotateAni = true;
        }
        this.setData({
            eggList: tmpEggList
        });
        timeoutTask(() => {
            for (let i = 0; i < 8; i += 1) {
                tmpEggList[i].isFallAni = false;
                tmpEggList[i].isRotateAni = false;
            }
            this.setData({
                eggList: tmpEggList
            });
        }, 2000);
    },
    beginAroundAni() {
        let tmpEggList = this.data.eggList;
        for (let i = 0; i < 8; i += 1) {
            tmpEggList[i].fallAniDelay = locatInfo[i].upAniDelay;
            tmpEggList[i].rotateAniDelay = locatInfo[i].rotateAniDelay2;
            this.setData({
                eggList: tmpEggList
            });
            // timeoutTask(() => {
            tmpEggList[i].isRotateAni = true;
            tmpEggList[i].aroundAni = `aroundAni${tmpEggList[i].num}`;
            this.setData({
                eggList: tmpEggList
            });
            // }, 100);
        }
    },
    endAroudAni() {
        let tmpEggList = this.data.eggList;
        for (let i = 0; i < 8; i += 1) {
            tmpEggList[i].isRotateAni = false;
            tmpEggList[i].aroundAni = '';
        }
        this.setData({
            eggList: tmpEggList
        });
    },
    handleStartBtnTap() {
        if (this.data.btnText === '发送礼物') {
            //判断是否选中某个礼物
            const resultIndex = this.data.giftList.findIndex((item) => {
                return item.isChoosed;
            });
            if (resultIndex > -1) {
                console.log(resultIndex);
                if (this.data.isEntry) {
                    // 充值入口开着
                    this.recharge();
                } else {
                    // 最后十五秒购买入口关闭
                    showWxToast('购买入口关闭');
                }
            } else {
                showWxToast('请选择一个礼物');
            }
        }
    },
    tapstartNyn() {
        getNynInfo().then((res) => {
            console.log(res);
            this.setData({
                turnId: res.data.id
            });
            this.startGame();
        }).catch((err) => {
            console.log(err);
            showWxToast('网络异常');
        });
    },
    // 选择礼物
    chooseGift(e) {
        console.log(e)
        const choosedId = e.currentTarget.dataset.id;
        const tmpGiftList = this.data.giftList;
        tmpGiftList.forEach(item => {
            if (item.id === choosedId) {
                item.isChoosed = true;
            } else {
                item.isChoosed = false;
            }
        });
        this.setData({
            giftList: tmpGiftList
        });
    },
    // 扭一扭动画
    gameAniStart(endIndex, endMoney) {
        this.beginAroundAni();
        timeoutTask(() => {
            console.log('***5s后结束扭一扭动画 展示luckyEgg***');
            this.endAroudAni();
            this.showLuckyEgg(endIndex, endMoney);
        }, 5000);
        timeoutTask(() => {
            console.log('***6s后 展示resultTip***');
            this.showResultTip(endIndex, this.data.name, endMoney);
        }, 6000);
        timeoutTask(() => {
            console.log('***10s后恢复状态***');
            this.setData({
                btnText: '发送礼物',
                giftListShow: true,
            });
        }, 10000);
    },
    // 充钱玩扭一扭
    recharge() {
        if (lock2) {
            return;
        }
        lock2 = true;
        nynRecharge({
            userId: this.data.userId,
            openId: this.data.openId,
        }).then((res) => {
            console.log(res);
            return wxPay(res);
        }).then(() => {
            showWxToast('礼物发送成功!');
            this.sendGift(this.getChoosedGift());
            //充值成功按钮状态立即改变
            this.setData({
                btnText: '扭一扭',
                giftListShow: false,
            });
            // startGame
            timeoutTask(() => {
                // this.handleStartBtnTap();
                console.log('***2s后自动扭一扭***')
                this.tapstartNyn();
            }, 2000);

        }).catch((err) => {
            console.log(err);
            lock2 = false;
            showWxToast('支付失败!');
        });
    },
    getChoosedGift() {
        return this.data.giftList.find(item => {
            return item.isChoosed;
        });
    },
    sendGift(giftChoosed) {
        let tmpCode = '';
        if (giftChoosed.id == 1) {
            tmpCode = 5002;
        } else if (giftChoosed.id == 2) {
            tmpCode = 6002;
        } else if (giftChoosed.id == 3) {
            tmpCode = 7002;
        }
        const c = JSON.stringify({
            code: tmpCode,
            param: {
                headImg: this.data.headImg,
                nickname: this.data.name,
                wish: wishList[parseInt(Math.random() * 3)]
            }
        });
        sendBroadCast({
            c,
        });
    },
    // 扭一扭
    startGame() {
        startNyn({
            turnId: this.data.turnId,
        }).then((res) => {
            console.log('startNyn result:', res);
            //res.data.desc 奖项；endMoney中奖的金额；totalMoney 奖池金额
            //奖池金额刷新
            if (res.data.totalMoney.balance) {
                this.setData({
                    poolMoney: res.data.totalMoney.balance
                })
            }
            //扭一扭动画开始
            this.gameAniStart(res.data.lotteryType, res.data.endMoney);

            // 5s动画停止后发送广播(必须要中奖的情况)
            if (parseInt(res.data.endMoney) > 0) {
                timeoutTask(() => {
                    this.sendBroad(res.data.endMoney, res.data.totalMoney.balance);
                }, 5000);
            }
            timeoutTask(() => {
                lock2 = false;
            }, 5000);
        }).catch((err) => {
            console.log(err);
            lock2 = false;
        });
    },
    // 点击进入扭一扭
    toGame() {
        if (lock3) {
            return;
        }
        lock3 = true;
        this.requestGameInitInfo();
    },
    // 获取奖池金额
    requestPoolMoney() {
        getPoolMoney().then((res) => {
            console.log(res);
            this.setData({
                poolMoney: res.data.balance
            });
        }).catch((err) => {
            console.log(err);
        });
    },
    // 获取扭一扭相关信息
    requestGameInitInfo() {
        getNynInfo().then((res) => {
            console.log('***获取扭一扭基本信息***');
            console.log(res);
            //res.data.id 发送礼物 1扭一扭
            if (res.data.id == 0) {
                this.setData({
                    btnText: '发送礼物',
                    giftListShow: true,
                    turnId: res.data.id
                })
            } else {
                this.setData({
                    btnText: '扭一扭',
                    giftListShow: false,
                    turnId: res.data.id
                })
            }
            // 时间处理(用于倒计时) res.data.endTime
            if (res.data.endTime === '0') {
                // 扭一扭未开始的情况处理
                showWxToast('扭一扭尚未开始!');
            } else {
                let countTime = this.timeHandle(res.data.endTime);
                console.log('***接口返回endTime***');
                console.log(res.data.endTime);
                this.countDown(countTime);
                this.setData({
                    gameStatus: 2,
                });
                this.fallEgg();
                // 轮询获取充值和中奖列表
                if (!tmpInterval2) {
                    tmpInterval2 = setInterval(() => {
                        console.log('tmpInterval2');
                        this.noticeShow();
                    }, 4000);
                }
            }
            lock3 = false;
        }).catch((err) => {
            console.log(err);
            lock3 = false;
        });
    },
    // 获取充值和中奖列表
    requestTipList() {
        let tmpLuckyTipList = [];
        let tmpRechargeTipList = [];
        getPoolMoney().then((res) => {
            console.log('***getPoolMoney***', res);
            const subTime = this.timeHandle(res.data.endTime);
            if (subTime <= 0) {
                // 扭一扭提前结束
                this.requestRankList();
            }
            for (let i = 0; i < res.data.list.length; i += 1) {
                tmpRechargeTipList.push({
                    nickname: res.data.list[i].wx_name,
                    money: res.data.list[i].gsum,
                });
                if (parseInt(res.data.list[i].c01) > 0) { //确保 “谢谢参与的” 奖项不弹出
                    tmpLuckyTipList.push({
                        nickname: res.data.list[i].wx_name,
                        endMoney: res.data.list[i].c01
                    })
                }
            }
            this.setData({
                rechargeTipList: tmpRechargeTipList,
                luckyTipList: tmpLuckyTipList,
                poolMoney: res.data.balance
            });
        }).catch((err) => {
            console.log(err);
        })
    },
    // 时间戳处理
    timeHandle(endTime) {
        //获取当前时间戳
        var nowTime = (new Date()).getTime();
        var subTime = parseInt((parseInt(endTime) - parseInt(nowTime)) / 1000);
        if (subTime < 0) {
            subTime = 0;
        }
        return subTime;
    },
    // 不带毫秒的倒计时
    countDown(second) {
        if (lock == false && !tmpInterval) {
            lock = true;
            tmpInterval = setInterval(() => {
                console.log('tmpInterval');
                if (second <= 1) {
                    this.setData({
                        isEntry: false,
                        countDownNum: second
                    })
                    this.requestRankList();
                } else {
                    second -= 1;
                    if (second <= 7) {
                        this.setData({
                            isEntry: false
                        })
                    } else {
                        this.setData({
                            isEntry: true
                        })
                    }
                    this.setData({
                        countDownNum: second
                    })
                }

            }, 1000)
        }
    },
    // 弹出消息(包括充值和中奖)
    noticeShow() {
        if (this.data.rechargeTipList[app.globalData.nynRechargeIndex] && this.data.isRechargeTipShow == false) {
            //当前存在未弹出的充值消息
            let tmpObj = {};
            tmpObj.nickname = this.data.rechargeTipList[app.globalData.nynRechargeIndex].nickname;
            tmpObj.money = this.data.rechargeTipList[app.globalData.nynRechargeIndex].money;
            this.setData({
                user: tmpObj
            })
            //调用showRechargeTip方法
            this.showRechargeTip();
        } else {
            //更新数组
            this.requestTipList();
        }
        if (this.data.luckyTipList[app.globalData.nynLuckyIndex] && this.data.isResultTipShow == false) {
            //当前存在未弹出的中奖消息
            let tmpObj = {};
            tmpObj = this.data.luckyTipList[app.globalData.nynLuckyIndex];
            //loopShowResultTip
            this.loopShowResultTip(tmpObj.nickname, tmpObj.endMoney);
        } else {
            //更新数组
            this.requestTipList();
        }
    },
    // 获取排行榜列表
    requestRankList() {
        getNynRank().then((res) => {
            console.log(res);
            lock = false;
            let tmpTopRankArray = [];
            let tmpOtherRankArray = [];
            let count = 0;
            let tmpLen = res.data.list.length;
            // 限制中奖名单人数最多不超过10个
            if (tmpLen > 10) {
                tmpLen = 10;
            }
            while (count < tmpLen) {
                if (count < 3) {
                    tmpTopRankArray.push({
                        nickname: res.data.list[count].wx_name,
                        headimgurl: res.data.list[count].avator,
                        money: Math.floor(parseFloat(res.data.list[count].money))
                    });
                } else {
                    tmpOtherRankArray.push({
                        num: count < 0 ? `0${count + 1}` : (count + 1),
                        nickname: res.data.list[count].wx_name,
                        headimgurl: res.data.list[count].avator,
                        money: Math.floor(parseFloat(res.data.list[count].money))
                    });
                }
                count += 1;
            }
            if (tmpTopRankArray.length < 3) {
                const tmpLen2 = tmpTopRankArray.length;
                for (let i = tmpLen2; i < 3; i += 1) {
                    tmpTopRankArray.push({
                        nickname: 'Player',
                        headimgurl: defaultContent.defaultHeadImg,
                        money: 0,
                    });
                }
            }
            // 不足七个补齐
            if (tmpOtherRankArray.length < 7) {
                const tmpLen3 = tmpOtherRankArray.length;
                for (let i = tmpLen3; i < 7; i += 1) {
                    tmpOtherRankArray.push({
                        num: i + 3 < 0 ? `0${i + 4}` : (i + 4),
                        nickname: 'Player',
                        headimgurl: defaultContent.defaultHeadImg,
                        money: 0,
                    });
                }
            }

            console.log(tmpOtherRankArray);
            this.setData({
                topRankList: tmpTopRankArray,
                otherRankList: tmpOtherRankArray,
                gameStatus: 3,
            });
            // 停止轮询
            clearInterval(tmpInterval2);
            clearInterval(tmpInterval);
            tmpInterval = null;
            tmpInterval2 = null;
        }).catch((err) => {
            console.log(err);
        });
    },
    showRechargeTip() {
        this.setData({
            isRechargeTipShow: true
        });
        this.setData({
            rechargeTipAni: 'rechargeTipAni'
        });
        timeoutTask(() => {
            this.setData({
                rechargeTipAni: 'rechargeTipAni2'
            });
        }, 3000);
        timeoutTask(() => {
            this.setData({
                isRechargeTipShow: false
            });
            app.updateNynRechargeIndex();
        }, 4000);
    },
    loopShowResultTip(pNickname, money) {
        let nickname = pNickname || '匿名';
        if (parseInt(money) > 0) {
            //抽中
            let result = {
                resultImgSrc: 'https://static.hudongmiao.com/joymewMp/nyn/happyMew-01.png',
                para1: '恭喜' + nickname,
                para2: '获得' + money + '奖励',
                result: 1,
                ptVal: 34,
            };
            this.setData({
                resultTipContent: result,
                isResultTipShow: true,
                resultTipAni: 'resultTipAni',
            });
            timeoutTask(() => {
                this.setData({
                    resultTipAni: 'resultTipAni2'
                });
            }, 4000);
            timeoutTask(() => {
                this.setData({
                    isResultTipShow: false
                });
                app.updateNynLuckyIndex();
            }, 4000);
        } else {
            //未抽中
            let result = {
                resultImgSrc: 'https://static.hudongmiao.com/joymewMp/nyn/sadMew-01.png',
                para1: '很遗憾没有抽中',
                para2: '谢谢惠顾，再接再厉',
                result: 0,
                ptVal: 44,
            };
            this.setData({
                resultTipContent: result,
                isResultTipShow: true,
                resultTipAni: 'resultTipAni',
            });
            timeoutTask(() => {
                this.setData({
                    resultTipAni: 'resultTipAni2'
                });
            }, 4000);
            timeoutTask(() => {
                this.setData({
                    isResultTipShow: false
                });
            }, 4000);
        }
    },
    showResultTip(num, pNickname, money) {
        console.log('***showReusltTip***');
        console.log(this.data.prizeItemList);
        console.log(num);
        let desc;
        if (this.data.prizeItemList[parseInt(num)]) {
            desc = this.data.prizeItemList[parseInt(num)].desc;
        } else {
            desc = '谢谢参与';
        }
        let nickname = pNickname || '匿名';
        if (money) {
            desc = money;
        }
        if (num == 0) {
            //未抽中
            let result = {
                resultImgSrc: 'https://static.hudongmiao.com/joymewMp/nyn/sadMew-01.png',
                para1: '很遗憾没有抽中',
                para2: '谢谢惠顾，再接再厉',
                result: 0,
                ptVal: 44,
            };
            this.setData({
                resultTipContent: result,
                isResultTipShow: true,
                resultTipAni: 'resultTipAni',
            });
            timeoutTask(() => {
                this.setData({
                    resultTipAni: 'resultTipAni2'
                });
            }, 4000);
            timeoutTask(() => {
                this.setData({
                    isResultTipShow: false
                });
            }, 4000);
        } else {
            //抽中
            let result = {
                resultImgSrc: 'https://static.hudongmiao.com/joymewMp/nyn/happyMew-01.png',
                para1: '恭喜' + nickname,
                para2: '获得' + desc + '奖励',
                result: 1,
                ptVal: 34,
            };
            this.setData({
                resultTipContent: result,
                isResultTipShow: true,
                resultTipAni: 'resultTipAni',
            });
            timeoutTask(() => {
                this.setData({
                    resultTipAni: 'resultTipAni2'
                });
            }, 4000);
            timeoutTask(() => {
                this.setData({
                    isResultTipShow: false
                });
                app.updateNynLuckyIndex();
            }, 4000);
        }
    },
    // 发广播
    sendBroad(golds, remainCoins) {
        sendPrizeInfo({
            gold: golds,
            remainCoin: remainCoins,
            turnId: this.data.turnId,
        }).then((res) => {
            console.log(res);
        }).catch((err) => {
            console.log(err);
            showWxToast('网络异常');
        });
    },
    // 蛋掉落 从蛋下落并停留到消失 耗时 3s
    showLuckyEgg(endIndex, endMoney) {
        this.createLuckyEgg(endIndex, endMoney);
        const tmpLuckyEgg = this.data.luckyEgg;
        tmpLuckyEgg.top = this.data.luckyEgg.luckyBeginY;
        console.log('***蛋下落动画执行***');
        tmpLuckyEgg.isFallLuckyAni = true;
        tmpLuckyEgg.isRotateAni = true;
        this.setData({
            luckyEgg: tmpLuckyEgg,
        });
        // 下落后保持在终点位置
        timeoutTask(() => {
            tmpLuckyEgg.end = 208;
            tmpLuckyEgg.isRotateAni = false;
            console.log('***保持在终点位置***');
            this.setData({
                luckyEgg: tmpLuckyEgg,
            });
        }, 1000);
        timeoutTask(() => {
            console.log('***回到初始位置***');
            tmpLuckyEgg.isFallLuckyAni = false;
            tmpLuckyEgg.end = '';
            tmpLuckyEgg.top = this.data.luckyEgg.luckyBeginY;
            this.setData({
                luckyEgg: tmpLuckyEgg,
            });
        }, 4000);
    },
    // 创建中奖扭蛋
    createLuckyEgg(num, money) {
        console.log('***createLuckyEgg***');
        console.log(num, money);
        console.log(this.data.prizeItemList);
        const eggTypeIndex = getRandom(0, 4);
        const tmpLuckyEgg = this.data.luckyEgg;
        tmpLuckyEgg.imgUrl = eggType[eggTypeIndex].imgUrl;
        tmpLuckyEgg.width = eggType[eggTypeIndex].width;
        tmpLuckyEgg.height = eggType[eggTypeIndex].height;
        tmpLuckyEgg.luckyBeginY = eggType[eggTypeIndex].luckyBeginY;
        let desc;
        if (this.data.prizeItemList[parseInt(num)]) {
            desc = this.data.prizeItemList[parseInt(num)].desc;
        }
        if (money) {
            desc = money;
        }
        if (num == 0) {
            desc = '谢谢参与';
        }
        tmpLuckyEgg.prize = desc;
        this.setData({
            luckyEgg: tmpLuckyEgg,
        });
    },
    toAgreement: function () {
        wx.navigateTo({
            url: '/pages/agreement/agreement'
        });
    },
});
```

## File: pages/nyn/nyn.json
```json
{
  "navigationBarTitleText": "扭一扭",
  "usingComponents": {
    "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
  },
  "disableScroll": true
}
```

## File: pages/nyn/nyn.wxml
```
<view class="nynContainer {{gameStatus === 3 ? 'rankShow' : ''}}">
    <view class="bgArea">
        <image src="https://static.hudongmiao.com/joymewMp/nyn/bg-01.png" class="bg" mode="widthFix"></image>
        <image src="https://static.hudongmiao.com/joymewMp/nyn/star-01.png" class="star"></image>
        <image src="https://static.hudongmiao.com/joymewMp/nyn/dotFall-01.png" class="dotFall"></image>
    </view>
    <!-- 等待界面 -->
    <view class="waitContainer" wx:if="{{gameStatus === 1}}">
        <view class="prizePool">
            <image src="https://static.hudongmiao.com/joymewMp/nyn/marquee.png" class="bg"></image>
            <view class="ct">
                奖池总金额
                <text class="money">{{poolMoney}}元</text>
            </view>
        </view>
        <image src="https://static.hudongmiao.com/joymewMp/nyn/ruleBox-02.png" class="ruleBox"></image>
        <view class="gameBox">
            <image src="https://static.hudongmiao.com/joymewMp/nyn/stageNew2-01.png" class="gameBoxImg"></image>
            <view class="tip">
                购买任意一款弹幕礼物，将
                <text class="strong">免费赠送</text>
                一次抽奖
            </view>
            <view class="startBtn" bindtap="toGame">开始</view>
            <image src="https://static.hudongmiao.com/joymewMp/nyn/dmGift.png" class="dmGiftTitle"></image>
            <view class="giftListWrap">
                <view class="giftItem">
                    <image src="https://static.hudongmiao.com/joymewMp/nyn/locat.png" class="locatImg"></image>
                    <view class="giftImgList">
                        <view class="giftImg g{{index+1}}" wx:for="{{giftList}}" wx:key="id">
                            <image src="{{item.imgUrl}}"></image>
                        </view>
                    </view>
                </view>
            </view>
        </view>
    </view>
    <!-- 扭一扭界面 -->
    <view class="gameContainer" wx:if="{{gameStatus === 2}}">
        <view class="rechargeTipWarp {{rechargeTipAni}}" wx:if="{{isRechargeTipShow}}">
            <span class="star">*</span>
            <span>{{user.nickname}}</span>
            充值了
            <span>{{user.money}}元</span>
        </view>
        <view class="eggBoxWrap" style="background-image:url('https://static.hudongmiao.com/joymewMp/nyn/eggBox.png')">
            <view class="prizePool">
                奖池总金额
                <view class="price">{{poolMoney}}元</view>
            </view>
            <view class="countDown">倒计时: {{countDownNum}}s</view>
            <view class="eggs">
                <view class="eggItem {{item.isFallAni?'fallAni':''}} {{item.aroundAni}}" wx:for="{{eggList}}" wx:key="index" style="width:{{item.width}}rpx;height:{{item.height}}rpx;left:{{item.left}}rpx;bottom:{{item.bottom}}rpx;animation-delay:{{item.fallAniDelay}}s">
                    <view class="egg {{item.isRotateAni?'rotateAni':''}}" style="animation-delay:{{item.rotateAniDelay}}s">
                        <view class="hb">
                            <text>{{item.prize}}</text>
                        </view>
                        <image src="{{item.imgUrl}}" class="eggImg"></image>
                    </view>
                </view>
            </view>
        </view>
        <view class="gameBox">
            <image src="https://static.hudongmiao.com/joymewMp/nyn/stageNew2-01.png" class="gameBoxImg"></image>
            <!-- <view class="tip" wx:if="{{giftListShow}}">
                购买任意一款弹幕礼物，将
                <text class="strong">免费赠送</text>
                一次抽奖
            </view> -->
            <view class="agreement" bindtap='toAgreement' wx:if="{{giftListShow}}">阅读并同意《充值服务协议》</view>
            <view class="giftListWrap" wx:if="{{giftListShow}}">
                <view class="giftItem">
                    <image src="https://static.hudongmiao.com/joymewMp/nyn/locat.png" class="locatImg"></image>
                    <view class="giftImgList">
                        <view class="giftImg g{{index+1}} {{item.isChoosed?'choosed':''}}" wx:for="{{giftList}}" wx:key="id" data-id="{{item.id}}" bindtap='chooseGift'>
                            <image src="https://static.hudongmiao.com/joymewMp/nyn/light2.png" class="lightImage lightAni" wx:if="{{item.isChoosed}}"></image>
                            <image src="{{item.imgUrl}}" class="giftImage"></image>
                        </view>
                    </view>
                </view>
            </view>
            <view class="startBtn" bindtap="handleStartBtnTap">{{btnText}}</view>
            <image src="https://static.hudongmiao.com/joymewMp/nyn/dmGift.png" class="dmGiftTitle" wx:if="{{giftListShow}}"></image>
            <view class="eggExit" wx:if="{{!giftListShow}}">
                <view class="luckyEggWrap">
                    <view class="luckyEgg {{luckyEgg.isFallLuckyAni?'fallLuckyAni':''}}" style="width: {{luckyEgg.width}}rpx;height: {{luckyEgg.height}}rpx;top: {{luckyEgg.top}}rpx;left: {{luckyEgg.left}}rpx;transform: translateY({{luckyEgg.end}}rpx)">
                        <view class="egg {{luckyEgg.isRotateAni?'rotateAni':''}}">
                            <view class="hb">
                                <text>{{luckyEgg.prize}}</text>
                            </view>
                            <image src="{{luckyEgg.imgUrl}}" class="eggImg"></image>
                        </view>
                    </view>
                </view>
            </view>
        </view>
        <view class="resultTipWarp {{resultTipAni}}" wx:if="{{isResultTipShow}}" style="padding-top:{{resultTipContent.ptVal}}rpx">
            <image class="bg" src="{{resultTipContent.resultImgSrc}}"></image>
            <view class="para1">{{resultTipContent.para1}}</view>
            <view class="para2">{{resultTipContent.para2}}</view>
        </view>
    </view>
    <!-- 扭一扭排行榜界面 -->
    <view class="rankContainer" wx:if="{{gameStatus === 3}}">
        <view class="topThree">
            <view class="second" wx:if="{{topRankList[1]}}">
                <image src="https://static.hudongmiao.com/joymewMp/nyn/secondRankBox1.png" class="rkSecond" mode="widthFix"></image>
                <image src="https://static.hudongmiao.com/joymewMp/nyn/rkSecondStage-01.png" class="rkSecondStage" mode="widthFix"></image>
                <view class="headImgBox">
                    <image src="{{topRankList[1].headimgurl}}" class="headImg"></image>
                </view>
                <view class="name">{{topRankList[1].nickname}}</view>
                <view class="money">{{topRankList[1].money}}元</view>
            </view>
            <view class="first" wx:if="{{topRankList[0]}}">
                <image src="https://static.hudongmiao.com/joymewMp/nyn/firstRankBox1.png" class="rkFirst" mode="widthFix"></image>
                <image src="https://static.hudongmiao.com/joymewMp/nyn/rkFirstStage-01.png" class="rkFirstStage" mode="widthFix"></image>
                <view class="headImgBox">
                    <image src="{{topRankList[0].headimgurl}}" class="headImg"></image>
                </view>
                <view class="name">{{topRankList[0].nickname}}</view>
                <view class="money">{{topRankList[0].money}}元</view>
            </view>
            <view class="third" wx:if="{{topRankList[2]}}">
                <image src="https://static.hudongmiao.com/joymewMp/nyn/thirdRankBox1.png" class="rkThird" mode="widthFix"></image>
                <image src="https://static.hudongmiao.com/joymewMp/nyn/rkThirdStage-01.png" class="rkThirdStage" mode="widthFix"></image>
                <view class="headImgBox">
                    <image src="{{topRankList[2].headimgurl}}" class="headImg"></image>
                </view>
                <view class="name">{{topRankList[2].nickname}}</view>
                <view class="money">{{topRankList[2].money}}</view>
            </view>
        </view>
        <view class="other">
            <view class="otherItem" wx:for="{{otherRankList}}" wx:key="index">
                <view class="num">{{ item.num }}</view>
                <image src="{{item.headimgurl}}" class="headImg" mode="widthFix"></image>
                <view class="name">{{item.nickname}}</view>
                <view class="money">{{item.money}}元</view>
            </view>
        </view>
    </view>
    <!-- 反馈入口 -->
    <feedbackEntry userId="{{userId}}"></feedbackEntry>
</view>
```

## File: pages/nyn/nyn.wxss
```
.nynContainer {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}

.nynContainer.rankShow {
  overflow: unset;
}

/* 公共背景区域 */
.nynContainer>.bgArea {
  width: 100%;
  position: absolute;
}

.nynContainer>.bgArea>.bg {
  width: 100%;
  height: 100%;
  position: absolute;
}

.nynContainer>.bgArea>.star {
  position: absolute;
  width: 100%;
  height: 267rpx;
  top: 0;
}

.nynContainer>.bgArea>.dotFall {
  position: absolute;
  width: 100%;
  height: 663rpx;
  top: 266rpx;
}

/* 等待界面 */
.nynContainer>.waitContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.nynContainer>.waitContainer>.prizePool {
  position: absolute;
  top: 25rpx;
  width: 529rpx;
  height: 119rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
}

.nynContainer>.waitContainer>.prizePool>.bg {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}

.nynContainer>.waitContainer>.prizePool>.ct {
  font-size: 37rpx;
  font-weight: 500;
  color: #FFFFFF;
  text-shadow: 0px 2px 2px rgba(209, 41, 41, 0.5);
  position: absolute;
}

.nynContainer>.waitContainer>.prizePool>.ct>.money {
  font-size: 37rpx;
  font-weight: 500;
  color: #FFEAC2;
  text-shadow: 0px 2px 2px rgba(209, 41, 41, 0.5);
  margin-left: 22rpx;
}

.nynContainer>.waitContainer>.ruleBox {
  width: 658rpx;
  height: 622rpx;
  position: absolute;
  bottom: 516rpx;
}

.nynContainer>.waitContainer>.gameBox {
  width: 769rpx;
  height: 548rpx;
  position: absolute;
  bottom: -33rpx;
  display: flex;
  justify-content: center;
}

.nynContainer>.waitContainer>.gameBox>.gameBoxImg {
  position: absolute;
  width: 100%;
  height: 100%;
}

.nynContainer>.waitContainer>.gameBox>.tip {
  font-size: 27rpx;
  font-weight: 500;
  color: #FFFDF0;
  position: absolute;
  top: 29rpx;
}

.nynContainer>.waitContainer>.gameBox>.tip>.strong {
  color: #F7D063;
}

.nynContainer>.waitContainer>.gameBox>.startBtn {
  font-size: 38rpx;
  color: #FFFFFF;
  width: 282rpx;
  height: 92rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 64rpx;
}

.nynContainer>.waitContainer>.gameBox>.dmGiftTitle {
  position: absolute;
  top: 277rpx;
  width: 358rpx;
  height: 83rpx;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap {
  position: absolute;
  top: 364rpx;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem {
  width: 512rpx;
  height: 136rpx;
  position: relative;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.locatImg {
  width: 100%;
  height: 100%;
  position: absolute;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList {
  position: absolute;
  width: 100%;
  height: 100%;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg {
  height: 133rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.g1 {
  left: 16rpx;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.g2 {
  left: 203rpx;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.g3 {
  left: 389rpx;
}

.nynContainer>.waitContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg>image {
  width: 108rpx;
  height: 108rpx;
}

/* 扭一扭界面 */
.nynContainer>.gameContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.nynContainer>.gameContainer>.rechargeTipWarp {
  position: absolute;
  left: 0;
  top: 20rpx;
  padding-left: 30rpx;
  padding-right: 30rpx;
  height: 64rpx;
  border-radius: 32rpx;
  background-color: #cd2bfb;
  color: #ffe590;
  font-size: 24rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
}

.nynContainer>.gameContainer>.rechargeTipWarp>.star {
  margin-top: 8rpx;
  margin-right: 8rpx;
}

.nynContainer>.gameContainer>.eggBoxWrap>.prizePool {
  width: 474rpx;
  height: 117rpx;
  background-image: linear-gradient(180deg, #FF908A 0%, #FF7876 6%, #E1525D 100%);
  box-shadow: 0rpx 10rpx 3rpx 0rpx rgba(255, 249, 242, 0.31);
  border-radius: 11rpx;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 36rpx;
  font-weight: 500;
  color: #FFFFFF;
  text-shadow: 0px 1rpx 1rpx rgba(209, 41, 41, 0.5);
  top: -122rpx;
  position: absolute;
  z-index: 1;
}

.nynContainer>.gameContainer>.eggBoxWrap>.prizePool>.price {
  font-size: 36rpx;
  font-family: PingFang-SC-Heavy, PingFang-SC;
  font-weight: 800;
  color: #FDEAB0;
  text-shadow: 0px 1rpx 1rpx rgba(209, 41, 41, 0.5);
  margin-left: 10rpx;
}

.nynContainer>.gameContainer>.eggBoxWrap>.countDown {
  width: 264rpx;
  height: 66rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/nyn/marquee.png');
  background-size: 100% 100%;
  position: absolute;
  top: 16rpx;
  font-size: 28rpx;
  font-weight: 800;
  color: #FDEAB0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nynContainer>.gameContainer>.eggBoxWrap {
  position: relative;
  width: 658rpx;
  height: 611rpx;
  margin-top: -11rpx;
  background-size: 100% 100%;
  position: absolute;
  bottom: 453rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.nynContainer>.gameContainer>.eggBoxWrap>.eggs {
  position: absolute;
  width: 557rpx;
  height: 449rpx;
  top: 81rpx;
  left: 51rpx;
  overflow: hidden;
}

.nynContainer>.gameContainer>.eggBoxWrap>.eggs>.eggItem {
  position: absolute;
}

.nynContainer>.gameContainer>.eggBoxWrap>.eggs>.eggItem>.egg {
  position: absolute;
  width: 100%;
  height: 100%;
}

.nynContainer>.gameContainer>.eggBoxWrap>.eggs>.eggItem>.egg>.hb {
  width: 80rpx;
  height: 94rpx;
  position: absolute;
  left: 29rpx;
  top: 18rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/nyn/hb01.png');
  background-size: 100% 100%;
  display: flex;
  justify-content: center;
}

.nynContainer>.gameContainer>.eggBoxWrap>.eggs>.eggItem>.egg>.hb>text {
  font-size: 24rpx;
  font-weight: bold;
  text-shadow: 0px 1px 2px rgba(0, 0, 0, 0.5);
  color: #ffffff;
  position: absolute;
  top: 24rpx;
  white-space: nowrap;
}

.nynContainer>.gameContainer>.eggBoxWrap>.eggs>.eggItem>.egg>.eggImg {
  position: absolute;
  width: 100%;
  height: 100%;
}

.nynContainer>.gameContainer>.gameBox {
  width: 769rpx;
  height: 548rpx;
  position: absolute;
  bottom: -34rpx;
  display: flex;
  justify-content: center;
}

.nynContainer>.gameContainer>.gameBox>.gameBoxImg {
  position: absolute;
  width: 100%;
  height: 100%;
}

.nynContainer>.gameContainer>.gameBox>.tip {
  font-size: 27rpx;
  font-weight: 500;
  color: #FFFDF0;
  position: absolute;
  top: 30rpx;
}
.nynContainer>.gameContainer>.gameBox>.agreement {
  font-size: 24rpx;
  font-weight: 400;
  color: #fff;
  position: absolute;
  top: 30rpx;
}
.nynContainer>.gameContainer>.gameBox>.tip.strong {
  color: #F7D063;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap {
  position: absolute;
  top: 364rpx;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem {
  width: 512rpx;
  height: 136rpx;
  position: relative;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.locatImg {
  width: 100%;
  height: 100%;
  position: absolute;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList {
  position: absolute;
  width: 100%;
  height: 100%;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg {
  height: 115rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  margin-top: 12rpx;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.g1 {
  left: 69rpx;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.g2 {
  left: 259rpx;
}

.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.g3 {
  left: 444rpx;
}
.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.choosed {
  background-color: #e04b4e;
  border: 2rpx solid #e04b4e;
}
.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg>.giftImage {
  width: 108rpx;
  height: 108rpx;
  position: absolute;
}
.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg>.lightImage {
  width: 200rpx;
  height: 200rpx;
  position: absolute;
}
.nynContainer>.gameContainer>.gameBox>.giftListWrap>.giftItem>.giftImgList>.giftImg.choosed>.giftImage {
  width: 108rpx;
  height: 108rpx;
  transform: scale(1.4);
}

.nynContainer>.gameContainer>.gameBox>.startBtn {
  font-size: 38rpx;
  color: #FFFFFF;
  width: 282rpx;
  height: 92rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 66rpx;
}

.nynContainer>.gameContainer>.gameBox>.dmGiftTitle {
  position: absolute;
  top: 270rpx;
  width: 358rpx;
  height: 83rpx;
}

.nynContainer>.gameContainer>.gameBox>.eggExit {
  width: 223rpx;
  height: 262rpx;
  position: absolute;
  background-image: url('https://static.hudongmiao.com/joymewMp/nyn/chukou.png');
  background-size: 100% 100%;
  top: 253rpx;
  left: 58rpx;
}

.nynContainer>.gameContainer>.gameBox>.eggExit>.luckyEggWrap {
  position: absolute;
  width: 177rpx;
  height: 213rpx;
  top: 26rpx;
  left: 22rpx;
  overflow: hidden;
}

.nynContainer>.gameContainer>.gameBox>.eggExit>.luckyEggWrap>.luckyEgg {
  position: absolute;
  left: 41rpx;
  top: -110rpx;
}

.nynContainer>.gameContainer>.gameBox>.eggExit>.luckyEggWrap>.luckyEgg>.egg {
  position: absolute;
  width: 100%;
  height: 100%;
}
.nynContainer>.gameContainer>.gameBox>.eggExit>.luckyEggWrap>.luckyEgg>.egg>.hb {
  width: 53rpx;
  height: 65rpx;
  position: absolute;
  left: 40rpx;
  top: 40rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/nyn/hb01.png');
  background-size: 100% 100%;
  display: flex;
  justify-content: center;
}

.nynContainer>.gameContainer>.gameBox>.eggExit>.luckyEggWrap>.luckyEgg>.egg>.hb>text {
  font-size: 13rpx;
  font-weight: bold;
  text-shadow: 0px 1px 2px rgba(0, 0, 0, 0.5);
  color: #FEDA80;
  position: absolute;
  top: 30rpx;
  white-space: nowrap;
}

.nynContainer>.gameContainer>.gameBox>.eggExit>.luckyEggWrap>.luckyEgg>.egg>.eggImg {
  width: 100%;
  height: 100%;
  position: absolute;
}

.nynContainer>.gameContainer>.resultTipWarp {
  width: 586rpx;
  height: 269rpx;
  position: absolute;
  right: 66rpx;
  top: 342rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding-left: 157rpx;
  padding-top: 44rpx;
}

.nynContainer>.gameContainer>.resultTipWarp>.bg {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}

.nynContainer>.gameContainer>.resultTipWarp>.para1 {
  color: #ffffff;
  font-size: 36rpx;
  font-weight: bold;
  position: relative;
}

.nynContainer>.gameContainer>.resultTipWarp>.para2 {
  color: #ffffff;
  font-size: 32rpx;
  font-weight: bold;
  margin-top: 5rpx;
  position: relative;
}

.nynContainer>.gameContainer .rechargeTipAni {
  animation: rechargeTipAni 1s ease-out;
}

.nynContainer>.gameContainer .rechargeTipAni2 {
  animation: rechargeTipAni2 1s ease-out;
}

.nynContainer>.gameContainer .resultTipAni {
  animation: resultTipAni 1s ease-out;
}

.nynContainer>.gameContainer .resultTipAni2 {
  animation: resultTipAni2 1s ease-out;
}

@keyframes rechargeTipAni {
  from {
    transform: translateX(-100rpx);
  }

  to {
    transform: translateX(0rpx);
  }
}

@keyframes rechargeTipAni2 {
  from {
    transform: translateY(0);
    opacity: 1;
  }

  to {
    transform: translateY(-80rpx);
    opacity: 0;
  }
}

@keyframes resultTipAni {
  from {
    transform: translateX(200rpx);
  }

  to {
    transform: translateX(0rpx);
  }
}

@keyframes resultTipAni2 {
  from {
    transform: translateY(0);
    opacity: 1;
  }

  to {
    transform: translateY(-80rpx);
    opacity: 0;
  }
}

/* 排行榜界面 */
.nynContainer>.rankContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.nynContainer>.rankContainer>.topThree {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 0rpx;
}

.nynContainer>.rankContainer>.topThree>.second {
  width: 205rpx;
  height: 377rpx;
  position: relative;
}

.nynContainer>.rankContainer>.topThree>.second>.rkSecond {
  width: 205rpx;
  height: 230rpx;
  position: absolute;
  top: 76rpx;
  z-index: 2;

}

.nynContainer>.rankContainer>.topThree>.second>.rkSecondStage {
  width: 204rpx;
  height: 456rpx;
  position: absolute;
  top: 190rpx;
}

.nynContainer>.rankContainer>.topThree>.second>.headImgBox {
  width: 160rpx;
  height: 160rpx;
  border-radius: 50%;
  overflow: hidden;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  left: 23rpx;
  top: 103rpx;
  z-index: 1;
}

.nynContainer>.rankContainer>.topThree>.second>.headImgBox>.headImg {
  width: 135rpx;
  height: 135rpx;
  border-radius: 50%;
  position: absolute;
  top: 14rpx;
}

.nynContainer>.rankContainer>.topThree>.second>.name {
  font-size: 28rpx;
  color: #FFFFFF;
  width: 100%;
  position: absolute;
  top: 359rpx;
  text-align: center;
}

.nynContainer>.rankContainer>.topThree>.second>.money {
  font-size: 28rpx;
  color: #FFF2B4;
  width: 100%;
  position: absolute;
  top: 413rpx;
  text-align: center;
}

.nynContainer>.rankContainer>.topThree>.first {
  width: 257rpx;
  height: 471rpx;
  position: relative;
}

.nynContainer>.rankContainer>.topThree>.first>.rkFirst {
  width: 250rpx;
  height: 267rpx;
  position: absolute;
  z-index: 2;
}

.nynContainer>.rankContainer>.topThree>.first>.rkFirstStage {
  width: 204rpx;
  height: 593rpx;
  position: absolute;
  left: 26rpx;
  top: 139rpx;
}

.nynContainer>.rankContainer>.topThree>.first>.headImgBox {
  width: 183rpx;
  height: 180rpx;
  border-radius: 50%;
  overflow: hidden;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  left: 36rpx;
  top: 17rpx;
  z-index: 1;
}

.nynContainer>.rankContainer>.topThree>.first>.headImgBox>.headImg {
  width: 156rpx;
  height: 156rpx;
  border-radius: 50%;
  position: absolute;
  top: 27rpx;
}

.nynContainer>.rankContainer>.topThree>.first>.name {
  font-size: 28rpx;
  color: #FFFFFF;
  width: 100%;
  position: absolute;
  top: 304rpx;
  text-align: center;
}

.nynContainer>.rankContainer>.topThree>.first>.money {
  font-size: 28rpx;
  color: #FFF2B4;
  width: 100%;
  position: absolute;
  top: 356rpx;
  text-align: center;
}

.nynContainer>.rankContainer>.topThree>.third {
  width: 191rpx;
  height: 367rpx;
  position: relative;
}

.nynContainer>.rankContainer>.topThree>.third>.rkThird {
  width: 188rpx;
  height: 202rpx;
  position: absolute;
  z-index: 2;
  top: 115rpx;
}

.nynContainer>.rankContainer>.topThree>.third>.rkThirdStage {
  width: 192rpx;
  height: 431rpx;
  position: absolute;
  top: 194rpx;
  left: 0rpx;
}

.nynContainer>.rankContainer>.topThree>.third>.headImgBox {
  width: 160rpx;
  height: 160rpx;
  border-radius: 50%;
  overflow: hidden;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  left: 14rpx;
  top: 103rpx;
  z-index: 1;
}

.nynContainer>.rankContainer>.topThree>.third>.headImgBox>.headImg {
  width: 135rpx;
  height: 135rpx;
  border-radius: 50%;
  position: absolute;
  top: 19rpx;
}

.nynContainer>.rankContainer>.topThree>.third>.name {
  font-size: 28rpx;
  color: #FFFFFF;
  width: 100%;
  position: absolute;
  top: 359rpx;
  text-align: center;
}

.nynContainer>.rankContainer>.topThree>.third>.money {
  font-size: 28rpx;
  color: #FFF2B4;
  width: 100%;
  position: absolute;
  top: 413rpx;
  text-align: center;
}

.nynContainer>.rankContainer>.other {
  width: 670rpx;
  height: 978rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/nyn/rkBox-01.png');
  background-size: 100% 100%;
  position: absolute;
  z-index: 2;
  top:430rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 51rpx;
}

.nynContainer>.rankContainer>.other>.otherItem {
  width: 548rpx;
  height: 112rpx;
  border-bottom: 1rpx solid rgba(255, 255, 255, 0.5);
  width: 494rpx;
  align-items: center;
  position: relative;
  display: flex;
}

.nynContainer>.rankContainer>.other>.otherItem>.num {
  font-size: 34rpx;
  color: #FFFFFF;
}

.nynContainer>.rankContainer>.other>.otherItem>.headImg {
  width: 64rpx;
  height: 64rpx;
  margin-left: 15rpx;
  border-radius: 50%;
}

.nynContainer>.rankContainer>.other>.otherItem>.name {
  font-size: 30rpx;
  color: #FFFFFF;
  position: absolute;
  left: 154rpx;
}

.nynContainer>.rankContainer>.other>.otherItem>.money {
  font-size: 28rpx;
  color: #FFF2B4;
  position: absolute;
  right: 16rpx;
}

.fallAni {
  animation: fallAni 1s linear backwards;
}

.fallLuckyAni {
  animation: fallLuckyAni 1s linear backwards;
}

.rotateAni {
  animation: rotateAni 1s linear backwards infinite;
}
.lightAni {
  animation: lightAni 1s linear backwards infinite;
}
.aroundAni1 {
  animation: aroundAni1 2s linear infinite;
}

.aroundAni2 {
  animation: aroundAni2 2s linear infinite;
}

.aroundAni3 {
  animation: aroundAni3 2s linear infinite;
}

.aroundAni4 {
  animation: aroundAni4 2s linear infinite;
}

.aroundAni5 {
  animation: aroundAni5 2s linear infinite;
}

.aroundAni6 {
  animation: aroundAni6 2s linear infinite;
}

.aroundAni7 {
  animation: aroundAni7 2s linear infinite;
}

.aroundAni8 {
  animation: aroundAni8 2s linear infinite;
}
@keyframes fallLuckyAni {
  0% {
    transform: translateY(0);
  }

  40% {
    transform: translateY(208rpx);
  }

  50% {
    transform: translateY(150rpx);
  }

  60% {
    transform: translateY(208rpx);
  }

  70% {
    transform: translateY(175rpx);
  }

  80% {
    transform: translateY(208rpx);
  }

  90% {
    transform: translateY(199rpx);
  }

  100% {
    transform: translateY(208rpx);
  }
}

@keyframes fallAni {
  0% {
    transform: translateY(-300%);
    opacity: 0;
  }

  5% {
    transform: translateY(-300%);
  }

  15% {
    transform: translateY(0);
  }

  30% {
    transform: translateY(-100%);
  }

  40% {
    transform: translateY(0%);
  }

  50% {
    transform: translateY(-60%);
  }

  70% {
    transform: translateY(0%);
  }

  80% {
    transform: translateY(-30%);
  }

  90% {
    transform: translateY(0%);
  }

  95% {
    transform: translateY(-14%);
  }

  97% {
    transform: translateY(0%);
  }

  99% {
    transform: translateY(-6%);
  }

  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes rotateAni {
  0% {
    transform: rotate(0);
  }

  100% {
    transform: rotate(360deg);
  }
}

@keyframes aroundAni1 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(299rpx, -150rpx);
  }

  40% {
    transform: translate(100rpx, -300rpx);
  }

  60% {
    transform: translate(-115rpx, -150rpx);
  }

  80% {
    transform: translate(-85rpx, -52rpx);
  }

  100% {
    transform: translate(185rpx, -152rpx);
  }
}

@keyframes aroundAni2 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(158rpx, -222rpx);
  }

  40% {
    transform: translate(60rpx, -18rpx);
  }

  60% {
    transform: translate(-200rpx, -230rpx);
  }

  80% {
    transform: translate(-255rpx, -32rpx);
  }

  100% {
    transform: translate(0rpx, -132rpx);
  }
}

@keyframes aroundAni3 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(-360rpx, -185rpx);
  }

  40% {
    transform: translate(25rpx, -10rpx);
  }

  60% {
    transform: translate(-125rpx, -210rpx);
  }

  80% {
    transform: translate(-392rpx, -100rpx);
  }

  100% {
    transform: translate(-50rpx, 15rpx);
  }
}

@keyframes aroundAni4 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(416rpx, -162rpx);
  }

  40% {
    transform: translate(120rpx, -180rpx);
  }

  60% {
    transform: translate(0rpx, 20rpx);
  }

  80% {
    transform: translate(416rpx, -163rpx);
  }

  100% {
    transform: translate(216rpx, 76rpx);
  }
}

@keyframes aroundAni5 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(292rpx, -108rpx);
  }

  40% {
    transform: translate(30rpx, 132rpx);
  }

  60% {
    transform: translate(-125rpx, -110rpx);
  }

  80% {
    transform: translate(150rpx, -132rpx);
  }

  100% {
    transform: translate(290rpx, 60rpx);
  }
}

@keyframes aroundAni6 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(152rpx, -85rpx);
  }

  40% {
    transform: translate(-263rpx, 105rpx);
  }

  60% {
    transform: translate(152rpx, -50rpx);
  }

  80% {
    transform: translate(-160rpx, -100rpx);
  }

  100% {
    transform: translate(-263rpx, 105rpx);
  }
}

@keyframes aroundAni7 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(-412rpx, -55rpx);
  }

  40% {
    transform: translate(-190rpx, 196rpx);
  }

  60% {
    transform: translate(6rpx, -40rpx);
  }

  80% {
    transform: translate(-300rpx, -70rpx);
  }

  100% {
    transform: translate(-410rpx, 136rpx);
  }
}

@keyframes aroundAni8 {
  0% {
    transform: translate(0rpx, 0rpx);
  }

  20% {
    transform: translate(300rpx, -44rpx);
  }

  40% {
    transform: translate(408rpx, 90rpx);
  }

  60% {
    transform: translate(70rpx, 170rpx);
  }

  80% {
    transform: translate(270rpx, -40rpx);
  }

  100% {
    transform: translate(408rpx, 136rpx);
  }
}
@keyframes lightAni {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@media screen and (max-height: 580px) {
  .nynContainer>.waitContainer>.ruleBox {
    bottom: 433rpx;
  }
}

@media screen and (min-height: 720px) {
  .nynContainer>.gameContainer>.title {
    top: 65rpx;
  }
}
```

## File: pages/pay/pay.js
```javascript
import {
  diamondRecharge,
  sendGift,
  sendGiftBroadCast,
  sendGiftGameRecharge,
  sendSuperDanmuRecharge,
} from '../../api/recharge/recharge';
import { wxPay } from '../../api/pay';
import { timeoutTask, showWxToast } from '../../utils/index';
import { setOrigin } from '../../utils/storage';
const app = getApp();

Page({
  /**
     * 页面的初始数据
     */
  data: {
    total: 0,
    userId: '',
    openId: '',
    origin: '',
    recommendGiftId: '',
    giftconst: '',
    giftText: '',
  },

  /**
     * 生命周期函数--监听页面加载
     */
  onLoad: function(options) {
    if (options.total) {
      this.setData({
        total: options.total,
      });
    }
    if (options.userId) {
      this.setData({
        userId: options.userId,
      });
    }
    if (options.openId) {
      this.setData({
        openId: options.openId,
      });
    }
    if (options.origin) {
      this.setData({
        origin: options.origin,
      });
    }
    if (this.data.origin === 'sendRecommendGift') {
      this.setData({
        recommendGiftId: options.giftId,
      });
      this.sendRecommendGift();
    } else if (this.data.origin === 'sendGiftGame') {
      this.setData({
        giftconst: options.giftconst,
      });
      if (this.data.giftconst === 'text') {
        this.setData({
          giftText: options.content,
        });
      }
      this.sendGiftGame();
    } else if (this.data.origin === 'sendSuperDanmu') {
      this.setData({
        giftconst: options.giftconst,
        giftText: options.content,
      });
      this.sendSuperDanmu();
    } else {
      this.rechargeDiamonds();
    }
  },
  //充值完直接发礼物
  sendRecommendGift: function() {
    diamondRecharge({
      total: this.data.total,
      userId: this.data.userId,
      openId: this.data.openId,
    })
      .then(res => {
        console.log(res);
        return wxPay(res);
      })
      .then(() => {
        return sendGift({
          giftId: this.data.recommendGiftId,
        });
      })
      .then(res2 => {
        console.log(res2);
        if (res2.data.code === 200) {
          showWxToast('喵钻不足!发送失败!');
          timeoutTask(() => {
            wx.navigateBack();
          }, 500);
          return;
        }
        showWxToast('发送成功');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
        return sendGiftBroadCast({
          giftId: this.data.recommendGiftId,
        });
      })
      .catch(err => {
        console.log(err);
        showWxToast('发送失败');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      });
  },
  //充值喵钻
  rechargeDiamonds: function() {
    diamondRecharge({
      total: this.data.total,
      userId: this.data.userId,
      openId: this.data.openId,
    })
      .then(res => {
        console.log(res);
        return wxPay(res);
      })
      .then(() => {
        showWxToast('充值成功');
        app.globalData.isH5NeedRefresh = true;
        if (this.data.origin) {
          setOrigin(this.data.origin);
        }
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      })
      .catch(err => {
        console.log(err);
        showWxToast('充值失败');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      });
  },
  // 送祝福游戏充值并发礼物
  sendGiftGame: function() {
    sendGiftGameRecharge({
      giftconst: this.data.giftconst,
      openid: this.data.openId,
      userId: this.data.userId,
      content: this.data.giftText,
    })
      .then(res => {
        console.log(res);
        return wxPay(res);
      })
      .then(() => {
        showWxToast('发送成功');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      })
      .catch(err => {
        console.log(err);
        showWxToast('发送失败');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      });
  },
  // 充值并发送全屏特效
  sendSuperDanmu: function() {
    sendSuperDanmuRecharge({
      giftconst: this.data.giftconst,
      openid: this.data.openId,
      userId: this.data.userId,
      content: this.data.giftText,
    })
      .then(res => {
        console.log(res);
        return wxPay(res);
      })
      .then(() => {
        showWxToast('发送成功');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      })
      .catch(err => {
        console.log(err);
        showWxToast('发送失败');
        timeoutTask(() => {
          wx.navigateBack();
        }, 500);
      });
  },
});
```

## File: pages/pay/pay.json
```json
{
  "navigationBarTitleText": "支付",
  "disableScroll": true
}
```

## File: pages/pay/pay.wxml
```
<!-- 此页面只用来调起支付 -->
<view></view>
```

## File: pages/photographerWall/photographerWall.js
```javascript
import { getToken, getLiveId } from '../../utils/storage';
import { getCurrentTimestamp } from '../../utils/date';
import  { PAGE_HOST } from '../../assets/constant/host';
const app = getApp();

Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: '现场照片',
    token: ''
  },
  onLoad: function () {
    app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photographerWall`);
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photographerWall`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: app.globalData.activityTitle
    });
  },
  onShow: function () {
    if (app.globalData.isH5NeedRefresh) {
      console.log('***h5 needRefresh***');
      app.globalData.isH5NeedRefresh = false;
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photographerWall`);
      this.setData({
        h5Url: app.globalData.h5Url,
      });
    }
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: '/pages/joymewIndex/joymewIndex?liveId=' + this.data.liveId,
    };
  },
})
```

## File: pages/photographerWall/photographerWall.json
```json
{
  "navigationBarTitleText": "现场照片"
}
```

## File: pages/photographerWall/photographerWall.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/photographerWall/photographerWall.wxss
```
page {
  background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/photoWall/photoWall.js
```javascript
import { getToken, getLiveId, setLiveId } from '../../utils/storage';
import { getCurrentTimestamp } from '../../utils/date';
import  { PAGE_HOST } from '../../assets/constant/host';
const app = getApp();

Page({
  data: {
    h5Url: '',
    liveId: '',
    activityTitle: '照片墙',
    token: ''
  },
  onLoad: function (options) {
    if (options.liveId && options.token) {
      // 分享进入
      setLiveId(options.liveId);
      app.setH5Url(`${PAGE_HOST}?liveId=${options.liveId}&token=${options.token}&time=${getCurrentTimestamp()}&photoWallShare=1#/photoWall`);
    } else {
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photoWall`);
    }
    console.log(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photoWall`);
    this.setData({
      h5Url: app.globalData.h5Url,
      activityTitle: `照片墙(${app.globalData.activityTitle})`
    });
  },
  onShow: function () {
    if (app.globalData.isH5NeedRefresh) {
      console.log('***h5 needRefresh***');
      app.globalData.isH5NeedRefresh = false;
      app.setH5Url(`${PAGE_HOST}?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photoWall`);
      // app.setH5Url(`https://shm.hudongmiao.com/?liveId=${getLiveId()}&token=${getToken()}&time=${getCurrentTimestamp()}#/photoWall`);
      this.setData({
        h5Url: app.globalData.h5Url,
      });
    }
  },
  onShareAppMessage: function () {
    return {
      title: this.data.activityTitle,
      path: `/pages/photoWall/photoWall?liveId=${getLiveId()}&token=${getToken()}`,
    };
  },
})
```

## File: pages/photoWall/photoWall.json
```json
{
  "navigationBarTitleText": "照片墙"
}
```

## File: pages/photoWall/photoWall.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/photoWall/photoWall.wxss
```
page {
  background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
}
```

## File: pages/recharge/recharge.js
```javascript
import { getGiftRankList, diamondRecharge, becomeVip } from '../../api/recharge/recharge';
import { wxPay } from '../../api/pay';
import { timeoutTask, showWxToast } from '../../utils/index';
import { setAdPopFlag, getAdPopFlag } from '../../utils/storage';

const app = getApp();
let requestLock = false;
// let showVideoAdLock = false;
// 在页面中定义激励视频广告
let videoAd = null
const couponUrl = ['https://static.hudongmiao.com/joymewMp/recharge/coupon.png', 'https://static.hudongmiao.com/joymewMp/recharge/coupon2.png']
Page({
    data: {
        userId: '',
        openId: '',
        moneyInput: '',
        money: 0,
        remainMoney: 0,
        nickname: '',
        headImg: '',
        rechargeList: [],
        activeDesc: '0',
        couponUrl: '',
        activeCouponUrl: '',
        giftRankList: [],
        isVipHeadBoxGetted: false,
        popupModVisible: false,
        isShowBagAni: false,
        isHideBagAni: false,
    },
    onLoad: function (options) {
        this.setData({
            userId: options.userId,
            openId: options.openId,
            remainMoney: options.money,
            rechargeList: options.rechargeListStr.split(','),
            nickname: options.name,
            headImg: options.headImg,
            couponUrl: couponUrl[0],
            activeCouponUrl: couponUrl[1],
            isVipHeadBoxGetted: options.isVipHeadBoxGetted === 'false' ? false : true,
        });
        // showVideoAdLock = false;
        this.getGiftRankList();
        // if (!this.data.isVipHeadBoxGetted) {
        //     if (wx.createRewardedVideoAd) {
        //         let tmpAdPopFlag = getAdPopFlag();
        //         if (!tmpAdPopFlag) {
        //             setAdPopFlag();
        //             // 弹出广告
        //             this.showPopupMod();
        //         }
        //         videoAd = wx.createRewardedVideoAd({
        //             adUnitId: 'adunit-bf5d5ab9f926a2de'
        //         });
        //         videoAd.onLoad(() => {
        //         });
        //         videoAd.onError(() => {
        //             console.log('广告视频加载出错');
        //             showVideoAdLock = false;
        //         });
        //         videoAd.onClose((res) => {
        //             showVideoAdLock = false;
        //             if (res && res.isEnded) {
        //                 console.log('领取奖励')
        //                 // 用户观看完广告视频领取奖励
        //                 becomeVip().then((res) => {
        //                     console.log(res);
        //                     app.globalData.isH5NeedRefresh = true;
        //                     timeoutTask(() => {
        //                         wx.navigateBack();
        //                     }, 1000);
        //                 }).catch((err) => {
        //                     console.log(err);
        //                 })
        //             } else {
        //                 console.log('中途退出，没有奖励!');
        //             }
        //         });
        //     }
        // }
    },
    onShow: function () {
    },
    onUnload: function () {
    },
    chooseMoney: function (e) {
        // 取消money输入区域的输入金额并设置输入的money值
        this.setData({
            moneyInput: '',
            money: e.currentTarget.dataset.desc,
            activeDesc: e.currentTarget.dataset.desc,
        });
        console.log(this.data.money);
    },
    handleMoneyInput: function (e) {
        let tmpMoneyStr = e.detail.value;
        let r = /^\+?[1-9][0-9]*$/;　　//正整数
        let flag = r.test(tmpMoneyStr);
        if (flag || tmpMoneyStr === '0.01') {
            // 只能是正整数或者是0.01
            this.setData({
                money: tmpMoneyStr,
            });
        } else {
            this.setData({
                money: '',
            });
        }
    },
    handleMoneyFocus: function () {
        // 取消money选择区域的active状态
        this.setData({
            activeDesc: '0',
        });
    },
    handleRecharge: function () {
        if (!this.data.money) {
            showWxToast('请输入或者选择充值金额!');
            return;
        }
        if (this.data.money === '0') {
            showWxToast('充值金额不能为0!');
            return;
        }
        this.recharge();
    },
    recharge: function () {
        if (!requestLock) {
            requestLock = true;
            diamondRecharge({
                total: this.data.money,
                userId: this.data.userId,
                openId: this.data.openId,
            }).then((res) => {
                console.log(res);
                return wxPay(res);
            }).then(() => {
                // 前端处理用户余额增加
                const tmpRemainMoney = (parseFloat(this.data.remainMoney) + parseFloat(this.data.money)).toFixed(2);
                this.setData({
                    remainMoney: tmpRemainMoney,
                });
                showWxToast('充值成功!');
                requestLock = false;
                app.globalData.isH5NeedRefresh = true;
                timeoutTask(() => {
                    wx.navigateBack();
                }, 1000);
            }).catch((err) => {
                console.log(err);
                showWxToast('充值失败!');
                requestLock = false;
            });
        }
    },
    getGiftRankList: function () {
        getGiftRankList().then((res) => {
            console.log(res);
            const tmpList = res.data.list;
            const tmpLen = tmpList.length;
            for (let i = 0; i < tmpLen; i += 1) {
                tmpList[i].num = (i + 1) < 10 ? '0' + (i + 1) : i + 1;
                tmpList[i].wx_name = tmpList[i].wx_name.length <= 6 ? tmpList[i].wx_name : tmpList[i].wx_name.substr(0, 6) + '...';
            }
            this.setData({
                giftRankList: tmpList,
            });
        }).catch((err) => {
            console.log(err);
        });
    },
    toAgreement: function () {
        wx.navigateTo({
            url: '/pages/agreement/agreement',
        });
    },
    showPopupMod: function () {
        this.setData({
            popupModVisible: true,
            isShowBagAni: true,
        });
        timeoutTask(() => {
            this.setData({
                isShowBagAni: false,
            });
        }, 300);
    },
    hidePopupMod: function () {
        this.setData({
            isHideBagAni: true,
        });
        timeoutTask(() => {
            this.setData({
                isHideBagAni: false,
                popupModVisible: false,
            });
        }, 300);
    },
    toGetHeadImgBox: function () {
        if (showVideoAdLock) {
            return;
        }
        // 用户触发广告后，显示激励视频广告
        if (videoAd) {
            showVideoAdLock = true;
            this.hidePopupMod();
            videoAd.show().catch(() => {
                // 失败重试
                videoAd.load()
                    .then(() => videoAd.show())
                    .catch(err => {
                        console.log('激励视频 广告显示失败');
                        showVideoAdLock = false;
                    })
            })
        }
    }
});
```

## File: pages/recharge/recharge.json
```json
{
  "navigationBarTitleText": "充值中心",
  "usingComponents": {
    "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
  }
}
```

## File: pages/recharge/recharge.wxml
```
<view class="rechargeContainer">
  <image src="https://static.hudongmiao.com/joymewMp/recharge/bg-01.png" class="bg" mode="widthFix"></image>
  <image src="{{headImg}}" class="headImg"></image>
  <view class="nickname">{{nickname}}</view>
  <view class="remain">
    <image src="https://static.hudongmiao.com/joymewMp/recharge/diamonds.png" class="diamondIcon"></image>
    <view class="remainMoney">{{remainMoney}}</view>
  </view>
  <!-- 自定义充值区域 -->
  <view class="customRechargeArea">
    <view class="title">充值金额</view>
    <input placeholder="自定义充值金额" type="number" maxlength="4" value="{{moneyInput}}" bindinput="handleMoneyInput" bindfocus="handleMoneyFocus" />
  </view>
  <!-- 固定充值金额区域 -->
  <view class="limitRechargeArea">
    <view class="rechargeItem" style="background-image:url('{{activeDesc === item ? activeCouponUrl : couponUrl}}')" wx:for="{{rechargeList}}" wx:key="index" data-desc="{{item}}" bindtap="chooseMoney">
      <image src="https://static.hudongmiao.com/joymewMp/recharge/diamonds.png" class="diamondIcon"></image>
      <view class="num {{activeDesc === item?'active':''}}">{{item}}</view>
    </view>
  </view>
  <view class="rechargeBtn" bindtap="handleRecharge">立即充值</view>
  <view class="agreement" bindtap="toAgreement">阅读并同意《充值服务协议》</view>
  <view class="wishSheetTitle">
    <image src="https://static.hudongmiao.com/joymewMp/recharge/loveIcon.png" class="loveIcon"></image>
    <view class="title">祝福榜单</view>
    <image src="https://static.hudongmiao.com/joymewMp/recharge/loveIcon.png" class="loveIcon"></image>
  </view>
  <view class="wishSheetList">
    <view class="item" wx:for="{{giftRankList}}" wx:key="index">
      <view class="leftCt">
        <image src="https://static.hudongmiao.com/joymewMp/recharge/firstMedal.png" class="medalImg" wx:if="{{index === 0}}"></image>
        <image src="https://static.hudongmiao.com/joymewMp/recharge/secondMedal.png" class="medalImg" wx:if="{{index === 1}}"></image>
        <image src="https://static.hudongmiao.com/joymewMp/recharge/thirdMedal.png" class="medalImg" wx:if="{{index === 2}}"></image>
        <view class="num" wx:if="{{index > 2}}">{{item.num}}</view>
        <image src="{{item.avator}}" class="headImg"></image>
        <view class="name">{{item.wx_name}}</view>
      </view>
      <view class="wish">送出价值{{item.size}}个钻礼物</view>
    </view>
  </view>
  <!-- 反馈入口 -->
  <feedbackEntry userId="{{userId}}"></feedbackEntry>
  <!-- 隐私授权弹窗 -->
  <privacyAuthorize></privacyAuthorize>
</view>
```

## File: pages/recharge/recharge.wxss
```
.rechargeContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.rechargeContainer>.bg {
    position: absolute;
    width: 100%;
}

.rechargeContainer>.headImg {
    position: absolute;
    width: 105rpx;
    height: 99rpx;
    top: 102rpx;
}

.rechargeContainer>.getRewardBtn {
    width: 130rpx;
    height: 36rpx;
    background: #FFDB27;
    border-radius: 18rpx 18rpx 18rpx 0rpx;
    position: absolute;
    top: 109rpx;
    right: 167rpx;
    font-size: 18rpx;
    font-weight: bold;
    color: #D8241D;
    display: flex;
    justify-content: center;
    align-items: center;
}

.rechargeContainer>.nickname {
    font-size: 30rpx;
    font-weight: 400;
    color: #FFFFFF;
    position: absolute;
    top: 222rpx;
}

.rechargeContainer>.remain {
    display: flex;
    align-items: center;
    font-size: 34rpx;
    font-weight: 500;
    position: absolute;
    color: #FFFFFF;
    top: 294rpx;
}

.rechargeContainer>.remain>.diamondIcon {
    width: 40rpx;
    height: 32rpx;
    margin-right: 13rpx;
}

.rechargeContainer>.customRechargeArea {
    width: 648rpx;
    height: 184rpx;
    background: #FEE857;
    border-radius: 15rpx 15rpx 0rpx 0rpx;
    position: absolute;
    top: 378rpx;
    display: flex;
    justify-content: center;
}

.rechargeContainer>.customRechargeArea>.title {
    font-size: 24rpx;
    font-weight: 400;
    color: #A24935;
    position: absolute;
    top: 32rpx;
    left: 44rpx;
}

.rechargeContainer>.customRechargeArea>input {
    width: 572rpx;
    height: 66rpx;
    font-size: 32rpx;
    font-weight: 400;
    color: #A24935;
    border-bottom: 1rpx solid rgba(162, 73, 53, 0.3);
    position: absolute;
    top: 78rpx;
}

.rechargeContainer>.limitRechargeArea {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    position: absolute;
    top: 615rpx;
    width: 641rpx;
}

.rechargeContainer>.limitRechargeArea>.rechargeItem {
    width: 187rpx;
    height: 180rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 32rpx 0;
    background-size: 100% 100%;
}

.rechargeContainer>.limitRechargeArea>.rechargeItem>.diamondIcon {
    width: 69rpx;
    height: 55rpx;
}

.rechargeContainer>.limitRechargeArea>.rechargeItem>.num {
    font-size: 55rpx;
    font-weight: 500;
    color: #9C2CF3;
    margin-top: 6rpx;
}

.rechargeContainer>.limitRechargeArea>.rechargeItem>.num.active {
    color: #FFFFFF;
}

.rechargeContainer>.rechargeBtn {
    position: absolute;
    width: 500rpx;
    height: 79rpx;
    border-radius: 6rpx;
    background-image: url('https://static.hudongmiao.com/joymewMp/recharge/btn.png');
    background-size: 100% 100%;
    top: 1101rpx;
    text-align: center;
    line-height: 79rpx;
    font-size: 34rpx;
    font-weight: 500;
    color: #A24935;
}

.rechargeContainer>.agreement {
    font-size: 24rpx;
    font-weight: 500;
    color: #9C2BF3;
    position: absolute;
    top: 1200rpx;
}

.rechargeContainer>.wishSheetTitle {
    display: flex;
    align-items: center;
    position: absolute;
    top: 1288rpx;
    font-size: 36rpx;
    font-weight: 500;
    color: #FFFFFF;
}

.rechargeContainer>.wishSheetTitle>.loveIcon {
    width: 30rpx;
    height: 26rpx;
    margin: 0 30rpx;
}

.rechargeContainer>.wishSheetList {
    position: absolute;
    top: 1355rpx;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #8A1DD3;
}

.rechargeContainer>.wishSheetList>.item {
    width: 695rpx;
    height: 114rpx;
    background: rgba(84, 59, 144, 0.3);
    border-radius: 8rpx;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 35rpx 0 28rpx;
}

.rechargeContainer>.wishSheetList>.item>.leftCt {
    display: flex;
    align-items: center;
}

.rechargeContainer>.wishSheetList>.item>.leftCt>.medalImg {
    width: 39rpx;
    height: 50rpx;
}

.rechargeContainer>.wishSheetList>.item>.leftCt>.headImg {
    width: 64rpx;
    height: 64rpx;
    border-radius: 50%;
    margin: 0 22rpx 0 17rpx;
}

.rechargeContainer>.wishSheetList>.item>.leftCt>.name {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFFFFF;
}

.rechargeContainer>.wishSheetList>.item>.leftCt>.num {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFFFFF;
}

.rechargeContainer>.wishSheetList>.item>.wish {
    font-size: 28rpx;
    font-weight: 400;
    color: #FFF32E;
}

.rechargeContainer>.adContainer {
    position: fixed;
    top: 125rpx;
    right: 8rpx;
    z-index: 2;
}

.rechargeContainer>.popupMod {
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.6);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1;
}

.rechargeContainer>.popupMod>.bagBox {
    width: 670rpx;
    height: 938rpx;
    background-image: url('https://static.joymew.com/joymewMp/adReward/bag.png');
    background-size: 100% 100%;
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.rechargeContainer>.popupMod>.bagBox>.tit {
    font-size: 36rpx;
    font-weight: bold;
    color: #FFFFFF;
    background: linear-gradient(0deg, #F7FED2 0%, #FCED9B 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-top: 404rpx;
    letter-spacing: 2rpx;
}

.rechargeContainer>.popupMod>.bagBox>.headImgBox {
    width: 177rpx;
    height: 155rpx;
    margin-top: 56rpx;
}

.rechargeContainer>.popupMod>.bagBox>.tip {
    font-size: 24rpx;
    font-weight: bold;
    color: #FFFFFF;
    background: linear-gradient(0deg, #F7FED2 0%, #FCED9B 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-top: 40rpx;
}

.rechargeContainer>.popupMod>.bagBox>.getBtn {
    width: 360rpx;
    height: 90rpx;
    background: linear-gradient(166deg, #F5E8CE, #DBB782);
    box-shadow: 2rpx 14rpx 24rpx 0rpx #84010F;
    border-radius: 45rpx;
    margin-top: 24rpx;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 36rpx;
    font-weight: bold;
    color: #6B2B24;
}

.rechargeContainer>.popupMod>.bagBox>.getBtn>.videoIcon {
    width: 44rpx;
    height: 31rpx;
    position: absolute;
    left: 59rpx;
}

.rechargeContainer>.popupMod>.bagBox>.closeIcon {
    width: 82rpx;
    height: 82rpx;
    position: absolute;
    bottom: -60rpx;
}

.showBagAni {
    animation: zoomIn 0.3s linear;
}

.hideBagAni {
    animation: zoomOut 0.3s linear;
}

@keyframes zoomIn {
    from {
        opacity: 0;
        -webkit-transform: scale3d(0.3, 0.3, 0.3);
        transform: scale3d(0.3, 0.3, 0.3);
    }

    50% {
        opacity: 1;
    }
}

@keyframes zoomOut {
    from {
        opacity: 1;
    }

    50% {
        opacity: 0;
        -webkit-transform: scale3d(0.3, 0.3, 0.3);
        transform: scale3d(0.3, 0.3, 0.3);
    }

    to {
        opacity: 0;
    }
}
```

## File: pages/recharge2/recharge2.js
```javascript
import { getRoleGiftRankList, diamondRecharge, becomeVip, wxChooseImage, uploadHeadImg, editUserInfo } from '../../api/recharge/recharge';
import { wxPay } from '../../api/pay';
import { timeoutTask, showWxToast, showWxLoading, hideWxLoading } from '../../utils/index';
import { setAdPopFlag, getAdPopFlag } from '../../utils/storage';

const app = getApp();
let requestLock = false;
// let showVideoAdLock = false;
// 在页面中定义激励视频广告
// let videoAd = null;
Page({
    data: {
        userId: '',
        openId: '',
        money: 0,
        remainMoney: 0,
        nickname: '',
        headImg: '',
        rechargeList: [],
        giftRankListBoy: [],
        giftRankListGirl: [],
        popupModVisible: false,
        isShowBagAni: false,
        isHideBagAni: false,
        deskList: [],
        editPopupVisible: false,
        editPopupAni: false,
        vipLevel: '',
        relativeType: '',
        currentStatus: '',
        editUserInfoPrice: '0',
        deskNum: '',
        statusList: ['伴郎', '伴娘', '单身贵族', '高富帅', '白富美', '钻石王老五'],
        formData: {
            avator: '',
            wx_name: '',
            type: '',
            table_number: '',
            position: '',
        },
    },
    onLoad: function (options) {
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
        this.setData({
            deskList: tmpDeskList,
        });
        this.setData({
            userId: options.userId,
            openId: options.openId,
            remainMoney: options.money,
            rechargeList: options.rechargeListStr.split(','),
            nickname: options.name,
            headImg: options.headImg,
            vipLevel: options.vipLevel,
            relativeType: options.relativeType,
            currentStatus: options.currentStatus,
            editUserInfoPrice: options.editUserInfoPrice,
            deskNum: options.deskNum,
        });
        let tmpFormData = {
            avator: this.data.headImg || '',
            wx_name: this.data.nickname || '',
            type: this.data.relativeType || '',
            table_number: this.data.deskNum || '',
            position: this.data.currentStatus || '',
        };
        this.setData({
            formData: tmpFormData,
        });
        this.getGiftRankList();
    },
    onShow: function () {
    },
    onUnload: function () {
    },
    handleRecharge: function () {
        this.recharge();
    },
    recharge: function (e) {
        if (!requestLock) {
            requestLock = true;
            this.setData({
                money: e.currentTarget.dataset.desc,
            });
            diamondRecharge({
                total: this.data.money,
                userId: this.data.userId,
                openId: this.data.openId,
            }).then((res) => {
                console.log(res);
                return wxPay(res);
            }).then(() => {
                // 前端处理用户余额增加
                const tmpRemainMoney = (parseFloat(this.data.remainMoney) + parseFloat(this.data.money)).toFixed(2);
                this.setData({
                    remainMoney: tmpRemainMoney,
                });
                showWxToast('充值成功!');
                requestLock = false;
                app.globalData.isH5NeedRefresh = true;
            }).catch((err) => {
                console.log(err);
                showWxToast('充值失败!');
                requestLock = false;
            });
        }
    },
    getGiftRankList: function () {
        getRoleGiftRankList().then((res) => {
            console.log('男方女方送礼物榜单');
            console.log(res);
            res.data.list1.map((item) => {
                return {
                    ...item,
                    wx_name: item.wx_name.length > 4 ? item.wx_name.slice(0, 4) + '...' : item.wx_name,
                }
            });
            res.data.list2.map((item) => {
                return {
                    ...item,
                    wx_name: item.wx_name.length > 4 ? item.wx_name.slice(0, 4) + '...' : item.wx_name,
                }
            });
            this.setData({
                giftRankListBoy: res.data.list1,
                giftRankListGirl: res.data.list2,
            });
        }).catch((err) => {
            console.log(err);
        });
    },
    toAgreement: function () {
        wx.navigateTo({
            url: '/pages/agreement/agreement',
        });
    },
    showPopupMod: function () {
        this.setData({
            popupModVisible: true,
            isShowBagAni: true,
        });
        timeoutTask(() => {
            this.setData({
                isShowBagAni: false,
            });
        }, 300);
    },
    hideEditPopup: function () {
        this.setData({
            editPopupAni: false,
        });
        timeoutTask(() => {
            this.setData({
                editPopupVisible: false,
            });
        }, 300);
    },
    showEditPopup: function () {
        this.setData({
            editPopupVisible: true,
        });
        timeoutTask(() => {
            this.setData({
                editPopupAni: true,
            });
        }, 100);
    },
    //上传图片
    upload: function () {
        let tempFilePaths;
        let tmpFormData = this.data.formData;
        wxChooseImage().then((res) => {
            console.log(res);
            tempFilePaths = res.tempFilePaths;
            tmpFormData.avator = tempFilePaths[0];
            this.setData({
                formData: tmpFormData,
            });
        }).catch((err) => {
            console.log(err);
        })
    },
    chooseRelatives: function (e) {
        console.log(e.detail.value);
        let tmpFormData = this.data.formData;
        tmpFormData.type = e.detail.value;
        this.setData({
            formData: tmpFormData,
        });
    },
    handlePickerChange: function (e) {
        console.log(e.detail.value);
        let tmpFormData = this.data.formData;
        tmpFormData.table_number = this.data.deskList[e.detail.value];
        this.setData({
            formData: tmpFormData,
        });
    },
    chooseStatus: function (e) {
        console.log(e.currentTarget.dataset.status);
        let tmpFormData = this.data.formData;
        tmpFormData.position = e.currentTarget.dataset.status;
        this.setData({
            formData: tmpFormData,
        });
    },
    editRecharge: function (cb) {
        diamondRecharge({
            total: this.data.editUserInfoPrice,
            userId: this.data.userId,
            openId: this.data.openId,
        }).then((res) => {
            console.log(res);
            return wxPay(res);
        }).then(() => {
            cb();
        }).catch((err) => {
            console.log(err);
            showWxToast('修改失败!');
        });
    },
    handleNameBlur: function (e) {
        console.log(e.detail.value);
        let tmpFormData = this.data.formData;
        tmpFormData.wx_name = e.detail.value;
        this.setData({
            formData: tmpFormData,
        });
    },
    confirmEdit: function () {
        console.log(this.data.formData);
        let tmpFormData = this.data.formData;
        if (!tmpFormData.avator) {
            showWxToast('头像不能为空!');
            return;
        }
        if (!tmpFormData.wx_name) {
            showWxToast('姓名不能为空!');
            return;
        }
        if (!tmpFormData.type) {
            showWxToast('请选择亲友团!');
            return;
        }
        if (!tmpFormData.table_number) {
            showWxToast('请选择桌号!');
            return;
        }
        if (!tmpFormData.position) {
            showWxToast('请选择身份!');
            return;
        }
        if (tmpFormData.avator.indexOf('tmp') > -1) {
            // 需要上传图片后修改
            this.edit1(tmpFormData);
        } else {
            // 已经上传过图片
            this.edit2();
        }

    },
    edit1: function (tmpFormData) {
        showWxLoading('信息修改中...');
        uploadHeadImg(tmpFormData.avator).then((res) => {
            let tmpRes = JSON.parse(res.data);
            tmpFormData.avator = tmpRes.data.filePath;
            this.setData({
                formData: tmpFormData,
            });
            return editUserInfo(this.data.formData);
        }).then((res2) => {
            console.log(res2);
            hideWxLoading();
            if (res2.data.code === '200') {
                showWxToast('修改成功!');
                app.globalData.isH5NeedRefresh = true;
                this.setData({
                    headImg: this.data.formData.avator,
                    nickname: this.data.formData.wx_name,
                    relativeType: this.data.formData.type
                });
                timeoutTask(() => {
                    this.hideEditPopup();
                }, 1000);
            } else if (res2.data.code === '100') {
                this.editRecharge(() => {
                    this.edit2();
                });
            }
        }).catch((err) => {
            console.log(err);
            hideWxLoading();
        })
    },
    edit2: function () {
        showWxLoading('信息修改中...');
        editUserInfo(this.data.formData).then((res2) => {
            console.log(res2);
            hideWxLoading();
            if (res2.data.code === '200') {
                showWxToast('修改成功!');
                app.globalData.isH5NeedRefresh = true;
                this.setData({
                    headImg: this.data.formData.avator,
                    nickname: this.data.formData.wx_name,
                    relativeType: this.data.formData.type
                });
                timeoutTask(() => {
                    this.hideEditPopup();
                }, 1000);
            } else if (res2.data.code === '100') {
                this.editRecharge(() => {
                    this.edit2();
                });
            }
        }).catch((err) => {
            console.log(err);
            hideWxLoading();
        })
    },

});
```

## File: pages/recharge2/recharge2.json
```json
{
  "navigationBarTitleText": "充值中心",
  "usingComponents": {
    "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
  }
}
```

## File: pages/recharge2/recharge2.wxml
```
<view class="rechargeContainer">
  <image src="/assets/image/hd2/topBg.png" class="topBg"></image>
  <view class="userInfo">
    <view class="headImgBox">
      <image src="{{headImg}}" class="headImg {{miao_vip ? 'vipBox' : ''}}"></image>
    </view>
    <view class="accountInfo">
      <view class="top">
        <view class="nickname">{{nickname}}</view>
        <view class="level">
          <image src="/assets/image/hd2/crown.png" class="crownImg"></image>
          <view class="levelVal">Lv{{vipLevel}}</view>
        </view>
      </view>
      <view class="bottom">
        余额: {{remainMoney}}
        <image src="/assets/image/hd2/diamond.png" class="diamondImg"></image>
      </view>
    </view>
    <view class="relativeType">
      <image src="/assets/image/hd2/boyIcon.png" class="relativeIcon" wx:if="{{relativeType === '1'}}" bindtap="showEditPopup"></image>
      <image src="/assets/image/hd2/girlIcon.png" class="relativeIcon" wx:if="{{relativeType === '2'}}" bindtap="showEditPopup"></image>
      {{relativeType === '1' ? '男方亲友' : '女方亲友'}}
    </view>
  </view>
  <!-- 固定充值金额区域 -->
  <view class="limitRechargeArea">
    <view class="rechargeItem" wx:for="{{rechargeList}}" wx:key="index" data-desc="{{item}}" bindtap="recharge">
      <image src="/assets/image/hd2/diamond.png" class="diamondIcon"></image>
      <view class="num">{{item}}</view>
      <image src="/assets/image/hd2/th.png" class="thIcon" wx:if="{{index === rechargeList.length - 1}}"></image>
    </view>
  </view>
  <view class="agreement" bindtap="toAgreement">
    阅读并同意
    <view class="bond">《充值服务协议》</view>
  </view>
  <view class="wishSheetList">
    <image src="/assets/image/hd2/bdTitle.png" class="bdTitle"></image>
    <view class="vsTitle">
      <view class="boy">
        <image src="/assets/image/hd2/boy.png" class="sexIcon"></image>
        男方亲友
      </view>
      <image src="/assets/image/hd2/vs.png" class="vsIcon"></image>
      <view class="girl">
        <image src="/assets/image/hd2/girl.png" class="sexIcon"></image>
        女方亲友
      </view>
    </view>
    <view class="gapLine"></view>
    <view class="listWrap">
      <view class="sexList boy">
        <view class="item" wx:for="{{giftRankListBoy}}" wx:key="index">
          <view class="user">
            <view class="baseInfo">
              <image src="{{item.avator}}" class="headImg"></image>
              <view class="name">{{item.wx_name}}</view>
            </view>
            <view class="level">
              <image src="/assets/image/hd2/crown.png" class="crownImg"></image>
              <view class="levelVal">Lv1</view>
            </view>
          </view>
          <view class="sendGiftNum">送出{{item.size}}个祝福</view>
        </view>
      </view>
      <view class="sexList girl">
        <view class="item" wx:for="{{giftRankListGirl}}" wx:key="index">
          <view class="user">
            <view class="baseInfo">
              <image src="{{item.avator}}" class="headImg"></image>
              <view class="name">{{item.wx_name}}</view>
            </view>
            <view class="level">
              <image src="/assets/image/hd2/crown.png" class="crownImg"></image>
              <view class="levelVal">Lv1</view>
            </view>
          </view>
          <view class="sendGiftNum">送出{{item.size}}个祝福</view>
        </view>
      </view>
    </view>
  </view>
  <!-- 反馈入口 -->
  <feedbackEntry userId="{{userId}}"></feedbackEntry>
  <!-- 弹出区域 -->
  <view class="popupArea" wx:if="{{editPopupVisible}}">
    <view class="shade" bindtap="hideEditPopup"></view>
    <view class="infoForm {{editPopupAni?'show':'hide'}}">
      <view class="formItem">
        <view class="key">头像</view>
        <view class="formCt">
          <image src="{{formData.avator}}" class="headImg" bindtap='upload'></image>
          <image src="/assets/image/hd2/arrowRight.png" class="arrowRight"></image>
        </view>
      </view>
      <view class="formItem">
        <view class="key">贵宾姓名</view>
        <view class="formCt">
          <input bindblur="handleNameBlur" value="{{formData.wx_name}}" placeholder="请输入贵宾姓名" placeholder-style="color:#5B5E63;font-size: 32rpx" class="nameIpt" maxlength="12" />
        </view>
      </view>
      <view class="formItem">
        <view class="key">亲友团</view>
        <view class="formCt">
          <radio-group class="relativeGroup" bindchange="chooseRelatives">
            <view class="radioItem">
              <view class="radioLabel boy">
                <image src="/assets/image/hd2/boy.png" class="sexIcon boy"></image>
                男方亲友
              </view>
              <radio value="1" checked="{{formData.type === '1'?true:false}}" class="relativesRadio"></radio>
            </view>
            <view class="radioItem">
              <view class="radioLabel girl">
                <image src="/assets/image/hd2/girl.png" class="sexIcon girl"></image>
                女方亲友
              </view>
              <radio value="2" class="relativesRadio" checked="{{formData.type === '2'?true:false}}"></radio>
            </view>
          </radio-group>
        </view>
      </view>
      <view class="formItem">
        <view class="key">桌号</view>
        <picker value="{{formData.table_number}}" range="{{deskList}}" bindchange="handlePickerChange">
          <view class="deskNumPicker">
            {{formData.table_number}}桌
            <image src="/assets/image/hd2/arrowRight.png" class="arrowRight"></image>
          </view>
        </picker>
      </view>
      <view class="formItem">
        <view class="key">身份</view>
        <view class="identyLabels">
          <view class="label {{item === formData.position ? 'active': ''}}" wx:for="{{statusList}}" wx:key="index" data-status="{{item}}" bindtap="chooseStatus">
            {{item}}
          </view>
        </view>
      </view>
      <view class="formConfirmItem">
        <view class="confirmBtn" bindtap="confirmEdit">确认修改</view>
        <view class="editTip">确认修改需要消耗{{editUserInfoPrice}}个喵钻</view>
      </view>
    </view>
  </view>
  <!-- 隐私授权弹窗 -->
  <privacyAuthorize></privacyAuthorize>
</view>
```

## File: pages/recharge2/recharge2.wxss
```
.rechargeContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #F4F7F9;
    height: 1624rpx;
}

.rechargeContainer>.topBg {
    width: 100%;
    height: 678rpx;
    position: absolute;
}

.rechargeContainer>.userInfo {
    width: 100%;
    display: flex;
    align-items: center;
    margin-top: 120rpx;
    padding: 0 40rpx;
    position: relative;
}

.userInfo>.headImgBox {
    position: relative;
    width: 110rpx;
    height: 110rpx;
}

.userInfo>.headImgBox>.headImg {
    width: 100%;
    height: 100%;
    border-radius: 50%;
}

.userInfo>.headImgBox>.getRewardBtn {
    width: 130rpx;
    height: 36rpx;
    background: #FFDB27;
    border-radius: 18rpx 18rpx 18rpx 0rpx;
    position: absolute;
    top: -61rpx;
    left: 16rpx;
    font-size: 18rpx;
    font-weight: bold;
    color: #D8241D;
    display: flex;
    justify-content: center;
    align-items: center;
}

.userInfo>.headImgBox>.pencilImg {
    width: 40rpx;
    height: 40rpx;
    position: absolute;
    top: -10rpx;
    right: -2rpx;
}

.userInfo>.accountInfo {
    margin-left: 36rpx;
}

.userInfo>.accountInfo>.top {
    display: flex;
    align-items: center;
}

.userInfo>.accountInfo>.top>.nickname {
    font-size: 36rpx;
    color: #FFFFFF;
    font-weight: 500;
}

.userInfo>.accountInfo>.top>.level {
    width: 48rpx;
    height: 42rpx;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 20rpx;
}

.userInfo>.accountInfo>.top>.level>.crownImg {
    width: 100%;
    height: 100%;
}

.userInfo>.accountInfo>.top>.level>.levelVal {
    font-size: 20rpx;
    color: #fff;
    position: absolute;
    margin-top: 6rpx;
}

.userInfo>.accountInfo>.bottom {
    margin-top: 16rpx;
    color: rgba(255, 255, 255, 0.6);
    font-size: 24rpx;
    display: flex;
    align-items: center;
}

.userInfo>.accountInfo>.bottom>.diamondImg {
    width: 32rpx;
    height: 26rpx;
    margin-left: 14rpx;
}

.userInfo>.relativeType {
    width: 140rpx;
    height: 48rpx;
    background: rgba(255, 255, 255, 0.28);
    border-radius: 24rpx;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20rpx;
    color: rgba(255, 255, 255, 0.6);
    position: absolute;
    right: 40rpx;
    bottom: 0;

}

.userInfo>.relativeType>.relativeIcon {
    width: 22rpx;
    height: 24rpx;
    margin-right: 10rpx;
}

.rechargeContainer>.limitRechargeArea {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 140rpx;
    position: relative;
}

.limitRechargeArea>.rechargeItem {
    width: 187rpx;
    height: 100rpx;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 12rpx 12rpx;
    background-color: #EEE9FF;
    border-radius: 10rpx;
    position: relative;
}

.limitRechargeArea>.rechargeItem>.diamondIcon {
    width: 64rpx;
    height: 52rpx;
    margin-top: 12rpx;
}

.limitRechargeArea>.rechargeItem>.num {
    font-size: 42rpx;
    font-weight: 500;
    color: #9C2CF3;
    margin-left: 6rpx;
}
.limitRechargeArea>.rechargeItem>.thIcon {
    width: 74rpx;
    height: 32rpx;
    position: absolute;
    top: -16rpx;
    right: -16rpx;
}
.rechargeContainer>.agreement {
    font-size: 22rpx;
    font-weight: 500;
    color: #666666;
    margin-top: 12rpx;
    position: relative;
    display: flex;
}

.rechargeContainer>.agreement>.bond {
    color: #DC2F2F;
}

.rechargeContainer>.wishSheetList {
    position: relative;
    margin-top: 90rpx;
    width: 690rpx;
    height: 856rpx;
    background: #FFFFFF;
    box-shadow: 0rpx 4rpx 10rpx -2rpx rgba(0, 0, 0, 0.06);
    border-radius: 8rpx;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.wishSheetList>.bdTitle {
    width: 372rpx;
    height: 86rpx;
    position: absolute;
    top: -42rpx;
}

.wishSheetList>.vsTitle {
    display: flex;
    align-items: center;
    width: 100%;
    justify-content: center;
    margin-top: 84rpx;
}

.wishSheetList>.vsTitle>.boy {
    display: flex;
    align-items: center;
    font-size: 32rpx;
    font-weight: 600;
    color: #4526C2;
}

.wishSheetList>.vsTitle>.boy>.sexIcon {
    width: 36rpx;
    height: 40rpx;
    margin-right: 8rpx;
}

.wishSheetList>.vsTitle>.girl {
    display: flex;
    align-items: center;
    font-size: 32rpx;
    font-weight: 600;
    color: #EA1877;
}

.wishSheetList>.vsTitle>.girl>.sexIcon {
    width: 32rpx;
    height: 44rpx;
    margin-right: 8rpx;
}

.wishSheetList>.vsTitle>.vsIcon {
    width: 52rpx;
    height: 52rpx;
    margin: 0 58rpx;
}

.wishSheetList>.gapLine {
    width: 636rpx;
    height: 2rpx;
    border: 1rpx solid #EEEEEE;
    margin-top: 24rpx;
}

.wishSheetList>.listWrap {
    display: flex;
    width: 100%;
    margin-top: 36rpx;
    justify-content: center;
    height: 800rpx;
    overflow-y: scroll;

}

.wishSheetList>.listWrap>.sexList {
    width: 35%;
    margin: 0 24rpx;
}

.sexList>.item {
    margin-bottom: 60rpx;
}

.sexList>.item>.user {
    display: flex;
    align-items: center;
    /* width: 240rpx; */
    justify-content: space-between;
}

.sexList>.item>.user>.baseInfo {
    display: flex;
    align-items: center;
    margin-right: 12rpx;
}

.sexList>.item>.user>.baseInfo>.headImg {
    width: 56rpx;
    height: 56rpx;
    margin-right: 14rpx;
    border-radius: 50%;
}

.sexList>.item>.user>.baseInfo>.name {
    font-size: 28rpx;
    color: #514E4E;
    font-weight: 400;
}

.sexList>.item>.user>.level {
    width: 36rpx;
    height: 30rpx;
    position: relative;
    display: flex;
    justify-content: center;
}

.sexList>.item>.user>.level>.crownImg {
    width: 100%;
    height: 100%;
}

.sexList>.item>.user>.level>.levelVal {
    font-size: 12rpx;
    color: #fff;
    position: absolute;
    top: 16rpx;
}

.sexList>.item>.sendGiftNum {
    font-size: 28rpx;
    font-weight: 400;
    color: #4526C2;
    margin-top: 12rpx;
}

.popupArea {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
}

.popupArea>.shade {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.3);
    top: 0;
    left: 0;
}

.popupArea>.infoForm {
    width: 750rpx;
    height: 1130rpx;
    background: #FFFFFF;
    position: absolute;
    bottom: 0;
    border-top-right-radius: 20rpx;
    border-top-left-radius: 20rpx;
    padding: 0 50rpx;
    padding-top: 30rpx;
    transition: all 0.3s ease-out;
}

.popupArea>.infoForm.hide {
    transform: translateY(1130rpx);
}

.popupArea>.infoForm.show {
    transform: translateY(0rpx);
}

.infoForm>.formItem {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 138rpx;

}

.infoForm>.formItem:nth-child(4) {
    position: relative;
}

.infoForm>.formItem>.key {
    font-size: 32rpx;
    font-weight: 400;
    color: #8F9297;
}

.infoForm>.formItem>.formCt {
    display: flex;
    align-items: center;
    position: relative;
}

.infoForm>.formItem>.formCt>.headImg {
    width: 76rpx;
    height: 76rpx;
    border-radius: 50%;
}

.infoForm>.formItem>.formCt>.arrowRight {
    width: 28rpx;
    height: 28rpx;
    margin-left: 30rpx;
}

.infoForm>.formItem>.formCt>.nameIpt {
    font-weight: 400;
    color: #5B5E63;
    font-size: 32rpx;
    text-align: right;
    width: 256rpx;
}

.infoForm>.formItem>.formCt>.relativeGroup {
    display: flex;
}

.relativeGroup>.radioItem {
    display: flex;
    align-items: center;
}

.relativeGroup>.radioItem:nth-child(1) {
    margin-right: 66rpx;
}

.relativeGroup>.radioItem>.radioLabel {
    display: flex;
    align-items: center;
    font-weight: 400;
    font-size: 28rpx;
    margin-right: 16rpx;
}

.relativeGroup>.radioItem>.radioLabel.boy {
    color: #6112B0;
}

.relativeGroup>.radioItem>.radioLabel.girl {
    color: #ED3488;
}

.relativeGroup>.radioItem>.radioLabel>.sexIcon.boy {
    width: 32rpx;
    height: 32rpx;
    margin-right: 8rpx;
}

.relativeGroup>.radioItem>.radioLabel>.sexIcon.girl {
    width: 28rpx;
    height: 34rpx;
    margin-right: 8rpx;
}

.formItem .deskNumPicker {
    display: flex;
    align-items: center;
}

.formItem .deskNumPicker>.arrowRight {
    margin-left: 30rpx;
    width: 28rpx;
    height: 28rpx;
}

.identyLabels {
    width: 520rpx;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding-top: 110rpx;
}

.identyLabels>.label {
    width: 135rpx;
    height: 64rpx;
    border-radius: 30rpx;
    border: 2rpx solid #EEEEEE;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 28rpx;
    font-weight: 400;
    color: #5B5E63;
    margin: 25rpx 10rpx;
    white-space: nowrap;
}

.identyLabels>.label.active {
    background: linear-gradient(276deg, #71B3FF 0%, #2C82E4 100%);
    color: #FFFFFF;
}

.formConfirmItem {
    flex-direction: column;
    display: flex;
    align-items: center;
    margin-top: 150rpx;
}

.formConfirmItem>.confirmBtn {
    width: 418rpx;
    height: 90rpx;
    background: linear-gradient(300deg, #C76BFB 0%, #EA1775 100%);
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 32rpx;
    font-weight: 400;
    color: #FFFFFF;
}

.formConfirmItem>.editTip {
    font-size: 24rpx;
    font-weight: 400;
    color: #E14D4D;
    margin-top: 14rpx;
}
```

## File: pages/test/index/index.js
```javascript
const app = getApp();

Page({
  data: {
    h5Url: '',
  },
  onLoad: function(options) {
    this.setData({
      h5Url: 'https://www.hudongmiao.com/templeEscape/index.html?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHQiOjE2MzM0ODg0NTQzOTAsInVpZCI6IjAyYjdkY2ExOTdmODRjYmI4MmY2OTExNTY0MGU1N2Y5IiwiaWF0IjoxNjMyODgzNjU0MzkwfQ.ogbVJVTNlicAkyWiCwspatimPV3Pjjo3ilXAMlZImEY',
    });
  },
  onShow: function() {
  },
});
```

## File: pages/test/index/index.json
```json
{
    "navigationBarTitleText": "首页"
}
```

## File: pages/test/index/index.wxml
```
<web-view wx:if="{{h5Url}}" src="{{h5Url}}"></web-view>
```

## File: pages/test/index/index.wxss
```
page {
	background: linear-gradient(139deg, #fec84e 0%, #feaf40 100%);
  }
```

## File: pages/test/login/login.js
```javascript
import { wxLogin, authUser } from '../../../api/login';

const app = getApp();

Page({
    data: {
    },

    onLoad: function (options) {
    },

    onShow: function () {

    },
    onShareAppMessage: function () {
        return {
            title: this.data.title,
            path: '/pages/test/login/login',
            success: function (res) { },
            fail: function (res) { }
        }
    },
    /**
     * 授权登录获取用户信息
     */
    getUserInfo: function (e) {
        console.log(e);
        wxLogin().then((res) => {
            console.log(res);
            return authUser({
                code: res.code,
                encryptedData: e.detail.encryptedData,
                iv: e.detail.iv,
            })
        }).then((res2) => {
            console.log('res2:', res2);
            console.log(`http://192.168.66.104/?liveId=692991d279f8411a98392ecb48ca4948&token=${res2.data.token}&time=1599788613040#/`);
        }).catch((err) => {
            console.log(err);
        })
    },
})
```

## File: pages/test/login/login.json
```json
{
    "navigationBarTitleText": "登录"
}
```

## File: pages/test/login/login.wxml
```
<!-- 登录 -->
<view class="login">
    <button class='btn' type='primary' open-type="getUserInfo" bindgetuserinfo="getUserInfo" lang="zh_CN">
        点击获取用户信息
    </button>
    <view class="userinfo-avatar">
        <open-data type="userAvatarUrl"></open-data>
    </view>
    <open-data type="userNickName"></open-data>
</view>
```

## File: pages/test/login/login.wxss
```
.userinfo-avatar {  
    overflow:hidden;  
    display: block;  
    width: 160rpx;  
    height: 160rpx;  
    margin: 20rpx;  
    margin-top: 50rpx;  
    border-radius: 50%;  
    border: 2px solid #fff;  
    box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);  
  }  
    
  .userinfo{  
    font-size: 14px;  
    background-color: #c0c0c0;  
    border-radius:40%;  
  }
```

## File: pages/test/pay/pay.js
```javascript
import { getSetting } from '../../../api/system.js'
import { recharge } from '../../../api/index/index.js'
import { timeoutTask, isNumber, showWxToast } from '../../../utils/index.js'
const app = getApp();

Page({
    data: {
        //是否授权
        isAuth: false,
        //授权询问弹窗
        authDialogVisible: false,
        headImg: '',
        nickname: '',
        userId: '',
        openId: '',
        money: 0,
    },

    onLoad: function (options) {
        //是否授权初始化
        this.initIsAuth();
        // 设置用户信息
        this.setUserInfo();
    },

    onShow: function () {

    },

    onShareAppMessage: function () {
        return {
            title: this.data.title,
            path: '/pages/index/index',
            success: function (res) { },
            fail: function (res) { }
        }
    },
    initIsAuth() {
        getSetting().then(res => {
            if (res.errMsg == 'getSetting:ok') {
                this.setData({
                    isAuth: res.authSetting['scope.userInfo'] || false
                })
            }
            if (!this.data.isAuth) {
                this.setData({
                    authDialogVisible: true
                });
            }
        }).catch(err => {
            console.log(err);
        });

    },
    authSuccessHandle() {
        this.setData({
            authDialogVisible: false
        });
        timeoutTask(() => {
            this.setUserInfo();
        }, 100);
    },
    setUserInfo() {
        this.setData({
            userId: wx.getStorageSync('userId'),
            openId: wx.getStorageSync('openId'),
            nickname: wx.getStorageSync('nickname'),
            headImg: wx.getStorageSync('headImg')
        });
    },
    pay() {
        if (!this.data.isAuth) {
            showWxToast('授权失败!');
            this.initIsAuth();
            return;
        }
        if (!isNumber(this.data.money) || !this.data.money) {
            showWxToast('请输入正确的金额!');
            return;
        }
        recharge(this.data.money).then(res => {
            console.log(res);
            showWxToast('支付成功!');
        }).catch(err => {
            console.log(err);
            showWxToast('支付失败!');
        })
    },
    moneyInput(e) {
        this.setData({
            money: e.detail.value
        });
    }
})
```

## File: pages/test/pay/pay.json
```json
{
    "navigationBarTitleText": "支付"
}
```

## File: pages/test/pay/pay.wxml
```
<!-- 首页 -->
<view class="payWrap">
    <view class="userInfo">
        <image class="headImg" src="{{headImg}}"></image>
        <view class="nickname">{{nickname}}</view>
    </view>
    <view class="price">
        <!-- {{money}} -->
        <input class="input"  placeholder="请输入充值金额" bindinput="moneyInput" />
        <view class="unit">元</view>
    </view>
    <view class="btnWrap">
        <view class="btn" bindtap="pay">支付</view>
    </view>
    <!-- 授权弹窗 -->
    <authDialog dialogVisible="{{authDialogVisible}}" bind:authSuccess="authSuccessHandle"></authDialog>
</view>
```

## File: pages/test/pay/pay.wxss
```
.payWrap {
    width: 100vw;
    height: 100vh;
}

.payWrap>.userInfo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.payWrap>.userInfo>.headImg {
    width: 240rpx;
    height: 240rpx;
    border-radius: 50%;
}

.payWrap>.userInfo>.nickname {
    font-size: 56rpx;
    margin-top: 24rpx;
}

.payWrap>.price {
    font-size: 96rpx;
    font-weight: bold;
    margin: 136rpx auto;
    display: flex;
    justify-content: center;
    align-items: center;
}

.payWrap>.price>.input {
    font-size: 26rpx;
    width: 309rpx;
    height: 80rpx;
    border: 1px solid #eaeaea;
    padding: 0 12rpx;
    margin-right: 20rpx;

}

.payWrap>.price>.unit {
    font-size: 56rpx;
    font-weight: normal;
}

.payWrap>.btnWrap {
    display: flex;
    justify-content: center;
    margin-top: 20%;
}

.payWrap>.btnWrap>.btn {
    width: 80%;
    height: 90rpx;
    background-color: rgba(19, 175, 18, 1);
    color: #FFFFFF;
    font-size: 36rpx;
    line-height: 90rpx;
    display: flex;
    justify-content: center;
    align-items: center;
}
```

## File: pages/zfdm/zfdm.js
```javascript
import {
  zfdmRecharge,
  getZfdmInfo,
  startZfdm,
  getZfdmRankList,
  getZfdmMessageList,
} from '../../api/zfdm/zfdm';
import { wxPay } from '../../api/pay';
import { timeoutTask, showWxToast, getRandom } from '../../utils/index';
import defaultContent from '../../assets/constant/default';
const app = getApp();

let second = 0;
// let millisecond = 0;
let m1 = 0;
let m2 = 0;
let m3 = 0;
let m4 = 0;
let millisecondReal = 0;
let timeStr = '00:0000';
let tmpInterval; //用于倒计时
let tmpInterval2;
let inPay = false;
let isEndLoop = false;
let btnLock = false;
let innerAudioContextStart = null;
let innerAudioContextEnd = null;
Page({
  /**
     * 页面的初始数据
     */
  data: {
    userId: '',
    openId: '',
    avator: '',
    timestr: '00:0000',
    resultTime: '',
    koPercentVal: '', // 击败了多少人%
    koDis: '', // 距离目标还差多少秒
    koBonus: '', // 目标奖励金额
    koOtherName: '', // 击败别人的人或者击败我的人
    ruleBoxVisible: false,
    rankVisible: false,
    guessInfoId: '',// 参与id
    redpackageId: '',// 轮次id
    isFree: false, // 本次挑战是否免费
    raceTime: '', // 本次挑战的目标时间
    raceStatus: '2', // 0: 游戏中 1: 游戏结束 2: 游戏等待
    tipVisible: false,
    tipBoxType: 0, // 0:挑战失败 1:挑战成功 2:放弃挑战 3:别人的ko信息 4:我被ko的信息
    currentRank: 0, // 当前名次
    rankList: [], // 排行榜
    isOnTimer: false, // 是否挑战中
    needPrice: 0,
    messageQueue: [],
    cdTxt: 3,
  },

  /**
     * 生命周期函数--监听页面加载
     */
  onLoad: function(options) {
    console.log(options);
    isEndLoop = false;
    inPay = false;
    this.resetTimer();
    this.setData({
      userId: options.userId,
      openId: options.openId,
      avator: options.headImg,
    });
    this.initZfdmInfo();
    btnLock = false;
    innerAudioContextStart = wx.createInnerAudioContext({
      useWebAudioImplement: true,
    });
    innerAudioContextStart.src =
      'https://ustatic.hudongmiao.com/joymewMp/zfdm/zfdmStart.mp3';
    innerAudioContextEnd = wx.createInnerAudioContext({
      useWebAudioImplement: true,
    });
    innerAudioContextEnd.src =
      'https://ustatic.hudongmiao.com/joymewMp/zfdm/zfdmEnd.mp3';
  },
  onUnload: function() {
    this.resetTimer();
    isEndLoop = true;
    inPay = false;
    btnLock = false;
    innerAudioContextStart.destroy();
    innerAudioContextStart = null;
    innerAudioContextEnd.destroy();
    innerAudioContextEnd = null;
  },
  replay: function() {
    this.closeTipBox();
    this.start();
  },
  bgAidStart: function(type) {
    if (type === 'start') {
      innerAudioContextStart.play();
    } else if (type === 'end') {
      innerAudioContextEnd.play();
    }
    wx.vibrateLong();
  },
  handleBtnTap: function() {
    if (this.data.isOnTimer) {
      this.end();
    } else {
      this.start();
    }
  },
  start: function() {
    if (btnLock) {
      return;
    }
    this.bgAidStart('start');
    if (this.data.isFree) {
      tmpInterval = setInterval(this.timer, 10);
      this.setData({
        isOnTimer: true,
      });
    } else {
      inPay = true;
      zfdmRecharge({
        userId: this.data.userId,
        openId: this.data.openId,
      })
        .then(res => {
          console.log(res);
          return wxPay(res);
        })
        .then(res2 => {
          console.log(res2);
          return this.updateZfdmInfo();
        })
        .then(() => {
          inPay = false;
          tmpInterval = setInterval(this.timer, 10);
          this.setData({
            isOnTimer: true,
          });
        })
        .catch(err => {
          showWxToast('支付失败');
          inPay = false;
          console.log(err);
        });
    }
  },
  end: function() {
    if (btnLock) {
      return;
    }
    console.log(this.transformTimeStr());
    if (tmpInterval) {
      this.bgAidStart('end');
      clearInterval(tmpInterval);
      tmpInterval = null;
      this.startGame(this.data.isFree);
      this.setData({
        isOnTimer: false,
      });
    } else {
      showWxToast('请点击挑战');
    }
  },
  startGame: function(isFree) {
    btnLock = true;
    this.setData({
      resultTime: this.transformTimeStr(),
    });
    startZfdm({
      guessInfoId: isFree ? 'free_id' : this.data.guessInfoId,
      raceTime: this.data.resultTime,
    })
      .then(res => {
        console.log('开始游戏后的结果：', res);
        btnLock = false;
        if (isFree) {
          this.setData({
            isFree: false,
          });
        }
        if (res.data.code === '200' && res.data.myRank) {
          let tmpRank = parseInt(res.data.myRank.size, 10);
          let tmpTipBoxType = 0;
          if (tmpRank <= 8) {
            tmpTipBoxType = 1;
          } else {
            tmpTipBoxType = 0;
          }
          this.setData({
            tipVisible: true,
            tipBoxType: tmpTipBoxType,
            currentRank: tmpRank,
            koPercentVal: res.data.myRank.chaoYueVal,
            koDis: res.data.myRank.raceTime_val_distance,
            koBonus: res.data.myRank.red_bao_money,
          });
        }
      })
      .catch(err => {
        console.log(err);
        btnLock = false;
      });
  },
  // 时间转化
  transformTimeStr: function() {
    let tmpLastTime = '';
    let zPart = '';
    let xPart = '';
    const tmpTimeArr = this.data.timestr.split('');
    console.log(tmpTimeArr);
    if (tmpTimeArr[0] === '0') {
      zPart = tmpTimeArr[1];
    } else {
      zPart = tmpTimeArr[0] + tmpTimeArr[1];
    }
    for (let i = 6; i >= 3; i -= 1) {
      if (tmpTimeArr[i] !== '0') {
        break;
      } else {
        tmpTimeArr[i] = '';
      }
    }
    xPart = tmpTimeArr[3] + tmpTimeArr[4] + tmpTimeArr[5] + tmpTimeArr[6];

    if (xPart) {
      tmpLastTime = `${zPart}.${xPart}`;
    } else {
      tmpLastTime = zPart;
    }
    return tmpLastTime;
  },
  resetTimer: function() {
    if (tmpInterval) {
      clearInterval(tmpInterval);
      tmpInterval = null;
      this.setData({
        isOnTimer: false,
      });
    }
    if (tmpInterval2) {
      clearInterval(tmpInterval2);
      tmpInterval2 = null;
    }
    second = 0;
    // millisecond = 0;
    m1 = 0;
    m2 = 0;
    m3 = 0;
    m4 = 0;
    millisecondReal = 0;
    timeStr = '00:0000';
    this.setData({
      timestr: timeStr,
    });
  },
  timer: function() {
    if (millisecondReal >= 100) {
      // millisecond = 0;
      millisecondReal = 0;
      second += 1;
      if (second === 99) {
        this.end();
      }
    }
    millisecondReal = millisecondReal + 1;
    // millisecond = getRandom(0, 9999);
    m4 += 1;
    if (millisecondReal % 3 === 0) {
      m3 += 1;
    }
    if (millisecondReal % 6 === 0) {
      m2 += 1;
    }
    if (millisecondReal % 10 === 0) {
      m1 += 1;
    }
    if (m4 > 9) {
      m4 = 0;
    }
    if (m3 > 9) {
      m3 = 0;
    }
    if (m2 > 9) {
      m2 = 0;
    }
    if (m1 > 9) {
      m1 = 0;
    }
    // timeStr =
    //   this.getConvertSecond(second) +
    //   ':' +
    //   this.getConvertMilliSecond(millisecond);
    timeStr = this.getConvertSecond(second) + ':' + m1 + m2 + m3 + m4;
    this.setData({
      timestr: timeStr,
    });
  },
  getConvertSecond: function(second) {
    const secondStr = second.toString();
    let resultStr;
    if (secondStr.length === 1) {
      resultStr = '0' + secondStr;
    } else if (secondStr.length === 2) {
      resultStr = secondStr;
    } else {
      resultStr = '00';
    }
    return resultStr;
  },
  getConvertMilliSecond: function(millisecond) {
    const millisecondStr = millisecond.toString();
    let resultStr;
    if (millisecondStr.length === 1) {
      resultStr = '000' + millisecondStr;
    } else if (millisecondStr.length === 2) {
      resultStr = '00' + millisecondStr;
    } else if (millisecondStr.length === 3) {
      resultStr = '0' + millisecondStr;
    } else {
      resultStr = millisecondStr;
    }
    return resultStr;
  },
  getIt: function() {
    this.setData({
      ruleBoxVisible: false,
    });
  },
  openRuleBox: function() {
    this.setData({
      ruleBoxVisible: true,
    });
  },
  closeTipBox: function() {
    // 如果关闭的是ko信息弹窗则更新消息队列的索引
    if (this.data.tipBoxType === 3 || this.data.tipBoxType === 4) {
      app.updateZfdmIndex();
    }
    this.setData({
      tipVisible: false,
      tipBoxType: 0,
      currentRank: 0,
      resultTime: '',
      koPercentVal: '',
      koDis: '',
      koBonus: '',
      koOtherName: '',
    });
    this.resetTimer();
  },
  initZfdmInfo: function() {
    getZfdmInfo()
      .then(res => {
        console.log(res);
        this.setData({
          guessInfoId: res.data.guess_info_id,
          redpackageId: res.data.red_package_id,
          isFree: res.data.isUseFreeChance === '0',
          raceTime: res.data.raceTime,
          raceStatus: res.data.race_status,
          needPrice: res.data.race_one_money,
        });
        app.initZfdmId(res.data.red_package_id);
        if (this.data.raceStatus === '1') {
          this.getRankList();
        } else {
          this.loopGetZfdmInfo();
        }
      })
      .catch(err => {
        console.log(err);
      });
  },
  updateZfdmInfo: function() {
    return new Promise((resolve, reject) => {
      getZfdmInfo()
        .then(res => {
          console.log('更新guessInfoId', res);
          this.setData({
            guessInfoId: res.data.guess_info_id,
            redpackageId: res.data.red_package_id,
            isFree: res.data.isUseFreeChance === '0',
            raceTime: res.data.raceTime,
            raceStatus: res.data.race_status,
            needPrice: res.data.race_one_money,
          });
          resolve();
        })
        .catch(err => {
          console.log(err);
          reject(err);
        });
    });
  },
  loopGetZfdmInfo: function() {
    if (isEndLoop) {
      return;
    }
    getZfdmInfo(true)
      .then(res => {
        console.log(res);
        this.setData({
          raceStatus: res.data.race_status,
        });
        if (this.data.raceStatus === '1') {
          isEndLoop = true;
          this.getRankList();
        } else {
          timeoutTask(() => {
            this.loopGetZfdmInfo();
          }, 2000);
          timeoutTask(() => {
            this.updateMessageQueue();
          }, 4000);
        }
      })
      .catch(err => {
        console.log(err);
        isEndLoop = true;
      });
  },
  updateMessageQueue() {
    getZfdmMessageList(this.data.redpackageId)
      .then(res => {
        if (res && res.data) {
          this.setData({
            messageQueue: res.data.playList,
          });
          console.log('消息列表：', this.data.messageQueue);
          this.popupMessage();
        }
      })
      .catch(err => {
        console.log(err);
      });
  },
  popupMessage() {
    if (btnLock || tmpInterval || inPay) {
      // 操作中(支付中、秒表转动、查看结果)
      return;
    }
    if (this.data.tipVisible) {
      // 弹出中
      return;
    }
    const tmpQueue = this.data.messageQueue;
    const tmpCurrentMsg = tmpQueue[app.globalData.zfdmIndex];
    if (!tmpCurrentMsg) {
      // 消息队列中无消息
      return;
    }
    console.log('弹出消息');
    try {
      // 解析出消息对象
      const tmpMsgObj = JSON.parse(tmpCurrentMsg.element);
      // 判断是别人的ko信息还是我被ko的信息
      if (tmpMsgObj.jb_userId === this.data.userId) {
        // 弹出我被ko的消息
        this.setData({
          tipVisible: true,
          tipBoxType: 4,
          koOtherName: tmpMsgObj.my_name,
          koPercentVal: tmpMsgObj.chaoYueVal,
          koBonus: tmpMsgObj.rank_money,
        });
      } else {
        // 弹出别人的ko消息
        this.setData({
          tipVisible: true,
          tipBoxType: 3,
          koOtherName: tmpMsgObj.my_name,
          resultTime: tmpMsgObj.my_guess_money,
          koPercentVal: tmpMsgObj.chaoYueVal,
          koBonus: tmpMsgObj.rank_money,
        });
        // 执行倒计时逻辑
        if (!tmpInterval2) {
           let tmpCd = 3;
          this.setData({
            cdTxt: tmpCd,
          });
          console.log('开始计时', tmpCd);
          tmpInterval2 = setInterval(() => {
            if (tmpCd === 1) {
              clearInterval(tmpInterval2);
              tmpInterval2 = null;
              this.closeTipBox();
            } else {
              tmpCd -= 1;
            }
            this.setData({
              cdTxt: tmpCd,
            });
          }, 1000);
        }
      }
    } catch (err) {
      console.log(err);
    }
  },
  getRankList: function() {
    getZfdmRankList(this.data.redpackageId)
      .then(res => {
        console.log('排行榜：', res);
        // let tmpList = res.data.list;
        let tmpList = [];
        const tmpLen = res.data.list.length;
        if (tmpLen > 8) {
          tmpList = res.data.list.slice(0, 8);
        } else {
          tmpList = res.data.list;
          // 补齐
          for (let i = tmpLen; i < 8; i += 1) {
            tmpList.push({
              avator: defaultContent.defaultHeadImg,
              wx_name: 'Player',
              guess_money: 0,
              lottery_money: 0,
            });
          }
        }
        this.setData({
          rankList: tmpList,
        });
      })
      .catch(err => {
        console.log(err);
      });
  },
  handleBack: function() {
    this.setData({
      tipBoxType: 2,
    });
  },
});
```

## File: pages/zfdm/zfdm.json
```json
{
  "navigationBarTitleText": "争分夺秒",
  "disableScroll": true
}
```

## File: pages/zfdm/zfdm.wxml
```
<view class="zfdmContainer">
    <image src="https://static.hudongmiao.com/joymewMp/zfdm/gameTitle.png" class="titleImg"></image>
    <view class="ruleEntry" bindtap="openRuleBox">
        <view class="para">规则</view>
        <view class="para">介绍</view>
    </view>
    <view class="targetTime">本次挑战{{raceTime}}秒</view>
    <view class="timer">{{timestr}}</view>
    <view class="firstFreeTip" wx:if="{{isFree}}">首次挑战免费</view>
    <view class="challengeBtn" bindtap="handleBtnTap" wx:if="{{raceStatus === '0'}}">
        <image src="https://static.hudongmiao.com/joymewMp/zfdm/cBtnText1.png" class="cBtnText1" wx:if="{{!isOnTimer}}"></image>
        <image src="https://static.hudongmiao.com/joymewMp/zfdm/cBtnText2.png" class="cBtnText2" wx:if="{{isOnTimer}}"></image>
    </view>
    <view class="waitTip" wx:if="{{raceStatus === '2'}}">等待主持人开始游戏......</view>
    <!-- 规则 -->
    <view class="ruleWrap" wx:if="{{ruleBoxVisible}}">
        <view class="ruleBox">
            <view class="content">
                <view class="para">1.等待主持人设置一个数字</view>
                <view class="para">2.来宾在手机需要准确的点到设置的数字</view>
                <view class="para">3.每人有多次机会，最接近数字的前8名将会获得奖励</view>
                <view class="para">4.超过1次机会后每次需要支付游戏币，所支付的金额进入红包口袋</view>
                <view class="para">5.游戏时间为2分钟。</view>
            </view>
            <view class="getItBtn" bindtap="getIt">我知道了</view>
            <image src="https://static.hudongmiao.com/joymewMp/zfdm/closeBtn.png" class="closeBtn" bindtap="getIt"></image>
        </view>
    </view>
    <!-- 游戏过程中的我被ko的提示框 -->
    <view class="onTipPopup" wx:if="{{tipVisible && tipBoxType === 4}}">
        <view class="koBoxMe">
            <view class="koller">{{koOtherName}}</view>
            <view class="para1">超越了你的成绩</view>
            <view class="para2">
                击败了全场
                <view class="strong">{{koPercentVal}}</view>
                %的来宾
            </view>
            <view class="para3">
                将获得
                <view class="strong">{{koBonus}}</view>
                元红包
            </view>
        </view>
        <view class="replayBtn" bindtap="replay">拿下TA({{needPrice}}元)</view>
        <view class="confirmBtn" bindtap="closeTipBox">为爱放弃</view>
    </view>
    <!-- 游戏过程中的其他人的ko提示框 -->
    <view class="onTipPopup" wx:if="{{tipVisible && tipBoxType === 3}}">
        <view class="cd">{{cdTxt}}秒</view>
        <view class="koBox">
            <view class="boxHeader">
                <image src="https://static.hudongmiao.com/joymewMp/zfdm/otherKo1.png" class="gx"></image>
                <view class="nameBox">{{koOtherName}}</view>
            </view>
            <view class="boxInfo">
                <view class="p1">
                    他的成绩为
                    <view class="strong">{{resultTime}}</view>
                    秒
                </view>
                <view class="p2">
                    击败了全场
                    <view class="strong">{{koPercentVal}}%</view>
                    的来宾
                </view>
                <view class="p3">
                    将获得
                    <view class="strong">{{koBonus}}</view>
                    元红包
                </view>
            </view>
        </view>
        <view class="replayBtn" bindtap="replay">拿下TA({{needPrice}}元)</view>
        <view class="confirmBtn" bindtap="closeTipBox">关闭</view>
    </view>
    <!-- 游戏过程中的放弃挑战提示框 -->
    <view class="onTipPopup" wx:if="{{tipVisible && tipBoxType === 2}}">
        <view class="tipBox giveup">
            <image class="closeImg" src="https://static.joymew.com/joymewMp/authDialog/closeIcon.png" bindtap="closeTipBox"></image>
            <image src="https://static.hudongmiao.com/joymewMp/zfdm/giveupt3.png" class="t1"></image>
            <view class="cjWrap">
                <view class="cjItem">
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/giveupt2.png" class="keyImg"></image>
                    {{resultTime}}
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/giveupSecond.png" class="unit"></image>
                </view>
                <view class="cjItem">
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/giveupt1.png" class="keyImg2"></image>
                    {{koDis}}
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/giveupSecond.png" class="unit"></image>
                </view>
            </view>
        </view>
        <view class="replayBtn" bindtap="replay">为爱继续（{{needPrice}}元）</view>
        <view class="confirmBtn" bindtap="closeTipBox">为爱放弃</view>
    </view>
    <!-- 游戏过程中的挑战成功提示框 -->
    <view class="onTipPopup" wx:if="{{tipVisible && tipBoxType === 1}}">
        <view class="tipBox">
            <image src="{{avator}}" class="avator"></image>
            <view class="tInfo1">
                <view class="tI1Pra1">
                    击败了全场
                    <view class="strong">{{koPercentVal}}</view>
                    %的来宾
                </view>
                <view class="tI1Pra2">
                    还差
                    <view class="strong2">{{koDis}}</view>
                    秒将获得
                    <view class="strong">{{koBonus}}</view>
                    元红包
                </view>
            </view>
            <view class="tInfo2">
                <image src="https://static.hudongmiao.com/joymewMp/zfdm/scoreKey.png" class="keyImg"></image>
                {{resultTime}}
            </view>
            <view class="tInfo3">
                <view class="tI3Pra1">请实时注意当前排名变化</view>
                <view class="tI3Pra2">1-8名可获得游戏奖励</view>
            </view>
        </view>
        <view class="replayBtn" bindtap="replay">为爱继续挑战（{{needPrice}}元）</view>
        <view class="confirmBtn" bindtap="handleBack">为爱放弃</view>
    </view>
    <!-- 游戏过程中的挑战失败提示框 -->
    <view class="onTipPopup" wx:if="{{tipVisible && tipBoxType === 0}}">
        <view class="tipBox fail">
            <image src="{{avator}}" class="avator"></image>
            <view class="tInfo1 fail">
                <image src="https://static.hudongmiao.com/joymewMp/zfdm/onFailTip2.png" class="keyImg"></image>
                {{resultTime}}
            </view>
            <view class="tInfo2 fail">
                <image src="https://static.hudongmiao.com/joymewMp/zfdm/onFailTip3.png" class="keyImg"></image>
                {{currentRank}}
            </view>
            <view class="tInfo3">
                <view class="tI3Pra1">请实时注意当前排名变化</view>
                <view class="tI3Pra2">1-8名可获得游戏奖励</view>
            </view>
        </view>
        <view class="replayBtn" bindtap="replay">再来一次（{{needPrice}}元）</view>
        <view class="confirmBtn" bindtap="handleBack">返回</view>
    </view>
    <!-- 排行榜 -->
    <view class="rankWrap" wx:if="{{raceStatus === '1'}}">
        <view class="rankBox">
            <view class="rankItem {{(index === 0 || index === 1 || index === 2)?'topThree':''}}" wx:for="{{rankList}}" wx:key="index">
                <view class="rankNum" wx:if="{{index === 0}}">
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/firstMedal.png" class="medal"></image>
                </view>
                <view class="rankNum" wx:if="{{index === 1}}">
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/secondMedal.png" class="medal"></image>
                </view>
                <view class="rankNum" wx:if="{{index === 2}}">
                    <image src="https://static.hudongmiao.com/joymewMp/zfdm/thirdMedal.png" class="medal"></image>
                </view>
                <view class="rankNum" wx:if="{{index > 2}}">{{index + 1}}</view>
                <image src="{{item.avator}}" class="avator"></image>
                <view class="nickname">{{item.wx_name}}</view>
                <view class="cTime">{{item.guess_money}}秒</view>
                <view class="money">{{item.lottery_money}}元</view>
            </view>
        </view>
    </view>
</view>
```

## File: pages/zfdm/zfdm.wxss
```
.zfdmContainer {
  position: absolute;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/bg.png');
  background-size: 100% 100%;
}
.zfdmContainer > .titleImg {
  width: 562rpx;
  height: 378rpx;
}
.zfdmContainer > .ruleEntry {
  width: 108rpx;
  height: 83rpx;
  background-image: url('https://static.joymew.com/joymewMp/zfdm/ruleEntry.png');
  background-size: 100% 100%;
  position: absolute;
  right: 0;
  top: 124rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.ruleEntry > .para {
  font-size: 24rpx;
  color: rgba(255, 255, 255, 0.5);
}
.zfdmContainer > .targetTime {
  width: 482rpx;
  height: 134rpx;
  background-image: url('https://static.joymew.com/joymewMp/zfdm/targetBox.png');
  background-size: 100% 100%;
  display: flex;
  justify-content: center;
  line-height: 122rpx;
  font-size: 42rpx;
  font-weight: 400;
  color: #d83607;
}
.zfdmContainer > .timer {
  width: 606rpx;
  height: 182rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/timeBg.png');
  background-size: 100% 100%;
  margin-top: 20rpx;
  font-size: 80rpx;
  font-weight: 500;
  color: #cf2322;
  letter-spacing: 35rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 30rpx;
}

.zfdmContainer > .firstFreeTip {
  margin-top: 20rpx;
  font-size: 32rpx;
  color: #ffffff;
}
.zfdmContainer > .waitTip {
  font-size: 32rpx;
  color: #ffffff;
  margin-top: 32rpx;
}
.zfdmContainer > .challengeBtn {
  width: 250rpx;
  height: 250rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/cBtnNew.png');
  background-size: 100% 100%;
}
.challengeBtn > .cBtnText1 {
  width: 102rpx;
  height: 98rpx;
}
.challengeBtn > .cBtnText2 {
  width: 102rpx;
  height: 50rpx;
}
.ruleWrap {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
}
.ruleWrap > .ruleBox {
  width: 624rpx;
  height: 796rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/ruleBox.png');
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
}
.ruleWrap > .ruleBox > .content {
  margin-top: 148rpx;
}

.ruleWrap > .ruleBox > .content > .para {
  font-size: 28rpx;
  font-weight: 400;
  color: #333333;
  padding: 0 30rpx;
  margin: 15rpx 0;
}
.ruleWrap > .ruleBox > .getItBtn {
  width: 336rpx;
  height: 72rpx;
  background-color: #fde37a;
  border-radius: 36rpx;
  position: absolute;
  bottom: 62rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 36rpx;
  font-weight: 400;
  color: #e07717;
}
.ruleWrap > .ruleBox > .closeBtn {
  width: 68rpx;
  height: 70rpx;
  position: absolute;
  bottom: -114rpx;
}
.onTipPopup {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.onTipPopup > .tipBox {
  width: 710rpx;
  height: 860rpx;
  background-image: url('https://static.joymew.com/joymewMp/zfdm/challengeSuccessBg.png');
  background-size: 100% 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  position: relative;
  padding-top: 350rpx;
}
.tipBox.fail {
  width: 674rpx;
  height: 876rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/onFailTip1.png');
}
.tipBox > .avator {
  width: 88rpx;
  height: 88rpx;
  position: absolute;
  top: 36rpx;
  border-radius: 50%;
}
.tipBox > .tInfo1 {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 505rpx;
}
.tipBox > .tInfo1 > .tI1Pra1 {
  font-size: 30rpx;
  font-weight: 400;
  color: #333333;
  display: flex;
  align-items: flex-end;
}
.tipBox > .tInfo1 > .tI1Pra1 > .strong {
  font-size: 46rpx;
  color: #fb4a40;
  line-height: 45rpx;
}
.tipBox > .tInfo1 > .tI1Pra2 {
  font-size: 30rpx;
  font-weight: 400;
  color: #333333;
  display: flex;
  align-items: flex-end;
  margin-top: 20rpx;
}
.tipBox > .tInfo1.fail {
  font-size: 63rpx;
  font-weight: 700;
  color: #5f4d8c;
  letter-spacing: 3rpx;
  justify-content: space-between;
  flex-direction: row;
  width: 520rpx;
}
.tipBox > .tInfo1.fail > .keyImg {
  width: 286rpx;
  height: 58rpx;
}
.tipBox > .tInfo1 > .tI1Pra2 > .strong2 {
  color: #fb4a40;
}
.tipBox > .tInfo1 > .tI1Pra2 > .strong {
  font-size: 46rpx;
  color: #fb4a40;
  line-height: 45rpx;
}
.tipBox > .tInfo2 {
  width: 512rpx;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 63rpx;
  font-weight: 700;
  color: #fb4a40;
  margin-top: 60rpx;
}
.tipBox > .tInfo2.fail {
  color: #5f4d8c;
  width: 520rpx;
}
.tipBox > .tInfo2 > .keyImg {
  width: 253rpx;
  height: 51rpx;
}

.tipBox > .tInfo3 {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 345rpx;
  font-size: 30rpx;
  font-weight: 500;
  color: #666666;
  letter-spacing: 2rpx;
  margin-top: 120rpx;
}
.tipBox > .tInfo3 > .tI3Pra1 {
  margin-bottom: 18rpx;
}

.tipBox.giveup {
  width: 622rpx;
  height: 458rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/giveupBox.png');
  padding-top: 75rpx;
}
.tipBox.giveup > .t1 {
  width: 472rpx;
  height: 42rpx;
}
.tipBox.giveup > .cjWrap {
  width: 521rpx;
  height: 224rpx;
  margin-top: 92rpx;
}
.tipBox.giveup > .cjWrap > .cjItem {
  width: 521rpx;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  font-size: 46rpx;
  font-weight: 700;
  color: #fb4a40;
  line-height: 37rpx;
}
.tipBox.giveup > .cjWrap > .cjItem:nth-child(2) {
  margin-top: 40rpx;
}
.tipBox.giveup > .cjWrap > .cjItem > .keyImg {
  width: 228rpx;
  height: 33rpx;
  margin-right: 10rpx;
}
.tipBox.giveup > .cjWrap > .cjItem > .keyImg2 {
  width: 264rpx;
  height: 33rpx;
  margin-right: 10rpx;
}
.tipBox.giveup > .cjWrap > .cjItem > .unit {
  width: 33rpx;
  height: 32rpx;
  margin-left: 10rpx;
}
.tipBox.giveup > .closeImg {
  width: 44rpx;
  height: 44rpx;
  position: absolute;
  top: -24rpx;
  left: 615rpx;
  z-index: 1;
}
.onTipPopup > .replayBtn {
  width: 670rpx;
  height: 104rpx;
  background: #fdf1ac;
  border-radius: 52rpx;
  margin-top: 50rpx;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 40rpx;
  font-weight: 700;
  color: #e07717;
  letter-spacing: 2rpx;
}
.onTipPopup > .confirmBtn {
  font-size: 32rpx;
  font-weight: 400;
  color: rgba(255, 255, 255, 0.4);
  margin-top: 30rpx;
  letter-spacing: 2rpx;
}
.onTipPopup > .koBox {
  width: 686rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 40rpx;
}
.onTipPopup > .cd {
  width: 94rpx;
  height: 46rpx;
  background: rgba(255, 255, 255, 0.4);
  border-radius: 66px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 28rpx;
  font-weight: 400;
  color: #ffffff;
  position: absolute;
  right: 38rpx;
  top: 38rpx;
}
.koBox > .boxHeader {
  width: 439rpx;
  height: 439rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/otherKo2.png');
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.koBox > .boxHeader > .gx {
  width: 336rpx;
  height: 239rpx;
}
.koBox > .boxHeader > .nameBox {
  width: 520rpx;
  height: 143rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/otherKo3.png');
  background-size: 100% 100%;
  overflow: hidden;
  text-align: center;
  text-overflow: ellipsis;
  white-space: nowrap;
  font-size: 52rpx;
  font-weight: 500;
  color: #ffffff;
  line-height: 143rpx;
  padding: 0 20rpx;
}
.koBox > .boxInfo {
  width: 686rpx;
  font-size: 56rpx;
  font-weight: 400;
  color: #ffffff;
}
.koBox > .boxInfo > .p1 {
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  margin-top: 20rpx;
}
.koBox > .boxInfo > .p1 > .strong {
  color: #fb4a40;
}
.koBox > .boxInfo > .p2 {
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: center;
}
.koBox > .boxInfo > .p2 > .strong {
  color: #fb4a40;
}
.koBox > .boxInfo > .p3 {
  margin-top: 50rpx;
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  line-height: 50rpx;
}
.koBox > .boxInfo > .p3 > .strong {
  font-size: 88rpx;
  color: #fb4a40;
}
.onTipPopup > .koBoxMe {
  width: 658rpx;
  height: 647rpx;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/challengeFailBg.png');
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 322rpx;
}
.koBoxMe > .koller {
  width: 605rpx;
  text-align: center;
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 56rpx;
  font-weight: 700;
  color: #ffbe23;
  white-space: nowrap;
}
.koBoxMe > .para1 {
  font-size: 30rpx;
  font-weight: 400;
  color: #333333;
  margin-top: 25rpx;
}
.koBoxMe > .para2 {
  font-size: 30.16rpx;
  font-weight: 400;
  color: #333333;
  display: flex;
  align-items: flex-end;
}
.koBoxMe > .para2 > .strong {
  color: #fb4a40;
}
.koBoxMe > .para3 {
  font-size: 30rpx;
  font-weight: 400;
  color: #333333;
  display: flex;
  align-items: flex-end;
  margin-top: 15rpx;
}
.koBoxMe > .para3 > .strong {
  color: #fb4a40;
  font-size: 45rpx;
}
.rankWrap {
  position: absolute;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url('https://static.hudongmiao.com/joymewMp/zfdm/rankBg.png');
  background-size: 100% 100%;
}
.rankWrap > .rankBox {
  width: 670rpx;
  height: 1175rpx;
  background: #fef1cf;
  border-radius: 56rpx;
  padding: 30rpx 0;
}
.rankBox > .rankItem {
  display: flex;
  align-items: center;
  width: 100%;
  position: relative;
  margin-bottom: 40rpx;
  padding-left: 5rpx;
}
.rankBox > .rankItem.topThree {
  margin-bottom: 10rpx;
}
.rankBox > .rankItem > .rankNum {
  font-size: 60rpx;
  font-weight: 400;
  color: #a47d18;
  width: 116rpx;
  text-align: center;
}
.rankNum > .medal {
  width: 116rpx;
  height: 132rpx;
}
.rankBox > .rankItem > .avator {
  width: 60rpx;
  height: 60rpx;
  border-radius: 50%;
  margin-left: 5rpx;
}
.rankBox > .rankItem > .nickname {
  width: 198rpx;
  font-size: 28rpx;
  font-weight: 400;
  text-align: left;
  color: #7a2309;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
  margin-left: 24rpx;
}
.rankBox > .rankItem > .cTime {
  color: #7d00fd;
  font-size: 28rpx;
  font-weight: 400;
  margin-left: 10rpx;
}
.rankBox > .rankItem > .money {
  font-size: 28rpx;
  font-weight: 400;
  color: #fd0000;
  position: absolute;
  right: 20rpx;
}
@media screen and (min-height: 720px) {
  .zfdmContainer > .targetTime {
    margin-top: 30rpx;
  }
  .zfdmContainer > .timer {
    margin-top: 40rpx;
  }
  .zfdmContainer > .firstFreeTip {
    margin-top: 40rpx;
  }
  .zfdmContainer > .challengeBtn {
    margin-top: 40rpx;
  }
}
```

## File: pages/zyz/zyz.js
```javascript
import { timeoutTask, showWxToast } from '../../utils/index';
import { getPoolMoney, getZyzInfo, getZyzRank, zyzRecharge, startZyz, sendPrizeInfo, sendBroadCast } from '../../api/zyz/zyz';
import { wxPay } from '../../api/pay';
import defaultContent from '../../assets/constant/default';

const zhufuList = [
    '美酒佳肴,不甚荣幸',
    '醉酒饱德，不胜感激',
    '小小红包,感谢招待',
    '感谢招待,祝愿安康',
];
// 礼物数组
const giftList = [
    {
        id: 1,
        gift: 'rocket1',
        name: '火箭小号',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket1.png',
        isChoosed: true
    }, {
        id: 2,
        gift: 'rocket2',
        name: '火箭中号',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket2.png',
        isChoosed: false
    }, {
        id: 3,
        gift: 'rocket3',
        name: '大号大号',
        imgUrl: 'https://static.hudongmiao.com/joymewMp/zyz/rocket3.png',
        isChoosed: false
    }
];

let tmpInterval = null; //用于倒计时
let tmpInterval2 = null; //用于轮询
let lock = false; //锁，用于确保 倒计时方法 一轮只调用一次
let lock2 = false;//锁，用于确保 执行动画的过程中不可以点按钮
let lock3 = false;//锁，用于确保 开始按钮不能连续点击
Page({
    data: {
        luckyMoney: 0,
        wheelRodateDeg: 0,
        isLuckyShow: false,
        luckyAni: '',
        gameStatus: 1, // 转一转状态(控制页面显示)
        prizeItemList: [],// 奖项列表(带汉字单位)
        prizeItemValList: [],// 奖项数值列表(不带汉字单位) 
        poolMoney: 0, //奖池金额
        countDownNum: 0,// 倒计时
        isEntry: false,// 充值入口
        topRankList: [],// 排行榜列表
        otherRankList: [],
        userId: '',
        openId: '',
        name: '',
        headImg: '',
        turnId: '', //一场 转一转的id 0代表要充值 否则代表这场 转一转的id
        giftList: giftList,
    },
    onLoad: function (options) {
        lock = false;
        lock2 = false;
        lock3 = false;
        tmpInterval = null;
        tmpInterval2 = null;
        this.setData({
            userId: options.userId,
            openId: options.openId,
            name: options.name,
            headImg: options.headImg,
            prizeItemList: options.zyzList.split(','),
            prizeItemValList: options.zyzList.replace(/[\u4e00-\u9fa5]/g, '').split(','),

        });
        this.requestPoolMoney();
    },
    onShow: function () {
        this.toGame();
    },
    onHide: function () {
        //清除定时器
        clearInterval(tmpInterval);
        clearInterval(tmpInterval2);
        tmpInterval = null;
        tmpInterval2 = null;
        lock = false;
    },
    onUnload: function () {
        //清除定时器
        clearInterval(tmpInterval);
        clearInterval(tmpInterval2);
        tmpInterval = null;
        tmpInterval2 = null;
    },
    showLucky() {
        this.setData({
            luckyAni: 'showLuckyAni',
            isLuckyShow: true,
        });
        // 4s后消失
        timeoutTask(() => {
            this.setData({
                luckyAni: 'hideLuckyAni',
            });
            timeoutTask(() => {
                this.setData({
                    isLuckyShow: false,
                });
            }, 100);
        }, 4000)
    },
    tapstartNyn() {
        getZyzInfo().then((res) => {
            console.log(res);
            this.setData({
                turnId: res.data.id
            });
            this.startGame();
        }).catch((err) => {
            console.log(err);
            showWxToast('网络异常');
        });
    },
    // 选择礼物
    chooseGift(e) {
        console.log(e)
        const choosedId = e.currentTarget.dataset.id;
        const tmpGiftList = this.data.giftList;
        tmpGiftList.forEach(item => {
            if (item.id === choosedId) {
                item.isChoosed = true;
            } else {
                item.isChoosed = false;
            }
        });
        this.setData({
            giftList: tmpGiftList
        });
    },
    // 转一转动画
    gameAniStart(endMoney) {
        let endIndex = this.findIndexByPrizeItem(endMoney);
        // 转盘当前选中项
        let nowIndex = 0;
        // 圈数(周期)
        let circle = 0;
        //转盘 加速阶段 缓冲阶段(确保<=5)
        //情况1：前三个周期->最后一个周期小于5   ani1 ani2
        //情况2:前三个周期->最后一个周期大于5   ani1 + endIndex-4
        let step1 = setInterval(() => {
            if (nowIndex === 9) {
                nowIndex = 0;
                this.setData({
                    wheelRodateDeg: (nowIndex * 36)
                });
                circle += 1;
            }
            if (circle === 3) {
                // 三圈后判断是否进入缓冲阶段
                if (endIndex < 4) {
                    clearInterval(step1);
                    let step2 = setInterval(() => {
                        if (nowIndex === endIndex) {
                            clearInterval(step2);
                            this.setData({
                                wheelRodateDeg: (nowIndex * 36)
                            });
                            timeoutTask(() => {
                                this.showLucky();
                            }, 500);
                        } else {
                            this.setData({
                                wheelRodateDeg: (nowIndex * 36)
                            })
                            if (nowIndex == 9) {
                                nowIndex = 0;
                            } else {
                                nowIndex += 1;
                            }
                        }
                    }, 500);
                } else {
                    //加速阶段停止位置 endIndex-4
                    if (nowIndex === (endIndex - 4)) {
                        clearInterval(step1);
                        let step2 = setInterval(() => {
                            if (nowIndex === endIndex) {
                                clearInterval(step2);
                                this.setData({
                                    wheelRodateDeg: (nowIndex * 36)
                                })
                                timeoutTask(() => {
                                    this.showLucky();
                                }, 500);
                            } else {
                                this.setData({
                                    wheelRodateDeg: (nowIndex * 36)
                                })
                                if (nowIndex == 9) {
                                    nowIndex = 0;
                                } else {
                                    nowIndex += 1;
                                }
                            }
                        }, 500)
                    } else {
                        this.setData({
                            wheelRodateDeg: (nowIndex * 36)
                        })
                        nowIndex += 1;
                    }
                }
            } else {
                this.setData({
                    wheelRodateDeg: (nowIndex * 36)
                });
                nowIndex += 1;
            }
        }, 100)

    },
    // 充钱玩转一转
    recharge() {
        if (!this.data.isEntry) {
            // 最后十五秒购买入口关闭
            showWxToast('购买入口关闭');
            return;
        }
        if (lock2) {
            return;
        }
        lock2 = true;
        zyzRecharge({
            userId: this.data.userId,
            openId: this.data.openId,
        }).then((res) => {
            console.log(res);
            return wxPay(res);
        }).then(() => {
            showWxToast('礼物发送成功!');
            this.sendGift(this.getChoosedGift());
            // startGame
            timeoutTask(() => {
                console.log('***2s后自动转一转***')
                this.tapstartNyn();
            }, 2000);

        }).catch((err) => {
            console.log(err);
            showWxToast('支付失败!');
            lock2 = false;
        });
    },
    getChoosedGift() {
        return this.data.giftList.find(item => {
            return item.isChoosed;
        });
    },
    sendGift(giftChoosed) {
        let tmpCode = '';
        if (giftChoosed.id == 1) {
            tmpCode = 5002;
        } else if (giftChoosed.id == 2) {
            tmpCode = 6002;
        } else if (giftChoosed.id == 3) {
            tmpCode = 7002;
        }
        const c = JSON.stringify({
            code: tmpCode,
            param: {
                headImg: this.data.headImg,
                nickname: this.data.name,
                wish: zhufuList[parseInt(Math.random() * 3)]
            }
        });
        sendBroadCast({
            c,
        });
    },
    // 转一转
    startGame() {
        startZyz({
            turnId: this.data.turnId,
        }).then((res) => {
            console.log('startNyn result:', res);
            //res.data.desc 奖项；endMoney中奖的金额；totalMoney 奖池金额
            //奖池金额刷新
            if (res.data.totalMoney.remainCoin) {
                this.setData({
                    poolMoney: res.data.totalMoney.remainCoin
                })
            }
            this.setData({
                luckyMoney: res.data.endMoney,
            });
            // 转一转动画开始
            this.gameAniStart(res.data.endMoney);

            // 4s动画停止后发送广播(必须要中奖的情况)
            if (parseInt(res.data.endMoney) > 0) {
                timeoutTask(() => {
                    this.sendBroad(res.data.endMoney, res.data.totalMoney.balance);
                }, 4000);
            }
            timeoutTask(() => {
                lock2 = false;
            }, 4000);
        }).catch((err) => {
            console.log(err);
            lock2 = false;
        });
    },
    // 点击进入 转一转
    toGame() {
        if (lock3) {
            return;
        }
        lock3 = true;
        this.requestGameInitInfo();
    },
    // 获取奖池金额
    requestPoolMoney() {
        getPoolMoney().then((res) => {
            console.log(res);
            this.setData({
                poolMoney: res.data.balance
            });
        }).catch((err) => {
            console.log(err);
        });
    },
    // 获取 转一转相关信息
    requestGameInitInfo() {
        getZyzInfo().then((res) => {
            console.log('***获取转一转基本信息***');
            console.log(res);
            //res.data.id 发送礼物 1转一转
            if (res.data.id == 0) {
                this.setData({
                    turnId: res.data.id
                })
            } else {
                this.setData({
                    turnId: res.data.id
                })
            }
            // 时间处理(用于倒计时) res.data.endTime
            if (res.data.endTime === '0') {
                //  转一转未开始的情况处理
                showWxToast(' 转一转尚未开始!');
            } else {
                let countTime = this.timeHandle(res.data.endTime);
                console.log('***接口返回endTime***');
                console.log(res.data.endTime);
                this.countDown(countTime);
                this.setData({
                    gameStatus: 2,
                });
                // 轮询获取充值和中奖列表
                if (!tmpInterval2) {
                    tmpInterval2 = setInterval(() => {
                        this.requestTipList();
                    }, 4000);
                }
            }
            lock3 = false;
        }).catch((err) => {
            console.log(err);
            lock3 = false;
        });
    },
    timeHandle(endTime) {
        //获取当前时间戳
        var nowTime = (new Date()).getTime();
        var subTime = parseInt((parseInt(endTime) - parseInt(nowTime)) / 1000);
        if (subTime < 0) {
            subTime = 0;
        }
        return subTime;
    },
    countDown(second) {
        if (lock == false && !tmpInterval) {
            lock = true;
            tmpInterval = setInterval(() => {
                if (second <= 1) {
                    this.setData({
                        isEntry: false,
                        countDownNum: second
                    })
                    this.requestRankList();
                } else {
                    second -= 1;
                    if (second <= 15) {
                        this.setData({
                            isEntry: false
                        })
                    } else {
                        this.setData({
                            isEntry: true
                        })
                    }
                    this.setData({
                        countDownNum: second
                    })
                }
            }, 1000)
        }
    },
    // 获取排行榜列表
    requestRankList() {
        getZyzRank().then((res) => {
            console.log(res);
            lock = false;
            let tmpTopRankArray = [];
            let tmpOtherRankArray = [];
            let count = 0;
            let tmpLen = res.data.list.length;
            // 限制中奖名单人数最多不超过10个
            if (tmpLen > 10) {
                tmpLen = 10;
            }
            while (count < tmpLen) {
                if (count < 3) {
                    tmpTopRankArray.push({
                        nickname: res.data.list[count].wx_name,
                        headimgurl: res.data.list[count].avator,
                        money: Math.floor(parseFloat(res.data.list[count].money))
                    });
                } else {
                    tmpOtherRankArray.push({
                        num: count < 0 ? `0${count + 1}` : (count + 1),
                        nickname: res.data.list[count].nickname,
                        headimgurl: res.data.list[count].headimgurl,
                        money: Math.floor(parseFloat(res.data.list[count].money))
                    });
                }
                count += 1;
            }
            if (tmpTopRankArray.length < 3) {
                const tmpLen2 = tmpTopRankArray.length;
                for (let i = tmpLen2; i < 3; i += 1) {
                    tmpTopRankArray.push({
                        nickname: 'Player',
                        headimgurl: defaultContent.defaultHeadImg,
                        money: 0,
                    });
                }
            }
            // 不足七个补齐
            if (tmpOtherRankArray.length < 7) {
                const tmpLen3 = tmpOtherRankArray.length;
                for (let i = tmpLen3; i < 7; i += 1) {
                    tmpOtherRankArray.push({
                        num: i + 3 < 0 ? `0${i + 4}` : (i + 4),
                        nickname: 'Player',
                        headimgurl: defaultContent.defaultHeadImg,
                        money: 0,
                    });
                }
            }

            console.log(tmpOtherRankArray);
            this.setData({
                topRankList: tmpTopRankArray,
                otherRankList: tmpOtherRankArray,
                gameStatus: 3,
            });
            // 停止轮询
            clearInterval(tmpInterval2);
            clearInterval(tmpInterval);
            tmpInterval = null;
            tmpInterval2 = null;
        }).catch((err) => {
            console.log(err);
        });
    },
    // 发广播
    sendBroad(golds, remainCoins) {
        sendPrizeInfo({
            gold: golds,
            remainCoin: remainCoins,
            turnId: this.data.turnId,
        }).then((res) => {
            console.log(res);
        }).catch((err) => {
            console.log(err);
            showWxToast('网络异常');
        });
    },
    // 根据奖项查找下标
    findIndexByPrizeItem(prizeItem) {
        let tmpLen = this.data.prizeItemValList.length;
        let tmpArr = this.data.prizeItemValList;
        let tmpIndex = -1;
        for (let i = 0; i < tmpLen; i += 1) {
            if (tmpArr[i] === prizeItem) {
                tmpIndex = i;
                break;
            }
        }
        return tmpIndex;
    },
    // 获取充值和中奖列表
    requestTipList() {
        getPoolMoney().then((res) => {
            console.log(res);
            const subTime = this.timeHandle(res.data.endTime);
            if (subTime <= 0) {
                //  转一转提前结束
                this.requestRankList();
            }
            this.setData({
                poolMoney: res.data.balance,
            })
        }).catch((err) => {
            console.log(err);
        })
    },
    toAgreement: function () {
        wx.navigateTo({
            url: '/pages/agreement/agreement'
        });
    },
});
```

## File: pages/zyz/zyz.json
```json
{
  "navigationBarTitleText": "转一转",
  "usingComponents": {
    "feedbackEntry": "../../components/feedbackEntry/feedbackEntry"
  },
  "disableScroll":true
}
```

## File: pages/zyz/zyz.wxml
```
<view class="zyzContainer">
    <view class="bgArea">
        <image src="https://static.hudongmiao.com/joymewMp/zyz/zyzBg2.png" class="bg" mode="widthFix" wx:if="{{gameStatus === 1 || gameStatus === 2}}"></image>
        <image src="https://static.hudongmiao.com/joymewMp/zyz/rankBg.png" class="bg" mode="widthFix" wx:if="{{gameStatus === 3}}"></image>
        <view class="shade" wx:if="{{gameStatus === 1 || gameStatus === 2}}"></view>
        <image src="https://static.hudongmiao.com/joymewMp/zyz/title.png" class="title" wx:if="{{gameStatus === 2}}"></image>
    </view>
    <!-- 等待界面 -->
    <view class="waitContainer" wx:if="{{gameStatus === 1}}">
        <!-- 奖池金额 -->
        <view class="totalMoney">
            奖池总金额: {{poolMoney}}元
            <image src="https://static.hudongmiao.com/joymewMp/zyz/coins.png" class="coinsImg"></image>
        </view>
        <view class="ruleBox">
            <image src="https://static.hudongmiao.com/joymewMp/zyz/ruleBox.png" class="ruleBoxImg" mode="widthFix"></image>
            <view class="ruleContent">
                <view class="para">1、主持人点击开始按钮， 转一转立即开始；</view>
                <view class="para">2、 转一转时长150秒，在倒计时结束前单个参与者可以不限次数参与 转一转；</view>
                <view class="para">3、参与者购买高级别弹幕后，系统将免费赠送机会；</view>
                <view class="para">4、所有奖项均为随机事件，参与者的消费将计入总奖池，中奖者的奖金将从奖池中扣除。</view>
            </view>
        </view>
        <view class="giftListWrap">
            <view class="giftItem {{item.isChoosed?'active':''}}" wx:for="{{giftList}}" wx:key="id" data-id="{{item.id}}" bindtap='chooseGift'>
                <view class="fudai"></view>
                <image src="{{item.imgUrl}}" class="giftImg g{{index+1}}"></image>
            </view>
        </view>
        <view class="startBtn" bindtap="toGame"></view>
    </view>
    <!--  转一转界面 -->
    <view class="gameContainer" wx:if="{{gameStatus === 2}}">
        <!-- 奖池金额 -->
        <view class="totalMoney">
            奖池总金额: {{poolMoney}}元
            <image src="https://static.hudongmiao.com/joymewMp/zyz/coins.png" class="coinsImg"></image>
        </view>
        <!-- 转盘区域 -->
        <view class="wheelArea">
            <image src="https://static.hudongmiao.com/joymewMp/zyz/wheelBorder.png" class="wheelBorderImg"></image>
            <image src="https://static.hudongmiao.com/joymewMp/zyz/wheel.png" class="wheelImg"></image>
            <image src="https://static.hudongmiao.com/joymewMp/zyz/wheelInner.png" class="wheelInnerImg" style="transform:{{'rotate('+wheelRodateDeg+'deg)'}}"></image>
            <image src="https://static.hudongmiao.com/joymewMp/zyz/wheelBtn.png" class="wheelBtn"></image>
            <view class="countdown">
                <view class="time">{{countDownNum}}</view>
                <view class="timeKey">倒计时</view>
            </view>
            <view class="prizeWrap">
                <view class="prizeItem" wx:for="{{prizeItemList}}" wx:key="index">
                    <view class="prizeName">{{item}}</view>
                    <image src="https://static.joymew.com/joymewMp/zyz/hb.png" class="hbImg" wx:if="{{index !== 3 && index !== 8}}"></image>
                </view>
            </view>
        </view>
        <!-- 选择发送礼物 -->
        <!-- <view class="tip">发送任意弹幕礼物，系统将免费赠送一次转盘抽奖机会</view> -->
        <view class="agreement" bindtap='toAgreement'>阅读并同意《充值服务协议》</view>
        <view class="giftListWrap">
            <view class="giftItem {{item.isChoosed?'active':''}}" wx:for="{{giftList}}" wx:key="id" data-id="{{item.id}}" bindtap='chooseGift'>
                <view class="fudai"></view>
                <image src="{{item.imgUrl}}" class="giftImg g{{index+1}}"></image>
            </view>
        </view>
        <view class="startBtn">
            <view class="text" bindtap="recharge">发送礼物</view>
        </view>
        <!-- 中奖结果 -->
        <view class="luckyWrap {{luckyAni}}" wx:if="{{isLuckyShow}}">
            <view class="tit">中奖啦</view>
            <view class="congragulations">
                恭喜你! 获得
                <text>{{luckyMoney}}</text>
                元红包!
            </view>
            <view class="wechatTip">微信已实时到账</view>
            <view class="money">{{luckyMoney}}元</view>
        </view>
    </view>
    <!--  转一转排行榜界面 -->
    <view class="rankContainer" wx:if="{{gameStatus === 3}}">
        <view class="firstLucky" wx:if="{{topRankList[0]}}">
            <view class="num">
                <view class="text">1</view>
            </view>
            <view class="headImgBox">
                <image src="{{topRankList[0].headimgurl}}" class="headImg"></image>
            </view>
            <view class="name">
                <view class="text">{{topRankList[0].nickname}}</view>
            </view>
            <view class="money">
                <view class="text">{{topRankList[0].money}}元</view>
            </view>
        </view>
        <view class="secondLucky" wx:if="{{topRankList[1]}}">
            <view class="num">
                <view class="text">2</view>
            </view>
            <view class="headImgBox">
                <image src="{{topRankList[1].headimgurl}}" class="headImg"></image>
            </view>
            <view class="name">
                <view class="text">{{topRankList[1].nickname}}</view>
            </view>
            <view class="money">
                <view class="text">{{topRankList[1].money}}元</view>
            </view>
        </view>
        <view class="thirdLucky" wx:if="{{topRankList[2]}}">
            <view class="num">
                <view class="text">3</view>
            </view>
            <view class="headImgBox">
                <image src="{{topRankList[2].headimgurl}}" class="headImg"></image>
            </view>
            <view class="name">
                <view class="text">{{topRankList[2].nickname}}</view>
            </view>
            <view class="money">
                <view class="text">{{topRankList[2].money}}元</view>
            </view>
        </view>
        <view class="otherWrap">
            <view class="otherLuckyList">
                <view class="item" wx:for="{{otherRankList}}" wx:key="index">
                    <view class="left">
                        <view class="num">{{ item.num }}</view>
                        <view class="headImgBox">
                            <image src="{{item.headimgurl}}" class="headImg"></image>
                        </view>
                        <view class="name">{{item.nickname}}</view>
                    </view>
                    <view class="right">{{item.money}}元</view>
                </view>
            </view>
        </view>
        <!-- 反馈入口 -->
        <feedbackEntry userId="{{userId}}"></feedbackEntry>
    </view>
</view>
```

## File: pages/zyz/zyz.wxss
```
.zyzContainer {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}

/* 公共背景区域 */
.zyzContainer>.bgArea {
  width: 100%;
  position: absolute;
}

.zyzContainer>.bgArea>.bg {
  width: 105%;
  height: 100%;
  position: absolute;
  left: -2%;
}

.zyzContainer>.bgArea>.shade {
  width: 100vw;
  height: 100vh;
  opacity: 0.6;
  background-color: #000000;
  position: absolute;
  top: 0;
  left: 0;
}

.zyzContainer>.bgArea>.title {
  position: absolute;
  width: 101%;
  height: 185rpx;
  top: -10rpx;
  left: -3rpx;
}


/* 等待界面 */
.zyzContainer>.waitContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.zyzContainer>.waitContainer>.totalMoney {
  position: absolute;
  top: 0rpx;
  width: 526rpx;
  height: 70rpx;
  background: #AC0C00;
  box-shadow: 0rpx 3rpx 7rpx 0px #F6544A, 0px 1rpx 3rpx 0rpx rgba(0, 0, 0, 0.35);
  border-radius: 29rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 44rpx;
  color: #FCF5CD;
}

.zyzContainer>.waitContainer>.totalMoney>.coinsImg {
  width: 97rpx;
  height: 80rpx;
  position: absolute;
  left: -59rpx;
}

.zyzContainer>.waitContainer>.ruleBox {
  width: 880rpx;
  height: 740rpx;
  position: absolute;
  top: 186rpx;
  overflow: hidden;
  display: flex;
  justify-content: center;
}

.zyzContainer>.waitContainer>.ruleBox>.ruleBoxImg {
  width: 880rpx;
  top: -65rpx;
  position: absolute;
  left: 70rpx;
}

.zyzContainer>.waitContainer>.ruleBox>.ruleContent {
  font-size: 28rpx;
  font-weight: 400;
  color: #FFFFDA;
  position: absolute;
  width: 475rpx;
  top: 140rpx;
}

.zyzContainer>.waitContainer>.ruleBox>.ruleContent>.para {
  margin: 20rpx 0;
}

.zyzContainer>.waitContainer>.giftListWrap {
  display: flex;
  justify-content: space-around;
  position: absolute;
  top: 860rpx;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem {
  width: 196rpx;
  height: 230rpx;
  position: relative;
  display: flex;
  justify-content: center;
  opacity: 0.3;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem.active {
  opacity: 1;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem>.fudai {
  width: 100%;
  height: 100%;
  position: absolute;
  background-image: url('https://static.joymew.com/joymewMp/zyz/fd1.png');
  background-size: 100% 100%;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem>.giftImg {
  position: absolute;
  top: 61rpx;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem>.giftImg.g1 {
  width: 67rpx;
  height: 157rpx;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem>.giftImg.g2 {
  width: 55rpx;
  height: 159rpx;
}

.zyzContainer>.waitContainer>.giftListWrap>.giftItem>.giftImg.g3 {
  width: 63rpx;
  height: 160rpx;
}

.zyzContainer>.waitContainer>.startBtn {
  width: 390rpx;
  height: 114rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/startBtn.png');
  background-size: 100% 100%;
  position: absolute;
  bottom: 0rpx;
}

/*  转一转界面 */
.zyzContainer>.gameContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.zyzContainer>.gameContainer>.totalMoney {
  position: absolute;
  top: 32rpx;
  width: 526rpx;
  height: 70rpx;
  background: #AC0C00;
  box-shadow: 0rpx 3rpx 7rpx 0px #F6544A, 0px 1rpx 3rpx 0rpx rgba(0, 0, 0, 0.35);
  border-radius: 29rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 44rpx;
  color: #FCF5CD;
}

.zyzContainer>.gameContainer>.totalMoney>.coinsImg {
  width: 97rpx;
  height: 80rpx;
  position: absolute;
  left: -59rpx;
}

.zyzContainer>.gameContainer>.wheelArea {
  width: 681rpx;
  height: 681rpx;
  position: absolute;
  top: 121rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.gameContainer>.wheelArea>.wheelBorderImg {
  position: absolute;
  width: 100%;
  height: 100%;
}

.zyzContainer>.gameContainer>.wheelArea>.wheelImg {
  position: absolute;
  width: 612rpx;
  height: 612rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.wheelInnerImg {
  position: absolute;
  width: 611rpx;
  height: 611rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.wheelBtn {
  position: absolute;
  width: 248rpx;
  height: 248rpx;
  top: 230rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.countdown {
  width: 205rpx;
  height: 205rpx;
  position: absolute;
  top: 273rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.zyzContainer>.gameContainer>.wheelArea>.countdown>.time {
  font-size: 72rpx;
  font-weight: normal;
  color: #DCA96F;
  text-shadow: #5F191B 1rpx 0 0, #5F191B 0 1rpx 0, #5F191B -1rpx 0 0, #5F191B 0 -1rpx 0, #5F191B 2rpx 0 0, #5F191B 0 2rpx 0, #5F191B -2rpx 0 0, #5F191B 0 -2rpx 0;
}

.zyzContainer>.gameContainer>.wheelArea>.countdown>.timeKey {
  font-size: 48rpx;
  color: #DCA96F;
  margin-top: -14rpx;
  text-shadow: #5F191B 1rpx 0 0, #5F191B 0 1rpx 0, #5F191B -1rpx 0 0, #5F191B 0 -1rpx 0, #5F191B 2rpx 0 0, #5F191B 0 2rpx 0, #5F191B -2rpx 0 0, #5F191B 0 -2rpx 0;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap {
  position: absolute;
  width: 100%;
  height: 100%;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem {
  position: absolute;
  width: 169rpx;
  height: 194rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem>.prizeName {
  font-size: 38rpx;
  font-weight: normal;
  color: #2d0800;
  position: absolute;
  width: 120rpx;
  text-align: center;
  white-space: nowrap;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem>.hbImg {
  width: 90rpx;
  height: 109rpx;
  position: absolute;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(1) {
  left: 237rpx;
  top: 51rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(1)>.prizeName {
  left: -34rpx;
  top: 21rpx;
  transform: rotate(-20deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(1)>.hbImg {
  transform: rotate(-41deg);
  top: 77rpx;
  left: 10rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(2) {
  left: 360rpx;
  top: 51rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(2)>.prizeName {
  left: 7rpx;
  top: 22rpx;
  transform: rotate(11deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(2)>.hbImg {
  top: 80rpx;
  left: -11rpx;
  transform: rotate(-8deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(3) {
  left: 437rpx;
  top: 165rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(3)>.prizeName {
  left: 59rpx;
  top: 5rpx;
  transform: rotate(53deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(3)>.hbImg {
  transform: rotate(33deg);
  top: 13px;
  left: 0px;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(4) {
  left: 535rpx;
  top: 271rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(4)>.prizeName {
  left: -53rpx;
  top: 50rpx;
  transform: rotate(0deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(5) {
  left: 642rpx;
  top: 546rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(5)>.prizeName {
  left: -145rpx;
  top: -78rpx;
  transform: rotate(-58deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(5)>.hbImg {
  transform: rotate(-81deg);
  top: -80px;
  left: -108px;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(6) {
  left: 613rpx;
  top: 653rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(6)>.prizeName {
  left: -247rpx;
  top: -81rpx;
  transform: rotate(-22deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(6)>.hbImg {
  transform: rotate(-46deg);
  top: -184rpx;
  left: -262rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(7) {
  left: 405rpx;
  top: 534rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(7)>.prizeName {
  left: -209rpx;
  top: 30rpx;
  transform: rotate(20deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(7)>.hbImg {
  top: -68rpx;
  left: -168rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(8) {
  left: 176rpx;
  top: 398rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(8)>.prizeName {
  left: -106rpx;
  top: 69rpx;
  transform: rotate(57deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(8)>.hbImg {
  top: -5rpx;
  left: -25rpx;
  transform: rotate(36deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(9) {
  left: 273rpx;
  top: 376rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(9)>.prizeName {
  left: -216rpx;
  top: -66rpx;
  transform: rotate(0deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(10) {
  left: 237rpx;
  top: 238rpx;
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(10)>.prizeName {
  left: -162rpx;
  top: -70rpx;
  transform: rotate(-55deg);
}

.zyzContainer>.gameContainer>.wheelArea>.prizeWrap>.prizeItem:nth-child(10)>.hbImg {
  top: -51rpx;
  left: -81rpx;
  transform: rotate(-76deg);
}

.zyzContainer>.gameContainer>.tip {
  font-size: 24rpx;
  font-weight: normal;
  color: #D87446;
  position: absolute;
  top: 815rpx;
  letter-spacing: 2rpx;
}

.zyzContainer>.gameContainer>.agreement {
  font-size: 24rpx;
  font-weight: 400;
  color: #fff;
  position: absolute;
  bottom: 132rpx;
}

.zyzContainer>.gameContainer>.giftListWrap {
  display: flex;
  justify-content: space-around;
  position: absolute;
  top: 800rpx;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem {
  width: 196rpx;
  height: 230rpx;
  position: relative;
  display: flex;
  justify-content: center;
  opacity: 0.3;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem.active {
  opacity: 1;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem>.fudai {
  width: 100%;
  height: 100%;
  position: absolute;
  background-image: url('https://static.joymew.com/joymewMp/zyz/fd1.png');
  background-size: 100% 100%;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg {
  position: absolute;
  top: 61rpx;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg.g1 {
  width: 67rpx;
  height: 157rpx;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg.g2 {
  width: 55rpx;
  height: 159rpx;
}

.zyzContainer>.gameContainer>.giftListWrap>.giftItem>.giftImg.g3 {
  width: 63rpx;
  height: 160rpx;
}

.zyzContainer>.gameContainer>.startBtn {
  width: 390rpx;
  height: 114rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/startBtn2.png');
  background-size: 100% 100%;
  position: absolute;
  bottom: 0rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.gameContainer>.startBtn>.text {
  position: absolute;
  top: 19rpx;
  font-size: 48rpx;
  font-weight: 400;
  color: #C14532;
  background: linear-gradient(177deg, #FCD58E 0%, #F8A65D 99.31640625%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.zyzContainer>.gameContainer>.luckyWrap {
  width: 548rpx;
  height: 607rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: absolute;
  top: 176rpx;
  left: 85rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/prizeResultBox2.png');
  background-size: 100% 100%;
}

.zyzContainer>.gameContainer>.luckyWrap>.tit {
  font-size: 60rpx;
  font-weight: 400;
  color: #D5261D;
  -webkit-text-stroke: 1px #D32F10;
  text-stroke: 1px #D32F10;
  position: absolute;
  top: 85rpx;
}

.zyzContainer>.gameContainer>.luckyWrap>.congragulations {
  font-size: 30rpx;
  font-weight: 400;
  color: #5E493D;
  position: absolute;
  top: 188rpx;
}

.zyzContainer>.gameContainer>.luckyWrap>.congragulations>text {
  color: #D5261D;
  font-size: 48rpx;
}

.zyzContainer>.gameContainer>.luckyWrap>.wechatTip {
  font-size: 24rpx;
  font-weight: normal;
  color: #8C7E77;
  position: absolute;
  top: 251rpx;
}

.zyzContainer>.gameContainer>.luckyWrap>.money {
  font-size: 36rpx;
  font-weight: 400;
  color: #FBA140;
  position: absolute;
  bottom: 105rpx;
}

.showLuckyAni {
  animation: zoomIn 0.1s linear;
}

.hideLuckyAni {
  animation: zoomOut 0.1s linear;
}

@keyframes zoomIn {
  from {
    opacity: 0;
    -webkit-transform: scale3d(0.3, 0.3, 0.3);
    transform: scale3d(0.3, 0.3, 0.3);
  }

  50% {
    opacity: 1;
  }
}

@keyframes zoomOut {
  from {
    opacity: 1;
  }

  50% {
    opacity: 0;
    -webkit-transform: scale3d(0.3, 0.3, 0.3);
    transform: scale3d(0.3, 0.3, 0.3);
  }

  to {
    opacity: 0;
  }
}

/* 排行榜界面 */
.zyzContainer>.rankContainer {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.zyzContainer>.rankContainer>.firstLucky {
  display: flex;
  align-items: center;
  flex-direction: column;
  position: absolute;
  width: 221rpx;
  height: 272rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/moneyBg.png');
  background-size: 100% 100%;
  top: 324rpx;
}

.zyzContainer>.rankContainer>.firstLucky>.num {
  width: 120rpx;
  height: 72rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/nt.png');
  background-size: 100% 100%;
  top: -27rpx;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.firstLucky>.num>.text {
  font-size: 31rpx;
  font-weight: normal;
  color: #fded9e;
  -webkit-text-stroke: 2rpx #57161b;
  text-stroke: 2rpx #57161b;
  background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.zyzContainer>.rankContainer>.firstLucky>.headImgBox {
  position: absolute;
  top: 38rpx;
  width: 78rpx;
  height: 78rpx;
  background: #e88f5d;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.firstLucky>.headImgBox>.headImg {
  border-radius: 50%;
  width: 72rpx;
  height: 72rpx;
}

.zyzContainer>.rankContainer>.firstLucky>.name {
  width: 164rpx;
  height: 43rpx;
  position: absolute;
  top: 125rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/nameBg.png');
  background-size: 100% 100%;
  background-position-x: 10rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.firstLucky>.name>.text {
  width: 124rpx;
  font-size: 24rpx;
  font-weight: normal;
  color: #FDE8E2;
  background: linear-gradient(0deg, #DCA96F 0%, #FFFFFF 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  text-align: center;
}

.zyzContainer>.rankContainer>.firstLucky>.money {
  position: absolute;
  top: 177rpx;
}

.zyzContainer>.rankContainer>.firstLucky>.money>.text {
  font-size: 42rpx;
  color: #fee4de;
  background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}


.zyzContainer>.rankContainer>.secondLucky {
  display: flex;
  align-items: center;
  flex-direction: column;
  position: absolute;
  width: 221rpx;
  height: 272rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/moneyBg.png');
  background-size: 100% 100%;
  top: 355rpx;
  left: 30rpx;
}

.zyzContainer>.rankContainer>.secondLucky>.num {
  width: 59rpx;
  height: 66rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/secondMedal.png');
  background-size: 100% 100%;
  top: -27rpx;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.secondLucky>.num>.text {
  font-size: 31rpx;
  font-weight: normal;
  color: #fded9e;
  -webkit-text-stroke: 2rpx #57161b;
  text-stroke: 2rpx #57161b;
  background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.zyzContainer>.rankContainer>.secondLucky>.headImgBox {
  position: absolute;
  top: 38rpx;
  width: 78rpx;
  height: 78rpx;
  background: #e88f5d;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.secondLucky>.headImgBox>.headImg {
  border-radius: 50%;
  width: 72rpx;
  height: 72rpx;
}

.zyzContainer>.rankContainer>.secondLucky>.name {
  width: 164rpx;
  height: 43rpx;
  position: absolute;
  top: 125rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/nameBg.png');
  background-size: 100% 100%;
  background-position-x: 10rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.secondLucky>.name>.text {
  width: 124rpx;
  font-size: 24rpx;
  font-weight: normal;
  color: #FDE8E2;
  background: linear-gradient(0deg, #DCA96F 0%, #FFFFFF 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  text-align: center;
}

.zyzContainer>.rankContainer>.secondLucky>.money {
  position: absolute;
  top: 177rpx;
}

.zyzContainer>.rankContainer>.secondLucky>.money>.text {
  font-size: 42rpx;
  color: #fee4de;
  background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}


.zyzContainer>.rankContainer>.thirdLucky {
  display: flex;
  align-items: center;
  flex-direction: column;
  position: absolute;
  width: 221rpx;
  height: 272rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/moneyBg.png');
  background-size: 100% 100%;
  top: 355rpx;
  right: 30rpx;
}

.zyzContainer>.rankContainer>.thirdLucky>.num {
  width: 59rpx;
  height: 66rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/thirdMedal.png');
  background-size: 100% 100%;
  top: -27rpx;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.thirdLucky>.num>.text {
  font-size: 31rpx;
  font-weight: normal;
  color: #fded9e;
  -webkit-text-stroke: 2rpx #57161b;
  text-stroke: 2rpx #57161b;
  background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.zyzContainer>.rankContainer>.thirdLucky>.headImgBox {
  position: absolute;
  top: 38rpx;
  width: 78rpx;
  height: 78rpx;
  background: #e88f5d;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.thirdLucky>.headImgBox>.headImg {
  border-radius: 50%;
  width: 72rpx;
  height: 72rpx;
}

.zyzContainer>.rankContainer>.thirdLucky>.name {
  width: 164rpx;
  height: 43rpx;
  position: absolute;
  top: 125rpx;
  background-image: url('https://static.joymew.com/joymewMp/zyz/nameBg.png');
  background-size: 100% 100%;
  background-position-x: 10rpx;
  display: flex;
  justify-content: center;
  align-items: center;
}

.zyzContainer>.rankContainer>.thirdLucky>.name>.text {
  width: 124rpx;
  font-size: 24rpx;
  font-weight: normal;
  color: #FDE8E2;
  background: linear-gradient(0deg, #DCA96F 0%, #FFFFFF 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  text-align: center;
}

.zyzContainer>.rankContainer>.thirdLucky>.money {
  position: absolute;
  top: 177rpx;
}

.zyzContainer>.rankContainer>.thirdLucky>.money>.text {
  font-size: 42rpx;
  color: #fee4de;
  background: linear-gradient(0deg, #db9f69 0%, #ffffff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.zyzContainer>.rankContainer .otherWrap {
  position: absolute;
  width: 100%;
  height: 600rpx;
  overflow-y: scroll;
  top: 641rpx;
  padding-bottom: 40rpx;
}

.zyzContainer>.rankContainer .otherLuckyList {
  position: absolute;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.zyzContainer>.rankContainer .otherLuckyList>.item {
  width: 660rpx;
  height: 90rpx;
  background: #E8CDBB;
  border-radius: 12rpx;
  display: flex;
  justify-content: space-between;
  padding: 0 40rpx;
  margin: 6rpx 0;
}

.zyzContainer>.rankContainer .otherLuckyList>.item>.left {
  display: flex;
  align-items: center;
}

.zyzContainer>.rankContainer .otherLuckyList>.item>.left>.num {
  font-size: 36rpx;
  font-weight: bold;
  color: #FCE67D;
  -webkit-text-stroke: 2rpx #62030F;
  text-stroke: 2rpx #62030F;
}

.zyzContainer>.rankContainer .otherLuckyList>.item>.left>.headImgBox {
  width: 51rpx;
  height: 50rpx;
  border-radius: 12rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #E69269;
  margin-left: 11rpx;
}

.zyzContainer>.rankContainer .otherLuckyList>.item>.left>.headImgBox>.headImg {
  width: 51rpx;
  height: 50rpx;
  border-radius: 12rpx;
}

.zyzContainer>.rankContainer .otherLuckyList>.item>.left>.name {
  width: 180rpx;
  font-size: 30rpx;
  font-weight: bold;
  color: #FFFFFF;
  -webkit-text-stroke: 2rpx #62030F;
  text-stroke: 2rpx #62030F;
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;
  margin-left: 16rpx;
}

.zyzContainer>.rankContainer .otherLuckyList>.item>.right {
  width: 100rpx;
  font-size: 33rpx;
  font-weight: bold;
  color: #9D0A20;
  display: flex;
  align-items: center;
}

@media screen and (min-height: 720px) {
  .zyzContainer>.gameContainer>.agreement {
    font-size: 24rpx;
    font-weight: 400;
    color: #fff;
    position: absolute;
    bottom: 240rpx;
  }
  .zyzContainer>.waitContainer>.ruleBox {
    top: 250rpx;
  }

  .zyzContainer>.waitContainer>.giftListWrap {
    top: 967rpx;
  }

  .zyzContainer>.waitContainer>.startBtn {
    bottom: 91rpx;
  }

  .zyzContainer>.gameContainer>.totalMoney {
    top: 53rpx;
  }

  .zyzContainer>.gameContainer>.wheelArea {
    top: 158rpx;
  }

  .zyzContainer>.gameContainer>.tip {
    top: 852rpx;
  }

  .zyzContainer>.gameContainer>.giftListWrap {
    top: 931rpx;
  }

  .zyzContainer>.gameContainer>.startBtn {
    bottom: 91rpx;
  }

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
  } if (compareDateTime === dateTime) {
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

// 获取当前年月日时分秒
export function getCurrentDate() {
  let d = new Date()
  let year = d.getFullYear()
  let month = d.getMonth()
  month = month + 1 > 12 ? 1 : month + 1
  month = month > 9 ? month : '0' + month.toString()
  let day = d.getDate()
  let hour = d.getHours()
  hour = hour > 9 ? hour : '0' + hour.toString()
  let minute = d.getMinutes()
  minute = minute > 9 ? minute : '0' + minute.toString()
  let second = d.getSeconds()
  return `${year}-${month}-${day} ${hour}:${minute}:${second}`
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

export const showWxToast = pTip => {
  if (!wxToastLock && !wxLoadingLock) {
    wxToastLock = true;
    wx.showToast({
      title: pTip,
      icon: 'none',
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

export const showWxLoading = pTip => {
  if (!wxToastLock && !wxLoadingLock) {
    wxLoadingLock = true;
    wx.showLoading({
      title: pTip,
      mask: true,
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
    wx.hideLoading();
    wxLoadingLock = false;
  } else {
    console.log('特殊情况hideWxLoading');
  }
};
const hideWxToast = () => {
  if (wxToastLock) {
    wx.hideToast();
    wxToastLock = false;
  } else {
    console.log('特殊情况hideWxToast');
  }
};

export const converNumToText = numStr => {
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
      text = '';
  }
  return text;
};

// 计算两个经纬度之间的距离(单位：米)
export const caculateLL = (lat1, lng1, lat2, lng2) => {
  let radLat1 = lat1 * Math.PI / 180.0;
  let radLat2 = lat2 * Math.PI / 180.0;
  let a = radLat1 - radLat2;
  let b = lng1 * Math.PI / 180.0 - lng2 * Math.PI / 180.0;
  let s =
    2 *
    Math.asin(
      Math.sqrt(
        Math.pow(Math.sin(a / 2), 2) +
          Math.cos(radLat1) * Math.cos(radLat2) * Math.pow(Math.sin(b / 2), 2),
      ),
    );
  s = s * 6378.137;
  s = Math.round(s * 10000) / 10;
  return s;
};
```

## File: utils/qiniu/index.js
```javascript
import { $request } from '../request';
import { generateRandomId } from '../index';

const qiniuUploader = require("./qiniuUploader");

function getQiniuToken() {
    return $request('host/getQnToken','POST', {
        cancelLoading: true
    })
}
// 初始化七牛云相关配置
function initQiniu(myToken) {
    var options = {
        // bucket所在区域，这里是华北区。ECN, SCN, NCN, NA, ASG，分别对应七牛云的：华东，华南，华北，北美，新加坡 5 个区域
        region: 'ECN',

        // 获取uptoken方法三选一即可，执行优先级为：uptoken > uptokenURL > uptokenFunc。三选一，剩下两个置空。推荐使用uptokenURL，详情请见 README.md
        // 由其他程序生成七牛云uptoken，然后直接写入uptoken
        uptoken: myToken,
        // 从指定 url 通过 HTTP GET 获取 uptoken，返回的格式必须是 json 且包含 uptoken 字段，例如： {"uptoken": "0MLvWPnyy..."}
        uptokenURL: '',
        // uptokenFunc 这个属性的值可以是一个用来生成uptoken的函数，详情请见 README.md
        uptokenFunc: function () { 
        	// do something
        },
        // bucket 外链域名，下载资源时用到。如果设置，会在 success callback 的 res 参数加上可以直接使用的 fileURL 字段。否则需要自己拼接
        domain: 'https://ustatic.hudongmiao.com/',
        // qiniuShouldUseQiniuFileName 如果是 true，则文件的 key 由 qiniu 服务器分配（全局去重）。如果是 false，则文件的 key 使用微信自动生成的 filename。出于初代sdk用户升级后兼容问题的考虑，默认是 false。
        // 微信自动生成的 filename较长，导致fileURL较长。推荐使用{qiniuShouldUseQiniuFileName: true} + "通过fileURL下载文件时，自定义下载名" 的组合方式。
        // 自定义上传key 需要两个条件：1. 此处shouldUseQiniuFileName值为false。 2. 通过修改qiniuUploader.upload方法传入的options参数，可以进行自定义key。（请不要直接在sdk中修改options参数，修改方法请见demo的index.js）
        // 通过fileURL下载文件时，文件自定义下载名，请参考：七牛云“对象存储 > 产品手册 > 下载资源 > 下载设置 > 自定义资源下载名”（https://developer.qiniu.com/kodo/manual/1659/download-setting）。本sdk在README.md的"常见问题"板块中，有"通过fileURL下载文件时，自定义下载名"使用样例。
        shouldUseQiniuFileName: false
    };
    // 将七牛云相关配置初始化进本sdk
    qiniuUploader.init(options);
}

function getTodayStr() {
    const today = new Date();
    const add0 = (item) => {
      return item > 9 ? item : `0${item}`;
    };
    return `${today.getFullYear()}${add0(today.getMonth() + 1)}${add0(today.getDate())}`;
}

function qiniuUpload(filePath) {
    const todayStr = getTodayStr();
    const key = `mpAvatar/${todayStr}/${generateRandomId(12)}/${generateRandomId()}`;
    return new Promise((resolve, reject) => {
        qiniuUploader.upload(filePath, (res) => {
            resolve(res);
        }, (err) => {
            reject(err);
        },{
            key,
            region: 'ECN'
        });
    });
}
export default {
    getQiniuToken,
    initQiniu,
    qiniuUpload,
}
```

## File: utils/request.js
```javascript
import { API_HOST, PAGE_HOST } from '../assets/constant/host.js';
import { getToken, clearStorage } from './storage.js';
import { showWxToast, showWxLoading, hideWxLoading } from './index.js';

const APPID = 'wxb52eed28ec54c06e';
export function request(url, method = 'GET', data) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    if (!data.cancelLoading) {
      showWxLoading('请求中');
    }
    wx.request({
      url: API_HOST + url,
      method,
      data,
      header: {
        token: tmpToken,
        appId: APPID,
        'Content-Type': 'application/x-www-form-urlencoded',
      },
      success: res => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        if (res.statusCode === 200) {
          if (res.data.success) {
            resolve(res.data);
          } else {
            if (res.data.message === '401') {
              showWxToast('登录已过期,请重新授权登录!');
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
      fail: err => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        showWxToast('网络异常');
        reject('网络异常');
      },
    });
  });
}

export function requestUpload(url, path) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    wx.uploadFile({
      url: 'https://www.hudongmiao.com/' + url,
      filePath: path,
      name: 'file',
      header: {
        token: tmpToken,
        'Content-Type': 'application/x-www-form-urlencoded',
      },
      formData: {
        prefix: 'wechat-complaints',
      },
      success: function(res) {
        resolve(res);
      },
      fail: function(err) {
        reject(err);
      },
    });
  });
}

export function $request(url, method = 'GET', data) {
  return new Promise((resolve, reject) => {
    const tmpToken = getToken();
    if (!data.cancelLoading) {
      showWxLoading('请求中');
    }
    wx.request({
      url: 'https://www.hudongmiao.com/' + url,
      method,
      data,
      header: {
        token: tmpToken,
        'Content-Type': 'application/x-www-form-urlencoded',
      },
      success: res => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        if (res.statusCode === 200) {
          if (res.data.success) {
            resolve(res.data);
          } else {
            if (res.data.message === '401') {
              showWxToast('登录已过期,请重新授权登录!');
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
      fail: err => {
        if (!data.cancelLoading) {
          hideWxLoading();
        }
        showWxToast('网络异常');
        reject('网络异常');
      },
    });
  });
}

export function requestH5(url, method = 'GET', data) {
  return new Promise((resolve, reject) => {
      const tmpToken = getToken();
      if (!data.cancelLoading) {
          showWxLoading('请求中');
      }
      wx.request({
          url: PAGE_HOST + url,
          method,
          data,
          header: {
              token: tmpToken,
              'Content-Type': 'application/x-www-form-urlencoded'
          },
          success: res => {
              if (!data.cancelLoading) {
                  hideWxLoading();
              }
              if (res.statusCode === 200) {
                  if (res.data.success) {
                      resolve(res.data);
                  } else {
                      if (res.data.message === '401') {
                          showWxToast('登录已过期,请重新授权登录!');
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
          },
      });
  })
}
```

## File: utils/storage.js
```javascript
export function setToken(token) {
    wx.setStorageSync('token', token);
}
export function getToken() {
    return wx.getStorageSync('token');
}
export function setLiveId(liveId) {
    wx.setStorageSync('liveId', liveId);
}
export function getLiveId() {
    return wx.getStorageSync('liveId');
}
export function clearStorage() {
    //  wx.removeStorageSync('liveId');
    wx.removeStorageSync('token');
    wx.removeStorageSync('nickName');
    wx.removeStorageSync('avatarUrl');
}
export function setUseTipFlag() {
    wx.setStorageSync('useTipFlag', 1);
}
export function getUseTipFlag() {
    return wx.getStorageSync('useTipFlag');
}
export function setAdPopFlag() {
    wx.setStorageSync('adPopFlag', 1);
}
export function getAdPopFlag() {
    return wx.getStorageSync('adPopFlag');
}
export function setUserInfo(paramObj) {
    wx.setStorageSync('nickName', paramObj.nickName);
    wx.setStorageSync('avatarUrl', paramObj.avatarUrl);
}
export function getUserInfo() {
    return {
        nickName: wx.getStorageSync('nickName'),
        avatarUrl: wx.getStorageSync('avatarUrl')
    }
}
export function setOrigin(origin) {
    wx.setStorageSync('origin', origin);
}
export function getOrigin() {
    return wx.getStorageSync('origin');
}
export function removeOrigin() {
    wx.removeStorageSync('origin');
}
```
