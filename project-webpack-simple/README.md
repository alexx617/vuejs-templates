#zq add: 
# vue init webpack-simple my-project-name
#webpack.config.js是vue-cli自动生成的，里面定义了打包步骤
#如果想使用sass,如把vue文件里的普通css代码换成<style lang='sass'>,就会提示找不到module，sass-loader,通过npm install sass-loader --save-dev后
#又提示找不到module node-sass,继续安装node-sass,再重新运行npm run dev恢复正常。
#url-loader也是自己手动安装，目的是自动把小图片变成base64格式
# project-webpack-simple

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
