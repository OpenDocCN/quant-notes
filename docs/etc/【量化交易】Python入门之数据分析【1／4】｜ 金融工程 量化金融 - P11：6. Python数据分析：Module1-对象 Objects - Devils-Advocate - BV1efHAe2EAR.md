# 【量化交易】Python入门之数据分析【1／4】｜ 金融工程 量化金融 - P11：6. Python数据分析：Module1-对象 Objects - Devils-Advocate - BV1efHAe2EAR

![](img/9b149dd1c4929e33a4fe6be702c58f02_0.png)

这节课我们来讲一下object and map。 objectsject呢是呃pyyon里的对象，这个对象是什么意思呢？不是你谈对象的对象，是呃它是一个类。比如说class。呃。

我们打头这个这个object开头就是class，就是我们拿就像就像。呃，函数它是defineDEF一样。这class比如说呃。School。啊，我们这是一个school class。

这个学校这个学校呢有一个department。departmentpart是什么呢？ music。音乐。那这里类里面呢一般会套套一些这个函数，比如说the fun。Set name。

然后这边肯定会有ex个self。然后new name。self name这个self就什么意思？你就指他自己。New name。我先把这个写完哈。😊，Said。Location。这边也有个self。

New location。大家不太明白，没关系，我一会儿跟大家解释，然后呢，self location等于new location。呃，我们怎么用它呢？比如说这是一个类，我们已经把它做好了，比如说go。

等于。

![](img/9b149dd1c4929e33a4fe6be702c58f02_2.png)

Scool。这是给它做一个初始化。那么这个就是以这这是这是你可以把它类理解为一个模板。就是它这个呃学校里面呢，它就会有music，嗯，对吧？这个department当然你可以有其他的。

但这个学校它只有music，嗯，但我可以干嘛呢？对吧？这边是比如说这个school。Said name。L网。



![](img/9b149dd1c4929e33a4fe6be702c58f02_4.png)

这里面有个老师，他是王老师，他叫alice王ong，然后还可以干嘛呢？这个s school他。呃，在在什么地方？Sa location。



![](img/9b149dd1c4929e33a4fe6be702c58f02_6.png)

比如说。上海。

![](img/9b149dd1c4929e33a4fe6be702c58f02_8.png)

对吧那所以所以呢这个这个school我们就给他定义了几个东西，一个是原本他自己就有的，它是music。第二个呢是我们给他的证明的老师。嗯，这个学校有一个叫王老师，alice王的老师。

然后jaake school在上海。alice王呢这边我们我们就像前面样的，这不是一个点嘛，set name我们在school里面。调用了这个set name这个函数。

然后呢把alice brown传到这个new name去了。new name等于self name啊，这个self呢放在这儿，它是在类这个里面啊它能通用。就是我能在这个类里面调用这个name。

所以要new name等于self到 name。然后我们把上比如说alice给self name放到这里来了。呃，这个self大家如果还不理解呢，我们后面会有呃比较详细的一个讲解。

就是我们可以在这个呃school里面啊继续调用这个self嗯，它在这个类至少在这里面是通用的意思。就像就像我们呃一个函数一个一个函数一样。

那么我们在函数里面它给它的variable只只有在函数里面才能互相调用。那在外面你这个new new name如果单说一个函数哈，就像我前面就是如果大家还不太明白，我们就是你可以看一下第一节课，呃。

我们在外面再设一个一样名字的函数呃，一样名字的变量。嗯，它其实跟类里面的这个变量呢是两个东西。所以说我们要想在上下在这个class里面调用这个name呢，你不能直接不不能直接用new name。

那你要用self name。你是就是这相当于我把alice斯邦给复制成这个类里面的name。那这个类呢它就有了。呃，他就有了他自己的一个东西啊，叫做name。比如说我调用了school。

namealice对吧？呃，就相当于不这不是这虽然我 said是一个new name，就是一个新的名字，但是我把它复制了复制给了这个名字，然后这个名字又属于这个学校的这个学校的老师嘛。

alice或者这个学校在在哪个location呢，我如果用s location行不行，那肯定不行，对吧？这肯定说他没有这个attribute，没有他这个属性，你你也可以就他这个模板嘛。

模板有不同的信息嘛？这个信息里面有名字department有这个location，那我可可不可以用这个location呢，那应该是新的对吧？他在上海，那我调要用这个department呢？



![](img/9b149dd1c4929e33a4fe6be702c58f02_10.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_11.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_12.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_13.png)

那也可以，对吧？所以这个是。

![](img/9b149dd1c4929e33a4fe6be702c58f02_15.png)

是我定死了的这个选项里面只有department of music。

![](img/9b149dd1c4929e33a4fe6be702c58f02_17.png)

呃，只有这个音乐学院，这是定死了的。但他这个学校里面的老师的名字啊，他可以改，对吧？这这这个名字至少他可以是老师，可以是配成么别的名字，你看你的印样你。

或者或者叫set of set principle。

![](img/9b149dd1c4929e33a4fe6be702c58f02_19.png)

我怎么这么搞，可能你会好理解s的。principal校长的名字，对吧？Priinciipple。Name。



![](img/9b149dd1c4929e33a4fe6be702c58f02_21.png)

这样，那我如果那这样子讲法，不就是school set principal，对吧？呃，叫什么呢？

![](img/9b149dd1c4929e33a4fe6be702c58f02_23.png)

A long。这个学校是al的，哎，这边要运行一下。

![](img/9b149dd1c4929e33a4fe6be702c58f02_25.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_26.png)

他就会报错。8。

![](img/9b149dd1c4929e33a4fe6be702c58f02_28.png)

啊，这边是我要重新初始化一下。重新初始化，那school现在就是我现在重新run一下，那s school现在是清空了的，它是没有这个name的东西了。



![](img/9b149dd1c4929e33a4fe6be702c58f02_30.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_31.png)

嗯。

![](img/9b149dd1c4929e33a4fe6be702c58f02_33.png)

对吧然后我再重新运行一下这这刚才这几个东西，al斯王 setet principle这样就给它s进去了。



![](img/9b149dd1c4929e33a4fe6be702c58f02_35.png)

嗯。Said principle， principle。对吧他的pri他的校长名字就是Elon mask，那或者这可能是这可以是两个老师啊嗯。小明李对吧？School name。对吧。

就比如说这这样这样 makesake sense一点啊，这这样大家就理解一点嘛，这边叫老师名字，学校地点，然后校长对吧？校长是allon Muk在上海，他有alice王和小明李小明两个老师。

所以这个是什么意思呢？这个class啊，他就是一个。

![](img/9b149dd1c4929e33a4fe6be702c58f02_37.png)

嗯，一个模板对吧？我我给这个人或者这个学校，他有一个定义，他有department music dement。music或者是art，对吧？那那我如果现在找。



![](img/9b149dd1c4929e33a4fe6be702c58f02_39.png)

Department。那是不是就是哎啊我要重新初始化，你在这里改啊，你光在这里改是没用的，你要把它重新初始化，然后再把它塞的进去，对吧？所以是。



![](img/9b149dd1c4929e33a4fe6be702c58f02_41.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_42.png)

不要忘了，千万不要像我一样的，把它忘了啊，你要重新把它初始化一下，这这是这是school一了，那我给他school二呢，对吧？😊。



![](img/9b149dd1c4929e33a4fe6be702c58f02_44.png)

我重新去重新干一个学校上学，就是这是另一所学校嘛。那这个学校的老师就不一样了，叫做。Christine。Christine。呃。Justing。L一嗯。George。嗯。乔治。Mask。随便随便输一下。

然后。再来啊location locationation北京。然后我们再来他的校长名字叫。

![](img/9b149dd1c4929e33a4fe6be702c58f02_46.png)

先等下，要不窗。Trump。

![](img/9b149dd1c4929e33a4fe6be702c58f02_48.png)

对吧。呃，那我们来看一下。它的这个首先它是不能变的东西department。

![](img/9b149dd1c4929e33a4fe6be702c58f02_50.png)

department还是musing art，因为我在这面没s嘛，但是可以变了的是什么呢？变了的是不是我们的name名啊？



![](img/9b149dd1c4929e33a4fe6be702c58f02_52.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_53.png)

对吧Chrisristine李和。哎，不对。

![](img/9b149dd1c4929e33a4fe6be702c58f02_55.png)

这边是2，你要要用2。我这边都用的是一，所以是他这边不对了，我重新把它跑一遍。

![](img/9b149dd1c4929e33a4fe6be702c58f02_57.png)

你看school2是christinlygeorge muk，然后school一呢对吧？school一仍然还是。



![](img/9b149dd1c4929e33a4fe6be702c58f02_59.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_60.png)

alice王和小李小明对吧？这什么意思呢？这个意思就是。

![](img/9b149dd1c4929e33a4fe6be702c58f02_62.png)

这个类啊它是相当于一个人的模板。比如说我定义一个人，他可以是小李、小张小明，他们都有不同的属性。

![](img/9b149dd1c4929e33a4fe6be702c58f02_64.png)

小明喜欢上数学，小王喜欢上语文，或者是像这里这个学校，我学校有不同的有一样的department，因为这是定死的。但是学校的。老师名字老师们和学校地点，还有校长的名字，他都不一样。这呃为什么这么做呢？

首先呢他就跟那个sname他跟那种呃函数就我们之前讲的像这个单独一个函数啊，相比于他来说呢，我们可以能就是有更加多变的一种情况给他做一些定义啊，做一些更复杂的运算啊，如果只用一个函数呢。

它可能还就是在某些情况下还不适用这种情况，咱你暂时没碰到过，就是比如说我像像之前我看一下我啊之前daytime，就它下面有不同的方法嘛，对吧？都都压在这一个daytime这个包里面。

然后这个daytime包又是在这个就是在这里面的，所以一层一层套一层的不同的方法，你程序复杂了以后呢，光用一个函数啊，啊，你可能就就比如说我我有这么多运算方法呢，我总不能一个一个一个inport。



![](img/9b149dd1c4929e33a4fe6be702c58f02_66.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_67.png)

![](img/9b149dd1c4929e33a4fe6be702c58f02_68.png)

对吧我要把它压在一个类里面，所以我可以直接压在一个类里面，我inport一下，然后再调用每一个方法，每一个这个。



![](img/9b149dd1c4929e33a4fe6be702c58f02_70.png)

每个函数。这样的话就方便很多，尤其是在那种就是在你你坐到后面，嗯，你你你程序变得非常复杂了，会用到这种方法。



![](img/9b149dd1c4929e33a4fe6be702c58f02_72.png)