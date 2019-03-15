# 那些好用的类库总结

## 函数库

- [lodash](https://lodash.com/):是一个一致性、模块化、高性能的`JavaScript` 实用工具库。集成了几乎所有你能想到的通用函数方法，起函数式编程风格也是其一大特点，作为一个`star`近 4w 的开源工具库，我们有什么理由放弃它呢？

## 组件库

- [material-ui](https://material-ui.com/):The world's most popular React UI framework。这段说明已经很能说明问题了，google出品，必属精品！

- [antd](https://ant.design/):Ant Design - The world's second most popular React UI framework。好吧，这段说明同样已经说明了问题，阿里巴巴出品的开源组件库，实现功能上与`material-ui`类似，同样非常优秀，其完善的中文文档显然会更受中国开发者的欢迎～

- [react-table](https://github.com/tannerlinsley/react-table): 一款基于`react`的`table`组件，功能极其强大，几乎能满足所有你对`table`的幻想:)

## 图表

- [ECharts](https://echarts.baidu.com/): 虽然`ECharts`并非为`react`而生，但是我们依旧可以通过简单的封装来使用它，毕竟，它真的很强大！

- [Recharts](http://recharts.org/en-US/): 同样是`Google`出品，设计也非常优秀，使用起来比`ECharts`更为灵活，但也因此对于复杂场景可能需要投入更多的学习成本。

- [AntV](http://antv.alipay.com/zh-cn/index.html): `AntV` 是蚂蚁金服全新一代数据可视化解决方案，致力于提供一套简单
方便、专业可靠、无限可能的数据可视化最佳实践。

    - [G2](http://antv.alipay.com/zh-cn/g2/3.x/index.html): 是一套基于可视化编码的图形语法，以数据驱动，具有高度的易用性和扩展性，用户无需关注各种繁琐的实现细节，一条语句即可构建出各种各样的可交互的统计图表。

    - [G6](http://antv.alipay.com/zh-cn/g6/2.x/index.html): 是一个简单、易用、完备的图可视化引擎，它在高定制能力的基础上，提供了一系列设计优雅、便于使用的图可视化解决方案。能帮助开发者搭建属于自己的图 图分析 应用或是 图编辑器 应用。主要包括 **树图**，**网图**，**流图**和**编辑器**。我们项目中用到的流程图也可以通过它实现！ 

    - [F2](http://antv.alipay.com/zh-cn/f2/3.x/index.html): 是一个专注于移动，开箱即用的可视化解决方案，完美支持 H5 环境同时兼容多种环境（Node, 小程序，Weex），完备的图形语法理论，满足你的各种可视化需求，专业的移动设计指引为你带来最佳的移动端图表体验。

    - [L7](http://antv.alipay.com/zh-cn/l7/1.x/index.html): 提供一套地理空间数据可视化框架，易用易扩展，支持海量数据的高性能和 3D 高质量渲染，安全可靠（无地图法务风险）的地理空间数据可视化解决方案。

## 网络请求

- [axios](https://github.com/axios/axios): 一款基于`Promise`的`HTTP` 客户端，功能强大，兼容性好，适用于几乎所有场景。

- [fetch](https://developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API/Using_Fetch): `Fetch API` 提供了一个 `JavaScript`接口，用于访问和操纵`HTTP`管道的部分，例如请求和响应。它还提供了一个全局 `fetch()`方法，该方法提供了一种简单，合理的方式来跨网络异步获取资源。缺点是兼容性较差，可能需要额外的开发成本。

## React框架

### 状态管理

- [Redux](https://redux.js.org/): 一款状态管理解决方案，特点是大量运用单向数据流和纯函数实现状态的可维护，并通过强大的中间件机制保证了高度的灵活性，是目前`React`最主流的状态容器管理工具，适用于大型项目的构建。

- [redux-form](https://redux-form.com/7.3.0/): The best way to manage your form state in Redux. 主要用于管理reudx中的form表单数据。可以帮助你轻松的实现表单数据的增删改查，并以优雅的方式实现数据校验，如果项目中表单数据处理的复杂度较高，且项目中使用了`Redux`，那么`redux-form`将是你不二的选择！

### 路由

- [react-router](https://reacttraining.com/react-router/web/guides/quick-start): 以组件化的方式实现了`SPA`项目的路由切换，`react-router4.0`的出现使得路由的生命和使用更加的灵活。

### immutable

- [immer](https://github.com/mweststrate/immer)
