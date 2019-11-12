## **webpack核心概念之output**

### **用法**

```
const path = require('path');
module.exports = {
  output: {
    path: path.join(__dirname, 'dist'),
    filename: 'bundle.js'
  }
}
```
此配置将一个单独的 bundle.js 文件输出到 当前配置文件所在目录（__dirname）的dist目录中。

### **多个入口起点**

```
module.exports = {
  entry: {
    app: './src/app.js',
    search: './src/search.js'
  },
  output: {
    filename: '[name].js',
    path: __dirname + '/dist'
  }
}
```
写入到硬盘：./dist/app.js, ./dist/search.js