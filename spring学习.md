
# spring学习

spring学习


<!-- TOC -->

- [spring学习](#spring学习)
- [第1章 Java EE应用和开发环境](#第1章-java-ee应用和开发环境)
- [第2章 JSP/Servlet及相关技术详解](#第2章-jspservlet及相关技术详解)
- [第3章 Struts 2的基本用法](#第3章-struts-2的基本用法)
- [第4章 深入使用Struts 2](#第4章-深入使用struts-2)
- [第5章 Hibernate的基本用法](#第5章-hibernate的基本用法)
- [第6章 深入使用Hibernate](#第6章-深入使用hibernate)
- [第7章 Spring的基本用法](#第7章-spring的基本用法)
    - [反射](#反射)
    - [动态代理](#动态代理)
- [第8章 深入使用Spring](#第8章-深入使用spring)
- [第9章 企业应用开发的思考和策略](#第9章-企业应用开发的思考和策略)
- [第10章 简单工作流系统](#第10章-简单工作流系统)

<!-- /TOC -->


#  第1章 Java EE应用和开发环境 



struts 使用2.3

spring 使用4.0 

hibernate使用4.3


1．1 Java EE应用概述 

1．1．1 Java EE应用的分层模型 

领域对象: 各自

DAO 数据访问对象

业务逻辑

控制器层

表现层



1．1．2 Java EE应用的组件 



1．1．3 Java EE应用的结构和优势 


1．1．4 常用的Java EE服务器 

tomacat
jetty
gboss


1．2 轻量级Java EE应用相关技术 

JSP servlet javaBean

JSP（全称JavaServer Pages）是由Sun Microsystems公司倡导和许多公司参与共同创建的一种使软件开发者可以响应客户端请求，而动态生成HTML、XML或其他格式文档的Web网页的技术标准。JSP技术是以Java语言作为脚本语言的，JSP网页为整个服务器端的Java库单元提供了一个接口来服务于HTTP的应用程序。

Servlet（Server Applet），全称Java Servlet，未有中文译文。是用Java编写的服务器端程序。其主要功能在于交互式地浏览和修改数据，生成动态Web内容。狭义的Servlet是指Java语言实现的一个接口，广义的Servlet是指任何实现了这个Servlet接口的类，一般情况下，人们将Servlet理解为后者。
Servlet运行于支持Java的应用服务器中。从实现上讲，Servlet可以响应任何类型的请求，但绝大多数情况下Servlet只用来扩展基于HTTP协议的Web服务器。




1．2．1 JSP、Servlet 3．x和JavaBean及替代技术 



1．2．2 Struts 2．3及替代技术 

Struts是最早的MVC框架,资料多,太老

- Struts 2.3  Spring MVC  JSF 三个框架相互竞争

 Spring MVC 由于Spring极高的市场占有率

 JSF oracle 推荐的JavaEE规范.  占有率最少.

1．2．3 Hibernate 4．3及替代技术 

需要采用面向对象的方式访问数据库.ORM

对象关系映射（英语：(Object Relational Mapping，简称ORM，或O/RM，或O/R mapping），是一种程序技术，用于实现面向对象编程语言里不同类型系统的数据之间的转换[1]  。从效果上说，它其实是创建了一个可在编程语言里使用的--“虚拟对象数据库”。

Hibernate 是轻量级额ORM框架.

将传统的java对象映射成了持久化的类.

除了Hibernate 外,轻量级的JavaEE 可以使用MyBatis 框架作为持久层.

1．2．4 Spring 4．0及替代技术 

Spring可以将大部分框架无缝整合.


1．3 Tomcat的下载和安装 

1．3．1 安装Tomcat服务器 

1．3．2 配置Tomcat的服务端口 

1．3．3 进入控制台 

1．3．4 部署Web应用 

1．3．5 配置Tomcat的数据源 

1．4 Eclipse的安装和使用 

1．4．1 Eclipse的下载和安装 

1．4．2 在线安装Eclipse插件 

1．4．3 从本地压缩包安装插件 

1．4．4 手动安装Eclipse插件 

1．4．5 使用Eclipse开发Java EE应用 

1．4．6 导入Eclipse项目 

1．4．7 导入非Eclipse项目 

1．5 Ant的安装和使用 

1．5．1 Ant的下载和安装 

1．5．2 使用Ant工具 

1．5．3 定义生成文件 

1．5．4 Ant的任务（task） 

1．6 Maven的安装和使用 

1．6．1 下载和安装Maven 

1．6．2 设置Maven 

1．6．3 创建、构建简单的项目 

1．6．4 Maven的核心概念 

1．6．5 依赖管理 

1．6．6 POM文件的元素 

1．7 使用SVN进行协作开发 

1．7．1 下载和安装SVN服务器 

1．7．2 配置SVN资源库 

1．7．3 下载和安装SVN客户端 

1．7．4 将项目发布到服务器 

1．7．5 从服务器下载项目 

1．7．6 提交（Commit）修改 

1．7．7 同步（Update）本地文件 

1．7．8 添加文件和目录 

1．7．9 删除文件和目录 

1．7．10 查看文件或目录的版本变革 

1．7．11 从以前版本重新开始 

1．7．12 创建分支 

1．7．13 沿着分支开发 

1．7．14 合并分支 

1．7．15 使用Eclipse作为SVN客户端 

1．8 本章小结



#  第2章 JSP/Servlet及相关技术详解 

2．1 Web应用和web．xml文件 

2．1．1 构建Web应用 

2．1．2 配置描述符web．xml 

2．2 JSP的基本原理 

2．3 JSP的4种基本语法 

2．3．1 JSP注释 

2．3．2 JSP声明 

2．3．3 输出JSP表达式 

2．3．4 JSP脚本 

2．4 JSP的3个编译指令 

2．4．1 page指令 

2．4．2 include指令 

2．5 JSP的7个动作指令 

2．5．1 forward指令 

2．5．2 include指令 

2．5．3 useBean、setProperty、getProperty指令 

2．5．4 plugin指令 

2．5．5 param指令 

2．6 JSP脚本中的9个内置对象 

2．6．1 application对象 

2．6．2 config对象 

2．6．3 exception对象 

2．6．4 out对象 

2．6．5 pageContext对象 

2．6．6 request对象 

2．6．7 response对象 

2．6．8 session对象 

2．7 Servlet介绍 

2．7．1 Servlet的开发 

2．7．2 Servlet的配置 

2．7．3 JSP/Servlet的生命周期 

2．7．4 load-on-startup Servlet 

2．7．5 访问Servlet的配置参数 

2．7．6 使用Servlet作为控制器 

2．8 JSP 2的自定义标签 

2．8．1 开发自定义标签类 

2．8．2 建立TLD文件 

2．8．3 使用标签库 

2．8．4 带属性的标签 

2．8．5 带标签体的标签 

2．8．6 以页面片段作为属性的标签 

2．8．7 动态属性的标签 

2．9 Filter介绍 

2．9．1 创建Filter类 

2．9．2 配置Filter 

2．9．3 使用URL Rewrite实现网站伪静态 

2．10 Listener介绍 

2．10．1 实现Listener类 

2．10．2 配置Listener 

2．10．3 使用ServletContextAttributeListener 

2．10．4 使用ServletRequestListener和ServletRequestAttributeListener 

2．10．5 使用HttpSessionListener和HttpSessionAttributeListener 

2．11 JSP 2特性 

2．11．1 配置JSP属性 

2．11．2 表达式语言 

2．11．3 Tag File支持 

2．12 Servlet 3．0新特性 

2．12．1 Servlet 3．0的注解 

2．12．2 Servlet 3．0的Web模块支持 

2．12．3 Servlet 3．0提供的异步处理 

2．12．4改进的Servlet API 

2．13 Servlet 3．1新增的非阻塞式IO 

2．14 Tomcat 8的WebSocket支持 

2．15 本章小结



#  第3章 Struts 2的基本用法 

3．1 MVC思想概述 

3．1．1 传统Model 1和Model 2 

3．1．2 MVC思想及其优势 

3．2 Struts 2的下载和安装 

3．2．1 为Web应用增加Struts 2支持 

3．2．2 在Eclipse中使用Struts 2 

3．2．3 增加登录处理 

3．3 Struts 2的流程 

3．3．1 Struts 2应用的开发步骤 

3．3．2 Struts 2的流程 

3．4 Struts 2的常规配置 

3．4．1 常量配置 

3．4．2 包含其他配置文件 

3．5 实现Action 

3．5．1 Action接口和ActionSupport基类 

3．5．2 Action访问Servlet API 

3．5．3 Action直接访问Servlet API 

3．5．4 使用ServletActionContext访问Servlet API 

3．6 配置Action 

3．6．1 包和命名空间 

3．6．2 Action的基本配置 

3．6．3 使用Action的动态方法调用 

3．6．4 指定method属性及使用通配符 

3．6．5 配置默认Action 

3．6．6 配置Action的默认处理类 

3．7 配置处理结果 

3．7．1 理解处理结果 

3．7．2 配置结果 

3．7．3 Struts 2支持的结果类型 

3．7．4 plainText结果类型 

3．7．5 redirect结果类型 

3．7．6 redirectAction结果类型 

3．7．7 动态结果 

3．7．8 Action属性值决定物理视图资源 

3．7．9 全局结果 

3．7．10 使用PreResultListener 

3．8 配置Struts 2的异常处理 

3．8．1 Struts 2的异常处理机制 

3．8．2 声明式异常捕捉 

3．8．3 输出异常信息 

3．9 Convention插件与"约定"支持 

3．9．1 Action的搜索和映射约定 

3．9．2 按约定映射Result 

3．9．3 Action链的约定 

3．9．4 自动重加载映射 

3．9．5 Convention插件的相关常量 

3．9．6 Convention插件相关Annotation 

3．10 使用Struts 2的国际化 

3．10．1 视图页面的国际化 

3．10．2 Action的国际化 

3．10．3 使用包范围的国际化资源 

3．10．4 使用全局国际化资源 

3．10．5 输出带占位符的国际化消息 

3．10．6 加载资源文件的顺序 

3．11 使用Struts 2的标签库 

3．11．1 Struts 2标签库概述 

3．11．2 使用Struts 2标签 

3．11．3 Struts 2的OGNL表达式语言 

3．11．4 OGNL中的集合操作 

3．11．5 访问静态成员 

3．11．6 Lambda（）表达式 

3．11．7 控制标签 

3．11．8 数据标签 

3．11．9 主题和模板 

3．11．10 自定义主题 

3．11．11 表单标签 

3．11．12 非表单标签 

3．12 本章小结



#  第4章 深入使用Struts 2 

4．1 详解Struts 2的类型转换 

4．1．1 Struts 2内建的类型转换器 

4．1．2 基于OGNL的类型转换 

4．1．3 指定集合元素的类型 

4．1．4 自定义类型转换器 

4．1．5 注册类型转换器 

4．1．6 基于Struts 2的自定义类型转换器 

4．1．7 处理Set集合 

4．1．8 类型转换中的错误处理 

4．2 使用Struts 2的输入校验 

4．2．1 编写校验规则文件 

4．2．2 国际化提示信息 

4．2．3 使用客户端校验 

4．2．4 字段校验器配置风格 

4．2．5 非字段校验器配置风格 

4．2．6 短路校验器 

4．2．7 校验文件的搜索规则 

4．2．8 校验顺序和短路 

4．2．9 内建校验器 

4．2．10 基于注解的输入校验 

4．2．11 手动完成输入校验 

4．3 使用Struts 2控制文件上传 

4．3．1 Struts 2的文件上传 

4．3．2 实现文件上传的Action 

4．3．3 配置文件上传的Action 

4．3．4 手动实现文件过滤 

4．3．5 拦截器实现文件过滤 

4．3．6 输出错误提示 

4．3．7 文件上传的常量配置 

4．4 使用Struts 2控制文件下载 

4．4．1 实现文件下载的Action 

4．4．2 配置Action 

4．4．3 下载前的授权控制 

4．5 详解Struts 2的拦截器机制 

4．5．1 拦截器在Struts 2中的作用 

4．5．2 Struts 2内建的拦截器 

4．5．3 配置拦截器 

4．5．4 使用拦截器的配置语法 

4．5．5 配置默认拦截器 

4．5．6 实现拦截器类 

4．5．7 使用拦截器 

4．5．8 拦截方法的拦截器 

4．5．9 拦截器的执行顺序 

4．5．10 拦截结果的监听器 

4．5．11 覆盖拦截器栈里特定拦截器的参数 

4．5．12 使用拦截器完成权限控制 

4．6 使用Struts 2的Ajax支持 

4．6．1 使用stream类型的Result实现Ajax 

4．6．2 JSON的基本知识 

4．6．3 实现Action逻辑 

4．6．4 JSON插件与json类型的Result 

4．6．5 实现JSP页面 

4．7 本章小结



#  第5章 Hibernate的基本用法 

5．1 ORM和Hibernate 

5．1．1 对象/关系数据库映射（ORM） 

5．1．2 基本映射方式 

5．1．3 流行的ORM框架简介 

5．1．4 Hibernate概述 

5．2 Hibernate入门 

5．2．1 Hibernate下载和安装 

5．2．2 Hibernate的数据库操作 

5．2．3 在Eclipse中使用Hibernate

5．3 Hibernate的体系结构

5．4 深入Hibernate配置文件 

5．4．1 创建Configuration对象 

5．4．2 hibernate．properties文件与hibernate．cfg．xml文件 

5．4．3 JDBC连接属性 

5．4．4 数据库方言 

5．4．5 JNDI数据源的连接属性 

5．4．6 Hibernate事务属性 

5．4．7 二级缓存相关属性 

5．4．8 外连接抓取属性 

5．4．9 其他常用的配置属性 

5．5 深入理解持久化对象 

5．5．1 持久化类的要求 

5．5．2 持久化对象的状态 

5．5．3 改变持久化对象状态的方法 

5．6 深入Hibernate映射 

5．6．1 映射属性 

5．6．2 映射主键 

5．6．3 使用Hibernate的主键生成策略 

5．6．4 映射集合属性 

5．6．5 集合属性的性能分析 

5．6．6 有序集合映射 

5．6．7 映射数据库对象 

5．7 映射组件属性 

5．7．1 组件属性为集合 

5．7．2 集合属性的元素为组件 

5．7．3 组件作为Map的索引 

5．7．4 组件作为复合主键 

5．7．5 多列作为联合主键 

5．8 使用传统的映射文件 

5．8．1 增加XML映射文件 

5．8．2 注解，还是XML映射文件 

5．9 本章小结



#  第6章 深入使用Hibernate 

6．1 Hibernate的关联映射 

6．1．1 单向N－1关联 

6．1．2 单向1－1关联 

6．1．3 单向1－N关联 

6．1．4 单向N－N关联 

6．1．5 双向1－N关联 

6．1．6 双向N－N关联 

6．1．7 双向1－1关联 

6．1．8 组件属性包含的关联实体 

6．1．9 基于复合主键的关联关系 

6．1．10 复合主键的成员属性为关联实体 

6．1．11 持久化的传播性 

6．2 继承映射 

6．2．1 整个类层次对应一个表的映射策略 

6．2．2 连接子类的映射策略 

6．2．3 每个具体类对应一个表的映射策略 

6．3 Hibernate的批量处理 

6．3．1 批量插入 

6．3．2 批量更新 

6．3．3 DML风格的批量更新/删除 

6．4 使用HQL查询 

6．4．1 HQL查询 

6．4．2 HQL查询的from子句 

6．4．3 关联和连接 

6．4．4 HQL查询的select子句 

6．4．5 HQL查询的聚集函数 

6．4．6 多态查询 

6．4．7 HQL查询的where子句 

6．4．8 表达式 

6．4．9 order by子句 

6．4．10 group by子句 

6．4．11 子查询 

6．4．12 命名查询 

6．5 条件查询 

6．5．1 关联和动态关联 

6．5．2 投影、聚合和分组 

6．5．3 离线查询和子查询 

6．6 SQL查询 

6．6．1 标量查询 

6．6．2 实体查询 

6．6．3 处理关联和继承 

6．6．4 命名SQL查询 

6．6．5 调用存储过程 

6．6．6 使用定制SQL 

6．7 数据过滤 

6．8 事务控制 

6．8．1 事务的概念 

6．8．2 Session与事务 

6．8．3 上下文相关的Session 

6．9 二级缓存和查询缓存 

6．9．1 开启二级缓存 

6．9．2 管理缓存和统计缓存 

6．9．3 使用查询缓存 

6．10 事件机制 

6．10．1 拦截器 

6．10．2 事件系统 

6．11 本章小结



#  第7章 Spring的基本用法 

7．1 Spring简介和Spring 4．0的变化 

依赖注入

AOP

在软件业，AOP为Aspect Oriented Programming的缩写，意为：面向切面编程，通过预编译方式和运行期动态代理实现程序功能的统一维护的一种技术。AOP是OOP的延续，是软件开发中的一个热点，也是Spring框架中的一个重要内容，是函数式编程的一种衍生范型。利用AOP可以对业务逻辑的各个部分进行隔离，从而使得业务逻辑各部分之间的耦合度降低，提高程序的可重用性，同时提高了开发的效率。

![](https://www.ibm.com/developerworks/cn/java/wa-spring1/spring_framework.gif)

组成 Spring 框架的每个模块（或组件）都可以单独存在，或者与其他一个或多个模块联合实现。每个模块的功能如下：
核心容器：核心容器提供 Spring 框架的基本功能。核心容器的主要组件是 BeanFactory，它是工厂模式的实现。BeanFactory 使用控制反转 （IOC） 模式将应用程序的配置和依赖性规范与实际的应用程序代码分开。

Spring 上下文：Spring 上下文是一个配置文件，向 Spring 框架提供上下文信息。Spring 上下文包括企业服务，例如 JNDI、EJB、电子邮件、国际化、校验和调度功能。

Spring AOP：通过配置管理特性，Spring AOP 模块直接将面向方面的编程功能集成到了 Spring 框架中。所以，可以很容易地使 Spring 框架管理的任何对象支持 AOP。Spring AOP 模块为基于 Spring 的应用程序中的对象提供了事务管理服务。通过使用 Spring AOP，不用依赖 EJB 组件，就可以将声明性事务管理集成到应用程序中。

Spring DAO：JDBC DAO 抽象层提供了有意义的异常层次结构，可用该结构来管理异常处理和不同数据库供应商抛出的错误消息。异常层次结构简化了错误处理，并且极大地降低了需要编写的异常代码数量（例如打开和关闭连接）。Spring DAO 的面向 JDBC 的异常遵从通用的 DAO 异常层次结构。

Spring ORM：Spring 框架插入了若干个 ORM 框架，从而提供了 ORM 的对象关系工具，其中包括 JDO、Hibernate 和 iBatis SQL Map。所有这些都遵从 Spring 的通用事务和 DAO 异常层次结构。

Spring Web 模块：Web 上下文模块建立在应用程序上下文模块之上，为基于 Web 的应用程序提供了上下文。所以，Spring 框架支持与 Jakarta Struts 的集成。Web 模块还简化了处理多部分请求以及将请求参数绑定到域对象的工作。

Spring MVC 框架：MVC 框架是一个全功能的构建 Web 应用程序的 MVC 实现。通过策略接口，MVC 框架变成为高度可配置的，MVC 容纳了大量视图技术，其中包括 JSP、Velocity、Tiles、iText 和 POI。

Spring 框架的功能可以用在任何 J2EE 服务器中，大多数功能也适用于不受管理的环境。Spring 的核心要点是：支持不绑定到特定 J2EE 服务的可重用业务和数据访问对象。毫无疑问，这样的对象可以在不同 J2EE 环境 （Web 或 EJB）、独立应用程序、测试环境之间重用。


- IOC:

控制反转模式（也称作依赖性介入）的基本概念是：不创建对象，但是描述创建它们的方式。在代码中不直接与对象和服务连接，但在配置文件中描述哪一个组件需要哪一项服务。容器 （在 Spring 框架中是 IOC 容器） 负责将这些联系在一起。
在典型的 IOC 场景中，容器创建了所有对象，并设置必要的属性将它们连接在一起，决定什么时间调用方法。下表列出了 IOC 的一个实现模式。


1. 类型 1	服务需要实现专门的接口，通过接口，由对象提供这些服务，可以从对象查询依赖性（例如，需要的附加服务）
2. 类型 2	通过 JavaBean 的属性（例如 setter 方法）分配依赖性
3. 类型 3	依赖性以构造函数的形式提供，不以 JavaBean 属性的形式公开

- AOP:


**清楚的解释:**
最近在学这方面的内容，读到的这段话我感觉说的很清楚了：这种在运行时，动态地将代码切入到类的指定方法、指定位置上的编程思想就是面向切面的编程。

[链接](https://www.zhihu.com/question/24863332/answer/48376158)

面向切面编程（AOP是Aspect Oriented Program的首字母缩写） ，我们知道，面向对象的特点是继承、多态和封装。而封装就要求将功能分散到不同的对象中去，这在软件设计中往往称为职责分配。实际上也就是说，让不同的类设计不同的方法。这样代码就分散到一个个的类中去了。这样做的好处是降低了代码的复杂程度，使类可重用。      

但是人们也发现，在分散代码的同时，也增加了代码的重复性。什么意思呢？比如说，我们在两个类中，可能都需要在每个方法中做日志。按面向对象的设计方法，我们就必须在两个类的方法中都加入日志的内容。也许他们是完全相同的，但就是因为面向对象的设计让类与类之间无法联系，而不能将这些重复的代码统一起来。    

也许有人会说，那好办啊，我们可以将这段代码写在一个独立的类独立的方法里，然后再在这两个类中调用。但是，这样一来，这两个类跟我们上面提到的独立的类就有耦合了，它的改变会影响这两个类。那么，有没有什么办法，能让我们在需要的时候，随意地加入代码呢？这种在运行时，动态地将代码切入到类的指定方法、指定位置上的编程思想就是面向切面的编程。       一般而言，我们管切入到指定类指定方法的代码片段称为切面，而切入到哪些类、哪些方法则叫切入点。有了AOP，我们就可以把几个类共有的代码，抽取到一个切片中，等到需要时再切入对象中去，从而改变其原有的行为。这样看来，AOP其实只是OOP的补充而已。OOP从横向上区分出一个个的类来，而AOP则从纵向上向对象中加入特定的代码。有了AOP，OOP变得立体了。如果加上时间维度，AOP使OOP由原来的二维变为三维了，由平面变成立体了。从技术上来说，AOP基本上是通过代理机制实现的。      AOP在编程历史上可以说是里程碑式的，对OOP编程是一种十分有益的补充。

面向方面的编程，即 AOP，是一种编程技术，它允许程序员对横切关注点或横切典型的职责分界线的行为（例如日志和事务管理）进
行模块化。AOP 的核心构造是方面，它将那些影响多个类的行为封装到可重用的模块中。

AOP 和 IOC 是补充性的技术，它们都运用模块化方式解决企业应用程序开发中的复杂问题。在典型的面向对象开发方式中，可能要将日志记录语句放在所有方法和 Java 类中才能实现日志功能。在 AOP 方式中，可以反过来将日志服务模块化，并以声明的方式将它们应用到需要日志的组件上。当然，优势就是 Java 类不需要知道日志服务的存在，也不需要考虑相关的代码。所以，用 Spring 
AOP 编写的应用程序代码是松散耦合的。

AOP 的功能完全集成到了 Spring 事务管理、日志和其他各种特性的上下文中。



## 反射

Class.forName、实例对象.class(属性)、实例对象getClass()的区别

1、相同点：
    通过这几种方式，得到的都是Java.lang.Class对象（这个是上面讲到的 类在加载时获得的最终产物）
  例如：
  
```
package demo;
public class A
{
    public static void main(String[] args) throws Exception
    {
        System.out.println(A.class);//通过类.class获得Class对象

        A a = new A();
        System.out.println(a.getClass());//通过 实例名.getClass()获得Class对象
        System.out.println(Class.forName("demo.A"));//通过Class.forName(全路径)获得Class对象
            System.out.println(".................................");
        System.out.println(a);//使用不同的方式创建对象
        System.out.println(A.class.newInstance());
        System.out.println(a.getClass().newInstance());
        System.out.println(Class.forName("demo.A").newInstance());  
    }
}

结果：class demo.A
      class demo.A
      class demo.A   （这里也可以得到一个类的Class对象是唯一的）
.......................................
      demo.A@de6ced
      demo.A@c17164
      demo.A@1fb8ee3
      demo.A@61de33
```

 2、区别：
  
1. Class cl=A.class; JVM将使用类A的类装载器,将类A装入内存(前提是:类A还没有装入内存),不对类A做类的初始化工作.返回类A的Class的对象
2. Class cl=对象引用o.getClass();返回引用o运行时真正所指的对象
(因为:儿子对象的引用可能会赋给父对象的引用变量中)所属的类的Class的对象 
3. Class.forName("类名"); JAVA人都知道.装入类A,并做类的初始化

## 动态代理

熟悉设计模式的人对于代理模式可 能都不陌生。 

代理对象和被代理对象一般实现相同的接口，调用者与代理对象进行交互。代理的存在对于调用者来说是透明的，调用者看到的只是接口。代理对象则可以封装一些内部的处理逻辑，如访问控制、远程通信、日志、缓存等。比如一个对象访问代理就可以在普通的访问机制之上添加缓存的支持。这种模式在RMI和EJB中都得到了广泛的使用。传统的代理模式的实现，需要在源代码中添加一些附加的类。这些类一般是手写或是通过工具来自动生成。

JDK 5引入的动态代理机制，允许开发人员在运行时刻动态的创建出代理类及其对象。在运行时刻，可以动态创建出一个实现了多个接口的代理类。每个代理类的对象都会关联一个表示内部处理逻辑的InvocationHandler接 口的实现。当使用者调用了代理对象所代理的接口中的方法的时候，这个调用的信息会被传递给InvocationHandler的invoke方法。在 invoke方法的参数中可以获取到代理对象、方法对应的Method对象和调用的实际参数。invoke方法的返回值被返回给使用者。这种做法实际上相 当于对方法调用进行了拦截。熟悉AOP的人对这种使用模式应该不陌生。但是这种方式不需要依赖AspectJ等AOP框架。

下面的代码用来代理一个实现了List接口的对象。所实现的功能也非常简单，那就是禁止使用List接口中的add方法。如果在getList中传入一个实现List接口的对象，那么返回的实际就是一个代理对象，尝试在该对象上调用add方法就会抛出来异常。


``` 
public List getList(final List list) {
    return (List) Proxy.newProxyInstance(DummyProxy.class.getClassLoader(), new Class[] { List.class },
        new InvocationHandler() {
            public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
                if ("add".equals(method.getName())) {
                    throw new UnsupportedOperationException();
                }
                else {
                    return method.invoke(list, args);
                }
            }
        });
 } 
```



7．1．1 Spring简介 

7．1．2 Spring 4．0的变化 

7．2 Spring入门 

7．2．1 Spring下载和安装 

7．2．2 使用Spring管理Bean 

所有的一切都是bean(只要是个java对象即可)

配置文件中的bean默认使用反射的方式调用无参数的构造器.


```
Class.forName(classNameStr)
```

ApplicationContext 是Spring常用的接口.


最常被使用的 ApplicationContext 接口实现：

1. FileSystemXmlApplicationContext：该容器从 XML 文件中加载已被定义的 bean。在这里，你需要提供给构造器 XML 文件的完整路径

1. ClassPathXmlApplicationContext：该容器从 XML 文件中加载已被定义的 bean。在这里，你不需要提供 XML 文件的完整路径，只需正确配置 CLASSPATH 环境变量即可，因为，容器会从 CLASSPATH 中搜索 bean 配置文件。

1. WebXmlApplicationContext：该容器会在一个 web 应用程序的范围内加载在 XML 文件中已被定义的 bean。


7．2．3 在Eclipse中使用Spring 

7．3 Spring的核心机制依赖注入


spring框架的核心功能有两个.

1. 容器的超级工厂,负责创建,管理所有的java对象. Bean
1. Spring管理所有Bean间的依赖关系. 采用依赖注入的方式来管理.

7．3．1 理解依赖注入 

依赖注入的两种注入的方式:
1. 设值注入  set方法
1. 构造注入  构造器注入

7．3．2 设值注入 

7．3．3 构造注入 

构造注入的本质:spring 调用无参数构造器来创建对象,利用构造器参数来执行初始化.

`constructor-arg ref="XX.XX.XX"`

7．3．4 两种注入方式的对比 

推荐使用设值注入为主,构造注入为辅的注入策略.


7．4 使用Spring容器 

7．4．1 Spring容器 

7．4．2 使用ApplicationContext 

7．4．3 ApplicationContext的国际化支持 

7．4．4 ApplicationContext的事件机制 

7．4．5 让Bean获取Spring容器 

7．5 Spring容器中的Bean 

7．5．1 Bean的基本定义和Bean别名 

7．5．2 容器中Bean的作用域 

7．5．3 配置依赖 

7．5．4 设置普通属性值 

7．5．5 配置合作者Bean 

7．5．6 使用自动装配注入合作者Bean 

7．5．7 注入嵌套Bean 

7．5．8 注入集合值 

7．5．9 组合属性 

7．5．10 Spring的Bean和JavaBean 

7．6 Spring 3．0提供的Java配置管理 

7．7 创建Bean的3种方式 

7．7．1 使用构造器创建Bean实例 

7．7．2 使用静态工厂方法创建Bean 

7．7．3 调用实例工厂方法创建Bean 

7．8 深入理解容器中的Bean 

7．8．1 抽象Bean与子Bean 

7．8．2 Bean继承与Java继承的区别 

7．8．3 容器中的工厂Bean 

7．8．4 获得Bean本身的id 

7．8．5 强制初始化Bean 

7．9 容器中Bean的生命周期 

7．9．1 依赖关系注入之后的行为 

7．9．2 Bean销毁之前的行为 

7．9．3 协调作用域不同步的Bean 

7．10 高级依赖关系配置 

7．10．1 获取其他Bean的属性值 

7．10．2 获取Field值 

7．10．3 获取方法返回值 

7．11 基于XML Schema的简化配置方式 

7．11．1 使用p：命名空间简化配置 

7．11．2 使用c：命名空间简化配置 

7．11．3 使用util：命名空间简化配置 

7．12 Spring 3．0提供的表达式语言（SpEL） 

7．12．1 使用Expression接口进行表达式求值 

7．12．2 Bean定义中的表达式语言支持 

7．12．3 SpEL语法详述 

7．13 本章小结



#  第8章 深入使用Spring 

8．1 两种后处理器 

8．2 Spring的"零配置"支持 

8．3 资源访问 

8．4 Spring的AOP 

8．5 Spring 3．1新增的缓存机制 

8．7 Spring整合Struts 2 

8．8 Spring整合Hibernate 

8．9 Spring整合JPA 

8．10 本章小结



#  第9章 企业应用开发的思考和策略 

9．1 企业应用开发面临的挑战 

9．2 如何面对挑战 

9．3 常见设计模式精讲 

9．4 常见的架构设计策略 

9．5 本章小结



#  第10章 简单工作流系统 

10．1 项目背景及系统结构 

10．2 Hibernate持久层 

10．3 实现DAO层 

10．4 实现Service层 

10．5 实现任务的自动调度 

10．6 实现系统Web层 

10．7 本章小结