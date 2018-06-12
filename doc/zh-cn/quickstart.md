## 服务器系统部署
 ```
    1.先下载xampp
    2.下载node.js
    3.安装相关依赖
    4.在命令行中执行 npm run start
 ```
## app本地环境配置

> ### 本地环境搭建
> 参考[官方文档](https://reactnative.cn/docs/0.51/getting-started.html)搭建环境    
> 最后还要下载一个react-native-cli和Gradle    
> windows注意环境变量的配置
> ### 常见错误说明
> 编译过程中若出现jar安装包重复错误执行  
> (windows:) cd android && gradle clean  
> (mac :)cd android && ./gradle clean  
> ### app运行
> 执行 yarn install 安装相关依赖  
> 运行项目时打开两个命令行窗口 一个运行npm run start 一个运行 react-native run-android  
> ### app打包
> (windows :) cd android && gradle assembleRelease  
> (mac:) npm run pack 
> ### 注意
> 在app的代码中,将 app/util/config.json中的路径替换为自己的url