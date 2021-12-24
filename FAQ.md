
# FAQ


## 关于Hummingbot

### Hummingbot是什么？

Hummingbot是一个开源的交易软件，可以帮助您构建和运行量化交易机器人。更多相关信息，请阅读[Hummingbot白皮书](https://www.hummingbot.io/whitepaper.pdf) 

### 为什么要让Hummingbot向公众开放，而不是仅仅在公司内部运行？

我们通过运行[流动性挖矿](https://miner.hummingbot.io)来赚钱，它允许项目方从去中心化网络获取流动性，而不是某个公司。Hummingbot是一个免费工具，任何人都可以使用它来参与流动性挖矿。

### 为什么让Hummingbot开源?

**信任和透明度。**要使用量化机器人进行数字货币，用户必须提供他们API keys和API密钥。开源代码库使任何人都可以审查和审计代码。

### 我需要多少加密货币才能开始？

虽然使用Hummingbot没有最小资产数量，但用户应该注意交易所设定的最小订单大小，在[交易所链接](https://docs.hummingbot.io/connectors)文档中，包含了交易所最小订单的链接。
我们建议您先从较小的资产开始,慢慢的熟悉Hummingbot。

### 我的API keys和API密钥安全吗？

由于Hummingbot是一个本地客户端，所以您的私钥和API密钥与运行它们的计算机一样安全。密钥用于在本地机器上本地创建授权指令，只有已经签名或授权的指令才从客户机发出。

始终保持谨慎，确保运行Hummingbot的计算机是安全的，没有未经授权的访问。

### 运行Hummingbot需要多少费用？
Hummingbot 是一款免费软件，因此您可以免费下载、安装和运行它。

Hummingbot的交易是在交易所进行的正常交易;因此，使用Hummingbot时，您需要支付每个交易所的费用(例如maker、taker和提现费)，就像你在那个交易所正常交易一样(比如没有使用Hummingbot)。

#### Hummingbot 支持哪些交易所？

Hummingbot有很多的中心化和去中心化交易所可供选择，您可以用不同的连接器进行不同的策略。了解更多信息，请参考一下链接：[Hummingbot 交易所连接器](https://docs.hummingbot.io/exchanges/)

## 关于流动性挖矿

### 什么是流动性挖矿？

流动性挖矿是一种基于社区的，数据驱动的做市方法，在这种方法中，代币发行者或交易所可以奖励矿工池，为指定代币提供流动性。

流动性挖矿收益的计量框架基于（1）时间（订单簿一致性），（2）订单价差和（3）订单大小，是一种较为公平报酬模型。风险和收益成正比。

有关更多信息，请阅读[英文白皮书](https://hummingbot.io/liquidity-mining.pdf)。

### 为什么称作“流动性挖矿”？

流动性挖矿类似于在更广义的加密货币上下文中使用的“挖矿”，因为：（1）参与者正在使用自己的计算资源进行做市（例如，通过运行Hummingbot客户端），以及（2）用户部署自己的加密货币资产清单（≈“抵押”）。

此外，为了实现共同的目标，一群参与者正在共同努力为特定代币和交易所提供流动性。作为回报，矿工将获得与其“工作”相对应的代币奖励。奖励分配的规则也如加密货币挖矿一样有明确的算法定义。

### 参与流动性挖矿，我应该使用什么做市策略？

流动性挖矿奖励是根据创建的限价订单（“Maker”订单）确定的。当前，Hummingbot客户有多种创建Maker订单的策略：
例如：
- 纯做市策略
- 跨交易所做市策略
- AS交易策略
- 流动性挖矿策略
更多详细信息，请查看：[做市策略](https://docs.hummingbot.io/strategies/#list-of-strategies)
使用这些交易策略中的任何一种，将使您有资格参与流动性挖矿并获得奖励。

### 如何评估流动性？

我们认为，相对于市场广泛使用的已成交订单量，滑点(Slippage)是量化流动性的最佳指标。滑点是指在给定规模的交易中，观察到的中间市场价格与实际执行价格之差，是交易成本之一。计算订单簿深度和不同深度价格的滑点系数，可以更好地了解实际交易该资产的摩擦和效率。较深且流动性高的订单簿的滑点较低，而较薄且流动性低的订单簿的滑点较高。

我们认为，滑点比交易量更能反映流动性。作为事前指标，滑点测量的是交易者在交易之前使用的信息，以决定是否执行交易以及在哪个时间点执行交易。相反，交易量是事后衡量标准，可以轻松地被人为操控。


### 如何计算流动性挖矿的奖励收益？

为了使做市商具有经济意义，做市商的薪酬必须与其承担的风险水平的相关。在流动性挖掘中，我们使用三个主要参数来确定做市商（也就是参与流动性挖矿的 “矿工”）薪酬：（1）时间：随着时间的推移在订单簿中连续下订单，（2）点差和（3）订单大小。

在流动性挖掘中，做市商通过持续不断地下订单来积累更多的报酬，并通过点差更小和规模更大的订单来获得更高的报酬。实时奖励信息将显示在实时Hummingbot Miner上。
![](https://docs.hummingbot.io/assets/img/mining-rewards-diagram.jpg)

更多详情，可以阅读[英文博客](https://hummingbot.io/blog/2019-12-liquidity-mining-rewards/)。


### 奖励是如何分配的？

在每个以周为单位的奖励周期，总付每周酬劳将平均分配到该周期中的每一分钟。对于每一分钟，都会从该分钟内获取随机快照，以用于计算奖励分配。

对于每个快照，奖励的一半分配给订单簿的买入方，另一半分配给订单簿的卖出方。我们强制执行50/50的分配比例，以阻止参与者使用我们的系统在一个方向或另一个方向上操纵价格。如果没有为特定快照提交符合条件的订单，则为该快照分配的奖励金额将滚存并添加到后续快照的奖励金额中。

### 我在某一交易对上的奖励收益会影响我在其他交易对上的收益吗？

不会，每个市场的奖励分配是独立计算的。每个付款分配将基于紧接在前的奖励周期上的符合要求的交易活动，而不是基于先前的奖励周期。

### 何时我才会收到我的挖矿收益？

每个周期开始和结束于每个周二上午8：00（北京时间）。奖励在每个周期结束后3个工作日分配给每个参与者的钱包地址。

### 作为矿工，我会承担什么风险呢？

像任何交易策略一样，做市也包括风险。主要风险之一是存货风险，即因做市而导致存货价值出现下跌的风险。例如，如果价格在短时间内大幅下跌，并且做市商由于买单的持续执行而在资产中积累了大量头寸，那么他们的整体库存价值可能会更低。

请注意，已发布的流动性挖矿回报说明了流动性报酬的回报与承诺维持订单的库存价值成正比。这些数字未考虑与交易有关的损益。收益数字也可能根据基础代币，报价代币和用于流动性挖矿支付的代币的价值的相对变化而波动。

### 我一定要使用Humminngbot交易机器人才能参与流动性挖矿吗？

不。您可以使用自己的交易机器人和策略进行流动性挖矿。

对于没有自己的交易机器人的一般用户群，可以使用Hummingbot进行流动性挖矿。
