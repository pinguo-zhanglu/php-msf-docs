# PHP-MSF开发手册

PHP微服务框架开发手册，即Micro Service Framework For PHP Develop Manual，PHP微服务框架即[“Micro Service Framework For PHP”](https://github.com/pinguo/php-msf)，是Camera360社区服务器端团队基于Swoole自主研发的现代化的PHP服务框架，简称msf或者php-msf，它的核心设计思想是采用协程、异步、并行的创新技术手段提高系统的单机吞吐能力，降低整体服务器成本。

本手册从介绍异步、并行、协程等基础概念出发，再到[PHP-MSF](https://github.com/pinguo/php-msf)框架如何使用，其中也介绍了部分内部实现的原理，简单易上手。通过学习本手册，再结合我们的demo示例项目，就能够[PHP-MSF](https://github.com/pinguo/php-msf)构建大规模高性能的微服务化分布式系统。

```bash
      _______                               ____
________  / /_  ____        ____ ___  _____/ __/
___/ __ \/ __ \/ __ \______/ __ `__ \/ ___/ /_
__/ /_/ / / / / /_/ /_____/ / / / / (__  ) __/
_/ .___/_/ /_/ .___/     /_/ /_/ /_/____/_/
/_/         /_/         Camera360 Open Source TM
```

# 目录

* 1.[为什么要研发新的PHP框架](01.0-为什么要研发新的PHP框架.md)
 - 1.1. [传统php-fpm工作模式的问题](01.1-传统php-fpm工作模式的问题.md)
 - 1.2. [压测数据对比](01.2-压测数据对比.md)
 - 1.3. [小结](01.3-小结.md)
* 2.[微服务框架研发概览](02.0-微服务框架研发概览.md)
 - 2.1. [通信框架技术选型](02.1-通信框架技术选型.md)
 - 2.2. [swoole](02.2-swoole.md)
 - 2.3. [协程原理](02.3-协程原理.md)
 - 2.4. [异步、并发](02.4-异步、并发.md)
 - 2.5. [小结](02.5-小结.md)
* 3.[框架运行环境](03.0-框架运行环境.md)
 - 3.1 [环境变量](03.1-环境变量.md)
 - 3.2 [运行代码](03.2-运行代码.md)
 - 3.3 [docker](03.3-docker.md)
 - 3.4 [小结](03.4-小结.md)
* 4.[框架结构](04.0-框架结构.md)
 - 4.1 [结构概述](04.1-结构概述.md)
 - 4.2 [控制器](04.2-控制器.md)
 - 4.3 [模型](04.3-模型.md)
 - 4.4 [视图](04.4-视图.md)
 - 4.5 [同步任务](04.5-同步任务.md)
 - 4.6 [配置](04.6-配置.md)
 - 4.7 [路由](04.7-路由.md)
 - 4.8 [小结](04.8-小结.md)
* 5.[框架组件](05.0-框架组件.md)
 - 5.1 [协程](05.1-协程.md)
 - 5.2 [类的加载](05.2-类的加载.md)
 - 5.3 [异步Http Client](05.3-异步Http%20Client.md)
 - 5.4 [请求上下文](05.4-请求上下文.md)
 - 5.5 [连接池](05.5-连接池.md)
 - 5.6 [对象池](05.6-对象池.md)
 - 5.7 [RPC](05.7-RPC.md)
 - 5.8 [公共库](05.8-公共库.md)
 - 5.9 [RESTful](05.9-RESTful.md)
 - 5.10 [小结](05.10-小结.md)
* 6.[常见问题](06.0-常见问题.md)
* 7.[附录](07.0-附录.md)
# links
  * [目录](<README.md>)
  * 上一节: [首页](<README.md>)
  * 下一节: [为什么要研发新的PHP框架](<01.0-为什么要研发新的PHP框架.md>)