# 【量化交易】Python入门之数据分析【3／4】｜ 金融工程 量化金融 - P5：3-4. Python数据分析：Module3-Pandas 时间和日期 - Devils-Advocate - BV1vVHveqEJH

接着之前这节课我们仍然讲pas，但是我们讲pas中间日期和时间的应用。那么首先inport一下n派和PD。我们看一下，如果我们要选择一个pandas里面的月份。比如说2024年1月。PD period。

12024。然后我们会给到他这个perry这个方法，perry的202024。然后1月份这变M代表mons。那如果我想选择到day呢，那就是PD periodd。然后3月5号。



![](img/7e8207fbbada1281bc2125c31ade7638_1.png)

2024。那么这就是我们选到day了。那么我们还有daytime的呃一个format。比如说我们可以generate一个daytime index。X等于PD series。

就是panda series，然后list。A b c。这个类似的ABC就是你这等于一个方括号ABC单独的exttrain，然后我把它。给到一个pas的timet。然后同样的我们可以给到他。

因为我们ABC嘛有3个。

![](img/7e8207fbbada1281bc2125c31ade7638_3.png)

2月1号3月1号，那我们来看一下X。那这就是我们的呃panda series，然后我们把padas的timet放在前面作为index。



![](img/7e8207fbbada1281bc2125c31ade7638_5.png)

然后我们来看一下它的index type。X的 index我们可以看到，这就是daytime daytime index。那么。



![](img/7e8207fbbada1281bc2125c31ade7638_7.png)

然后我们就来看一下如何把。一个str变成一个daytime format。比如说我。202401。01，那么这个应该是一个train，对吧？那如果在一个pas的 data frame里。



![](img/7e8207fbbada1281bc2125c31ade7638_9.png)

像这样，我有一个一整个data frame，那它的前面。Type。

![](img/7e8207fbbada1281bc2125c31ade7638_11.png)

Date。DF。然后我们我们选择data的第一个，那它就是一个str啊。那我们应该怎样把它变成一个d time呢？呃，其实data frame呃pas data frame内置了，说d。

等于 pan us to date time。然后DF。d那么我现在拿了这个DF的date，也就是我们上面这个str。呃，这一堆 string的 series。

然后把它转化成to datetime format，然后我们复制给了DFd。

![](img/7e8207fbbada1281bc2125c31ade7638_13.png)

那么我们再来看一下这个。

![](img/7e8207fbbada1281bc2125c31ade7638_15.png)

那它是不是就是一个time stamp啊？其实表面上你可能看不太出来，这跟之前的涨涨是一模一样，但是它的性质已经变了。因为train你没法给它排序。



![](img/7e8207fbbada1281bc2125c31ade7638_17.png)

那么我们后面如果做到了这种时间序列的问题，那么我们需要给这个date做一个排序的话，那么我们就会用到这个time stamp的东西，所以所以的话我们就会需要用to date time来给它呃做一个转化。

然后还有包括还有一个timetime deta的问题。就是它之前会有差异，就是他们两个时间之间会有差异。比如说time stamp。



![](img/7e8207fbbada1281bc2125c31ade7638_19.png)

![](img/7e8207fbbada1281bc2125c31ade7638_20.png)

![](img/7e8207fbbada1281bc2125c31ade7638_21.png)

![](img/7e8207fbbada1281bc2125c31ade7638_22.png)

9月4号2025。我们是可以减去。一个 timet。10月4号2025，那么这边是负的30天。那么我们也可以加上一个。具体的时间比如说8点10分。A。11点PM。可以这样子做，直接把时间也给加上。

这又精确到小十分钟了。对吧然后我们还可以干嘛？我们还可以直接加上一个time deelta，就是你不能直接加一个str pDtime delta。但如果你想比如说再往后加上12天3小时。



![](img/7e8207fbbada1281bc2125c31ade7638_24.png)

那么我们可以就这么做。

![](img/7e8207fbbada1281bc2125c31ade7638_26.png)

啊，这边我们小时不能。用大写的用小写的。

![](img/7e8207fbbada1281bc2125c31ade7638_28.png)

12天3小时，那么我们就变成9月4号到9月16号。那这就是我们的time delta，然后它中间的差值呢，它也是一个time delta。



![](img/7e8207fbbada1281bc2125c31ade7638_30.png)

然后我们还可以用它来生成一个日期。比如说PD。Date range。我们从。10月1号。2025。开始period。periods等于10生成10个日期。Frequency就是 frequency。

用 two weeks。

![](img/7e8207fbbada1281bc2125c31ade7638_32.png)

然后从一个sunday开始。我们来看一下 date。

![](img/7e8207fbbada1281bc2125c31ade7638_34.png)

那么这里我可能要解释一下two weeks和这个s是什么意思？two weeks表示啊它是一个白wely，就是两个星期之间，就15号。到19号，那么是14天。19号到10月2号之间也是14天。

所以这是一个by weekly two weeks那一个。11个week或者3个week，大家应该都知道怎么办了。这sunday就是我们从。星期日开始。那么25年10月5号呢，大概率也是一个星期日啊。

pers ten就时生成10个啊，这个就是开始日期。但你看我们并不是从10月1号开始的，因为我们要sunday嘛，那就是往后推算。看他第一个周日是什么时候。那这是我们的to date range。



![](img/7e8207fbbada1281bc2125c31ade7638_36.png)

然后我们再来讲一下时间日期的重新采样。重采样。

![](img/7e8207fbbada1281bc2125c31ade7638_38.png)

Example。这个在时间。时间序列里面也是比较常用的。比如说我先gene一个date range。I'm going to start。From2021。2024。你一。0。End。到2024。

0107吧。fck等于H。frency就是H1小时际啊，这仍然要用。

![](img/7e8207fbbada1281bc2125c31ade7638_40.png)

小H。那么我们可以看到我们应该generate到了很多145个。

![](img/7e8207fbbada1281bc2125c31ade7638_42.png)

这样的date range，然后呢。我们要再加一些数字。

![](img/7e8207fbbada1281bc2125c31ade7638_44.png)

地答。等于NP run。When in length date。这个len就是145啊，我要生成145个数据。



![](img/7e8207fbbada1281bc2125c31ade7638_46.png)

然后我们把它放在一起DF等于PD。Different。Data index等于 date range。然后columns给他们命一个名。



![](img/7e8207fbbada1281bc2125c31ade7638_48.png)

valueue。我来看一下DF。那这就是我们145个数据呃，对应的这些随机数，我们要给它重新采样。就比如说现在我们现在是orly吧，对吧？那我们要把它算成daily。



![](img/7e8207fbbada1281bc2125c31ade7638_50.png)

应该怎么办？然后这个数据呢，我们要把它就是我们从就这一天有24个小时嘛，有24个数据，那这个数据我们要怎么办呢？我要把它给加总起来，应该用DF resample。



![](img/7e8207fbbada1281bc2125c31ade7638_52.png)

佢地。然后用一个s。

![](img/7e8207fbbada1281bc2125c31ade7638_54.png)

这样就行了。然后我们就是按天来的那除了day，除了这个s还应该还可以变成什么，也可以变成me。

![](img/7e8207fbbada1281bc2125c31ade7638_56.png)

或者是。Minimal。Maximal。这可以用在哪呢？同学们大家可以思考一下，就比如说我有。嗯，我取取股票数据，那么最好的应该取什么？最小的时间单位。但是我们想把我们又想要。呃，每天的按天来的这个。

嗯，这个数据那应该怎么办呢？我们就把它重新采样一下，然后呃最高值就用max最低值用m，对吧？那开盘价和收盘价之类的这边嗯这边大概大家可以思考一下怎么用。那这就是我们在时间序列中非常重要的一个功能。

就是resample。

![](img/7e8207fbbada1281bc2125c31ade7638_58.png)

这节课就先到这儿。

![](img/7e8207fbbada1281bc2125c31ade7638_60.png)