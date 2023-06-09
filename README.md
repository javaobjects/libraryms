
<p align="center"><a href='https://docs.oracle.com/en/java/javase/8'><img alt="Java 8" src="libraryms-Vue/static/Java8.png">
</a>
    <a href='https://docs.spring.io/spring-boot/docs/2.6.2-SNAPSHOT/reference/html'>
<img alt="Spring Boot 2" src="https://img.shields.io/badge/Spring%20Boot%202-%23000000.svg?logo=springboot">
</a>
    <a href='https://staging-cn.vuejs.org'>
<img alt="Vue 3" src="https://img.shields.io/badge/Vue%202%20-%232b3847.svg?logo=vue.js">
</a><br/>
    <a href='#'><img alt="Github stars" src="https://img.shields.io/github/stars/201206030/novel?logo=github"></a>
    <a href='#'><img alt="Github forks" src="https://img.shields.io/github/forks/201206030/novel?logo=github"></a>
    <a href='#'><img alt="Gitee stars" src="https://gitee.com/novel_dev_team/novel/badge/star.svg?theme=gitee"></a>
    <a href='#'><img alt="Gitee forks" src="https://gitee.com/novel_dev_team/novel/badge/fork.svg?theme=gitee"></a>
</p>

# 图书管理系统

#### 项目说明

- 此项目为图书管理系统，后台使采用的是springboot+mybatis等技术实现数据持久化以及api服务调用，前台使用vue.js,vue-resource,vue-router,iView2.0UI框架,vue-quill-editor等技术实现前台页面

#### 开发环境
Windows
#### 配置环境

| 程序           | 版本        | 说明                       |
|--------------|-----------|--------------------------|
| Jdk          | 1.8.0 161 | Java 开发工具包               |
| Mysql        | 5.5.27    | 关系型数据库                   |
| Apache-maven | 3.9.0     | Java 项目管理和构建工具           |
| Nvm          | 1.10      | Node.js 版本管理器            |
| Node         | 8.12.0    | Node.js JavaScript 运行时环境 |

#### 开发工具

| 工具                       | 版本            | 说明                      |
|--------------------------|---------------|-------------------------|
| IDEA                     | 2022.3.2      | 后前端开发IDE                |
| Git                      | 2.24.1        | 代码托管平台                  |
| Google   Chrome          | 75.0.3770.100 | 浏览器、前端调试工具              |
| Navicat                  | 11.1.13       | 数据库连接工具                 |
| Postman                  | 7.1.0         | 接口测试工具                  |
| VMware   Workstation Pro | 14.1.3        | 虚拟机(未用到或许你会用到)          |
| PowerDesigner            | 15            | 数据库设计工具(未用到或许你会用到)      |
| SQLyog                   | 12.0.3        | 数据库连接工具 (未用到或许你会用到)     |
| Visio                    | 2013          | 时序图、流程图等绘制工具(未用到或许你会用到) |
| ProcessOn                | ——            | 架构图等绘制工具(未用到或许你会用到)     |
| XMind   ZEN              | 9.2.0         | 思维导图绘制工具(未用到或许你会用到)     |
| RedisDesktop             | 0.9.3.817     | redis客户端连接工具(未用到或许你会用到) |

#### 编码规范

- 规范方式：严格遵守阿里编码规约。
- 命名统一：简介最大程度上达到了见名知意。
- 分包明确：层级分明可快速定位到代码位置。
- 注释完整：描述性高大量减少了开发人员的代码阅读工作量。
- 工具规范：使用统一jar包避免出现内容冲突。
- 代码整洁：可读性、维护性高。

#### 包结构
```
 +- libraryms-sb -- 图书管理系统服务端
    +- .mvn
        +- wrapper
    +- src
    |   +- main
    |   |    +- java
    |   |    |    +- com
    |   |    |    |    +- lin
    |   |    |    |    |    +- appapidemo
    |   |    |    |    |    |    +- controller -- 控制器类 负责接收和处理HTTP请求
    |   |    |    |    |    |    +- mapper -- MyBatis框架的数据访问层
    |   |    |    |    |    |    +- model -- 数据模型类
    |   |    |    |    |    |    +- util -- 工具类
    |   |    |    |    |    |    +- AppapidemoApplication.java -- 应用程序入口类
    |   |    |    |    |    |    +- CorsConfig.java -- 配置跨域访问
    |   |    |    |    |    |    +- Swagger2.java -- 用于集成 Swagger2 API 文档工具的相关配置
    |   |    +- resources
    |   |        +- application.properties -- 应用程序的配置信息
    |   +- test -- 测试代码
    |  	|	+- java
    |  	|	    +- com
    |  	|	        +- lin
    |  	|	            +- appapidemo
    +- target -- Maven建项目时自动生成的目录
    +- .gitignore -- 指定需要 Git 忽略的文件或目录
    +- LICENSE -- 开源软件的授权协议
    +- mvnw --  Maven Wrapper 的脚本，作用是为了在开发团队中使用一致的 Maven 版本，以及简化在新环境中安装 Maven 的步骤 用于 Linux 或 macOS 系统
    +- mvnw.cmd --  Maven Wrapper 的脚本，作用是为了在开发团队中使用一致的 Maven 版本，以及简化在新环境中安装 Maven 的步骤 用于 Windows 系统
    +- pom.xml -- 用于声明和管理项目依赖的XML文件
    +- README.md -- 项目的相关信息文档
 +- libraryms-Vue -- 图书管理系统客户端
     +- build -- 用于存放打包构建相关的配置文件和脚本
        +- build.js -- 构建脚本
        +- check-versions.js -- 用于检查 Node.js 和 npm 版本是否符合要求的脚本
        +- logo.png -- 项目的 logo 图片文件
        +- utils.js -- 构建脚本中用到的工具函数
        +- vue-loader.conf.js -- Vue-loader 的配置文件，用于解析和转换 .vue 文件
        +- webpack.base.conf.js -- Webpack 基础配置文件
        +- webpack.dev.conf.js -- Webpack 开发环境配置文件
        +- webpack.prod.conf.js -- Webpack 生产环境配置文件
     +- config --用于存放项目的配置文件
        +- dev.env.js -- 开发环境的配置文件
        +- index.js -- 主配置文件
        +- prod.env.js -- 生产环境的配置文件
     +- src
        +- assets -- 静态资源文件 如图片、字体等
        +- components -- Vue 组件
        +- router -- 路由配置
        +- App.vue -- 根组件 协调整个应用程序的视图和管理应用程序的状态
        +- main.js -- 项目的入口文件
        +- tip -- 提示信息相关的组件和样式
     +- static -- 用于存放不需要 webpack 处理的静态文件
     +- .babelrc -- Babel 的配置文件
     +- .editorconfig -- 编辑器的配置文件，用于约定不同编辑器之间的代码风格和格式
     +- .eslintgnore -- 指定需要忽略的文件或目录，让 ESLint 不对其进行检查
     +- .eslintrc.js -- ESLint 的配置文件
     +- .gitignore -- 指定需要 Git 忽略的文件或目录
     +- .postcssrc.js -- PostCSS 的配置文件
     +- db_appapidemo.sql --用于初始化数据库的 SQL 脚本文件
     +- index.html -- 项目的入口 HTML 文件
     +- LICENSE -- 开源软件的授权协议
     +- packge.json -- 项目元数据的文件 用于描述 Node.js 应用程序或模块的属性
     +- packge-lock.json -- 锁定当前安装的包的版本号和依赖关系
     +- READE.md -- 项目的相关信息文档
```

#### 后端技术栈

| 技术                             | 版本            | 说明                 |
|--------------------------------|---------------|--------------------|
| Spring Boot                    | 1.5.8.RELEASE | Spring Boot框架版本    |
| Spring Boot DevTools           | -             | 热部署工具              |
| Spring Boot Starter Web        | -             | Web模块依赖            |
| MyBatis Spring Boot Starter    | 1.3.0         | 整合MyBatis的核心依赖     |
| mysql-connector-java           | 5.1.43        | 连接MySQL数据库依赖       |
| Mapper Spring Boot Starter     | 1.1.3         | MyBatis通用Mapper依赖  |
| PageHelper Spring Boot Starter | 1.1.2         | 分页插件PageHelper依赖   |
| Lombok                         | 1.16.18       | 避免Get/Set方法重复创建依赖  |
| Spring Boot Starter Data Redis | -             | Redis数据库依赖         |
| springfox-swagger2             | 2.7.0         | Swagger2 API文档依赖   |
| springfox-swagger-ui           | 2.7.0         | Swagger2 API文档UI依赖 |
| Spring Boot Starter Mail       | -             | 发送邮件依赖             |

#### 前端技术栈

| 技术                                 | 版本      | 说明                                              |
|------------------------------------|---------|-------------------------------------------------|
| iview                              | ^2.7.4  | 基于 Vue.js 的 UI 组件库                              |
| vue                                | ^2.5.2  | 渐进式 JavaScript 框架                               |
| vue-quill-editor                   | ^3.0.4  | 基于 Quill 的富文本编辑器                                |
| vue-resource                       | ^1.3.4  | 基于 Vue.js 的网络请求库                                |
| vue-router                         | ^3.0.1  | Vue.js 官方的路由管理器                                 |
| autoprefixer                       | ^7.1.2  | 为 CSS 自动添加浏览器前缀的 PostCSS 插件                     |
| babel-core                         | ^6.22.1 | 一个用于使用 Babel 的 JavaScript 编译器                   |
| babel-eslint                       | ^7.1.1  | 用于使用 ESLint 的 Babel 解析器                         |
| babel-helper-vue-jsx-merge-props   | ^2.0.3  | 合并 Vue JSX 组件中的属性                               |
| babel-loader                       | ^7.1.1  | 用于 Webpack 的 Babel 模块加载器                        |
| babel-plugin-syntax-jsx            | ^6.18.0 | Babel 插件，用于支持 JSX 语法                            |
| babel-plugin-transform-runtime     | ^6.22.0 | Babel 插件，用于将 ES6+ 语法转换为 ES5                     |
| babel-plugin-transform-vue-jsx     | ^3.5.0  | Babel 插件，用于将 Vue JSX 转换为渲染函数                    |
| babel-preset-env                   | ^1.3.2  | Babel 预设，用于将 ES6+ 语法转换为 ES5                     |
| babel-preset-stage-2               | ^6.22.0 | Babel 预设，用于支持 ES7+ 语法                           |
| chalk                              | ^2.0.1  | 用于在终端中输出彩色文字的 Node.js 模块                        |
| copy-webpack-plugin                | ^4.0.1  | 用于复制文件和目录的 Webpack 插件                           |
| css-loader                         | ^0.28.0 | 用于在 Webpack 中加载 CSS 文件的加载器                      |
| eslint                             | ^3.19.0 | 用于在 JavaScript 代码中检测和报告问题的工具                    |
| eslint-config-standard             | ^10.2.1 | 用于在 JavaScript 代码中实施标准风格的 ESLint 配置             |
| eslint-friendly-formatter          | ^3.0.0  | 用于在终端中输出更友好的 ESLint 错误信息的插件                     |
| eslint-loader                      | ^1.7.1  | 用于 Webpack 的 ESLint 模块加载器                       |
| eslint-plugin-html                 | ^3.0.0  | ESLint 插件，用于处理 HTML 文件                          |
| eslint-plugin-import               | ^2.7.0  | 一个 ESLint 插件，用于检查 import/export 语句              |
| eslint-plugin-node                 | ^5.2.0  | 一个 ESLint 插件，用于检查 Node.js 代码                    |
| eslint-plugin-promise              | ^3.4.0  | 一个 ESLint 插件，用于检查 Promise 相关的代码                 |
| eslint-plugin-standard             | ^3.0.1  | 一个 ESLint 插件，提供一组符合 JavaScript Standard 风格规范的规则 |
| eventsource-polyfill               | ^0.9.6  | 一个 Webpack 插件，提供 EventSource 接口的 polyfill       |
| extract-text-webpack-plugin        | ^3.0.0  | 一个 Webpack 插件，用于将所有的 CSS 代码提取到一个文件中             |
| file-loader                        | ^1.1.4  | 一个 Webpack 加载器，用于将文件作为模块导入，并返回其 URL             |
| friendly-errors-webpack-plugin     | ^1.6.1  | 一个 Webpack 插件，用于在终端上友好地展示 Webpack 构建时的错误信息      |
| html-webpack-plugin                | ^2.30.1 | 一个 Webpack 插件，用于生成 HTML 文件，并将打包后的资源自动引入该文件中     |
| node-notifier                      | ^5.1.2  | 用于跨平台显示通知的 Node.js 模块                           |
| optimize-css-assets-webpack-plugin | ^3.2.0  | 优化和最小化 CSS 资源的 Webpack 插件                       |
| ora                                | ^1.2.0  | 为终端显示 spinner 和文字消息的 Node.js 模块                 |
| portfinder                         | ^1.0.13 | 在 Webpack 开发服务器上查找可用端口的 Node.js 模块              |
| postcss-import                     | ^11.0.0 | 用于处理 @import 规则的 PostCSS 插件                     |
| postcss-loader                     | ^2.0.8  | 将 CSS 转换为 JavaScript 可以导入的模块的 Webpack 加载器       |
| rimraf                             | ^2.6.0  | 用于删除文件和文件夹的 Node.js 模块                          |
| semver                             | ^5.3.0  | 语义化版本控制的 Node.js 模块                             |
| shelljs                            | ^0.7.6  | 在 Node.js 脚本中使用 Unix shell 命令的 Node.js 模块       |
| uglifyjs-webpack-plugin            | ^1.1.1  | 用于缩小 JavaScript 文件的 Webpack 插件                  |
| url-loader                         | ^0.5.8  | 处理和加载 URL 的 Webpack 加载器                         |
| vue-loader                         | ^13.3.0 | 将 Vue.js 组件转换为 JavaScript 模块的 Webpack 加载器       |
| vue-style-loader                   | ^3.0.1  | 将 CSS 转换为 JavaScript 模块的 Webpack 加载器            |
| vue-template-compiler              | ^2.5.2  | 编译 Vue.js 模板的 Node.js 模块                        |
| webpack                            | ^3.6.0  | JavaScript 模块打包器                                |
| webpack-bundle-analyzer            | ^2.9.0  | 可视化分析 Webpack 打包输出的工具                           |
| webpack-dev-server                 | ^2.9.1  | Webpack 开发服务器                                   |
| webpack-merge                      | ^4.1.0  | 合并 Webpack 配置的工具                                |

#### 项目启动
- 1.数据库：mysql5.6执行以下脚本,前台项目下脚本文件--db_appapidemo.sql  （数据库脚本在前台项目下）
- 2.后台启动：导入项目，进入控制台，到项目所在路径，执行命令：mvn clean spring-boot:run
- 3.前台启动：导入项目，进入控制台，到项目所在路径，执行命令：npm install 后 npm run dev，访问地址：http://localhost:8075  测试账号：super 密码： super

![](libraryms-Vue/static/sb-1.png)

![](libraryms-Vue/static/sb-2.png)

![](libraryms-Vue/static/vue-1.png)

![](libraryms-Vue/static/vue-2.png)

![](libraryms-Vue/static/vue-3.png)

+ 目前里面各种bug懒得改了。。。。

#### 效果展示
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/1.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/2.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/3.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/4.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/5.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/6.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/7.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/8.png?raw=true)
![](https://github.com/yangyuscript/Vue-iView-demo/blob/master/static/9.png?raw=true)

#### 解决bug

1. 解决端口被占用的问题,如下图所示

![](readme/sb-2.png)

+ 解决方法，打开Windows PowerShell 输入如下的命令查看被占用的端口

```
netstat -ano | findstr :8080
```

+ 输入如下的命令，杀掉进程

```
taskkill /F /PID 进程ID

在这里进行id为8080

taskkill /F /PID 14696
```

![](readme/bug-1.png)