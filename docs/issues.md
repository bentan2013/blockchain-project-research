# 区块链项目调研汇总（整理自 Issues）

本文档由仓库 [Issues](https://github.com/bentan2013/blockchain-project-research/issues) 整理而来，内容包括各 issue 正文及评论中的笔记。整理时间：2026-11-05。

> 说明：#17 是一条与本仓库无关、误投到这里的 XYO 产品退款投诉（已关闭），里面有个人邮箱和银行扣款记录，所以没有收录。

## 目录

| # | 项目 | 标签 | 内容 |
|---|------|------|------|
| 1 | [北斗链](#1-北斗链) | 地理、区块链平台 | 官网、白皮书、代币分配 |
| 2 | [Map 去中心三维制图协定](#2-map-去中心三维制图协定) | 地理、区块链协定、数据众包 | 可借鉴点、数据验证、案例、代币架构 |
| 3 | [Geo Satoshi 地理空间数据区块链](#3-geo-satoshi-地理空间数据区块链) | 地理、应用方向、存储 | 摘要、数据验证、机构节点 |
| 4 | [TrustSQL 腾讯可信区块链平台](#4-trustsql-腾讯可信区块链平台) | 区块链平台、存储 | 官网、白皮书、截图 |
| 5 | [Gems 区块链分散式众包协议](#5-gems-区块链分散式众包协议) | 区块链平台、区块链协定、数据众包 | 链接、行业痛点、代币、评分、验证机制 |
| 6 | [BigChainDB](#6-bigchaindb) | 存储 | 官网、源码、简介 |
| 7 | [Startcrowd 基于区块链的 AI 项目众包平台](#7-startcrowd-基于区块链的-ai-项目众包平台) | 应用方向、数据众包 | 官网、简介 |
| 8 | [基于 IPFS 和 GeoHash 构建具有地理位置价值服务的 DDApp](#8-基于-ipfs-和-geohash-构建具有地理位置价值服务的-ddapp) | 地理、存储 | 文章、相关代码 |
| 9 | [TFCoin](#9-tfcoin) | — | 待补充 |
| 10 | [GXChain](#10-gxchain) | — | 待补充 |
| 11 | [FileCoin](#11-filecoin) | — | 待补充 |
| 12 | [FOAM](#12-foam) | — | 官网、白皮书、开发者文档 |
| 13 | [Platin](#13-platin) | — | 待补充 |
| 14 | [XYO network](#14-xyo-network) | 地理、区块链协定 | 官网、白皮书、代码、文章 |
| 15 | [Dataeum](#15-dataeum) | — | 待补充 |
| 16 | [QOS](#16-qos) | 应用方向、区块链平台 | 官网、目标、跨链协议 |

### 按标签分类

- **地理**：#1 北斗链、#2 Map、#3 Geo Satoshi、#8 IPFS + GeoHash、#14 XYO network
- **区块链平台**：#1 北斗链、#4 TrustSQL、#5 Gems、#16 QOS
- **区块链协定**：#2 Map、#5 Gems、#14 XYO network
- **数据众包**：#2 Map、#5 Gems、#7 Startcrowd
- **存储**：#3 Geo Satoshi、#4 TrustSQL、#6 BigChainDB、#8 IPFS + GeoHash
- **应用方向**：#3 Geo Satoshi、#7 Startcrowd、#16 QOS
- **未打标签**：#9 TFCoin、#10 GXChain、#11 FileCoin、#12 FOAM、#13 Platin、#15 Dataeum

---

## 1. 北斗链

- Issue：[#1](https://github.com/bentan2013/blockchain-project-research/issues/1)
- 标签：地理、区块链平台
- 官网：http://www.beidouchain.com/
- 白皮书：http://www.beidouchain.com/wp-content/uploads/2018/01/BeidouChain-White-Paper-V1.1.pdf

![北斗链](https://user-images.githubusercontent.com/5510943/43498856-5a44f2be-957b-11e8-820e-a35828232f60.png)

### 代币分配

北斗币的总发行量，将会在 5 亿枚左右。货币流通的分配比例如下：

1. **矿工池** 42,000 万枚（占流通货币的 84%）：用户支付矿工的工资，不足部分从投资池中支出；
2. **投资池** 6,000 万枚（占流通货币的 10%）：用于项目的对外投资，包括与其他数字货币的兑换；
3. **奖金池** 3,000 万枚（占流通货币的 6%）：用于项目的市场推广和社区建设。

在北斗币中，矿工的作用只有交易验证和数据存储，并不会获得铸币的权利。矿工的激励来自于“货币发行委员会”支付的工资。2017-2018 年度，每位矿工的工资标准平均为：2000 北斗币/月。

目前是核心团队在控制矿工数量和矿工工资标准，未来要交给“矿工工会”自治。

> 来源：简书，作者：剑辰_TCP_盗火，https://www.jianshu.com/p/30a65f057930

---

## 2. Map 去中心三维制图协定

- Issue：[#2](https://github.com/bentan2013/blockchain-project-research/issues/2)
- 标签：地理、区块链协定、数据众包
- 官网：https://mapplatform.com/
- 白皮书（原链接无法打开）：https://mapplatform.com/#section-research
- 相关报道：http://www.qukuaiwang.com.cn/news/7900.html

**MAP 要解决的核心问题是将数字信息锚定到一个去中心化的且实时更新的数字地图**，基于众包机制采集地理空间信息。

![MAP](https://user-images.githubusercontent.com/5510943/43499184-e0f3f944-957c-11e8-8983-7c4ff29a1f54.png)

### 可以借鉴的地方

- **区域管理者**：随着 MAP 的不断发展，MAP 内置的协议允许划分出更小的管理区域，这些管理区域可以由单独的区域管理者进行管理。这让 MAP 能实现自我组织并划分出合适的区域大小。（是否能够加以应用？）
- **扩展性**：存储整个地球的地理空间点数据所需存储空间是巨大的。MAP 提供了一个分片机制，数据按照地理邻近性进行分组。主链将根据经纬度范围在索引中寻找所属的侧链。应用程序和设备可以自由访问所有的公共侧链，同时可以请求获取在设备附近的地理空间信息数据。
- **侧链**：应用程序、公司以及其他用例可以将公共地理空间信息上传到 MAP 公有网络上，同时也可以将部分私有数据上传到私有网络。应用程序将某些私有的数据集保存到私有网络下，且可与 MAP 公有网络无缝集成。

### 数据验证机制

#### 用户角色

- **数据上传者**：通过上传地图数据获得 MAP 代币奖励。要成为数据上传者，用户必须向系统抵押一定数量的 MAP 代币作为保证金，抵押数量决定并限制了其可以上传的数据量和可以获得的奖励。
- **数据验证者**：通过验证地图数据的正确性获得 MAP 代币奖励，作用如同预言机。同样需要抵押 MAP 代币，抵押数量决定并限制其可验证的数据量和奖励。大多数情况下，数据上传者同时也可以是数据验证者。

#### 数据特征验证

MAP 将实现可扩展、可插拔的数据验证策略。例如，一个数据验证策略要求节点（数据上传者）将采集的 3D 地图数据加密后提交以进行共识。提交期结束、共识期开始后，节点提供解密密钥，这样他人无法从区块链复制数据集来骗取代币奖励。共识模型按以下步骤运作：

1. 将数据集添加到区块链需要抵押代币，抵押后产生系统代币债券并暂时锁定。形成共识后，代币债券连同奖励返还给上传者；如果数据集被拒绝，债券将被没收。债券数量不得低于系统最小值，参与者可在此之上自行设定。形成共识时，债券数量更高的数据集权重更高。这一机制让网络参与者通过提交有效且抵押充分的数据集，来抬高不良行为的代价。
2. 存在相同数据集时，系统只认可第一位上传者的数据。
3. 数据集中若不包含最低数量的已有特征点，将被排除在共识之外。
4. 数据集之间相互作特征比对。同一时间段、同一空间中不同设备采集的数据应具有非常相似的特征点。特征点的变化（添加或删除）程度按降序排序。
5. 数据集中被共识接受的特征点，按特征点数量比例获得奖励。

MAP 团队将提供基础的 3D 数据聚合工具，用于识别和过滤来自用户设备的无效数据。3D 数据聚合节点上传无效数据会受到惩罚，因此有经济动机采取额外的识别和过滤措施来提高数据质量。

### 案例

1. **混合现实系统**：混合现实系统（The Mixed Reality System - MRS）是一种将现实世界与通用资源标识符（URI）绑定在一起的数据登记与目录服务，由 W3C 下属的混合现实系统小组开发（https://mixedrealitysystem.org）。MAP 将提供符合 MRS 规范的开发组件，实现公有和私有位置数据的去中心化 MRS 服务。
2. **增强现实**：MAP 使增强现实应用可以运行在去中心化、持续更新的环境中。基于 MAP 开发的应用可以利用其他所有基于 MAP 的应用共享的信息。应用上传地图数据获得的激励收入可用于资助开发与运营，开发商获得的 MAP 代币可在市场上交换其应用的使用权。
3. **地图**：自由的地理空间映射信息加上包含位置信息的去中心化数字地球，使 MAP 成为地图应用数据来源的理想选项。基于地理位置的评价、兴趣点等信息可以轻易添加和更新，且不依赖封闭的中心化地图服务。
4. **无人驾驶载具**：结合路径查找和防碰撞功能，无人驾驶载具使用的路线和航点可在 MAP 中创建和更新。MAP 为无人驾驶载具共享地图数据提供了一种无需大型基础设施支持、简单可靠且容错的方法，载具之间可利用共享信息优化路线、避免碰撞并交换位置信息。
5. **历史档案库**：MAP 为公众提供一个不断更新、所有人可访问的现实世界记录，也可用于前后比对的历史档案，例如建筑许可合规、保险索赔和艺术等用途。
6. **市场推广**：如果没有去中心化平台让用户分享和利用地理空间信息，大型企业将利用资本和能力收集这些数据供私人使用。去中心化平台让每个用户都能从中受益并参与构建。苹果宣布将有 2.5 亿台设备支持 ARKit，Google Tango 手机已开始发售，HoloLens、ODG Glasses 和 Meta 2 等 AR 设备也已面向消费者，数十亿设备将提供更准确、可靠的地理空间信息。
7. **侧链**：同上文“可以借鉴的地方”。
8. **扩展性**：同上文“可以借鉴的地方”。另外，共识和数据验证由随机指定的节点处理，确保无法被恶意行为者接管。
9. **应用程序模型：赞助或直接贡献者**：将虚拟信息嵌入数字地球对娱乐、游戏、社交等几乎所有行业都有价值，嵌入信息需要使用或拥有 MAP 代币。MAP 为用户上传地理空间数据提供多种激励。随着越来越多用户使用 AR 应用，他们会被动地为构建全球地理空间点信息作出贡献；这些应用用其用户数据获取的 MAP 代币，不断添加和更新物理世界中的空间特征点数据。应用虽然是代币激励的受益者，但也会与用户共享 MAP 提供的信息。用户也可以独立上传数据获取收益，可以使用专门方案主动采集，也可以被动共享已采集的数据，例如无人驾驶载具可以成为大规模数据集提供者。

### 代币架构

1. **通胀**：MAP 代币年通胀率 5%，用于代币激励。
2. **代币用途**：将内容加入 MAP 需要抵押 MAP 代币，修改和添加数据也需要消耗代币。部分代币收益给予区域管理者及其支持的节点，其余用于支付网络运行费用，如数据采集激励。
3. **代币发行**：MAP 以共识中被接受的特征点数量为依据，向采集数据的用户发放代币奖励，奖励在用户间平均分配。每个块（每小时或每天）对过去 X 个块中上传的数据做一次统计并计算奖励。网络节点可以是用户，也可以是中介，例如基于 MAP 的应用开发商利用其用户采集的数据获得奖励，以创建完全去中心化、自我维持的应用。

---

## 3. Geo Satoshi 地理空间数据区块链

- Issue：[#3](https://github.com/bentan2013/blockchain-project-research/issues/3)
- 标签：地理、应用方向、存储
- 官网和白皮书：一直没有找到
- 相关资源：
  - https://my.oschina.net/u/2306127/blog/1794310
  - https://www.linkedin.com/pulse/geosatoshi-blockchain-geospatial-data-mark-seibel/?published=t

### 摘要

> Abstract. A purely peer-to-peer open source ecosystem allowing for the aggregation, storage and distribution of geospatial data. The proposed system uses digital coins to incentivize organizations to publish their proprietary geospatial data to benefit the geospatial community at large.

一个纯粹的端到端开源生态系统，允许地理空间数据的整合、存储和分发。区块链技术提供了这一解决方案的一部分，但如果仍需要可信第三方来管理和控制系统，主要的好处就丧失了。该提议是一个建立在区块链技术之上的数字商业系统，用以鼓励和促进高质量地理空间数据的建立。为了激励高质量数据，作者和浏览者都会获得生态系统内的 GeoSatoshi 数字币奖励。区块链技术解决了地理空间数据的几个问题：可访问性、中心化权属和全球可负担性。浏览数据免费，以促进数据开放访问，但下载 features 需要支付 GeoSatoshi coin。系统提议支持匿名，以减少外部胁迫的影响，鼓励非传统但符合道德的数据收集方式。在区块链方式下，数据不是被发送，而是通过 key 访问。该系统使用数字货币鼓励机构公开自己的私有数据，从而在更大范围内造福地理空间数据社区。

**简单说就是一个去中心化的、安全的、社区驱动的全球地理空间数据存储系统。**

### 一些摘录

这一生态系统为地理空间信息社区创建了一个空间，可以交换和创建高质量的数据，且建立在一个去中心化的、可伸缩的公共存储系统之上。

#### 数据验证

> First, created data is submitted to a level 1 data pool. Then, another user of the system, who may or may not be known to the data creator, can peer review the data for level 1 approval. Chance may be introduced if the data creator does not have a peer selected to review their work. Approved level 1 data is submitted to the level 2 pool, where a randomly selected user is chosen for final quality control. Chance is the proposed measure to add spice to the ecosystem as well as anti-conspiracy protection for community users.

### 可借鉴的地方：机构节点托管（Organizational Node Hosting）

> Organizations often have GIS Professionals clustered geographically, with GIS users spread out globally. Enterprise configurations for GIS typically centralize data in a spatial database for client software to access. Historically, organizations have invested a lot of capital to build and acquire geospatial data. Organizations, both public and private, play an enormous role in the development of geospatial data. Organizations should be seen as an ally to the project.
>
> When an organization hosts a node, they are a peer node on the network. Organizations have no authority over the system and the only control they have is turning the node on or off. If they misbehave, the community can exclude the node. Organizations provide a benefit to the community by providing resources to strengthen the network through the node they host.
>
> The benefit organizations receive is faster access to high-quality data without the expense of maintaining a data server. It can take a long time to download geographic data because of their potential enormous size. Local node hosting can be extremely beneficial to organizations in parts of the globe with slow Internet access.

---

## 4. TrustSQL 腾讯可信区块链平台

- Issue：[#4](https://github.com/bentan2013/blockchain-project-research/issues/4)
- 标签：区块链平台、存储
- 官网：https://trustsql.qq.com/
- 白皮书：https://trustsql.qq.com/chain_oss/TrustSQL_WhitePaper.html

![TrustSQL 1](https://user-images.githubusercontent.com/5510943/43503682-d6d70d28-9592-11e8-84d0-52c873409fd9.png)
![TrustSQL 2](https://user-images.githubusercontent.com/5510943/43503670-cdd0f3b0-9592-11e8-8287-a41ebcb62249.png)
![TrustSQL 3](https://user-images.githubusercontent.com/5510943/43503692-e4dd4036-9592-11e8-8d2e-4d170462c1a8.png)
![TrustSQL 4](https://user-images.githubusercontent.com/5510943/43503700-ed338da8-9592-11e8-8b8d-fd6b1673021b.png)
![TrustSQL 5](https://user-images.githubusercontent.com/5510943/43503707-f324d5d2-9592-11e8-87fe-c8a7fc8b820c.png)

---

## 5. Gems 区块链分散式众包协议

- Issue：[#5](https://github.com/bentan2013/blockchain-project-research/issues/5)
- 标签：区块链平台、区块链协定、数据众包
- 官网：https://gems.org/
- 博客：https://blog.gems.org/
- 白皮书：https://gems.org/whitepaper.pdf
- Telegram：https://t.me/gemsorg
- Twitter：https://twitter.com/Gems
- YouTube：https://www.youtube.com/channel/UCn5o1UPQhXjYVKilsohkABA
- 其他资料：https://zhuanlan.zhihu.com/p/33314704

Gems 是一个基于以太坊区块链构建的分散式开源人工任务众包协议。

> The Protocol for Decentralized Mechanical Turk — Decentralized Mechanical Turk powered by Ethereum

### 行业痛点

1. 取消中间人大笔费用
2. 验证来自众包任务的结果的准确性
3. 提供和构建可重用的接口
4. 消除对现有银行基础设施的需求
5. 适当地激励和校验矿工和请求者

### 代币

- 令牌分发：暂无令牌分发计划，或采取荷兰式拍卖方式。
- 总量：80 亿 Token
- 发售：20 亿 Token
- 官方持有：80 亿 Token（原文如此）
- 变动后修改为取消公开募集、白名单，补偿白名单空投份额。
- 募集量 15 万以太坊，流通总量 1.5 亿美金，总量 6 亿美金。

### 评分

| 维度 | 说明 | 总分 | 得分 |
|------|------|-----:|-----:|
| 令牌分发 | 团队过高 | 5 | 0 |
| 商业模式 | 模式清晰 | 20 | 12 |
| 发展阶段 | 公开测试 | 10 | 9 |
| 市场热度 | 热度高 | 5 | 5 |
| 市场规模 | 千亿级 | 10 | 8 |
| 市场定位 | 平台协议 | 20 | 15 |
| 必要性 | 必要性中 | 20 | 12 |
| 行业格局 | 巨头垄断 | 10 | 5 |
| **总计** | | **100** | **66** |

### 验证机制

![Gems 验证机制 1](https://user-images.githubusercontent.com/5510943/43503930-f6e16b08-9593-11e8-906d-cd6b2689b4a4.png)
![Gems 验证机制 2](https://user-images.githubusercontent.com/5510943/43503947-00210ea8-9594-11e8-8956-ccbd7e71d7b3.png)

---

## 6. BigChainDB

- Issue：[#6](https://github.com/bentan2013/blockchain-project-research/issues/6)
- 标签：存储
- 官网：https://www.bigchaindb.com
- 源码：https://github.com/bigchaindb

> Rather than trying to enhance blockchain technology, BigchainDB starts with a big data distributed database and then adds blockchain characteristics - decentralized control, immutability and the transfer of digital assets.

BigchainDB 不是去改进区块链技术，而是从大数据分布式数据库出发，再加上区块链的特性：去中心化控制、不可篡改和数字资产转移。

---

## 7. Startcrowd 基于区块链的 AI 项目众包平台

- Issue：[#7](https://github.com/bentan2013/blockchain-project-research/issues/7)
- 标签：应用方向、数据众包
- 官网：http://www.startcrowd.club/
- 相关链接：
  - https://medium.com/the-ai-lab/startcrowd-a-blockchain-network-for-artificial-intelligence-projects-728069ffd5a1
  - https://blog.csdn.net/mongo_node/article/details/79864031

Startcrowd 是一个分享 AI 项目的社交网络。在 Startcrowd，项目发起者可以发布他们的项目，其他人可以参与项目。在未来的迭代中，贡献者将能够通过区块链代币获得报酬。Startcrowd 产品已经启动（暂时还没有开通区块链功能）。

---

## 8. 基于 IPFS 和 GeoHash 构建具有地理位置价值服务的 DDApp

- Issue：[#8](https://github.com/bentan2013/blockchain-project-research/issues/8)
- 标签：地理、存储
- 原文：[【IPFS】基于IPFS和GeoHash构建具有地理位置价值服务的DDApp（理论篇）](https://www.daijiale.cn/%E5%8C%BA%E5%9D%97%E9%93%BE/%E3%80%90ipfs%E3%80%91%E5%9F%BA%E4%BA%8Eipfs%E5%92%8Cgeohash%E6%9E%84%E5%BB%BA%E5%85%B7%E6%9C%89%E5%9C%B0%E7%90%86%E4%BD%8D%E7%BD%AE%E4%BB%B7%E5%80%BC%E6%9C%8D%E5%8A%A1%E7%9A%84.html)

打造地理位置信息与区块链的关系对象模型，建立一套 **人 -> 位置 -> 真实世界 -> 传递信任 -> 价值转移 -> 位置 -> 人** 的生态模型，实现用区块链来索引真实世界的愿景。

![IPFS + GeoHash](https://user-images.githubusercontent.com/5510943/43505104-6e360b7e-9598-11e8-9fc9-8cbf83613549.png)

### 相关资料

- [利用IPFS构建自己的去中心化分布式Wiki系统](https://www.daijiale.cn/%E5%8C%BA%E5%9D%97%E9%93%BE/%E3%80%90ipfs%E3%80%91%E5%88%A9%E7%94%A8ipfs%E6%9E%84%E5%BB%BA%E8%87%AA%E5%B7%B1%E7%9A%84%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%8C%96%E5%88%86%E5%B8%83%E5%BC%8Fwiki%E7%B3%BB%E7%BB%9F.html)
- https://github.com/ipfs/ipfs-geoip
- https://github.com/daijiale/ipfs-geo

---

## 9. TFCoin

- Issue：[#9](https://github.com/bentan2013/blockchain-project-research/issues/9)
- 暂无内容，待补充。

## 10. GXChain

- Issue：[#10](https://github.com/bentan2013/blockchain-project-research/issues/10)
- 暂无内容，待补充。

## 11. FileCoin

- Issue：[#11](https://github.com/bentan2013/blockchain-project-research/issues/11)
- 暂无内容，待补充。

---

## 12. FOAM

- Issue：[#12](https://github.com/bentan2013/blockchain-project-research/issues/12)
- 官网：https://foam.space/
- 白皮书：https://foam.space/publicAssets/FOAM_Whitepaper.pdf
- 技术白皮书：https://github.com/f-o-a-m/public-research/blob/master/FOAM%20Techincal%20Whitepaper%20Draft.pdf
- 开发者文档：https://f-o-a-m.github.io/foam.developer/
- Telegram：https://t.me/foamspace

---

## 13. Platin

- Issue：[#13](https://github.com/bentan2013/blockchain-project-research/issues/13)
- 暂无内容，待补充。

---

## 14. XYO network

- Issue：[#14](https://github.com/bentan2013/blockchain-project-research/issues/14)
- 标签：地理、区块链协定
- 官网：https://xyo.network/
- 白皮书：https://xyo.network/papers/
- 代码：https://github.com/XYOracleNetwork
- 产品：https://www.xyfindit.com/
- 视频：
  - XY4+ 视频：https://youtu.be/aJ45UQ07G8Y
  - XYO 简介中文语音视频：https://youtu.be/ykLNM_qkHdE

### 技术基础设施

XYO Network 拥有具有以下功能的技术性基础设施：

- 通过 XYO 网络的设备生态系统确定物体具体的平面 XY 坐标，让智能合约能够与真实世界连接起来；
- 用户可以使用在智能合约中执行交易的应用程序；
- 以地理为重点，达成一致并对位置数据进行可靠的验证；
- 确保实时验证对象确切位置的精确性和可靠性。

![XYO 1](https://user-images.githubusercontent.com/5510943/43626759-d7818246-9725-11e8-897a-25a506c6960e.png)
![XYO 2](https://cdn-images-1.medium.com/max/1400/1*LR8SL7fwSlDUFY1Lgl86Ng.png)

### 相关文章

- [XYO Network 是如何工作的？](https://medium.com/@1782181712/xyo-network%E6%98%AF%E5%A6%82%E4%BD%95%E5%B7%A5%E4%BD%9C%E7%9A%84-394be68c6193)
- [ICO 分析：首次代币发行分析 XYO Network](https://medium.com/@1782181712/%E9%A6%96%E6%AC%A1%E4%BB%A3%E5%B8%81%E5%8F%91%E8%A1%8C%E5%88%86%E6%9E%90-xyo-network-175100d3bd76)
- 与 XYO Network 的整合：以太坊 vs EOS vs NEO
  - [上篇](https://medium.com/@1782181712/%E4%B8%8Exyo-network%E7%9A%84%E6%95%B4%E5%90%88-%E4%BB%A5%E5%A4%AA%E5%9D%8Avs-eos-vs-neo-%E4%B8%8A-4edaf833be2)
  - [下篇](https://medium.com/@1782181712/%E4%B8%8Exyo-network%E7%9A%84%E6%95%B4%E5%90%88-%E4%BB%A5%E5%A4%AA%E5%9D%8Avs-eos-vs-neo-%E4%B8%8B-34b5866d4998)

---

## 15. Dataeum

- Issue：[#15](https://github.com/bentan2013/blockchain-project-research/issues/15)
- 暂无内容，待补充。

---

## 16. QOS

- Issue：[#16](https://github.com/bentan2013/blockchain-project-research/issues/16)
- 标签：应用方向、区块链平台
- 官网：https://www.qoschain.io （首页有白皮书下载链接）
- 相关文章：https://mp.weixin.qq.com/s/xe5DWP37NVE3V98cYrFMwQ

**QOS 的目标是通过底层公链把传统公司化行为转换成社区行为，通过通证把中心化激励体系变成社区自激励体系，赋能实体经济。**

**QOS 通过打造基于公链与联盟链混合的底层操作系统、统一身份认证体系、自激励的双层代币协议、超级节点 + 交易挖矿的双层挖矿机制、分布式文件系统、联通开发者和用户的互动社区……**

![QOS 1](https://user-images.githubusercontent.com/5510943/43768330-b63c007e-9a69-11e8-8a31-3eee52fc25a6.png)

> 我们不是设计区块链基础协议，而是专注于权益记录和转移的区块链网络。

QOS 提供一种跨链的协议标准，相当于一个中间层，所有的应用链通过它来交换数据。

> QSC 协议是符合 QOS 公链标准的、基于智能合约的代币发行与运营协议。开发者基于 QSC 协议可以在 QOS 上实现自己的自治组织，由于开发者遵循统一的 QSC 协议，因此能安全地实现价值互转。

![QOS 2](https://user-images.githubusercontent.com/5510943/43769320-0c6132e2-9a6c-11e8-9a76-d32d242333bf.png)
