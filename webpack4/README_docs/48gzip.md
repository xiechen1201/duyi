# 48 gzip

gzip 和 Webpack 没有关系，那是服务端和客户端之间的事情

压缩文件有很多种方式，gzip 是其中一种。

## B/S 结构中的压缩传输

- 浏览器告诉服务器支持哪些压缩包解压

- 服务器经过代码、配置，读取源文件，然后进行压缩返回到浏览器，并且在响应头告诉浏览器压缩的文件格式（根据客户端支持的格式）

- 浏览器根据响应头的内容进行解压，然后正常显示

优点：传输效率得到极大的提升，但并不是绝对的！

缺点：服务器压缩需要时间，客户端的解压需要时间

## 使用 Webpack 进行压缩

使用 compression-webpack-plugin 插件，可以对打包结果进行预压缩，减少服务器压缩的时间

缺点：服务端缺少一些灵活性，不能针对特殊情况进行不同格式的压缩

![](../README_files/iShot_2023-11-01_17.00.35.png)

这样服务器就可以去判断要返回哪个文件了