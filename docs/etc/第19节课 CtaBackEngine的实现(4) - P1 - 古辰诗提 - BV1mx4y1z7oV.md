# 第19节课 CtaBackEngine的实现(4) - P1 - 古辰诗提 - BV1mx4y1z7oV

欢迎大家来到从零开始量化系列课程，VMPI课程的第19节课，上一节课呢咱们讲到了这个process new bug，也就是合约的撮合，合约的撮合。

其实算是整个btesting engine里面最核心的内容了，这一块你一定要搞明白，一定要搞明白，可能会有些绕，希望你多看一看，首先咱们肯定先去进行一下，就是说这个切割，你肯定得就是说撮合不光是停止的。

还有限价单是吧，所以说咱们得给它分成两个方法去给他去完成，首先第一个是cf点啊，Class class limit order，把这个bar给他传过去，然后四点class stop order。

把这发型给他传递过去啊，然后咱们定义一下啊，cos啊，Limit order cf8。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_1.png)

PDA是吧，好咱们先pass一下，然后d e f gis are stop order，然后把这个cf给他放进去，bar br data好pass好，首先咱们来先说这个limit order。

limit order的撮合肯定是用这个霸线的，它的这个价格来和，就是咱们存储在了那个live orders里边的。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_3.png)

这个order委托就是存放在这个里边。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_5.png)

所有的order委托进行一个对比，然后如果说有满足条件的，就去让它成交，对不对，好，所所以说首先第一步咱们得检查一下，检查什么呢，就是看看这个CD limit orders有没有order。

没有order就直接可以return了对吧，所以说if not slimit orders就直接return了啊，你想这样的代码啊，你一定要会写，以后多用这样的，因为什么呀，如果说你换一种方式。

就是if self limit orders，你这么来写呢，就是就是整个这个下面会都在这个，衣服下边儿呃，感觉不是很好，这样的话你下面就不用，就是整个的代码就都涵盖在这个if下面了啊。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_7.png)

如果说有这个LIORDERS，咱们是不是就应该去查看是吧，For order in self limit orders，点values，就是这个是获取每一个这个order，然后去进行查看嘛是吧。

他是通过VTO的id作为key。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_9.png)

然后order作为value进行存储的是吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_11.png)

咱们说也说了，为什么他会用那个VTUO的id来进行呃。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_13.png)

就是说这个做key啊，这个跟整个stop order id啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_15.png)

这个是VTL的id是吧，这个是被跳大D，咱们把这个order给print给删掉啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_17.png)

嗯好那咱们就是说便利了之后，咱们肯定是首先得看，就是说他的这个就是这个状态啊，这个咋怎么说呢，在原本的这个代码里边，也是后来这个维纳新添加进去的，它有一个就是它有一段这个代码肯定是有用处。

但是呢看你愿不愿意去添加了，他会怎么办呢，它会if order点studio等于studios t。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_19.png)

就是这个状态导入这个包，在这STATUS啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_21.png)

这个studio t a t u s，第二就是submitting，如果说他的这个状态啊，还是在申请中，如果还是在申请中的话，就把他这个状态order studio等于s t a t studies。

NO traded啊，然后呢去调用一下s t r a t o on order是吧，把这个order给他放进去，这段话是什么意思呢，就是如果说你在申请中，我给你把他这个状态变为NO trait。

然后再回调给这个order，其实这算是贴合，就是实际的行情，就是发你发限价谈委托的时候啊，除非出现这种极特殊的情况，就是你的这个委托价格超出了它的这个边界，这个边界是指这个涨跌停价，除了这样的情况呢。

你发的这个委托价就是限价单，都会被这个服务器所接收啊，都会被服务器所接收呃，当然你可能就是说差的，这个跟当前行情的这个价格差的比较大的话，它会一直在那等着，所以说他会告诉你还没有成交啊。

然后你就应该判定他是不是有这个，long cos c l o s就是有这个多单的成交啊，撮合成功啊，long class它这个布尔它它这个返回的是这个车祸force，然后满足ln class。

它有哪些条件呢，你首先你的方向就是order，第2direction啊，等于等于direction点浪对吧，你首先你得是多方向的，这个不管开屏，就只要你是买。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_23.png)

就是代表多方向嘛，它就应该是long class，就是多单成交，另外你还得满足一个条件，这个条件是在什么情况下，他应该去成交，也就是如何去撮合这个呢。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_25.png)

咱们得捋一下，这个很关键，比如我发了一个限价单，我这价格在这儿，比如说这个价格比如说是五是5000块钱，那在下一根K线它出现什么样的一个情形，它是能成交的呀，就是买限价单，它有一个逻辑就是什么呀。

我成交的绝对不能比我这个价格高，对不对，所以说你这个在下一根K线，只要出现了你这个价格，我就认为他成交了啊，这个你没办法去判定成交量啊什么的，因为除非你有tick数据。

当然这个数据也不能完全模拟这个实盘，是不是，因为你不知道它的成交量和这个它的买一卖一，对你的成交有什么影响啊，这个你如果想越多的去贴近，就是实盘的话你越得往下去研究，但是对于咱们一分钟航行。

只要只能判定这个一分钟，它的这个K线和这个价格的关系，然后来判定它能不能成交，还是刚才那个就是说，如果说下一根K线出现了这个价格，是不是我就认为它就是成交了，是不是，那按照这个逻辑的话。

你这根K线出现这个价格应该是什么逻辑啊，应该是它的最低价，就是比这个你定的这个价格要小于等于是吧，我也就是我这个价格要大于等于它的最低价。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_27.png)

我就默认它成交了，是不是，所以说应该是order点price大于等于应该是什么呀，就是这个八点low price吧是吧，这个就默认成交了吧，是不是好，咱们再来判定shirt cross。

好首先它的这个order direction，它是不是应该等于direction shirt，咱们再来分析一下你这个空单，空单这个价格就是说我卖我卖的越贵越好，就是卖的价格不能低于我当前这个价格。

那在你的这个下一根K线里边应该是什么呀，就是说只要是出现了这个价格，或者高于这个价格了，就默认它成交了吧，所以说应该判定它的最高价啊，同样的这个K线，它的最高价只要大于等于这个价格，是不是就默认成交了。

对不对啊，一定要理解这个啊，就是限价单买买的越便宜越好，这很容易理解啊，就跟你买东西似的，我买的越同意，就是同样的品质买的越便宜越好吗，我卖东西在同样的品质下，我卖的越贵，是不是我挣得越多是吧好。

那就是应该是什么呀，应该是older their price，就是小于等于八点，High price，这个就默认两个是成交了吧，对不对啊。

如果说if not short class and not long class，是不是这个我就可以直接略过了，就是这个就说明在这根八线里边儿。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_29.png)

这个委托三没有成交，是不是我就可以continue了吧，如果说有成交，if long class有成交的话，咱们首先得确定什么呀。

他的trade price是不是他的trade price就是它的成交价，那成交价咱们如何去确定呢，可能容易理解的是什么呀，就用older their price，但是你考虑一下这个逻辑啊。

就是你委托发送的时候是前面一根K线结束了，下一根K线，如果说它的开盘价就低于啊，我指的是多大啊，低于你这个价格就比你报出这个价格要低了，是不是我就应该是立马就成交了，是不是。

那如果说开盘价没有低于你的这个呃，这个价格后续的价格咱们就没办法去呃了解了，因为他只有高开低手这几个值是吧，在一分钟K线里边，所以说咱们就只能以你这个价格为准，是不是这个是最合理的吧。

你既不能说我都按这个来进行这个来确定价格，那都按这个的话，你开盘价，那这一块是按道理是很符合逻辑的，因为你开盘价低嘛，是不是，但是如果说都按就是呃这个开盘价，开盘价要是高上去的话。

不符合你的limit委托，那如果说都按你的这个最低价的话，可能比它低的很多，那这个东西就会出现你的回测的偏差，或者跟你实际的成交会相差很大，只有这种方式，就是说我在开盘价和和我的这个价格。

之间做一个选择，是不是这样是最好的啊，那我的这个tra price我就应该挑选一个最低的吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_31.png)

就是拔掉open price和我的这个order their price。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_33.png)

中间选一个最低的，既然这根K线出现了这个order prize，这个价格，说明他在咱们回测里面默认它肯定能成交的好，如果肯定能成交，它的开盘价肯定要在它的最低价之前，或者说最起码是两个时间节点是相等的。

是不是如果说开盘机制啊，比我这个order press要低。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_35.png)

从逻辑上来说，是不是我应该按照开盘价来进行成交，对吧啊，好，这是啊，Long price aif shirt clothes，这个你一般在写这个if air if的时候，你少用else。

因为这个很多时候，比如说你写了三四个if air if后面加一个else，你容易把ELS给忘掉啊，容易把ELS给忘掉，就是你在尤尤其是debug的时候，你会忘掉啊。

好这个trade price咱们是不是就可以直接写了，就是max8点这个open price和这个order点price对吧，就是我开盘如果就比我这个价格高了，那我就按开盘价来成交，如果说开盘以后。

我就不知道是就是呃他是个什么情况了，会在什么时间节点出现我这个order price，所以说我就按照我order price来成交，对不对，好，那这个就是委托就算是成交了，对不对，那我得委托成交了。

我得回调这个strange，那我回调，我首先得把这个order掉里边的一些对象给变化啊，比如说他的这个studio，它应该等于什么呀，就是STATUR点o traded是吧，他已经全部成交了吗。

另外还有一个什么呀，就是他order里边有一个traded，就是成交了多少手，咱们这就直接等于order点VN是吧，就是就是我就认定它为全部成交了啊，因为这个的话你想去贴近实盘。

这个永远不可能因为什么呀，实盘这个它是一个撮合逻辑，你在这，它只是一个根据你的这个数据来做一个，数据的处理，对不对，所以说你这就等于order点volume是不是就可以了啊。

然后这个时候你是不是就可以去进行回调了，就是self点strange点on order，然后把这个order给它放进去啊，回调完了之后，咱们是不是就应该给他生成这个trade data了啊。

Try data，导入一下这个try data。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_37.png)

Trade data，try data等于我给它生成一个trad，这个里边gateway name，首先getaway name就是cf点啊，Get away name，然后第二个是什么呀。

simple simple应该是等于simple是吧，S y m b l，那这个simple我没有，我还是得去拆分一下啊，simple呃。

exchange in c h e x c h n g x等于就这个CVT，然后把这个exchange给它翻过去啊，exchange翻过去，然后后边这个order id。

order id就是应该是等于order order id吧是吧，Oro d o d。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_39.png)

然后后边的china china d，咱们是不是得生成一下，得生成一下吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_41.png)

所以说这咱们肯定是得添加啊，self点trade，try count吧，它是一个int类型的啊，等于零，然后我在这on word下面啊，cf点tread count加等于一是吧。

然后try的id应该是等于什么呀。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_43.png)

T r a d i d trad，它应该是STR类型的，它应该是等于我在这儿我再加一个是吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_45.png)

try的。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_47.png)

它的前缀出的前缀TRAD就直接写出来的吧，啊trade，然后这就应该try AD，还是这个F两个中间用点啊，第一个是什么呀，就是说这个try的就是它的前缀啊，第二个是cf点try count吧对吧。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_49.png)

然后这的trad等于try的id吧，嗯好下一个direction，direction应该是等于order的direction吧，嗯嗯然后offset等于order点offset。

price等于trade price吧，然后volume等于这个order点VLO，最后一个dead time daytime，应该是等于C点daytime吧是吧，这个trade就是不给他创建好了。

创建好这个就说明它是成交了是吧，那成交了是不是应该去改一下他的这个仓位，是不是strange点pose，应该是加等于它应该是什么呀，如果说你是多单的话，是不是应该减空单的话，是不是应该加，是不是啊。

你应该是等于什么呀，就是四点strange pose，C点strange s t r a t e strange点pose，然后加上这个order点。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_51.png)

if是什么呀，if这个是long class是吧，是多单除法。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_53.png)

else应该是等于cf点，strange减去a self。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_55.png)

DISTRANGEPOS减去order点WW，是这个逻辑吧，我从这儿给他用一个反斜杠。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_57.png)

这样是不是就可以了，就是你把他的这个策略的。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_59.png)

就是它的持持仓啊进行了一些变化是吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_61.png)

当然在原本的那个呃VMPY里边，他是这么来写的。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_63.png)

他在这啊，他在这如果是long class的话，他的这个啊他给了一个这个pose change啊，等于order点volume啊。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_65.png)

然后如果是是空单成交的话，他把这个pose change等于负的order of。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_67.png)

然后他就直接在这啊，strange pos加等于这个pose change啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_69.png)

这个也可以的，但是看着更加的利索是吧，没有那么长的代码啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_71.png)

都可以啊，好这个try就是已经作为这个什么成交了，成交了之后这个try的呀，咱们是不是应该给他保存一下。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_73.png)

因为咱们最后还得看它成交的，是不是跟咱们用维纳平台回测的那个成交。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_75.png)

是不是一样的，包括你在之后去计算它的这个一些指标的时候。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_77.png)

是不是肯定得用到try的对吧，所以说咱们从这儿呢给他看self traders啊，它也是一个DICTOR，然后是这个STR存储的呢是这个trial data啊，然后等于啊，然后咱们这儿给它添加一下。

就是cf点cf点treads这个它的key，咱们用tread点vt try AD，这个v t try it i d啊，其实是跟这个VTOD是一样的，它就是你的try to d里面。

前面加了一个cgv name啊，就是这个没什么，咱们只是为了跟这个实盘或者跟维纳更加贴近，然后等于出是不是就可以了，另外别忘了self distrange，回调它的这个on triad是吧。

On trade，然后把这个trade给它放进去，是不是就可以了啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_79.png)

这个就可以了吧啊这个就是class limit order，下面还有个close stop order是一样的，这个咱们就写的稍微快一点好吧。

好if not self stop orders就return对了。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_81.png)

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_82.png)

上面有个忘了说了，就是这个order已经all tragedy了。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_84.png)

我是不是应该把它从这个CLIMIT，orders里面去删除掉，对不对，你最后应该把它给pop掉，就是cf点这个limit orders，然后点pop是什么呀，应该是order order呃。

这个VTOID对不对，但这有一个非常就是值得大家注意的一点。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_86.png)

就是在循环之内啊，你不能改变你这个字典的。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_88.png)

你不能改变你字典的这个长度，什么意思呢。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_90.png)

给大家演示一下啊，就是新建一个demo是九点PY。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_92.png)

好就是比如说我有一个字典A哈，他是这里面我随便写一个A1A1B，二好我这个时候呢我for i in a点values values，for key value in a点items items。

你这是在便利它是吧，这个时候呢我A点pop，A点pop这个key从里边我把它给删了，这个会报错的啊，肯定会报错，你就是说字典在iteration就是去便利的时候嘛，在迭在迭代的时候呃。

这个这个iteration是ITERABLE和iterator是吧，迭代器呃，迭代对象可迭代对象就是他在迭代的时候。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_94.png)

它是不能改变它的size的，就是不能改变它的长度的。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_96.png)

所以在这呢你想要实现这个pop的话，你必须得在前面加一个什么呀。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_98.png)

就是说你把它强转成list s t强转成list啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_100.png)

强转成list，同样的你从这你想去删除它的话，应该是什么呀，for key in a点kiss，这样这个时候你删除呢，他应该是还会会报错，但是如果说你前面加一个list，就是把它变成了一个列表。

等于是啊等于是你新建了一个列表，然后把它给填进去了啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_102.png)

这个时候他就不会了，对吧啊，这一点呃是比较容易出问题的一个地方啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_104.png)

虽然只加了一个list，但是没有这个list肯定会报错的啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_106.png)

所以说代码里边没有一个单词，它是没有用的好吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_108.png)

那咱们就往下写，for stop order in cf点in list，别忘了啊，cf点这个stop orders values去便利它。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_110.png)

去便利它编辑它的时候，咱们这儿就不去调用那个什么了，就是这个把它改成这个什么NO trait，而且stop order里边有NO trait吗。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_112.png)

咱们可以看一下啊，这个stable，Stop order trait，还是waiting是吧，一触发一撤销只有这三个，所以说他没有这个NO trait。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_114.png)

所以说就不用去写了，咱们直接判定long class，one class等于这个括号，首先还是就是说这个stop order，direction等于direction点long。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_116.png)

那后边咱们就需要去分析它的这个价格，如何去进行判定，这个这个stop order和limit order，咱们之前一直在说，limit order是符合咱们正常的一个逻辑的。

就是我买东西我就买的越便宜越好，然后卖东西卖的越贵越好，但是其实就是这个stop order，咱们一直说他跟这个lime order是反过来的，但是你逻辑上不通顺呀。

那没有人会说我买我就要买的特别贵是吧，同样的品质买的特别贵，呃我呃我卖啊，我同样的东西我卖的特别便宜，越便宜越好，没有这种可能性，他的目的是什么呢，他的目的是什么呀，我必须得到这个价格我才出手啊。

对吧啊，比如说我要买房，你房子在在3000块钱的时候谁买啊，因为他没有这种就是挣钱的属性，或者说是你投资的属性，好房子还涨涨到3500了，我再买是吧，那就说明他一直在涨，对不对。

咱们是不是通常都是这个逻辑啊，都是这个逻辑，另外包括你想啊这个stop time在开车在开仓的时候，咱们得等到一个价位去进行操作，然后在平仓的时候，它是不是一般都作都作为一个止损了。

是不是就是说他不到那个价格，我不评是吧，他到那个价位我才停的对啊，所以说他应该是等到那个价格，得等到那个价格是吧，所以说你有这个逻辑的话，你多单就是也不是多单啊，就是你多方向，不管是买多单还是凭空单啊。

这两个方向是多嘛，对不对，你买多单的时候，你就是你你报了一个价格是在这儿，然后他的这个我指的是买多，就是开多仓啊，他的这个价格肯定是在它下面的，是不是往往上走的，如果说是你凭空仓的时候，你这个价格。

你也是等着它这个价格往上走的是吧，不然的话你价格在它上面，你用stop dan你去评，你去评的话，咱们用这个什么这个逻辑来说，就是比如说我这个是我这个stop价格，你你你价格还在这儿呢。

那我要凭这个多单的话，不是要凭这个空单就是多的方向嘛，我要凭空单的话，我就是stop单和LIM单相反，LIM单是我买的，就是我买的越便宜越好，那stop丹，就是说我就是在这个价格我就可以成交了对吧。

就立马就成交了啊，这个是咱们之前包括在我很多课里边都说过，反复强调过，就说什么场景用stop done，什么场景用limit da，什么情况下你不能用limit dan和stop done。

它会导致他立即就立刻成交，你像这种情况，你stop单挂在这，你价格还在这呢，你要挂stop单的话，你立马就成交了啊，你立马就成交了啊，所以说你以这个逻辑就是说我这个是多单的话，我的价格肯定是在下面的。

那价格在下面，然后我要等到这个价格再开始买，我是不是应该判定它的最高价，就是我下一根K线的最高价，如果最高价大于等于我这个价格了，我是不是就可以判定那成交了啊，这个时候你就不能看最低价了吧。

最低价就是你要说大于等于，你说最低价大于等于就是完全就不对了，因为你最低价大于等于的话，你最高价肯定是大于等于，那你就说最低价要小于等于这个价格的话，他可能这样是吧，他就达不到，对不对。

所以说你应该是最高价大于等于你的这个价格，是不是就可以了。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_118.png)

是不是，所以说应该是应该是怎么写，应该是最高价八点high price大于等于你的这个order啊，这个stop order their price。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_120.png)

对吧啊，这个一定要好好去理解啊，shut class c l s不等于好，这个stop order direction应该是等于direction shirt，然后这个时候你再判定就是说这个空单。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_122.png)

空单就是说我要么是开空仓，要么是平多仓，是不是我我开空仓的时候，我肯定是什么呀，我就说这个价格，比如说我开还是开开5000，开5000，我得等到出现这个价格，我再去开，那肯定价格是在上面的，对不对。

你在下面的话，它就会立马就成交了，所以说价格是在上面的，所以说你开5000，你得等到他什么呀，有这个最低价就是小于等于啊，这个应该是小于等于是吧，应该是小于等于这个5000是不是就可以了。

有最低价小于等于5000就可以了啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_124.png)

好所以说应该是嗯就是这个八点这个low price，然后小于等于啊这个stop price，stop order the price啊，这个是不是就满足了这个空单成交的条件。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_126.png)

对不对，那下面就是跟咱们就是这个limit就类似了吧，就是当这个满足了这个long class和class，就说明他有触发了，但是如果不满足的话。

就是if not long class and not shockles就continue吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_128.png)

这continue一定要写对啊，你写return的话，它就直接这个它就不循环了啊，If lg class，你首先得判定它的这个trail price是吧，P r i c e trade li。

这个应该怎么去进行对比啊，这个应该怎么去进行对比啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_130.png)

同样的啊，就是这个价格啊，然后在这他有这个肯定是等到这个价格了，那肯定还是拿开盘价是吧，这个open price然后进行对比，然后呢open price对比就说后边肯定是就是说呃。

如果说你是long cos的话，它对比的是这个八点HYRICE吧，对不对，八点high price吧，啊不是这个open price和当前的这个price来进行对比吧，他肯定是挑一个什么啊。

挑一个较高值吧，是不是挑一个较高值啊，为什么说挑一个较高值，就是你这个价格我得等到你这个价格，然后再去进行就是操作，那我开盘的时候就比你这个价格要高了，是不是我得立马去进行操作是吧。

如果说开盘的时候没有比你这个价格高，或者也没有等你这个价格，那我是不是得在后边它的这个呃，就是说其就是这个其他的这个价格里面去找，但是咱们看不到这个一分钟K线里边，tick的情况。

所以说咱们只能用这个这个stop price是不是，所以说你应该挑一个较高者是吧啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_132.png)

挑一个较高者应该是max这个八点open price，和你这个stop order点price。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_134.png)

是不是啊，同样的这个pose change咱们也提前写啊，pose change如果是long class的话，应该是这个这个stop order点volume吧。

啊然后air if short class这个trade price应该就等于mini嘛，就是这个八点open price和这个stop order点price，来进行对比吧，就是找他就是较小值。

是不是从这你就能看出来啊，就是说你看啊他是找这个较小值，较小值就是说明找比我这个价格更小的，就是卖的越便宜越好，是不是，然后找较大值，就是相较于我这个发送的这个价格，找一个较大值。

是不是就是买的越贵越好是吧，为什么说他跟lion是完全相反的，你从这呃就是就能看出来是吧，而并不是说从理论上，从理解上来说，并不是说我要卖的越就是我要卖的越便宜越好，我要买的越贵越好。

只不过我要等到那个价格是吧，但是在实际的错误过程中，尤其是在回测里边，你可以这么理解，包括成交里边也是这样的，你去理解的啊，因为底层的呃不是这个在CT引擎里边，它是用涨跌停价去发，他得等到。

就是说这个价格等到了这个价格的时候，他又转涨跌，定价很容易就出现滑点，对不对，但是也有可能出现很偶然的情况，他碰了一下这个价格就反方向跑了，也有可能出现正向的滑点，但是大概率是反向滑点对吧。

这个一定要理解清楚了啊，不然的话你这个没法去写代码，因为这个写代码其实写，写到最后还是一个逻辑上的问题啊。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_136.png)

逻辑上的问题好，这个两个都有了之后，咱们是不是首先应该去改变一下，就是说这个stop order啊，点studio是吧，应该等于stop order，stop order点studio啊。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_138.png)

这个没有导入导入一下啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_140.png)

stop order应该是在这stop order their studio。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_142.png)

把他的这个studio的stop order the studio改成这个呃。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_144.png)

trip就是触发了是吧，然后呢。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_146.png)

这个stop order它还有什么东西需要去改变的吗，啊需要去赋值的吗。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_148.png)

啊，stopped这个volume也没有，Direction strange name，the time就没有了吧，也就是这个studio还有这个VTODVTOID，咱们之前也说过，它是存放什么呢。

就是因为你的这个停止答案需要转换成这个order，就是这个限价单去发送给底层，那限价单可他给你拆分的时候，可能会拆分成一个限价单，也有可能拆分成多个，那每个限价单它是不是也有这个v to ord啊。

他会把这个VTOID放到这个，就是他的这个stop order这个VTOID里边啊，主要是存放这个的，为什么它是一个可变数据类型呢，它是一个列表吗，他就是为了存放一个或者多个。

这个由step order转换成的这个limit order，它的这个委托单号啊，委托单号好，那咱们是不是得有他的这个委托单号啊。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_150.png)

那在有委托单号之前，咱们是不是应该去创建一个order data是吧，Order data，然后因为你这个order data在实盘过程中，你给他转换，you stop单，你stop单触发之后。

你转换成限价单去发出去之后，他成交了，或者说他发到底层了，他也会去调用on order吧是吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_152.png)

咱们之前看过这个C这个CDP引擎的吧，就是你在SORDER这in order这。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_154.png)

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_155.png)

就是它发送到底层，最终是到这吧，到这之后他肯定会去调用这个on order的，是不是它只不过是放到事件引擎里边去吧，啊所以说你从这个order。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_157.png)

你肯定是得创建一个这个order data的啊，是给这个stop order专门创建的这个order data啊，这个首先这个gateway name等于cf点啊，Gateway name。

然后这个symbol应该是等于simple nb啊，你还是得去拆分一下是吧，从这啊，当然你可以直接呃在这个音初始化的时候。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_159.png)

给他把这个simple和X线也都给它给复制出来啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_161.png)

这个就省得每次用的时候都得拆分一下是吧，我这因为写了这么多了，我就不去改它了啊，exchange等于change，X减去后边是呃order id，Order id。

order id是不是咱们也得去给它创建一下呀，就是这个order id，那首先就是self点啊，limit order count是不是得加等于一啊，然后这个order id等于它是一个STR类型。

等于什么呀，哎STR类型它等于F这个，然后一个前缀加一个后边的这个是吧，这个是limit order prefix，然后后边加上cf点limit order count吧是吧。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_163.png)

这个order id就等于order id啊，然后呃O的id后面有了这个tap order type，Order type，那肯定还是limit，我就不写了啊。

然后direction是不是应该等于direction的啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_165.png)

不是等于这个stop order direction吧，Stop order direction，然后offset等于stop order of s。

然后price等于这个等于咱们就cha price吧，啊这个其实放哪个都可以啊，啊就用trader price吧，因为他发送的时候，你要模拟底层的话，他肯定是用涨跌停价去发的是吧。

后边还有什么price，后面vu volume等于这个stop order点，volume volume后边studio s t a t u s studio，等于还是等于先等于submitting嘛。

你放到底层，你是不是先得submitting，是不是，然后后边还有个time给他写一下啊，daytime等于C点啊，这个daytime你放到底层是不是先去呃，就是这个咱们先去on strange一下啊。

Strange on order，这个等于是放到服务器了啊，先去进行一下触发是吧，就是先提交到服务器，然后服务器呢模拟它完全成交了，所以说这个order点studio就等于啊。

X t a t u studio or trait or trait，完了之后，是不是你还得回调这个什么呀，就是说这个呃就是这个卷积order是吧，就是去毁掉这个on order吧。

但是啊就是你触发在这个order之前，是不是应该先回调这个stop order，是不是在他这个发送到底层之前，因为你先触发嘛，你先触发，你就应该strange，第2on stop order。

把这个stop order给它给放过去，先触发嘛，然后再到底层调用own order，是不是，然后假设他全部成交了，然后再回头再调用一个strange点on order对吧，就是全部给触发了嘛是吧。

就是他的这个studio这个就变成all traded了吧，同时还要给他改变的就是order traded吧。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_167.png)

啊等于这个stop order your warm，是不是这个流程你还是得走的，是不是，不然的话，如果说你在策略里面调用到了这个on order，Australian，点击这个它和实盘不一样。

是不是也会产生问题，你别忘了前面这个stop order，咱们为什么要创建这个BER，一个是为了方便这个调用，另外一个你得把这个stop order点VTOID，应该是点append。

把这个什么给添加进去啊，A p p in the end，把这个order点VT的id给添加进去吧，对不对，直接用这个stop order点video is a pen，因为它是个list。

直接给添加进去啊，是不是就可以了，是不是啊，捋一下逻辑啊，就是在实际过程中，首先就是先是stop order出发，stop order出发之后，他会给去发送一个委托到底层是吧，发送委托到底层。

它发送成功了之后，它会有一个返回这个VTOID啊，所以说你第一步应该是先unstoppable是吧，你肯定是得先发送到底层嘛，是不是，然后呢呃发送到底层之后呢，它有返回值了之后。

然后会把这个这个order点这个VTOD，给到这个stop order，然后这个stop order再去调用strange on stop order。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_169.png)

对吧啊，没有问题吧，然后底层如果说是成功的成交了，然后它会就是说给反馈啊，然后成交了，然后再去调用这个on order是吧，这个不是on bar啊，是on order，是不是啊，我的是吧。

这个逻辑一定要捋清楚啊，尽量的贴近于实盘，然后最后他成交了，成交了肯定是有这个try的吧，TRA啊，Trad。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_171.png)

咱们刚才把这个tread光写了个try count是吧，没有写这个c trees t r AD s啊，写了啊，写了serve trees trees。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_173.png)

之前上面那个给添加进去了吗，on trade没有给tries也添加进去了啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_175.png)

好然后这个trade data等于try data。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_177.png)

然后这个首先啊这个get to name就等于一个。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_179.png)

我直接算了写吧，给ta name等于C点gta name，下一个symbol等于symbol。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_181.png)

exchange等于exchange。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_183.png)

好这个order id等于order。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_185.png)

应该是这个上面这个order order，Order id。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_187.png)

其实你这个order order id这个trade啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_189.png)

它本身它是应该根据就是最顶层的这个stop order，它进行成交的，当然你说他根据这个order进行成交也可以，这个都可以，那我就直接写这个呃order order id了。

我就不写那个stop order id了啊，OD后边应该是什么，OD后边应该是try的id，Tri i did try id，咱们是不是得写一下啊，就是cf点呃，trade count加啊等于一啊。

然后trad t r AD，china d等于F两个中括号是吧，两个中括号，然后这个里边是try的prefix，然后后边是这个cf点，trail account好，try的id就等于try的id。

然后这个，Direction，direction等于order the direction，Upset等于order点，Upset哎o offset，然后price等于trade price。

vo volume等于order点volume，啊然后还有个daytime，the time等于cf点DETO。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_191.png)

是不是这样就可以了，然后同样的咱们得在下面cf点卷接点，pose加等于pose change吧。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_193.png)

然后self strange点on strange啊。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_195.png)

on trade是吧，把这个trade给它传递过去，然后最后你还得把这个pop掉，把这个C调stop orders点pop，这个这个stop order点orstop order id是吧。

咱们添加的时候是用stop order id往里去添加的啊，然后最后self tries，这个他的这个try的ID是吧，t r AD try的D等于train。



![](img/2ee9004fe4028dcccb6dc3d5809e39ea_197.png)

是不是这个就整个的就流程就完了，是不是啊好。

![](img/2ee9004fe4028dcccb6dc3d5809e39ea_199.png)