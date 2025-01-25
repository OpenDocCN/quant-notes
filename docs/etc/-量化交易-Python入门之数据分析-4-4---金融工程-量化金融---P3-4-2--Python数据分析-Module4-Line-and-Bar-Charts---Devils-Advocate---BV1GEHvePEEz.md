# 【量化交易】Python入门之数据分析【4／4】｜ 金融工程 量化金融 - P3：4-2. Python数据分析：Module4-Line and Bar Charts - Devils-Advocate - BV1GEHvePEEz

![](img/1eae6142e0d30998e5fb650c8396bd01_0.png)

上堂课我们介绍了line cloud应该怎么画？那么这堂课我在首先在line cloud上加一些东西。比如说如何把这个黄色的competition和baseline中间做一个fill。



![](img/1eae6142e0d30998e5fb650c8396bd01_2.png)

就是把它们之间给颜色进行填充一下。那么这里我可以写。PLT。点GCA。然后它自带一个fill。between的一个函数，然后这边是rangech。N。理你。Date。0年。



![](img/1eae6142e0d30998e5fb650c8396bd01_4.png)

呢个 data。然后这也是我们上面给到的linear data。然后。我们要给到lin尼。Data和 exponentialial。data，因为我们要在这两个之间做填充嘛，所以这两个都要给到。

然后我们要给一个face color。给个re。阿法是它的透明度0。5。然后多余的空话我可以删掉。

![](img/1eae6142e0d30998e5fb650c8396bd01_6.png)

来看一下情况。那这就是我们在两条线中间做填充。那如果我阿尔法改高一点，会发现更加实心或者是改低一点。

![](img/1eae6142e0d30998e5fb650c8396bd01_8.png)

那它就是没那么就是比较透明，所以阿法是它的透明度。

![](img/1eae6142e0d30998e5fb650c8396bd01_10.png)

接下来呢我们讲一下如何。

![](img/1eae6142e0d30998e5fb650c8396bd01_12.png)

在如何把把横坐标变成一个时间。我们可以使用，比如说PLT点。fiigure。Observation。observation date等于MP点。A range。



![](img/1eae6142e0d30998e5fb650c8396bd01_14.png)

然后这边我可以给他，因为这是n派function，我可以给他2024。

![](img/1eae6142e0d30998e5fb650c8396bd01_16.png)

0101，然后一直让他走到。2024。09。01。09。当然我也得告诉他他的低态就是。这个前面给到的含前面给到的这两个日期，它是一个day time的格式。Date time。等于4。D代表日代表日。

OP T plot。Observation dates。리니얼 data。这就跟前面一样。然后再给到我们的observation date。然后再给一个exponential data。同样的也是一个。

哦。

![](img/1eae6142e0d30998e5fb650c8396bd01_18.png)

那么这样子我们可以看到我们的下面有我们的日期，但是。

![](img/1eae6142e0d30998e5fb650c8396bd01_20.png)

![](img/1eae6142e0d30998e5fb650c8396bd01_21.png)

但是它粘在一起了，对不对？这时候我们应该怎么办呢？

![](img/1eae6142e0d30998e5fb650c8396bd01_23.png)

这边我们可以用到一个rotation的一个方式。

![](img/1eae6142e0d30998e5fb650c8396bd01_25.png)

然后首先它其实并不能识别它这个日期啊，它其实识别的仍然是一个str的格式。

![](img/1eae6142e0d30998e5fb650c8396bd01_27.png)

所以首先呢我们。

![](img/1eae6142e0d30998e5fb650c8396bd01_29.png)

我把这个拷贝一下。然后把observation date转换一下。转换一下格式list map。然后这边给他PD to day time。然后再给到呃。

servation date就相当于使用map map这个函数把observation date使用PD to date time这个函数来进行转换，然后最后把它变成一个list。然后我们来看一下。

这边inport一下PD。

![](img/1eae6142e0d30998e5fb650c8396bd01_31.png)

![](img/1eae6142e0d30998e5fb650c8396bd01_32.png)

那其实它没有变化，因为它仍然是一个string的格式。那这时候我可以把它进行一个转制。

![](img/1eae6142e0d30998e5fb650c8396bd01_34.png)

X等于POT点GCA。X， A X， is。I。然后我们现在就要做旋转for I in X get。Ter labels。我们把这些。下面的横坐标。都拿到，然后s rotation。



![](img/1eae6142e0d30998e5fb650c8396bd01_36.png)

45。这样的话他就做了1个45的转制。

![](img/1eae6142e0d30998e5fb650c8396bd01_38.png)

![](img/1eae6142e0d30998e5fb650c8396bd01_39.png)

然后这边由于我们用了GCA。我们可以。我们可以通过GCA的这个函数给它设定label X等于POT点GCA。X set。X label。Fates。X set。喂你。Data。Ex set。Title。

Some data。我们来看一下。这样的话我就加上了它的X label横坐标和纵坐标的。嗯你定。它的坐标。



![](img/1eae6142e0d30998e5fb650c8396bd01_41.png)

你接着我们来讲一下bar charts。

![](img/1eae6142e0d30998e5fb650c8396bd01_43.png)

barsh是我们的。条状图。PT飞。然后我们X values exp range。No。

![](img/1eae6142e0d30998e5fb650c8396bd01_45.png)

linear尼。对的。AndPT bar X values。linear data。

![](img/1eae6142e0d30998e5fb650c8396bd01_47.png)

With。设定宽度等于0。4啊。那我们可以看到这是我们的bar chart，在以这边变的是POT。82。呃，我可以再加上一些别的。别的数据。比如说这里newX values。

就是我可以画不止一个X value6，我可以再加上别的条呃条形图，跟它放在一起。就比如说这是一个这是一条。然后我在边上再加上别的数据，那不是有呃每个坐标上面都会有几个。几个条，几个数据 orI inX。

V。我正在干的是给他。只做一个别的数据。

![](img/1eae6142e0d30998e5fb650c8396bd01_49.png)

耳T bar。USX box Exp能 show data。然后位。Colors。In red。

![](img/1eae6142e0d30998e5fb650c8396bd01_51.png)

这边不应该是colorss，应该是color。那这样子我们就有了两条数据在上面，那我仍然可以给它再加一些别的数据。比如说它可以加一个。



![](img/1eae6142e0d30998e5fb650c8396bd01_53.png)

加些airline。嗯，这样时候你可能不太懂，我先inport一下。

![](img/1eae6142e0d30998e5fb650c8396bd01_55.png)

From random import。Rent int。run这这是我们的随机整数。然后0年。As。Rand it。从0到15。For x in range length。美你。对的。然后呢。

我们再把它。变画上去。B儿。

![](img/1eae6142e0d30998e5fb650c8396bd01_57.png)

Ling areas。这样的话，这上面就有一条eror线，这是这就取决于你想画成什么样的嗯图形。

![](img/1eae6142e0d30998e5fb650c8396bd01_59.png)

然后这大概是我们的条形图。那如果我想画一个别的样式，那其实也是有的。

![](img/1eae6142e0d30998e5fb650c8396bd01_61.png)

因为这边它是分放在两边嘛，那我如果想把它堆叠起来，就比如说它上下堆叠应该怎么做呢？PLT点fire。

![](img/1eae6142e0d30998e5fb650c8396bd01_63.png)

X value跟上面一样。

![](img/1eae6142e0d30998e5fb650c8396bd01_65.png)

![](img/1eae6142e0d30998e5fb650c8396bd01_66.png)

然后我们首先把 linearar data给画出来。

![](img/1eae6142e0d30998e5fb650c8396bd01_68.png)

这也跟上面一样。加一个col虑。等于。Green。这边我们有exponential data。然后但是我们要加一个地方，就是but。等于。



![](img/1eae6142e0d30998e5fb650c8396bd01_70.png)

Lar data。

![](img/1eae6142e0d30998e5fb650c8396bd01_72.png)

这样就呃，这边我们用read吧。这样我们就画画出来一个堆叠形式的图。

![](img/1eae6142e0d30998e5fb650c8396bd01_74.png)

嗯，那除了这样竖着的，我们还可以把它画成一个很像的。那这里有时候不显示的话，就POT到 show。

![](img/1eae6142e0d30998e5fb650c8396bd01_76.png)

这样。如果把它画成横向的话，我们就加个H，这是horizonal的意思。有点问题。因为这边是变成了 horizontalonal，所以它就不是宽度了，那它就变成了一个长度，hight高度。



![](img/1eae6142e0d30998e5fb650c8396bd01_78.png)

所以这就是我们的一个。竖向的啊，当然这边有bo，这边应该是left。

![](img/1eae6142e0d30998e5fb650c8396bd01_80.png)

我们从左边对吧？那这是我们的一个b chart。

![](img/1eae6142e0d30998e5fb650c8396bd01_82.png)