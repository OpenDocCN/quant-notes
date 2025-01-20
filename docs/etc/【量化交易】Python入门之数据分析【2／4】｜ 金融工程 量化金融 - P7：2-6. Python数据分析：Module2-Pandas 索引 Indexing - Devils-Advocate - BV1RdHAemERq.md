# 【量化交易】Python入门之数据分析【2／4】｜ 金融工程 量化金融 - P7：2-6. Python数据分析：Module2-Pandas 索引 Indexing - Devils-Advocate - BV1RdHAemERq

紧接着上一个视频，我们讲了data frame的。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_1.png)

一些选择方法。那么这里呢我们来讲一下它的。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_3.png)

indexing它的索引，如果你没有import的话，我们在这里import一下pandas SPD。



![](img/74bd2fb9e97ebe25d1c7502ab653a16d_5.png)

那么我们现在有了泰坦尼克号这1个CSB。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_7.png)

我们需要做什么呢？我们想把它的这个我们的索引不是0123456789嘛，然后我换一个索引。我如果想。用。比如说它的name作为索引，可不可以呢？你这么做。DF等于 DF set index。这边座位。

name作为它的索引，然后我们来看一下。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_9.png)

那这里name就把它变成了我们的索引值。那么我们可以干什么呢？

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_11.png)

比如说我们每次做一个选择，DF等于。嗯，来选择H还是拿H来做吧。H。小于等于25。这样的一个人，他们都有谁呢？比如说我想看一下。



![](img/74bd2fb9e97ebe25d1c7502ab653a16d_13.png)

那么这里的name仍然在最前面，所以呃这算是用索引值的一个好处吧。就是我们能一直观察到我们想要的信息放在前面作为索引。然后我们可以看一下unique value。

就是我们这边有DF里面到底有多少一个不同种的。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_15.png)

H。就是他分他它的分布。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_17.png)

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_18.png)

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_19.png)

啊，也不是分布哈，他比如说有2个22岁的人，那我这里只会显示一个，你的直接是unique。呃，我们可以看到还有一些0。67，那这说明他就是一个小婴儿嘛，对吧？那么我们其实也可以st一个复合索引值。



![](img/74bd2fb9e97ebe25d1c7502ab653a16d_21.png)

比如说DF set。Index。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_23.png)

然后这里加上方括号，我想用。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_25.png)

是。Hge。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_27.png)

和。性别来作为它的复合索引值。那这样也是可以的，或者是我觉得我可以把它反一下，先用先用性别再用H。那么可以看到这边，比如说mail里面有22和2岁的这。



![](img/74bd2fb9e97ebe25d1c7502ab653a16d_29.png)

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_30.png)

应该是两个人。啊，这样子的话。他有时候没尔会把他框框进去更多的人，然后在不同的年龄。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_32.png)

然后我们回到前面，重新读取一下DF，把它复位一下。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_34.png)

这样。然后我们来看一下怎么处理我们的missing value前面。呃，我们说了可以做。drop and a我们可以把它d掉。那么我们是否还有一些别的办法呢？我们可以把它做一个forward fill。

怎么说呢？就是呃把它向前填充，来看一下DF。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_36.png)

Cavin。Phill and they。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_38.png)

然后 methodod我们可以用。F fail向前填充。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_40.png)

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_41.png)

那么这边就向前填充了哈，这边是我可以看一下原始原值。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_43.png)

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_44.png)

cabinbinC85C85就是跟它跟上面一个，如果后面咱后面有1个NA，它会跟上面一个最近的上面的一个非NA的值跟它一起填充。这边C123，后面紧跟着两个是NA的。

然后这边我们可以看一下这两个C123就紧跟着它这个填充。那第一个仍然是NA，那这也是非常正常的，因为它之前是没有数的，所以它这个NA仍然是NA。



![](img/74bd2fb9e97ebe25d1c7502ab653a16d_46.png)

那有forward fill，那肯定就有一个向后填充嘛。back啊back fell。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_48.png)

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_49.png)

对吧。那么这样子的话，第一个就会拿后面一个的数进行填充，然后这边也填充成C123。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_51.png)

当然在这里可能没有什么意义。那么我们做其他的东西的时候。呃，它可能会有就是在别的场景下，它会有它特定的用处的这会需要你们碰到不可呃不可能数据自己来使用一下。当然这边我们3。1已经开始warning了。

这个这个me会被deprecate掉，会被取消掉。W是 backfil forfil。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_53.png)

呃，他会直接用。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_55.png)

F fell这个方法也就是F fell。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_57.png)

讲。这样就没有问题了。然后back sale就是。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_59.png)

这样。那么这是向前填充和向后填充。

![](img/74bd2fb9e97ebe25d1c7502ab653a16d_61.png)