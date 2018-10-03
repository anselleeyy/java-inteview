---
description: Micro Services
---

# 微服务

### 什么是微服务

* 一系列微小的服务共同组成
* 跑在自己的进程里
* 每个服务为独立的业务开发
* 独立部署
* 分布式的管理

### 微服务架构的基本框架、组件

* 服务注册发现
* 服务网关
* 后端通用服务（中间层服务）
* 前端服务（边缘服务）【多 API 聚合、单个 API 裁剪】

## Spring Cloud Eureka

* 基于 Netflix Eureka 实现了二次封装

### 包含组件

* Eureka Server，注册中心
* Eureka Client，服务注册

