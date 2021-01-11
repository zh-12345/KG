# KG
一些笔记
1.	windows环境下安装neo4j
 
测试ne04j运行
 
安装服务，并启动服务
 
成功进入该页面，并修改密码
 
 

2.问题解决
问题1：
初次尝试创建节点，出现如图所示错误
 
尝试重新安装最新版本
 
 
安装最新版本后发现，需要更新JDK11，算了，还装回原来版本了，然后发现成功了。。。

3.学习新语句
删除节点MATCH（n:Person）DELETE n
增加节点 CREATE (n: Person) RETURN n
添加关系，第一种是同类型节点之间添加关系，第二种是不同类型节点之前添加关系
查询节点：查询对外有关系的节点 Match (a)—()
          查询所有有关系的节点  Match(a)-[r]->()
利用关键字 DELETE删除节点，SET给节点设置属性，REMOVE删除节点属性
效果如图所示：


4.python环境下使用neo4j
4.1参考官方文档https://neo4j.com/developer/python/
使用命令：pip install neo4j
 

示例：
 
 
注意：使用driver对象来创建Session对象，通常在单个线程中短暂存续，在python通常是用with语句，事务函数提交事务是neo4j推荐的提交事务的方式，定义事务函数，利用（write_transaction）进行调用事务函数。
结果如图所示：
 
问题1：若出现ERROR:neo4j.exceptions.AuthError: {code: None} {message: None}
答：可以关注下是不是账号密码输错，使得python无法连接neo4j
问题2：参考网址https://www.cnblogs.com/ljhdo/p/10907941.html
4.1.2
使用命令pip install py2neo
 
如图所示，即为安装成功。
问题1：使用链接进入neo4j浏览器界面，默认的端口号就是7474,最新的链接方式是传入用户名和密码的元组
问题2有一些简单的py2neo用法，利用node,https://www.jianshu.com/p/febe8a248582

5.通过python 批量导入图数据
参考网址：https://www.cnblogs.com/wzwi/p/10706307.html
