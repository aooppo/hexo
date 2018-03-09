title: Whats new in Spring Boot 2
date: 2018-03-09T09:35:26.198Z
tags: [springboot]
categories: []
---
# 新版本值得关注的亮点有哪些：

## 基于 Java 8，支持 Java 9

也就是说Spring Boot2.0的最低版本要求为JDK8，据了解国内大部分的互联网公司系统都还跑在JDK1.6/7上，因此想要升级到Spring Boot2.0的同学们注意啦，同时支持了Java9，也仅仅是支持而已。

## 响应式编程

使用 Spring WebFlux/WebFlux.fn提供响应式 Web 编程支持， Webflux 是一个全新的非堵塞的函数式 Reactive Web 框架，可以用来构建异步的、非堵塞的、事件驱动的服务，在伸缩性方面表现非常好，此功能来源于Spring5.0。

Spring Boot2.0也提供对响应式编程的自动化配置，如：Reactive Spring Data、Reactive Spring Security 等

## HTTP/2支持

在Tomcat, Undertow 和 Jetty 中均已支持 HTTP/2

## 对Kotlin支持

引入对 Kotlin 1.2.x 的支持，并提供了一个 runApplication 函数，让你通过惯用的 Kotlin 来运行 Spring Boot 应用程序。

## 全新的执行器架构

全新的执行器架构，支持 Spring MVC, WebFlux 和 Jersey

## 支持 Quartz

Spring Boot1.0并没有提供对 Quartz 的支持，之前出现了各种集成方案，Spring Boot2.0给出了最简单的集成方式。

## Security

大大的简化了安全自动配置

## Metrics

Metrics方面，Spring Boot 2引入了Micrometer，来统一metrics的规范，使得开发人员更好的理解和使用metrics的模块，而不需要关心对接的具体存储是什么。

## 监控方面

Spring Boot 2 增强了对 Micrometer 的集成。RabbitMQ、JVM 线程和垃圾收集指标会自动进行 instrument 监控，异步控制器(controller)也会自动添加到监控里。通过集成，还可以对 InfluxDB 服务器进行监控。

## 数据方面

db方面，默认引入了HikariCP，替代了之前的tomcat-pool作为底层的数据库连接池， 对比于tomcat-pool， HikariCP拥有更好的性能，总而言之就是提高了db的访问速度
JOOQ的支持
Redis方面， 默认引入了Lettuce, 替代了之前的jedis作为底层的redis链接方式
MongoDB\Hibernate优化
Thymeleaf 3

Spring Boot 2支持了Thymeleaf 3，Thymeleaf 3相对于Thymeleaf 2性能提升可不是一点点，因为2.0的性能确实不咋地，同时也使用了新的页面解析系统。

## OAuth 2.0

同时也加入了 对于OAuth 2.0的支持， 使得开发人员更加友好的使用spring-security来完成权限模块的开发

## 依赖组件的更新

Jetty 9.4
Tomcat 8.5
Flyway 5
Hibernate 5.2
Gradle 3.4
Thymeleaf 3.0