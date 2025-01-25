# 清华博士带你学习python金融量化投资分析与股票交易【附项目实战】 - P68：70回测框架 - python大师姐 - BV1BYyDYbEmW

好同学们，那我们这个下班还是写完了啊，接下来就实现一下，我们整个回测框架的一个主体，啊比如说我们叫做一个run函数，好这个函数啊，这个我们干什么呢，首先啊我们的目的是为了什么，目的是为了什么。

回测傻子回测是严肃啊，回测回测的目的是要干啥，是不是我们要那条线，要两两条，两条线对吧，一条是我们自己的收益曲线，一条是我们哎可能还要我们的什么这个基准的，这个曲线对吧好，那我们先不管这种。

我们先说这个自己的线怎么实现啊，那我们就要写一个什么呢，写一个data frame，记录一下每个交易日的收益率或者是收益，那对吧，那这个时候比如说我记录一个叫做PL，TDF啊。

这个就是意思就是我接下来是要给他画图用的，建成什么呢，一个新的data frame啊，索引就是什么，就是我的data range，对吧，嗯啊context点data range啊，注意这个东西。

这是一个数组，如果说我想把它变成一个date time index的话，我需要DF点to date time，这些函数有都给大家讲过了啊，打错了。

这个是把它把里边这个数组变成一个date time index，这这不是点，这是pd好嗯，然后建一列column等于嗯叫什么呢，叫叫叫叫，比如说就叫value吧，就是就是评分叫想不出来英文了。

就是说收益率OK吧，那为啥建一个data frame，这一列为啥建这些说没用吗，后来还有一点，这是我们收益的评分，我们接下来还可能加一列是什么呢，是我们那个参照的评分，就是那个基准的评分，好吧好。

那这个DF建完了之后，接下来是要模拟每一天来做买，来做一些事情对吧好，For d t in context，点date range，这个DT是不是就是一个时间啊。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_1.png)

嗯好那这个时候因为我不说每天执行一次吗，这个时候我要什么解决一下之前那个问题了。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_3.png)

什么问题呢，我之前有一个小问题是啥。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_5.png)

是这个cf点DT，它刚开始的时候被复制成start date，但是start it可能不是交易日对吧，那没有关系，那这个时候怎么办呢，你可以在这赋值成study不交易日，但是这个date range中。

括号零是不是交易日第一个交易，这是这个范围的第一个交易日对吧，那这儿写写不写都行啊，其实我们可以把这就改成NN。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_7.png)

然后下边我们不是for循环吗，反正你for循环，这也要维护对吧。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_9.png)

那你这个时候的context点DT就是什么。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_11.png)

就是相当于是你把这个DT这个DT是什么，这个DT是字符串。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_13.png)

对对吧，所以你要把它变成你的DTUTIL点passer。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_15.png)

点点pass dt变成一个时间对象啊，传到context点DT嗯，好，然后接下来模拟每一天嘛啊，我们说每一天你要什么用户，他是不是要调用他自己什么，他获取日志数据，然后他根据他的规则，他来买。

不是他来买，他来进行买卖下单对吧。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_17.png)

所以这应该是什么呢，要给用户留出两个函数来哪个函数呢。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_19.png)

initialize怎么拼，以匿ITIALIZE，好参数context。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_21.png)

然后第二个这个先不写，这是用户写的吧，第二个参数是handle data啊，我们这个都和基本上和我们的啊。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_23.png)

这个距宽那个平台保持一致，好，那run的时候刚开始应该是用户调用它的，Initialize，应该在这个后边后边写吧，用户调用应该是来的，传就传那个全局的context进去啊。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_25.png)

然后在for循环里算了，每天之后啊算了，就是更新了今天的日期之后，那接下来是用户调handle data。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_27.png)

调用户写的这个HAZA，这个HADA是用户的代码，用户在这里边他肯定会有一些就是买卖的东西，对吧好，那这个东西弄完了之后，接下来我就要算目的就是什么，算今天的价值，不是把今天的价值放到这个PLTDF。

对应这一天的这个value列里对吧，对不对好，那这个value等于什么呢，是不是包括两部分，第一部分是现金，第二部分是股票值的钱，这个咱们第一部分那个练习就已经预说，说过了好。

所以现金是不是context点catch对吧，这是不是这个HAOA完了之后，我还有的钱是在这嗯，就你买卖完了之后，钱都存在这，那股票值多少钱呢，我就需要便利context点partitions对吧。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_29.png)

你看每一支股票值多少钱啊，首先啊价格等于什么，等于今天的开盘价，那就是get today data stock传进来，OK嗯这是今天的价格，那如果说这个如果说今天的价格是有的，啥意思呢。

就是价格有可能就是说有可能考虑到一种情况，有可能什么有可能今天停牌，对对吧，我的P正常写是P乘它，然后P乘上它的数量加到这个value里对吧，但是要考虑一个情况，考虑什么情况呢，就是考虑停牌的情况。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_31.png)

考虑停牌的情况，其实也就是我不是这个get他，他就给他写了吗，停牌的话，他是不是返回一个什么返回一个空的series，对吧嗯，对M7，它是不是返回一个空的series。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_33.png)

这个时候data是不是相当于是空的对啊，所以我这个里边啊，如果，啊这个要这样写了，today data等于好，他妈的，如果today data是空的长度，等于零的话。

那这是不是说明就今天没有拿到今天的价格，说明是不是停牌了，嗯对吧，没有拿到价格是不是就说明停牌了啊，停牌的话怎么办，平台的话就不能买了呗，不能买了怎么办呢，那你算计的价值怎么算，哎，这个停牌不好说。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_35.png)

我们先跳过去，先写else else是没停牌，没停牌就直接走了吧，P等于它点open，然后什么我的value加上我的P乘上它的数量，是不就可以了，对不对好，所以这个时候我的value加上P乘上数量。

数量是什么，context点positions stock，对对好，这是说没停牌的时候处理了。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_37.png)

停牌的时候，我的P怎么办，是个问题对吧，那我的这个价格按什么算呢，那我们是不是可以这样按照前一天的，或者前他们停牌之前。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_39.png)

那一天的那个价格来算对吧，嗯那我们想一下，就是就有好多种方法，你可以怎么样，你可以写一个函数，说如果说特data data没有的话，你去啊这个data frame1行一行往上找，找到为止对吧。

这是一种方法，那还有哦，比如说我们是不是可以写一个什么呢，我们写一个，Last price，一个字典这样一个字典记什么呢，就是我每有一个有一个这个价格，有每有一次价格。

我就把这个价格记在这个last pri嗯懂，那也就是说如果说我的P等于它了，那last price，Stock，它就等于P就是说继上一上一天，就之前那个有没停牌的时候的P，每次更新更新到最后一天。

那如果说他今天停牌了，我怎么办呢，他今天停牌的，我就拿last price，这个字典里对应的那个位置的那个价格，是不是就他之前那一天的价格对，或者说之前几天停牌前那一天的价格好。

那我这个时候P就应该等于什么呢，Last price，嗯对不对啊，那这比如说我这个呃打印一下，今日股票停牌就不打印了吧，这个时候打印也无所谓了，好那这个时候我P用这个，否则的话P用这个啊。

反正不管if else最后都有一个价格来让我算对吧，那我这个时候价格乘上它，算出来的是我现在的股票价值，嗯对吧，这个for循环，这个for循环执行完了之后就到这，我的价值是不是算出来了。

这个value是不是算出来的，这个value是不是就是我的总价值，对不对，所以这个时候我把它写到PLTDF里啊，点lock行是时间，TT列是value value，对不对。

这个DT就是他每一天的这个时间啊，等于value哎，这value这一列存的是啥呢，存的是就是我每一天我有多少价值，对不对。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_41.png)

好这个循环完了之后，就是外边这个循环完了之后，我现在是不是每一列都有一个value了。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_43.png)

对不对，好比如说我可以随便写一个handle data，这个时候我们来看一下，我就假设我这个用户的策略是啥呢，每天买一手可以吧，可以啊。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_45.png)

好这个时候我打印一下我的PLCDF。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_47.png)

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_48.png)

我们来看一下，In。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_50.png)

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_51.png)

没打印吗，嗯你调的什么啊。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_53.png)

我没有调用啊，你太傻了，我我太傻了，我太傻了，Run。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_55.png)

啊后边会打印好多个现金为零，因为什么呢，因为肯定他每次买100买，买一手，买完之后就没钱了对吧，我把时间调短一点。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_57.png)

这个时间太长了，他最后打印了啊，打印了，但是这个时间太长了。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_59.png)

我把它调短一点，现在是16年1月1号到，比如16年3月1号吧，3月31号啊，2月31号，1月31号吧，一个月短一点。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_61.png)

一个月可能钱还够吧，好有了哎，这个就是我什么呢，我每一天的刚开始第一天10万，第二天18号10万，然后因为呃然后然后是就这些钱，这些钱这些钱对不对，就一直这样来啊，然后这个价格我最后要的不是我的价值。

我要的是什么呢，我要的是不是。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_63.png)

我要的那个图上那个东西是收益率啊，对不对，所以收益率怎么算呢，我这又得开一个收益率这一行，比如说我叫它啊，ratio就比例，它是不是应该等于价值减去最开始的价值。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_65.png)

括起来，再除以最开始的价值，对不对。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_67.png)

那最开始的价值是啥呢，最开始的价值是不是最开始的钱。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_69.png)

你最开始只有现金嘛对吧，所以我这记一下INIT，value就等于等于什么呢，context点cash，最开始的时候钱没有动嘛，对吧好，所以我的ratio应该是等于PLT。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_71.png)

value这一列减去init cash。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_73.png)

init value测试啊，括起来，再除以init value对吧，这个是我用的，相当于这是一个series，这是一个数啊，这也是一个数，用的是批量的那个运算，然后这个完了之后，那我的PLTDF。

ratio就相当于是维护了每一天的这个，收益值对，那我一会再把它画出来就可以了对吧。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_75.png)

好看这有正的有负的，好像负的多一点，就说明这咱们运气不好。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_77.png)

没有办法赔了好，这是PLCDF，那除此之外还有别的吗，我们是不是说过要画两条线对吧。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_79.png)

一条是收益率，一条是基准收益啊，那说到基准收益，刚开始我们这有一个收益。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_81.png)

有一个基准啊，是benchmark，这是none对吧，那我们需要一个什么呢。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_83.png)

set benchmark的函数，比如我写在这。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_85.png)

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_86.png)

这我就怎么样呢，我就直接self点分啊，不是self。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_88.png)

Sorry，Context，点benchmark等于啊，别security了啊，也无所谓，security了，也正常情况下，我们的收益是应该好像指数是有多一点，但是我们这如果指数的话写起来。

那就稍微复杂了，就是你要指数要算一下这个指数的成分股，获取指数，成分股获取指数的权重，那就复杂一点，但我们这就简单为主啊，我们这简化版的嘛都水版啊，我们就什么呢，假设也不是，假设就是这里只支持。

啊一只股票作为基准。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_90.png)

所以这个时候啊基准啊，这个时候你的security。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_92.png)

估计也就传那个601318了，就是因为操作他自己嘛，所以传他自己也是合理的啊。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_94.png)

这个这个我们一般是在initialize啊，Set，benchmark601318好，那这个时候他set完了，就是说这个奔驰Mark现在有值了，那我们接下来是要算基准的收益率对吧。

对我们说算基准的收益率是怎么算的呢，就是假设我第一天把这些钱都拿进去买了股票，然后股价的变化，其实就反映到我的收益率变化上好。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_96.png)

所以我这样写啊，我的attribute data rage history。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_98.png)

这还是要用上了啊，就是我之前的那个给两给两个时间范围，然后传这个啊，传一个股票代码进去，股票代码是context，点benchmark，这是股票时间范围。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_100.png)

就是回测的这段时间对吧，context点start range。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_102.png)

start date和context点n n it。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_104.png)

这就是说明什么，我要求这段时间之内的它的那个历史数据对，把它拿到，比如说我这叫什么这个奔驰啊，奔驰Mark data frame，好那这个是我什么呢，这个是这个是股票每天的价格。

那他最开始的价值是什么呢，最开始的价格初始benchmark in it，是不是等于就是，啊B啊，奔驰马BMINIT，是不是等于BMDF这个data frame里，第一天的那个价格。

嗯啊所以这点儿啊别点了，先取open，然后领啊，用open这个来作为每一天价格的代表。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_106.png)

开开盘价好，那接下来什么呢，我这个BMDF，其实我们的这个参照价格就是这个啊，参额参照的这个是人参照的收益率，就是参照的价格的波动的变化对吧，其实也就是说拿它这么长时间的价格，跟它最开始的价格比啊。

比如说最开始的价格是五块钱，那今天的价格如果是八块钱，那我的收益就是3/5，也就是60。6%就这么来的，所以这个时候哎，我们可以在我们之前这个PLTDF这了，加一列。

什么叫比如说叫benchmark rati。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_108.png)

它等于什么呢，它应该等于。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_110.png)

benchmark data frame里open那一列，open那一二列减去benchmark in it，再括起来除以benchmark in it，哎那这样的话。

我这一列就表示的是我的参照的这个参，参照的这个这个这个什么，这个这个这个这个收益率好，那这个时候我们打印一下我的PRTDF，可以看一下它应该是有三列了啊。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_112.png)

有value这一列，当然value这类我们不用了，用ratio跟什么跟这个benchmark ro这两列，对吧好。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_114.png)

那我接下来把这两列画上来，是不是就可以了对啊，那接下来怎么画呢，画PLTPLTDF，ratio这一列和，奔驰Mark o这一列这两列我这用的是花索引啊，直接点PLOT就可以。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_116.png)

因为我们说过pandas对plot可以有支持，然后PLLT点show就把这个图打印出来了。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_118.png)

好那为了证明我们这个框架写到现在。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_120.png)

这个run写完了，那接下来我们按照就是，其实就是模仿那个距宽的写法，把我们的initialize和handle data，这两个函数就是用户的函数，现在我们开发工作基本上干完了啊。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_122.png)

不知道有没有bug，可能有可能有，然后现在我们就假装自己是用户。

![](img/bc0037efb8b3c1d0e426ed06fb33cffd_124.png)

测试一下，我们把initialize和HANDDA这两个函数写出来，然后看一下画图的效果就知道了，好好吧。



![](img/bc0037efb8b3c1d0e426ed06fb33cffd_126.png)