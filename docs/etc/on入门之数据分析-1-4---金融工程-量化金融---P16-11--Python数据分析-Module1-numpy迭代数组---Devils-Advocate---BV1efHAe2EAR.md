# 【量化交易】Python入门之数据分析【1／4】｜ 金融工程 量化金融 - P16：11. Python数据分析：Module1-numpy迭代数组 - Devils-Advocate - BV1efHAe2EAR

这里我们讲一下数据的复制。比如说我如果想让R等于R。的。一部分。

![](img/d3cd592e4396ecb8b3270a5da950de0d_1.png)

那么我们的R是前面是这样的一个数呃，矩阵R呢？

![](img/d3cd592e4396ecb8b3270a5da950de0d_3.png)

这是这样子的。

![](img/d3cd592e4396ecb8b3270a5da950de0d_5.png)

012一直到这儿切了这一部分出来。那我如果把R。所有的数值都变成0。

![](img/d3cd592e4396ecb8b3270a5da950de0d_7.png)

那我们看一下。

![](img/d3cd592e4396ecb8b3270a5da950de0d_9.png)

我们先看一下2。那它是那R变了嘛，就是R是R切出来的嘛，那R是否会变。那一般的来说，逻辑上来讲，就是正常人的逻辑上来讲是不会的。但是在pyython里面其实是会变。



![](img/d3cd592e4396ecb8b3270a5da950de0d_11.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_12.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_13.png)

就比如说这里它全变成了0，那是如何让R变成一个单独的东西呢？

![](img/d3cd592e4396ecb8b3270a5da950de0d_15.png)

那我们就要用到copy这个东西，比如说R copypy。等于R点copy，就是copy这个函数，我们叫它深度拷贝。那这样的R的拷贝就不会影响到R。



![](img/d3cd592e4396ecb8b3270a5da950de0d_17.png)

R的copy就不会影响到R。比如说R copy R copy。我们把它所有的数都换成100。

![](img/d3cd592e4396ecb8b3270a5da950de0d_19.png)

看一下R卡平对吧？直都变成了100。那我们来看一下R有没有变，R是没有变的。所以如果你要。

![](img/d3cd592e4396ecb8b3270a5da950de0d_21.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_22.png)

建立一个新的矩阵，千万不要继续使用之前的矩阵的切片，一定要把它作一个深度拷贝。

![](img/d3cd592e4396ecb8b3270a5da950de0d_24.png)

然后我们再来讲一下迭代的数迭代数组。

![](img/d3cd592e4396ecb8b3270a5da950de0d_26.png)

首先我们创建一个。4乘3的数组，那随机数呢从0到9。run就是随机数嘛run in就是0到9的一个。整述。



![](img/d3cd592e4396ecb8b3270a5da950de0d_28.png)

四行三列。🎼看一下test。这是我们创建的矩阵。然后。我们想按行迭代它怎么怎么迭代for row in。



![](img/d3cd592e4396ecb8b3270a5da950de0d_30.png)

Test。R。这样它就是每每一行一行的打印。那这个时候之前我讲过for循环的时候，这个也是任何啊。只不过我们在这里写不是就是给它命名为roach，比较方便。我们。



![](img/d3cd592e4396ecb8b3270a5da950de0d_32.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_33.png)

呃，比较方便我们读它是行行的意思嘛，对吧？

![](img/d3cd592e4396ecb8b3270a5da950de0d_35.png)

那如果单独拿出来，你们还知道什么意思？为什么是966啊？因为我最后一次打印是966，它最后一行是966，它是一行一行一行一行迭代下来的。最后一行是966，它保存在这里边了，所以它是966。



![](img/d3cd592e4396ecb8b3270a5da950de0d_37.png)

那我如果想。按照索引来迭代呢，这应该怎么办？🎼For are in rangech。

![](img/d3cd592e4396ecb8b3270a5da950de0d_39.png)

那就是。之前其实提到过。

![](img/d3cd592e4396ecb8b3270a5da950de0d_41.png)

lan test是什么？lan test是4。它是它表示带有4个元素嘛，也四行4个元素。对吧它就是那这么range是代表什么？0123对吧？所以I会等于0123。那我如果打印一下print I。



![](img/d3cd592e4396ecb8b3270a5da950de0d_43.png)

Print a test I。这是不是就是按它索引来打印了？我们看一下艾应该是最后一个是3。

![](img/d3cd592e4396ecb8b3270a5da950de0d_45.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_46.png)

或者我再print一下I。就是零打第零行打印一下，第一行打印一下，第二行打印一下。

![](img/d3cd592e4396ecb8b3270a5da950de0d_48.png)

这就是我们的按。

![](img/d3cd592e4396ecb8b3270a5da950de0d_50.png)

就是或者是如果你把它单独拿出来。

![](img/d3cd592e4396ecb8b3270a5da950de0d_52.png)

是一对吧？这01755，这就是暗行迭代它。

![](img/d3cd592e4396ecb8b3270a5da950de0d_54.png)

或者我们也可以这么写。🎼For I。🎼Rll in enumerate。Test。如果我们有inumererate的话，就表示就是我们可以放两个进去，前面一个是它的缩引，后面一个是它的值。Print。

R。中间往加一个空格。对吧这是第零行是979，这样以此来打印。呃，通常情况下，我们会习惯用innurate而而不要用这种方式。这种方式呢。嗯，比较复杂，然后这种是pyython里面的。



![](img/d3cd592e4396ecb8b3270a5da950de0d_56.png)

叫什么呃，best practice最好的方案。其他的我们还能干嘛呢？还有就是这嗯。🎼比如说啊。Jy。Zip。test two我再建再建立一个数据。



![](img/d3cd592e4396ecb8b3270a5da950de0d_58.png)

🎼Test to name test。两倍。Copy。嗯。先要点咖py在。

![](img/d3cd592e4396ecb8b3270a5da950de0d_60.png)

这这就是test two是test one的一个。

![](img/d3cd592e4396ecb8b3270a5da950de0d_62.png)

两呃2次方2次方。

![](img/d3cd592e4396ecb8b3270a5da950de0d_64.png)

然后我们可以同时循环test。Her test to。

![](img/d3cd592e4396ecb8b3270a5da950de0d_66.png)

里面的数。Print。J。

![](img/d3cd592e4396ecb8b3270a5da950de0d_68.png)

对吧这打一下啊I再打一下J，所以我们同时循环这两个。

![](img/d3cd592e4396ecb8b3270a5da950de0d_70.png)

然后其他的我想提一点，就是比如说还可以用嗯。我再给一个。

![](img/d3cd592e4396ecb8b3270a5da950de0d_72.png)

361。🎼a range就是0到36，然后除了之前的resize，我们还可以用re shape。

![](img/d3cd592e4396ecb8b3270a5da950de0d_74.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_75.png)

把它变形成为6乘6的一个矩阵。然后我们还可以用。

![](img/d3cd592e4396ecb8b3270a5da950de0d_77.png)

7个补长。来把它每隔7个打印一下。074，这就相当于我们打出了一个diagonal。打印出了它的对角线。



![](img/d3cd592e4396ecb8b3270a5da950de0d_79.png)

那么我觉得这节就差不多了。

![](img/d3cd592e4396ecb8b3270a5da950de0d_81.png)

后面的话我会咱第一个module已经结束了。后面的话我会给大家下发一个。

![](img/d3cd592e4396ecb8b3270a5da950de0d_83.png)

![](img/d3cd592e4396ecb8b3270a5da950de0d_84.png)

assignment大家就是一个作业，大家可以跟着作业自己练习一遍。如果有问题的话，嗯，大家可以在留言区互相帮助一下。然后呢，我还会在后面发布答案。



![](img/d3cd592e4396ecb8b3270a5da950de0d_86.png)

大家可以呃大家可以来我主页找一下。