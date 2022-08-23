# 220823 [background check stage]

> A plan for building up CEPH cluster by RBPi (CM4 .etc) or other linux cards to replace x86 dual CPU NAS server, purpose for having high availability with no higher power consumption.

### 项目初衷 (痛点): 为什么需要搭建低功耗的 CEPH 集群

作为一个即将出国的留学生，我希望家里的NAS可以一直运行。显然，我不能让让爸妈来当服务器运维，也不能使用太夸张的高可用方案。我目前运行 ESXi 和 Truenas SCALE 的四台 4U 服务器，总计 80 个 cpu 线程和 134GB 内存的洋垃圾机柜已经使父母不愿支持我的瞎折腾了。因此，我必须确保留学期间家里的NAS足够轻量。

### 此项目正在背调阶段

谷歌到了个类似的产品 - Jeff Geerling (@geerlingguy) 在油管评测了个 ITX 的能装 6 个 CM4 的底板，并且就是用于测试 CEPH 的部署。 `https://www.youtube.com/watch?v=ecdm3oA-QdQ`

但以下功能是这个产品不具有，而我需要的:

- 板型需要是 E-ATX 或 SSI-EEB 以充分利用机箱空间
- 核心板应该设计立体的扩展板载板，以充分利用 3U/4U 机箱的立体空间
- 每个核心板都应该配置独立的 PCIE 插槽，以扩展诸如 HBA 卡、缓存 SSD 或其他高速 IO 扩展卡
- 需要足够容易在中国获得