# 比刷剧还爽！公认最全的Python金融分析与量化交易实战教程，从编程基础到金融量化实战，全程干货讲解，学完即可就业！——人工智能／机器学习／数据分析／数据可视化 - P43：【Python金融量化】43-获取给定区间全部数据( - 迪哥的CV课堂 - BV1nF4m1T7qA

![](img/872f979d8e9af46b39c55c32ffa8dbf2_0.png)

再写一写啊，是不是说现在唉你的一个日期，它是一个序列，然后你会查其中一天，那你会查其中一天，那每一天，那说白了咱写个for循环呗，for i in ranch一下Rush什么，咱们当前就看一看。

一共我是有多少天就行了好了。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_2.png)

你这个序列你不是有这么多天吗，看你这个日期呢。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_4.png)

日期在上面看看日期一共多长，那相当于是有多少天吧。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_6.png)

便利其中呢我的每一天数据，然后呢对我每天说句话，都要我都要干什么。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_8.png)

都要去获取一下当前它的一个值吧，好了，我这块直接复制就行，对于每一天的数据。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_10.png)

我都要获取它的一个值哦，只不过这回这回这里边它就是不是传一个零了，而传什么，应该不是应该是传一个I是吧，获取它第I天实际的一个值，然后他对值来说，它返回的是一个三维的，我不需要还是IOC一下。

LOC当中第一个指标就是一个零二，然后第二个也是零二，然后第三个指标去全部啊，因为有用的全在第三个指标当中吧，刚才这个shape值属于大家打印来看了，这样我就能取到当前诶。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_12.png)

它的就是每一天他的一个数据了，那行吧，那取完每一天的数据之后，那我最后啊你不能只把每一天都告诉我，你是不是要做一个汇总啊。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_14.png)

我希望能这样，我做一个数据啊，是这样啊，第一个维度它是一个日期啊，代表它是哪一天，209年3月8号，然后第二指标，第二指标可能是它的一个股票的一个名字是吧，然后第三个指标可能是它的一个实际指标值。

一个value到底是等于多少吧，那我是不是说我得构建一个新的大点data frame。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_16.png)

然后呢我这里读完每一天数据之后。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_18.png)

把每一天数据，把每一天数据拼接到哪啊，拼接到我当前组成的一个整体的一个data frame。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_20.png)

当中吧，Fighters，然后呃fetters的一个data吧。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_22.png)

等一下呃新建一个data frame。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_24.png)

一会呢咱拿这个data frame往里去传数据啊，我说先构建一个这个就是总的啊，就是一个总表吧，然后这个就是一个每天的每天的数据好了，那现在我们已经有了一个每天数据。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_26.png)

然后呢在这里我们先给它指定一个列名吧，在这里，我说我现在也是重新的去创建一个data frame嘛。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_28.png)

然后一会对data frame进行一个拼接操作好了。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_30.png)

我说当前我的一个data啊，等于一个新建一个data frame，新建一个data frame，然后在我当前的data frame当中啊。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_32.png)

我看一看当前pandas中哦，panda当中我直接把data frame导进来了吧。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_34.png)

所以说在这里可以直接去用哦，再创建一个新的data frame，然后呢我就把实际它的一个值诶，给它传进去就行了，然后这个给它起个名字吧，它就是一个这个FM了，不是这么一列数了啊行了。

咱们现在有了一列值了。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_36.png)

有一页纸还没完，还有什么咱得给它起个名字，这个列啊你得告诉我它叫什么名字是吧，咱们自己来起一个啊，呃起出名都行。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_38.png)

我们来写一个等于它的一个名字传进去，它就是哎这个factor。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_40.png)

它的一个实际指标值等于多少吧，好了这样我们现在创建一个data frame，当中只有一列数据，哎我们还给它起了一列名字，那我们刚才说啊，就是在这个DFM当中啊，哎呀你不光定个值。

你是不是还有得有一些日期的一些信息啊，好了我说这样你再新加一列吧，新加一列，我说指定名字就是一个日期，日期等于什么，在这里哎你说我们现在有没有它是哪一天啊。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_42.png)

是不是当前遍历到第二天了，我把第二天数据加进去不就行了，这样我现在构建了一个哎就是每一次循环当中。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_44.png)

我都会构建一个data frame，这个data frame有两列，一列呢就是我的一个日期。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_46.png)

一列就是它的一个value值啊，咱们也有了吧，好了，那我说我现在啊哎呀有了所有的操作了，那我那我是不是应该怎么样。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_48.png)

把这些个数据做一个拼接操作，怎么拼接，你for循环每一次都得到一个新的data frame。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_50.png)

你是不是把每个data frame放到这个总表当中啊，最后我要的是什么，就是这样一个总表吧，好了再来执行拼接操作，pandas点contact一下呃，拼接拼接当中你需要传递参数，谁跟谁拼呢，好啦。

先把咱们呃最开始我说我构建的1data啊，拼到我这个总表当中，把谁拼上去呢，咱刚才是不是自己哎。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_52.png)

我构建了一个data frame，把咱们当下这个data frame给勾进去，我说拼接成啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_54.png)

拼接到总表中吧，行了，这就是执行一个拼接操作呃。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_56.png)

我们先来执行一下，看有没有什么问题啊，这一块的速度肯定会比较慢哦。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_58.png)

因为这里它是咱们现在指定什么，我们是指定了一个呃。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_60.png)

时间间隔是有这么一年吧，19年1月1号到这个20年1月1号。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_62.png)

时间间隔会比较久，所以说它的速度相对来说会比较慢啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_64.png)

到时候大家自己玩的时候啊，要不就没没有说完就没有后话了，大家自己玩的时候也不用了。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_66.png)

也不用再改小了，一年这个时间挺快的，很快就出来了。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_68.png)

好了，说完之后再打印一下当前head，看看跟我想要的是不是一样的啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_70.png)

哎呦这个data frame当中总体来说有点问题，再来检查一下这一块拼接完。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_72.png)

拼接完之后再疏忽了一点什么，这个表时间是啥也没有，我这个拼接完就是光拼了，怎么样，没赋值吧。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_74.png)

咱们是不是得重新赋值啊，要不然相当于这个表始终没东西吧，这不行，咱再来再重新执行一下啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_76.png)

这回重新执行完之后，咱再点还得看一看当前啊，我们的一个表当中是不是按照我的一个想要的，有我的一个日期，然后有它实际指标的一个值。



![](img/872f979d8e9af46b39c55c32ffa8dbf2_78.png)

然后还你还得还得有什么，还有这里有当前这个股票它是什么吧。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_80.png)

我们需要这几个指标来看一看呃，稍微再等几秒啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_82.png)

咱们就来执行一下，好啦，你看一下这些是不是我们想要的股票啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_84.png)

这具体是什么，不管了，他的一个值是不是也有了，它的日期是不是也有了，这样是咱们现在完成第一步哎。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_86.png)

把我们的数据啊全部给它取出来了，取的过程当中啊。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_88.png)

其实挺麻烦的，但是也没什么好办法，你不能就是有个HANDBAR自动一天天给你执行。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_90.png)

所以说咱必须得自己完成这样一个操作。

![](img/872f979d8e9af46b39c55c32ffa8dbf2_92.png)