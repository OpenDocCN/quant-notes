# 吹爆！这可能是B站最完整的（Python＋机器学习＋量化交易）实战教程了，花3小时就能从入门到精通，看完不信你还学不到东西！ - P7：第07节-事件驱动的交易策略和实施 - 凡人修AI - BV1Yx4y1E7LG

大家好，今天的第五节课，我们主要讨论的是传统量化交易策略和Python，的实现，那么我们分为以下几块来简单介绍，第一块是even driven training。

strategies和implementation，也就是我们会简单地介绍，事件驱动交易的策略以及框架，以及最后怎么样具体实施，那么这个是我们量搭建量化交易平台，不可或缺的一个步骤。

我们会将很多的class或者abstract class啊联合在一起，那么这个作为我们一整个交易平台，或者说交易系统的呃，所有的object的一个基础，那么接下来我们所有的量化交易的策略。

都是在中间的一个叫strategies，点PY和portfolio，点PY中override以实现不同的交易策略，那么第二点是我们会运用我们第一步，我们呃build好的事件驱动的交易框架来进行统计。

交易策略，也就是上面提到的，把strategies这个class给重写嗯，并且做几个简单的实施，那么第一个是moving average trade，就是移动平均交易，那么第二个是嗯。

利用我们之前简单介绍过的一些机器学习，像啊logistic regression，或者是LDAQDA和SBM，就support vector machine进行一次回归的预测交易。

那么第三个是采用一对儿嗯，股股票equity的配对敲交易，Pair training，那么来构造我们上一节课讨论过的啊，使得我们的长差是啊stationary的。

并且是啊mean reverting就是均值回复，那么第三块内容是做参数的最优化，那么是基于我们第二部的统计模型嗯，中间有很多参数，比如说啊string creature。

regression中的惩罚项C，那么应该取多大，包括像啊s b m support vector machine里面的几个参数，第一个是我们的soft margin，也就是软边界的。

我们能够承受多少的错分率，或者是像ridge regression，the sore regression的啊，惩罚项应该对每一个COEFFICI惩罚多少等等，这些参数我们都需要进行最优化。

那么介绍两种方法，第一种是cross validation，交叉验证，那么第二种方法是research，就是网格搜索，那么让我们接下来来看一下我们的第一步，也就是1even driven的这个交易框架。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_1.png)

那么在我们搭建事件驱动方法的，回测系统的时候，我们有几个点PY组件就是py class，需要我们建立，第一个是event，称为事件，这个事件呢，是我们事件驱动交易系统的一个基本元素，那么它包含几种的啊。

世界就是event，第一个是市场叫market event，那第二个是信号叫signal event，那第三个呢是订单叫order，那第四个是填充，也就是feel。

就是我们的一个订单额到达到了exchange的时候，那么他会选择如何来啊，对我们的订单进行fail，那么这些事件呢，在我们的一整个我们所有的information信息都是嗯，包含在我们的event中。

并且在下面的class之间进行信息的传递，那么event u顾名思义，就是我们上面的事件的一个队列，因为我们在不同的时刻都会有不同的啊，事件被创造，那么就应该存储在一个Q中。

由下面的strategy和portfolio，甚至是啊execution进行读取，那嗯接下来一个是叫data handler，它是一个啊抽象基类，那么适用于处理呢历史或者是实时的数据的。

那么在每一个hit line上呢，嗯data handle了，会从我们上面的event q中对数据进行抽取，抽取之后嗯，给后面的strategy点啊，和portfolio的class进行调用。

那么当市场有就下一秒如果有新的呃，嗯historical的data point进来，那么data handle了会对我们的这个event q进行update，也就是提到的。

在每个headline上呢会创造一个新的market event作为存储，那么我们接下来的strategic for folio。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_3.png)

会通过data handle进行读取，那下一个的class呢叫strategy，也是一个抽象类，那么像我们啊我们之前的概述说过，我们接下来我们所有的交易策略，都是在strategy中进行修改。

那么在我们搭建平台的时候，strategy呢先设为一个抽象类，那么根据后面不同的我们的策略，对它进行override，那么strategy呢。

会通过我们data handler里面提供的market data，进行数据分析，并产生相应的signal，也就是交易信号，那么这个交易信号呢最终是由这个portfolio。

就下面这个class进行使用的，所以这个signal event顾名思义得包含股票代码，得告诉portfolio它是哪一只股票，并且告诉呢我们交易是是long还是SHT嗯，以及stand嗯。

一个时间的这个stem。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_5.png)

一个时间点等等等等，接下来的这个strategy呢，是来处理相关的订单的层次，并且呢这个就是strategy的位置，那么它同时呢也执行风险管理，也就是当strategy产生交易信号之后。

portfolio会对我们的啊，holding和我们的现在current的价值进行计算，并且呢会对我们的这一整个策略，进行实时监控，算出我们的部门风险，也就是VR，还有投送规模。

以及我们的啊回撤就是draw down和method，DRAWDOWN和draw down duration，这都是我们上一节课提过的，这几个衡量风险的参变量。

那么嗯接下来呢这个portfolio就投资组合呢，会根据需要从我们上面的event u中抽取signal event，并且呢会生成即将要添加队列的嗯order event。

那么后面会把这个order event传送给execution。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_7.png)

那么进行fail，那接下来这个execution handler，就会从我们portfolio中得到我们的order event，并且与经济上也就是broker进行连接。

那么它从我们的队列中接收order event，并且执行他们，那么一旦执行之后呢，就会创建相应的field event，会发送给发送给我们的，Excuse handler。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_9.png)

那么来最终结算我们的收益，那么back test呢，也就是将上面我们提到的这所有的class。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_11.png)

一个动态的aggregate起来，那会产生最后产生相应的结果，所以back test是我们这一整个事件驱动，最后的执行文件，就是这个back test。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_13.png)

那么接下来让我们先来看一下event这个class。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_15.png)

那event里面包括我们上面提到过的四种event，首先market event是最好理解的，它是嗯可以引发我们的这个strategy，也就是market event呢传送到我们的strategy中。

那么由strategy产生新的交易信号。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_17.png)

那么strategy呢也就利用了我们的这个market market event，也就是market data会产生相应的交易的signal event。

那么这个signal event呢传送到portfolio中，所以需要包括我们的strategy的id，还有我们到底是哪一条ticker，那么是什么时间，以及我们交易的方向和这个stress强度。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_19.png)

那么fill fill event呢，是由嗯execution收到我们的这个oral event之后呢，会从broker中return一个信号，返还给我们的execution来计算。

那么包括如下这几个啊。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_21.png)

features就性特征，那么order event呢是是我们的呃，strategy和portfolio产生之后呢，送给我们的exexecution system。

那由broker读取之后转换成fill event，所以它应该包括我们的symbol，也是我们的ticker，还有嗯older type到底是买还是卖。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_23.png)

然后数量包括direction。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_25.png)

那接下来呢这些代码就是event啊。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_27.png)

Market event，signal event嗯，order event和failed the event的具体的嗯。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_29.png)

class代码的写法，那么接下来这些代码呢会啊发给大家。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_31.png)

那么呃主要呢主要其实都是定义。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_33.png)

每一个他们带的feature。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_35.png)

那接下来要介绍的是data handler啊。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_37.png)

data handler我们上面说过，他是一个，它是一个包含了一个event q和别的数据处理。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_39.png)

那么主要呢会将historical data或者是data from website，进行读取，读取之后呢，把它们存，把这些呃读好的一行一行的data，转换成我们上面提过的monkey event。

那么接下来strategy会对data handle的Q中的market，event进行读取，最后进行数据分析，那么data handle主要有两种，一种是from website。

就与网页或者是一些嗯数据库进行连接的，那么还有一种是从我们本地的历史数据中读取，那么我们这边利用的是historical啊，csv data handler就是从我们本地数据进行读取。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_41.png)

那么它会包含如下几种方法，第一种叫做呃get here嗯，get last bus和get get last bar两种，一种带S都不带S，那么都是用于呢获取我们的历史数据。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_43.png)

那么嗯后面带daytime和value的，就是获得近期历史数据的时间，以及他们的price，那么还有一种方法呢是进行update，就是当我们下一下一分钟。

或者是下一天有新的一个historical data进来之后呢。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_45.png)

要创造一个新的market event，并且加入到我们的队列中，所以我们需要一个update boss这样的一个方法。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_47.png)

那么呢因为data handler处理的是market event，所以我们需要从event中把market event啊import进来。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_49.png)

那么这个是我们接我们的data handler的嗯。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_51.png)

abstract就是抽象类，那么接下来呢是具体的执行过程。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_53.png)

那么initial也就初始化是定义这些啊特征。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_55.png)

那么呢嗯我们要将这个csv files打开。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_57.png)

那么打开之后我们要定义的是column的名字。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_59.png)

并且呢对所有的symbol进行循环添加。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_61.png)

根据id添加到不同的队列中。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_63.png)

那么我们要get上面提到的GALABUS，就是最后一个历史点和最后N个历史点。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_65.png)

Latest bus。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_67.png)

那么嗯最后历史点的时间和最后历史点的price。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_69.png)

那么嗯或者是最后N个的历史点，那么我们的default是N，那么当N比如说取五的时候。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_71.png)

也就是最后五个点，那么最后一个方法呢是update bs。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_73.png)

也就是当有新的历史数据进来之后，我们把它添加到啊队列的最尾端。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_75.png)

那么接下来的一个方法是最重要的strategy，当然此处的strategy是一个抽象类，是一个空的，因为我们之后是根据不同的啊，不管是统计也好，还是时间序列也好的交易策略进行具体的复写。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_77.png)

strategy呢，是封装所有市场数据的一种计算方法，那么它的output呢是产生一种建议性的signal，也就是signal event，那么最终把它传送到portfolio object中来。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_79.png)

最后对跟交易所进行连接，所以这里是一个啊strategy的一个框架。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_81.png)

那么主要的方法呢，就是这个calculate signal的这个方法。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_83.png)

那么根据我们不同的统计模型进行implement。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_85.png)

那么接下来我们要介绍一个最大的class。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_87.png)

也就是PERFOLIO，那么在做PFOLIO之前呢。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_89.png)

嗯我们先定一个它的小类叫performance，那么performance主要是有两个函数，第一个是提供我们的sharp ratio，一个是提供捉down的分析。

也就是呃performance函数呢是在portfolio的最末端，就是当我们呃产生了交易信号。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_91.png)

并且对交易所发送信号之前。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_93.png)

我们会计算一下我们的这个strategy，它的SEPARATIO有多高。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_95.png)

那我们的draw down大概是多少，是进行一个同步的风险分析，那么呢它对我们实行实现交易，是没有任何影响的，只是同步的做一个风险的output，让我们实时监控我们的交易策略的风险。



![](img/fb01e1a2b45df9d1f60d5c935f0301d2_97.png)

那在上一节课。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_99.png)

我们已经提过这个sharp ratio的计算，包括DRAWDOWN的计算。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_101.png)

那么此处呢调用的代码跟上一节课是类似的。

![](img/fb01e1a2b45df9d1f60d5c935f0301d2_103.png)