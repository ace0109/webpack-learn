## **webpack安装**
### **前提条件**
在开始之前，请确保安装了 Node.js 的最新版本。正常都是使用 Node.js 最新的长期支持版本(LTS)。使用旧版本，你可能遇到各种问题，因为它们可能缺少 webpack 功能以及/或者缺少相关 package 包。
### **安装nodejs**
可以直接在[node官网](https://nodejs.org/en/)下载node安装程序。

这里建议使用nvm进行node的安装，因为nvm可以帮助我们安装多个版本的node（*因为可能我们使用的项目或者工具依赖于不同的node版本*），并且很容易的使用下面命令来切换node版本：
```
nvm use 版本号
```
### **本地安装**
要安装最新版本或特定版本，请运行以下命令之一：
```
npm install --save-dev webpack
npm install --save-dev webpack@<version>
```
如果你使用 webpack 4+ 版本，你还需要安装 CLI。
```
npm install --save-dev webpack-cli
```

现在都是用webpack4来开发了，所以在项目中，直接执行下面命令就可以了：
```
npm install --save-dev webpack webpack-cli
```

**对于大多数项目，我们建议本地安装。这可以使我们在引入破坏式变更(breaking change)的依赖时，更容易分别升级项目。**

### **全局安装**

```
npm install --global webpack
```
**不推荐全局安装 webpack。这会将你项目中的 webpack 锁定到指定版本，并且在使用不同的 webpack 版本的项目中，可能会导致构建失败。**