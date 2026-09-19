# IEPL 套餐：MkCloud 广港、沪日、沪美全线价格与配置对照，按流量和带宽选对档位

搜“IEPL 套餐”的人，十有八九卡在同一个地方：已经知道 IEPL 专线比普通 VPS 稳定、延迟低，但打开产品页就懵了——共享带宽、独享带宽、流量计费，档位从几百元排到上万元，不知道哪一档够自己用，也不知道标价里有没有坑。

这篇文章直接用 Mkcloud 官方商店当前展示的完整套餐价格来回答这个问题：每条线路有哪些档、差在哪、什么场景选哪档、下单前要注意什么限制。价格和配置全部来自 2026 年 9 月抓取的官方商店页，不是旧文章里搬来的历史价。

## 先把三件事说清楚

**第一，IEPL 套餐不是机场套餐。** Mkcloud 卖的是“专线 VPS”：一台完整的云服务器，外加一条跨境专线。你用 SSH 或远程桌面连上入口 IP，在服务器里跑业务程序，流量从独立的出口 IP 发出去。它没有订阅链接、没有客户端节点，官方也明确禁止机场、回国等用途。如果你要找的是那种按月订阅的代理服务，这篇可以帮你省下时间。

**第二，IEPL 和 IPLC 的区别没那么玄乎。** 两者都是点对点跨境专线，IEPL（国际以太网专线）走以太网二层承载，IPLC 走传统专线承载，对用户来说最直观的差别是：IEPL 段内延迟更低、更不容易受公网拥塞影响。普通 VPS 走公网出口，跨境高峰期延迟波动大；专线产品解决的就是这个问题。

**第三，宣传页上的“1~2ms”是端内延迟**，也就是国内入口到海外出口这一段的延迟，不包括你家宽带到入口、以及出口到目标网站的后半程。广港 IEPL 官方标 1~2ms，沪港 21ms，沪日 25~28ms，沪美 124~134ms。判断全程速度时，要把前后的路径加进去，不能拿端内数字当全程延迟。

## Mkcloud 是谁，交付形态长什么样

Mkcloud 是 2023 年开始运营的国人商家，主打合规跨境专线服务器，现售线路覆盖广港 IEPL、沪港/沪日/沪美 IPLC、福建高防专线、IX 云接入线路和上海 CN2。第三方测评（2023 年末）提到它支持支付宝付款、现货约一分钟自动开通，这两点至今仍出现在用户的购买流程反馈里。

买之前，有几条硬性限制必须先知道，它们直接影响“该不该买”：

- **实名与省份绑定**：购买需要中国身份信息实名（手机号、身份证、姓名一致性验证）。直连产品采用省级白名单，只允许一个省份的 IP 连入，之后可以修改绑定省份。
- **流量双向统计**：计量型套餐按上行+下行双向合计，标 1TB 实际等效的单向流量约 500GB，超量后暂停，可购买流量重置或提交工单补差价升级。
- **出口不支持外部连入**：适合店铺后台操作、素材上传、授权 API 访问这类“从服务器向外访问”的任务，不能拿来做公开网站、支付回调或游戏服务端。
- **退款政策严格**：仅质量问题支持退款，需要工单里提交具体延迟、速度数据，开通后不支持更换地域。
- **默认无 SLA**：标准产品不承诺无中断，有保障需求要先问客服。
- **升降级走工单**：降级差价不退，这点和多数云厂商不同，买大档前想清楚。

官方知识库里还有一条值得注意的口径差：部分文章写着“广港 IEPL 共享入门 228 元/月”，那是较早的资料。当前商店页的共享起步档是 1TB 流量、358 元/月。历史活动价（比如早年 198 元/500GB 的档位）也已经调整过。**一切以购物车结算价为准**，这也是下文所有表格的取数原则。

## 广港 IEPL：华南到香港，1~2ms

广港是 Mkcloud 的招牌线路：广州入口（腾讯广州八线 BGP），香港 BGP 出口，端内延迟 1~2ms，每台配独立入口 IP + 独立出口 IP。共享和独享两个计费体系，档位全部列在下面。

**流量计费（共享带宽）档位：**

| 档位 | 配置 | 价格 | 购买 |
| --- | --- | --- | --- |
| 1TB/月 | 1核2G / 20G盘 / 200M峰值 | ¥358/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 2TB/月 | 2核4G / 40G盘 / 300M峰值 | ¥568/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 4TB/月 | 2核4G / 40G盘 / 300M峰值 | ¥998/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 6TB/月 | 4核8G / 60G盘 / 500M峰值 | ¥1388/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 10TB/月 | 4核8G / 60G盘 / 500M峰值 | ¥2288/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |
| 20TB/月 | 4核8G / 60G盘 / 1G峰值 | ¥4500/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh) |

**独享带宽（不限流量）档位：**

| 带宽 | 配置 | 价格 | 购买 |
| --- | --- | --- | --- |
| 5M独享 | 2核4G / 40G盘 | ¥500/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 10M独享 | 2核4G / 40G盘 | ¥700/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 20M独享 | 2核4G / 40G盘 | ¥1320/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 50M独享 | 4核8G / 60G盘 | ¥3150/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 100M独享 | 4核8G / 60G盘 | ¥5800/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 200M独享 | 4核8G / 60G盘 | ¥11600/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |
| 300M独享 | 4核8G / 60G盘 | ¥17400/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-ex) |

算一笔流量账：1TB 档 358 元，按双向合计口径，等效单向约 500GB，折合约 0.7 元/GB——和 2023 年末第三方测评给出的 0.7~0.8 元/GB 基本一致，说明价格调整后单价口径没变。如果你的业务每月稳定传输超过 1.5TB，5M 独享（500 元/月，跑满一个月理论流量约 1.5TB）反而更划算，且不受超量停机影响。

## 沪日 IPLC：上海到日本，25~28ms

沪日共享入口为上海电信，独享则分上海电信和上海 BGP（UCloud）两种入口，后者贵一些但入口网络不同，适合按你本地宽带的实测来挑。

**流量计费（共享带宽）：**

| 档位 | 配置 | 价格 | 购买 |
| --- | --- | --- | --- |
| 1TB/月 | 1核2G / 200M峰值 | ¥358/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 2TB/月 | 2核4G / 300M峰值 | ¥568/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 4TB/月 | 2核4G / 300M峰值 | ¥998/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 6TB/月 | 4核8G / 500M峰值 | ¥1388/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 10TB/月 | 4核8G / 500M峰值 | ¥2288/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |
| 20TB/月 | 4核8G / 1G峰值 | ¥4500/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-sh) |

**独享带宽（不限流量）：**

| 带宽 | 上海电信入口 | 上海BGP入口 |
| --- | --- | --- |
| 5M | ¥600/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex) | ¥700/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-jp-ex) |
| 10M | ¥800/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex) | ¥1000/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-jp-ex) |
| 20M | ¥1560/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex) | ¥1960/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-jp-ex) |
| 50M | ¥3500/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex) | ¥4500/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-jp-ex) |
| 100M | ¥6000/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex) | ¥8500/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-jp-ex) |

电信入口独享还有 200M（12000 元/月）和 300M（18000 元/月）两档，同样在 [👉 沪日独享套餐页](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-jp-ex) 可以选到。

## 沪港 IPLC：上海到香港，21ms

沪港共享入口是上海电信，独享入口分上海电信和上海 BGP。这条线是四个方向里共享起步价最低的：

| 档位 | 配置 | 价格 | 购买 |
| --- | --- | --- | --- |
| 1TB/月 | 1核2G / 200M峰值 | ¥288/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 2TB/月 | 2核4G / 300M峰值 | ¥428/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 4TB/月 | 2核4G / 300M峰值 | ¥696/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 6TB/月 | 4核8G / 500M峰值 | ¥988/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 10TB/月 | 4核8G / 500M峰值 | ¥1536/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |
| 20TB/月 | 4核8G / 1G峰值 | ¥3072/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-sh) |

独享带宽（上海 BGP 入口）档位：5M ¥650、10M ¥950、20M ¥1760、50M ¥4000、100M ¥7500，均在 [👉 沪港独享套餐页](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-hk-ex) 选购。另外官方知识库确认上海电信入口的独享入门为 5M、388 元/月、不限流量，是全站独享档的最低价；该档位在商店里以入口网络区分，下单前可在 [👉 Mkcloud 商店](https://bit.ly/MKCLoud) 里核对当前可选入口。

计费周期方面，官方资料确认沪港共享 1TB 档季付 864 元、年付 3456 元，也就是月付 ×3 和 ×12，长周期本身不打折。想省钱的路径不是囤年付，而是用好下面说的优惠码和活动。

## 沪美 IPLC：上海到美国，124~134ms

美区业务（ERP、eBay、TikTok 美区后台等）看这条线。物理距离摆在那里，124~134ms 的端内延迟是正常水平，专线解决的是稳定和丢包，不是把延迟变成 30ms。

| 档位 | 配置 | 价格 | 购买 |
| --- | --- | --- | --- |
| 1TB/月 | 1核2G / 200M峰值 | ¥428/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 2TB/月 | 2核4G / 300M峰值 | ¥698/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 4TB/月 | 2核4G / 300M峰值 | ¥1258/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 6TB/月 | 4核8G / 500M峰值 | ¥1758/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 10TB/月 | 4核8G / 500M峰值 | ¥2888/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |
| 20TB/月 | 4核8G / 1G峰值 | ¥5666/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-sh) |

独享带宽（不限流量，可 24 小时持续跑满）：

| 带宽 | 上海电信入口 | 上海BGP入口 |
| --- | --- | --- |
| 5M | ¥800/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) | ¥850/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-us-ex) |
| 10M | ¥1100/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) | ¥1300/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-us-ex) |
| 20M | ¥2100/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) | ¥2560/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-us-ex) |
| 50M | ¥5000/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) | ¥6000/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-us-ex) |
| 100M | ¥9000/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) | ¥11500/月 [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fshh-us-ex) |

电信入口独享更高还有 200M（18000 元/月）和 300M（27000 元/月）两档，在 [👉 沪美独享页](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fsh-us-ex) 可见。

## 福建高防与 IX 云接入线路

**泉港高防 IPLC**（泉州电信入口 → 香港 BGP 出口，端内 1~2ms，默认含 100Gbps DDoS 高防，防御可定制升级，无跨省 QoS、无省份限制）全部为独享带宽：

| 带宽 | 配置 | 价格 | 购买 |
| --- | --- | --- | --- |
| 200M独享 | 4核8G | ¥5600/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fqz-hk-ex) |
| 500M独享 | 8核8G | ¥11500/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fqz-hk-ex) |
| 1G独享 | 28核64G（赠独立服务器） | ¥20000/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fqz-hk-ex) |
| 2G独享 | 28核64G（赠独立服务器） | ¥38000/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fqz-hk-ex) |
| 5G独享 | 28核64G（赠独立服务器） | ¥90000/月 | [ 购买](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fqz-hk-ex) |

同系列的厦港（厦门 BGP 入口）需要注意：Mkcloud 在 2026 年 2 月曾发布公告，称因上游要求厦门 BGP 产品将关停，虽然商店里厦港高防页面目前仍挂在售，**下单前建议先提交工单确认该线路现状**，避免买到中途停服的产品。

**IX 云接入线路**走云厂网络（阿里云、腾讯云、百度云国内全网等）作为前置，端内延迟 1~2ms（深港）或 21ms（沪港）。以沪港 IXP 独享为例：100M 独享 2500 元/月、200M 4600 元、500M 11000 元、1G 19000 元、2G 38000 元、5G 95000 元，可在 [👉 沪港IXP独享页](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fcloud-sh-hk-ex) 查看现售档位。IX 共享入门价 158 元/月起，是全站门槛最低的档位，但 2026 年上半年官方通知 IX 产品曾因需求激增整体售罄、且阿里云至深圳/上海 IX 方向一度切断整改，**买前务必确认库存和方向可用性**。另外这类产品需要自备支持的云厂机器做前置，前置成本要算进总预算。

还有一款特殊产品**上海动态 IP 双线 CN2**（上海动态联通入口、上海电信 CN2 出口，8 核 16G / 500Mbps 独享，4500 元/月），这是国内优化线路而不是海外出口，不要当美区或港区产品买。详情可通过 [👉 Mkcloud 官方商店](https://bit.ly/MKCLoud) 和客服确认。

## 优惠码与省钱方式

Mkcloud 的活动频率不低，但口径要分清“当前有效”和“历史活动”：

- **MK-IEPL-WELCOME**：IEPL 产品 9 折循环。第三方优惠汇总站目前标注有效期至 2026 年 12 月 31 日；早年测评提到过最低档不适用，现在下单时在购物车试一下抵扣即可确认。对应产品入口：[👉 领九折选购IEPL套餐](https://www.mkcloud.net/aff.php?aff=390&url=https%3A%2F%2Fwww.mkcloud.net%2Findex.php%2Fstore%2Fgz-hk-sh)
- **MK-IPLC-WELCOME**：IPLC 产品 9 折循环，有效期口径同上。
- **MK-8.8 / MK-7.8**：分别对应流量计费产品 8.8 折循环和独享带宽首月 7.8 折。官方活动回顾页标注“活动期内有效”，第三方优惠站目前仍列到 2026 年 12 月 31 日——两个口径有出入，**以购物车实际结算为准**，能用就是能用的最直接证据。
- **部分节日活动直接在购物车选择优惠**，不需要填码。比如 2026 年 9 月初结束的沪港 IPLC 新品活动（流量产品 7.7 折循环、独享首月 5 折）就是这种形式，已经结束，官方明确表示不再作为当前价格依据。

一个提醒：Mkcloud 的历史活动（新春机 236 元/月、618 限定机 268 元/月、两周年限定 486 元/月等）价格确实诱人，但都已过期，官方在每个活动回顾页顶部都标注了“活动已结束”。看到第三方文章里的折后价，先看日期，再对照商店现价。

## 按场景选档位

- **TikTok/独立站店铺后台、多账号防关联**：1~2TB 共享档够用，重点是要独享 IP 和稳定的端内延迟，广港（1~2ms）或沪港（21ms）按你的地理位置和宽带实测选。Mkcloud 官方也把“一账号一 VPS 一 IP”作为这类场景的推荐用法。
- **间歇性素材上传、备份**：按月流量选共享档，2TB 或 4TB 档起步，注意双向统计口径。
- **7×24 持续传输（数据同步、直播推流中继）**：直接看独享带宽。5M 独享跑满一个月约 1.5TB，比同流量的共享档更省心，且不受超量停机影响。
- **美区 ERP、eBay 运营**：沪美方向，共享 1TB 起步试水，流量上来后换 5M/10M 独享。
- **有攻击风险的业务**：泉港高防，预算从 5600 元/月起，防御参数建议先问客服确认再下单。

## 常见问题

**IEPL 套餐月付季付年付怎么选？** 现有资料显示长周期按月付倍数计算（季付 ×3、年付 ×12），囤长周期本身不省钱；省钱靠活动码和节日折扣。月付试水、稳定后再考虑长周期是更稳的路径。

**出口 IP 是原生 IP 吗？** 官方口径明确：当前为服务器 IP，不保证原生、住宅、流媒体解锁或历史完全干净。有 IP 质量硬需求的，下单前先工单咨询或小规模试用。

**超流量会怎样？** 计量型套餐超量后暂停服务，可自助购买流量重置，或提交工单补差价升级套餐。降级差价不退。

**能建站吗？** 不能。出口不支持外部连入，公开网站、支付回调、邮件接收、游戏服务端都需要另外找支持入站的产品。

**能用来挂代理吗？** 不能。官方服务条款明确禁止机场、回国等用途，产品采用省份白名单等措施防止转售，违规会被清退且不退款。
