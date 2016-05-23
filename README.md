# NeoReader

## Update
[2016-05-23] Android 版已可供下载 [NeoReader for Android](neoreader.apk)，或者扫描以下二维码下载（第一个 Android 版本，目前还存在一些问题)

[2016-05-16] iOS 版已可供下载：https://appsto.re/cn/hA0pcb.i ，或者扫描以下二维码下载（因为审核等了一段时间，在这段时间对 UI 做了一些调整，所以第一次打开 app 会受到热更新推送，待自动重启之后即更新完成）

iOS 版：   
![iOS version](qrcode.png)

Android 版：   
![Android version](qrcode-android.png)

## Planning

- [x] Android 版本适配  
- [x] 再添加几个 source  
- [ ] 部分 source 集成用户系统（即登录功能，主要是 V2EX） 

## About

关于 NeoReader，我的想法其实很简答，就是把自己平时看得多的几个资讯聚合在一起，平时不喜欢安装各种客户端，也为了减少自己刷网页的频率

本来只是为了自用，所以做的比较简单，UI 没什么讲究，只是把自己想法实现出来，颜色布局什么的就随便来了

采用 React Native 写的，所以理应有 Android 版本，刚才在发布 iOS 版本的时候测试了下 Android 版本，虽然基本能用，但是 UI 方面还需要很多的调整，所以还需要一些时间

因为时间仓促，所以还存在很多问题，现在已经放到 TestFlight，对于想试用的朋友，可以把 AppleID 发到我邮箱我来添加，欢迎提交 issue

目前还需要改进的有：
* 数据缓存，现在还没有提供清除方法
* 数据请求判断，现在基本没有做错误处理

## DEMO

![reader1.gif](reader1.gif)
![reader2.gif](reader2.gif)
