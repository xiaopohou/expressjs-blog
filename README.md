expressjs-blog
==============

##用expressjs开发的个人博客系统
###主要功能和特色
1. 文集功能，将文章整理成册
2. 功能齐全的富文本编辑器，写博客更随心
3. 响应式布局，手机上效果也很出色
4. 搜索引擎优化，自动提取文章大纲和关键词，填入description和keywords
5. 占内存少，方便托管于bae的128m最小web服务上。
6. 漂亮的侧边栏
###待开发功能
1. 文章右侧边栏增加一个自动提取的文章大纲，充当文章的目录功能，自动添加锚点进行定位，用户无需手动添加
2. 增加markdown的编辑器
3. 回复审核和删除功能
4. seo优化目前只是雏形，继续深入开发。
5. 博主信息侧边栏
6. 相关文章推荐侧边栏
###1.安装mongodb
    sudo apt-get install mongo
###2.执行以下四条命令
    mongo
    use blog
    db.addUser("root","1234")
    db.auth("root","1234");

###3.配置 common/config.js文件
    dbName 为 blog
    dbUser 为 root
    dbPass 为 1234
    dbAddress 为 mongodb所在机器IP
注mongodb默认不能远程连接，如果需要远程连接，要更改mongo的配置。如果在本机连接，dbUser, dbPass不要填。
###4.执行
    npm install
    node server.js
###5.到 /register 下注册
注册成功之后注释掉useRoutes.js的63-66行。
###6.到 /admin 下管理博客
##作者个人博客
[www.thinkspring.cn](http://www.thinkspring.cn)
