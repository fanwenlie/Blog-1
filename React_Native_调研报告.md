# React Native 可用性调研报告

----------------------

## 简介

`React Native` 由 Facebook 于 2015 年 3 月份对外发布, 并开源, 从 0.14 版本开始支持 `Android` 平台, 目前稳定版本为 0.31.

允许开发者使用 `React` 框架跨平台开发原生移动应用.

它的设计理念是: 使用 `React Native` 开发, 即拥有 Native 的良好人机交互体验, 又保留了 `React` 框架的开发效率.


## 特点

### 一次学习, 随处编写

> Learn once, write anywhere.

在 H5 与 Native 中理论上可使用同一套代码 (通常需要修改大概 __5% ~ 15%__ 代码)

### 真正的原生

通过内置 `JS` 引擎 (`JavaScriptCore`) 运行 `JS` 代码, 并通过 `JS` 代码控制原生组件

### 高效的 UI 开发

+ 独特的 UI 实现框架
+ 组件化开发
+ 跨平台代码移植迅速
+ 自动匹配不同屏幕大小 (Flex)

### 高效的 UI 调试

不需要像原生一样, 每次改动都要经历 `编译 => 构建 => 上传到手机(非必要)` 的流程, 通常需要 __10__ 秒以上, 在大工程中会更慢,

而 `React Native` 在保存更新后可通过模块热替换 (`HMR, Hot Module Replacement`) 在 __1__ 秒内看到结果 (电脑不同, 可能结果不同), 并可将代码都移到 `Chrome` 中运行, 借助 `Chrome` 的开发者工具

### 可方便地整合到现有项目上

### 学习门槛低, 开发难度低, 容易招人

从 0.18 开始已全面支持 `ES6/7`, 并向下兼容, 理论上任何懂点前端开发的人都能快速上手

+ 开发语言简单
+ 语法接近自然语言
+ 积木式 UI 开发

### 完全开源, 社区庞大

+ 庞大的组件库
+ 各种坑基本都有解决方案

### 开发软硬件要求低

官方有三个平台的开发环境部署方案 (`iOS` 在非 `Mac` 系统下需要虚拟机或黑苹果)

各种开源优秀 代码编辑器, IDE 对 `React Native` 有良好支持


## 缺点

### 固有缺点

+ 无法做到 `Write once, Run anywhere`

开发者需要为某些需求提供 `iOS` 和 `Android` 两套不同的代码, 官方有不少组件提供不同的版本

这与官方的设计理念有关, 官方认为 `iOS` 与 `Android` 是两个不同的交互系统

+ 无法完全屏蔽 `iOS` 与 `Android` 的区别, 开发者需要对原生平台有所了解

+ 对于移动开发者 (不懂 `JS`) 来说, __完全不具备__使用 `React Native` 的能力

+ `Android` 版本的更新不如 `iOS`, 还需要时间完善 (不过大部分场景并不影响)

### 与 Native 对比

+ 内存消耗略大

"开发模式" 下会大 20MB 左右, "发布模式" 相差不到

+ 运行速度

主要有以下几方面的消耗:

1. `JS Code` 与 `Native Code` 的交互机制需要花费大概 __2ms__ 左右, 在大部分情况下只会有一次交互

2. 应用载入前需要先载入 `JS Code`, 应用才会开始渲染, 这个时间大概是 __100ms__

+ 安装包比原生代码包大

## 总结

`React Native` 在跨平台移动应用上有极快开发速度, 代码复用可做到 __80%__ 以上, 可实现绝大部分效果(第一方与第三方组件)

PS: 极少情况下需要自己编写原生组件


## 参考

- [React Native 夸平台移动应用开发](https://book.douban.com/subject/26809232/)
- [Flex](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
- [Awesome React Native](https://github.com/jondot/awesome-react-native)
- [React-Native 学习指南](https://github.com/reactnativecn/react-native-guide)
- [官网](http://facebook.github.io/react-native/)
- [React Native 中文网](http://reactnative.cn/)
- [React Native 从入门到原理](http://www.jianshu.com/p/978c4bd3a759)
- [使用 React Native 来撰写跨平台的 App](http://www.infoq.com/cn/articles/react-native-introduction)
