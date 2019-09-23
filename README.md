Reader-赵海棠
***
# 注意事项
* 讲项目导入工作空间时注意一下运行环境的版本
  * Tomcat 8.0.48
  * Tomcat的运行环境: jre 1.8.0_212
  * 项目的运行环境: jre 1.8.0_212
  * 项目的编译环境: 1.8
  * SSH的版本号详见jars文件
* 项目java源码结构解释
  * **action** Struts2框架下的功能实现处; 个人的理解是其与**dao**和**service**一起对应MVC设计模式中的C(Controller） 
  * **dao** 被**service**调用, 利用Hibernate控制持久化层(即对数据库的数据进行操作)
  * **entity** 用于表示ER模型中的E, 作为pojo其属性与E的字段一一对应; 对应MVC设计模式中的M(Model),
  * **service** 为**action**的功能实现提供服务, 并调用**dao**完成数据库的操作, 为当次功能的实施写下句点
  * **utils** 所有根架构无关的东西的实现, 例如查询函数的实现, 创建sessionFactory的函数的实现, 密码加密函数的实现等
* Spring框架此处的作用
  * 在项目运行时控制所有java bean(经配置后的java对象)的生命周期
