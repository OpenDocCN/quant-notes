# 【量化交易】Python入门之数据分析【4／4】｜ 金融工程 量化金融 - P5：4-4. Python数据分析：Module4-Seaborn - Devils-Advocate - BV1GEHvePEEz

这节课我们来讲一下sborn这个 package，它是用来美化你padas的图片。那么跟前面一样，我们要import一下各个包。但是这里面呢我们加了一个import SSNS。然后我给到两个。

panda series0到10，然后有1000个，6015之间有1000个，分别叫做V1和V2。我们首先plot一下。一个hiisttogramPLT点fi。然后PLThist。V一。

阿尔法透明度等于0。7。bins就是它的间隔NP点A range。-50到150之间间隔5，这就是它每横坐标的一个间隔label等于。位移。然后这边我们自然就是用V2。他的label也是VR。

再给他1个PLT点leggend。

![](img/39b2344298b072a9f767fedf534fab0e_1.png)

POT点 show。这是我们的一个histyle brand。

![](img/39b2344298b072a9f767fedf534fab0e_3.png)

使用SNS我们可以。plot一个joy plot。然后这边。包括号V一。They are。阿尔法我们等于0。5。



![](img/39b2344298b072a9f767fedf534fab0e_5.png)

相比于我们使用。

![](img/39b2344298b072a9f767fedf534fab0e_7.png)

嗯，这个POTmyplpy plot。

![](img/39b2344298b072a9f767fedf534fab0e_9.png)

我们的join plot使用SNS的方式，它更好的给了我们一个style。图像上它会更好看一点。

![](img/39b2344298b072a9f767fedf534fab0e_11.png)

那么我们还可以这么做。Great。S，N S。Joint plot。这边其实也是跟上面一样的。然后我们给他一个。Great X。Joint。Set aspect。一口。



![](img/39b2344298b072a9f767fedf534fab0e_13.png)

之所以这么做呢，是因为我们的X轴和Y轴，它们的。他们的单位不太一样，就比如说这边是0到150，但是下面的单位是0到1200。那使用这种方法呢，可以看到他们这两个横横纵坐标。

它们的单位是就是它的un是一样的。所以这样的话呃，我们可以得到一个更准确的一个图形。

![](img/39b2344298b072a9f767fedf534fab0e_15.png)

![](img/39b2344298b072a9f767fedf534fab0e_16.png)

![](img/39b2344298b072a9f767fedf534fab0e_17.png)

除此之外呢，我们还可以。US SN S画个 joint plot。V2使用 kindine等于X。

![](img/39b2344298b072a9f767fedf534fab0e_19.png)

![](img/39b2344298b072a9f767fedf534fab0e_20.png)

然后我们加上space等于0。这这。之上我们可以改一下它的style。She on white。Sead style。然后这边要用方括号圈起来。



![](img/39b2344298b072a9f767fedf534fab0e_22.png)

![](img/39b2344298b072a9f767fedf534fab0e_23.png)

看着改成KDE。

![](img/39b2344298b072a9f767fedf534fab0e_25.png)

刚才还子是似乎。呃，并没有用，所以这便我们改成KDE。然后这样呢是我们的一个jo port。

![](img/39b2344298b072a9f767fedf534fab0e_27.png)

除此之外呢，我们还可以有perpl。Iris。DF。Q等于。你。就是它的颜色。D二agonal kind。KDE。



![](img/39b2344298b072a9f767fedf534fab0e_29.png)

Ss等于2。

![](img/39b2344298b072a9f767fedf534fab0e_31.png)

这边出了点问题。我们要用小写的name，因为我们的de frame里面是小写的。

![](img/39b2344298b072a9f767fedf534fab0e_33.png)

所以这是我们的一个pair plot。跟前面我们画的类似，只不过这边它的颜色。和各种setup都更好一点。我们这边有做。每个图像的散点图都有做区分。比如说sto啊。

Bie Collo her Virginiaica。

![](img/39b2344298b072a9f767fedf534fab0e_35.png)

这是因为我们对它的name进行了一个呃分配。

![](img/39b2344298b072a9f767fedf534fab0e_37.png)

如果看我们的数据的话。

![](img/39b2344298b072a9f767fedf534fab0e_39.png)

就是我们的不同的tet对应不同的name。以此来把只有150个数据分成了三类，所以我们会有三组。

![](img/39b2344298b072a9f767fedf534fab0e_41.png)

![](img/39b2344298b072a9f767fedf534fab0e_42.png)

除了air plots呢，我们还可以做一些。比如说swarm plot，还有 volumeolin plot。



![](img/39b2344298b072a9f767fedf534fab0e_44.png)

这边我们设置一下它这个PLTfi的大小。我们按照12比6的方式来做图。Pty sub plot。121。我要解释一下这边的suplo121什么意思？121呢代表总共有一行两列。

然后最后一个一代表我第一个图在第一行第一列，所以这是一个一行两列。一行两列的一个图，然后我画第一个图。S，N S。Swarm plot。X等于 name。Y等于。Petal。



![](img/39b2344298b072a9f767fedf534fab0e_46.png)

我们先看一下它都有哪些。GBM网名pedal lens。然后data等于irISDF。然后我们之前画的是121嘛，那是第一张图，122是不是第二张图？这边他为什么给我打红线？哎，这边多一个。122。

类似的，我们这边改成一个vololume plot。一个小提琴图。tight layout是把它们放的更紧凑一些。PLT电视。



![](img/39b2344298b072a9f767fedf534fab0e_48.png)

![](img/39b2344298b072a9f767fedf534fab0e_49.png)

这样前面的是我们的sm plot，然后后面的是我们的violin plot。

![](img/39b2344298b072a9f767fedf534fab0e_51.png)

![](img/39b2344298b072a9f767fedf534fab0e_52.png)