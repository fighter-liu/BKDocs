# 第三方 ES 接入

第三方 ES 接入的场景主要是解决，已存在的 ES 集群接入日志服务使用，或者是从采集入到第三方的集群中。

## 前置步骤

### 功能介绍

* 先接入 ES 集群

导航路径：管理  →  数据接入  →  ES 源接入  →  新建

![-w2020](./media/2019-12-13-17-30-30.jpg)


输入完整的 ES 集群地址后，进行连通性测试，测试通过方可保存。

> 第三方 ES 集群版本支持 >=5.4 ， 测试验证过 5.4 到 7 的版本。

* 创建索引集

接入第三方 ES 的集群后，要能够真正的使用起来，还需要创建索引集才可以使用。

导航路径：管理  →  索引集管理  →  新建

![-w2020](./media/2019-12-13-17-26-59.jpg)

支持“*”匹配多个索引，要求所有匹配到的索引的字段一致，并且索引必须包含一个时间字段，否则无法完成接入。

* 采集接入

想把采集数据接入到第三方 ES 的集群，在采集的时候选择第三方的 ES 集群即可。具体查看[采集接入](./logs_overview.md)
