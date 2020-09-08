# node.js安装
+ DOS清屏cls git清屏clear
+ 安装node.js后，会带着一个孪生兄弟:NPM  node模块管理工具：基于npm可以快速安装和卸载对应的模块(类库、插件、组件、框架...都是模块)
+ 安装node，一路下一步 遇框全选，选择长期稳定版的
+ 通过下面指令查看版本，是否安装
```
$ node --version(简写node -v)
$ npm --version
```
# npm 指令
+ 安装在全局(任意窗口打开cmd)
   + 安装在全局的模块，一般适用于当前电脑上的每一个项目，一般还能基于命令来操作
   + 安装$ npm install xxx --global简写：$ npm i xxx -g
   + 卸载$ npm uninstall xxx -g 
   + 查看全局安装的目录$ npm root -g
```
npm i yarn -g
npm i nrm -g
简写
npm i yarn nrm -g

MAC电脑前面加 sudo 安装

//=>检测是否安装成功
$ yarn -v
$ nrm -v
出现版本号代表安装成功
```
+ 安装在某个项目本地(安装在本地的模块无需加 -g)
   + 安装的模块只对当前项目起作用（最常用的）
   + 在指定的目录下打开DOS/终端命令窗口(地址栏输入cmd)
      + $ npm i 模块
      + $ npm uninstall 模块
      + 安装成功后，当前目录下会出现一个node_modules文件夹，包含我们安装的模块信息
+ 这样安装都是安装模块的最新版本，我们还可以安装当前模块的指定版本号
   + 查看版本号 $ npm view 模块 versions > 模块.versions.json
   + $ npm i 模块@版本号
```
$ npm i 模块 安装最新版本的模块
$ npm i 模块@版本号 安装模块指定版本
$ npm i 模块@3 安装模块第三代版本中的最后一个版本
```

【npm的安装会慢一些】
所有安装的模块都是在https://www.npmjs.com/国外网站下载，想要提高安装的速度，我们可以有下述的解决方案：
+ 切换安装来源  nrm
   + $ nrm ls 查看当前下载源
   + $ nrm use taobao 把下载源切换到淘宝镜像上
   > 首先要在全局安装nrm($ npm i nrm -g)，切换源成功后，后续的时候还是基于npm操作
+ 使用其他的模块管理工具(这种方案一般只是往本地安装，安装在全局还是基于npm)
   + yarn
      >首先要在全局下安装yarn
      + $ yarn add 模块@版本号
      + $ yarn remove 模块 
   + cnpm
   + bower