## **webpack初体验：一个最简单的例子**
1. 创建一个项目目录，比如：webpack-demo
2. 进入到webpack-demo，执行命令：
```
npm init -y  //-y作用是在所有选项中都选择yes
```
3. 本地安装webpack：
```
npm install --save-dev webpack webpack-cli
```
4. 在根目录创建webpack配置文件webpack.config.js，代码如下：
```
'use strict';

const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    path: path.join(__dirname, 'dist'),
    filename: 'bundle.js'
  },
  mode: 'production'
}
```
5. 在package.json里的script中添加一个命令：
```
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack"
  }
```
这样我们就可以执行下面命令来执行webpack打包操作
```
npm run build
```

6. 创建src目录，作为我们的项目文件目录。在src内创建index.js作为入口文件，创建helloworld.js作为一个工具，代码是这样的：
```
// helloworld.js

export function helloworld() {
  return 'hello webpack';
}
```
```
// index.js

import { helloworld } from './helloworld';

document.write(helloworld());
```

7. 最后，执行命令： npm run build 

就可以看到根目录生成了dist目录和里面的bundle.js，在dist中创建一个index.html，引入bundle.js，打开页面，就可以看到页面输出的 hello webpack。
