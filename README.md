## 前后端全部开源微信小程序商城（Java + uniapp）

### 重要链接
- 新手必看视频教程：[https://doc.fly2you.cn/zh-CN/start/videos.html](https://doc.fly2you.cn/zh-CN/start/videos.html)
- 官网：[https://fly2you.cn](https://fly2you.cn)
- 开发文档：[http://doc.fly2you.cn](http://doc.fly2you.cn)
- 在线体验：[https://doc.fly2you.cn/zh-CN/start/view.html](https://doc.fly2you.cn/zh-CN/start/view.html)
- Gitee仓库：[https://gitee.com/fuyang_lipengjun/platform](https://gitee.com/fuyang_lipengjun/platform)
- Github仓库：[https://github.com/lipengjun92/platform-wxshop](https://github.com/lipengjun92/platform-wxshop)

### 官方QQ群
- <a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=HNLRmaIdvnj2e_TGkMspORvIn-AHNZCb&jump_from=webapi"><img border="0" src="//pub.idqqimg.com/wpa/images/group.png" alt="微同科技 ①群" title="微同科技 ①群"></a>：66502035
- <a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=4i3Z9xgp7SlPnk_X1v0TWToSOoT_gJMz&jump_from=webapi"><img border="0" src="//pub.idqqimg.com/wpa/images/group.png" alt="微同科技 ②群" title="微同科技 ②群"></a>：870579539
- <a target="_blank" href="https://qm.qq.com/cgi-bin/qm/qr?k=hQLMx7vYLfP_C-d2-yP_udx1yciJXfHC&jump_from=webapi"><img border="0" src="//pub.idqqimg.com/wpa/images/group.png" alt="微同科技 ③群" title="微同科技 ③群"></a>：151602347

<p align="center">
  <b>特别赞助</b>
</p>
<br/>
<table align="center" cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td align="center" valign="middle" colspan="3">
	      <a href="http://www.ccflow.org/?from=fuyang_lipengjun" target="_blank">
					<img src="https://platform-wxmall-1251990035.cos.ap-shanghai.myqcloud.com/ccflow.png">
				</a>
      </td>
    </tr>
  </tbody>
</table>

## 重要信息
1. 项目合作洽谈，请联系客服微信（使用微信扫码添加好友，请注明来意）。
2. 如需购买 [商业版源码](https://fly2you.cn/ma.html) 请联系客服。<br>
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/image/2023_09_20/11_33_59.png "微信")

## 使用须知
### ✅允许
- 个人学习使用
- 允许用于学习、毕设等
- 允许进行商业使用，请自觉遵守使用协议，如需要商业使用推荐购买[商业版源码](https://fly2you.cn/ma.html)
- 请遵守 Apache License2.0 协议，再次开源请注明出处
- 推荐Watch、Star项目，获取项目第一时间更新，同时也是对项目最好的支持
- 希望大家多多支持原创作品

## 项目结构
~~~
platform
|--_sql 初始化数据库脚本
|--platform-admin 后台管理（打包发布此项目）
|--platform-api 微信小程序商城api接口
|--platform-common 公共模块
|--platform-gen 代码生成
|--platform-schedule 定时任务
|--uni-mall uniapp版商城
|--wx-mall 微信小程序原生商城
~~~

## 系统架构图
![18_14_55.PNG](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/image/2023_10_19/18_14_55.png)

## 数据流向图
![18_16_01.PNG](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/image/2023_10_19/18_16_01.png)

## 安装教程

* 配置环境（推荐jdk1.8、maven3.3、tomcat8、mysql5.7、redis4.0.1）
* 创建数据库
* 依次初始化sql脚本 
    * /_sql/platform.sql
    * /_sql/sys_region.sql

* 导入项目到IDE中
* 导入支付证书至/platform-admin/src/main/resources/cert/目录下（申请商户号、开通微信支付、下载支付证书）
* 修改配置文件 /platform-admin/src/main/resources/dev/platform.properties
    * jdbc.url
    * jdbc.username
    * jdbc.password
    * wx.appId
    * wx.secret
    * wx.mchId
    * wx.paySignKey
    * wx.notifyUrl
    * sms.validIp
    * mp.appId
    * mp.secret
    * mp.token
    * mp.aesKey
* 修改配置文件 /platform-admin/src/main/resources/j2cache.properties
    * redis.hosts
    * redis.password
* 启动redis服务
* 启动后台项目（参照<a href="https://doc.fly2you.cn/zh-CN/start/02.html#%E6%9C%AC%E5%9C%B0%E9%83%A8%E7%BD%B2">开发文档</a>）
* 打开微信开发者工具
* 导入 /wx-mall填写appId
* 修改 /wx-mall/config/api.js里API_BASE_URL的值
* 使用idea启动项目访问路径
    * [http://localhost:8080/platform-framework](http://localhost:8080/platform-framework)
* 出现404问题的同学请检查设置`Application context`为`/platform-framework`

## 驰骋工作流引擎的安装
   1. 请参考: https://gitee.com/opencc/JFlow/wikis/pages/preview?sort_id=4199224&doc_id=31094
   
## 页面展示
### 接口文档
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/image/2023_09_20/15_06_39.png "接口文档")
### 登录页面
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180708/login.png "登录")
### 首页
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180708/index.png "首页")
### 捐赠
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/4.png "捐赠")
### 小程序首页
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/5.png "小程序首页")
### 专题
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/6.png "专题")
### 分类
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/7.png "分类")
### 购物车
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/8.png "购物车")
### 优惠券
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/10.png "优惠券")
### 小程序并联手机
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/upload/20180727/11.png "并联手机")

## 贡献者列表
![](https://platform-wxmall.oss-cn-beijing.aliyuncs.com/image/2023_09_20/12_11_57.png "贡献者列表")
