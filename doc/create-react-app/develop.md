# react 开发

## 编辑器设置

### 在编辑器中显示 Lint 输出

> 注意：此功能适用于 react-scripts@0.2.0 及更高版本。
> 它也适用于 npm 3 或更高版本。

如果你希望在编辑器中显示 `lint` 结果，则可以执行一些额外的步骤。

你需要先为编辑器安装 `ESLint` 插件。 然后，将名为 `.eslintrc.json` 的文件添加到项目根目录：

```
{
  "extends": "react-app"
}
```

### 在编辑器中进行调试

你需要安装最新版本的 VS Code 和 [VS Code Chrome Debugger Extension](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) 。

然后将下面的代码块添加到 launch.json 文件中，并将其放在应用程序根目录中的 .vscode 文件夹中。

```
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Chrome",
      "type": "chrome",
      "request": "launch",
      "url": "http://localhost:3000",
      "webRoot": "${workspaceRoot}/src",
      "sourceMapPathOverrides": {
        "webpack:///src/*": "${webRoot}/*"
      }
    }
  ]
}
```

> 注意：如果你对 `HOST` 或 `PORT` 环境变量 进行了调整，则 `URL` 可能会有所不同。

通过运行 `npm start` 启动应用程序，然后按 `F5` 或单击绿色调试图标在 `VS Code` 中开始调试。你现在可以编辑代码，设置断点，更改代码，以及从编辑器调试新修改的代码。

[了解更多](https://github.com/Microsoft/vscode-chrome-debug/blob/master/README.md#troubleshooting)

### 自动格式化代码

[Prettier](https://github.com/prettier/prettier) 是一个固定的代码格式化程序，支持 JavaScript ，CSS 和 JSON 。使用 Prettier，你可以自动格式化你编写的代码，以确保项目中的代码风格。

要在 git 中进行提交时格式化代码，我们需要安装以下依赖项：

```
npm install --save husky lint-staged prettier
```

- husky 使得使用 githooks 变得很容易，就好像它们是 npm 脚本一样。
- lint-staged 允许我们在 git 中的 staged 文件上运行脚本。有关 lint-staged 的更多信息，请参阅 [Make linting great again!](https://medium.com/@okonetchnikov/make-linting-great-again-f3890e1ad6b8)。
- prettier 的是我们将在提交运行之前的 JavaScript 格式化程序。

现在，我们可以通过向项目根目录中的 package.json 添加几行来确保每个文件的格式正确。

将以下字段添加到 package.json ：

```
"husky": {
    "hooks": {
        "pre-commit": "lint-staged"
    }
}
```

接下来，我们在 package.json 中添加一个 'lint-staged' 字段，例如：

```
"lint-staged": {
    "src/**/*.{js,jsx,ts,tsx,json,css,scss,md}": [
        "prettier --single-quote --write",
        "git add"
    ]
},
```

好了，现在我们已经能够在`commit`之前实现代码的语法检查以及美化了～

关于如何在`eslint`中集成`prettier`，可以参考[官方文档](https://prettier.io/docs/en/eslint.html)，但是我们这里建议不这么做，还是抱着 Facebook 这课大树，跟着组织走吧:)

但是，我们如果想在保存时自动实现上述功能该如何办呢？
答案是直接在 IDE 中去实现，参考[官方文档](https://prettier.io/docs/en/editors.html#visual-studio-code)，以`vscode`为例，安装[prettier-vscode](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)扩展。

安装完成后已经就可以直接在 IDE 中实现代码的格式化啦，具体方法可以是:

```
CMD + Shift + P -> Format Document
```

或者

```
alt + shift + F
```

当然，我们也可以直接配置用户设置`setting.json`为：

```
"editor.formatOnSave": true
```
