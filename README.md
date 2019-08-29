TypeScript React Webpack Publish Component Demo
===============================================

对于typescript的项目，使用webpack publish为component的关键点在于：

1. `tsconfig`中`module`选`commonjs`，但webpack config中`output.libraryTarget`选`umd`
1. 不要把react打包，在webpack config中设置`externals: ['react']`

webpack在这里做得非常不好，上面两个选项猜了一天才猜出来。以后发布package还是首选rollup。

其它需要注意的：

1. tsconfig中设置`declaration=true`等
1. package.json中设置正确的入口文件和types入口

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
