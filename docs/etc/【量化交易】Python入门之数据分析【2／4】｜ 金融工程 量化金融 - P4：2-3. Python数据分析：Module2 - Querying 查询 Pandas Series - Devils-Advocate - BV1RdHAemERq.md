# 【量化交易】Python入门之数据分析【2／4】｜ 金融工程 量化金融 - P4：2-3. Python数据分析：Module2 - Querying 查询 Pandas Series - Devils-Advocate - BV1RdHAemERq

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_0.png)

那么这节课我们讲一下pandadas的查询，queing a panda theory。我们首先有了一个字典，sports的字典，然后我们把它塞到一个seerious里，我们就会得到一个字典和。

我们就会得到一个andnda siri，它有着 tennisnis baseball这样的。运动来做它的索引，然后对应的国家是它的值。那我如果想查brazil，我想把brail这个值拿出来。

应该怎么做呢？我们可以用用一个定位的方法S点。I log这边的log就是location，I表示它用数字进行索引。那所以我们看一下012brazil在第二位，我们就是I log2。

就是得到了brazil，那我们可不可以按它的这个索引呢，那也是可以的。比如说S，那这时候就直接用log就行了。location。那么我们放比如说。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_2.png)

soccccer那也能查到bra Brazil，那 baseball呢。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_4.png)

对应的japan，所以这个可以的那。以前有的很古老的方法，这边我觉得也可以讲一下S3。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_6.png)

那在后面的pyython版本里面，比如说pyython3。2或者是3。3的版本，可能这样已经不行了。那么这边我也拿到了future warning这个定位的方式已经被deprecated。

就是未来将会取消。所以请大家以后不要这样用，就是你可能在你现在的pyython版本里面还可以，但是在未来呃这个版本这种方案将不再能适用。然后你也会呃你之前写的代码也就不能再复用了。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_8.png)

所以这边大家注意一下。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_10.png)

然后除了呢。str作为索引，我们可不可以拿数字作为索引呢？那么也是可以的。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_12.png)

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_13.png)

我这边有一个做好的pennda seriesri。可以看到，比如说99吨于USA100吨于japan101对于braale，那这边就是用数字做的索引，但是用数数字做的索引。

可不可以用比如说我刚才的上面这种方法索引到它呢？就因为它是数字嘛，那我。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_15.png)

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_16.png)

所以99。可以得到USA那我如果想。想用零呢，就比如说我想索引到第一个这个USA呢，可不可以这么办呢？那其实是不行的。嗯，也所以这样子就会有一些confuion。如果我不写log和i log的话。

那这里我最好还是用I log加上那就是USA，那如果是log的话，就是99。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_18.png)

也是USA100。如果用I log的话，就是一。嗯，所以用log和i log之间，这样就不会有混淆，不会有confusion。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_20.png)

那我们再来看一下。panda series中的计算，比如说我们有一个sries S，它有这样的一些数字。呃，有一种方法呢我我想把它们都加起来，那么。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_22.png)

如果你不知道那个sum的函数应该怎么做呢？如果用一个for循环，那么可以先用total。等于0做一个累加嘛，我就循环到这里的每个数字forI inS。等不懂。Toal。加。白en。

这边的total加等iteen也等于total等于total。加I。这两个是一样的。所以简化一点，大家一般就是加等I就行了。然后我们再来。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_24.png)

Prunning一下 total。等于324。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_26.png)

那如果用直接用some的方式呢，import non派 SNP。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_28.png)

呃，都头等于一个能派点上S。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_30.png)

这样是不是也能得到324呀？那这两个是有什么区别呢？区别就在他们的运算时间上。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_32.png)

比如说我想。做1万次的运算。那这样两个加起来。这两种方法呃做累加哪个更快一点呢？S等于PD series。我先generate的1万个数MP。Ran。1万个。1万个0到1万的随机00到1000的随机数。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_34.png)

那么这是1万个数，可以看到lesss等于1万，然后它是integer。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_36.png)

然后嚟。看一下它的时间。没有我们这样来计算。计时summary等于0。我I in S。Summary。加等S。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_38.png)

加点 time， itemen，加点 itemen。然后这边用了376微秒。那同样的方法。来计算一下summary。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_40.png)

等于MP点3S。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_42.png)

这边用了9。96微秒，那么大家可以看到这边差的就是。它的差距非常大，所以说。呃，这也当然这也看电脑性能可能性能越差，差距越大。所以说呃如果能用函数的方法，我们直接用函数，能用n派。

我们直接用n派n派的计算，通常超过呃for循环啊，或者用pandas自己的计算。呃，讲到这个，我们再回过头来看一下我们前面的。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_44.png)

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_45.png)

Jig。这里。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_47.png)

我们如果想修改它怎么办？就比如说我想在最后再加一行，那么我们可以这样子哎点lock啊，这边不是102england吗？我再加一个animal吧。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_49.png)

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_50.png)

Animal。等于。Bs。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_52.png)

来看一下，所以这边其实是可以混搭的。它这个缩引呃，我们前面这个数字啊。

![](img/d6b0b6890984dfbb07b02c33c5e63aaf_54.png)

数字它也可以混到这个str，它的这个str里面去。所以说这基本上是我们pannda seriesri的查询了。



![](img/d6b0b6890984dfbb07b02c33c5e63aaf_56.png)