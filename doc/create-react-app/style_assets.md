# 样式和资源

## 使用css模块
`CSS Modules`能够帮助我们将同一份样式文件应用于不同的dom元素，而不产生冲突，允许通过自动创建 `[filename]\_[classname]\_\_[hash]` 格式的唯一 `classname` 来确定 `CSS` 的作用域。详情可参考[What are CSS Modules](https://css-tricks.com/css-modules-part-1-need/)。对于具体组件的样式命名可以使用`[name].module.css`的形式。

## 使用SASS

安装`node-sass`:

```
$ npm install node-sass --save
$ # or
$ yarn add node-sass
```

将`App.css`修改为`App.scss`后，一切正常，这时我们就能够使用`sass`为我们带来的各种便利了。

## stylelint

> 参考[官方文档](https://stylelint.io/)

### 安装`stylelint`:

```
yarn add --dev stylelint
```

### 配置 `Stylelint` 规则

这里我们为 `Stylelint` 选择了官方的代码风格 `stylelint-config-standard`。该风格是 `Stylelint` 的维护者汲取了 `GitHub`、`Google`、`Airbnb` 多家之长生成的。

```
yarn add --dev stylelint-config-standard
```

然后编辑配置文件 `.stylelintrc`：

```
{
  "extends": ["stylelint-config-standard"],
  "rules": {
    "at-rule-no-unknown": [true, {"ignoreAtRules" :[
      "mixin", "extend", "content"
    ]}]
  }
}
```
配置文件中单独配置 `at-rule-no-unknown` 是为了让 `Stylelint` 支持 `SCSS` 语法中的 `mixin`、`extend`、`content` 语法。

修改`lint-staged`配置项：

```
"lint-staged": {
  "src/**/*.{js,jsx,ts,tsx,json,md}": [
    "prettier --single-quote --write",
    "git add"
  ],
  "src/**/*.{css,scss}": [
    "stylelint src/**/*.scss src/**/*.css --fix",
    "git add"
  ]
},
```

### 安装编辑器插件

以`vscode`为例，安装[vscode-stylelint](https://github.com/shinnn/vscode-stylelint)，重启后即可生效。

为了防止与编辑器自带规则产生冲突，我们还需要修改一下用户配置：

```
"css.validate": false,
"less.validate": false,
"scss.validate": false
```