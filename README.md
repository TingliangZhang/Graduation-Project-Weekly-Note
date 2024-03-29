# 研究日志-张庭梁

 

## 2019年11月24日星期日  

本周从芬兰比赛回来，开始工作：

 

本周周报暂时使用word（由于主要是调试工作），下周将换成Markdown或者Latex写，方便之后整理成正式论文。

 

配置了毕业论文模板，并建立了GitHub Repo用于记录工作和撰写论文：

https://github.com/TingliangZhang/BachelorThesis

 

配置并巩固了AD19的用法，用学习笔记做了一个PPT（太大就不上传了），顺手做了一个教学视频，下周放到视频网站上备忘。

 

购买了Intel 8265NGW 无线网卡模块以及配套天线，并买了三台Nvidia Jetson NANO Dev kit，在这些硬件平台的基础上着手搭建实验平台。

近一周配置了Jetson开发环境，遇到的困难及解决办法如下。

 

Jetson Nano开发指南：

https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit

Tutorial

https://www.jetsonhacks.com/2019/06/07/jetson-nano-gpio/

https://www.jetsonhacks.com/2019/04/25/jetson-nano-run-on-usb-drive/

一些库

https://github.com/JetsonHacksNano/ServoKit

**烧写镜像**

[SD Memory Card Formatter for Windows](https://www.sdcard.org/downloads/formatter_4/eula_windows/)

[Etcher](https://www.balena.io/etcher)

**启动**

**python**

pip改镜像源：

windows上在 C:\Users\ZTL\pip\pip.ini 中写入

 [global]

 index-url = https://pypi.tuna.tsinghua.edu.cn/simple

 

**NLP**

https://cloud.google.com/speech-to-text/docs/quickstart-client-libraries?hl=zh-CN#client-libraries-install-python

 

Powershell:

$env:GOOGLE_APPLICATION_CREDENTIALS="C:\Users\ZTL\pip\My First Project-49d67a9713b6.json"

CMD:

set GOOGLE_APPLICATION_CREDENTIALS=C:\Users\ZTL\pip\My First Project-49d67a9713b6.json

 

 

pip install pyaudio

error: Microsoft Visual C++ 14.0 is required. Get it with "Microsoft Visual C++ Build Tools": https://visualstudio.microsoft.com/downloads/

 

解决方法：https://stackoverflow.com/questions/52283840/i-cant-install-pyaudio-on-my-python-how-to-do-it

https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio 下载需要的版本 直接

pip install .\PyAudio-0.2.11-cp37-cp37m-win32.whl

 

 

获取Python多线程的返回值(give up)

https://blog.csdn.net/u012050154/article/details/80032072

 

 

**API汇总**

 

 

pygame

example:

https://gist.github.com/claymcleod/028386b860b75e4f5472

 

google Cloud Speech-to-Text

https://cloud.google.com/speech-to-text/

**可视化**

http://bl.ocks.org/dbuezas/9306799

饼状图

 

https://github.com/d3/d3/wiki/Gallery

D3

HTML可视化

 

Pie charts labels

http://bl.ocks.org/dbuezas/9306799

Updated:Pie Chart Labels with missing data

http://bl.ocks.org/dbuezas/9572040

 

MAKE A WORD CLOUD

https://worditout.com/word-cloud/create

https://www.wordclouds.com/

Josefin Sans

Python用户指南

https://github.com/TingliangZhang/susi

下载文件包并解压

 

配置gcloud API：

https://cloud.google.com/speech-to-text/docs/quickstart-client-libraries?hl=zh-CN#client-libraries-install-python

 

在搜索里搜path

添加环境变量并应用(记得点确定并重启powershell)：

GOOGLE_APPLICATION_CREDENTIALS

C:\Users\Tina\Desktop\susi\Susi-4f9ca6baf25d.json

![1](Fig/1.png)

 

[安装并初始化 Cloud SDK](https://cloud.google.com/sdk/docs/)

（需要我的Google账号）

 

> pip install --upgrade google-cloud-speech
>
> pip install numpy

 

python3.7运行controller.py

 

## 2019年11月29日星期五 

颜心裴学长讲解了毕设论文的算法原理，现在的想法是先做GM的方法，然后做分布式潮流，有时间再做电价，这些部分的展示效果最好，难度也是逐渐提高（电价部分虽然不严谨，其实和gm的出力搭界情况一样，只是线路搭界过多就保证不了收敛）。非线性报价不做了，麻烦而且没特别的展示效果。
 现在主要是毕设开题要准备，打算做出GM的分布迭代，然后在预先给定权重的情况下展示收敛过程。

 

目前需解决的问题主要包括算法的迁移、通信架构的选择和可视化界面的设计。

其中，因为目前用的ARM核Ubuntu无法导入Matlab库，代码不能继续沿用Matlab代码，而是以学长的算法思路为依据编写Python/C。

通信暂时想使用双向通信信道，比如使用Ethernet协议来写，看情况决定是否使用交换机。

可视化部分最好还是要能体现潮流和出力随迭代次数的即时变化

 

 

## 2019年12月1日星期日

目前进行了一部分代码迁移的工作，先从Matpower迁移到了Pypower，感觉自己Python功力不足，准备在下周五开一次Python3讲座，以此来促进自己提升Python水平。

 

## 2019年12月5日星期四

Python没搞完，明天先讲一次Latex巩固一下。

对做的方向有些迷茫，于是对共识算法和ED进行更加深入的调研和学习。

 

ED：

https://en.wikipedia.org/wiki/Economic_dispatch



共识算法：

https://yeasy.gitbooks.io/blockchain_guide/04_distributed_system/algorithms.html

 

https://zhuanlan.zhihu.com/p/33941594

 

markdown：

https://about.gitlab.com/handbook/engineering/technical-writing/markdown-guide/

 

## 2019年12月8日

有选择的阅读了新购买的几本书，包括**算法导论**、**ZooKeeper：分布式过程协同技术详解**、**分布式系统：概念与设计（第5版）** **[Distributed Systems：Concepts and Design,Fifth Edition]**、**分布式机器学习：算法、理论与实践**等，也思考在未来的硬件架构中怎样搭建最合适。

在Google的过程中，无意中看到了区块链的底层算法，发现加密货币（如比特币）的底层算法是根据分布式系统来写的，觉得可以借鉴。

于是转而进行用于分布式系统核心技术的相关调研。

### 一致性问题

一致性问题是分布式领域最基础、最重要的问题，也是半个世纪以来的研究热点。

随着业务场景越来越复杂，计算规模越来越庞大，单点系统往往难以满足高可扩展（Scalability）和高容错（Fault-tolerance）两方面的需求。此时就需要多台服务器通过组成集群，构建更加强大和稳定的“虚拟超级服务器”。

任务量越大，处理集群的规模越大，设计和管理的挑战也就越高。谷歌公司的全球搜索集群系统，包括数十万台服务器，每天响应百亿次的互联网搜索请求。

集群系统要实现一致性不是一件容易的事。不同节点可能处于不同的状态，不同时刻收到不同的请求，而且随时可能有节点出现故障。要保持对外响应的“一致性”，好比训练一群鸭子齐步走，难度可想而知。

### 一致性的要求

规范来看，分布式系统达成一致的过程，应该满足：

- 可终止性（Termination）：一致的结果在有限时间内能完成；
- 约同性（Agreement）：不同节点最终完成决策的结果是相同的；
- 合法性（Validity）：决策的结果必须是某个节点提出的提案。

### 共识算法

共识（Consensus），很多时候会见到与一致性（Consistency）术语放在一起讨论。严谨地讲，两者的含义并不完全相同。

一致性的含义比共识宽泛，在不同场景（基于事务的数据库、分布式系统等）下意义不同。具体到分布式系统场景下，一致性指的是多个副本对外呈现的状态。如前面提到的顺序一致性、线性一致性，描述了多节点对数据状态的共同维护能力。而共识，则特指在分布式系统中多个节点之间对某个事情（例如多个事务请求，先执行谁？）达成一致看法的过程。因此，达成某种共识并不意味着就保障了一致性。

实践中，要保障系统满足不同程度的一致性，往往需要通过共识算法来达成。

共识算法解决的是分布式系统对某个提案（Proposal），大部分节点达成一致意见的过程。提案的含义在分布式系统中十分宽泛，如多个事件发生的顺序、某个键对应的值、谁是主节点……等等。可以认为任何可以达成一致的信息都是一个提案。

对于分布式系统来讲，各个节点通常都是相同的确定性状态机模型（又称为状态机复制问题，State-Machine Replication），从相同初始状态开始接收相同顺序的指令，则可以保证相同的结果状态。因此，系统中多个节点最关键地是对多个事件的顺序进行共识，即排序。

*注：计算机世界里采用的是典型的“多数人暴政”，足够简单、高效。*

### 问题与挑战

无论是在现实生活中，还是计算机世界里，达成共识都要解决两个基本的问题：

- 首先，如何提出一个待共识的提案？如通过令牌传递、随机选取、权重比较、求解难题……等；
- 其次，如何让多个节点对该提案达成共识（同意或拒绝），如投票、规则验证……等。

理论上，如果分布式系统中各节点都能以十分“理想”的性能（瞬间响应、超高吞吐）稳定运行，节点之间通信瞬时送达（如量子纠缠），则实现共识过程并不十分困难，简单地通过广播进行瞬时投票和应答即可。

可惜地是，现实中这样的“理想”系统并不存在。不同节点之间通信存在延迟（光速物理限制、通信处理延迟），并且任意环节都可能存在故障（系统规模越大，发生故障可能性越高）。如通信网络会发生中断、节点会发生故障、甚至存在被入侵的节点故意伪造消息，破坏正常的共识过程。

一般地，把出现故障（Crash 或 Fail-stop，即不响应）但不会伪造信息的情况称为“非拜占庭错误（Non-Byzantine Fault）”或“故障错误（Crash Fault）”；伪造信息恶意响应的情况称为“拜占庭错误”（Byzantine Fault），对应节点为拜占庭节点。显然，后者场景中因为存在“捣乱者”更难达成共识。

此外，任何处理都需要成本，共识也是如此。当存在一定信任前提（如接入节点都经过验证、节点性能稳定、安全保障很高）时，达成共识相对容易，共识性能也较高；反之在不可信的场景下，达成共识很难，需要付出较大成本（如时间、经济、安全等），而且性能往往较差（如工作量证明算法）。

*注：非拜占庭场景的典型例子是通过报数来统计人数，即便偶有冲突（如两人同时报一个数）也能很快解决；拜占庭场景的一个常见例子是“杀人游戏”，当参与者众多时很难快速达成共识。*

### 常见算法

根据解决的场景是否允许拜占庭错误情况，共识算法可以分为 Crash Fault Tolerance (CFT) 和 Byzantine Fault Tolerance（BFT）两类。

对于非拜占庭错误的情况，已经存在不少经典的算法，包括 Paxos（1990 年）、Raft（2014 年）及其变种等。这类容错算法往往性能比较好，处理较快，容忍不超过一半的故障节点。

对于要能容忍拜占庭错误的情况，包括 PBFT（Practical Byzantine Fault Tolerance，1999 年）为代表的确定性系列算法、PoW（1997 年）为代表的概率算法等。确定性算法一旦达成共识就不可逆转，即共识是最终结果；而概率类算法的共识结果则是临时的，随着时间推移或某种强化，共识结果被推翻的概率越来越小，最终成为事实上结果。拜占庭类容错算法往往性能较差，容忍不超过 1/3 的故障节点。

此外，XFT（Cross Fault Tolerance，2015 年）等最近提出的改进算法可以提供类似 CFT 的处理响应速度，并能在大多数节点正常工作时提供 BFT 保障。

Algorand 算法（2017 年）基于 PBFT 进行改进，通过引入可验证随机函数解决了提案选择的问题，理论上可以在容忍拜占庭错误的前提下实现更好的性能（1000+ TPS）。

*注：实践中，对客户端来说要拿到共识结果需要自行验证，典型地，可访问足够多个服务节点来比对结果，确保获取结果的准确性。*

### 理论界限

科学家都喜欢探寻问题最坏情况的理论界限。那么，共识问题的最坏界限在哪里呢？很不幸，在推广到任意情况时，分布式系统的共识问题无通用解。

这似乎很容易理解，当多个节点之间的通信网络自身不可靠情况下，很显然，无法确保实现共识（例如，所有涉及共识的消息都丢失）。那么，对于一个设计得当，可以大概率保证消息正确送达的网络，是不是一定能获得共识呢？

理论证明告诉我们，**即便在网络通信可靠情况下，一个可扩展的分布式系统的共识问题通用解法的下限是——没有下限（无解）。**

这个结论，被称为“FLP 不可能原理”。该原理极其重要，可以看做是分布式领域里的“测不准原理”。

*注：不光分布式系统领域，实际上很多领域都存在类似测不准原理的约束，或许说明世界本源就存在限制。*



**下周准备将注意力集中在致力于解决Paxos 问题的Paxos 算法与 Raft 算法上。**

*Paxos 问题是指分布式的系统中存在故障（crash fault），但不存在恶意（corrupt）节点的场景（即可能消息丢失或重复，但无错误消息）下的共识达成问题。这也是分布式共识领域最为常见的问题。因为最早是 Leslie Lamport 用 Paxos 岛的故事模型来进行描述，而得以命名。解决 Paxos 问题的算法主要有 Paxos 系列算法和 Raft 算法。*

**另外快要开题了，我也着手准备开题报告和找英语文献翻译了，工作会在Github的两个Repo里面更新：**

周报链接：https://github.com/TingliangZhang/Graduation-Project-Weekly-Note

论文链接：https://github.com/TingliangZhang/BachelorThesis





## 2019年12月15日

https://book.8btc.com/books/1/gaosheng_blockchain_report/_book/5/1.html

本周主要进行区块链相关学习，并进行了国创立项和挑战杯报名。

区块链可以建立一个去中心化的能源市场。在最具颠覆性的场景中，我们认为结合区块链和通信技术可以促进数百万的参与者之间更安全的交易和支付，为一个去中心化能源市场赋能。简单地说，区块链天然的分布式特征可以让分布式的能源用户无缝地将电力卖给附近的消费者，实现真正的本地化能源生产和消费。

在接下来的数十年中，我们预计国家电网会从现有的中心化公共事业模型向着融合更多去中心化资源、实时报价系统和更紧密匹配需求和供应的方向进化。这个进化的核心是通过智能电表、智能装备、可再生能源和能源储存的结合实现电网的现代化，我们预计这个过程中会产生数千万甚至上亿个去中心化节点，这些节点不仅能够收发数据，也能执行P2P交易。我们认为区块链技术将在促进沟通、交易和数百万个交易对手方之间的安全性方面发挥重要作用。在我们看来，区块链会带来一个去中心化的能源市场，不仅极大地推动分布式能源方面的投资活动，也会将25-70亿美元的电力收入再分配给新的市场参与者（也就是说不再是给公用事业公司）。



https://link.springer.com/article/10.1007/s00450-017-0360-9

The increasing amount of renewable energy sources in the energy system calls for new market approaches to price and distribute the volatile and decentralized generation. Local energy markets, on which consumers and prosumers can trade locally produced renewable generation directly within their community, balance generation and consumption locally in a decentralized approach. We present a comprehensive concept, market design and simulation of a local energy market between 100 residential households. Our approach is based on a distributed information and communication technology, i.e. a private blockchain, which underlines the decentralized nature of local energy markets. Thus, we provide energy prosumers and consumers with a decentralized market platform for trading local energy generation without the need of a central intermediary. Furthermore, we present a preliminary economic evaluation of the market mechanism and a research agenda for the technological evaluation of blockchain technology as the local energy market’s main information and communication technology.



- DOI  https://doi.org/10.1007/s00450-017-0360-9

## 2019年12月16日

通过和坏人（贵系博士）的谈话，发现普通的去中心化分布式算法就可以满足电力网里的需求，没必要上区块链的PoW或者[PoS](https://en.wikipedia.org/wiki/Proof_of_stake)。

由于电力物联网中所有的电表（出力/能耗证明）都是经过官方认证的，所以发出的报文经过证书加密，收到的报文首先验证是否符合规则，不符合的舍弃，所以进入算法的数据本身一定是可信的，不存在拜占庭问题（恶意提交的错误信息），只可能数据丢失。不需要用区块链解决拜占庭问题。

所以最终还是需要仔细搞搞分布式算法。

上两周搞的区块链用不上了......
