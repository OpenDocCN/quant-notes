# 【量化交易】Python入门之数据分析【3／4】｜ 金融工程 量化金融 - P2：3-1. Python数据分析：Module3-Pandas merging 数据合并 - Devils-Advocate - BV1vVHveqEJH

欢迎大家来到weake send的学习。这节课我们继续讲data frame，但是是data frame的一些其他操作。这里我们讲到data frame的合并，那么合并呢可以根据不同的键。

比如说链来进行啊不同类型的合并。比如说内连接 innerer做连接left and右连接right and全连接是aler。

那么我们首先input一下paas panel SPDand这边有两个data frame。

![](img/6e8c2113b6be5189d27504cdeeb09093_1.png)

那么怎样做我们的merge呢？mge就是就像上面说的，把它两个结合在一起。那么我们先看一下DFE长什么样。



![](img/6e8c2113b6be5189d27504cdeeb09093_3.png)

DF2长什么样？这边是ABCDBDEF那么BD是重复的AC和EF分别是DF1和DF2里面单独存在的那我们把它进行内连接是什么意思呢？那就是我们只保留BDEF和。AC这边他们独呃独自存在的东西。

他们都会被舍弃。

![](img/6e8c2113b6be5189d27504cdeeb09093_5.png)

呃，那么们比如说result等于先复制个resultPD merge。然后我们先敲DF1DF2，然后我们用哪个。我们有哪一行作为索引进行合并，那这个就是我们的on。嗯。

key因为我们bo both data frame两个data frame都有key这个。这一列，所以我们 merge on key。然后我们来选择一下how我们这边选择in there。

然后我们来看一下result长什么样。

![](img/6e8c2113b6be5189d27504cdeeb09093_7.png)

那么就像我之前说的，我们这里有BD，然后其他单独的都被舍弃了。那如果是。

![](img/6e8c2113b6be5189d27504cdeeb09093_9.png)

好腿了。al就是我们包括了他们所有的元素，这就叫全链接。

![](img/6e8c2113b6be5189d27504cdeeb09093_11.png)

![](img/6e8c2113b6be5189d27504cdeeb09093_12.png)

全合并。对吧那么就是AABCDEF。但是注意到我们这边。

![](img/6e8c2113b6be5189d27504cdeeb09093_14.png)

DF1它的valuevalue的话和第二DF2的value，它的collons都是一样的。那么为了做区分呢。



![](img/6e8c2113b6be5189d27504cdeeb09093_16.png)

![](img/6e8c2113b6be5189d27504cdeeb09093_17.png)

这边在合并的时候，它单独加了一个后缀呃，value。呃，下滑杠X，然后valueslash Y呃，对于我们作为区分。那么还有其他的方法，比如说left，那就是只看DF1，因为DF1在DFDF2的右边。

那么就是DF1DF一有的就都有DF2有的不一定有。那right自然就是全部反过来喽。那么这边就是BDEF，也就是DF2所含的所有东西。



![](img/6e8c2113b6be5189d27504cdeeb09093_19.png)

![](img/6e8c2113b6be5189d27504cdeeb09093_20.png)

那么还有一种合并的方法。我们来用一下DF3和DF4，这里我们用LK和RK，就是在它的coon的名字不一样的时候，我们应该怎样合并呢？我们也是把它复制给result。



![](img/6e8c2113b6be5189d27504cdeeb09093_22.png)

![](img/6e8c2113b6be5189d27504cdeeb09093_23.png)

等于PDmarriage。嘅三。DF4。left on注意我们就不是on了，我们用left on。左边DF3，它是on L key left key。Right on。这边就是RK。

那么how我们仍然选择iner吧。

![](img/6e8c2113b6be5189d27504cdeeb09093_25.png)

我们看一下result。那么这边 left onLK，然后valueX。right on也是BD，那么value是56，所以说我们仍然是合并了它，但是这里的这里的合并呢，我们保留了两个。



![](img/6e8c2113b6be5189d27504cdeeb09093_27.png)

呃，两个key它的con，然后仍然有两组value。一个是24，一个是56。那么可能有人会问我，这边的后缀，这边value X和valueY这下滑杠X和下滑杠Y我们是不是可以变化呢？那么其实也是可以的。

我们重新来两组data frame。

![](img/6e8c2113b6be5189d27504cdeeb09093_29.png)

然后呢，我们用result。作为它的赋值的名字，然后我们用一下merchDF3。DF4。how我们选择outer。选链接，然后我们。呃，要 on key。

因为这边我们就没再使用left和 right那个 key了。然后这里我们要选一下suffix。suffixes，然后我们使用。比如说。第一个data frame用下滑杠DF3。

然后另外一个我们就只能用下滑杠DF4了。这样的话我们就会得到。

![](img/6e8c2113b6be5189d27504cdeeb09093_31.png)

Result。这边是DF3DF3，然后DF4DF4。

![](img/6e8c2113b6be5189d27504cdeeb09093_33.png)

![](img/6e8c2113b6be5189d27504cdeeb09093_34.png)

那么这节课就到这儿。