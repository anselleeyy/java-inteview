---
description: Redis
---

# Redis 缓存

### 0 前言

> Redis 是完全开源免费的，遵守BSD协议，是一个高性能的 key-value 数据库
>
> Redis 相比其他 key-value 缓存产品有以下三个特性：
>
> * Redis支持数据的持久化，可以将内存中的数据保持在磁盘中，重启的时候可以再次加载进行使用
> * Redis不仅仅支持简单的key-value类型的数据，同时还提供list，set，zset，hash等数据结构的存储
> * Redis支持数据的备份，即master-slave模式的数据备份

### 目录

* [为什么使用 Redis](redis.md#1-wei-shen-me-shi-yong-redis)
* 
### 1 为什么使用 Redis

#### 1.1 性能

> 场景：当我们遇到需要执行耗时特别久，且结果不频繁变动的SQL的情况下，将结果放入缓存，让后面的请求去缓存中读取，使得请求能够迅速响应

#### 1.2 并发

> 场景：在大并发的情况下，所有的操作直接访问数据库，数据库会出现连接异常。我们通过使用 Redis 做一个缓冲操作，减少数据库的压力

### 2 Redis 的五种基本数据类型

<table>
  <thead>
    <tr>
      <th style="text-align:center">数据类型</th>
      <th style="text-align:center">可以存储的值</th>
      <th style="text-align:center">操作</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">STRING</td>
      <td style="text-align:center">字符串、整数以及浮点数</td>
      <td style="text-align:center">
        <p>对整个字符串或者字符串的一部分执行操作</p>
        <p>对整数和浮点数执行自增或者自减操作</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">LIST</td>
      <td style="text-align:center">列表</td>
      <td style="text-align:center">
        <p>从两端压入或者弹出元素</p>
        <p>对单个或者多个元素进行修剪，只保留一个范围内的元素</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">HASH</td>
      <td style="text-align:center">包含键值对的无序散列列表</td>
      <td style="text-align:center">
        <p>添加、获取、移出单个键值对</p>
        <p>获取所有键值对</p>
        <p>检查某个键是否存在</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">SET</td>
      <td style="text-align:center">无序集合</td>
      <td style="text-align:center">
        <p>添加、获取、移出单个元素</p>
        <p>检查一个元素是否在集合中</p>
        <p>计算交集、并集、差集</p>
        <p>从集合中随机获取元素</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">ZSET</td>
      <td style="text-align:center">
        <p>有序集合</p>
        <p>每个元素都会关联一个double类型的分数</p>
        <p>redis正是通过分数来进行从小到大的排序</p>
      </td>
      <td style="text-align:center">
        <p>添加、获取、删除元素</p>
        <p>根据分值范围或者成员来获取元素</p>
        <p>计算一个键的排名</p>
      </td>
    </tr>
  </tbody>
</table>### 3 Redis 为什么快

* Redis 是纯内存的操作
* Redis是单线程的，避免了频繁的线程上下文切换
* 采用了非阻塞 I/O 多路复用机制

#### 3.1 I/O 多路复用机制

_**什么是 I/O多路复用**_

> I/O 即网络 I/O，多路指多个TCP连接（或多个Channel），复用指的是复用一个或少量线程
>
> I/O 多路复用和阻塞式I/O的区别：
>
> * I/O 多路复用通过 select 机制，可以避免传统阻塞式 I/O 为每一个连接创建线程的问题
> * 多路复用将大量的连接请求注册到 selector 复用器上，使用少量的线程来处理这些连接请求

_**Redis 提供的多路复用方法**_

> Redis 提供了 select、poll、epoll 等方法，以此可以同时监察多个流的 I/O 事件的能力
>
> 在空闲时，Redis 会将当前线程阻塞掉，当有一个或多个 I/O 请求时间时，就会从阻塞态中唤醒，程序会轮询（epoll）一遍那些发出了请求的流，并依次处理
>
> 通过多路复用的方法，单个线程可以高效的处理多个连接请求，且内存的高效速度，使得操作数据并不会成为 Redis 的性能瓶颈，最终造就 Redis 的高吞吐量

### 4 Redis 的持久化机制

#### 4.1 RDB

#### 4.2 AOF

### 5 Redis 的缺点

#### 5.1 缓存和数据库双写一致性的问题

