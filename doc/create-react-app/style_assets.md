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

安装`stylelint`:

```
yarn add --dev stylelint
```