# Vue
### 1.解决vuecli打包后，css，js资源无法访问的问题
> 在项目的根目录添加vue.config.js文件，添加以下内容
```
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
    ? './' : '/'
}
```
### 2.忽略语法检查,vue.config.js+
```
lintOnSave: false,
    devServer: {
        overlay: {
            warning: false,
            errors: false
        }

    }
```
### 3.解决npm run build 报错
执行
```
cnpm install --global vue-cli
```

```
//报错信息
error code ELIFECYCLE
21 error errno 1
22 error cli@0.1.0 build: `vue-cli-service build`
22 error Exit status 1
23 error Failed at the cli@0.1.0 build script.
23 error This is probably not a problem with npm. There is likely additional logging output above.
```
### 4.安装淘宝镜像
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
npm install -g nrm
nrm ls
nrm use taobao
```
