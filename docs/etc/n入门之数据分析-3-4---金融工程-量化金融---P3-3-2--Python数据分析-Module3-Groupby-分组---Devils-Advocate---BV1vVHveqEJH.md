# 【量化交易】Python入门之数据分析【3／4】｜ 金融工程 量化金融 - P3：3-2. Python数据分析：Module3-Groupby 分组 - Devils-Advocate - BV1vVHveqEJH

这个堂课我们讲一下pyython pandas里面的goodbye操作。那goodbye是pyython中的分组功能。我们可以对它进行聚合的。比如说求和平均计数。

那么这边我们会给大家展示一些比较常用的聚合函数。首先我们先create一个data frame。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_1.png)

可看一下我们的late dream长什么样。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_3.png)

category是由AB组成的一列。然后values是它们对应的不同的值。group by呢就是对它分组。那么我们首先group等于把它分成AB两组嘛？那分成AB两组怎么办呢？那A组总共多少？

B组总共多少呢？

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_5.png)

我们来看一下DF group。Bye。Category。然后我们用你的s函数。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_7.png)

然后我们就能知道group是多少。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_9.png)

那么。A列A类，那么它的总共的值是90，B类总共的值是120。除了sum函数呢，我们还可以用me。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_11.png)

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_12.png)

平均值。还可以用count来作为计数。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_14.png)

A组有3个，B组有3个。那么我们现在只有一一个索引，如果我们有多个索引，应该怎么办呢？

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_16.png)

假如说我们不仅有category，还有type。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_18.png)

I can help the data frame。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_20.png)

category type那A组里面就可能有X或者Y，那同理也是B组。那么我们如果要对它进行goodby。grouproup等于DF group。对因为这可能就会有很多组。有不同组合嘛。

所以我们gr by。Category。和。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_22.png)

Type。然后再进行上。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_24.png)

不那就是。A类里面有X型和Y型，它们分分别的。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_26.png)

和是60和30同理B。嗯，那那当然也有呃除了sum以外的其他的一些。刚才我们已经说的someum包括some。



![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_28.png)

还有命。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_30.png)

Count。然后这里再讲一下别的，比如说me。mininimal就是最小值。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_32.png)

然后可能还有max。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_34.png)

接大而知。他们就是这一类里面最小值这一类里面最大值。当然这有多个的情况下。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_36.png)

还有什么？还有standvation标准强STD。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_38.png)

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_39.png)

我单独写一个吧。STD。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_41.png)

standandvation，然后还有variance。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_43.png)

方产。这边是标准差，这边是方差。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_45.png)

然后甚至我们还可以自定义一个函数。比如说。我想做一个custom的agggregator，就是我们把它加起来以后，再对它乘以个2，那应该怎么做呢？DF我们定义一个函数cast。Aggregator。

这里面是series，它是panda series，所以我们叫它s。Return。一个 seriesries的。一个sious，然后我们要把它s起来，对吧？然后乘以2，就是我们s米以后它的两倍。

那么继续呢我们可以got。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_47.png)

Df goodbye。Goododbye。Category。然后我们放上自己的custom。Agregator。



![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_49.png)

可以看一下group。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_51.png)

那么可以看到证明很有意思的是，他把这个X和Y都放在一起。但因为毕竟我们group by只group by category了嘛，然后他把加了，他把这个加起来。

但甚至吧它也应该是乘以了28XYX然后这边是呃对应的。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_53.png)

如果只把它加起来，be by category。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_55.png)

上了。这样我们可以对比一下。

![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_57.png)

这边的type明显是乘了一个2，然后90和180120和24，然后这个它也乘了一个2，也很有意思。因为他把这个str也做了个计算。然后本堂课我们的goodby就讲到这里。谢谢各位。



![](img/ab50be52a7ee1ccf3b07e5d294ce2b23_59.png)