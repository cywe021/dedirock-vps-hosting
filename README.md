# dedirock测试ip：洛杉矶&纽约双节点实测，年付最低$8.88起轻松上车

买VPS这件事，说白了就两个步骤——先测后买。

先用测试IP跑一遍Ping、跑个路由，确认延迟能接受；再比一比价格，觉得划算就下单。顺序不能反，反了就是在给自己挖坑。

最近有不少人问起 **DediRock 的测试IP是多少**，这家美国主机商最近一年活跃得很，价格打得很低，套餐花样也越来越多。正好整理一篇全面的资料，帮大家搞清楚：DediRock 测试IP在哪、怎么测、测出来怎么用——以及如果测完觉得满意，该买哪个套餐。

---

## **DediRock 是什么来头？**

DediRock 是一家美国主机商，以"Rock-Solid Hosting"（磐石级托管）为卖点，主营 KVM VPS、存储VPS、独立服务器三大产品线。数据中心分布在两个核心节点：

- **洛杉矶（Los Angeles, CA）** — 靠近亚洲用户，对中国用户友好度相对较高
- **纽约/布法罗（Buffalo, NY）** — 美国东部，到欧洲延迟更优

机房资源来自 ColoCrossing / H4Y IDC 体系，属于业内老牌数据中心资源。官方宣称年同比增长超过 2000%——听上去很夸张，但价格在低端VPS圈子里确实有目共睹。

👉 [立即前往 DediRock 官网查看最新套餐](https://bit.ly/DediRock)

---

## **DediRock 测试IP 一览**

这是最核心的信息，直接用：

| 节点 | 测试IP（Test IP） | Looking Glass 地址 |
| --- | --- | --- |
| **洛杉矶（Los Angeles）** | `107.174.123.100` / `107.174.123.254` | [la1.lg.dedirock.com](https://bit.ly/DediRock) |
| **纽约/布法罗（Buffalo, NY）** | `199.188.100.133` | [buf1.lg.dedirock.com](https://bit.ly/DediRock) |

> **怎么用？**
> - 直接 `ping 107.174.123.100`，看延迟和丢包率
> - 打开 Looking Glass 网页，输入你的 IP 或域名，选 `mtr`、`traceroute`、`ping6` 等命令，看路由走向
> - 也可以在 Looking Glass 页面下载测试文件（如 `buf1.lg.dedirock.com/10.mb`），感受实际带宽

从国内用户实测来看，**洛杉矶节点**到电信、联通的延迟大概在 150-180ms 区间，路由走 AS36352；**纽约节点**对电信联通的视频速度实测曾达到 12万+ Kbps，美国原生IP，AI 流媒体解锁表现不错，但移动用户路由体验相对一般。

两个节点各有侧重，建议对照自己运营商实测一遍再决定。

---

## **Looking Glass 测速实战指南**

很多人知道有 Looking Glass，但真正会用的不多。简单说一下流程：

1. 打开对应节点的 LG 页面
2. **Ping**：输入你家宽带的公网 IP，直接测往返延迟
3. **Traceroute / MTR**：看路由经过哪些节点，有没有绕路或者明显丢包的跳点
4. **文件下载测试**：用浏览器或 `wget` 命令下载测试文件，看实际下行速度

一个真实的第三方测试数据（YABS，洛杉矶节点，2025年12月）显示：

- **磁盘读写**（512k 块大小）：读约 2.18 GB/s，写约 2.29 GB/s
- **网络带宽**：本地 Los Angeles 节点 iperf3 跑出接近 900 Mbps 上传/920 Mbps 下载
- **Geekbench 6 单核**：710 分

对于入门级年付套餐来说，这个数字相当说得过去了。

---

## **DediRock 全套餐价格对比表**

测完IP觉得可以，下面直接看套餐。DediRock 产品线分几条，从几块钱到几百块都有，总有一款对得上你的预算。

### 🔥 LET Favorites™ — 年付最低价款

| 套餐名称 | 内存 | CPU | 硬盘 | 带宽 | IPv4 | 价格/年 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **New York** | 2 GB | 1核 | 30 GB SSD | 2 TB / 1Gbps | ✓ | **$8.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-let-favorites-ny) |
| **Los Angeles** | 2 GB | 1核 | 30 GB SSD | 2 TB / 1Gbps | ✓ | **$9.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-let-favorites-la) |

> 这两个是 DediRock 最出圈的入门款，社区口碑不错，有库存时随时可下单。

---

### ⚡ The i9 Dream™ — Intel i9-14900K + DDR5 + NVMe

> i9-14900K 单核性能强悍，适合对 CPU 性能有要求的场景（游戏服、编译、Python跑任务）

| 套餐名称 | 内存 | CPU | 硬盘 | 带宽 | 价格/年 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| **Core** | 2 GB DDR5 | 1核 | 30 GB NVMe | 2 TB | **$24.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-performance-vps-ny-core) |
| **Plus** | 3 GB DDR5 | 1核 | 40 GB NVMe | 4 TB | **$34.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-performance-vps-ny-plus) |
| **Power** | 4 GB DDR5 | 2核 | 60 GB NVMe | 6 TB | **$44.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-performance-vps-ny-power) |

---

### 💾 Storage Wars™ — 大硬盘存储 VPS（RAID 5 / RAID 6）

> 备份、归档、私有云（Nextcloud）首选，RAID 阵列加持更稳

| 套餐名称 | 内存 | 存储空间 | 带宽 | 价格/年 | 购买 |
| --- | --- | --- | --- | --- | --- |
| **Core** | 1 GB | 256 GB | 1 TB | **$12.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-storage-ny-core) |
| **Plus** | 2 GB | 1 TB | 2 TB | **$19.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-storage-ny-plus) |
| **Power** | 2 GB | 2 TB | 4 TB | **$29.88** | [立即购买](https://billing.dedirock.com/aff.php?aff=201&pid=promo-storage-ny-power) |

---

### 🖥️ KVM VPS 标准月付款（洛杉矶 / 纽约）

| 套餐名称 | 内存 | CPU | 硬盘 | 带宽 | 价格/月 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| **Starter** | 1 GB | 1核 | 20 GB SSD | 750 GB | $5.99 | [立即购买](https://bit.ly/DediRock) |
| **Essentials** | 2 GB | 2核 | 40 GB SSD | 1 TB | $9.99 | [立即购买](https://bit.ly/DediRock) |
| **Plus** | 4 GB | 4核 | 100 GB SSD | 2 TB | $15.99 | [立即购买](https://bit.ly/DediRock) |
| **Premium** | 16 GB | 8核 | 300 GB SSD | 4 TB | $34.99 | [立即购买](https://bit.ly/DediRock) |

---

### 🚀 The Ryzen Experience™ — AMD Ryzen 9 独立服务器（月付）

> 面向高性能工作负载：渲染、虚拟化、数据库等重量级场景

| 套餐 | CPU | 内存 | 存储 | 价格/月 | 购买 |
| --- | --- | --- | --- | --- | --- |
| **Core** | Ryzen 9 5950X（16核32线程） | 32 GB DDR4 | 1 TB NVMe | **$68.88** | [立即购买](https://bit.ly/DediRock) |
| **Plus** | Ryzen 9 7950X（16核32线程） | 64 GB DDR5 | 2 TB NVMe | **$126.88** | [立即购买](https://bit.ly/DediRock) |
| **Power** | Ryzen 9 7950X3D（16核32线程） | 128 GB DDR5 | 4 TB NVMe | **$211.88** | [立即购买](https://bit.ly/DediRock) |

---

### 🖧 传统独立服务器（月付，Intel Xeon 系列）

| CPU | 内存 | 存储 | 带宽 | 价格/月 | 购买 |
| --- | --- | --- | --- | --- | --- |
| E3-1230v3（4核） | 32 GB | 250 GB SSD | 10 TB | **$49** | [立即购买](https://bit.ly/DediRock) |
| 2× L5520（8核） | 32 GB | 500 GB SSD | 10 TB | **$70** | [立即购买](https://bit.ly/DediRock) |
| E3-1270v5（4核） | 64 GB | 500 GB SSD | 15 TB | **$102** | [立即购买](https://bit.ly/DediRock) |
| 2× E5-2670（16核） | 128 GB | 500 GB SSD | 20 TB | **$119** | [立即购买](https://bit.ly/DediRock) |
| 2× E5-2680v2（20核） | 192 GB | 1 TB SSD | 20 TB | **$138** | [立即购买](https://bit.ly/DediRock) |
| 2× E5-2697v3（28核） | 256 GB | 1 TB NVMe + HWRAID | 25 TB | **$202** | [立即购买](https://bit.ly/DediRock) |
| 2× Gold 6148（40核） | 256 GB | 2×2 TB NVMe + HWRAID | 40 TB | **$263** | [立即购买](https://bit.ly/DediRock) |

> **独立服务器专属优惠码：`15OFFDEDI`** — 所有独立服务器套餐**终身享受 15% 折扣**，直接在结账页面输入。

---

## **真实用户评价怎么说**

从 Trustpilot、LowEndTalk、LowEndBox 等社区收集到的反馈大概这样：

- "Pretty good offers. They offer real good deals from time to time." ——大多数用户对价格满意
- "VPS performance is stable, network quality is reliable." ——LowEndTalk 社区用户：稳定性没什么惊喜但也没出问题
- "Very good performing storage VPS. Fast response to tickets and extremely helpful!" ——存储VPS 用户：磁盘性能ok，工单响应快
- "Hey, it only cost $6.85/year. Even if it's not perfect, it's still an awesome buy." ——LowEndBox 测评博主：$6.85一年，不完美但太划算了

当然也有一些小吐槽：时区默认设置有时候会错，Reverse DNS 设置生效偏慢，这些都是小问题，改一下就好。

---

## **适合哪些人买？**

总结一下适用场景，对号入座：

- **个人建站、博客、小工具部署** → LET Favorites™ 年付款，$8.88 起，够用
- **需要原生美国IP、解锁流媒体** → 纽约节点，电信联通速度有保障
- **有 CPU 密集型需求（跑脚本、编译）** → The i9 Dream™，i9-14900K + DDR5 性价比跑分高
- **备份、归档、私有云** → Storage Wars™，2TB存储才$29.88/年，没理由不心动
- **企业级高性能需求** → Ryzen Experience™ 或 Intel Xeon 独立服务器，按需选型

---

## **下单前最后提醒**

1. **先跑 dedirock 测试IP**，确认洛杉矶 `107.174.123.100` 或纽约 `199.188.100.133` 延迟在你的接受范围内
2. 促销套餐有库存限制，看上了就别拖
3. 独立服务器记得用优惠码 **`15OFFDEDI`**，终身折扣不用白不用
4. 支持 PayPal 和信用卡，付款简单无障碍

👉 [点这里查看 DediRock 所有在售套餐，选你的那一款](https://bit.ly/DediRock)
