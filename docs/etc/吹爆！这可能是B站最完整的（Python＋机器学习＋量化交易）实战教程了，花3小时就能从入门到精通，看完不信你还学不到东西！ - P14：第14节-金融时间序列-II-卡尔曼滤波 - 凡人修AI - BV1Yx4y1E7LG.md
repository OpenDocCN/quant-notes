# 吹爆！这可能是B站最完整的（Python＋机器学习＋量化交易）实战教程了，花3小时就能从入门到精通，看完不信你还学不到东西！ - P14：第14节-金融时间序列-II-卡尔曼滤波 - 凡人修AI - BV1Yx4y1E7LG

那接下来让我们来介绍一下common filter的理论，那么如果对理论推导不是感兴趣的同学的话呢，可以跳过呃，在我们介绍卡尔曼滤波理论之前呢，我们要先要弄清楚几种啊。

问题就几种estimation的情况，那么第一种呢就是estimation of啊，这个status x t，那depends on呢是从一时克的Y，一直到T减10克的。

那这个呢称为prediction problem，就是预测问题，那么非常好理解，因为这个时候你只有从第一时刻到T减，一时刻的过程，那么你要预测第T时刻的那向前了一步。

所以称为的是预测prediction，那么第二个呢，唯一的区别就是这个时候多加一个YT，那么这个时候相当于你有T时刻的observation，但是你要得到的是70克啊。

内置inner inner process的这个dynamic xt，在T时刻的estimation，那么这个称为filtering，也就是叫滤波滤波问题，那么第三种问题呢。

我们在这里并不会用到第三种问题，就是我有一整个full set time series，就从一时刻到第N时刻，那么N时刻大于T，但这个时候我还是要estimate。

比N之前的T10克的XT的inner process，他这个时候的估计值是多少，那么这个称为smooth thing，就是有了未来的时刻，但是我返回去到current status。

那么我为了得到的是有further information的时候呢，我把现在的current status给smooth掉，那么我们在这个讨论卡尔曼滤波的时候。

用到第一条prediction和第二条filtering，那么这两条这两个problem呢，在combined with这个gation process，高选的意思，就是我的这个VT跟在T呢都是独立的。

零一标准正胎。

![](img/5bc79037fb0f16244aaebb31bf77f43b_1.png)

![](img/5bc79037fb0f16244aaebb31bf77f43b_2.png)

那我们来看卡尔曼滤波的具体的一个实现过程，那么第一点呢嗯我们要介绍的是呃，我们有了卡尔曼滤波的两条state model的方程，第一条是dynamic update，第二条是observation。

那通过这两条我们可以得到如下的这两个概率，概率过程，也就是我们知道XT呢是等于probability，x t depend中XT减一，为什么呢，因为取了probability之后。

因为后面的这一项其实它是一个，它是一个零一正态的劳动项，所以这个时候他是depend中，只depend中XT减一，因为VT并不会提供further information，那么对于YT来说呢，也是啊。

诸如此类，ZT是可以省略的，也就是YT的information是完全由XT给予我们的hint，那把上面这个model转换成如下的图形解释。

也就是我们内置的inner process或者叫做hidden process，那么自己本身在一步一步的啊更新，那这个时候呢每到第I时刻，那么就会往外set out的一个observation。

所以呢我们作为一个观测值，我们人站在这个外面，我们观测的是我们观测到的是这个绿色的YI，那么但是真正的能把这个model driven起来的呢。

是我们里面的这个hidden dynamic update，那么这个这个common filter的这一整个hidden state and，observation的过程呢。

其实是一个hidden Mark of machine，或者叫hidden Mark of chain的一个啊。



![](img/5bc79037fb0f16244aaebb31bf77f43b_4.png)

应用，那这个时候让我们先走一遍，我们的这个filter and prediction的过程，首先我们的filter其实是反过来的，因为我们拥有了YT的observation，那我们进入这个卡尔曼滤波。

那这个时候急于啊，通过卡尔曼滤波的推导公式，给予我们的是estimated of t时刻的x state，那大概取一个什么样的值，那么这个时候我们要用到的公式就是probability。

XT那是depend中什么呢，depend中T时刻包括T时刻之前的所有的YT，那我们在做这个estimation之前，我们需要的是两步，第一步是先有这个depends on。

嗯T减一时刻之前的YT的XT的probability，因为这个地方比后面啊来的有一个one lag，所以我们把它称为prediction，at time t减一，那我们拥有这个式子之后呢。

嗯我们得到下面的表达式，就我们后面推过推导，大家可以看到就是嗯这个表达式，这个表达式的推导呢需要利用到一个因子，就是上面这个prediction，那么我们主要的目的呢其实是得到probability。

xt depends on y1到T时刻的这个称为filter，也就是我们卡尔曼滤波，Come on filter，filter的意义所在，那嗯就是首先有一部prediction。

其次通过这个prediction t减一时刻的prediction，得到T时刻的filtration，就是我们这一整个卡尔曼滤波的一个。



![](img/5bc79037fb0f16244aaebb31bf77f43b_6.png)

two step的一个过程，那首先让我们来看prediction step的推导，那么proposition step，首先呢我们给一个join probability的表达式。

也就是啊depends on y t减1~1时刻的，这个information呢，啊WALLACE就他们的XT和XT减一两个联合，概率分布是什么呢，那么可以由这个probability rules。

就是啊BS公式得到这样的一个拆分表达式，那么由于我的这个XT是一个Mark of property，也就是Y从一到T减一时刻的information，其实完全由XT减一表示了。



![](img/5bc79037fb0f16244aaebb31bf77f43b_8.png)

为什么呢，我们可以通过看上面的这个表达式，因为YT呢都是由x t given的。

![](img/5bc79037fb0f16244aaebb31bf77f43b_10.png)

所以这个时候上面这个表达式可以简化成如下，子含XT减一的一个probability，那么可以写成如下的两种probability的拆分，那么这个是联合概率分布。

但是我们focus on的是xt depend，从Y从一到T减一时刻的，那么这个时候就要把XT减一给积分掉，所以利用下面这个开办，COMMOLOGO的这个equation呢。

我们通过积分就得到了这个prediction的表达式，那我们就完成了我们的第一步，就是片中从Y1到T减一时刻，对XT做prediction，这样的一个概率表达式，是一个这联合概率的积分。

那么接下来让我们来看update。

![](img/5bc79037fb0f16244aaebb31bf77f43b_12.png)

那update stamp的话会稍微复杂一些，那么用到的是这个贝叶斯法则，那首先呢我们有啊上一步的prior distribution。

那prior distribution呢从我们嗯step one的prediction可以得到，那么还有我们的state space model，就是原来就拥有的两个概率，一个是XT的盘中XT减一的。

一个是YT的片中XT的这样的两个uh from，Stay space，The likelihood，那我们拥有这个之后呢，嗯我们得到了上面的information，我们来推导下面的这个update。

也就是filter的step，我们先写如下的一个表达式，就是XT呢要depend中，YT和Y从一到T减一时刻的information，那么用贝叶斯公式可以拆成如下这样的表达式。

那么又由我们上一步已经用过的这个马可复性，我们YT减一时刻的information呢是totally，由XT得到XT减一得到的，那么XT呢又是由XT减一得到，所以这个时候我们可以把上面的这个简化写成。

嗯XT那YT呃，depends on xt呢，是由上面我们这个state space model probability呢，可以直接得到，那p x t depend中YT减一。

就是我们上一步通过prediction得到的这个probability，那么这个就完成了我们这一整个upstate啊。



![](img/5bc79037fb0f16244aaebb31bf77f43b_14.png)

update的这个过程，那呃这个是一个我们这个position，一整个流程的表达方式，那我们可以看到我们上面这个position step呢，需要用到一个什么信息呢，是xt depends on。

嗯XT减一，这边Y从一到T减一是可以不用写了，这个式子呢是我们本来就有的，通过我们的那个啊222元的这个方程组，那么这个XT减1depend中Y从一到T减一，这个式子其实是T减一部的啊。

update或者叫做T减一部的filter，所以这个东西其实是我们上一步的，就是T减一步的step two得到的东西，所以呢这个是一个互相依赖关系，那么我们有了第七步的prediction带到呢。

呃第七部的update这个表达式就得到了第七步的update，然后在so far so force到DT加一部，那带到T加一部里面的PREDITION，就得到T加一部的process。

这样的一个dynamic的一个啊动力机。

![](img/5bc79037fb0f16244aaebb31bf77f43b_16.png)

那我们接下来先，我们接下来看一下我们的这个prediction跟呃，update的具体的公式是如何迭代的，那么首先呢这个是我们嗯标黄线的，这两个呢是我们通过我们的model得到的，也是我们一直在提的。

第一步是XT自己本身update的一个过程，那么YYT呢本身是这个依赖，就observation的依赖过程。

所以我们在prediction book跟update book有这两个probability呢，是永远依赖于我们的model，那么在prediction的这一块。

白色的这一块呢是我们上一步DT减一步的update，也就是这个东西，那么在update的这个位置呢，是我们本部，也就是第七部里面的第一块prediction得到的东西。

所以是这样的一个dynamic update的一个process。

![](img/5bc79037fb0f16244aaebb31bf77f43b_18.png)

我们就称为是一个卡尔曼滤波。

![](img/5bc79037fb0f16244aaebb31bf77f43b_20.png)

那这里呢是我们先给出一个卡尔曼滤波的update，的一个呃公式，那么如果嗯我们后面会介绍，这个公式是如何推导得到的，那么对推导不感兴趣的同学呢，就可以直接就直接看这一页，那这一页说的是什么呢。

就是先given我们的这个model这个卡尔曼滤波，dynamic of observation的一个model，那接下来呢我们要做predict嗯，做predict的话。

我们知道ST如果depend中T减一的information，那么它就是如下的一个表达式，把VT取其实取1heat，也就是take expectation，那么后面这步VT因为它的均值是零。

所以就消掉了，那么下面这一步呢其实是对呃，左右两边同时take一个COVERANCE，就是斜方差，那么PTDEBONT减一呢，就是第七部的predict的协方差正，那么A乘以斜方差。

正上一步的斜方差正乘以A的转置，那么VT的话take斜方差，也就是它的Q，也就是啊N的这边上的这个位置是一个对角阵，那么Y呢是一个observed，就第七步我得到一个这样的观测。

那么update的时候我们要update几个量，就第一个量呢是叫做come on game，叫卡尔曼啊game，那caron game呢是呃有助于我们下一步对于呃。

coverance matrix跟本身state的一个update一个因子，我们可以把它看成是一个coefficient，那我们得到第七部的卡尔曼game之后呢。

D第七步的coverance matrix呢就是一减去这个come on game，乘以边上的这个C系数乘以DT减一部的这个嗯，coverance metric的这是一个prediction。

因为是t depend on t减一，那这个时候你得到第T步的converance matrix，就可以update第七步的嗯，这个是future的过程。

因为是t depend中T那它是由滴滴步的prediction，就是对X的prediction，因为它是DEBAN中DT减一的，然后再加上本部我得到的common game乘以呢，第七步。

我的observation，我的观测值减去一个可呃，减去一个coefficient乘以，我们上面提到的DT部的prediction，那么得到了我DT部对X1head完全的一个更新。

或者是称为filter，那这个这个很重要的卡尔曼滤波的，这一整个update的表达式是如何得到的呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_22.png)

我们下面来一步一步的说明，那么首先呢先给大家看一个直观的例子，也就是KA尔曼滤波，对于render Mark随机游走的这个滤波的prediction。



![](img/5bc79037fb0f16244aaebb31bf77f43b_24.png)

那大家可以看到就是observation，YT本身呢是一个啊一个很离散的，很扰动的一个点，那么我通过signal processing呢就得到我的这个绿线，就叫做state estimation。

那state estimation就是我们所说的XT，也就是内涵的驱动因子，那么大家可以看到这个红色的点呢，就是几乎是围绕着这个驱动因子进行，向下震荡的，那么蓝色的这根线呢。

也就是啊我所谓的signal也就是嗯XT，但是底片中T减一的一个过程，可以看到这个蓝线和绿线呢非常的接近，那么。



![](img/5bc79037fb0f16244aaebb31bf77f43b_26.png)

那么接下来呢我们来看一下啊，这个是刚才我们上述的，对于random work的common filter呢，它的式子的代入，那么我们这边先不看这个上面的推导，就大家回去可以自己一页一页slice。



![](img/5bc79037fb0f16244aaebb31bf77f43b_28.png)

看我们这边主要讲的是一整个generic的。

![](img/5bc79037fb0f16244aaebb31bf77f43b_30.png)

就是对于卡尔曼滤波是如何推导的，首先呢我们拥有一个嗯，这个是我们需要用到的一些normal process，的一些一些结论吧，首先是我们有它们各自的分布，那如何得到联合分布，或者有各自的分布。

如何得到一个conditional的一个分布条件分布。

![](img/5bc79037fb0f16244aaebb31bf77f43b_32.png)

那么那么我们这个就是通过这几个Z码呢，我们后面会得到联合分布和各自的概率分布，或者是由概率，或者是由联合概率分布，得到它们各自的拆分分布，或者是相互之间的概率分布。

那么这个在我们看曼滤波最后结论的推导中呢，会应用到嗯，就先把它present在这里。

![](img/5bc79037fb0f16244aaebb31bf77f43b_34.png)

那么大家来看一下这个update过程，首先我们先看啊prediction啊，prediction呢，如果我们上面那个嗯嗯cap man equation，提到它由这两部组成，那么这两步得到之后呢。

我们要做一个积分，首先有这个join distribution，我们把xt depend on xt减一，就是自己XT本身的update的表达式带进去。

那么它是由我们的第一条dynamic update，这个方程得到的，那么它是一个高斯分布，那么这个A乘以T减一是均值，那么方差呢也就是V的呃，V的方差也就是Q，那么带到第一个位置。

第二个位置呢是我们T减一部的filter，或者叫T减一部的update，就是step two，那这个呢就是我们只能用T减一部的filter的值，和T减一部。

由卡尔曼滤波得到的coverance matrix来替代，那么这两个值是由上一步更新的。

![](img/5bc79037fb0f16244aaebb31bf77f43b_36.png)

最后一个final state来得到的。

![](img/5bc79037fb0f16244aaebb31bf77f43b_38.png)

那么我们通过上面我们展现的两个嗯，那个LEMA，我们可以把这两个高斯乘积进行进行积分嗯。

![](img/5bc79037fb0f16244aaebb31bf77f43b_40.png)

那积分的结果呢就是写在这里，这个是我们第一步，也就是prediction，得到的两个两个高斯分布进行结合，并对XT做积分，那么能得到我们XT本身depend中，YT减一这样的一个。

marginal distribution的高斯分布的表达式，那么其实本身也很make sense，他以自己上一步的future的结果呢作为me，那么乘以了前面的一个系数A。

那么它的COVERANCE呢是上一步的结构的COVERANCE，乘以本身的系数，那么会加上什么呢，加上我这一部本部s st内部更新的一个嗯COVERANCE，也就是我自己本身更新会存在一个noise。

所以呢顺理成章的这个noise的COVALANCE，就加到我这个后面，就作为一个waiting song。



![](img/5bc79037fb0f16244aaebb31bf77f43b_42.png)

那这个是我们prediction的最后的结果，那么接下来让我们来看嗯，如何从position到update的一个过程，那么首先呢我们要update，我们把update的表达式写出，也就是XT的底片中。

YT和上一步的这个一从T减一的这个Y，那么这个时候呢我知道他的mean跟CONVERANCE，应该诸如此类的展示啊，展示出来，那么我们需要用到的几个因子呢，我们后面会prepare。

第一个就是这个state model的这两个分布是会用到的，那么其次呢就是上一步，我们得到这个prediction的这个结论。



![](img/5bc79037fb0f16244aaebb31bf77f43b_44.png)

那么，那么我们的x t depends on这呃XTYT啊。

![](img/5bc79037fb0f16244aaebb31bf77f43b_46.png)

depend中YT减一的这个表达式呢，我们根据上一步我们提到的呃，prediction的结论跟YT的这一行本身，Observation depends on。



![](img/5bc79037fb0f16244aaebb31bf77f43b_48.png)

XT这样的一个regression的一个结果呢，我们可以把它的表达式写在这边，那这个时候大家就可以看到，就是我们真正想求的是xt depends on，YT减一和YT，那么这个时候YT跑到前面去了。

那么我们可以利用我们上面有的一个这样的，depency dependency的结论，就是我们有XT的分布，有y depend中X的分布，我们可以得到X和Y之间的联合分布。

所以这个时候我们有了这个分布和这，两个分布之后，我们可以得到，我们下面这个联合分布的一个表达式，那么有了这个联合分布的表达式呢，我们上面还有一个LEMA会得出，有了它们两个联合分布。



![](img/5bc79037fb0f16244aaebb31bf77f43b_50.png)

那有没有他们的条件分布的表达式呢，就是确实是有啊，所以有了这个表达式之后，我们可以推出xt depend中，YT跟YT减一的分布是什么，那我们可以利用上面所得到的这个样子的结论。

把x depends on y也就是x t depends on，把这一块当成是Y，所以就放到里面去了，所以就是一个如下的这个结果，那么这个结果通过这上面的四个系数带到下面。

就可以算出它的均值应该是多少，那么这个coverence matrix。

![](img/5bc79037fb0f16244aaebb31bf77f43b_52.png)

也就是协方差正应该是什么样的表达式，那么这边呢就是我们得到这个表达式之后，对均值跟得到这个协方差进行一个整理，整理之后呢，把这一项比较run的这一项就是很复杂的。

这一项我们称为come on again，那么我们得到看完电之后呢，就可以简化我们对均值的update跟协方差的update过程。



![](img/5bc79037fb0f16244aaebb31bf77f43b_54.png)

那么最后的一个aggregate就是结合在一起的，结果呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_56.png)

就是大家看到的一整个就是卡尔曼滤波，卡尔曼滤波的这三条update的过程，实现update第七步的come on game，然后嗯update呢第七部的coverse matrix。

最后由come on game呢，跟我上一部的这个啊prediction。

![](img/5bc79037fb0f16244aaebb31bf77f43b_58.png)

得到本部的filter的结果，那我们这边来看一，再回顾一下上一部的这个例子，也就是random work的这个dynamic system。

那random work system呢可以写成如下这个state model，那么WT呢跟absent t呢，是满足这样子的一个IID的呃正态分布，那我们可以由这个式子来写出。

XT跟y t depend on呃，自己本身上一步和这个依赖关系的一个，高斯分布，那么通过高斯分布呢。



![](img/5bc79037fb0f16244aaebb31bf77f43b_60.png)

我们可以带到上面的这个表达式中，我们可以得到这个random work k。

![](img/5bc79037fb0f16244aaebb31bf77f43b_62.png)

在卡尔曼滤波之后得到的这个filter过后的啊。

![](img/5bc79037fb0f16244aaebb31bf77f43b_64.png)

signal也就是大家所看到的蓝线，那嗯KA曼滤波还有几个地方的用处，第一个用处呢是我们之前一直强调的，在linear regression中，那么在linear regression中。

我们经常需要update的是我们的这个嗯，翻零跟翻译一，也就是这时候它不固定是二三，有可能是F0跟翻一关于时间那个函数，那我们也如下写成这样的一个state，model的表达式和update的状态。

也就是把X等于AXT减一的，这个A跟Y等于C，XT加上一个B乘以ZT的这个C写出来。

![](img/5bc79037fb0f16244aaebb31bf77f43b_66.png)

带到上面卡尔曼滤波的这个表达式。

![](img/5bc79037fb0f16244aaebb31bf77f43b_68.png)

那我们就能得到它的一整个更新的过程。

![](img/5bc79037fb0f16244aaebb31bf77f43b_70.png)

那么，那么C呢跟A都写好之后呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_72.png)

我们边上这个更新过程就自己得到了，得到之后带到就这里是一个MATLAB的一个编程，那我们可以看到发一跟F0，当我们假设发音跟发音本身是不大，随时间变动的，但是只是加一个呃一个高斯扰动的话。

那么你会发现当进行过200次迭代之后呢，他就收敛到了真实值。

![](img/5bc79037fb0f16244aaebb31bf77f43b_74.png)

那么嗯接下来再看一个嗯AR model，那么AR model呢是我们之前假设的这个参数呢，都是随时间变化的，而不随时间变化的，那么这边让我们来看一个parameter，是啊，时间依赖。

也就是他们dependent的一个R1的啊例子，那我们假设呢，它随时间分布也是满足一个随机游走，那么我们可以看到这一整个fit的演变过程，跟本身的这个YT的演变流程，那么因为我们假设他的这个参数呢。

是随机游走过程，所以说呢他是一个不收敛的，是一个不管在任何时间呢，都是一个可上可下的一个动态过程。

![](img/5bc79037fb0f16244aaebb31bf77f43b_76.png)

那么这个呢就是大家如下所示的，这个AR model的simulation的这一整个例子。

![](img/5bc79037fb0f16244aaebb31bf77f43b_78.png)

那么我们接下来看一下呃。

![](img/5bc79037fb0f16244aaebb31bf77f43b_80.png)

卡尔曼滤波的Python的代码举例，那么我们KA滤波呢会用到这个py karma，那我们得在就是得打开这个程序程序框terminal，那么打开terminal之后呢，我们输pipe py comma。

那我们先install这个package，那install好之后呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_82.png)

我们才才才能在这边进行import，那么我们在这边define了一个function。

![](img/5bc79037fb0f16244aaebb31bf77f43b_84.png)

就是画我们的这个我们叫做热度。

![](img/5bc79037fb0f16244aaebb31bf77f43b_86.png)

热度矩阵，或者叫一个热度plot，那么热度pro的一个idea呢就是越高位的点，那么它就颜色越红，那么越往下呢颜色就越淡越稀疏，那么这个利于我们做以后的进一步的数据分析。



![](img/5bc79037fb0f16244aaebb31bf77f43b_88.png)

那这边呢我们是做一个卡尔曼滤波的update。

![](img/5bc79037fb0f16244aaebb31bf77f43b_90.png)

跟KAR曼滤波，最后final final day就是大家看到的这个啊，time varying coefficient的一个变化图。



![](img/5bc79037fb0f16244aaebb31bf77f43b_92.png)

那这边呢也是DRA我们的change这样的两条啊。

![](img/5bc79037fb0f16244aaebb31bf77f43b_94.png)

我们会用到的很常用的卡尔曼滤波的function，那我们这边主要呢做的是啊两个ETF。

![](img/5bc79037fb0f16244aaebb31bf77f43b_96.png)

就两个股票的ETF，那么这两个之间我们在之前也讨论过，它们具有协整性，也就是他们俩的相关度比较高，并且他们回归之后的残差是具有均值回复的，那么所以这两个这一对player呢。

非常适合我们做pair trading，但是在做pair trading的时候，我们的那个head ratio贝塔，之前是假设不随时间变化的，那么这个其实不现实的。



![](img/5bc79037fb0f16244aaebb31bf77f43b_98.png)

那这个时候如果我们用了state model的话，那么呃我们的这个贝塔，也就是一个dynamic hin，那么它会随时间变动。



![](img/5bc79037fb0f16244aaebb31bf77f43b_100.png)

那这个时候我们从宽岛上把两组数据破下来，破下来之后呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_102.png)

用我们用卡尔曼滤波，就上面写的这样的吊卡曼滤波的一个一个函数。

![](img/5bc79037fb0f16244aaebb31bf77f43b_104.png)

那么嗯掉了之后呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_106.png)

我们来看一下最后展现的结果，那么这个就是我上面所说的这个热度图，那么越往上呢就是颜色越重，说明它的值是越大的。



![](img/5bc79037fb0f16244aaebb31bf77f43b_108.png)

那么这边呢是啊卡尔曼滤波之后，我们得到的coefficient，的一个跟随时间波动的图，那么intercept也就是我的阿尔法截距项，那么slope呢就是我的贝塔，也就是斜率下。

那么随时间波动的一个轨迹图，那么我们在做真实的pair trading的时候呢，我们的这个阿尔法也是我们的access return，跟我们的这个HRATIO呢，就必须跟随着新的数据进行适当的调整。



![](img/5bc79037fb0f16244aaebb31bf77f43b_110.png)

那么卡尔曼滤波呢。

![](img/5bc79037fb0f16244aaebb31bf77f43b_112.png)