# 53 搭建 Node 应用

在 Node 在的开发模式：

1、直接开发、直接部署；

- 搭建 Node 工程，直接开发

- 开发过程中使用 git 进行管理

- 开发完成，提交 git

- 登录部署服务器，从 git 中拉取最新的代码，然后执行 npm install 安装依赖包

存在的问题：

- 服务器在 npm install 的时候，会占用比较大的网络资源

- 代码没有压缩，拉取的速度比较慢

- 在开发过程中，无法使用比较新的语法

- 开发过程中，无法使用 ES6 模块化

2、直接开发，使用 Webpack 进行打包，然后进行部署

- 搭建 Node + Webpack 工程

- 开发后使用 Webpack 进行打包

- 将打包结果上传到服务器，服务器直接运行

详见 demo53 目录