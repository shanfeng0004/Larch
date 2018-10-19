# Summary

* [介绍](README.md)
* 语言
  * C++
    * 基础语法
    * 标准库
    * boost
    * muduo库
    * 实现String类
    * 内存泄漏
    * makefile
    * gdb
    * 如何实现守护进程
    * 标准库函数和系统调用的区别
    * [推荐书籍](language/cplusplus/recommand_book.md)
  * golang
    * [推荐书籍](language/golang/recommand_book.md)
  * python
  * java
  * php
* 数据结构
  * 队列
    * 用队列实现栈
  * 集合
  * 链表、数组
    * 链表翻转
    * 链表是否有环
  * 字典、关联数组
  * 栈
    * 用栈实现队列
  * 树
    * 二叉树
      * 递归遍历
      * 非递归遍历
    * 完全二叉树
    * 平衡二叉树
    * 二叉查找树（BST）
    * 红黑树
    * trie树
    * B-，B+，B\*树
    * LSM 树
    * [redix 树](data_structure/tree/radix_tree.md)
  * 图
    * 有向
    * 无向
    * 广度优先
    * 深度优先
    * 最短路径: dijkstra/floyd
  * BitSet
* [常用算法](chang-yong-suan-fa.md)
  * 排序、查找算法
    * [选择排序](algorithm/select_sort.md)
    * [冒泡排序](algorithm/bubble_sort.md)
    * [插入排序](algorithm/insert_sort.md)
    * [快速排序](algorithm/quick_sort.md)
    * [归并排序](algorithm/merge_sort.md)
    * [希尔排序](algorithm/shell_sort.md)
    * [堆排序](algorithm/heap_sort.md)
    * [计数排序](algorithm/count_sort.md)
    * [桶排序](algorithm/bucket_sort.md)
    * [基数排序](algorithm/radix_sort.md)
    * [二分查找](algorithm/binary_search.md)
    * Java 中的排序工具
  * 布隆过滤器
  * 字符串
    * 字符串比较：KMP 算法
  * [数字](chang-yong-suan-fa/shu-zi.md)
    * [最长递增子序列](chang-yong-suan-fa/zui-chang-di-zeng-zi-xu-lie.md)
    * 最大子序列
    * 数组中最长递减子序列
    * [topN](algorithm/number/topN.md)
  * 深度优先、广度优先
  * 贪心算法
  * 回溯算法
  * 剪枝算法
  * 动态规划
  * 朴素贝叶斯
  * 推荐算法
  * 最小生成树算法
  * 最短路径算法
* 并发
  * Java 并发
  * C++ 并发
  * 多进程
  * 多线程
  * 线程安全
  * 一致性、事务
    * 事务 ACID 特性
    * 事务的隔离级别
    * MVCC
    * BASE
  * 锁
    * Java中的锁和同步类
    * 公平锁 & 非公平锁
    * 悲观锁
    * [乐观锁 & CAS & ABA 问题](concurrent/lock/cas.md)
    * lock free 队列
    * CopyOnWrite
    * RingBuffer
    * 可重入锁 & 不可重入锁
    * 互斥锁 & 共享锁
    * 死锁

* 操作系统
  * 计算机原理
  * CPU
    * 多级缓存
  * 进程
  * 线程
  * 协程
  * Linux
  * proc目录

* 设计模式
  * 设计模式的六大原则
  * 设计原则
  * 23种常见设计模式
  * 应用场景
  * 单例模式
  * 责任链模式
  * MVC
  * IOC
  * AOP
  * UML
  * 微服务思想
    * 康威定律
  

* [运维 & 统计 & 技术支持](yun-wei-and-tong-ji-and-ji-zhu-zhi-chi.md)
  * 常规监控
  * APM
  * 统计分析
  * 持续集成
    * Jenkins
    * 环境分离
  * 自动化运维
    * Ansible
    * puppet
    * chef
  * 测试
    * TDD 理论
    * 单元测试
    * 压力测试
    * 全链路压测
    * A/B 、灰度、蓝绿测试
  * 虚拟化
    * KVM
    * Xen
    * OpenVZ
  * 容器技术
    * Docker
  * 云技术
    * OpenStack
  * DevOps
  * 文档管理
* 中间件
  * Web Server
    * Nginx
    * OpenResty
    * Apache Httpd
    * Tomcat
      * 架构原理
      * 调优方案
    * Jetty
  * 缓存
    * 本地缓存
    * Web缓存
    * Memcached
    * Redis
      * 架构
        * [流程图](midware/redis/arch/redis_flow_chart.png)
      * 回收策略
      * 主从/sentinel/cluster
      * [推荐书籍](midware/redis/recommand_book.md)
    * Tair
  * 消息队列
    * 消息总线
    * 消息的顺序
    * RabbitMQ
    * RocketMQ
    * ActiveMQ
    * Kafka
    * Redis 消息推送
    * ZeroMQ
  * 定时调度
    * 单机定时调度
    * 分布式定时调度
  * RPC
    * Dubbo
    * Thrift
    * gRPC
  * 数据库中间件
    * Sharding Jdbc
  * 日志系统
    * 日志搜集
  * 配置中心
  * API 网关
* 网络
  * 协议
    * OSI 七层协议
    * TCP/IP
    * HTTP
    * HTTP2.0
    * HTTPS
  * 网络模型
    * select
    * epoll
      * ET & LT
    * Java NIO
    * kqueue
  * 连接和短连接
  * 三次握手，四次挥手
  * reset触发时机
  * TIME\_WAIT,CLOSE\_WAIT
  * shutdown和close区别
  * nagle算法和NO\_DELAY开关
  * SO\_LINGER选项
  * 大小端
  * TCP & UDP
  * 如果select返回可读，结果只读到0字节，什么情况\(对端关闭\)
  * 滑动窗口
  * 框架
  * 全双工 & 半双工
  * 零拷贝（Zero-copy）
  * 序列化
    * Hessian
    * Protobuf
  * [推荐书籍](net/recommand_book.md)
* 数据库
  * 基础理论
    * 数据库设计的三大范式
  * MySQL
    * 原理
    * InnoDB
    * 优化
    * 索引
      * 聚集索引, 非聚集索引
      * 复合索引
      * 自适应哈希索引
    * explain
  * NoSQL
    * MongoDB
    * Hbase
* 搜索引擎
  * 搜索引擎原理
  * Lucene
  * Elasticsearch
  * Solr
  * sphinx
* 性能
  * 性能优化方法论
  * 容量评估
  * CDN 网络
  * 连接池
  * 性能调优
* 大数据
  * 流式计算
    * Storm
    * Flink
    * Kafka Stream
    * 应用场景
  * Hadoop
    * HDFS
    * MapReduce
    * Yarn
  * Spark
* 机器学习
  * 深度学习
* 安全
  * web 安全
    * XSS
    * CSRF
    * SQL 注入
    * Hash Dos
    * 脚本注入
    * 漏洞扫描工具
    * 验证码
  * DDoS 防范
  * 用户隐私信息保护
  * 序列化漏洞
  * 加密解密
    * 对称加密
    * 哈希算法
    * 非对称加密
  * 服务器安全
  * 数据安全
    * 数据备份
  * 网络隔离
    * 内外网分离
    * 登录跳板机
  * 授权、认证
    * RBAC
    * OAuth2.0
    * 双因素认证（2FA）
    * 单点登录
* 常用开源框架
  * 开源协议
  * 日志框架
    * Log4j、Log4j2
    * Logback
  * ORM
  * 网络框架
    * libevent
    * muduo
  * Web 框架
    * Spring 家族
  * 工具框架
* 分布式设计
  * 扩展性设计
  * 稳定性 & 高可用
    * 硬件负载均衡
    * 软件负载均衡
    * 限流
    * 应用层容灾
    * 跨机房容灾
    * 容灾演练流程
    * 平滑启动
  * 数据库扩展
    * 读写分离模式
    * 分片模式
  * 服务治理
    * 服务注册与发现
    * 服务路由控制
  * 分布式一致
    * CAP 与 BASE 理论
    * 分布式锁
    * 分布式一致性算法
      * PAXOS
      * Zab
      * Raft
      * Gossip
      * 两阶段提交、多阶段提交
    * 幂等
    * 分布式一致方案
    * 分布式 Leader 节点选举
    * TCC
  * 分布式文件系统
  * 唯一ID 生成
    * 全局唯一ID
  * 一致性Hash算法
* 设计思想 & 开发模式
  * DDD
    * 命令查询职责分离
    * 贫血，充血模型
  * Actor 模式
  * 响应式编程
    * Reactor
    * RxJava
    * Vert.x
  * DODAF2.0
  * Serverless
  * Service Mesh
* 项目管理
  * 架构评审
  * 重构
  * 代码规范
  * 代码 Review
  * RUP
  * 看板管理
  * SCRUM
  * 敏捷开发
  * 极限编程（XP）
  * 结对编程
  * PDCA 循环质量管理
  * FMEA管理模式
* 通用业务术语
* 技术趋势
* [架构师素质](jia-gou-shi-su-zhi.md)
* [团队管理](tuan-dui-guan-li.md)
  * 招聘
* 资讯
  * 行业资讯
  * 公众号列表
  * 博客
    * 团队博客
    * 个人博客
  * 综合门户、社区
  * 问答、讨论类社区
  * 行业数据分析
  * 专项网站
  * 其他类
  * 推荐参考书
    * 在线电子书
    * 纸质书
      * 开发方面
      * 架构方面
      * 技术管理方面
      * 基础理论
      * 工具方面
      * 大数据方面
* 技术资源
  * 开源资源
  * 手册、文档、教程
  * 在线课堂
  * 会议、活动
  * 常用APP
  * 找工作
  * 工具
  * 文件服务
  * 综合云服务商
    * VPS



