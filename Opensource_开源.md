**目录：**

- [1）SQL数据库相关(ORM/DBA...)](#1sql%E6%95%B0%E6%8D%AE%E5%BA%93%E7%9B%B8%E5%85%B3ormdba)
  - [Java数据库开发](#java%E6%95%B0%E6%8D%AE%E5%BA%93%E5%BC%80%E5%8F%91)
    - [ORM](#orm)
      - [MyBatis](#mybatis)
      - [Stream API方式操作数据库](#stream-api%E6%96%B9%E5%BC%8F%E6%93%8D%E4%BD%9C%E6%95%B0%E6%8D%AE%E5%BA%93)
      - [其它ORM框架](#%E5%85%B6%E5%AE%83orm%E6%A1%86%E6%9E%B6)
    - [数据库连接池](#%E6%95%B0%E6%8D%AE%E5%BA%93%E8%BF%9E%E6%8E%A5%E6%B1%A0)
    - [数据库中间件](#%E6%95%B0%E6%8D%AE%E5%BA%93%E4%B8%AD%E9%97%B4%E4%BB%B6)
  - [数据库客户端](#%E6%95%B0%E6%8D%AE%E5%BA%93%E5%AE%A2%E6%88%B7%E7%AB%AF)
  - [数据库服务器](#%E6%95%B0%E6%8D%AE%E5%BA%93%E6%9C%8D%E5%8A%A1%E5%99%A8)
  - [数据生成(mock)](#%E6%95%B0%E6%8D%AE%E7%94%9F%E6%88%90mock)
  - [DBA](#dba)
    - [SQL自动审核](#sql%E8%87%AA%E5%8A%A8%E5%AE%A1%E6%A0%B8)
    - [数据库迁移/同步](#%E6%95%B0%E6%8D%AE%E5%BA%93%E8%BF%81%E7%A7%BB%E5%90%8C%E6%AD%A5)
- [2）NoSQL数据库相关(redis/mongoDB/ES...)](#2nosql%E6%95%B0%E6%8D%AE%E5%BA%93%E7%9B%B8%E5%85%B3redismongodbes)
  - [redis](#redis)
    - [客户端](#%E5%AE%A2%E6%88%B7%E7%AB%AF)
      - [Redis 操作工具包](#redis-%E6%93%8D%E4%BD%9C%E5%B7%A5%E5%85%B7%E5%8C%85)
      - [两级缓存框架](#%E4%B8%A4%E7%BA%A7%E7%BC%93%E5%AD%98%E6%A1%86%E6%9E%B6)
    - [服务器](#%E6%9C%8D%E5%8A%A1%E5%99%A8)
    - [运维/监控](#%E8%BF%90%E7%BB%B4%E7%9B%91%E6%8E%A7)
- [3）Java相关](#3java%E7%9B%B8%E5%85%B3)
  - [特别推荐](#%E7%89%B9%E5%88%AB%E6%8E%A8%E8%8D%90)
  - [awesome](#awesome)
  - [源码学习](#%E6%BA%90%E7%A0%81%E5%AD%A6%E4%B9%A0)
  - [学习案例](#%E5%AD%A6%E4%B9%A0%E6%A1%88%E4%BE%8B)
  - [开发手册](#%E5%BC%80%E5%8F%91%E6%89%8B%E5%86%8C)
  - [Lib](#lib)
  - [框架](#%E6%A1%86%E6%9E%B6)
    - [快速开发框架：](#%E5%BF%AB%E9%80%9F%E5%BC%80%E5%8F%91%E6%A1%86%E6%9E%B6)
    - [微服务](#%E5%BE%AE%E6%9C%8D%E5%8A%A1)
  - [tools-代码生成器](#tools-%E4%BB%A3%E7%A0%81%E7%94%9F%E6%88%90%E5%99%A8)
  - [tools-监控](#tools-%E7%9B%91%E6%8E%A7)
  - [JVM](#jvm)
  - [JVM语言](#jvm%E8%AF%AD%E8%A8%80)
    - [Groovy](#groovy)
    - [Kotlin](#kotlin)
    - [Cloujure](#cloujure)
- [主题研究](#%E4%B8%BB%E9%A2%98%E7%A0%94%E7%A9%B6)
  - [1）REST API](#1rest-api)
    - [客户端](#%E5%AE%A2%E6%88%B7%E7%AB%AF-1)
    - [Swagger](#swagger)
    - [测试框架HttpRunner](#%E6%B5%8B%E8%AF%95%E6%A1%86%E6%9E%B6httprunner)
  - [2）JSON](#2json)
    - [服务器开发](#%E6%9C%8D%E5%8A%A1%E5%99%A8%E5%BC%80%E5%8F%91)
    - [工具](#%E5%B7%A5%E5%85%B7)
- [运维相关](#%E8%BF%90%E7%BB%B4%E7%9B%B8%E5%85%B3)
    - [发布/部署](#%E5%8F%91%E5%B8%83%E9%83%A8%E7%BD%B2)
    - [docker部署](#docker%E9%83%A8%E7%BD%B2)
    - [配置中心](#%E9%85%8D%E7%BD%AE%E4%B8%AD%E5%BF%83)
- [大数据](#%E5%A4%A7%E6%95%B0%E6%8D%AE)
  - [查询](#%E6%9F%A5%E8%AF%A2)
  - [数据同步](#%E6%95%B0%E6%8D%AE%E5%90%8C%E6%AD%A5)
- [AI算法](#ai%E7%AE%97%E6%B3%95)
- [前端](#%E5%89%8D%E7%AB%AF)
- [中小团队技术选型](#%E4%B8%AD%E5%B0%8F%E5%9B%A2%E9%98%9F%E6%8A%80%E6%9C%AF%E9%80%89%E5%9E%8B)
- [开源网站](#%E5%BC%80%E6%BA%90%E7%BD%91%E7%AB%99)
- [22待整理](#22%E5%BE%85%E6%95%B4%E7%90%86)

===============================================




## 1）SQL数据库相关(ORM/DBA...)

### Java数据库开发



> 【list】----------数据库相关工具 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/java/categories/java-database.html
数据库相关工具 - **简化**数据库交互的Java相关工具


#### ORM

##### MyBatis


//
> ----------wuhao000/mybatis-xmlless-spring-starter: 使用这个项目，你基本可以不用写Mybatis的xml文件了，它可以自动推断sql（不是生成），既可以完成简单的增删改查，也可以支持复杂的连表查询
> https://github.com/wuhao000/mybatis-xmlless-spring-starter
如果你对于写mapper文件非常厌恶，那么这个项目非常适合你
``` 
【mybatis-xmlless-spring-starter】
----------使用这个项目，你基本可以不用写Mybatis的xml文件了 - Java开发社区 | CTOLib码库
https://www.ctolib.com/wuhao000-mybatis-xmlless-spring-starter.html

sql推断名称与方法名称隔离
在mapper方法上使用@ResolvedName注解，该注解的必选参数name将会代替方法名称作为推断sql的名称，这样可以让方法名称更具语义化

例如

@ResolvedName("findIdAndNameAndAge")
fun findSimpleInfoList(): List<User>

//
指定方法获取的属性集合
使用 @SelectedProperties注解

例如

@SelectedProperties(properties=["id", "name", "age"])
fun findSimpleInfoList(): List<User>

```


> ----------Mybatis 增强工具包 - 只做增强不做改变，简化CRUD操作 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/baomidou-mybatis-plus.html

> ----------Mybatis通用分页插件 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/pagehelper-Mybatis-PageHelper.html


> ----------MyBatisCodeHelper是Intellij下mybatis相关代码自动生成插件 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/MyBatisCodeHelper.html
Intellij下代码自动生成插件 支持生成mybatis的dao接口,mapper xml,和建表sql, 支持直接从接口方法名直接生成sql.

> ----------mybatis 自动生成代码web工具 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/generator-web.html
mybatis文件在线自动生成器-让机械无味的mybatis文件编写工作一去不返 随时随地 - 方便快捷


> ----------MyBatis-CMEU是基于javafx8开发的一款图形界面的Mybatis逆向工程; - Java开发社区 | CTOLib码库
> https://www.ctolib.com/shenzhenMirren-MyBatis-CMEU.html


> ----------perseus：基于 Mybatis + Spring 的读写分离方案 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/chengdedeng-perseus.html



> + ----------扩展mybatis-generator插件;高效率分页查询,自动添加swagger2注解到实体类 - Java开发社区 | CTOLib码库
>https://www.ctolib.com/MisterChangRay-mybatis-generator-plugins.html
```
1. 自动添加swagger2注解到实体类
自动为entity类生成swagger2文档注解，注解内容为数据库comment内容

        <!-- 自动为entity生成swagger2文档-->
        <plugin type="mybatis.generator.plugins.GeneratorSwagger2Doc">
          <property name="apiModelAnnotationPackage" value="io.swagger.annotations.ApiModel" />
          <property name="apiModelPropertyAnnotationPackage" value="io.swagger.annotations.ApiModelProperty" />
        </plugin>
```



##### Stream API方式操作数据库

> ----------Speedment：一个数据库访问库它利用了Java 8 Stream API进行查询 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/speedment.html
Speedment：一个数据库访问库它利用了Java 8 Stream API进行查询


> ----------【Anima】🍶 像 Stream API 那样操作数据库 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/biezhi-anima.html

```
Query
long count = select().from(User.class).count();
// SELECT COUNT(*) FROM users

long count = select().from(User.class).where("age > ?", 15).isNotNull("user_name").count();
// SELECT COUNT(*) FROM users WHERE age > ? AND user_name IS NOT NULL

User user = select().from(User.class).byId(2);
// SELECT * FROM users WHERE id = ?

List<User> users = select().from(User.class).byIds(1, 2, 3);
// SELECT * FROM users WHERE id IN (?, ?, ?)

String name = select().bySQL(String.class, "select user_name from users limit 1").one();

List<String> names = select().bySQL(String.class, "select user_name from users limit ?", 3);

List<User> users = select().from(User.class).all();
// SELECT * FROM users

List<User> users = select().from(User.class).like("user_name", "%o%").all();
// SELECT * FROM users WHERE user_name LIKE ?

```



##### 其它ORM框架

> 【list】----------ORM框架 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/categories/java-orm-pg-2.html


> ----------MyBatis：支持定制化 SQL、存储过程以及高级映射的优秀的持久层框架 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/mybatis-3.html

> ----------jOOQ：构建类型安全的SQL查询 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/jOOQ.html
jOOQ从数据库产生Java代码，并允许您通过其流畅API构建类型安全的SQL查询。




#### 数据库连接池

> ----------Druid是Java语言中最好的数据库连接池。Druid能够提供强大的监控和扩展功能。 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/druid.html




#### 数据库中间件


> ----------| MYCAT官方网站—中国第一开源分布式数据库中间件
> http://www.mycat.io/


> ----------Ctrip DAL是携程框架部开发的数据库访问框架 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/dal.html
Ctrip DAL是携程框架部开发的数据库访问框架，支持代码生成和水平扩展。其由携程技术中心框架部DAL团队开发，历经3年不断打磨，并在长期的实际使用中基于大量的用户反馈不断优化。



> ----------分表分库的新思路——服务层Sharding框架 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/QNJR-GROUP-sharding-method.html
分表分库的新思路——服务层Sharding框架，全SQL、全数据库兼容，ACID特性与原生数据库一致，能实现RR级别读写分离，无SQL解析性能更高







### 数据库客户端

> ----------mysq数据库管理工具navicat基本使用方法 - 师者乐享 - 博客园
> https://www.cnblogs.com/neuedu/p/5876874.html
navicat是mysql数据库的客户端查询管理工具



> ----------DataGrip: 一种工具支持多种数据库
> https://www.jetbrains.com/zh/datagrip/specials/datagrip/datagrip.html?utm_source=baidu&utm_medium=cpc&utm_campaign=cn-bai-br-datagrip-ex-pc&utm_content=datagrip-pure&utm_term=datagrip&gclid=CO6389SJiuACFcd2vAodj1gC_A&gclsrc=ds



> ----------DBeaver免费通用数据库管理器和SQL客户端 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/serge-rider-dbeaver.html
免费的多平台数据库工具，适用于开发人员，SQL程序员，数据库管理员和分析人员。 支持任何具有JDBC驱动程序的数据库（这主要表示ANY数据库）。

> DBeaver 是一个通用的数据库管理工具和 SQL 客户端，
http://blog.51cto.com/12042068/2115077


### 数据库服务器

> ----------SQLiteToExcel：一个轻量级库用于将SQLite数据库转换为Excel - Java开发社区 | CTOLib码库
> https://www.ctolib.com/SQLite2XL.html

> ----------H2：小型SQL数据库，以可以作为内存数据库使用著称 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/ar-454.html
H2采用Java开发的免费SQL数据库


> Realm是一个用来**替代sqlite**的解决方案，它比sqlite更轻量，同时速度更快，而且使用起来很简单顺手，还跨平台，目前已支持Java，Objective C，Swift，React-Native，Xamarin这五种语言。




### 数据生成(mock)

> ----------基于多数据库的数据生成器 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/ysc-data-generator.html
数据生成器 -- 如果你在从事大数据BI的工作，想对比一下MySQL、GreenPlum、Elasticsearch、Hive、Presto、Impala、Drill、HAWQ、Druid、Pinot、Kylin等不同实现方案之间的表现，那你就需要一份标准的数据进行测试，这个开源项目就是为了生成这样的标准数据。




### DBA



#### SQL自动审核

> ----------cookieY/Yearning: Mysql web端sql审核平台
> https://github.com/cookieY/Yearning
Mysql web端sql审核平台 http://yearning.io/
> 
> SQL审核
流程化工单
SQL语句检测与执行
SQL回滚
历史审核记录
> 
> 推送
E-mail工单推送
钉钉webhook机器人工单推送
> 
> //用户权限及管理
拼图式权限划分
组合式权限组
支持限制邮箱后缀名的有限注册功能
>
> ![enter image description here](http://yearning.io/img/per.png)


> 【Inception-SQL自动审核工具】
> 
> ----------中小团队快速构建SQL自动审核系统：：运维咖啡吧
> https://mp.weixin.qq.com/s?__biz=MzU5MDY1MzcyOQ==&mid=2247483715&idx=1&sn=0afbe6ae23c9b052b70d11cf441775ca&scene=21#wechat_redirect
SQL审核与执行，作为DBA日常工作中相当重要的一环，一直以来我们都是通过人工的方式来处理，效率低且质量没办法保证。为了规范操作，提高效率，我们决定引入目前市面上非常流行的SQL自动审核工具Inception。
>
>github：https://github.com/mysql-inception/inception
官方文档：http://mysql-inception.github.io/inception-document
Inception是一个开源的Mysql自动化工具，具有SQL审核、执行、回滚等实用的功能，由国内大神基于mysql源码开发，可以很明确的，详细的，准确的审核Mysql的SQL语句，工作模式与Mysql完全相同，可以直接使用mysql客户端来连接。但遗憾的是2年前已停止更新，不过兼容大部分的mysql版本，仍然是开源SQL审核工具的翘楚。



> 【Inception-SQL自动审核工具】
> 
> ----------中小团队快速构建SQL自动审核系统：：运维咖啡吧
> https://mp.weixin.qq.com/s?__biz=MzU5MDY1MzcyOQ==&mid=2247483715&idx=1&sn=0afbe6ae23c9b052b70d11cf441775ca&scene=21#wechat_redirect
SQL审核与执行，作为DBA日常工作中相当重要的一环，一直以来我们都是通过人工的方式来处理，效率低且质量没办法保证。为了规范操作，提高效率，我们决定引入目前市面上非常流行的SQL自动审核工具Inception。
>
>github：https://github.com/mysql-inception/inception
官方文档：http://mysql-inception.github.io/inception-document
Inception是一个开源的Mysql自动化工具，具有SQL审核、执行、回滚等实用的功能，由国内大神基于mysql源码开发，可以很明确的，详细的，准确的审核Mysql的SQL语句，工作模式与Mysql完全相同，可以直接使用mysql客户端来连接。但遗憾的是2年前已停止更新，不过兼容大部分的mysql版本，仍然是开源SQL审核工具的翘楚。


> Data Transfer Project 旨在创建一个开源的服务到服务数据可移植平台，以便其网站用户和其他人可以轻松将数据从一个平台迁移到另一个平台。它提供了一个通用框架和生态系统，可接受服务提供商的贡献，以实现数据无缝传输到服务之间。
https://github.com/google/data-transfer-project





#### 数据库迁移/同步

> ----------Flyway：简单的Java数据库迁移工具 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/flyway.html


>【canal：跨机房同步】
> 
> ----------阿里巴巴mysql数据库binlog的增量订阅&消费组件 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/canal.html
早期，阿里巴巴B2B公司因为存在杭州和美国双机房部署，存在跨机房同步的业务需求。不过早期的数据库同步业务，主要是基于trigger的方式获取增量变更，不过从2010年开始，阿里系公司开始逐步的尝试基于数据库的日志解析，获取增量变更进行同步，由此衍生出了增量订阅&消费的业务，从此开启了一段新纪元。


> ----------DataLink是一个满足各种异构数据源之间的实时增量同步，分布式、可扩展的数据交换平台 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/ucarGroup-DataLink.html
> DataLink是这样一个产品：
> 
> 满足各种异构数据源之间的实时增量同步
平台提供统一的基础设施（高可用、动态负载、同步任务管理、插件管理、监控报警、公用业务组件等等），让设计人员专注于同步插件开发，一次投入，长久受益
> 
> 吸收、整合业内经验，在架构模型、设计方法论、功能特性、可运维、易用性上进行全面的升级，在前瞻性和扩展性上下足功夫，满足未来5-10年内的各种同步需求
> 
> DataLink开发时间从2016年12月开始，第一版于2017年5月份上线，在神州优车集团服役到现在，基本上满足了公司所有业务线的同步需求。此次外部开源版本为去除内部依赖后的版本。
> 
> 目前同步规模：
日均数据同步量800G+
涉及272个数据库实例之间的3208个同步映射
60台Worker+2台Manager机器的集群规模







## 2）NoSQL数据库相关(redis/mongoDB/ES...)

### redis


#### 客户端

##### Redis 操作工具包

> ----------jedis：Redis的Java客户端 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/jedis.html

> ----------lettuce - 高级Java Redis客户端，用于线程安全同步，异步和reactive用法 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/lettuce-io-lettuce-core.html

> 【Spring Data Redis】
> 
> ----------它提供了 Spring 应用对 Redis 的简单配置和访问 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/spring-data-redis.html
Spring Data Redis, 是 Spring Data 家族的子项目。它提供了 Spring 应用对 Redis 的简单配置和访问。低级和高级的抽象用于存储，使用户无需考虑考虑基础。

> ----------jedipus 是一个 Redis 3.2 + Java 8 客户端和命令行执行器 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/jedipus.html
jedipus 是一个 Redis 3.2 + Java 8 客户端，用于管理客户端对象池和命令执行。 特点： 1.可使用Consumer<RedisClient> 和Function<RedisClient, R>执行lambda 2.灵活的泛型和初始返回类型会匹配Redis动态的返回类型。

> ----------Redis 操作工具包分装。单点、哨兵、cluster均支持。简单配置即可使用 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/sudo168-redis-helper.html
redisHelper.cmd().set("name", "lisi");


##### 两级缓存框架

> ----------J2Cache: Java **两级缓存框架**，可以让应用支持两级缓存框架 ehcache(Caffeine) + redis 。避免完全使用独立缓存系统所带来的网络IO开销问题
> https://gitee.com/ld/J2Cache
J2Cache 是 OSChina 目前正在使用的两级缓存框架（要求至少 Java 8）。第一级缓存使用内存(同时支持 Ehcache 2.x、Ehcache 3.x 和 Caffeine)，第二级缓存使用 Redis(推荐)/Memcached 。 由于大量的缓存读取会导致 L2 的网络成为整个系统的瓶颈，因此 L1 的目标是降低对 L2 的读取次数。 该缓存框架主要用于集群环境中。单机也可使用，用于避免应用重启导致的缓存冷启动后对后端业务的冲击。




#### 服务器
> ----------**Redisson** - 构建在Redis服务器之上的分布式可扩展Java数据结构 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/redisson.html

> ----------**Redis集群**方案之使用豌豆荚Codis搭建（待实践） - EasonJim - 博客园
> https://www.cnblogs.com/EasonJim/p/7630405.html




#### 运维/监控

> ----------CacheCloud:搜狐视频的CacheCloud提供一个Redis云管理平台 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/cachecloud.html
CacheCloud提供一个Redis云管理平台：实现多种类型(Redis Standalone、Redis Sentinel、Redis Cluster)自动部署、解决Redis实例碎片化现象、提供完善统计、监控、运维功能、减少运维成本和误操作，提高机器的利用率，提供灵活的伸缩性，提供方便的接入客户端。
> 3. 监控、统计和管理不完善
       一些开源的Redis监控和管理工具，例如：RedisLive(Python)、Redis Commander(Node.js)，Redmon(Ruby)无论从功能的全面性(例如配置管理，支持Redis-Cluster等等)、扩展性很难满足需求。
>
>4. 运维成本
       Redis的使用者需要维护各自的Redis，但是用户可能更加善于使用Redis实现各种功能，但是没有足够的精力和经验维护Redis。Redis的开发人员如同使用MySQL一样，不需要运维Mysql服务器，同样使用Redis服务，不要自己运维Redis，Redis由一些在Redis运维方面更有经验的人来维护（保证高可用，高扩展性），使得开发者更加关注于Redis使用本身。

> ----------基于SpringBoot开发的redis缓存数据图形化管理工具 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/xuebus-redis-admin.html
一个简单好用的redis缓存图形化管理工具，包含redis的5种数据类型的CRUD操作; 由于该系统是在大名鼎鼎的JeeSite基础之上开发的，所有保留了原系统的用户/角色/权限/菜单等模块.





==================================================

## 3）Java相关



### 特别推荐

> 特别推荐：apiJSON，EOVA，CBoard

> 分布式开源程序：mall，zheng



### awesome

> 【JavaGuide: Java学习+面试指南】
> 
> ----------Snailclimb/JavaGuide: 【Java学习+面试指南】 一份涵盖大部分Java程序员所需要掌握的核心知识。
> https://github.com/Snailclimb/JavaGuide
【Java学习+面试指南】 一份涵盖大部分Java程序员所需要掌握的核心知识。 https://github.com/Snailclimb/JavaGuide


> 【awesome-java】
> 
> ----------akullpp/awesome-java: A curated list of awesome frameworks, libraries and software for the Java programming language.
> https://github.com/akullpp/awesome-java
作者将JAVA中那些最常用的第三方库按照分类整理成了一个列表。包含Ancients(古老，但常用的)，Bean Mapping，Build，Bytecode Manipulation，Code Analysis，Command-line Argument Parsers，Configuration，Continuous Integration，CSV，Database等等，简直是一本jiava第三方库大全，如果你对项目中应该使用哪一个库不确定，或希望选择几个库来做比较，都可以到awesome-java上进行参考。



+ [weiweifan/Big-Data-Resources](https://github.com/weiweifan/Big-Data-Resources): 大数据/数据挖掘/推荐系统/机器学习相关资源
+ [onurakpolat/awesome-bigdata](https://github.com/onurakpolat/awesome-bigdata): A curated list of awesome big data frameworks, ressources and other awesomeness.
+ [bulutyazilim/awesome-datascience](https://github.com/bulutyazilim/awesome-datascience)：An awesome Data Science repository to learn and apply for real world problems.
+ [MaximAbramchuck/awesome-interview-questions: A curated awesome list of lists of interview questions. Feel free to contribute!](https://github.com/MaximAbramchuck/awesome-interview-questions)

+ [Search · topic:awesome](https://github.com/search?q=topic%3Aawesome&type=Repositories)
+ [sindresorhus/awesome](https://github.com/sindresorhus/awesome): Curated list of awesome lists(6w star+)
+ [lyfeyaj/awesome-resources](https://github.com/lyfeyaj/awesome-resources): Awesome resources for coding and learning: open source projects, websites, books e.g.


### 源码学习

> + [芋道源码 —— 纯源码解析博客(愿半生编码，如一生老友！)](http://www.iocoder.cn/)




### 学习案例

https://github.com/JeffLi1993/springboot-learning-example
spring boot 实践学习案例，是 spring boot 初学者及核心技术巩固的最佳实践。

> 【99-Problems】
> 
> ----------shekhargulati/99-problems: This is an adaptation of the Ninety-Nine Prolog Problems written by Werner Hett.
> https://github.com/shekhargulati/99-problems
99-Problems是一个很有意思的GitHub项目，它对三种不同的语言Java 8,Scala和Haskell分别提出了99个问题，让你通过使用特定语言编程来提供一个最优的解决方案。
这些问题分为不同的难度等级，用*表示，一个星号表示在15分钟内解决，2个星号可能需要30-69分钟，而最难的3个星号，则需要更长时间（90分钟左右），如果你能在限定的时间内使用JAVA8的特性解决所有的问题，那说明你对JAVA8的掌握程度已经非常牢固了。如果你没办法解决所有问题也没关系，你可以查看作者提供的代码示例，这也是你学习JAVA8很好的途径。

### 开发手册

> 阿里开发规范

> 唯品会Java开发手册，结合唯品会的内部经验，参考《阿里巴巴Java开发手册》《Clean Code》、《Effective Java》等重磅资料进行了大幅定制，包含核心基础类库VJKit ，问题排查工具VJMap 和 VJTop 三部分。
https://github.com/vipshop/vjtools


### Lib

> ----------GitHub 上那些值得一试的 Java 开源库 - arthur.dy.lee的专栏 - CSDN博客
> https://blog.csdn.net/paincupid/article/details/51923284
Strmen-java是一个字符串处理工具，你可以通过maven将它引入到项目中。除了Java本身的字符串处理方式外，我们还可以使用Apache Common Langs里的StringUtils来简化String的操作。但以上两种方式对于我们日常编程中最容易碰到的字符串处理来说，仍然显得有些不足。Strmen-java为我们提供了一个非常完整且强大的解决方案，使用它可以解决几乎所有字符串处理场景。


> NullAway 是 Uber 开源的一款帮助你清除 Java 代码中的 NullPointerException（NPE）的工具，快速且实用。NullAway 类似于 Kotlin 和 Swift 语言中的基于类型的可空性检查，能显着提高开发人员的生产力，同时也满足高要求的安全检查需求。
https://github.com/uber/NullAway


### 框架



#### 快速开发框架：

> JFinal，

> nutz，


#### 微服务

> Nacos是一个易于使用的平台，旨在实现动态服务发现，配置和服务管理。它可以帮助开发者轻松构建云本机应用程序和微服务平台。
https://github.com/alibaba/nacos



### tools-代码生成器

> ----------Spring-generator是基于javafx8开发的图形界面Spring代码生成器 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/EliMirren-Spring-generator.html





### tools-监控

> + MBean

> 【Automon-JAVA监控工具】
> 
> ----------stevensouza/automon: Automon combines the power of AOP (AspectJ) with monitoring or logging tools you already use to declaratively monitor your Java code, the JDK, and 3rd party libraries.
> https://github.com/stevensouza/automon
Automon是一个非常灵活的JAVA监控工具，它结合了AOP(AspectJ)以及JDK和其他依赖库的功能特性，以声明方式去监控你的Java代码。它可以与JAMon，JavaSimon，Yammer Metrics，StatsD和像 perf4j,log4j,sl4j这样的logging库结合使用。
Automon最常被用于跟踪**Java方法的调用时长，异常次数**等信息，并在你选择的工具中显示监控结果。它并不自己进行任何监控动作，但却很好地扮演了“我应该监控什么”以及“我如何进行监控”这两者之间中间人的角色。而且它的安装也非常简单，只需要简单进行配置便可使用。


> 【Gumshoe - Java程序检测】
> 
> ----------GitHub 上那些值得一试的 Java 开源库 - arthur.dy.lee的专栏 - CSDN博客
> https://blog.csdn.net/paincupid/article/details/51923284
Gumshoe - Java程序检测
Gumshoe是一个JAVA程序检测工具，它能帮助你跟踪程序的负载和性能。它能通过度量TCP,UDP,CPU使用等信息，帮助你分析出资源的使用情况 ，同时它也提供了Java程序中调用栈的分析功能，比如提供某个方法调用的次数，频度等信息。




> 【LeakCanary - 内存泄漏监控】
> 
> ----------GitHub 上那些值得一试的 Java 开源库 - arthur.dy.lee的专栏 - CSDN博客
> https://blog.csdn.net/paincupid/article/details/51923284
LeakCanary - 内存泄漏监控
内存泄漏一直是令Java程序员苦恼的问题，因为在你开发阶段很难察觉内存泄漏问题，而一旦到了生产环境，则可能因为它而造成严重的后果。LeakCanary是一个内存泄漏检查工具，只需要像下面这样简单加入LeakCanary，它便能全程监控你的应用，并在出现内存泄漏时给你发出警告。LeakCanary同时支持Android和Java，下面是在Android应用中使用的例子。




### JVM


> 【JarsLink (原名 Titan ) -基于 Java 的**模块化**开发框架】
> 
>https://github.com/alibaba/jarslink Star 21058
JarsLink (原名 Titan ) 是一个基于 Java 的模块化开发框架，它提供在运行时动态加载模块（一个 Jar 包）、卸载模块和模块间调用的 API。目前蚂蚁金服微贷事业部几个系统和几十个模块已经使用JarsLink框架。

> 【Swiss Java Knife(**SJK**) - JAVA工具集】
> 
> ----------aragozin/jvm-tools: Small set of tools for JVM troublshooting, monitoring and profiling.
> https://github.com/aragozin/jvm-tools
SJK（Java瑞士军刀）是一个用于JVM监控、排错以及调优的工具集。它是一个命令行工具，但使用起来非常方便，你可以用它来**查询JVM中线程的CPU使用，GC实时信息**，以及基本调优选项。也可以结合MBean以JSON格式导出所有你需要的信息。


> bytecodeviewer是一款简单易用功能强大的反编译软件。
> 它是一款基于图形界面的Java反编译器，Java字节码编辑器，APK编辑器，Dex编辑器，APK反编译器，DEX反编译器。不仅如此，它还是一款Hex查看器，代码搜索器和代码调试器。除此之外，它还具备Smali和Baksmali等汇编器的相关功能。


> Graal 是一个用 Java 编写的新的 JVM 即时编译器，集成到 HotSpot 虚拟机，侧重性能和语言互操作性。Graal 为 Java 代码提供性能优势，这得益于方法内联、流转对象分配和推理执行等新技术，从而可以实现高性能的脚本语言引擎。
https://github.com/oracle/graal



### JVM语言

> ----------Groovy，Clojure和Kotlin都是基于jvm的语言，那他们在实际项目中的运用场景有什么区别？ - 知乎
> https://www.zhihu.com/question/29818569?sort=created

#### Groovy


#### Kotlin

#### Cloujure

> ----------Toucan 一个优雅的高级Clojure库，用于定义应用程序模型并从DB中检索它们 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/toucan.html






===================================================



## 主题研究

### 1）REST API

#### 客户端

> Postman

> VSCode插件：REST Client

#### Swagger


> ----------让接口测试成为合格的桥梁——本地搭建 Swagger-UI 环境搭建 · TesterHome
> https://testerhome.com/topics/8168
思路就是借鉴服务端开发使用的Swagger UI，定制化我们自己需求的既可以展示Jmeter执行结果，又能让开发在线调试的页面。
>
>最后在Swagger UI界面可以查看这里的json文件展示的样式：
![](https://testerhome.com/uploads/photo/2017/58b183395d7b395df3adae77d379f893.png!large)



> + ----------扩展mybatis-generator插件;高效率分页查询,自动添加swagger2注解到实体类 - Java开发社区 | CTOLib码库
>https://www.ctolib.com/MisterChangRay-mybatis-generator-plugins.html
```
1. 自动添加swagger2注解到实体类
自动为entity类生成swagger2文档注解，注解内容为数据库comment内容

        <!-- 自动为entity生成swagger2文档-->
        <plugin type="mybatis.generator.plugins.GeneratorSwagger2Doc">
          <property name="apiModelAnnotationPackage" value="io.swagger.annotations.ApiModel" />
          <property name="apiModelPropertyAnnotationPackage" value="io.swagger.annotations.ApiModelProperty" />
        </plugin>
```




#### 测试框架HttpRunner


### 2）JSON

#### 服务器开发

> apiJSON

> GraphQL

> 纯JSON框架

#### 工具

> IDEA插件：JSON转javaBean

> json在线格式化：http://json.cn



## 运维相关

#### 发布/部署

> ----------walle 2.0 瓦力 | walle 瓦力 - 部署系统
> http://walle-web.io/docs/
walle 让用户代码发布终于可以不只能选择 jenkins！支持各种web代码发布，php、java、python、go等代码的发布、回滚可以通过web来一键完成。walle 一个可自由配置项目，更人性化，高颜值，支持git、多用户、多语言、多项目、多环境同时部署的开源上线部署系统。




#### docker部署

> ----------从Jenkins迁移到Jenkins X：一场持续交付之旅：：高效开发运维
> https://mp.weixin.qq.com/s/yq7cBZJiTd_TlafNuX17WA
Jenkins X 是一个高度集成化的 CI/CD 平台，基于 Jenkins 和 Kubernetes 实现，旨在解决微服务体系架构下的云原生应用的持续交付的问题




> ----------探秘varian：优雅的发布部署程序：：运维咖啡吧
> https://mp.weixin.qq.com/s?__biz=MzU5MDY1MzcyOQ==&mid=2247483730&idx=1&sn=435c10f8c1ec6938f80b0e7d814dfdcd&scene=21#wechat_redirect
varian是我们基于Python3编写的一套部署程序，处在整个部署系统的中心，与CMDB、Jenkins、SVN/Git、镜像仓库Harbor、Kubernetes API、通知系统等都有交互，负责将源代码经过一系列的处理后打包成Docker镜像，并发布到各个环境，然后通知相关人员。简化后的varian架构如下：


> ----------Docker环境的持续部署优化实践::运维咖啡吧
> https://mp.weixin.qq.com/s/xnBehfSlZ3J02xb0GFuGDw
背景介绍
那年公司快速成长，频繁上线新项目，每上线一个项目，就需要新申请一批机器，初始化，部署依赖的服务环境，一个脚本行天下
那年项目发展如火如荼，A项目流量暴增马上给A扩机器，B项目上线新功能又要扩容B，上线新项目没资源了，就先下线处于流量低峰的C项目主机
每天日夜加班，疲于奔命
那年得知了Docker能拯救我于水火，遂决定为了荣誉（发际线）而战。
为了快速落地以及尽量降低引入Docker对整个CICD流程的影响，用最小的改动把Docker加入到了我们上线的流程中，流程变化参考下图
![](https://mmbiz.qpic.cn/mmbiz_png/s0ib4cHvBPB92uq5ibUINQYLbx46O7j6RkVO4I3VtTPqnmBeOM4T9CDz4iaT9GGBvF9hKTNicllfxR3ibXlZibhXA4aA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
>
>//
多环境下配置文件的处理
我们采用了项目代码打包进镜像的镜像管理方案，开发、测试、预发布、生产环境配置文件都不同，所以即便是同一个项目不同的环境都会单独走一遍部署发布流程打包镜像，把不同环境的配置打包到不同的镜像中，这个操作太过繁琐且没有必要，还大大增加了我们的上线时间
>
> 用过k8s的都知道，k8s中有专门管理配置文件的ConfigMap，每个容器可以定义要挂载的配置，在容器启动时自动挂载，以解决打包一次镜像不同环境都能使用的问题，对于没有用到k8s的要如何处理呢？配置中心还是必不可少的，之前一篇文章《中小团队落地配置中心详解》有详细的介绍我们配置中心的方案
>
> 我们处理不同配置的整体思路是，在Docker启动时传入两个环境变量ENVT和PROJ，这两个环境变量用来定义这个容器是属于哪个项目的哪个环境，Docker的启动脚本拿到这两个环境变量后利用confd服务自动去配置中心获取对应的配置，然后更新到本地对应的位置，这样就不需要把配置文件打包进镜像了
> 
> 做到了一次镜像打包多环境共用，上线时也无需再走一次编译打包的流程，只需更新镜像重启容器即可，效率明显提高
>
>//
> 写在最后
**缺少编排的容器是没有灵魂的**，继续推进编排工具的运用将会是2019年工作的重点
实际上我们在Docker改造稳定后，内网开发测试环境部署了一套k8s集群用到现在已经一年多的时间比较稳定
线上用到了多云环境，一部分线上项目已经使用了基于k8s的容器编排，当然还有一部分是我上边介绍的纯Docker环境


#### 配置中心

> ----------中小团队落地配置中心详解 - 云+社区 - 腾讯云
> https://cloud.tencent.com/developer/article/1380942
配置中心选型
选型的原则：**简单，易落地**，不挑平台，不挑语言，**尽量少的依赖**。
对比了Disconf、Apollo等方案，最终选择了**Etcd+Confd**的方案，基本符合上边的原则，且Etcd我们在部署Kubernetes的时候已经有过使用，算是轻车熟路。
> 
> //配置中心架构图:
![配置中心架构图](https://ask.qcloudimg.com/http-save/yehe-2933803/vctroqw9cp.png?imageView2/2/w/1620)




=======================================================

## 大数据

### 查询

> ----------Quicksql：360 开源的更简单，更安全，更快速的跨数据源统一 SQL 查询引擎 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/Qihoo360-Quicksql.html



> 【Tablesaw - “大数据”】
> 
> ----------GitHub 上那些值得一试的 Java 开源库 - arthur.dy.lee的专栏 - CSDN博客
> https://blog.csdn.net/paincupid/article/details/51923284
Tablesaw - “大数据”
谈到大数据，我们想到的总是Hodoop加上集群部署，但有没有一种更小巧的方式，能让我们在单机上方便地实现大数据的那些功能呢？Tablesaw给我们提供了一种基于内存的高性能大数据解决方案。你可以使用它的API方便地从RDBMS或是CSV中导入数据，然后利用Tablesaw提供的接口对数据进行排序、筛选、分组、map/reduce等操作。
根据文档给出的说明，你将可以在22秒内将500,000,000行（每行4个字段）的数据文件加载到10G的内存中。而查询速度更是达到仅需1-2ms。

> ----------Presto：针对大数据的分布式SQL查询引擎 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/presto.html




### 数据同步

> ----------DataX 是阿里巴巴集团内被广泛使用的离线数据同步工具/平台 - Java开发社区 | CTOLib码库
> https://www.ctolib.com/DataX.html
DataX 是阿里巴巴集团内被广泛使用的离线数据同步工具/平台，实现包括 MySQL、Oracle、HDFS、Hive、OceanBase、HBase、OTS、ODPS 等各种异构数据源之间高效的数据同步功能。





==========================================================

## AI算法
。。https://github.com/hankcs/HanLP Star 6273
HanLP是由一系列模型与算法组成的Java工具包，目标是普及自然语言处理在生产环境中的应用。HanLP具备功能完善、性能高效、架构清晰、语料时新、可自定义的特点。在提供丰富功能的同时，HanLP内部模块坚持低耦合、模型坚持惰性加载、服务坚持静态提供、词典坚持明文发布，使用非常方便，同时自带一些语料处理工具，帮助用户训练自己的模型。






=============================================

## 前端

> SmartTable 是一套数据源使用 Ajax 获取数据，并展现成表格与图像的形式，并且支持下载（思路源于talkingdata）的智能表格。开源引入：Bootstrap 3.0，Bootstrap respond (IE解决方案)，Jquery 11.02，dataTables，echarts，table2CSV


=======================================================



## 中小团队技术选型

> ----------小团队构建大网站：中小研发团队架构实践_百度百科
> https://baike.baidu.com/item/%E5%B0%8F%E5%9B%A2%E9%98%9F%E6%9E%84%E5%BB%BA%E5%A4%A7%E7%BD%91%E7%AB%99%EF%BC%9A%E4%B8%AD%E5%B0%8F%E7%A0%94%E5%8F%91%E5%9B%A2%E9%98%9F%E6%9E%B6%E6%9E%84%E5%AE%9E%E8%B7%B5/23232448?fr=aladdin
**《小团队构建大网站：中小研发团队架构实践》**结合作者十几年的工作经验，总结了一套系统又详细、且可落地的中小研发团队架构实践指导方案。



> ----------中小型研发团队架构实践三要点 - 坤少_jkson - CSDN博客
> https://blog.csdn.net/jiangzhexi/article/details/78311302
中小型研发团队很多，而社区在中小型研发团队架构实践方面的探讨却很少。中小型研发团队特别是 50 至 200 人的研发团队，在早期的**业务探索**阶段，更多关注**业务逻辑**，快速迭代以验证商业模式，很少去关注技术架构。这时如果继续按照原有的架构及研发模式，会出现大量的问题，再也无法玩下去了。能不能有一套可直接落地、基于开源、成本低，可快速搭建的中间件及架构升级方案呢？


===============================================


## 开源网站

> ----------CTOLib码库
> https://www.ctolib.com/


## 22待整理

==============================================

//整理到opensource分类，2019-1-25 13:58:19
。。https://github.com/cachecats/coderiver


coderiver 中文名 河码，是一个为程序员和设计师提供项目协作的平台，类似程序员客栈，但主要目的是方便各细分领域人才之间技术交流，共同成长，多人协作完成项目。暂不涉及金钱交易。


。。https://github.com/kdn251/interviews Star 30614


Java工程师面试指南，里面涵盖几乎所有软件工程师面试时会碰到的问题以及答案。


。。Spring Cloud Alibaba 致力于提供微服务开发的一站式解决方案。此项目包含开发分布式应用微服务的必需组件，方便开发者通过 Spring Cloud 编程模型轻松使用这些组件来开发分布式应用服务。通过它，只需要添加一些注解和少量配置，就可以将 Spring Cloud 应用接入阿里微服务解决方案，通过阿里中间件来迅速搭建分布式应用系统。
。。一个小商城。litemall = Spring Boot后端 + Vue管理员前端 + 微信小程序用户前端，由于没有上线，只能在微信开发工具中测试运行
。。https://github.com/crossoverJie/JCSprout Star 17084
这是一个还处于萌芽阶段的 Java 核心知识库。分为常用集合、Java多线程、JVM、分布式相关、常用框架等内容
。。https://github.com/Snailclimb/JavaGuide Star 14726
这是一份Java学习指南，涵盖大部分Java程序员所需要掌握的核心知识

。。https://github.com/iluwatar/java-design-patterns Star 42081
Design patterns 是程序员在设计应用程序或系统时可用来解决常见问题的最佳实践手册。
。。https://github.com/macrozheng/mall Star 3249
mall项目是一套电商系统，包括前台商城系统及后台管理系统，基于SpringBoot+MyBatis实现。 
。。https://github.com/b3log/symphony Star 8931
一款用 Java 实现的现代化社区（论坛/BBS/社交网络/博客）平台。分为社区版和商业版
。。https://github.com/eugenp/tutorials Star 10447
该项目是一系列小而专注的教程，每个教程都涵盖一个明确的开发领域。大多数教程项目都专注于Spring Framework（和Spring Security）。以下技术是重点：core Java，Jackson，HttpClient，Guava。
。。Arthas旨在帮助开发人员解决Java应用程序的生产问题，无需修改代码或重新启动服务器。有了Arthas，你就可以在不重新启动JVM或需要额外的代码更改的情况下实时地对问题进行故障排除。


==============================================
