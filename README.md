# Webpack配置的自我修养 (持续优化。。。)
[![6uZpd0.jpg](https://s3.ax1x.com/2021/03/06/6uZpd0.jpg)](https://imgtu.com/i/6uZpd0)

## :whale: 初衷
  - 用于工作运用
  - 记录工作中或者未来工作中遇到的一些场景
  - 目前是基于Webpack 4x 来实现构建打包,随着Webpack 5的出现慢慢也是会去升级

## :rocket: 项目运行
  ```
  项目运行：npm run start
  项目打包：npm run build
  ```

## :mega: 正文
梳理混乱的 Babel
 类型      | 用途       
 -------- | :-----------: 
 @babel/core     | Babel 实现转换的核心    |   
 @babel/cli     | Babel 提供的命令行    |   
 @babel/parser     | 生成 AST    |   
 @babel/traverse     | 对 AST 进行遍历    |   
 @babel/types     | 对新的 AST 进行聚合并生成 JavaScript 代码    |   
 @babel/preset-env     | 暴露给开发者在业务中运用的包能力    |  
 @babel/plugin-transform-runtime     | 重复使用 Babel 注入函数，达到节省代码大小的目的。
 @babel/plugin-syntax-*    | Babel 的语法插件    | 
 @babel/plugin-proposal-*    | 编译转换在提议阶段的语言特性    |
 @babel/plugin-transform-*    | Babel 的转换插件    |
 @babel/template     | 封装了基于 AST 的模板能力    |
 @babel/node     | 在命令行执行高级语法的环境    |
 @babel/register      | 为 require 增加了一个 hook    |

## 生产环境优化
  - 代码拆分和按需加载场景
  - Tree Shaking 是在编译时进行无用代码消除的
  - 使用 HappyPack 让 Webpack 同一时刻处理多个任务，提升构建速度
  - 压缩代码：UglifyJsPlugin
  - 分割代码按需加载
  - 将css单独生成文件：MiniCssExtractPlugin
  - 压缩JS代码：UglifyJsPlugin
  - ....
## 开发环境优化
  - 缩小文件搜索范围：1）resolve.extensions 2) 设置别名resolve.alias 3）合理设置include,exclude
  - 使用 HappyPack 让 Webpack 同一时刻处理多个任务，提升构建速度
  - 优化 module.noParse 配置，让 Webpack 忽略对部分没采用模块化的文件的递归解析处理
  - ....

## :books: 阅读
  - [深入浅出 Webpack](https://xbhub.gitee.io/wiki/webpack/ "深入浅出 Webpack")
  - [Webpack中文文档](https://webpack.docschina.org/ "Webpack中文文档")
  - [Webpack 好文](https://github.com/webpack-china/awesome-webpack-cn "Webpack 好文")

## :speech_balloon: END
  本项目持续优化更新，有问题也希望及时指正，包括有新知识可以写在issue让我学习学习 :star:
