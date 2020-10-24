# vue初始化脚手架

> node js：https://nodejs.org/zh-cn/ （下载LTS版本）

> CNPM:
>
> https://developer.aliyun.com/mirror/NPM?from=tnpm
>
> `npm install -g cnpm --registry=https://registry.npm.taobao.org`
>
> `cnpm install cnpm -g`
>
> cnpm i [name] -g

> https://cn.vuejs.org/

> node.js 和 yarn 安装
> https://www.cnblogs.com/yang-xiansen/p/11332610.html

```
安装vue的命令行
cnpm install -g @vue/cli
cnpm install -g @vue/cli-init

安装webpack的初始化脚手架(以下安装cli-init没有成功)
cnpm install -g yarn
yarn global add @vue/cli-init
```

# vue-修改vue项目运行端口号
https://www.cnblogs.com/atjinna/p/6907369.html


# 初始化项目
> Vue 使用Vue-CLI4 创建Vue项目
> https://blog.csdn.net/mengxianglong123/article/details/102949138

> 【详细】在新版Microsoft Edge和Chrome中安装vue-devtools
> https://blog.csdn.net/qq_40738077/article/details/97493593

```
vue create vue_element_demo
# 或
vue init webpack vue_element_demo # 推荐
选择项目的配置
注意项目名称不能有大写字母
```

```
cd vue_element_demo
npm run serve

npm run build
vue ui
```

```
VSCode 开发Vue必备插件
https://blog.csdn.net/yujing1314/article/details/90340647

Vetur 
EsLint
Debugger for Chrome
Auto Close Tag
Auto Rename Tag
JavaScript(ES6) code snippets
Path Intellisense
HTML CSS Support
Beautify
Bracket Pair Colorizer
Indent Rainbow
open in browser
```

# 安装element UI
> https://www.cnblogs.com/Pecci/p/11803512.html
```
// 使用 npm 方式安装 element 可以更好地和 webpack 打包工具配合使用
npm install element-ui -S 
// or
cnpm i element-ui --save

# cnpm i sass -S
# cnpm i sass-loader -S
```

# 在vue中使用sass的配置的方法
> https://blog.csdn.net/lily2016n/article/details/75309492
> 
> vue 解决关于*!!vue-style-loader!css-loader?{"sourceMap":true}!../../../../vue-loader类似问题的
> https://blog.csdn.net/genius_yym/article/details/82222424
> 
> Vue项目设置lang="scss"报错* !!vue-style-loader!css-loader?{"sourceMap":true}!../../../node_modules/vue-loa
> https://blog.csdn.net/pang787559613/article/details/105006744
> 
> VUE 项目引入Sass后启动报错 TypeError [ERR_INVALID_ARG_TYPE]: The "path" argument must be of type string 解决方法
> https://www.cnblogs.com/monkeyblog/p/13728272.html
> 
> npm install 安装某个指定的版本
> https://blog.csdn.net/idomyway/article/details/80601864
> 
> npm 依赖包版本号~和^的区别
> https://www.jianshu.com/p/4544a1e63a5c

```
# cnpm install --save-dev sass
# cnpm install --save-dev node-sass
# cnpm install --save-dev sass-loader

# cnpm install stylus stylus-loader css-loader style-loader --save-dev
# cnpm install less less-loader --save-dev

# 注意版本
# cnpm install node-sass --save-dev
# cnpm install sass sass-loader --save-dev

cnpm install node-sass@^4.11.1 --save-dev
cnpm install sass@^1.26.11 sass-loader@^7.3.0 --save-dev
```

清理缓存
npm cache clean -f

# vs code
> VSCode 初次写vue项目并一键生成.vue模版
> https://www.jianshu.com/p/8610215a8a84

# Element UI
> 基于vue-cli、elementUI的Vue超简单入门小例子
> https://blog.csdn.net/csdnear/article/details/79426915


# ES6 入门教程
> https://es6.ruanyifeng.com/