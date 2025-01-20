# 【量化交易】Python入门之数据分析【2／4】｜ 金融工程 量化金融 - P5：2-4. Python数据分析：Module2-Pandas Structure 数据结构 - Devils-Advocate - BV1RdHAemERq

module two的第三节课，我们来讲一下padas data frame。那么我们如何完成一个data frame呢？那可以看到我这边做了三套 series pannda series呃。

分别是name item和cos。这就说明这三个人johnmarion scott在商店里面买了三种不同的物品，他们分别第一个是keyboard，第二个marymelon mouse鼠标。

第三个scott买了 monitor，然后下面的co分别对应他们的价格。那我把它变成一个excel一样的面板数据，应该怎么办呢？因为至今为止我们学习到的都是单列。那如果把它变成多列数据。

也就是我们的面板数据呢，应该这样做。DF data frame，我们通常叫面板数据就是DF，但是你可以给他其其他的名字了。PDdata frame。然后我们进里面要放一个list。

把我们的purchase123放进去。Purchase E。Purchase R。And purchase sun。然后我们要给它分别一个。分别给他一个这个index。等于。store一。

说明他在就比如说john也是john在story买的，mary也是在sstoreory买的。但是scope呢我们要把它放在stone2。就是第二个商店里面来买。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_1.png)

我们来看一下DF data frame。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_3.png)

那么我们就有呃呃store一对应的john和mary他们分别买的这些东西啊，这样子非常方便展示。那我如果在这里想查询他的数据，比如说我想查询在store2都有谁买了，我们怎么做呢？DF点lock。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_5.png)

嗯。Store 2。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_7.png)

这样我们就可以定位到啊srestore two的scott它有。the name gotcott monitor， and他花了599。5块。那如果想定位到store一，他应该是有两个人的对吧？

那john和mary的名字都在这儿。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_9.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_10.png)

然后我们来看一下它的type是什么东西。它应该是一个data呃data frame。但如果面对到二，它只有一个呢，它就是一个panda series。所以说如果只有单列，它就是se。如果是多列。

它就是pandas data frame。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_12.png)

然后我们可以对data frame做一个变形，就比如说做一个转制，那一般就是用T来表示。我们之前学n派也是转制，也是用T。那么pas这里面也可以这么做。呃。

这边的store呃列的store变成行的store，然后行的呃各种它的name I cost变成列，所以是行列转制。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_14.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_15.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_16.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_17.png)

那么行列转制以后会不会呃如何再做定位呢？那么也是一样的，做lockuck。比如说cost。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_19.png)

那就可以定位到所有的价格来。呃，所有的各各类商品的价格。那么DF的考虑，如果不做转制，它是否也能进行定位呢？那其实也是可以的DF因为你仔细想想，我们才开始它的cost就是就是这一列吧，对吧？

所以如果直接定位到它的这个cost的，我们也能拿出东西。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_21.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_22.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_23.png)

那我们如果想定位到某一个具体的数据呢，就比如说这个105cost，然后再后面再加一个。Store one。那就可以是这样。但是一般来说我们一定要把lockuck加上。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_25.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_26.png)

但是加log的话，我们就需要这样子sure需要用这个store一就是我们的这个索引在前面，然后它的列名在后面呃，用来做log。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_28.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_29.png)

当然I like也是可以的。DF点I like。00对吧？

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_31.png)

这样如果是030203朝范围了。02就是表示它在。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_33.png)

第零行store一里面的。这个012对吧？105。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_35.png)

所以这是Ilog做定位。那。我是不是可以定位多行，比如说DF。如果我想呃我想把。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_37.png)

name和cos都拿出来，但是。我想要所有的store的数据应该怎么办？

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_39.png)

就比如说。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_41.png)

name和co这两个列，但是。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_43.png)

所有的所有所有行数据。应该怎么办？

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_45.png)

呃，他们首先DF它的定位应该是。所有的。所有的行行在前面，列在后面，然后列呢我们再给它一个呃这个方括号。然后是cost。所以这样子我们就。这个。这个冒号表示我接受所有的数据，所有的列数，所有的行数据。

然后这边是我只要name和co的两列，所以以此类推，相信大家应该有了别的花切的办法。花式切分。我们之前在讲n派的时候也讲过。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_47.png)

呃，那么如果想drop某一列呢。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_49.png)

DF点drop就是我把这一列去掉。嗯，再来看一下DF这个。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_51.png)

就比如说我想drop掉。第一列第一行第一行。就是d。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_53.png)

do one，但你看它返回的值。返回我们直接返回了一个store to，对吧？那所以这已经是我们d掉的一个后果。那我们真d掉了吗？



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_55.png)

那其实没有，你只是只是它这个是这样的返回的。所以我们要怎么做呢？我们首先要对它之前我们讲的copy的概念。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_57.png)

讲呃我们先对它进行一个copy。然后。Copy， dear。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_59.png)

这样我们就给呃给data frame做了一个深度拷贝。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_61.png)

那么我们可以看一下深度拷贝，它就是DF的一模一样的对吧？但是copy。点。我们我们从这个拷贝上把它的store one给d掉。这样我们就它的copydF应该留下来留下来的是store two。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_63.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_64.png)

所以我们这就是如何把我们d的东西保留下来。我们现在回头看DF，但仍然是。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_66.png)

嗯。它仍然是它仍然没有变，对吧？所以这个做了深度拷贝以后，它就是不会影不会影响他之前的。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_68.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_69.png)

这个他之前的这个。Data frame。我们再来看一下另一个。我们比如说我们有了copyDF，我们先把这一列把它的名字删掉，我们应该怎么做？delete靠BDF。



![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_71.png)

Name。我们进来看一下靠PDF。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_73.png)

这样子的话就把它的name给这一列给去掉了。那我如果想再加一列呢，就是比如说copy，我用DF吧。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_75.png)

可以看到DF还是这样的，但是我想加一列location。Df。location，但是他们的这个地方地址我暂时不知道，我先给他一个noun，他们给来看一下DF长什么样，就是我们加了一列。

但是它全都是nun的一个东西。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_77.png)

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_78.png)

那么这节课查呃data frame我们暂时讲到这儿。

![](img/9bf7f248d5c1c438cb937e0c5c83c6e6_80.png)