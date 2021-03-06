# 5.Spring AOP

面向方面编程（AOP）通过提供对程序结构的另一种思考方式来补充面向对象编程（OOP）。OOP中模块化的关键单元是类，而AOP中模块化的单元是方面。方面支持跨多个类型和对象的关注点（如事务管理）的模块化。（在AOP文献中，这种关注通常被称为“横切”关注。）

Spring的关键组件之一是AOP框架。虽然SpringIOC容器不依赖于AOP（也就是说，如果不想使用AOP，就不需要使用AOP），但是AOP补充了SpringIOC，提供了一个非常强大的中间件解决方案。

> Spring AOP和AspectJ切点
>
> Spring提供了使用基于模式的方法或@Aspectj注解样式来编写自定义方面。这两种风格都提供了完整类型的通知，并可以在使用SpringAOP进行编织的同时使用AspectJ切入点语言。
>
> 本章讨论基于 schema-和@Aspectj的AOP支持。下一章将讨论较低级别的AOP支持。

AOP在Spring框架中被使用，主要用在以下几个方面：

* 提供声明性企业服务。最重要的此类服务是声明性事务管理。
* 让用户实现自定义方面，用AOP补充OOP的使用。

> 如果你只对通用声明性服务或其他预打包的声明性中间件服务（如池）感兴趣，则不需要直接使用SpringAOP，可以跳过本章的大部分内容。

