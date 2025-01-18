# Pandas基础（三） - P1 - Crypto小白书 - BV1AT421U7va

sorry大家好，这里是虾米小白书，今天我们将继续为大家介绍，pandas中一些数据处理相关的常用操作，首先是数据筛选的操作，这行代码的目的是筛选出data frame中close。



![](img/13419275b26b0adb4a71a494a0ba9a7a_1.png)

价格小于4万2的部分。

![](img/13419275b26b0adb4a71a494a0ba9a7a_3.png)

可以看到筛选出来的部分close价格都小于4万2。

![](img/13419275b26b0adb4a71a494a0ba9a7a_5.png)

我们也可以根据多个条件组合来进行筛选。

![](img/13419275b26b0adb4a71a494a0ba9a7a_7.png)

比如，利用这行代码，我们筛选符合条件，close价格小于4万2，并且HAMSTAMP大于，2024年1月29日凌晨一点，这个时间点需要同时符合这两个条件。



![](img/13419275b26b0adb4a71a494a0ba9a7a_9.png)

才能被我们筛选出来，好的可以看到我们成功筛选出了三条数据，这三条数据呢同时符合两个条件。

![](img/13419275b26b0adb4a71a494a0ba9a7a_11.png)

接下来我们来看一下append和merge，也就是合并的操作，这在我们后期处理数据将会被经常用到，首先是append。



![](img/13419275b26b0adb4a71a494a0ba9a7a_13.png)

使用这行代码呢，我们选取了data frame中的前十行，并且选取其中的tom stamp，clothes和volume这三列，并组成一个新的data frame，叫做data frame。

One play，出来看一下。

![](img/13419275b26b0adb4a71a494a0ba9a7a_15.png)

好的，接下来我们通过同样的方式，选取data frame中的第五行到第14行，并且选取其中的这三列，组成一个新的data frame to。



![](img/13419275b26b0adb4a71a494a0ba9a7a_17.png)

然后我们做一个append操作。

![](img/13419275b26b0adb4a71a494a0ba9a7a_19.png)

那使用data frame one，appendframe two呢，我们进行了一个拼接操作，将data frame one和two在垂直方向进行合并，拼接结果将被输出。



![](img/13419275b26b0adb4a71a494a0ba9a7a_21.png)

我们来试试看，OK我们看到有一个报错，他说data frame object has NO attribute，pan已经没有这个属性了哦，我懂了，就是说现在新版的pandas中呢。

其实他是做了一个变更，可以用两种方法将两个data frame上下合并，一种呢是继续沿用P但是在IPAD前面加上下划线。



![](img/13419275b26b0adb4a71a494a0ba9a7a_23.png)

对这样就成功上下拼接，或者我们可以使用pandas can cat，来拼接两个data frame。

![](img/13419275b26b0adb4a71a494a0ba9a7a_25.png)

来看一下。

![](img/13419275b26b0adb4a71a494a0ba9a7a_27.png)

是的。

![](img/13419275b26b0adb4a71a494a0ba9a7a_29.png)

这两个方法都可以好的，刚才是两个data frame上下合并，如果需要两个data frame左右合并的话，我们需要使用merge操作。



![](img/13419275b26b0adb4a71a494a0ba9a7a_31.png)

我们来举个merge的例子，计算代码比较长，它本质就是将两个data frame，Data frame，One，Data frame to，按照列的方式进行左右合并，并创建一个新的data frame。

小data frame merged。

![](img/13419275b26b0adb4a71a494a0ba9a7a_33.png)

可以看到在左边的是data frame1，在右边的是data frame2，合并的烈士，Time stamp suffix，这个函数呢则规定在有同名列的情况下，左边的列添加后缀，右边的列添加后缀。

用于区分，避免混淆。

![](img/13419275b26b0adb4a71a494a0ba9a7a_35.png)

我们再介绍一些其他常用的重要函数，首先是reset index这个函数的作用呢，就是调用data frame中的方法来重置索引，in place等于true的话，表示在原地进行修改。

drop等于true的话就是表示丢弃原本的索引列，rename函数，我们使用rename这个函数呢，用来重命名data frame中的列名，传入一个字典，作为参数，字典的J是原始列名，值是新的列名。

In place in true，表明在原地进行修改。

![](img/13419275b26b0adb4a71a494a0ba9a7a_37.png)

我们来运行一下。

![](img/13419275b26b0adb4a71a494a0ba9a7a_39.png)

啊这报错，Invalid syntax，我们检查一下这行代码有什么错误，后面忘加了一个逗号。

![](img/13419275b26b0adb4a71a494a0ba9a7a_41.png)

![](img/13419275b26b0adb4a71a494a0ba9a7a_42.png)

可以看到，我们成功的把每行列的列名都改成了中文。

![](img/13419275b26b0adb4a71a494a0ba9a7a_44.png)

Empty，Empty，属性呢是用来判断data frame对象是否为空值，他返回了一个布尔值，表示data frame是否为空，如果是的话就为true，如果不是的话。



![](img/13419275b26b0adb4a71a494a0ba9a7a_46.png)

就是false，我来试试。

![](img/13419275b26b0adb4a71a494a0ba9a7a_48.png)

嗯反馈为空值，因为我们的data frame显然不是一个空值，那我们来创建一个空值试试看，pd点data frame里面没有任何内容，看看他是不是empty。



![](img/13419275b26b0adb4a71a494a0ba9a7a_50.png)

我们再来看T属性，T属性呢，实际上是将data frame的数据进行一个转置，那转置呢是一个线性代数中的概念，通俗的话讲啊，原本的行变成列，原本的列变成行。



![](img/13419275b26b0adb4a71a494a0ba9a7a_52.png)

进行了一个翻转，我们来看一看，先来看原文的data frame是什么样的。

![](img/13419275b26b0adb4a71a494a0ba9a7a_54.png)

进行一个转职操作以后，看看data frame是怎么样的。

![](img/13419275b26b0adb4a71a494a0ba9a7a_56.png)

![](img/13419275b26b0adb4a71a494a0ba9a7a_57.png)

可以清晰的看到原本的列变成了现在的行。

![](img/13419275b26b0adb4a71a494a0ba9a7a_59.png)