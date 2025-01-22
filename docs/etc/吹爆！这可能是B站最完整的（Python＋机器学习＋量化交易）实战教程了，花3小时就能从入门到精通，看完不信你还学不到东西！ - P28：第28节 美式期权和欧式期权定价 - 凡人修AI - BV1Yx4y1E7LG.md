# 吹爆！这可能是B站最完整的（Python＋机器学习＋量化交易）实战教程了，花3小时就能从入门到精通，看完不信你还学不到东西！ - P28：第28节 美式期权和欧式期权定价 - 凡人修AI - BV1Yx4y1E7LG

来继续看这个OU过程，首先呢这个ET呢是我们最后嗯推导出的这个，积分项的这个积分的结果，那么呢ET我们通过数学分析可以看，发现呢它的均值是零，然后方差呢是如下这样一个表达式的正态分布。

那么前面呢其实都是一个常数，所以XT呢也就是均值是前面这一个部分，那么方差呢是这一块的一个正态分布，所以呢OO过程呢其实本质上呢也就是一个嗯，normal distribution的一个分布的啊。



![](img/0b311f50277b9da4cc039119e5d2bdb0_1.png)

蒙特卡罗模拟，那我们来看一个稍微复杂一点的CR过程，三二过程呢本身呢就不像前面的这个OO过程，跟那个几何布朗运动有解析解了，那么呢它是一个满足均值回复的一个过程，那均值回复的速率呢为K。

那长期的均值呢就是X100，那后面的这个这就是它的这个漂移项，我们称为drift ten，那么后面的这一项呢称为随机项，那也就是一个这个维纳过程乘以它的这个方，标准差呢，其实就是本身的一个西格玛。

一个常数乘以我们这个序列值的，本身就是根号XT，那么这样的一个CRR过程呢，呃它的它的性质呢是一个均值回复，那么它是趋向于回复到一个X18，这个长期均值，那么回复的这个嗯波动呢。

是跟我这个现current里的这个股价有关，那么我这个价格越高呢，我的这个波动率呢就越大，也就是它在均值上面，震荡的这个幅度呢也就越高，那这个CNR过程呢，就可以用我们上面提到的这个呃。

欧拉离散化来进行离散，那这样的一个过程呢，它有个坏处，就是它有时候会hit到一个额负数的这个值，不是说欧拉的DISAPTION，它会利到这个XT的一个negative value。

那我为了想这个避免它呢。

![](img/0b311f50277b9da4cc039119e5d2bdb0_3.png)

这时候我可以取一个这个log欧拉过程，也就是说这个时候我把这个嗯，把这令这个YT等于log的XT，然后嗯那然后这个时候等式的右边呢，把它列为这个样子的一个表达式。

那么这样呢可以就是避免我能够hit到一些这个，log的price，所以它是这个c i r process的一个变体，那么嗯这样的一个logo欧拉过程跟上combine with。

上面的cr process经常是用于一些利率曲线的simulation，那在我们这里，我们主要用的还是上面提到的几何布朗运动。



![](img/0b311f50277b9da4cc039119e5d2bdb0_5.png)

来这个simulate骨架，那下面让我们来具体的看一下，这个欧式期权定价的这个蒙特卡罗模拟，首先呢我们依照之前所说，我们假设我们的这个安underlying的骨架，能满足几何布朗运动。

那么满足几何布朗运动呢，也就会得到我们下面的一个讲的解析式，也就是在这个最后末尾，大T时刻的这个股价，就等于零时刻的这个初始值乘以指数，那上面呢是这个R减去西格玛平方，除以二乘以T这个R呢是无风险利率。

西格玛平方呢也就是这个股价波动率的平方，然后呢再加上这个股价的波动率乘以根号T，再乘以Z，那在这边Z呢是一个零一的标准正态分布，那如果呢这嗯上面的这个是我们的欧式期权，那如果是亚式期权呢。

亚式期权是一个pass dependent的一个期权，也就是说，亚式期权最后的收益，并不是我们的S大T减去K，而是这个S1整条这个股价的这个均值，然后减去一个K，所以这个时候我们就不能直接用这个中值。

我们得每一步的这个小ti都simulate出来，但是表达式呢跟上面一样，因为都是满足几何布朗运动的。

![](img/0b311f50277b9da4cc039119e5d2bdb0_7.png)

那我们每一步都similarly出来，这个小ti之后呢，我们对它取一个average，然后依旧是减去这个strike k，然后取一个这个跟零，取一个maximize，那可以用这个括号呃。

以加号为下角标来表示，那么呢这边呢是我们常见的一些option的payoff，那么大家只要记住这个call option嗯。



![](img/0b311f50277b9da4cc039119e5d2bdb0_9.png)

put option跟这个asian option就可以了，那接下来呢我们要讨论，我们在做这个option pricing的时候，我们这个蒙特卡罗模拟的物error是具体是多少。

那我们知道我们的这个mean呢，mi hat是满足我们这个正态分布，那么呢均值就是mu本身，因为它是无偏估计的，那么方差我们上面推导过，是这个西格玛除以根号NN，是我们similar了多少次。

那么对于这个呃期权来说呢，N就是我们simulate了多少条stop pass，那这个时候呢，也就意味着我这个误差，确实就是一个以零为均值，西格玛除以根号N为这个方差的一个。

这样啊为标准差的这样的一个正态分布，那这个时候我们通过这个数数量的构造，那么我们令这样的一个数值量为Y。



![](img/0b311f50277b9da4cc039119e5d2bdb0_11.png)

那Y就满足一个零一的标准正态分布，那我们一般呢我们要run多少次，我们得给出一个confidence level，也就是置信区间，我们比如说说我们的这个error啊，小于某一个值的。

这个我们认为的概率呢，是等于99。7%。

![](img/0b311f50277b9da4cc039119e5d2bdb0_13.png)

那这个时候我们可以反解，我们可以通过正态分布，因为我们知道这个Y已经推出来。

![](img/0b311f50277b9da4cc039119e5d2bdb0_15.png)

还是一个零一标准正态，我们可以通过标准正态的这个框太好，得出Y等于三，那这个时候呢也就意味着，三乘以西格玛除以根号N等于0。01，那我们可以把这个N给反解出来。

也就是我们要simulate多少次蒙特卡罗模拟，来得到什么呢，得到我们的这个误差，误差小于1%的概率呢，是等于99。7%，相当于是我非常有信心，我的真正的这个误差呢是这个小于0。01的。

因为犯错的概率仅为0。3%。

![](img/0b311f50277b9da4cc039119e5d2bdb0_17.png)

我们在simulate中途呢需要collect什么东西呢。

![](img/0b311f50277b9da4cc039119e5d2bdb0_19.png)

第一个就是我们的样本均值，因为我们上面的这个M其实我们是不知道的，所以我们得用样本均值来代替，那同理这个西格玛我们也是不知道的。



![](img/0b311f50277b9da4cc039119e5d2bdb0_21.png)

我们得用这个样本的啊方差来替代，所以呢这个是样本，我们每一步都要迭代啊，来更新我们的样本均值，然后呢还要来更新我们的样本方差。



![](img/0b311f50277b9da4cc039119e5d2bdb0_23.png)

然后我们来看一下一个Python的一个例子，就是我们假设这是我们要嗯定价一个欧式看跌，也就是european put，那我们假设呢T也就是时间，时间呢是一年，那我们总共我们的时间的grade就是DT。

我们取这个嗯52个52个时间间隔，也就是每一周取一个，那R呢是这个无风险利率，我们列为0。1，然后S0呢我们认为是这个100，也就是股价的这个开始是100，那这个strike呢我们依旧收有100。

然后我们underline的这个股票的方差啊，标准差呢或者是volatility就设为0。25，然后我们总共呢是SIMATE400000次，也就是40万个stock price。

那我们通过这个Python的pricing出来之后，我们知道市场上的true value是5。46，是通过这个black shequation直接代入啊，算出，把这上面这因子代入可以直接算出。

那么我们通过这个simulate算出来的，蒙特卡罗的price呢是5。47，所以我们MONTICA的error呢就是0。015，那我们可以看一下上面的这个啊。

我们的pricing的这一整个pricing的这个机器。

![](img/0b311f50277b9da4cc039119e5d2bdb0_25.png)

是具体是怎么做的。

![](img/0b311f50277b9da4cc039119e5d2bdb0_27.png)

![](img/0b311f50277b9da4cc039119e5d2bdb0_28.png)

比如说在这边，我们首先呢定义我们上面要的这个因子。

![](img/0b311f50277b9da4cc039119e5d2bdb0_30.png)

然后我们对这个时间进行这个离散化，然后呢我们把这个POR给这个import进去。

![](img/0b311f50277b9da4cc039119e5d2bdb0_32.png)

那这个POR呢是我写好的一个这个包。

![](img/0b311f50277b9da4cc039119e5d2bdb0_34.png)

那里面具体的实现呢，其实就是我们上面的这个公式。

![](img/0b311f50277b9da4cc039119e5d2bdb0_36.png)

就是大家上面可以看到蒙特卡洛模拟的。

![](img/0b311f50277b9da4cc039119e5d2bdb0_38.png)

这个公式的这样的一个步骤，其实自己其实大家自己写的也很简单。

![](img/0b311f50277b9da4cc039119e5d2bdb0_40.png)

写完之后呢，我们定义我们这个put的payoff是这个maximum。

![](img/0b311f50277b9da4cc039119e5d2bdb0_42.png)

然后呢再乘以我们的这个discount factor，那然后最后呢算命，然后也算我们的这个send deviation，也就是这这一步呢。



![](img/0b311f50277b9da4cc039119e5d2bdb0_44.png)

是介绍我们的蒙特卡罗的这个误差，然后我们最后把我们simulate出来的。

![](img/0b311f50277b9da4cc039119e5d2bdb0_46.png)

这个stop pass的前100条给画在这，然后我们的stock value呢就是我们最后present这个。



![](img/0b311f50277b9da4cc039119e5d2bdb0_48.png)

我们最后被我们最后通过这个东西算出来的，这个值就是e inputs，那么放到我们的这个这个里面进行进行simulation。



![](img/0b311f50277b9da4cc039119e5d2bdb0_50.png)

那么可以上除我们的这个值嗯。

![](img/0b311f50277b9da4cc039119e5d2bdb0_52.png)

那接下来呢我们来看一下。

![](img/0b311f50277b9da4cc039119e5d2bdb0_54.png)

这个american option是怎么price的。

![](img/0b311f50277b9da4cc039119e5d2bdb0_56.png)

那接下来呢让我们来介绍一下，美式期权和美式期权的定价，那么美声侵权呢，在basic idea上呢跟欧胜清泉是一模一样的。



![](img/0b311f50277b9da4cc039119e5d2bdb0_58.png)

那我们来回顾一下欧式期权有的那几个参变量，那么首先呢是这个T，这个T呢是我们的这个time to maturity，也就是多长到了多长时间之后呢，我们可以决定是否交割。

那么呢M呢是我们的这个step的步数，那我们在这边不考虑，那R呢是无风险利率，S0呢是股价在临时贺的时候的价格，那么呢K是我们的strike，也就是我们到期了，我们要以什么样的价格进行执行。

那vow呢是我们的这个假的，Underlying asset volatility，那它跟这个欧式期权的唯一区别。



![](img/0b311f50277b9da4cc039119e5d2bdb0_60.png)

就是它可以提前执行，比如说我们的这个T是三个月的，那么我们从今天开始过了一个月之后嗯，我们买的是call option，那发现呢我们的这个骨架呢变得啊，非常非常的高了，比如说我们的strike是100。

那现在的股价上涨到了200，那这个时候呢，我们中间我们中间相当于有100块的差价，那这个时候如果我提前执行，那我就可以以100块的价格买到现在，甚至是200块钱的股票，那就可以make profit。

但是呢大家要记住一点的是，我们有两条理论来支持我们的这个american call，也就是看涨的美式期权，如果是这个安underlying股票是没有dividend的，就是没有分红的话。

那我们是never do early access，就是不要提前执行，那大家可能一开始会很confusing，会觉得很奇怪，就是如果我这个时候脱手，我明明可以赚这100块钱的差价。

为什么我不early access，那第一个的解释呢是这个time value of money，意思就是说如果这个时候我要提前执行，我要来买这个股票的话，那么我还不如等到三个月之后。

因为这个时候已经是200块钱了，其实三个月之后，按照我们对jomo tribal motion的理解，其实这个股价是波动上升的，也就是说我们再过两个月，我在strike的，我在hit out。

除去strike的话呢，其实我是依旧是可以赚100块甚至以上的，但是嗯期间执行有一个什么坏处呢，也就是我要提早向银行贷款，这个K因为我们是假设，我们是我们本身是没有任何本金的。

所以我如果我们要执行这个option，那我们必须有这个呃k dok dollar的现金，那我得提前向银行贷款，所以我就相当于多贷了两个月的款，那呃那我当到时候就得配银行，更多的这个interest r。

所以这是time value of money的这个理论，那第二个理论呢是这个更好理解一些，叫做protection of buin price是什么意思呢，也就是说对于这个看涨期权，如果我提前执行了。

那就说明我现在持有了这个股票，那就是我用100块钱买，买到了一个市值为200块钱的股票，OK但是呢你就失去了你的这个protection of，Your price drop。

也就是说我现在手上已经没有这个期权了，我已经执行了，我现在手上拥有的是这个股票，那这个时候如果呃price drop了，也就是说这个股票现在从200块钱，忽然跌到50块钱了。

那么啊是不是再后悔都来不及了，也就是说嗯也就是说我现在持有的这个股票，我就失去了这个嗯call给我带来的一个protection，因为如果你三个月之后才决定是否执行的话。

那三个月之后即使跌到50块钱以下，那我就选择我不执行这个option就好了，所以说可以降低损失，那即使是你觉得你觉得这个股票特别诱人，就是说现在它值200块钱了，我为什么不去hit out呢。

那即使你认为现在你这个call是deep in the money，也就是说你的strike比现在的current market，price要低很多，那你也不是持有股票。

你也应该把这个option给卖出去来game profit，而不是现在current里立马执行来拥有这个股票，因为这个时候当这个股价非常高的时候，我们通过这个black shequation定价。

我们可以知道我们的这个call option，现在本身非常的值钱，所以我倒不如我现在把option卖出去来，Game profit，然后呢，把我得到的这个钱就是卖这个呃，option得到的钱呢。

直接invest在银行里，那我就可以以risk free rate来赚钱，所以这个是american option，在call没有dB等的情况下呢，是永远不提前执行的啊，那么另外一个理论呢。

其实是在这个数学上的理论，也就是嗯call option price，它的价格always是在intrinsic value之上，那么你提前执行american option。

你获得的一定是interesting value，所以说这个american call一直比interesting value来得高，所以如果这个时候你提前卖嘛，把这个就是股票给嗯，持有了你呃。

现在选择early access的话，那么你得到的钱是intring value，永远比你set直直接sell这个american option。



![](img/0b311f50277b9da4cc039119e5d2bdb0_62.png)

赚的profit来的少，嗯但是对于这个嗯american put来说就不一定了，就有时候我可以选择在有的时间段提前执行，那这样子呢我可以获利，那么对于这个early exercise的option呢。

我们不可以用最简单的MONTECARO来进行price，那理由呢待会大家可以看到，那首先如果我们要early access了，那我们对于每一个step，我们得定义现在的这个cod呃。

american put的value，因为定义了value才能跟我的intracing value进行比较，才能决定我是否要选择early access，那在这个ti时刻的这个value是等于什么呢。

等于maximize，我现在的这个intrintrinsic value，也就是我现在如果执行access，我能获得的利润和我继续持有这个american put的话。

那我现在的这个current value是多少，也就是T加一时刻的value，但是要discount到TI时刻，所以成了一个E的负的R德尔塔T，那当时要take一个expectation。

所以在每一步的时候是否执行呢，就是比较第一项和第二项之间的关系，嗯我们要算这个是否提早执行，那我们就得算出我们这个执行边界，叫做exercise boundary。

那么嗯提早执行这个deep in the money put的话，那可能是最佳选择，但是对于deep in the morning call，永远是不要提早执行的。

所以呢我们可以假设我们这个最优执行边界，是这个B，那么B呢跟我的这个current stock price，跟这个T都是有关系的，所以我们可以假设这个B的函数的形式。

我们带到这个呃这个put value里面去。

![](img/0b311f50277b9da4cc039119e5d2bdb0_64.png)

你和他，那么我们可以看一下，首先为什么大家很纠结的一个问题是，为什么这个普通的蒙特卡罗模拟就不行了，因为我们从intuition上来解释，我们每一步呢都有可能要提前执行。

但是我们每一步是不知道current option，value到底是多少的，因为我们现在依旧是处于simulation阶段。



![](img/0b311f50277b9da4cc039119e5d2bdb0_66.png)

大家可以看到，其实对于每一步来说，第一个这个位置就是提早执行，这个收益非常的好算，但是第二步其实不仅仅是V的TI加一乘以，被discount，我们要take一个expectation。

但是对于我们一条stop pass来说的一个点，我们是没有这个expectation的意义，在的我们只能对一整条的，对所有的stop pass，我们才有一个说是一个期望的一个概念。

但是由于我们每一条path都要决定，每一个点是否early exercise，所以这个东西是永远算不出来的，所以如果我们强行要算的话，只能把这个E给去掉，也就是对于一条pass来说。

你上一个点discount到current i的点来算，这个呃，Current current to value。



![](img/0b311f50277b9da4cc039119e5d2bdb0_68.png)

但是这样的话就是会失去准确性，大家不信的话呢，可以看一下，如果采用最直接的这个嗯蒙特卡洛模拟，我们直接是用这个current price，discount下来来算的话。

我们最后算出来的这个用pass wise，也就是跟这个嗯stop pass stop pass跟踪的走的，我们算出的这个american pop price跟这个true的值呢，差了非常的多。

所以我们要采用最小二乘蒙特卡罗，来拟合这个最优的执行边界来进行计算。

![](img/0b311f50277b9da4cc039119e5d2bdb0_70.png)

那么一整个的过程呢是如下所示，假设呢我们现在已经已经算完了，我们是从后往前倒退的算的，因为我们要算是否执行嘛，所以我们从大厅神间往前倒退算，那么假设我们已经算到了DTM部的这个VTM，那我们就假设呢。

我们这一整项discount到TM减一时刻，我们的这个值是已经知道的，那么我们通过蒙特卡洛simulation，我们知道了这个stock price在这个TM减一的值。

首先呢我们要construct一个smooth function，来最优化我们的这个执行边界，首先我们假设我们的执行边界是一个跟stop price嗯，相关的一个二次的函数。

那这个时候我们把它带到这个最优化的这个，表达式里嗯，最优化是什么呢，是当我这个put是in the money，也就是stop price比strike来的小，这个时候我的这个USTM减一。

才能才才能才能进入我们这个optimization，然后呢减去我们的这个嗯，从上一个步骤discount下来的这个呃put value，我们对它进行最小二乘的拟合，就是让这个这个二次的这个二次S的。

二次的这个表达式，最接近于我们的这个discount value，那我们最优化这个之后，我们可以得到C0C1C二的值，所以我们就有这个decision boundary的表达式。

那有了这个帮助里的表达式之后呢，我们要决定我们是否选择在TM减一时刻，我们要early exercise，也就是说而立exercise的node呢，我们就定为我们这个呃intrc value。

也就是我们提早执行能获得的收益，大于我们现在的这个put option的的值，也就是U的STM减一，那如果是大于呢，我们就执行，如果呢我们不是的话呢，这个就是取零不执行。

所以现在的这个价格就等于如果是执行，那就是这一块如果不执行的就是后面这一块，所以我们可以算出V的TM减一呃的加的值，也就是put option，American put option。

在T减一时刻的value，那我们再把它discount delta步，就discount到TM减二，然后再返回这一步值算到T0为止。



![](img/0b311f50277b9da4cc039119e5d2bdb0_72.png)

那我们这边可以看一下我们的这个Python举例，那我们是用这个new ero的这个表达式，我们假设呢maturity是一年，然后呢S0的stop pass呃，price是100。

那么strike也是为100，RETT的是0。25，跟我们上面的这个european option的设的是一样，那我们的这个无风险利率呢是0。1，那我们知道我们这american put。

的理论价格是6。523，那我们来看一下，我们用LISQUMONICCOLO算出来的值。

![](img/0b311f50277b9da4cc039119e5d2bdb0_74.png)

是不是跟这个比较接近的，那我们我写了一个这个MC点PY。

![](img/0b311f50277b9da4cc039119e5d2bdb0_76.png)

那么嗯它的里面的具体实现呢是这样的。

![](img/0b311f50277b9da4cc039119e5d2bdb0_78.png)

这个fit u呢其实就是fit我们的这个decision boundary。

![](img/0b311f50277b9da4cc039119e5d2bdb0_80.png)

也就是啊这一步的过程，那么呃fit u最后输出的是一个拉姆达，又是我们第四声帮助你的这个表达式，是一个关于stop pstop price的一个二次项。



![](img/0b311f50277b9da4cc039119e5d2bdb0_82.png)

那么我们这个fit ex呢，就是最后我们输出的是我们的，我们是否early exercise或者keep the value。



![](img/0b311f50277b9da4cc039119e5d2bdb0_84.png)

也就是输出，我们这个E也就是一个叫我们我们把它叫做，也是指示函数，就是不是取一就是取零。

![](img/0b311f50277b9da4cc039119e5d2bdb0_86.png)

那是根据这个大小关系，然后呢，嗯这边呢是这个early exercise。

![](img/0b311f50277b9da4cc039119e5d2bdb0_88.png)

帮助里的表达式的输出。

![](img/0b311f50277b9da4cc039119e5d2bdb0_90.png)

那么最后o overall的东西呢，都放在这个american opt里面，那他第一个需要输入的是stop path，也是我们similarly出来的这个几何布朗运动。



![](img/0b311f50277b9da4cc039119e5d2bdb0_92.png)

第二个呢是一个discount factor，也就是我们的这个嗯E的负啊。

![](img/0b311f50277b9da4cc039119e5d2bdb0_94.png)

Delta，那这个EXV的这个F呢，嗯需要输入的是这个exercise value function。



![](img/0b311f50277b9da4cc039119e5d2bdb0_96.png)

也就是我们是需要take的是一个vector，那我们这边early size function是一个put price，所以我们把它的pay off放在这边，也就是K减去S逗号零。



![](img/0b311f50277b9da4cc039119e5d2bdb0_98.png)

取一个maximum，那这个EXF呢是定义。

![](img/0b311f50277b9da4cc039119e5d2bdb0_100.png)

我们是选取什么样的体积深function，那我们使用的是这个feit ex。

![](img/0b311f50277b9da4cc039119e5d2bdb0_102.png)

也就是我们固定了我们的这个表达式呢，是一个二次的，那么opt ex呢是是不确定我的DISION。

![](img/0b311f50277b9da4cc039119e5d2bdb0_104.png)

boundary的表达形式是什么样的，那我们这边使用的是face。

![](img/0b311f50277b9da4cc039119e5d2bdb0_106.png)

那fix之后呢，我们就把它放进来进行循环，这边是定义初值，然后呢是从第一倒数第二个开始循环到呢。

![](img/0b311f50277b9da4cc039119e5d2bdb0_108.png)

第呃T等于零的这个点，然后最后呢再把我们的这个price跟这个迪decision。

![](img/0b311f50277b9da4cc039119e5d2bdb0_110.png)

帮主给输出，所以我们最后输出的梦，list moniccolo的价格呢是这样的，大家可以发现呢值呢只差了啊0。01，也就是1%，所以呢我们这个list ramediccd的值呢是可靠的。



![](img/0b311f50277b9da4cc039119e5d2bdb0_112.png)

那接下来我们prat一下，我们的这个ercise boundary，那大家可以看到我们这个迪士声帮主在这个呃，一年内的这个分布应该是什么样的一个情况。



![](img/0b311f50277b9da4cc039119e5d2bdb0_114.png)

然后我们把我们的这个stop pass跟这个list square feet呢，我们给present在这个地方，那这个红线呢，也就是我们每我们最后一步做这个LISQUARE。

monte carlo fit出来的这个DISCN，帮助这样的一个表达式。

![](img/0b311f50277b9da4cc039119e5d2bdb0_116.png)