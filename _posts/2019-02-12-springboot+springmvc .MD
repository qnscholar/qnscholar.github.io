---
layout: post
title: "springBoot+springMvc"
date: 2019-02-12
description: "复习--springBoot+springMvc"
tag: 复习
---
### 1.springBoot
#### 1.什么是 Spring Boot
Spring Boot是spring开源组织下的子项目，是spring组件一站式解决方案。主要是简化了spring的使用难度和简化了繁重的配置，提供了各种启动器，使开发者更容易上手。
#### 2.为什么要用 Spring Boot
独立运行、配置简化、自动配置、无代码生成和xml配置、应用监控、上手容易。
#### 3.SpringBoot 的核心注解是哪个？它主要由哪几个注解组成的
启动类上面的注解是@SpringBootApplication，它也是SpringBoot的核心注解，主要组合包含了以下 3 个注解：  
@SpringBootConfiguration：组合了 @Configuration 注解，实现配置文件的功能。  
@EnableAutoConfiguration：开启自动配置的功能，也可以关闭某个自动配置的选项，如关闭数据源自动配置功能： `@SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })`。  
@ComponentScan：Spring组件扫描。
#### 4.SpringBoot 自动配置原理
SpringBoot 自动配置主要通过 @EnableAutoConfiguration, @Conditional, @EnableConfigurationProperties 或者 @ConfigurationProperties 等几个注解来进行自动配置完成的。  
@EnableAutoConfiguration 开启自动配置，主要作用就是调用 Spring-Core 包里的 loadFactoryNames()，加载类路径及所有jar包下META-INF/spring.factories配置中映射的自动配置的类。  
@Conditional 条件注解，通过判断类路径下有没有相应配置的 jar 包来确定是否加载和自动配置这个类。  
@EnableConfigurationProperties 的作用就是，给自动配置提供具体的配置参数，只需要写在 application.properties 中，就可以通过映射写入配置类的 POJO 属性中。
#### 5.SpringBoot 中的 Starters
Starters可以理解为启动器，它包含了一系列可以集成到应用里面的依赖包，你可以一站式集成Spring及其他技术，而不需要到处找示例代码和依赖包。如你想使用Spring JPA访问数据库，
只要加入spring-boot-starter-data-jpa启动器依赖就能使用了。
#### 6.如何在 SpringBoot 启动的时候运行一些特定的代码
可以实现接口 ApplicationRunner 或者 CommandLineRunner，这两个接口实现方式一样，它们都只提供了一个 run 方法。
#### 7.SpringBoot 配置加载顺序
在 SpringBoot 里面，可以使用以下几种方式来加载配置。1）properties文件；2）YAML文件；3）系统环境变量；4）命令行参数；等。
#### 8.参考链接
[参考文章1](https://www.jianshu.com/p/63ad69c480fe) 
[参考文章2](https://www.cnblogs.com/3xmq/p/springboot.html)

### 2.SpringMVC
#### 1.什么是SpringMVC
SpringMVC是一个基于MVC架构、用来简化web应用程序开发的应用开发框架，它是Spring的一个模块,无需中间整合层来整合。
#### 2.SpringMVC的流程
（1）用户发送请求至前端控制器DispatcherServlet；  
（2） DispatcherServlet收到请求后，调用HandlerMapping处理器映射器，请求获取Handle；  
（3）处理器映射器根据请求url找到具体的处理器，生成处理器对象及处理器拦截器(如果有则生成)一并返回给DispatcherServlet；  
（4）DispatcherServlet通过HandlerAdapter处理器适配器调用处理器；
（5）执行处理器(Handler，也叫后端控制器)；  
（6）Handler执行完成返回ModelAndView；  
（7）HandlerAdapter将Handler执行结果ModelAndView返回给DispatcherServlet；  
（8）DispatcherServlet将ModelAndView传给ViewResolver视图解析器进行解析；  
（9）ViewResolver(包括InternalResourceViewResolver、XmlViewResolver、BeanNameViewResolver)解析后返回具体View；  
（10）DispatcherServlet对View进行渲染视图（即将模型数据填充至视图中）；  
（11）DispatcherServlet响应用户。  
![springMvc流程图](/images/article/javaWeb/springmvc-process.jpg "springMvc流程图")  

#### 3.Spring MVC 常用的 5 个注解:</h4>
@RequestMapping 、@PathVariable 、@RequestParam 、@RequestBoy 、@ResponseBody

#### 3.springMVC和struts2的区别
（1）springMvc的入口是一个servlet即前端控制器（DispatchServlet），而struts2入口是一个filter过虑器（StrutsPrepareAndExecuteFilter）。  
（2）springMvc是基于方法开发(一个url对应一个方法)，请求参数传递到方法的形参，可以设计为单例或多例(建议单例)，struts2是基于类开发，传递参数是通过类的属性，只能设计为多例。  
（3）Struts采用值栈存储请求和响应的数据，通过OGNL存取数据，springMvc通过参数解析器是将request请求内容解析，并给方法形参赋值，将数据和视图封装成ModelAndView对象，最后又将ModelAndView
中的模型数据通过request域传输到页面。Jsp视图解析器默认使用jstl。
#### 4.SpringMVC怎么设定重定向和转发
（1）在返回值前面加"forward:"就可以让结果转发,譬如`forward:user.do?name=method4`  
（2）在返回值前面加"redirect:"就可以让返回值重定向,譬如`redirect:http://www.baidu.com`
#### 5.SpringMvc里面拦截器是怎么写的？
有两种写法,一种是实现HandlerInterceptor接口,另外一种是继承适配器类,，接着在接口方法当中，实现处理逻辑；然后在SpringMvc的配置文件中配置拦截器即可。
#### 6.如何解决POST和GET请求中文乱码问题
（1）解决post请求乱码问题：在web.xml中加入CharacterEncodingFilter过滤器。  
（2）get请求中文参数出现乱码解决方法有两个：①修改tomcat配置文件添加编码与工程编码一致;②另外一种方法对参数进行重新编码。
#### 7.SpringMvc的控制器是不是单例模式,如果是,有什么问题,怎么解决？</h4>
是单例模式,所以在多线程访问的时候有线程安全问题,不要用同步,会影响性能的,解决方案是在控制器里面不能写字段。
#### 8.怎么样在方法里面得到Request,或者Session？
直接在方法的形参中声明request,SpringMvc就自动把request对象传入。
#### 9.参考链接
[参考文章](https://blog.csdn.net/a745233700/article/details/80963758)
