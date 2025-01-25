# 吹爆！这可能是B站最完整的（Python＋机器学习＋量化交易）实战教程了，花3小时就能从入门到精通，看完不信你还学不到东西！ - P26：第26节-机器学习于量化交易中的应用IV - 凡人修AI - BV1Yx4y1E7LG

大家好，欢迎收听Python机器学习与量化金融的第12堂课，那么我们第12堂课呢，主要讲的是机器学习的第四部分，那也是机器学习的最后一个部分的内容了，那么机器学习这个章节，我们主要是介绍。

我们如何将前面几个章节介绍的，机器学习的方法等等，运用到这个真正的logo training中，那么会run出我们呃based on历史数据的training，包括真实数据的testing。

那么run出我们的year return，然后包括active curve，包括sharp ratio跟certain erratio等等，还有捉到一些啊测评数据，那对我们的交易策略进行评估。

那么这堂课过后呢，接下来的十三十四十五是主要介绍期权啊，期权期货产品的，因为大家知道，其实嗯我们之前这个Python课程，主要介绍的其实都是一些序列模型，或者是一些回归模型和预测模型等等。

那么这些呢主要做的是这个统计套利，那么在传统的这个衍生品市场呢，我们做的还有一方面，其实也是主要业务，其实是定价套利，也就是说像option future呃，swap等等。

那么我们系统呢会有一个理论的定价，那么当我们发现market value，那如果是over price了，那么这个时候我们就shot，那如果相反是under price的话，那这时候我们就log。

那么我们后面要介绍的是定价套利模型，那我们截止到12堂课之前的内容呢，主要是统计套利模型，所以我们结束完这堂课，我们就move forward到pricing model中去。

那么让我们来看一下这堂课的大纲内容。

![](img/4aca8059f57b56ac1238e8675968ee29_1.png)

那么首先呢我们会介绍这个Python中，实现实盘量化交易的一个嗯module，那么是一个开源的一位大神写的嗯，在GITHUB上可以破下来，叫qs trader。

那qs trader主要完成的任务呢有两点，第一个呢是它模拟了一个交易系统，就是exchange的一个功能，那么我们作为这个client，那像我们的这个exchange发送，我们想要的订单。

想要的order，那么这个exchange呢根据实时的数据帮我们fail order，并且把order的情况呢send back给我们，那我们再run我们下一步的model或者是prediction。

那嗯qs trainer，另外一个呢做的主要是啊做back testing，也就是说嗯，Q a stranger，能够自动的帮我们生成一个tr sheet。

那包括我们这个historical的performance，那跟我们的benchmark portfolio进行比较，并且呢会给出我们这个portfolio各种的statistics。

比如说这个啊annual return啊，比如说啊这个sharp利率啊，比如说一个SOTA啊，ratio啊，比如说嗯还有他的volatility啊，嗯嗯包括他的maximum。

draw done和draw done duration等等，包括每年的这个return的分析啊，分析的这个柱状图啊是一个很漂亮的，作为我们这个量化金融分析的时候，我们前台交易都会用到的一个报表。

那么qs trader呢自动帮我们实现了，所以科二吹的不管是做回测还是做实盘交易，都是非常常用的一个啊，应该说是线下的API，那在真正工作中的话，我们每一家银行自己都会写一个。

类似于cos strator，那么对于大家啊这个业余与search的话，那么用这个开源的qs trader就好了，那么我们主要介绍啊以下几种交易模型，其实也都是我们之前接触过的。

那么我们前面介绍过时间序列模型，我们介绍过arena model，介绍过garch model，那么都是一些简单的如何做这建立model，那么在这里呢我们会用ORIGA加GARCH模型呢。

进行这个stock market的实盘交易，要么呢主要用的是R，那原因也很简单，之前提到过这个R的话，做时间序列的这个包是最完善的，那么下一个模型呢，我们会讲基于谐振的这个pair trading。

那么我们在之前pair trading已经提了无数次了，也就是通过这个谐振信，我们得到了这个长差，那么残渣会满足均值回复，那均值回复呢就有一个非常好的特性，那当然现在count level低于这个嗯。

回复均值线以下的时候，那么认为他会回复到均值线，那这个时候呢我们就买入，那我们可以赚中间的这个spread，那反之如果这个时候他在均值线以上的话，那我们认为它finally会捉不到。

所以这个时候我们提前shut，那来这个规避他作down的这个风险，那这个呢就是基于谐振性的这个，pair trading的想法原理，那么在这里呢。

我们用cover trader进行一个dynamic的嗯，基于谐振性的一个pair trading，那么这个谐振性有一个问题，也就是说配对交易的时候。

我们默认我们在一个固定的historic和window中，我们进行这个回归，我们发现我们的这个PEETRADING的贝塔，也就是hedge ratio应该是多少，比如说1。2，但是呢这个还是ratio。

其实真实情况下，他是每天都要在随着时间变化的，这个regression line不可能是一条固定的直线，那么呃时间不同呢，这个regression line的倾斜角度，一定会因为我们新进的数据而改变。

所以这个时候呢，我们用这个common filter，来改善上面的这个QUINTEGRATION，那come on filter呢。

其实我们的state也是linear regression model，但是这个时候的regression coefficient，它是随时间变化了。

所以我们会update我们的这个嗯regression的profession，达到一个这个动态啊，pair trading的一个嗯一个想法。

那么接下来一个呢是这个基于supervisor learning，也就是我们说的常说的这个比较，narrow的机器学习，也就是说基于我们一条时间序列，以及他自己的lag。

我们通过这个呃嗯prediction model，我们predict他明天或者是未来几天内，它到底是up还是done，那我们进行这个classification，那所以呢在这种监督学习之下。

比如说有uh support vector machine啊，Uh linear discriminate analysis，U，还有一些树形模型，比如说这个random forest。

比如说这个梯度啊，gradient boosting tree等等等等，那么都可以用在我们这个第五条，那么第五条跟前面的区别是，前面的这些模型都是predict，第二天它的return值是多少。

那么第五个呢就是我们这个supervised learning呢，我们只predict啊，他第二天到底是属于哪一类，属于上哪类还是下跌类，所以呢想法跟前面不同，而且这个第五类嗯。

我们用的是intro data data，也就是说我们的data精确到minutes，精确到分钟数，所以呢对我们的这个主机的CPU要求更高，那么前面两三类呢。

RUREGRESSION的时候相对啊没有这么heavy1些，那么接下来让我们啊对，先对这个qs trader做一个介绍。



![](img/4aca8059f57b56ac1238e8675968ee29_3.png)

首先呢让我们来介绍一下qs trader这个module，那么qs trader呢是一个网上开源的，在GITHUB上嗯，一个大神Python大神自己写的，那么我把网址链在这里了。

那么待会我们会go through一下他的website，那么首先呢qs trader是做什么的啊，大家还记得我们第五节课的时候啊，Long time ago，我们提到了我们的一个交易系统。

当时可能大家会觉得那堂课很confusing说，哇交易系统东西这么复杂，我自己要怎么写，其实不用很紧张，就是这个一般的交易系统，在银行中也都是由前台的interface developer写的。

那么我们只要懂得每一个交易系统之间的接口，我们需要define什么variable，然后呢，我们每一个这个interface之间的相互dependency，是什么关系就好了，所以对于第五堂课的内容呢。

大家不需要知道每一个step具体怎么写，具体怎么实现，看起来很繁琐，那么大家只要明白我们每一个对于每一个class下，那么它有什么呃，都define了哪一些variable。

那每一个class的作用是什么，然后每一个class之间，他们的information是应该怎么传递的就好了，所以呢在我们第五节课提到的这个交易系统，cos strator呢帮我们实现了。

所以我们不需要自己写，我们只需要调用就好了，那么大家还记得我们一开始define就是一个event，首先呢我们要向不管是向我们的strategy，还是像我们的交易系统还是交易系统，sm back回来。

这些所有的信息传递都是由这个event来封装的，所以说呢event它代表的是这个message of data，那像一条data进来之后，我得知道它的price，我得知道它的value有多少。

然后呢我得知道这条呃，那如果比如说是sin exchange的，那exchange得知道你这一条线过来，你到底是要long还是要shot，那exchange stand bet回来。

我得知道我这个我这一条啊，request呃，被我丢回来之后呢，他到底是被fail了还是被partially fail了，还是被cancel了等等等等，那么它它在下面呢会包括这个tick event。

也就是ticker那bar event signal event，那这是我们之前就已经介绍过的，就是一条历史数据进来，我们会把它包装成这个signal event。

然后order event是send给exchange的，那fail event是exchange send back回来的，那position呢其实是嗯也是一个class，那么它封装的是什么呢。

是封装了所有的带着这个open position的这些data嗯，然后portfolio呢这一项呢其实是一个，相当于是我们呃对于一条strategy来说。

我们比如说这个时候决定这一条historical data进来，我对它执行的操作是我们要log，那这个时候呢，我们的这个strategy就会像我们这个portfolio，Send。

我们这些event cu把它们排在一个队列中，那么由portfolio进行处理，最后发送给这个exchange，就叫做这个dea handler，那么所以PERFORMNIO呢。

我们可以理解成它是中间的一个媒介，那么它包含了啊，所有我们要向exchange place传递的这些信息，包括pfolio handler，那么price handler他们这些所有的handler。

包括PO6，自己本身呢，都是作为我们跟exchange之间信息传递的一个媒介，那strategy呢是我们一整个交易系统中，最核心的部分了，也就是我们前面所有构造好的东西，都由strategy吸收。

包括我们这个signal event，那么进了strategy之后呢，由strategy决定，我最我对这条signal event，我们采取的到底是short还是long，还是不采取任何措施。

所以strategy呢顾名思义，也就是把我们的策略实现的地方，我们可以在strategy里实现最简单的，比如说啊这个main variance optimization呢。

可以在strategy里实现我们的pair trading，或者在里面实现我们利用这个random forest，那么对我们的这个data进行啊class的这个prediction。

可以PREDATION它到底后面未来5分钟内，它到底是up and down，并且呢对对我们的这个prediction呢，进行进行这个呃hit，所以呢它它的意思呢就是contain了。

我们这个阿尔法generation code，那么阿尔法generation呢，嗯意思呢其实就是厂商阿法嘛，阿尔法其实是access return的意思。



![](img/4aca8059f57b56ac1238e8675968ee29_5.png)

也就是一个盈利的一个strategy的来源，那么它还包含着如下的这些class，那么position seor呢，我们上面提到跟这个PFOLIO嗯。

portfolio跟portfolio handler呢是在一起的，那risk manager呢，risk manager其实是对这个pfoo handler跟position。

进行一个monitor的东西，那它最后呢是会generally出一些statistics，那对于from death race manager来说，他需要做到VR，他需要知道volatility。

他需要知道return，他需要知道daily piano等等，然后exexecution handler呢，其实是一个跟这个broker后面叫exchange啊，一个产生这个信息交换的地方。

所以呢我们把这个order send到呃execution handler，那由这个execution呢，它来决定我们应该是如何fail的，所以在这个curse strator里面。

这个class其实就扮演着一个这个交易中心这样的，一个角色，那statistics跟这个rise manager很像，也是产生我们需要的，就是我们这条策略要评估它，那么它会产生各种各样的数据报表。

那么呢在这个QSSTRATOR里面，他最著名的就会产生这个tear sheet，那是一个有助于不管是做fundamental的人来说，还是做矿trading的人来说。

所有的useful information都在这个TLC里面了，主要是来这个判断我们的这每，我们每一条策略的这个performance到底怎么样，那back test呢就是encapsulate。

也是封装我们这一整个event driven的这个QSSTRATOR，module的一个嗯一个class，那么我们最后呢其实只要call这个bad test，那就会把前面所有的东西它有机地结合在一起。

并且把我们的这个output，也就是我们的tear sheet啊给run出来，那我们接下来看看我们这个qs trader的网页，那么要提醒大家一下的是。

这个qs trade的run呢是在我们的terminal里面，也，那么对于windows来说，就是CMD就come on line，那么它并不能在我们的这个jupiter notebook。

或者是任何的id上运行，因为呃尤其是在run这个啊supervised learning的时候呢，它是一个GPU based的，最好是用GPU based的这个环境。

所以说呢我们一般都是选择在terminal上，直接扣我们的这个点，Py back test，那么直接run直接在terminal里run出我们的结果，那我们这节课会用到的数据源呢。

包括案例数据源都是来自这个纳斯达克里面的，那大家怎样输入我们这个symbol，然后后面呢在里面选这个historical line啊，就可以DOWNLO我们的这个数据。

那么它download的格式呢是这个CSB形式。

![](img/4aca8059f57b56ac1238e8675968ee29_7.png)

那我们这边来先简单的看一下，这个qs trader的这个网页。

![](img/4aca8059f57b56ac1238e8675968ee29_9.png)

那么呢它是一个如下的这个一个get up呢。

![](img/4aca8059f57b56ac1238e8675968ee29_11.png)

然后旗下呢他有这个qs trader，那在qs stray里面呢。

![](img/4aca8059f57b56ac1238e8675968ee29_13.png)

它有包括例子，就是data data里面放的，就是它下面它下面案例会用到的数据，那examples呢就是它的点PY扣，都是一些back test code。

那out呢是存放这个output file的地方，那qs trailer呢里面呢，就是主要都是他一些事例的strategy放在其中。



![](img/4aca8059f57b56ac1238e8675968ee29_15.png)

包括这边有read me啊等等等等。

![](img/4aca8059f57b56ac1238e8675968ee29_17.png)

然后这边呢是他的一些current features。

![](img/4aca8059f57b56ac1238e8675968ee29_19.png)

还有包括qs trader的一些介绍，那么呢感兴趣的同学可以阅读一下啊。

![](img/4aca8059f57b56ac1238e8675968ee29_21.png)

包括他现在遇到的有一些issue，也就是有一些exception。

![](img/4aca8059f57b56ac1238e8675968ee29_23.png)

那他可能未来expect会如何改善它。

![](img/4aca8059f57b56ac1238e8675968ee29_25.png)

那我们来看一下如何安装，那在这个installation and example usage这边嗯。

![](img/4aca8059f57b56ac1238e8675968ee29_27.png)

首先呢如果对呃，其实对于python3环境的人来说呢。

![](img/4aca8059f57b56ac1238e8675968ee29_29.png)

去掉前面的这一段内容，那由于我用的是python2。7。

![](img/4aca8059f57b56ac1238e8675968ee29_31.png)

那我们直接在command line里面，就是我们的这个terminal里面直接扣pipe这两条，那么就直接从这个呃，这个qs trader的这个website里面呢。

把我们的这个一整个package呃。

![](img/4aca8059f57b56ac1238e8675968ee29_33.png)

那个pipe pipe down下来，相当于我们的q s trader已经安装好了，那在这边呢是一个运行的示例，也就是我们首先呃make directory就是创造路径。

首先呢我们要创造在我们当前运行路径下，有一个qre state的folder，那这个folder下呢创造一个examples folder，那在这个example photo里面。

我们未来自己写的strategy，都要放在这个example folder之下，就是啊我们之后呢，就是前面的这个票号是我们这个user，然后在example里面呢。



![](img/4aca8059f57b56ac1238e8675968ee29_35.png)

也就是我们之后自己写的strategy，都得存在这个下面。

![](img/4aca8059f57b56ac1238e8675968ee29_37.png)

然后在下面的这个CD啊，data呢，也就是说啊，现在把我们的当前路径放到这个data里面去，因为我们要读取我们的data，那这次的这个data呢是在website上面直接download。

那以后如果有我们自己user，我们自己弄好的，准备好的一个，然后csv file呢我们也要存在这个当前路径，点点data下面。



![](img/4aca8059f57b56ac1238e8675968ee29_39.png)

那QS追人呢会直接从里面破，那，一般的格式呢是cs。

![](img/4aca8059f57b56ac1238e8675968ee29_41.png)

那接下来呢是这个we get we get这个函数，如果如果大家没有安装的话，其实要搜一下，比如说啊mike we get，那么we get呢要在我们自己的terminal里先装好，没有装好的话。

we get是会报错的，那么这一行的意思是说呢，直接从它这个网页里，把这个s spy点CSVDOWNLO下来，所以我们不需要在这个data里面先存一份这个，那么这条指令呢是直接帮我们download。

那这个CDQC的点examples，也就是回到我们这一块的这个路径来，因为我们要调examples里面的点PY，那么这个时候examples里面的PY呢，是叫这个名字。

也就是by and后是最简单的一个strategy，就是买入，那么只一直hold住，那么直到这个historical，historical data and的时候。



![](img/4aca8059f57b56ac1238e8675968ee29_43.png)

我们再抛出，那么乱完这这几行之后，我们在Python的command line里面call这一条，那么就会直接调用这个by and，hobad test的这个Python函数。



![](img/4aca8059f57b56ac1238e8675968ee29_45.png)

那么它呢会给我们输出如下的这些嗯。

![](img/4aca8059f57b56ac1238e8675968ee29_47.png)

这个output，那么很漂亮，那么第一个呢是我们这个strategy，在historical上，我们这个accumulative return，也就是累计的return有多少。



![](img/4aca8059f57b56ac1238e8675968ee29_49.png)

那么第二个呢是在这个历史历史的每一时刻。

![](img/4aca8059f57b56ac1238e8675968ee29_51.png)

我们的JADOWN每天的捉热down有多大，那接下来是这个monthly return，那么它都会通过这个his map给我们看，包括yearly return是一个这样如下一个柱状图。



![](img/4aca8059f57b56ac1238e8675968ee29_53.png)

那么下面呢有三个这个格子，那么第一个是比较重要的，就是这个克服克服下呢，会给我们这个total return百分比，包括shi ratio，包括这个satio ratio。

包括这个每年年化的这个volatility，我们的波动率有多大，然后呢包括我们max的就是最大的，当每一天的捉到会有多高，那做猪肉档呢能持续多长的时间，包括呢我这个每年我到底能做多少个。



![](img/4aca8059f57b56ac1238e8675968ee29_55.png)

trade等等等等，那么这个呢就是我们这个呃一个简单的。

![](img/4aca8059f57b56ac1238e8675968ee29_57.png)

包括他这个网页上的事例，那么下面呢还有别的，比如说这个moving average，cross by test的这样的呃一个例子，那么大家可以看到，其实如果用moving average的话。

那么return呢其实已经比这个s spy，也就是比嗯一个正常的band的嗯，hold的这个return来的高的多了。



![](img/4aca8059f57b56ac1238e8675968ee29_59.png)

当然他这个桌背就是这个MASMU，桌down可能会比较高。

![](img/4aca8059f57b56ac1238e8675968ee29_61.png)

然后呢这个是一个这个因为如果有benchmark，因为这时候你不再是最简单的band host。

![](img/4aca8059f57b56ac1238e8675968ee29_63.png)

所以对第一个这个表格来说会多一列，那么后面的这一列呢也是benchmark，benchmark指的是这个s spy，那么s spy我们这个band host这样的一个performance。

跟我们这个strategy。

![](img/4aca8059f57b56ac1238e8675968ee29_65.png)

performance这些statistics的比较，那么呢对于advanced的这个strategy呢。



![](img/4aca8059f57b56ac1238e8675968ee29_67.png)

大家就就override，qs trader的strategy的这个这个class就好了。

![](img/4aca8059f57b56ac1238e8675968ee29_69.png)

那我们后面会用这个代码，包括step by step的这个解释，我们这里提到的每一条strategy。



![](img/4aca8059f57b56ac1238e8675968ee29_71.png)

是如何在qs trader上实现的。

![](img/4aca8059f57b56ac1238e8675968ee29_73.png)

![](img/4aca8059f57b56ac1238e8675968ee29_74.png)

那首先呢让我们来看一下第一块，也就是最简单的策略，如何用cos trader做BTESTING，那在这边呢，主要不是让大家学习这一些特别傻的，比较难应付的策略，而是通过调用这个最简单的策略。

第一是学习这个strategy，点PY具体是怎么写的，第二呢是让大家了解这个HUASTRATOR，他自己本身是怎么FUNCTIONALIZED的，那我们先通过这个最基础的认领呢。

我们才可以step by step的写比较advanced的这个strategy，那么首先呢在这边提供三条策略，第一条呢是啊，我们只放两个，一个呢是empty，一个呢是BD，那比如说这个时候。

我认为这个equity市场是relatively，比较好的，因为其实equity市场呢跟棒的市场，可以作为两个互补的，也就是说当equity其实比较好的时候，B的生产relatively。

它就会来的比较萧条，所以呢如果我想做一条做一个简单的hatch的话，那我可以选择一部分买equity，那一部分呢买BD，那这样呢可以相对来说降低我们的风险，所以呢第一条我们选择60%的equity。

那么选择40%的的BD也就是债券，那第二条呢我想有一个这个自己portfolio manager，自己define的一个allocation，那我想做这个30%能做u s equity。

那呢就是做s spy或者做这个到JONES那分配，那么第二个呢是因为认为这个emerging market，也是新兴市场，就比如说这个亚洲市场，中国啊，HONGKONG啊等等。

那么都称为emerge market，那我们在emerge market，equities里面呢也放一些portfolio，那接下来呢还要放一些USBD，那么来规避一下风险。

那么呢再买一些这个commodity和railway day，也就是这个大宗商品和房地产，那我们有如下的这样的第二条strategy，我们对于每一条TIKER来说。

我们的这个嗯asset allocation，那作为第三条呢就比较简单粗暴了，就是对我们所有前面提到的那些ticker，我们都做这个equal weight的allocation。

那么我们的这个strategy呢是这样的，也就是说在我们一开始的时候的这个weight a sign，好啊，呃比如说equity是60%，40%是根据他的current price。

那这个时候呢通过一个月的变动，那么它们之间的这个price一定是有所改变的，所以这个时候我想保证还是60%equity，40%bt的话。

我们要做一个REBALANCE说嗯based on dollar weight，也就是这个价格的这个位贴，所以到了月底之后呢，我们会做一次调整，那SOFIANCESOF。

直到我们这个back testing结束，那可以让我们来看一下我们的，我们提我们上述提到的这三条，很简单的strategy，我们是具体是怎么写的。



![](img/4aca8059f57b56ac1238e8675968ee29_76.png)

那让大家有一个比较好的概念，那首先呢我们得写一个这个monthly rebalance run，点PY，那么这个我们这条class呢。



![](img/4aca8059f57b56ac1238e8675968ee29_78.png)

主要做的是做这个我们的这个strategy，那么我们做这个每个月based on，我们这个新的asset，它现在current的价格，那么进行这个weight的重新分配。



![](img/4aca8059f57b56ac1238e8675968ee29_80.png)

那这是我们class呢主要做的事情，那首先呢我们要define啊，Initialize，initialize什么呢，我们第一个是ticker，就是这些这些ticker的名字，那第二个呢是我们要做的。

一般cu，也就是说我们每一天有数据进来，我们得把它排成一个waiting的这样的一个Q，那么跟我们第五节课谈到的一样，我们所有的event其实都是以一个队列的形式排好，那first come。

那那个first out。

![](img/4aca8059f57b56ac1238e8675968ee29_82.png)

那out的呢具有我们的这个exchange handle的吸收，并且进行处理，那end of month，这个class呢，主要是决定我们现在current date，是不是到了这个月底了。



![](img/4aca8059f57b56ac1238e8675968ee29_84.png)

那到了月底了之后呢，我们就得做这个REBALANCE的这样的一个事情，那create investment list呢，这个也是一个helper function。

主要做的就是防止我们这些ticker他们的id重复，那其实对于每一个strategy来说。

![](img/4aca8059f57b56ac1238e8675968ee29_86.png)

其实最重要的就是这个kk signal的这个方向，这个signal呢主要是就是做我们的这个event，进来之后到底是勾输入什么样的strategy，最后呢把它处理成一个event啊。

一个是一个signal events send给我们的exchange，告诉他对于这一条historical data，我们要不要做什么样的action，是应该观望啊，还是应该买呀，还是应该卖。

那么呢在这里呢啊就比较简单，我们判断他是不是月底，那判断了是月底之后呢，那如果这个时候需要REBALANCED，呃如果呃就是说他这个INVESTIER如果是true，也就是需要REBALANCE。

那这个时候呢我们就把之前的asset了，然后这时候我们来做这个REBALANCE的事情，那如果没有呢，我们就扣这个BOT，那我们还不要忘记，就因为他被扣过了。



![](img/4aca8059f57b56ac1238e8675968ee29_88.png)

所以说这个时候我们的tickle invested，要把它设成true，那接下来我们就来run我们的这个啊，monthly rebalance这样的一个函数。



![](img/4aca8059f57b56ac1238e8675968ee29_90.png)

那么主要是set的，像这个嗯调上面我们的这个monthly balance。

![](img/4aca8059f57b56ac1238e8675968ee29_92.png)

strategy等等等等，那其实对于这个monster与balanced。

![](img/4aca8059f57b56ac1238e8675968ee29_94.png)

我们qs trailer其实有自己内置的本身呢，就是这个liquid dary balance position，SEOR和这个reban strategy，那么由这两条就是本身内置的这个函数的话。

呃q s trader呢会帮我们run这个monthly如何，这个liquid的，包括REBALANCE。



![](img/4aca8059f57b56ac1238e8675968ee29_96.png)

所以这两条函数呢不需要我们自己重新写，我们只要把参数给input in就好了。

![](img/4aca8059f57b56ac1238e8675968ee29_98.png)

那我们report出来这个result也就是call这个bad test，Star trading，就会给我们，后面我们之前提到的那个很漂亮的report，也就是tear sheet。

那这个时候呢我们做三条消息，第一条就是这个equity和BN的，40%和60%，那么其实调用非常简单，就已开始我们得有我们自己的input，就是我们的ticker名嗯，是s spy跟这个ANGUSBN。

那么它的这个weight呢，我们得PREDEFINE好，是一个dictionary的形式，然后我们扣我们上面写好的这个run monthly，REBALANCE这个函数，那把我们上面调用要求到的这个呃。

BARRB放进去，分别是这个ticker名，ticker的weight，然后title呢是我们TIERSHIP那个equity curve的那个title。

那么start day跟end day就是我们的起终点时间，还有这个initial equity呢，是我们这个资金量，就我们之前的这个资金量得是多少，那么我们可以设一个这个50万刀。



![](img/4aca8059f57b56ac1238e8675968ee29_100.png)

然后这个对于这个qs trader来说呢。

![](img/4aca8059f57b56ac1238e8675968ee29_102.png)

其实我们的这个IQT，对于最简单的这个monstry balance的，这个前面的这个main函数的设置都很简单，比如说大家还在可以再看一个例子，其实就明白，然后比如说是这个啊。

我们predefined的这个weight，那我们其实都不变，tickers也就是如下八条，那which呢也是这样，如下写好，跟上面就是其实比上面的60跟这个40来的。



![](img/4aca8059f57b56ac1238e8675968ee29_104.png)

其实就是多几个key而已，那一样的是扣这个run monthly balance。

![](img/4aca8059f57b56ac1238e8675968ee29_106.png)

跟前面的这个其实没有任何区别，其实也是只差了weight的地方。

![](img/4aca8059f57b56ac1238e8675968ee29_108.png)

那么对于equal weight其实也是一样的，那么做调用的话呢，是直接在command line里面call Python，然后空格我们这个某一个strategy的bad test点。



![](img/4aca8059f57b56ac1238e8675968ee29_110.png)

Py，那么final里呢出的output就是如下这样的形式。

![](img/4aca8059f57b56ac1238e8675968ee29_112.png)

那么很漂亮的一个报表，首先会给这个equity curve，然后给这个historical的这个JORD，然后呢给这个MONTERRETURN的这个hit map。

大家可以看到这个越红的地方就亏得越厉害了，越绿的地方就是return比较高的，然后给了这个yearly return这个百分比，然后正如我们所料，其实在08年的时候就有很大的捉到。

那别的时刻呢就是会有一个比较高的return，然后会给这个curve and benchmark的comparison，会给我们的年化的return和sharp ratio。

然后包括我们每年会完成多少单的trade，那我们看最后一条指标的原因是，主要是看我们的这个呃trading cost有多高，就有时候可能换手率太高的话。

我们的这个commission fee也会去的比较多，所以呢这个也是在量化交易中，很需要考虑的一个点嗯。



![](img/4aca8059f57b56ac1238e8675968ee29_114.png)

然后这个就是主要是我们后面的这些t，其实也都大同小异。

![](img/4aca8059f57b56ac1238e8675968ee29_116.png)

那我们主要分析一下这个strategy嗯，首先呢其实对于这个6%，40%的这个portfolio呢，我们在run之前，其实自己本身就要有个概念，就是说在08年的时候，对一整个equity市场大跌。

那么BD的relatively是比较稳健的，所以对于这一条六十四十的strategy来说呢，在08年的时候，我们的亏损一定比别的，就是说没有用BD来hedge的这个亏损要来的少的。

所以大家可以看到在08年的时候，我们这个我们自己的bad test也是绿色，这条线其实是outperform of，我们的这个裸的benchmark，也就是strategy的。

但是近年来的performance，没有我们的s spy来的高，是因为近年的这个BB的一直比较低迷，那那个equity市场的话，一直是比较这个positive的，所以说我们在嗯金融危机前后的两个区间。

也就是equity比较兴盛的时候呢，我们的这一条很保守的strategy，我们的performance比我们的这个benchmark来的低。



![](img/4aca8059f57b56ac1238e8675968ee29_118.png)

那么对于这个waited的来说，当然因为这个时候因为你的PFOLIO更分散了，你没有一个主次之分，那么对于别的别的TIKER来说呢，他的表现并没有s spy来的好，所以你oppo all综合下来呢。

他的这个收益率呢就远在s spy之下了，而且呢对于这个equity的这个ETF，其实是有更高的这个纯session cost的，所以说也relatively降低了你的收益率。



![](img/4aca8059f57b56ac1238e8675968ee29_120.png)

然后呢再看这个EQUWAITED，那么equwaited performance，那就更差了，因为这个时候相当于是一个完全无脑的把所，我把我们的资金等量的分配在所有的这个market上。

那么你嗯综合起来来说的话，那效果就不是很好，但是对于equal wait有一个好处，就是呢你赚也不是赚的很多，那么你亏呢也不会亏的很多，所以呢这就是这个很像基金的由来。

那基金呢就是当当当然不可能只买一只股票，他就是在很多种investment里面呢，其实都进行了合理的分配和选择，那么这个时候呢它可以规避风险。



![](img/4aca8059f57b56ac1238e8675968ee29_122.png)

那么接下来让我们来看这个嗯advanced的一些的，也是基于我们这个AIGAGARCH时间序列模型的，那么对于呃这个来说的话，我们这边没有使用COSTA，因为科strator currently。

它跟R是没有接口的，但是他expect在未来之后呢，QSSTRATOR也可以与R呢进行，这个啊UI的这个共享。



![](img/4aca8059f57b56ac1238e8675968ee29_124.png)

那我们接下来介绍一下这个ORIGMA加GUCH，在啊扣子里面这个时间序列模型跟应用，那我们这个strategy的想法呢，主要是一个这个rolling historical window。

那么我们的steps呢对于每天，那我们利用前K天的这个lag的log return和呢，我们固定的一个historical window，比如说我看这个three months的，如果对于daily的。

那如果对于intro intro day的话，那么比如说每天我有啊这个60个data点，那我们可以考虑看这个五天的，就是三天到五天的，也就是差不多是一周的数据。

这样的我们来拟合我们这个ORIGMA加GTCH模型，并且用我们这个模型对于这个第二天的prediction，这个return呢，来决定我们的今天count的那个action应该如何。

那如果我们预测第二天的预测值是正的呢，并且现在呢不在market里面，那我们就long，那如果预测只是负的，并且我们现在在market中，那我们就short。

那对于其他嗯这个combination的结果呢，我们就那个观望hold就叫不take action，那我们这里面有几个东西，是需要我们做optimization的，那么第一个呢是这个K。

也就是到底是我们利用前多少个的REICH呃，这个lag来看，也就是我们的这个时间序列模型，我们我们那个lag取最长的长度要多少，因为如果太长会OVERFIT，那如果太短的话。

可能就没有capture到我们这个序列相关性，那么还有我们这个look back的historical window应该取多长，那么这个都需要optimization，那在我们第五节课说过。

我们可以用网格搜索或者cross validation，来做optimization，那第四点我们需要注意的是，在这个real time training的时候呢。

我们需要考虑到我们的commission，fee和transaction cost，也就是说我们的换手率如果越高，我们的这个存session cost也就会越大，所以我们还要把这个给take嗯。

给这个take into啊，Consideration，所以这个时候呢，我们这个固定的window如果取太短的话，那会导致我们模型的volatility，就是我们模型变化的太快了。

那么这个换手率就一定很频繁，那么这样的话有可能不会带来，就是虽然我们带来了额外的收益，但是我们减去我们的存session，用cost。



![](img/4aca8059f57b56ac1238e8675968ee29_126.png)

我们那个total的这个收益率还降低了，那我们来看一下这个时间序列模型的这个流程，首先呢我们在R中要用这个are u，GARCH的这个library。

那我们在这边我们选用的是这个garch one one model，这是其实是基于一个经验的选择，也就是对于其实对于金融实践训练来说，一般尬取这个在一阶或者说两斤以内的模型，就足以能够解释波动率集群了。

如果太高的话，是会OVERFITTING的，然后接下来是要set up这个you gu这个东西，那这个呢其实是我们要define一个object，那么它呢会对我们model的这个variance。

跟min进行建模，那我们在里面define我们的这个variance呢，就是我们这个时间序列，log return的vs是由garch one one model来解释的。

那么min呢是由这个阿玛模型来解释，min也就是阿玛PQ，那这个阿玛PQP取多少，Q取多少呢，其实我们啊在这个r code里面待会会看到啊，依旧呢是用这个嗯，对于每一个P跟Q我们都loop过去。

从0~5，因为其实五阶以上其实也已经够了，那在对0~5阶我们进行loop，我们比较谁的AIC嗯最小，那我们就选择最好的那个model，然后呢接下来我们选这个HGED就是distribution呢。

作为我们的这个error term的distribution，就大家还记得，对于不管对于阿玛还是DH来说，我们这个model后面都会有一个的IMMSNOT下，那在这边呢我们assume。



![](img/4aca8059f57b56ac1238e8675968ee29_128.png)

它是如下这样的一个分布的，那么我们可以来简单的看一下这个r code。

![](img/4aca8059f57b56ac1238e8675968ee29_130.png)

那么r code具体的呢我们不可能每一步都讲，那么而且尤其是它run起来其实很花时间，那么我们可以嗯对于每一个step做什么，我们进行简要的介绍，那么呢这个呢这个r code的这个代码名称呢。



![](img/4aca8059f57b56ac1238e8675968ee29_132.png)

其实叫ORIGAGOTCH啊。

![](img/4aca8059f57b56ac1238e8675968ee29_134.png)

在这个photo里面，那我们首先我们import的这几个我们要用到的library，然后在这边呢，我们从website上get这个s spy的symbol。



![](img/4aca8059f57b56ac1238e8675968ee29_136.png)

并且呢取这个log return，那在这边我们define我们的historical window，包括我们的这个forecast的长度，和我们这个forecast的嗯。

我们focus得先建好一个这个啊vector空的vector，那最后把我们forecast呢填到这个里面，那这边呢我们是在做一个这样的一个，loop的一件事情，那首先呢我们要得到这个SNP摆盘。

就rolling window和这个day，因为我们我们的这个model呢，其实也是rolling的那个做prediction的，然后其次我们要对这个阿玛PQ的这个PQ，进行定接。

那我们定接的话依旧是靠我们的这个比较，我们的这个AIC，那我们选择AIIC最优的，作为我们的这个阿玛阿玛model，然后接下来我们define我们的这个gush model，那我们定死了的。

用这个GUI one one，然后error distribution呢用我们之前提到的SGED。

![](img/4aca8059f57b56ac1238e8675968ee29_138.png)

然后呢我们要catch我们的这个yoga fit，看我们这个fit的结果如何。

![](img/4aca8059f57b56ac1238e8675968ee29_140.png)

然后呢在这边我们会output我们这个forecast的result，那前提是呢我们这个gtch model得这个convert，那我们啊forecast forecast，我们结果之后。

然后来拿来run我们这个forecast vector，你就把我们答案放到这个forecast vector之后，我们用这个CSV的格式呢进行output，然后中间我们要做的一件事情。

是要把它input到Python里面，让我们做一个forecast知识，只是一个data frame的一个调整，也就是因为forecast one step，所以我们去掉了第一行。

然后把forecast跟我们这个真实的real time，history a数据进行一个把它补齐，那么补齐之后我们reading import进来，我们用我们之前我们得到的这个return的。

这个序列呢，我们做阿玛加garch return的这个prediction，那做好PREDITION之后呢，我们create我们的这个back testing。

那么并且与最简单的s spy的by and后，这个strategy呢进行比较，那接下来我们就pd出我们的这个active curve。



![](img/4aca8059f57b56ac1238e8675968ee29_142.png)

那么嗯具体的这个code讲完之后。

![](img/4aca8059f57b56ac1238e8675968ee29_144.png)

我们pro啊pro出来最后的结果呢是如下图所示，大家可以看到在不同的时间区间内，比如说这个1960到这个2000年，当我们这个数据就是本身这个s spy嗯，都是一直向好的情况下呢。

大家可以看到这re码加gage model呢，是嗯非常大程度的outperform了，我们这个啊s spy就是最简单的这个buy and hold，也是只买s spy这个strategy。

那么在这个近期大家可以看到，在这个08年这个区间内呢，在这这个time series model呢，其实比我们这个，真正的只买s spy来的效果还要坏一些，如果这个时候其实相当于。

你可以理解成一个追涨杀跌的一个情况，所以这个时候比值特别保守的，只买这个SMP呢，你来的收益率来的低，那么到后面呢，当这个序列的VATILITY震荡很高的时候。

大家可以看到我的这个二维码加garage model的，又比这个s spy outperform了，所以我们其实在这个市场经验上来看，大家可以看到对于这个volatility非常大的，这个时候嗯。

ORIGA加GTCH模型呢能够很精准的capture到，我们这个时间序列的volatility。

![](img/4aca8059f57b56ac1238e8675968ee29_146.png)

所以呢他的表现呢会更好一些，那么接下来让我们来看比较重要的，也就也是非常常用的，就是嗯这个pair trading，那么pair trading我们介绍两块，一块是这个就是最基本的。

只基于一个静态谐振的，那么第二块呢是基于这个卡尔曼滤波的，这个动态的dynamic headging的pair training。



![](img/4aca8059f57b56ac1238e8675968ee29_148.png)

接下来我们来看这个基于谐振性的PEETRADING，那么这是一个难意思的，这个hedging ratio，的一个这个PEETRADING的strategy。

也就是说呢我们对应一整条historical data，我们run一个这个regression，我们得到一个hedge ratio，那我们就利用这个固定死的这个hedge ratio呢。

我们做这个pair trading，那么我们定义我们的这个weight，也就是我们run好这个regression之后的，这个位置的这个比率，那么look at periods呢。

跟这个entry跟这个acid than呢，我们跟这个第，我们当时做pre training那节课讲的意义是一样的，也就是说对于每一个这个时间点。

我们都可以算我们的这个regression的residual，我们regression receduo可以算一个DESCORE，那么当这个cs score呢比这个entry再来的高。

那我们就嗯entry这个market，说明这个时候这个market的是呃potential能赚钱的，那如果低于这个acid than呢，那我们这个时候就ax in the market，就是这个时候呢。

它其实属于一个比较低迷的实践，那我们在定义我们这个base quinity，也就是我们一开始手串有多少capital，那我们在做这个谐振型的PATTRATING之前呢。

我们得run一个r co来决定我们这个hedge ratio。

![](img/4aca8059f57b56ac1238e8675968ee29_150.png)

贝塔是多少的，那么这个呃嗯r code呢，其实跟我们之前做的这个pair trading，那次r code非常类似，我们就先get我们想要做pre training的这两条ETF，那这都是跟铝相关的。

就是这个金属铝相关的ETF，那我们嗯先plot先看一下这个backward adjusted，那么之间的相关关系有多少，那么做好之后呢，我们就run一个非常简单的。

由a based on b的这个regression，那run好regression之后呢，我们做这个AD f test，我们test我们我们这个VC9，是否是一个我们认为的一个啊均值回复的。

类似于why noise这样，无序列相关的一个这样的过程，那如果是，我们就可以把我们这个hedge ratio投入使用了。



![](img/4aca8059f57b56ac1238e8675968ee29_152.png)

那么我们由R扣得到我们这个HDRATION的，是这个负的1。213，那这个时候我们可以把这个结果呢。

![](img/4aca8059f57b56ac1238e8675968ee29_154.png)

带到我们的Python的这个qs trader里面的strategy。

![](img/4aca8059f57b56ac1238e8675968ee29_156.png)

来进行调用。

![](img/4aca8059f57b56ac1238e8675968ee29_158.png)

![](img/4aca8059f57b56ac1238e8675968ee29_159.png)

那我们来简单看一下我们这个QC的，做这个基本的pair trading的这个步骤。

![](img/4aca8059f57b56ac1238e8675968ee29_161.png)

那么首先呢我们做这个PATCHETING的这implementation，跟我们别的这个科，SHELDER的strategy呢非常类似，只是在这个calculate的signal这边。

也就是我们提到的主要的strategy的实现。

![](img/4aca8059f57b56ac1238e8675968ee29_163.png)

都在calculate signal这边改，那嗯首先我们这边defined的这个，initial的东西就会多一些，包括我们这个entry xi，还有我们这个look back period到底有多少。

就比我们之前做最简单的这个啊，基于这个monthly rebalance来的稍微多一些，那么这个代码就给了大家，其实通过这些，其实通过这个名字其实也顾名思义能看到我们。

大概我们后面要用到的这些variable，大概是一些谁，那我们要corrector这个time and price，那这也是一个help的函数，主要做的呢就是说啊。

我们想要使用的这个price and event time的这个bar呀，必须是这个out of orders在这event q中的不能说不在，然后相当于是一个helper的函数。



![](img/4aca8059f57b56ac1238e8675968ee29_165.png)

它并不实现任何的strategy。

![](img/4aca8059f57b56ac1238e8675968ee29_167.png)

那做这个long units跟salt units也是类似，那主要呢是让他这个啊number能够是一个正常的，close out这个form。



![](img/4aca8059f57b56ac1238e8675968ee29_169.png)

然后进入到我这个q event中，并且把它put到里面，然后以这些固定的形式。

![](img/4aca8059f57b56ac1238e8675968ee29_171.png)

是根据他的这个weight跟零之间的关系的，那么short呢也是类似。

![](img/4aca8059f57b56ac1238e8675968ee29_173.png)

然后这个jescot trade呢，主要是要呃决定我是否是trade，那就会用到我们上面这个exit跟这个enter，这个z score，就如果比我设的这个下限啊来的这个低了。

那这个时候呢比minus是来的低呢，这是我long，那如果呢比我们这个entry的来得高呢，那这个时候呢我就得shot，那如果是在两者中，就是说如果又满足了这个条件，但是我已经在market之中。

或者是反之，那么我们就选择close，然后这个主要的主成分内容呢，在这个calculate signal里面，那这个时候我们不要得把我们之前使用到的，这个利用weight的这个放进去。

那主要做的事情就是把这个signal，我们这个一整个strategy能send出来的，这个signal封装好呃，分装好之后呢，准备献给qs trader里面的这个exchange handler。



![](img/4aca8059f57b56ac1238e8675968ee29_175.png)

那么做这个back test呢。

![](img/4aca8059f57b56ac1238e8675968ee29_177.png)

就是主要是调用我们上面提到的这个呃，我们上面define好的，这个COINTEGRATION的pair trading，那么所有的这个参数设置都在下面，包括我们的这个weight等等嗯。



![](img/4aca8059f57b56ac1238e8675968ee29_179.png)

然后嗯上面的这个weight这边输入的这个东西，是由我们的这个r code，run r code的这个regression得到的，那我们把这个负的1。213填在这边。

然后我们把这个back test的给set up好，set up之好，好之后呢，我们就调用我们的这个ma，然后在这边呢set up我们好了，我们的tickets的名字。

最后呢是这个run我们一整个这个CONFIG来，最后铺出我们的结果。

![](img/4aca8059f57b56ac1238e8675968ee29_181.png)

那么最后呢他会generate的这个贴扣的结果，是如这个下图所示，这边呢就是我们一整个贴扣的结果，我们可以看到我们这个在15年之后呢，是一个稳步上升的区间，但是到16年之后。

我们这个strategy就是啊，我们的performance就没有这么好了，那主要原因呢，其实是，因为我们是用15年之前的数据来run，regression的，那之后呢我们就用我们regression。

好的，hedge ratio负的1。2来做我们的pair trading，那么一开始的时候呢，它离我们之前的数据点都会比较近，那么越来越偏离越来越偏离，其实大家也可以看到，在这个后来16年之后呢。

其实他们这个序列之间的这个相关性，就越来越弱了，那就说明我们的这个residual，我们的残差不再满足是一个均值回复的y nice，所以这个时候我们得采取这个别的方法，进行ZHDR，那要不然呢。

我们其实我们这个RECEI就越来越偏离，这个均值回复这样的定义，那么自然而然这个strategy呢就生效了。



![](img/4aca8059f57b56ac1238e8675968ee29_183.png)

所以这个时候我们需要引入我们这个，基于卡尔曼滤波的这个动态filter，那么我们这边用的是这个i shares，这个tilt跟这个IEI这两条这个bond的，就是treasury bond的ETF。

那么也是在纳斯达克里面破我们的这个data，那我们要建立的呢依旧是他们之间的regression，但是呢它这个唯一的区别就是，我们之前的这个regression，静态的这个贝塔是我们提前算好的。

但是在这边呢，我们把它加入到我们这个stay model中去update，那这个时候我们的这个trade，我们在满足什么情况下，我们选择交易呢，是如下这样的一种strategy。

也就是我们在做这个嗯common filter的时候，同时算出我们现在这个return的VR就是volatility，那这个时候呢，我嗯我run这个卡曼滤波会有一个一样的。

跟前面的这个嗯pair trading有一个这个长叉，那如果长唱呢比我这个volatility，minus volatility来的小，那说明这个时候呢，我更有概率回复到均值上面去。

所以我就long the spread，那如果比它大于等于呢，那这个时候我就ACITO，我这个long也就是在这个上下巴之间，那如果比这个上坝来的还要来得高呢。

那这个时候我就shut the spread。

![](img/4aca8059f57b56ac1238e8675968ee29_185.png)

那如果在这个坝中间呢，就是essay the shot，我们来回顾一下，我们之前这个卡尔曼滤波的知识，那么我们这个state model，我们之前呢有如下这样的一个情况。

首先是我的这个内层dynamic的update，是7-10克，update到70克，然后接下来有一个observation yy是我们的观测值，那是由这个内场的hidden layer。

那么进行这个线性组合得到这个Y，那么我一整个卡尔曼滤波的这个update的式子呢，是如下所示，我们update我们这个卡玛卡玛GA，然后update我们的convinced matrix。

最后update我们的这个Y，也就是我们内置的这个dynamic的这个，system的current state，我们来看一下我们哈发微博用于我们的这个嗯，Linear regression。

或者叫做我们这边的dynamic pair trading，那呃真实的情况呢，比如说是Y等于二加上，所以ST加上ZT，那这个时候这个二三，其实这两个位置都是我们不知道的，它会随时间变化。

所以这个时候我的这个state，也就是内涵的这个hidden state，我就设成我的这两个二三的这两个位置，就是coefficient，那我们的stay update呢是如下所示，那X呢就是等于这。

因为我们假设我们这个COEFFICI之间，是不存在的一些最时间的扰动的，所以我们就设一个单位正，那么YT的这个update的YT呢，其实是我们这个PETRADING前面的这个ETF的return。

那么呢等于啊这个S1呢是第二条ETF的return，那么乘以这个XT也就是我们的coefficient，那么加ZT，那么我们把这个卡尔曼滤波，通过这个come on gain的这个公式。

带到我们的这个code里面去实现，那么我们可以得到我们这个parameter，一整条，这个随这个呃，我们时间序列波动这样的一个波动图，那我们把嗯我们前面提到的这个理论呢。

带到我们的这个qs trader strategy里面去完成。

![](img/4aca8059f57b56ac1238e8675968ee29_187.png)

那么完成的主要形式呢，其实come on petraining，我们前面要提供的东西跟我们的这个啊，携程性的trading呢非常的类似，那么它唯一的区别呢。

就是我们需要提供我们这个卡尔曼滤波的first date，就是initial初始值，那么这些呢define都是我们这个初始值的嗯，Value，那么定义成什么答案呢，其实不是太影响。

因为它最后都会converge到我们的这个一个，比较比较稳定的一个state中，那么依旧有这个secreate time and price这些help的函数。

那么呢主要的区别是在这个calculate signal里面，也就是我们strategy实现的地方，那在这边呢，我们会做我们这个卡尔曼滤波的一整个update。

然后包括像这个y hat的update observation的update。

![](img/4aca8059f57b56ac1238e8675968ee29_189.png)

我们的ems sal。

![](img/4aca8059f57b56ac1238e8675968ee29_191.png)

我们的常差的update，我们的这个qt就是斜方差正的这个update，包括最后的ATC塔，也就是我们的这个呃，内置的我们的coefficient也能称为XT。

那然后最后再update我们的这个新一步的呃，Coverance matrix。

![](img/4aca8059f57b56ac1238e8675968ee29_193.png)

就这一步的实现呢，就是跟我们上面这个slice是相对应的。

![](img/4aca8059f57b56ac1238e8675968ee29_195.png)

那么大家回去呢可以自己去看，然后在这一步呢。

![](img/4aca8059f57b56ac1238e8675968ee29_197.png)

我们是实现了我们上面说的那个strategy，就是跟负的根号qt和根号qt之间的关系。

![](img/4aca8059f57b56ac1238e8675968ee29_199.png)

我们选择long或者short或者是closing。

![](img/4aca8059f57b56ac1238e8675968ee29_201.png)

我们的log或者是closing我们的SHT，那么到这边呢我们的strategy就写完了。

![](img/4aca8059f57b56ac1238e8675968ee29_203.png)

那这边呢是调用我们的这个呃karman filter的back test。

![](img/4aca8059f57b56ac1238e8675968ee29_205.png)

主要呢是为了generate我们的这个tm map。

![](img/4aca8059f57b56ac1238e8675968ee29_207.png)

一样的是我们要定义好我们的这个ticker，那么最后呢run我们这个function。

![](img/4aca8059f57b56ac1238e8675968ee29_209.png)

那前面的这个initial equity，包括star day and day，那么都跟我们time series match上就好了。



![](img/4aca8059f57b56ac1238e8675968ee29_211.png)

那么我们之后present的这个结果呢是如下图所示。

![](img/4aca8059f57b56ac1238e8675968ee29_213.png)

那么我们可以看到我们的这个dynamic hedge，我们这个back test的是我们这个accumulate return呢。



![](img/4aca8059f57b56ac1238e8675968ee29_215.png)

嗯比我们之前我们之前提到的这个嗯，那就直接做这个正常的，这个没有dynamic hing的效果呢来的好的很多。



![](img/4aca8059f57b56ac1238e8675968ee29_217.png)

然后我们主要是我们可以看到我们的这个捉down。

![](img/4aca8059f57b56ac1238e8675968ee29_219.png)

我们这个桌down的percentage呢，就是其实是比别的来的好的非常多。

![](img/4aca8059f57b56ac1238e8675968ee29_221.png)

大家可以看，比如说前面像比较过分的，会有这种负的80%等等等等，那么这种dynamic hing呢，能够比较好的规避我们strategy的风险。



![](img/4aca8059f57b56ac1238e8675968ee29_223.png)

然后我们可以看一下我们这个耶律return，那么基本上呢都是一个很好的performance，就是在12年的时候呢，这一段时间out of control了，那么这个主要是可以通过比较。

我们这个我们自己本身ticker的问题，那么12年的时候呢，就是贵金属在这一段时间有一个很大的捉到，所以一整个market其实都是down了，那么这边如果想要拯救这一段时间的strategy。

那么只能通过你很机智的停止，我们的这个机器人的这个自动交易，或者是使用别的产品来hedge，那么这边可以看到我们的哈呃哈呃。



![](img/4aca8059f57b56ac1238e8675968ee29_225.png)

这个SHAPARRATIO跟我们这个偷偷return，那我们接下来介绍最后一块，也就是基于我们这个machine learning的这个L狗。



![](img/4aca8059f57b56ac1238e8675968ee29_227.png)

那接下来呢让我们来讲最后一个模型，也就是基于machine learning的algo trading策略，那么在这里呢我们跟前面有所不同的，有两个地方。

第一个地方是呢呃我们采用的是intro data data，也就是日间数据，所以我们数据的哪个最小单位呢是分钟，那么之前呢只是一天一个数据点。

所以呢我们这边是一个high frequency的training，所以对我们这个CPU的要求会比较高，那么第二块呢是我们之前的模型都是predict，第二天的return呃。

或甚至呢把它转成price，那么我们这边的模型是predict的，第二天他的这个涨涨势到底是up或是down，所以是一个分类就是classification的一个问题，那么我们在这里呢。

举例呢是使用这个EREX的intro day data，那么我们用呃13年呢，到14年做我们的train data来train我们的machine learning model。

那么那我们后面的data数据呢拿来做这个呃，Back testing，也就是嗯也就是我们的建模，那么我们从这个website上破下来的erect data呢，有以下几个feature。

那么date open low high clothes，还有volume，还有一个open interest，那我们主要用的是date这个feature，还有close。

那呃首先呢嗯我们定义一些这个呃，variable的名字，首先我们learning用的feature，也就是我们的x variable呢，用的是我们return的拼接之后项啊，那么leg到底取多少呢。

是取5leg还是取10leg，那么这个是需要我们来learning的，也就是啊optimized的，那么在optimize之前呢，我们default先用五个lag，那么在我们的这个后面。

我们Python的code里面的这个look back这个参数，也就是定义我们到底是学习之后多少项呢，作为我们的x features，那我们的response呢是我们的这个up和down。

也就是正一和一，那么我们用的是如下这几种学习方法，一种是我们之前提过的这个linear discriminate，analysis和这个random forest是随机数。

还有这个gradient decent boosting tree，那么呃第四个呢是这个support vector machine，那我们的代码例子呢举的是random forest的。

那我们之后布置的大作业，会让大家尝试着用别的三种方法来进行这个learning。

![](img/4aca8059f57b56ac1238e8675968ee29_229.png)

那我们的参数设置是如下的，首先呢我们得有csv file path，也就是我们的input data存在哪里，那我们的是historical的minute的，price lag的就是日间分钟数据。

那我们还有设两个仓量，叫做updown factor跟percent factor，那么这两个呢是control我们这个上涨的ratio，也就是呃我们认为我们下一个的这个点。

我们是predictor正一还是一呢，是根据我们这个up down，非factor跟这个percent呃fact来决定的，比如说我们这个updown feat是2。0。

那percent factor定为0。01，那是什么意思呢，那正一是说明在下一个的这个look for a minute里面，我们的这个return，那么呢至少要超过20%。

但是这个时候它的下跌不会超过1%，那有人会问，为什么不，我们设一个上下坝，都是这个百分之百分之一就好了，因为我们在做trading的时候，我们我们大部分的策略都是选择比较保守的。

也就是说我们希望我们上涨是下跌的多少倍，那么我们才认为我们这个下一条吧，我们把它归为上涨的，也就是说我们希望上涨的幅度呢，比下跌的这个幅度来的高很多，那么我们才有理由认为。

我们下一个点是这个going up的，所以我们啊设置了这样子两个参数来control，我们对这个risk的厌恶程度，因此呢是这个阀值设的意思是，在这个固定的时间区间内，我们这个上升是下降了至少两倍。

那我们把它划分成正一，否则呢就划分为这个一，那么在我们后面的这个代码里，大家会看到有一个这个job lip的这个设置，那就是说我们的，我们最后run我们这个strategy的时候。

我们要point to一个pass to your machine learning model，那么我们举例，因为是random forest，所以说是下划线IFPKL。

那么这个呢是这个job lib这个pon module，automate做的，那么做的是这样，我们之前呢通过我们说过的这个呃。



![](img/4aca8059f57b56ac1238e8675968ee29_231.png)

07年到12年是learn我们train我们的model。

![](img/4aca8059f57b56ac1238e8675968ee29_233.png)

那train model好之后呢，把我们model information存在这个里面，那存在这个里面之后，当我们让我们真正的这个一三到14年的那个。



![](img/4aca8059f57b56ac1238e8675968ee29_235.png)

train trading的时候呢。

![](img/4aca8059f57b56ac1238e8675968ee29_237.png)

我们就会调用这个model里面的参数，那么进行prediction。

![](img/4aca8059f57b56ac1238e8675968ee29_239.png)

那让我们来看一下我们的这个代码。

![](img/4aca8059f57b56ac1238e8675968ee29_241.png)

首先呢我们要define这个intro呃，Machine learning model fit。

![](img/4aca8059f57b56ac1238e8675968ee29_243.png)

那么呢他主要做的事情呢，就是创造我们刚才看到的这个嗯m l model。

![](img/4aca8059f57b56ac1238e8675968ee29_245.png)

点这个IFPKL这个file。

![](img/4aca8059f57b56ac1238e8675968ee29_247.png)

那我们一开始是有一个这个help function。

![](img/4aca8059f57b56ac1238e8675968ee29_249.png)

做的是这个create up and down data frame，就按照我们刚才提到过的这个方式，设一个这个up factor跟这个down的percentage，那把这个设好之后呢。

我们吸入我们的这个historical data，那根据刚才这个弱来判断，我们下我我们的这个BN呢。

![](img/4aca8059f57b56ac1238e8675968ee29_251.png)

到底是属于，就是我们的Y到底是属于正一还是一，那么把我们historical data吸进去之后，append1列，那么这一列呢是根据我的这一个look look forward，period里面呢。

可以决定我们这个报对应的，到底是上涨还是下跌。

![](img/4aca8059f57b56ac1238e8675968ee29_253.png)

那么这边的代码主要做的是两件事，第一件事这个create这个look back the column，那是为了我们后面learning使用，那这个look forward the column呢。



![](img/4aca8059f57b56ac1238e8675968ee29_255.png)

我们对这个look forward的time window也是自己定义的长度，那比如说定义5分钟，那就是每五个bar看一次，看我们到底是属于这个up还是down的这个区间。



![](img/4aca8059f57b56ac1238e8675968ee29_257.png)

那我们把它呢放在这个序列里面。

![](img/4aca8059f57b56ac1238e8675968ee29_259.png)

然后最后equate成这个up down的这个column，那最后呢把这一整个清理好的data frame output出来。



![](img/4aca8059f57b56ac1238e8675968ee29_261.png)

那output好之后呢。

![](img/4aca8059f57b56ac1238e8675968ee29_263.png)

我们来调用我们上面提到过的这个方选，那么调用function的时候。

![](img/4aca8059f57b56ac1238e8675968ee29_265.png)

我们这边使用的是这个random forest classifier，那把我们处理好的这个X跟Y放进去，那么我们这边呢用我们做一个这个model split，做一个cross validation。

来测一下我们的kate rate，包括我们这个confusion map，如混沌矩阵。

![](img/4aca8059f57b56ac1238e8675968ee29_267.png)

那我们包括我们的这个model score啊等等等等，output之后，我们最后呢就是调用了，我们之前提到过这个job live点down，那把我们这个model呢存在我们的folder下。

那后面的strategy就直接从这里面调用。

![](img/4aca8059f57b56ac1238e8675968ee29_269.png)

不用再run我们这个learning model，因为比较浪费时间。

![](img/4aca8059f57b56ac1238e8675968ee29_271.png)

那这边可以看到我们的这个正确率与错分率，那这个时候我们开始run我们真正的这个machine learning。



![](img/4aca8059f57b56ac1238e8675968ee29_273.png)

Strategy，基于我们上面用这个随机数random forest。

![](img/4aca8059f57b56ac1238e8675968ee29_275.png)

认过这个pk l file，那我们导入这个啊strategy。

![](img/4aca8059f57b56ac1238e8675968ee29_277.png)

那我们建立这个introdumachine learning的这个class，跟我们之前的这个strategy一样，我们首先得initial来，就是初始化我们所有的参变量。

那么参变量需要定义的呢就是比较注意的一点，就是在这边有个self点model，把我们上面存好的这个PICO啊file给low进去。

那这个update currenreturn呢是一个help function，就主要是把我们现在呢我们要用的strategy的。

这个return feature呢给这个update到我们的data frame里面，那与之前一样，我们在一条strategy下，最重要的核心函数就是这个calculate signals。

那么在这里面呢，它把我们的啊，historical data每一个点吸进去之后，我们generally我们的signal啊，那这个signal signal event呢。

最后是选择要献给execution handler的决定。

![](img/4aca8059f57b56ac1238e8675968ee29_279.png)

我们到底是buy啊还是short，那就根据我们之前提到过的啊，我们的strategy就是当我们呢不在market中，并且呢我们对下一步的prediction是正一，那么这个时候我们选择lg。



![](img/4aca8059f57b56ac1238e8675968ee29_281.png)

那如果呢我们这个时候嗯在市场中，并且对下一步的prediction是一下跌，那这个时候呢我们选择是S嗯，对其他的情况下呢。



![](img/4aca8059f57b56ac1238e8675968ee29_283.png)

我们选择的是hold嗯，那这个就完成了我们这个strategy的这个点。

![](img/4aca8059f57b56ac1238e8675968ee29_285.png)

PY的构建，那接下来呢我们来write我们的这个back test。

![](img/4aca8059f57b56ac1238e8675968ee29_287.png)

也是真正run我们这个model的这个函数，那把我们之前define这个strategy跟import进来。



![](img/4aca8059f57b56ac1238e8675968ee29_289.png)

那import进来好之后呢。

![](img/4aca8059f57b56ac1238e8675968ee29_291.png)

一样的也是initialize啊，我们的这个嗯所有需要的参变量。

![](img/4aca8059f57b56ac1238e8675968ee29_293.png)

那initially整好之后呢，我们最后选择做这个run函数。

![](img/4aca8059f57b56ac1238e8675968ee29_295.png)

那么run函数呢，主要就是主要就是把我们所有的这个。

![](img/4aca8059f57b56ac1238e8675968ee29_297.png)

之前提到过的啊，Fit。

![](img/4aca8059f57b56ac1238e8675968ee29_299.png)

包括我们的strategy给aggregate起来，那么我们需要使用到的是这个呃start date and end date，还有我们前面的这个price handle了。

然后呢是基于historical data的8price handler。

![](img/4aca8059f57b56ac1238e8675968ee29_301.png)

如果大家有印象的话呢。

![](img/4aca8059f57b56ac1238e8675968ee29_303.png)

这个在我们第五节课上其实也提过了，那么这个其实是QSSTRATOR一个非常好的方式。

![](img/4aca8059f57b56ac1238e8675968ee29_305.png)

是能帮我们自动的做这个intro day，那这个sell呢嗯sell and by，那么我们只需要把我们的这个model define好，那么呢由他吸那个吸入进行这个training就好了。



![](img/4aca8059f57b56ac1238e8675968ee29_307.png)

那在这边呢，我们要用我们把我们的这个之前提过的。

![](img/4aca8059f57b56ac1238e8675968ee29_309.png)

person handle啊，rise manager啊等等等等都初始化，然后呢这边需要注意的是，这个period是用来算我们这个word的，那和我算我们这个shop ratio。

因为我们这个是minutes的，所以说呢每天也就睡6。5个小时，然后每个小时呢是60分钟，所以这边呢需要有所这个改进，那么在bad test这边呢。

就是setup我们bad test需要用到的所有的参变量，那么result呢就是输入我们的tr matrix。



![](img/4aca8059f57b56ac1238e8675968ee29_311.png)

那这边与前面讲的一样，就是我们前面的strategy一样的，也就是这几行代码的调用，我们需要CONFIG，我们需要我们的ticket，那么fire name呢我们之前提过，所以在这边我们设为now。



![](img/4aca8059f57b56ac1238e8675968ee29_313.png)

因为在CONFIG里面呢都CONFIRE好了，那么嗯我们最后run出来的结果呢。

![](img/4aca8059f57b56ac1238e8675968ee29_315.png)

嗯是在这边我们可以看到我们做这个machine learning，基于这个random forest的策略呢，return呢嗯已经大大的提高了很多，而且大家可以发现很显著的一点是。

这个捉到呢已经被控制在2%左右的，那么这个对于这个一条strategy来说呢，做down是相当之小的，然后我们可以看我们这个monster return，包括我们这个sharp ratio12。84。

就是比之前提到的呃，任何的一条衰而举都来的高的很多，然后这个yelly return呢也都是一个很不错的结果，那么对于这个方法的改进呢，我们可以通过对这个random forest的深度。

包括呃我们这个look back跟look for a period，到底选的长度可以进行optimization。



![](img/4aca8059f57b56ac1238e8675968ee29_317.png)

可以继续优化我们这个策略，那我们这节课呢有一个大作业，那么大作业的deal呢可以到这个课程结束，大家可以继续做，也就是嗯因为这一节课的内容很多，那么对于整个包括strategy怎么写。

然后还有bad test怎么写，那么我会把我们上课用到的代码发给大家，那么大家通过模仿，然后自主完成这个machine learning logo里面关于这个LDA。



![](img/4aca8059f57b56ac1238e8675968ee29_319.png)

SVM等别的分类器，对于我们刚才这个intro day的这个嗯。

![](img/4aca8059f57b56ac1238e8675968ee29_321.png)

machine learning的logo的进行的实现。

![](img/4aca8059f57b56ac1238e8675968ee29_323.png)