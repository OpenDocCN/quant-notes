# 第2节课 EventEngine2 - P1 - 古辰诗提 - BV1hA4m1A7tV

![](img/f60ec97a50afbe564bf6e4fa16b8e093_0.png)

欢迎大家来到从零开始量化系列课程，VMPI课程的第二节课，上一节课咱们讲到了这个注册。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_2.png)

一个很简便的写法，但是大家一定要知道。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_4.png)

他是一个就是什么个情况啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_6.png)

呃咱们注册完了之后，你去往里边去放数据。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_8.png)

数据放了之后去获取，当然这个获取是一开始，从这个start里边就就不断的去获取，它是一个循环嘛，啊当然在size里边。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_10.png)

咱们漏写了一个C点active等true是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_12.png)

TRUE就是我得我得让它先为true，然后他才能启动这个线程啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_14.png)

它才能作为一个循环去不断的去执行这个代码，呃你现在也把方法也注册进去了。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_16.png)

那后边就是如何去分发了对吧，咱们上节课就给大家写过，这个这个里边存放类型是，比如说我这个是tick啊，就是类型的数据，然后呢这个冒号这个列表里边是什么方式，一方式二啊等等等。

我要做的是当我有一个这个数据来了之后。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_18.png)

我这个function需要挨个的去调用对吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_20.png)

这个其实很容易去实现，有一些Python基础的就非常容易去写了，就是我在process data这嗯。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_22.png)

我LT等于cf点FUNCW。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_24.png)

然后这个key就是key，就是invent type嘛对吧，放李白，然后如果说这个如果说我这里边只存放了这些，那如果说我这个type是order的话，那他会给一个空的列表，这个时候你进行一下判断。

If l s t，然后这个列表里面就可以进行遍历了对吧，我FNC0这个LST啊，然后FUNC括号把这个给他放进去，就是当这个方法作为一个对象的时候，你不能加括号，它其实就是一个内存地址是吧。

这是Python基数里边的，然后你用括号进行调用的时候，它就可以直接执行这个方法里边的，这个函数了啊，他是这么一个逻辑，你直接进行调用，但是呢从这儿呢有个问题，就是你这LST如果是个空的话。

你留着也没有什么意义是吧，所以说你需要一个else，如果它是空的的话，那就是if f l o s t，然后else如果它是空的话，我cf点FUNCW点pop，我把它给删掉啊。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_26.png)

就是这个这个invent点tab。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_28.png)

我把它给删掉，这样就比较简洁了，对不对啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_30.png)

但是呢源码里面不是源码里面是这么来写的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_32.png)

这个呢需要给大家演示一下啊，就是demo02点PY。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_34.png)

咱们以前在生成一个列表的时候，是一般情况下是怎么来做，比如说for i in range，比如说100就是，然后啊我先定义一个LST，它是一个列表，然后LST点append这个是吧，这个列表就有了吧。

print a s t啊，这是最基础最基础的内容了。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_36.png)

就有了，但是呢咱们后来又学了一个叫列表生成式，列表生成式是什么呢，就是我不需要这么复杂了，变量i for i in range，100对吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_38.png)

这个我LS我print一个LST就可以了吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_40.png)

就可以了吧是吧，那这个我原本有这个列表了，那如果说我列表里边LST等于等于什么呢，就是比如说我LST1等于一个IFIE，L s t，然后呢我这个I我做一个什么呢，I加一。

那我print我在print这个LST，我不是print l s t一样啊，我print l s t啊，咱们看一下它它是没有加的吧，但是LST1它是它是加上了吧是吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_42.png)

最多是到100，这是到99，对不对，那如果说我直接从这加一个print，你看一下啊，我这个时候再print一个LST1，你看一下啊，我先不print l s t e，我先我先这样。

因为他会自己去print，是从1~100，对不对，那我如果说我print一个LST，你会发现看着啊这个LSTE里边全是N值吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_44.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_45.png)

对不对，那我如果说我直接这样一个列表的话，我是不是就实现了，比如说我print我执行了这个里边这个函数了，但是呢我这个列表就是我本身的这个LST，它又没动啊，啊我本身的这个LST它又没动。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_47.png)

对吧好，咱们运行一下啊，我先把它给注释掉，你会发现它执行了里边这个方法了，都加一了，但是呢我本身的这个LT它没有动，对不对，所以说既然这个列表生成式是，里边可以直接执行代码。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_49.png)

那我这个它本身也是一个列表，对不对，那我是不是可以直接把它。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_51.png)

a t y p d in cf点FW啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_53.png)

如果说他在字典里边有这个key值的话，好我用个列表的这个生成式，然后我直接去执行，我首先第一个是function，然后把这个给他放进去吧，EVENT是吧，然后我这个funk它是一个就是变量是吧。

f u NC in这个cf点，F u n c w，然后这个括号里面写上这个invent点，对吧我不就执行一遍了吗。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_55.png)

同时呢我这个列表里边是不会有任何变化的啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_57.png)

这个就是源码里边他是这么来写的啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_59.png)

只不过他有两个啊，两个为为什么会有两个，咱们后面再讲。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_61.png)

你看源码里边它是怎么来写的是吧，所以说不要觉得陌生啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_63.png)

其实在基础里边咱们都学过啊，其实到这儿呢你会发现其实这样一个就是呃。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_65.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_66.png)

invent engine已经写完了，就已经写完了啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_68.png)

只不过这它有一个是这个是一啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_70.png)

这个soft interval它是用在哪的呢。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_72.png)

interval是在这wrong time，这啊这个咱们一会再说。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_74.png)

其实这时就是一个简单的这个image engine了，比如说咱们做一个演示啊，把它给注释掉好，我给他导入一下from这个咱们自己的这个event engine。

Import my invent engine，好，咱们进行一下演示呃，我先创建一个invent等于int engine，ENGIE等于MN哎，My int engine。

然后括号里面不需要填任何东西啊，然后我写一个循环，For i in range，比如100，然后往里边去放这个数字啊，就是但是你得包装一下对吧，所以说咱们也得把这个event给导入进来，然后event。

哎invent等于invent，这里边放tap，tap呢我写上，比如说number number，然后data我写上就是这个I，然后往里放，我放一次呢，我先0。5秒啊，From time。

sleep歇一次呢，我歇五秒，Sleep 1。1p sleep0。5，这个是可以的吧，我把它定义成一个方法行不行，比如说呃number put put，好然后这样，啊这个我还没给它放进去啊。

这个invent engine点put这个event好吧，这是往里放好，放了之后我得有方法去处理啊是吧，这个处理呢我就直接是out不吃吧，output output里面event event。

然后我接收过来，我这个方法我就直接写一个print了啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_76.png)

接收到数据括号。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_78.png)

然后第2format，然后这边写上这个点。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_80.png)

这个data是吧，这个我就模拟方法，这个呢我就模拟往里边去放这个内容啊，当然你放内容，你既然这么去放了，而且它取有可能是同步的，有可能是就是两个会就是就这个往里放，它会不断的去执行嘛。

我往外去取的时候也是一个线程是吧，所以说我最好这我担另一个线程啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_82.png)

from threading import thread啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_84.png)

然后我这写一个thread等于对。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_86.png)

然后这个target等于那个number put板。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_88.png)

这个因为不是累啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_90.png)

我得写到这number put，好然后呢，我从这儿写一个if，好我这个invent engine，我先这个把它给启动起来是吧，Invent engine start，然后启动完了之后。

我就该呃就是先往里注册事件，是不是，然后这就是invent engine register。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_92.png)

这type应该是什么呀，number是吧，所以说我可以从这定义一个就是number常量等于number，是不是就可以了啊，如果说你按照咱们这个就是被那里面写的。

就是event什么什么什么event什么什么好，我这就可以写成event number是吧，然后我注册的时候，我就可以用这个limit number，然后把我的这个output给它注册进去，是不是。

然后这个我先给他注册，然后再启动吧，好在启动啊，就是invincil engines启动起来，然后再启动什么呀，就是这个three就是three的t h AD three点start是吧，给启动起来。

按说你按照这个逻辑来说的话，你应该是不断的去输出，这个123456789十，一直到100，对不对，好，咱们去运行一下啊，接收到数据了吧，0123456789十是吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_94.png)

这个时候你只要有方法啊，你就可以直接把它给注册进去就可以。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_96.png)

然后它就会给你自动的实现分发。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_98.png)

对不对，但是啊这是需要注意的，把它给先给关掉。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_100.png)

注意什么呢，就是你在注册的时候，你启动起来，你再给他注册也是没有问题的，比如说我再写一个方法，Df output to，就是MIT limit啊，然后我这写上print。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_102.png)

就是FUNC2接收到数据。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_104.png)

然后这个点format，然后这里边写上这个点data啊，就是我启动起来了，已经整个都全启动起来了，我这个时候下划线engine点register，比如说我这个还是limit number。

然后这个是out put o u t output to。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_106.png)

啊咱们这个时候再运行下，你看就是他已经都启动起来。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_108.png)

你再注册是可以的啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_110.png)

你再注册是可以的，但是如果说我中间我把这个什么呀，就是output2，我给撤掉了，他会报错的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_112.png)

当然在这演示不好演示啊，就是我注册进去之后。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_114.png)

这个functions啊，就是这个function突然有一个function它没了。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_116.png)

因为咱们在真正使用的时候不会这样，很直白的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_118.png)

它会比如说我给他传到一个类里边，如果这个类没有了，比如说咱们就是啊写的那个数据啊，写的这个策略，你到了下午三点多收盘之后，你先把策略给注销掉了，或者你先把这个某个东西给注给注销掉了。

你半途你没给它给取出来的话，给它给注释掉的话，它会报错的啊，它会报错的，所以呢你必须得有个取消的这么一个机制。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_120.png)

第六个取消的机制，用咱们这个engine里边话来说，就是on register。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_122.png)

那这个其实也很容易理解是吧，我UNREGISTER怎么来写。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_124.png)

既然有注册，那我就得把它给取消注册，同样的cf点啊，这个是type什么t r f u NC call。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_126.png)

我取消注册，同样的u s t list等于C点，f u NC type是if f f u NC in u s t在里边。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_128.png)

如果说在里边的话，我LST点我应该是什么呀。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_130.png)

remove吧，我把它给删除掉是吧，我把这个value给删除掉，就是这个function给删除掉，后边呢你还需要判断一下，If not，如果说没有这个这个列表就为空了，就删除之后这个列表就为空了。

我就需要cf点FUNC这点pop是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_132.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_133.png)

把这个key pop掉，就是tap。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_135.png)

这样就可以了是吧，同样的源码里边也是有这个UNREGISTER。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_137.png)

你看它就是remove是吧，Remove，但是他这没有写这个什么，就是把那个空的这个列表给它给删掉。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_139.png)

都是一样的意思啊，都是一样的意思。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_141.png)

就是当然你不删也行好吧，就是说这是这是注册，这是取消注册，如果说你这个image engine在运行的时候，你的这个类丢失了，或者你的这个方法丢失了，它会报错的，所以说比如说我有个程序，我这个程序呢。

就是说这个invent engine一直在运行着，比如我自己写了一个我一直在运行着，但是呢你像这个tick数据实时数据的接收，它中间会有这个柜台断开链接对吧，会有都会有这个柜台就断开链接。

柜台断开链接之后，你那些策略呀需要接收到这个呃这个音，这个提个数据的呀，你是不是就应该把它给注释掉，就是给从这儿给取消注册，你不然的话你断开链接了，然后你需要把那些呃数据保存之后啊。

你就把那些就是你已经实例化好的，那些类给取消掉，你取消掉，如果说你不给他就是取消注册的话，它会报错，当然更多的时候你是结合界面来写的时候，可能会遇到这样的问题啊。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_143.png)

这就是UNREGISTER啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_145.png)

如果说有另外的需求，比如说这个里边写了两个。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_147.png)

就是还有一个就是self general handles，这是什么意思呢。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_149.png)

其实就是什么呀，如果说我不分类别，就是我不分这个我是tick还是order，我都要我都要在一个方法里边进行处理，这时候呢你就可以写一个什么呢，就是说啊CFD2FUNC啊。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_151.png)

我就是general是吧，GENA啊，就这么简单写吧，等于我这个就不需要我这个default这个dict了，我就直接一个列表对吧，然后呢我在register的时候，我出我。

我在注册的时候就DFIGIGSTERG，general的时候啊，它是代码是一样的是吧，type s t r嗯，就是这个FNCCOLLAB，然后我就是注册的时候啊，if for time啊。

我这就不需要type了，因为我都注册进去，我只需要一个FUNC就行了，对吧啊，If f u n c not in self。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_153.png)

这个FUNCSJO，然后cf点f u NC general，点pend，然后这个换是吧，同样的，我在取消注册的时候。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_155.png)

我就是u NC in list，list等于type in list，然后watch就是pop a啊，就是我重新写一个UNREGISTI，G i s t e r ja c f f n c collib。

然后if f u NC in这个cf点f u NC general，然后FUNC啊，cf点FUNCJ到点还是remove吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_157.png)

然后这个value f u NC就可以了吧对吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_159.png)

然后我在处理的时候就是process这个data的时候。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_161.png)

是不是可以把它删了啊，同样的以这种方法就是来来进行处理吧，就是同样的我写个列表啊，就是当然我也可以就做一下判断啊，一副cf点FUNC，见到就是他这个里边不是空的啊，同样的一个列表，然后FUNC嗯。

invent for function fn c in cfa呃，这个f u NC general，这样不就可以了吗对吧，因为它是个列表吗。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_163.png)

啊是吧，这个就是我所有的事情我都需要接收过来。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_165.png)

然后进行处理，这个一般用在什么呀，就是咱们之前提到过的这个CP，就是我从一个接口就是统一的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_167.png)

就比如说我服务端，我服务端连接着这个服务器行情啊，包括数据库啊都在里边，然后我客户端比如说我租了一个服务器，然后上面写着代码，然后我客户端我在使用的时候呢，为了给多个客户端就进行的进行使用。

然后我可以去接这个服务器啊，那你接的时候，你就需要把所有的东西都全接过来，tick也好，order也好啊是吧，全部接过来，这个时候就可以。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_169.png)

register这个general就是整个的给注册进来，这个咱们engine里边也是一样的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_171.png)

你看它是一个list啊，你在process的时候它也是一样判断啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_173.png)

都是一样的，然后on register是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_175.png)

on register general一样的意思好，还有一个需求。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_177.png)

什么需求呢，就是咱们也应该看见了啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_179.png)

就是这个timer timer是干嘛的，就是在咱们这个呃就是底层接口里面。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_181.png)

肯定是有主动去申请的一些东西，就是你主动的去申请一些东西，比如说你的这个position就是持仓信息，它不可能就是说你可能连上服务器的时候，就是他会给你发一遍你的持仓，但是中间如果说你的持仓有变化了。

他只会给你发那个try的信息，获得order信息，他position这个信息他可能给你发，但是呢如果说你想获取的话，实时获取的话，你得主动去获取对吧，你得主动去获取。

包括你的这个account data，Account data，它是实时根据这个行情的变化，它是变化着的，就是我这个账户里边我活动盈余啊什么的是吧，是有变化着的，一般咱们看这个平台软件的时候。

看的都是它这个数字一直在动，那如果说你想获取账户信息，应该你应该去主动的去申请去获取，然后他服务器给你响应，再给你就是返回来，而且这俩东西啊，就是一个账户信息，一个是持仓信，尤其是持仓信息。

你得过一会儿你就得更新一下，过一会儿就得更新一下，你要账户信息，你你要是更新的频率快的话，它才能不断的去进行变化，对吧啊，所以说你需要主动去申请一些东西，主动去申请一些东西的时候呢。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_183.png)

你就需要一个计时器啊，这个计时器呢其实就放一个就是event。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_185.png)

这个event里边含的内容呢就是timer。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_187.png)

Timer，它是个什么东西呢。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_189.png)

它其实就是一个咱们可以啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_191.png)

这个。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_193.png)

咱们从这儿看一下啊，它这个invent timer。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_195.png)

导入一下就是。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_197.png)

这个VMPY点trade t点M。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_199.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_200.png)

这同样是在这个，因为timer它其实就是个标记，1TEER他也是个常量啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_202.png)

你需要给他放这个event。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_204.png)

这个timer，然后告诉这个程序，然后你该去获取账户信息和持仓信息了啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_206.png)

这个是他的作用写其实也很简单啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_208.png)

就是sector timer t i m e r timer thread，它也是个线程是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_210.png)

thie sweet target等于四点timer timer put好。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_212.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_213.png)

我定义一个d f t i m e temp，然后SELF，然后。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_215.png)

就是while这个self active。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_217.png)

就是我在就是运行着的时候。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_219.png)

然后这个cf点，put一个event，这个event是什么呢，就是把这个EVENT等于invent。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_221.png)

然后这个timer t i m e invent啊，就是invent，这样就是1TAETEER，这里边放一个NN值，我把它放到这个。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_223.png)

就是这个咱们的这个队列里边去啊，但是你不能一直放啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_225.png)

就是这个会一会就给你放很多，你可以放一次，我sleep一个，比如说一秒钟我每隔一秒放一回。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_227.png)

或者说我每隔三秒放一回是吧对吧，这不来421品。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_229.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_230.png)

啊这。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_232.png)

From time import sleep，我每隔三秒翻译回那这个数字。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_234.png)

我是不是可以给它定义一个变量cf点啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_236.png)

这个i n t e r v l interval是吧，这边我就可以写一个cf点。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_238.png)

INTERVAL等于RINTERVAL，我传入的时候INTERVAL是吧，我给的int，然后默认等于。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_240.png)

比如说等于一是吧，这个interval不就有了吗，就是在咱们这个这个哎呀那个invent engine又没了。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_242.png)

找一下这个unit engine啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_244.png)

啊它这个served interval不就是这个意思吗。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_246.png)

就是你放到这个，就是你隔一段时间往里放一个时间，隔隔一段时间往里放一个事件是吧，然后提醒就这个需要用到这个计时器的。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_248.png)

去做一些事情啊，他写的有点不太一样啊，这边他没有NN。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_250.png)

那是因为什么呀，他在这个data它默认了一个NN值好吧，这个时候我就可以把这个NN给取消掉了。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_252.png)

直接这个同时呢我可以从这定义一个MTI。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_254.png)

tom等于e t i m e r e timer是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_256.png)

然后我把这个就是这个e timer改成limit time。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_258.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_259.png)

这个不就可以了吗，当然我得启动它是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_261.png)

Tempt tempt，然后我start的时候，然后就是self time，四点time three的点SP，然后我stop的时候就是sp time，time three的点，Join。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_263.png)

对吧，这就可以了吗啊当然这个可以往里缩进两个啊，这样啊就是我在它启动的时候。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_265.png)

我才进行就是呃关闭的这么一个操作。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_267.png)

然后就是启动啊，就是这个就是一个invent engine。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_269.png)

虽然代码不复杂，但是它很重要。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_271.png)

你一定要理解清楚了，而且他也是有注意事项的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_273.png)

就是你在就是。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_275.png)

就是当你这个image engine并不停止的时候啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_277.png)

因为在engine并不停止的时候，你的一些需要停止的东西。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_279.png)

你停止之前你要on register，一定要记住这个on register啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_281.png)

另外呢这个engine呢其实是可以进行，你自己进行一些变化，你在写一些代码的时候啊，你有可能会碰见什么呀。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_283.png)

比如说这个队列，比如说我数据存储的时候，我数据存储的时候，我排着很多的数据，比如说8data，可能我全市场全行情，那我去录制行情啊，我去录制了，就是说这个数据，然后呢我这个就是队列里面存放了很多的。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_285.png)

就是它会有很多的这个数据堆积着，因为我往里存的时候是需要时间的。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_287.png)

你慢慢的数据就会堆积起来，那你再去发送。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_289.png)

比如说我要实时获取，现在是个什么情况，我需要输出日志对吧，你日志在咱们VNPY里边，它也是放到这个这个这个里边的，就是cf点Q这一个里边的啊，一个队列里边的，如果说你想把它拆开来，你可能就是说。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_291.png)

前面堆着一堆数据呢，这个时候呢你往里放了一个日志message是吧，就是你放到这个里边了，你只有等到前面的这些数据全部存放完了，你才会把这个日志输出出来，是不是这个日志就输出的迟了呀，对不对。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_293.png)

所以说你可以单另一个Q就是cf点，比如QUE就是专门的log。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_295.png)

等于一个QU1U1啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_297.png)

然后我在存储的时候，就是说如果说是是日志信息。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_299.png)

比如说我从这定义一个mt log等于一。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_301.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_302.png)

我如果说我注册的，比如我往里放的啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_304.png)

这个invent，如果说if event type等于A，event type等于这个invent log是吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_306.png)

如果是等于它，那我cf点q u e log put这个invent啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_308.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_309.png)

然后else，然后我再给它放到这个队列里面来对吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_311.png)

然后我就是注册的时候，注册的时候你还要加以区分，if这个type等于这个event log，我就可以把它单独的。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_313.png)

比如说我self。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_315.png)

FX log等于一个列表，我单独的给它放到一个列表里面去，就是，从这and f u NC not in c点成log。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_317.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_318.png)

然后C点换成log，叫a panda func是吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_320.png)

如果说你是这个event log的话，如果说你不是event log else，诶，你再这么来操作，当然最好是把这个单独来写啊。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_322.png)

就是这个给它剪切一下，对啊，那个嗯冒号这样，这样的话他和ELS有一个只执行一个嘛，你如果加一个这个条件，如果说他在里边了，他会不会给他添加到，就是这个你就是CD就是FX这个W里面去是吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_324.png)

同样的我on register，就是比JJENNER里边也可以写上。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_326.png)

当然我这里JJENNER我就不写了啊，我on register，你同样可以判断一个就是这个type是吧，Type，等于等于invent log。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_328.png)

如果它是等于invent log的，if这个，f u NC in这个cf点f u NC log。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_330.png)

就是cf点f u NC log点remove，然后这个FUNC对吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_332.png)

然后else这边加个else，是不是就可以这样来写了是吧，或者直接不加ELS，就是你写到这儿的时候就可以直接去称了是吧。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_334.png)

就是我下面就不执行了，如果说他是unity log的话，他不管在不在这里边啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_336.png)

我就执行完了，我就不蹭就可以了，对吧啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_338.png)

同样的就是说这个get你需要就是try对，就是比如说我再写一个DEFGLOG，然后self这样就是YSACTIVE，然后try，然后invent啊，我这可以写上MIT log等于四点q log点git。

然后event log直接给它放进去。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_340.png)

然后我这再建一个线程是吧，sales调log three等于四位的t h r e d sweet。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_342.png)

![](img/f60ec97a50afbe564bf6e4fa16b8e093_343.png)

然后target等于C调，那就是GLOG对吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_345.png)

这个你就可以把信息。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_347.png)

就是你的这个日志信息，和你其他的一些数据信息给拆分开。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_349.png)

同样的，如果说你想就是把tick，因为tick数据比较，就是可能如你全市场全行情去录制的时候，tick数据会比较多呃，我想把这个tick数据单拎开来，你也可以再写一个单独的TK线程。

就是去单独的去进行tick的分法啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_351.png)

这都是可以的，这个模块是可以进行改造的，而且它你改造完了之后。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_353.png)

你其他的代码是不需要动的，这都是给你，就是说全部就是按照原来的这个，给你签到好了的对吧。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_355.png)

从这儿呢，最后还要给大家提醒一点是什么呢，这个只是在一个进程里边去使用的，一定要记住是在一个进程里边，因为这个QEUE它其实是县城里面的。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_357.png)

它的这个队列，就是如果说我这个是我开启了一个进程，就是process这个里边的这个Q啊是可以通用的，Q u e u e，然后你这里边不管开多少线程，都是可以跟这个数据是可以通用的，如果说有老板们想。

比如说我去录制航行，我开一个进程，然后我这边交易，我开个进程，记住了，这个QEUE是不能进行通用的啊，不能进行，同样你不要以为我创建一个QEUE，我这边就能从这去获取数据，不行的啊，这个QUQUE。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_359.png)

只能是在一个县城里边进行使用，如果说你想多个进程里边吧，只能是在一个进程里面进行使用，如果说你想在多个进程里面进行使用的话。



![](img/f60ec97a50afbe564bf6e4fa16b8e093_361.png)

from这个processing multiprocessing import。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_363.png)

Q u e u e，啊这个才是进程里面使用的QEUE。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_365.png)

但是啊如果说你想开多个进程，而使用一个数据来进行链接的话，或者一个gateway这个数据的话，建议你使用这个这个这个，这个就是咱们的这个这个这个这个IPC模块，而不是说我创建了几个进程，怎么怎么样啊。

就是这个是提醒的，一个是在一个进程。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_367.png)

一定是在一个进程里边进行去使用，好吧好。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_369.png)

那这个event咱们就讲到这，MIT必须得熟练掌握，必须得有一个充分的了解啊，这个是整个这个VNPY里边的一个驱动器，非常的重要，在咱们别的课里边儿也反复讲过这个，但是很多人就是用的不太熟悉。

这一块是很重要的啊。

![](img/f60ec97a50afbe564bf6e4fa16b8e093_371.png)