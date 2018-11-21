# java.net.ConnectException: Connection refused

1 异常描述
------

在启动 Tomcat 服务器的时候，控制台一直输出异常信息，然后停止服务器，报出如下异常：

![1](http://img.blog.csdn.net/20170417162232103)

2 异常原因
------

通过观察上图中被标记出来的异常信息，咱们可以知道

>  java.net.ConnectException: Connection refused

此异常，为：**连接被拒绝异常**。

之前也在网上搜索过该异常出现的原因，大多数人给出的答案是端口号被占用，或者在启动本次 Tomcat 服务器之前“关闭”的 Tomcat 服务器没有被彻底关闭，因此才导致此异常的发生。也就是说，此异常一般不会在初次启动 Tomcat 服务器的时候出现。



3 解决方法
------

通过了解异常出现的原因，咱们知道，可以用以下两种方法解决此异常：

 - 杀死占用端口号（一般为8080）的进程，释放端口；
 - 彻底关闭 Tomcat 服务器，或者重新启动项目。

在此，博主采用了第二种解决方法，关闭项目后重新启动，解决了此异常，Tomcat 服务器启动成功。

----------

**温馨提示**：暂时了解到此异常出现的原因及解决方法如上所述，如果大家有其他解决此异常的方法，可以通过`PR`，在此分享给大家，非常感谢。


----------
———— ☆☆☆ —— [返回 -> 超实用的「Exception」和「Error」解决案例 <- 目录](https://github.com/guobinhit/cg-blog/blob/master/articles/solutioncase/README.md) —— ☆☆☆ ————