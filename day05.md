# HTTP

## Servlet 线程安全问题

1. Servlet 的 service 方法是被并发访问的.
2. 如果 "Servlet中存在公共的可读写变量" 将出现线程安全问题
	- Servlet中存在公共的可读写变量: 有状态的Servlet
3. 将 Servlet 声明成无状态的, 来解决线程安全问题.

如何避免业务层的线程安全问题? 

将控制器和业务层声明为 "无状态" 来解决线程安全问题.

## JSP 的9大内置对象

常用的: request, response, out, session
不常用: application, pageContext, page
很少使用: execption, config

可以用标准标签替代: JSTL+EL

## Spring

默认情况下Spring 中的Java Bean是单例的!
	- 单一实例, 任何是从Spring获取Bean都是同一个对象

单例: 在一个软件中, 对象的个体始终是一个的现象称为单例.

模式(设计模式): 解决特定问题的固定编程套路.

单例模式: 解决软件中对象始终位置的固定编程套路.

容器: 泛指能承载对象的一种集合

能够承载 Servlet/JSP等WEB组件的服务器被叫做 Web容器/Servlet容器/Servlet引擎.

WEB 服务器: 能够作为服务器端出来HTTP请求服务器
	- nginx
	- Apache+PHP
	- MS IIS + .net
	- Java Web 服务器
		- Tomcat
		- Jetty
		- Web Spare
		- Web Logic

Spring 是 Java Bean 容器: Spring 用于承载JavaBean对象.

Java Bean: 类型符合特定规则的Java 对象

- 必须有包
- 必须有无参数构造器
- 实现序列化接口
- 可以包含 getXxx setXxx 声明的 Bean属性 xxx
	- Bean 属性就是指 get 和 set 方法, Bean属性不是对象属性!
	- boolean类型的Bean属性, 可以 getXxx 或 isXxx  

Spring 两大核心功能: 

1. IOC/DI 控制反转/依赖注入
	- 控制反转: 将用代码控制对象创建管理的功能交给Spring容器, 由Spring控制对象创建管理 
	- 依赖注入: 按照对象之间的依赖关系进行赋值, 解决对象依赖问题.
	- 底层利用反射技术实现.
2. AOP 面向切面(儿)编程: 在不改变软件原有功能情况下为软件扩展横切功能.
	- Spting AOP 底层 是 AspectJ, AspectJ的底层是 动态代理   
	- 声明式事务底层就是 AOP, 日志, 性能测试...

MVC 与 3层架构的区别

- MVC 和 3层结构 没有直接关系! 

看图...


MVC 与 Spring MVC


