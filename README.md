
---

:confused: **或许你在网上看过一些资料，了解一些分布式事务的解决办法，然而，一切还只是停留在理论阶段。**

:confused: **或许你知道可以通过可靠消息、TCC、最大努力通知等方案来解决分布式事务问题，然而，一切还只是停留在理论阶段。**

:confused: **或许你能说出来可以通过一些开源的技术来实现分布式事务，然而，一切还只是停留在理论阶段。**

---


#### > 好吧，先看看下面的业务场景
以商城下单支付作为案例

    1. 支付成功后，可能会出现垮多个服务修改数据，就会遇到分布式事务问题，如何保证垮服务下的业务数据一致性？

    2. 支付成功后，积分、账户等数据需要实时变更，在分布式服务下，如何保证数据实时一致性？

    3. 支付成功后，银行异步通知支付结果，如果网络或者自身服务器出现故障，如何保证业务数据一致性？

    4. ......


#### > 当前项目的功能业务说明
    以【商城下单支付】作为当前分布式项目的核心功能，最终的目的是通过代码来解决分布式事务的相关问题。

    最终，你将会知道如何通过代码来解决上面提到的3个业务场景的问题，从而摆脱理论阶段进入项目实战。

#### > 常见的分布式事务解决方案：
>     1. 可靠消息最终一致性（异步确保型）

>     2. 最大努力通知（定期校对）

>     3. TCC（两阶段型、补偿型）

   以上3种分布式事务的解决方案，将会在项目中通过代码完整的展现。


#### > 项目技术选型
    - 项目主要采用Dubbo作为服务治理框架
    - 采用SpringBoot作为微服务开发框架。服务之间可独立部署、业务解耦、扩展性好。
    - 项目整体框架为Spring、SpringMVC、Mybtais、Mysql、Zookeeper、ActiveMQ、Dubbo、JSP、Dwz(富客户端)、......

#### > 项目功能模块划分简单说明
通过模拟真实业务场景，通过代码来解决实现分布式事务，故，就需要对业务进行拆分，而非单实例应用！

项目模块大概划分如下：
01. 在线商城系统
02. 支付网关系统
03. 银行支付通知(模拟通知回调)
04. 订单服务
05. 积分服务
06. 会计原始凭证记账服务
07. 账户服务
08. 商户通知服务
09. 可靠消息服务
10. TCC服务
11. 消息状态确认子系统
12. 消息恢复子系统
13. 消息管理子系统
14. BOSS系统
15. (后续更新)

#### > 最新动态
    目前处于开发阶段，还未完成，敬请期待。

