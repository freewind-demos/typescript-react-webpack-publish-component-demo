TypeScript React Publish Component Demo
=======================================

对于typescript的项目，publish为component的关键点在于：

1. 不要使用webpack打包，否则可能会产生不正确的bundle文件（或者需要其它方式修正）
2. tsconfig中设置`declaration=true`等
3. package.json中设置正确的入口文件和types入口

本demo中的my-component为一个独立的项目，在demo根目录下不直接引用，而是通过`npm publish`发布出去以后，
在根目录下以package的形式引用。

### my-component

```
npm install
npm run dist
npm publish
```

### 根目录

```
npm install
npm run demo
```

It will open page on browser automatically.
