**牛读** 是一款定制的技术类资讯聚合阅读器，目前包括定制的 知乎日报、V2EX、CNODE、开发者头条、Github Trending、Hacker News

**如果觉得 App 不错，请记得去 AppStore 好评哟**（入口在关于界面，*怕你们找不到……*）

**我没有开源牛读的计划，希望大家还能继续喜欢它，放在 Github 的主要原因是我还没有时间给牛读做一个专门的主页而我又习惯了这里，也方便大家提建议**

Android 版因为 React Native 的支持问题，相比 iOS 版有两个主要的区别：
* header 的 TabBar 自动跟随不够流畅（iOS用的原生方法处理）
* <del>section header不能固定（这个比较影响体验，可能会采用第三方原生组件解决）</del>
* <del>暂时不支持 GIF</del>

[iOS 版下载](https://itunes.apple.com/cn/app/niu-du-neoreader/id1111443079?l=en&mt=8)

![iOS 版下载](https://raw.githubusercontent.com/nihgwu/NeoReader/master/qrcode.png)

[Android 版下载](http://android.myapp.com/myapp/detail.htm?apkName=com.liteneo.reader)

![Android 版下载](https://raw.githubusercontent.com/nihgwu/NeoReader/master/qrcode-android.png)

## 关于 NeoReader 的一些说明

* 采用 React Native 开发，没有任何后端，所以某些资源访问会比较慢，比如 V2EX，因为官方并未提供 tab 的 API，所以目前是采用实时爬取得手机页面，解析 DOM，然后使用 Native View 渲染出来，这个过程可能会稍微有点耗时，如果有后台爬取提供API会好很多，但是我目前并不想做后台
* 关于数据刷新机制，目前只有在 WIFI 环境才会自动刷新，否则必须手动下拉更新数据，而且只会更新当前页面，所以第一次使用的时候其他页面内容都是空的（早期是全部更新，但是会影响启动体验，而且并不合理）
* 对于方便解析的页面内容，都是采用解析 DOM 然后用 Native View 渲染，包括 知乎日报、V2EX、CNODE、Hacker News，开发者头条因为内容源多变，没办法做解析，<del>Github Trending 没时间处理目前也是用WebView打开，后面会做专门的Native页面</del>
* 访问 CNODE 某些帖子闪退的问题，其实是有一篇帖子的GIF图片过大，然后 React Native 的 GIF 解析有 bug，所以造成内存占用过大而闪退
* Hacker News 加载很慢，因为 HN 官方 API 的特殊性，列表需要多个请求才能完成，而且在国外，所以更新会稍慢，进入详情页面是直接用 WebView 打开这个链接，更慢，点击后面的回复可以查看回复列表，目前采用了分级加载的策略，会稍微好点
* 目前 Android 版没有针对 Android6.0 优化
* **关于大家关心的权限问题**，大家尽可以放心，除了处理资讯，没有做任何其他动作，如果提示需要一些电话之类的权限，可能是因为添加的分享模块需要

## 截图

![1](http://a2.mzstatic.com/us/r30/Purple18/v4/92/14/cb/9214cb49-ada5-b1ad-9e28-b070ad510dc7/screen696x696.jpeg)
![2](http://a3.mzstatic.com/us/r30/Purple20/v4/86/b0/a1/86b0a14d-e2a8-eb6d-714e-8ced4bc46031/screen696x696.jpeg)
![3](http://a5.mzstatic.com/us/r30/Purple30/v4/62/ba/81/62ba81f9-1e89-9325-24de-709ca5c60208/screen696x696.jpeg)
![4](http://a5.mzstatic.com/us/r30/Purple30/v4/c1/e8/4c/c1e84cb4-a778-e4c7-d031-be3304741147/screen696x696.jpeg)

## DEMO

![reader1.gif](reader1.gif)
![reader2.gif](reader2.gif)
