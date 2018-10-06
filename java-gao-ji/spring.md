---
description: Based on Spring5
---

# Spring

## IoC

### IoC 简介

> 控制反转（Inversion of Control，缩写为IoC），是面向对象编程中的一种设计原则，可以用来减低计算机代码之间的耦合度。其中最常见的方式叫做依赖注入（Dependency Injection，简称DI），还有一种方式叫“依赖查找”（Dependency Lookup）。通过控制反转，对象在被创建的时候，由一个调控系统内所有对象的外界实体，将其所依赖的对象的引用传递给它。也可以说，依赖被注入到对象中。\(from Wiki\)

控制反转是一种通过描述并通过第三方去产生或获取特定对象的方式。在Spring中实现控制反转的是IoC容器，其实现方法是DI（依赖注入）。

比如说我们现在有两个类A和B，那么我们不需要new A\(\)、或者new B\(\)来创建A和B的对象，Spring会帮我们创建A和B的对象（默认是单例），并且把A和B的对象放入IoC容器中，如果B对象中需要用到A对象的话，那么就要用到DI，Spring会帮我们把A对象注入到B对象中，一般是通过setter方法注入或构造器注入。

### IoC 容器的设计

> 在 Spring 中，有两个主要的 IoC 容器系列，一个是实现 BeanFactory 接口的简单容器系列，这系列容器只实现了容器的基本功能，另一个是实现 ApplicationContext 接口的高级容器系列，相较于简单容器系列，增加了许多面向框架的特性

#### BeanFactory

#### ApplicationContext

