# 【量化交易】Python入门之数据分析【1／4】｜ 金融工程 量化金融 - P13：8. Python数据分析：Module1-numpy - Devils-Advocate - BV1efHAe2EAR

大家好，这节课我们来讲一下n派。numb派在线性代数中呢用的非常多。那线性代数呢在AI啊机器学习深度学习中呃非常需要。所以涉及到AI方面的n派必须掌握。那当然你如果你只是呃停留在一些表面阶段。

可能还好不涉及举重举不涉及矩证运算的话，嗯，numb派用的不太多，但是一旦你到比较深的地方，numb派还是需要呃它是掌握的。嗯，那这里呢我们先inport一下numb派。SNP。MP是一个非常。

长就是大家约定俗成的一个东西。嗯，我把它呢派叫MP。然后我先给他一个list。my list等于。123。X等于NP I。My。List。所以这样的话。

我们就把一个一个列表list转换成一个n派的 ray，这跟列表有点像哈。

![](img/e9f684ad6d2de87e46e424b90cdeecca_1.png)

123，我们的list也是这样，非常像。那么。如果就是除了除了这种方法呢，我们还可以比如说Y等于直接把列表放进去。34。



![](img/e9f684ad6d2de87e46e424b90cdeecca_3.png)

356吧。所以除了我们先赋值，然后再传递进来，我们还可以直接把它放进来，直接造一个呃array。那可以做一个多层的array，多层嵌套的方式。比如说。



![](img/e9f684ad6d2de87e46e424b90cdeecca_5.png)

Jiang。356。469，然后呢这两个这是两个list嘛，然后我们要把它合到一起，外面再套一层。

![](img/e9f684ad6d2de87e46e424b90cdeecca_7.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_8.png)

所以这就是多层嵌套的ray。那么我们可以拿ship的方式啊查看它的维度。

![](img/e9f684ad6d2de87e46e424b90cdeecca_10.png)

这是两行三列对吧？两行三列，356469。然后呢，我们。我们可以用A range囊派的A range啊呃。NPA range。



![](img/e9f684ad6d2de87e46e424b90cdeecca_12.png)

0到30，这用来设定等步长的0到30之间数。比如说02468对吧？等步长不长就是20到30呃，间隔为2。



![](img/e9f684ad6d2de87e46e424b90cdeecca_14.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_15.png)

我们来看一下N。啊024680一直到30啊，我这个显示我这只显示1到10，你可以让它显示所有，所以就是28啊，前B后开，所以这个没有直接到30到30前面一个，所以就是0到。



![](img/e9f684ad6d2de87e46e424b90cdeecca_17.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_18.png)

30。有点长。

![](img/e9f684ad6d2de87e46e424b90cdeecca_20.png)

printnt弹一下。我们还可以把它reshipreship一下这样子嗯。这样子的能让它变个形，咱现在不是一个就是一维嘛，对吧？我可以把它resha。re shape一下。

比如说我呃它是可 reship成三行五列。

![](img/e9f684ad6d2de87e46e424b90cdeecca_22.png)

对吧012345678到这样，对吧？这是三行五列的一个形式。呃，再来介绍一个东西叫link space。



![](img/e9f684ad6d2de87e46e424b90cdeecca_24.png)

嗯，M等于MP到。

![](img/e9f684ad6d2de87e46e424b90cdeecca_26.png)

0。Space。这个是干嘛呢呃。

![](img/e9f684ad6d2de87e46e424b90cdeecca_28.png)

先用一下，你看吧。

![](img/e9f684ad6d2de87e46e424b90cdeecca_30.png)

就是它0到4我们要找0到4之间，然后呢，我要把它分有我我要找出9个数值，9个等。等间隔的数是吧？零那就是每个0。5都有一个，要找9个嘛，012345678就是9个数，0到4之间找出9个数。

它们之间必须等间隔，所以它就是临 space返回指定间隔内均匀分布的数字。那还有一下，我们还可以把还有就是就把它这个resize一下。刚才是ray shape，咱这个可以用res size。



![](img/e9f684ad6d2de87e46e424b90cdeecca_32.png)

进来看下嗯。那么这这就变成了三行三列的一个东西。还有什么呢？MP我还介绍一下MP到ones，这就是比如说我给一个32，这就是三行两列，但是三行两列的一个矩阵，但是都拿一填充。



![](img/e9f684ad6d2de87e46e424b90cdeecca_34.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_35.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_36.png)

那你想到有一是不是还有零啊，NPzes。

![](img/e9f684ad6d2de87e46e424b90cdeecca_38.png)

也是32三行两页。这在之后我们矩阵运算中呃，可能会用。然后矩证运算还有什么呢？NPI3。

![](img/e9f684ad6d2de87e46e424b90cdeecca_40.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_41.png)

对吧，这就是嗯。就是构造一个嗯这种对角对角数组，这边都是一嘛，对吧？嗯，如果是4呢。

![](img/e9f684ad6d2de87e46e424b90cdeecca_43.png)

四行四列对吧？这是I对角数组，然后。还有啥？比如说Y等于。

![](img/e9f684ad6d2de87e46e424b90cdeecca_45.png)

MP array。

![](img/e9f684ad6d2de87e46e424b90cdeecca_47.png)

456。然后呢。NP。Dagonal。

![](img/e9f684ad6d2de87e46e424b90cdeecca_49.png)

456这个是这也是这种形式的对角数组。

![](img/e9f684ad6d2de87e46e424b90cdeecca_51.png)

然后还有比如说像MP。tile这个我用的比较少。

![](img/e9f684ad6d2de87e46e424b90cdeecca_53.png)

123。然后是3，这样就给出了，比如说1231233个123NPt。

![](img/e9f684ad6d2de87e46e424b90cdeecca_55.png)

然后如果会它它基本上等于1个NPR乘以3NPR就是我自己建1个NPR就是123，对吗？然后我再乘以1个3，就当时我们学列表的时候也学了，对吧？123乘以3，然后再把它变成1个NPR。



![](img/e9f684ad6d2de87e46e424b90cdeecca_57.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_58.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_59.png)

最后呢我们还可以用MPrepeat。

![](img/e9f684ad6d2de87e46e424b90cdeecca_61.png)

Young。

![](img/e9f684ad6d2de87e46e424b90cdeecca_63.png)

啊，不一样。这边是112233，repeat每一个elements。每一个eleement它都repeat一下，repeat三遍，呃。

这是NP repeatpeat MPP ray和NP tile这三者之间的区别。

![](img/e9f684ad6d2de87e46e424b90cdeecca_65.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_66.png)

嗯，我再来讲一下tack。😊，哦，没讲完。

![](img/e9f684ad6d2de87e46e424b90cdeecca_68.png)

比如说NP one，咱之前不是讲了1个NP one嘛，对吧？这个这给的都是浮点数。那我如果想要一个整数怎么办？这边加上int。



![](img/e9f684ad6d2de87e46e424b90cdeecca_70.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_71.png)

这样就能把他们所有的都变成一个ininteger。

![](img/e9f684ad6d2de87e46e424b90cdeecca_73.png)

然后我再来讲一下tack。

![](img/e9f684ad6d2de87e46e424b90cdeecca_75.png)

嗯，我刚才是给了。

![](img/e9f684ad6d2de87e46e424b90cdeecca_77.png)

是是。我就拿这个吧，Y来看一下，我们的Y是。

![](img/e9f684ad6d2de87e46e424b90cdeecca_79.png)

诶。

![](img/e9f684ad6d2de87e46e424b90cdeecca_81.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_82.png)

这样子。

![](img/e9f684ad6d2de87e46e424b90cdeecca_84.png)

Y等于。NPwise。23。

![](img/e9f684ad6d2de87e46e424b90cdeecca_86.png)

喂hy。这样它是两行三列的一个integer。然后呢，我们要我们要堆叠堆叠两个，这样上下堆叠起来，那叫什么呢？v stack。Vertiical stacking。Y呃为了让你们能看得出来区别呢。

我呃第二个。第二个矩阵，我乘一个2。这个要用列表框出来。

![](img/e9f684ad6d2de87e46e424b90cdeecca_88.png)

所以这边两个这不是一个矩阵嘛？Y然后这个矩阵把一都成了2，然后它们上下对叠，就是vertical stack， verticalical是垂直嘛？然后那有上下t还有左右t了。

那就hor stackNPH stack。嗯。然后YY乘以个2。

![](img/e9f684ad6d2de87e46e424b90cdeecca_90.png)

你可以看到这边是11，这边是R2，所以这边是上面是vtHt这两个挺重要的。其实至于tles那个可以倒可以不记，还有repeat倒也可以不记one和zero，啊，你们可能会在深度学习里面用的比较多。

因为我们需要建个举证之前，我们需要做一个站位啊，当然这你们后面才遇到，现在你要不懂也没关系，那这堂课就暂时到这儿。



![](img/e9f684ad6d2de87e46e424b90cdeecca_92.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_93.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_94.png)

![](img/e9f684ad6d2de87e46e424b90cdeecca_95.png)