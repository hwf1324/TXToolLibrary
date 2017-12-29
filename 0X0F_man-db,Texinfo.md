# 0X0F man-db, Texinfo

## man-db

man-db是包名,意思是manual database.是类UNIX系统的帮助信息查看工具.

使用的时候则是使用命令man.

一般的软件在安装的时候都会自动在man的数据库目录(例如'/usr/share/man')下注册自己的帮助文件.

man不仅仅能搜索命令.也可以把系统调用或者库函数当作关键词进行搜索.

例如:

```shell
man 3 sleep
```

这里的3表示在man数据库的第3章(库函数章节)搜索sleep关键字.

## Texinfo

Texinfo是GNU计划的软件文档查看工具.texinfo是其包名,而其命令名为info.它的文档的组织方式更像网页,使用了很多的超链接.阅读起来感觉比man要顺畅方便一些.

GNU计划的软件其实都会写man和info两份帮助文件.一般来说man中只是一个简介,而info中是完整的软件手册.

一些非GNU计划的软件也会把自己的文档写成info格式.

## 资料

* [man-db官网](http://www.nongnu.org/man-db/)
* [Texinfo官网](https://www.gnu.org/software/texinfo/)