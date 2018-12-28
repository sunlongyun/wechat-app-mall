# 微信小程序商城
微信小程序商城，微信小程序微店，长期维护版本，欢迎大家踊跃提交贡献代码；

使用说明和常见问题，可参阅下面的说明，如还有疑问，可访问工厂官网 [https://www.it120.cc/](https://www.it120.cc/) 寻求帮助！

## 扫码体验

<p>
<img src="https://cdn.it120.cc/apifactory/2017/09/15/487409738ebb80c44eda01c46d59b20c.jpg" width="200px">
<img src="https://cdn.it120.cc/apifactory/2018/04/04/570e9a77dbc9cacda176e98a4f2778c5.jpg" width="200px">
<img src="https://cdn.it120.cc/apifactory/2018/04/01/b7b8f5a0fcfc72454ade8510ab929717.jpg" width="200px">
<img src="https://cdn.it120.cc/apifactory/2018/04/19/fbf88e05686b6d9c7c5d5476c7b798d1.jpg" width="200px">
</p>

## 接口 & 后台声明
本项目为小程序商城纯前端项目，由于人力和精力所限，本项目并未有开发配套的后台系统，而是直接使用了 [api工厂](https://www.it120.cc/) 提供的免费接口和云后台，可以完全满足本项目的所有功能需求。

## 最新功能

- [新增小程序购物单支持](https://developers.weixin.qq.com/miniprogram/introduction/widget/order/quickstart/orderlist/import.html)

## 使用说明

1、[申请后台账号/获取专属域名](https://www.it120.cc/info/wxapp/115)

2、开通商城模块

<img src="https://cdn.it120.cc/apifactory/2018/11/14/b61fe6ffb2460f7e4554758b394814f5.png">

3、修改根目录下  config.js 文件

```javascript
module.exports = {
  version: "5.0",
  note: '优化接口调用流程',
  subDomain: "tz", // 如果你的域名是： https://api.it120.cc/abcd 那么这里只要填写 abcd
  appid: "wxa46b09d413fbcaff", // 您的小程序的appid，购物单功能需要使用
  shareProfile: '百款精品商品，总有一款适合您' // 首页转发的时候话术
}
/*
根据自己需要修改下单时候的模板消息内容设置，可增加关闭订单、收货时候模板消息提醒；
1、/pages/to-pay-order/index.js 中已添加关闭订单、商家发货后提醒消费者；
2、/pages/order-details/index.js 中已添加用户确认收货后提供用户参与评价；评价后提醒消费者好评奖励积分已到账；
3、请自行修改上面几处的模板消息ID，参数为您自己的变量设置即可。  
*/
```

4、[设置小程序合法服务器域名](https://www.it120.cc/info/wxapp/116)

5、重启您的小程序开发工具，完成


## 常见问题

- [如何修改小程序商城的标题？](https://www.it120.cc/info/faq/778)

- “无法登录” / Token 无效 ？

  1. app.js 里面的 subDomain  改成你自己的，保存；
  2. 登录你的小程序后台（MP那个地址），Request 域名处增加 api.it120.cc
  3. 确保小程序后台（MP那个地址） 的appid，工厂后台填写的 appid ，开发工具右上角 “项目详情” 打开后显示的 appid ，这3个 appid 是一模一样的；
  4. 开发工具上点击 “清除缓存” —>  “编译”

- [小程序提示“无法登录”的错误？](https://www.it120.cc/info/faq/392)

- [如何发布自己的商品？](https://www.it120.cc/info/faq/436)

- [如何给Banner增加链接，点击打开某个商品？](https://www.it120.cc/info/faq/437)

- [获取我的accesstoken，以便我在其他系统使用](https://www.it120.cc/info/faq/763)

- 工厂后台设置 appid、secret、微信支付商户号和秘钥时候的 token 怎么填？

  **不要填！**

  **不要填！**

  **不要填！**

  **重要的事情说三遍，这个小程序用不到，是给服务号使用的，所以大家空着不要填**

- 微信支付时候，提示 50000 错误，不能获取到预支付id

  > 这个错误是无法获取到微信支付的预支付信息

  - 可能是你没有在后台配置您的微信支付商户号和秘钥，或者配置错误
  - 可能是你配置的微信支付不是当前小程序申请的（微信支付目前无法跨小程序调用）
  - 确保微信开发工具上面登录的 APPID 和你在后台配置的 APPID 是同一个

- 能否帮我免费添加功能？

  可以！

  <img src="https://cdn.it120.cc/apifactory/2017/07/29/18ae9b8aaedcd747fc5f1c3fa8bc0fe4.png" width="300px">

  1. 点击页面顶部的 Star ，关注后，项目有最新动态 github 会提醒您，不错过重要更新；
  2. 点击页面顶部的 Fork， 将您需要增加的功能完成 小程序 端界面的调整，然后在 github  上请求将您的代码合并到 EastWorld；
  3. 您的代码合并请求审核通过后，我们将会为您完善配套的后台功能；
  4. 开源项目离不开您的支持和代码共享，我们一起把 EastWorld 项目长期维护下去；

- [如何使用在线客服功能？](https://www.it120.cc/info/faq/867)

- 下单的时候没有地方填写收货地址？

  1. 添加一个“物流模板”，只有需要快递的商品才会提示用户填写收货地址
  2. 发布商品的时候，选择刚才添加的“物流模板”
  3. 重新下单，将会需要用户输入收货地址

- 后台设置appid和secret的时候提示不正确？

  1. 请确认您填写的appid和secret是否正确
  2. 输入的时候确保没有空格（复制的时候可能会多复制了空格）
  3. 在微信后台设置服务器IP地址白名单（106.14.43.122）

- 如何使用退款功能？

  1. 后台支持针对订单指定退款多少金额；
  2. 可选择退款至用户可用余额或者按照用户支付原路退还第三方或者银行卡；
  3. 如果选用原路退还，需要在商户号和秘钥设置的地方上传您的微信支付证书文件（PK12格式文件）

- 如何设置满多少包邮？

  1. 后台系统设置 -- 系统参数，增加系统参数；
  2. 参数名 free_shipping_for_purchases （注意不要有空格）
  3. 参数值填写您希望的买满金额即可

- [“规格与尺寸”怎么玩](https://www.it120.cc/info/faq/1208)

- [如何设置用户提现手续费](https://www.it120.cc/info/faq/1589)

- [商品如何显示视频？](https://www.it120.cc/info/faq/1802)

- [货到付款、积分赠送规则设置](https://www.it120.cc/notice/22)

- [小程序如何使用“模板消息”给用户推送消息](https://www.it120.cc/info/faq/2823)

- 如何修改或者关闭订单超过30分钟未付款自动关闭？

  1. 创建订单接口增加 expireMinutes 参数；
  2. 代表多少分钟未支付自动关闭本订单，传0不自动关闭订单；


## 如何升级到最新版

- 小程序程序的修改和您后台的数据是独立的，所以不用担心您会丢失数据
- 先把你开发工具下的现有版本程序备份
- 下载最新版的程序，直接覆盖您本地的程序
- 用开发工具修改域名 mall 为你自己的域名
- 开发工具里面上传代码提交微信审核
- 审核通过后，小程序后台去发布新版本即可
- 用户无需重新扫码，关闭小程序重新打开就是新版本了
