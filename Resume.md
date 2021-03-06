
### 联系方式

- 手机：13761223471
- Email：shannonchenchn@foxmail.com
- 微信：CXL-273879688

---

### 个人信息

 - 陈祥龙 / 男 / 1992.10 / 湖南 
 - 本科 / 中北大学 / 飞行器制造工程专业 
 - 工作年限：3 年    
 - 应聘职位：iOS 开发工程师
 - Github：[https://github.com/ShannonChenCHN](https://github.com/ShannonChenCHN)
 - 博客：[http://www.jianshu.com/u/4ef5e287fc91](http://www.jianshu.com/u/4ef5e287fc91)   

------ 

### 工作经历


#### 公司：上海悦会信息科技有限公司 （ 2016年08月至今）
##### 职位：iOS 开发工程师

##### 项目：YHOUSE （4人团队、美食玩乐预订+社交）

###### 职责：负责 YHOUSE 业务的开发和基础类库、框架的优化、维护

- 图文快照
  - 设计了一个快照生成系统，通过模块化和 POP 的方式实现解耦，从而达到强弱业务逻辑分离的目的，同时提高了代码的可重用性。因此，在从首版的帖子快照，发展到后续版本的商户快照、足迹快照、个人名片，再到快照预览功能的过程中，核心逻辑基本上没有做太多改动，提高了开发效率，节省了维护成本
  - 在版本的迭代过程不断改进，以提高程序稳定性和开发效率，比如改进保存图片到相册的方式、改进下载/读取图片的方式
  - 定义一套 `NSError` 规则，并引入了日志系统，用来记录和上报错误，一旦出现错误，就可追踪到详细信息
- Hybrid
  - 引入 `WKWebView`
     - 通过查阅文档和博客，调研了 WKWebView 的基本使用和各种坑，参考多个不同的开源方案，结合项目的自身需求，设计了一个同时支持 `UIWebView` 和 `WKWebView` 的类库 [SCWebBrowerView](https://github.com/ShannonChenCHN/SCWebBrowserView)
     - 为了避免因为迁移到 `WKWebView` 导致上线后出现新的问题，采用了类簇模式优雅地实现新旧 web view controller 的动态切换
  - 架构上的优化
     - 引入 JS Bridge 机制，规范 JS 和 OC 之间的调用关系
     - 针对项目现状，通过研究 `WebViewJavaScriptBridge` 框架，分别在 JS 和 OC 端做了架构设计上的优化，解决了以前一个项目中存在多个 web view 和 web view controller 的问题，同时改进了 JS 端的调用方式，从沟通成本和研发成本上提高了开发效率
     - 负责编写了相关文档，力求减低沟通成本，同时保证项目后续的生命力
- 会员页
  - 自定义 `UICollectionViewFlowLayout` 来实现可定义吸顶偏移量的 `section header` 
  - 借鉴 MVVM 架构的设计，采用 POP 的方式，抽象了一套可复用的列表框架
  - 拆分 controller 中的逻辑，将一些与业务逻辑不相关的代码分离出来，比如 `UICollectionView` 的代理方法
  - 针对会员页的特殊情况，对现有的网络层的调用进行针对性优化，采用离散型的调用和 delegate 形式的回调，以达到简化逻辑，提高程序稳定性和减低维护成本的目的

##### 项目：OnlyU （独立开发、视频聊天+社区）

###### 职责：从 0 到 1，一人独立负责整个 iOS 项目的开发、上线，在保证速度的同时不忘质量，同时积极参与团队中的产品设计和项目管理

- 项目功能主要包括，即时聊天、视频聊天、个人信息展示、社区活动、支付、分享
- 调研业界各种架构的设计，进行架构选型，制定规范，设计网络层，早期的坚实基础保证了后期的开发效率
- 采用 URL Routes 的方式，实现页面的动态跳转（推送跳转、轮播图动态配置跳转）
- 引入并改进 In-App 调试工具，方便调试网络和 UI，同时为 UI 设计师和服务端开发人员的协同工作提供了便利
- 应用 AOP 实现埋点解耦，以及埋点漏埋检测方案
- 将文案集中管理起来，既方便修改，又有利于后期文案本地化的快速开展
- 集中管理数据存储，避免后期业务增多后的失控，包括 NSUserDefaults 和 SQL 存储等
- 针对视频聊天匹配逻辑难以调试、出现 bug 难以追踪的问题，引入了日志记录工具进行追踪
- 优化 cookie 管理机制，实现原生与 web view 共享 cookie
- 设计了一个可动态配置的个人中心列表，整个列表可以在后台自由控制展示内容和交互

 
#### 公司：宝宝树的电商-美囤妈妈 （ 2015年02月 ~ 2016年08月 ）
##### 职位：iOS 开发工程师

##### 项目：宝宝树孕育、美囤妈妈 （多人团队、电商+社区）   
 

###### 职责：先后负责了树生活、首页改版、分类导航、社区帖子详情等开发任务和维护任务，并在后期临时担任过团队 leader
- 新版首页
  - 设计了一个基于 `UICollectionView` 的框架 [SCStickyCellHeaderCollectionView](https://github.com/ShannonChenCHN/SCStickyCellHeaderCollectionView)
  - 自定义 UICollectionViewFlowLayout， 实现带有吸顶效果的 “cell header” 
  - 对 `UICollectionView` 的代理方法的调用以及相关转算进行封装，在实现功能的同时还保证了代码的可维护性 
- 采用数据源思想，设计了一个低耦合的、可复用的三级分类列表
- 通过 分类 + runtime 的形式优雅地实现了自定义 `UITabBarButton` 上的小红点
- 实现 `UIWebview` 加载 WebP 格式图片的功能，同时保证不影响页面加载性能
- 实现多个 APP 间共享同一设备唯一标识
- 与前端同学一起解决 UIWebView 加载一个 h5 页面时导致崩溃的问题
- 通过 Instrument 工具找出了机身发热的元凶 —— 导航栏中跑马灯的 bug 导致 CPU 消耗过高

#### 中航工业江西洪都航空工业集团有限责任公司 （ 2014年07月 ~ 2015年02月 ）

##### 职位：飞机装配工艺工程师

##### 相关经历：
在此期间，通过自学入门 iOS 开发，先后学习了 Objective-C 语言和 Cocoa Touch 框架等 iOS 开发相关知识，并在后期分别通过模仿微博、京东完成了两个小项目，基本掌握了面向对象编程思想、MVC、架构思想、封装思想以及各种常用 API 的使用、常用功能的开发、版本控制工具的使用。

---

### 开源项目和作品
- 技术文章
  - [WebViewJavascriptBridge 详解](http://www.jianshu.com/p/6f34903be630) ：Hybrid 优化过程中的调研总结，从`WebViewJavascriptBridge` 的功能 API、实现原理到源码解读、针对公司项目现状的最佳实践做了一个全面的介绍
  - [SDWebImage 源码解析](http://www.jianshu.com/p/06f0265c22eb)：在实现图文快照需求过程中，其中用到 `SDWebImage` 来批量下载图片，在使用该框架的过程中也遇到了一些问题，索性就把 `SDWebImage` 源码详细阅读了一下，学习其中的设计思想和技术点
  - [图文快照分享框架的实现](http://www.jianshu.com/p/b3fcb449cb35)：对图文快照需求实现过程的总结，针对长图片的功能从需求分析，到技术实现、架构抽象、相关问题讨论做了一个简单的介绍
- 个人作品
  - [SCKit](https://github.com/ShannonChenCHN/SCKit)：自己在平时工作中总结出来的代码库合辑，包括一些常用的可复用的 UI 控件、业务开发中抽象出来的框架、调试工具等                
  - [SCGoJD](https://github.com/ShannonChenCHN/SCGoJD)（Star 71）：模仿京东客户端，iOS 入门时做的原创作品，正是通过这个项目开始对架构思想、封装思想、模块化设计思想和可维护性有了真正的了解
- 演讲讲义
  - [iOS In-App Purchase](https://github.com/ShannonChenCHN/iOSLevelingUp/blob/master/TechNotes/InAppPurchaseGuide/iOS%20In-App%20Purchase.key)（keynote）：在公司内部给同事们分享的 iOS 内购相关知识

-----

### 技能清单
- 语言：
  - C（熟练）
  - Objective-C（熟练）
  - Swift（通读了 3.1 版本的 The Swift Programming Language，初步了解了 Swift 的基础语法，写过一些 Swift 小项目，详见 [ASwiftTour](https://github.com/ShannonChenCHN/ASwiftTour)）
  - JavaScript/HTML/CSS(系统学习过 HTML 和 JavaScript 的基础知识，并实践使用过，详见 [AFrontEndWebDevTour](https://github.com/ShannonChenCHN/AFrontEndWebDevTour/tree/master/learning-notes))
  - React Native（从入门基础、环境搭建、储备知识到基础概念、API 和组件，以及使用第三方库、原生混合开发都有所了解和实践，详见 [AFrontEndWebDevTour/React-Native](https://github.com/ShannonChenCHN/AFrontEndWebDevTour/blob/master/React-Native/README.md)）
- 版本管理
  - SVN
  - Git
  

