## **webpack核心概念之entry**

### **单页面应用（spa）**

```
module.exports = {
  entry: './src/index.js'
}
```

### **多页面应用（mpa）**

```
module.exports = {
  entry: {
    pageOne: './src/pageOne/index.js',
    pageTwo: './src/pageTwo/index.js',
    pageThree: './src/pageThree/index.js'
  }
}
```