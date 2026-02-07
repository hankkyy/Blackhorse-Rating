# 黑马点评（hm-dianping）
# Blackhorse Rating (hm-dianping)

> 基于 Spring Boot 的本地生活服务平台后端项目（黑马程序员课程实战）  
> A backend project for a local lifestyle service platform based on Spring Boot (Blackhorse Programmer course practice).

---

## 📌 项目简介 | Project Overview

### 中文
本项目是“黑马点评”后端系统的实现与学习实践，围绕真实的本地生活业务场景，系统性地练习 **Spring Boot + MyBatis + Redis** 的工程化开发能力。  
重点涵盖用户体系、商户管理、优惠券秒杀、高并发缓存设计以及分布式锁等核心后端技术。

### English
This project is a backend implementation of **Blackhorse Rating**, designed as a practical learning project based on a real-world local service platform scenario.  
It focuses on building engineering skills with **Spring Boot, MyBatis, and Redis**, covering user management, shop services, coupon seckill, high-concurrency optimization, and distributed locking.

---

## ✨ 核心功能 | Key Features

### 中文
- **用户模块**
  - 手机号验证码登录
  - 基于 Redis 的 Token 登录态管理
- **商户模块**
  - 商户与分类查询
  - 附近商户查询（基于地理位置）
- **优惠券模块**
  - 优惠券发布与查询
  - 秒杀优惠券（高并发场景）
- **高并发优化**
  - 缓存穿透 / 雪崩 / 击穿处理
  - 基于 Redis 的分布式锁
  - 秒杀库存扣减与订单异步处理
- **数据一致性**
  - 数据库与缓存一致性设计

### English
- **User Module**
  - Phone-based login with verification code
  - Token-based authentication using Redis
- **Shop Module**
  - Shop and category queries
  - Nearby shop search (Geo-based)
- **Coupon Module**
  - Coupon creation and query
  - Seckill (flash sale) coupons under high concurrency
- **High-Concurrency Optimization**
  - Cache penetration, breakdown, and avalanche protection
  - Distributed locks based on Redis
  - Asynchronous order processing for seckill scenarios
- **Data Consistency**
  - Consistency strategies between database and cache

---

## 🛠 技术栈 | Tech Stack

- **Backend Framework**: Spring Boot  
- **ORM**: MyBatis / MyBatis-Plus  
- **Database**: MySQL  
- **Cache**: Redis  
- **Build Tool**: Maven  
- **Others**:
  - Redis GEO (location-based queries)
  - Redis Stream / Message Queue
  - Distributed lock design

---

## 📁 项目结构 | Project Structure

hm-dianping
├── src
│ ├── main
│ │ ├── java
│ │ │ └── com.xxx.hmdianping
│ │ └── resources
│ │ ├── mapper
│ │ ├── application.yml
│ └── test
├── pom.xml
└── README.md


---

## 🚀 本地运行 | Getting Started

### 1️⃣ 环境要求 | Prerequisites
- JDK 8+
- Maven 3.x
- MySQL 8.x
- Redis 6.x+

### 2️⃣ 配置 | Configuration
修改 `application.yml`：

```yml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/hm_dianping
    username: your_username
    password: your_password

  redis:
    host: localhost
    port: 6379
3️⃣ 启动项目 | Run the Application
mvn spring-boot:run
🎯 学习重点 | Learning Outcomes
中文
深入理解 Redis 在高并发业务中的应用

掌握秒杀系统的完整设计思路

熟悉缓存与数据库一致性问题的解决方案

提升 Spring Boot 后端项目工程能力

English
Gain hands-on experience with Redis in high-concurrency scenarios

Understand the complete design of a seckill system

Learn practical solutions for cache-database consistency

Improve backend engineering skills with Spring Boot

📎 说明 | Notes
本项目主要用于 学习与实践
This project is for learning and practice purposes

