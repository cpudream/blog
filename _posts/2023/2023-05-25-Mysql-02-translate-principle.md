---
layout: post
title:  "Mysql进阶-事务"
date:   2023-05-25 22:10:54
catalog:  true
tags:
    - Mysql进阶计划
    - Mysql

---

**事务、索引、锁等是数据库使用中的高频知识点**

> 最经典的例子就是转账，你要给朋友小王转 100 块钱，而此时你的银行卡只有 100 块钱。转账过程具体到程序里会有一系列的操作，比如查询余额、做加减法、更新余额等。

事务支持是在引擎层实现的。MyISAM引擎不支持事务，也就是被InnoDB取代的原因。

## 一、隔离性与隔离级别

ACID（Atomicity、Consistency、Isolation、Durability，即原子性、一致性、隔离性、持久性）

