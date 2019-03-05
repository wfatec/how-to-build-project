# react项目构建流程

> Create React App 是官方提供的用于构建react单页面应用的工具方法. 它提供了现代化的零配置构建方案。

## 快速安装

```
npx create-react-app my-app
cd my-app
npm start
```

此时我们已经构建好了最基本的`react`应用，无需安装或配置像`webpack`或`babel`这样的第三方工具，它们已经被提前配置好并隐藏掉了，因此你可以专注于业务代码本身。

### 输出结果

安装完成后`my-app`文件结构为：

```
my-app
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
└── src
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    └── serviceWorker.js
```

## Scripts

接下来为我们试验一下默认生成的脚本文件

### `npm start` 或 `yarn start`

执行完成后我们将在`localhost:3000`看到初始页面

### `npm test` 或 `yarn test`

测试结果如下：

```
PASS  src/App.test.js
  ✓ renders without crashing (24ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        3.505s
Ran all test suites.
```

### `npm run build` 或 `yarn build`

此命令用于打包发布生产环境下的代码，执行完成后将会在根目录下新建`build`文件夹，该文件夹下即为打包后的代码。


## 支持的语言特性

该项目支持最新 JavaScript 标准的超集。 除了 ES6 语法功能外，它还支持：

- 指数运算符 (ES2016).
- Async/await (ES2017).
- Object Rest(剩余)/Spread(展开) 属性 (ES2018).
- 动态 import() (stage 3 proposal)
- Class 字段和静态属性 (part of stage 3 proposal).
- JSX, Flow 和 TypeScript.

注意: **此项目默认不包含 polyfills**。

如果你使用任何其他需要运行时（runtime）支持 的 `ES6+` 特性（例如 `Array.from()` 或 `Symbol` ），请确保 手动包含相应的 `polyfill`，或者你所定位的浏览器已经支持它们。