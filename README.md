# Vue
### 1.解决vuecli打包后，css，js资源无法访问的问题
> 在项目的根目录添加vue.config.js文件，添加以下内容
```
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
    ? './' : '/'
}
```
