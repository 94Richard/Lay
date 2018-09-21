# Lay
快速上手

部署

解压文件后，将 layuiAdmin 完整放置在任意目录

通过本地 web 服务器去访问 ./start/index.html 即可运行 Demo

由于 layuiAdmin 可采用前后端分离开发模式，因此你无需将其放置在你的服务端 MVC 框架中，你只需要给 layuiAdmin 主入口页面（我们也称之为：宿主页面）进行访问解析，它即可全权完成自身路由的跳转和视图的呈现，而数据层则完全通过服务端提供的异步接口来完成。


目录说明
src/
layuiAdmin 源代码，通常用于开发环境（如本地），推荐你在本地开发时，将 ./start/index.html 中的 layui.css 和 layui.js 的引入路径由 dist 改为 src 目录。

src/controller/：存放 JS 业务模块，即对视图进行事件等交互性处理

src/lib/：layuiAdmin 的核心模块，一般不推荐修改

src/style/：存放样式，其中 admin.css是核心样式

src/views/：存放视图文件。其中 layout.html 是整个框架结构的承载，一般不推荐做大量改动。

src/config.js：layuiAdmin 的全局配置文件，可随意修改。

src/index.js：layuiAdmin 的入口模块，一般不推荐修改

dist/
通过 gulp 将 layuiAdmin src 目录的源代码进行构建后生成的目录（即：将 JS 和 CSS 文件进行了压缩等处理），通常用于线上环境。关于 gulp 的使用，下文也有介绍。

start/
存放 layuiAdmin 的入口页面、模拟接口数据、layui
