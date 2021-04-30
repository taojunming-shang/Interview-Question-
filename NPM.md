### NPM

> node package manger： node模块管理工具，根据NPM我们可以快速安装。卸载所需要的资源文件（例如：jQuery，Vue，Vue-router...）
>
> 去NODE官网下载https://nodejs.org/en/ 下载node，安装以后NPM也跟着安装了
>
> $ node -v
>
> $ npm - v  出现版本好证明安装成功

#### 基于npm进行模块管理

> https://www.npmjs.com/ 基于npm是从npmjs.com平台下载安装

```
$ npm install xxx   把模块安装到当前项目下（node_modules)
$ npm install xxx -g  把模块安装到全局环境中
$ npm i xxx@1.00 安装指定版本号的模板
# npm view xxx versions > xxx.version.json  查看某个模块的版本信息（输出到指定的JSON文件中）
$ npm init -y 初始化当前项目的配置依赖清单
$ npm i xxx --save  把模块保存在清单生产依赖中
$ npm i xxx --save-dev  把模块保存在清单开发依赖中
$ npm install 跑环境，按照清单安装所需的模板

$ npm root -g 查看全局安装模板的目录
$ npm uninstall xxx
$ npm uninstall xxx -g 卸载安装过的模


npm -version  查看npm版本

npm install <name>  安装node.js的依赖包

npm install <name> @3.0.6 安装版本为3.0.6的依赖包

npm install <name> --save  安装的同时将信息写入package.json 中

npm install <name> -g  全局安装

npm init  会引导你创建一个package.json文件，包括名称，版本，作者等这些信息

npm remove express 移除express

npm update express 更新express

npm ls  列出当前安装的所有包

npm root  查看当前包的安装路径

npm root -g 查看全局包的安装路径

npm help  帮助

npm view express  dependencies  查看express 包的依赖关系

npm view express respository.url  查看express包的源文件地址

```

