# 【量化交易】Python入门之数据分析【1／4】｜ 金融工程 量化金融 - P6：1. Python数据分析：Module1-函数-Functions1 - Devils-Advocate - BV1efHAe2EAR

大家好，欢迎来到我们第一节课。那在开始讲课之前呢，我先带大家来认识一下pyy charm，左边这是我们的文件，右边这是我们的操作界面。那么在文件里给大家可以看到。

我把它安排在一盘pyython project work下面之前的一堂课我带大家创建了一个这个pyython project。如果大家还不清楚，可以回看一下。那么我们有两种pyython file。

一种是jupyter notebook，然后可以看到它的后缀是ippython notebook啊，第二种是到PY这两种file呢，这两种文件。都是可以运行排ython程序的。

只是notebook呢它比较方便教学，可以看到我这边有比较呃方便查看的一个mark等，就是我这些解释说明啊，然后所有的所有的回答，所有的答案都能留在它这个界面上。比如说在这里。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_1.png)

呃，可以看到它的答案是在这儿的那我如果在这里执行呢，其实结果是一样的，只是。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_3.png)

![](img/dfafbddcd82dbd439f37451d2d11f4bd_4.png)

我在这边run file in python console。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_6.png)

那么这里就会跳到这里。比如说我ro this line。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_8.png)

excuse selling in python console。那么就可以看到我这里也是给它进行了运算。所以呢这两种都是可以的。jupyion notebook你只需要看界面就行了。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_10.png)

![](img/dfafbddcd82dbd439f37451d2d11f4bd_11.png)

的 pie就是可以看到我们的pyython console。那除了pyython console，这还有一些其他的一呃功能。比如说。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_13.png)

这边terminal terminal就是我们之前如果大呃大家没有安装。那个pandas或者是。呃，n派我们会在这里安装peep installst non派。那么这里我已经inst过了。

paep installst pandas它是直接跟系统相连。所以这边这边的。呃，terminal除了你安装package的时候，呃，其他时候并不会用来操作。

然后还有我们的version controll，这是跟gitthub相连problems，这是会检测你。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_15.png)

代码里面是否有一些问题，他会给你报错。比比如说像呃这些，他会告诉你statement haveve no effect在我的第五行业，就是这个，因为我没给它复制，所以他说这个有问题。

也是挺正常的services啊，这些你暂时不需要管，还有packs，就是package是我们已经install的一些package，啊，或者我们可以从别的呃别的version，别的。地方别的盘里面加载。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_17.png)

然后呢，是我们的conl，可以看到这个pyython的标志，这边我们可以直接操作，也可以在从上面运行。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_19.png)

这边rom这边没有东西，juter是我们的记事本的后台。那么大家也可以不要动它，除非你想关掉这个记事本，我们可以点一下stop driftter server。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_21.png)

呃，那就是。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_23.png)

那这是排唱的一些界面。那么我们现在进入到这个排查来看一下代码。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_25.png)

首先我要讲一下函数，那么从函数开始呢，可能会比较难。但是我觉得它是一个。嗯，怎么说呢？它是展示pyython它一个功能强大的一个基本的一个方式。所以我觉得从这儿开始会比较有趣。那么什么叫函数呢？

也就是这个functions，那functions可以它可以。define一些复杂的运算，然后把它封装起来，用于反复操作。就比如说呃我这里这边首先我讲一下它的结构，define它以DEF开头。

这是它的name这个name。比如说我现在写的operation one，这可以随意呃，我只需要在后面调用它。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_27.png)

比如说这里。我给它复制到A上面。然后X和Y呢，我分别给他们复制X等于1。Y等于2。那么在这里X和Y就会。就会被引用到这，然后呢，进而在这个已经封装好的函数里进行运算，给到我们的answer。

最后我们return回来，就是这是一个return是返回的意思，返回一个值。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_29.png)

那么我们可以看一下。我们首先要 defineine它。我可以看一下它pre A就得到了3。那这是具体是怎么来的呢？这这个X和Y和这个X和Y是否有关系呢？那其实我可以给它AB。

那大家可以看到这边XY打了小红线，那么我们把它给成AB也行。照样能出来3。或者是22。应该出来是4，对吧？那么这个这个为什么和这个XY不一样？那其实我们封装到一个方里面的东西啊，它只存在于这个这个函数。

就是它跟外界它的命名可以是就是不相通的。就比如说我这里的X和Y。如果我这边是乘X和Y。那么跟这里其实是不相连接的。那在外面相连接的地方，就是我们可以看到这其实是外外面这一层。

我把这个X和Y这两个值给到它。这两个定义的一个。啊，一个parameter，一个参数这里，然后它才传到的传递到onswer。那么如不管是这个是如何命名，比如说CD我只要在我只能在这里引用它。

你看如果我这边不引用CD的话，它这边就是按下来了。所以这边我们引用一下C和D，那就相当于把这里的参数传递过来。那这也是一个。嗯，你可以讲它是占位，我只是拿一个东西占着它的位置。然后后期我把这两个。

这两个。参数的值传过来，那我可以还可以干什么呢？我们也可以直接。呃，写数字而不给他。一个具体的值。那么这里我们得到是4或者是。3四得到是7，那这也是一个站位的一个思想，就是三给到C4给到D。

那么这里会进行引用。那如果是。56。一样的那这只代表一个站位。如果你用不管你这里填的是已经赋值了的XY还是AB还是CD或者是一长串，比如说。XYZ等于11。FGH等于12。因为我把11赋值给了XYYZ。

然后12赋值给了FGH那么这里的。11就是被我带到了这儿，因为XYZ相当于等于11了，FGH相当于等于12了，他们就实取代了C和D。然后会对，然后继而他会拿到这个数，他就把它当成C，拿到这个数。

他就会把它当成D，然后我们进行预算。嗯，那这大概是一个函数的结构。那为什么我这边只做了加法，为什么说它。呃，可以减少计算的重复量呢，就是你可以使代码简洁。

你这里比如说我有一个更复杂的operation to，那么X和Y进行了各种复杂的运算。呃，所以我每次可以调用它，就比如说我有很在在不同地方有不同的数学公式嘛，那可能都会用到这一个部分。

比如说23这个19。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_31.png)

然后继续把它复制给A。我把这个复制给B。99。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_33.png)

100。那么这边我们已经算完了，都是一套一样的运算方案。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_35.png)

我们可以看一下我们的A的值。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_37.png)

然后可以看一下我们B的值。那所以不管你怎么，就是你每次进行这个运算，都不需要再手打一遍这个操作，不然我们应该怎么办啊？不然我们是不是要每次都要比如说A。哎，刚才A是多少？23和19。

那我们每次是不是都要这样23。19。然后这边answer还乘了一个3乘以3。这边是不是要打个中括号？我们打我们这跟数学运算不一样哈，我们这边不能打中括号，正括号是另外一种东西，我们只能打原括号。

我现在就不算B了。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_39.png)

那A还是这，对吧？那我们。是不是B也得这样子计算呢？如果没有function的话，没有这个函数的话，那么这个这个我也不记得是多少了。Y应该是在这儿。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_41.png)

然后这个要复制个B，对吧？我们每次算任何东西都需要都需要改改这么多这么多次。然后每一次里面都需要做IXY就是互相调整。那如果我有了这一套复杂的这个机制，我给保存下来。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_43.png)

![](img/dfafbddcd82dbd439f37451d2d11f4bd_44.png)

那我是不是每次就是operations to这样子来，直接直接改就行了，120210。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_46.png)

30。然后这个参数有人问可以呃，是只有两个吗？还是可以更多，这可以无限多。嗯，但是但是他们名字不能一样ABC对吧？这边可以比如说加A加B加C。这样的话我们就可以，只要我们在上面有的。

我们都可以在后面进行调用。但是可不可以两个都一样呢？那这其实是不合适的。因为你既然是一样，你为什么要。都放在上面了，所以这这不能出现一样的命密。可不可以是其他的，比如说中文。嗯。你好。那也是可以的。

加上你好。这个任何名字都只是一个占位，它可以是多个多个字母组成的单词。Hello。他也可以是。单个的就是单个的字母。比如说我可能就是我可能有些复杂的命名啊，比如说。嗯。Cold shares。

如果你碰到股票方面的东西，对吧？那可能我这边要调用一下股票的code。要对它做下，否也不能说是运算吧。shares呢我们确实可以就是进行运算。比如说这这只股票有5万股。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_48.png)

对吧他的price。等于多少？

![](img/dfafbddcd82dbd439f37451d2d11f4bd_50.png)

它的pri我就把code删掉吧，priice等于。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_52.png)

20。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_54.png)

那我们的。市值是多少？86等于20乘以5万。那我们就不用。20乘以5万了，因为它每次都不一样，price乘以share。然后我们返回的值是value。那这里呢我只需要提供。每个股票它的价格。

那这里我我是把它的。这个价值已经定义了嘛，那其实不要这么干，那我们出来。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_56.png)

Price。和挽留。我们这边用operation two。然后把pri放进去。Shares放在这儿。然后我可能会有不同的股票嘛。Stock a。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_58.png)

我们打印一下。Print。stock a那这里我最好还是把它share aA。股票A它的。价值和 shares。对吧那我可以同理，我可以做股票股票B。那甚至你可以比如说另一个股票。

我可以就不用写到上面的这pri，它的 price price是30，然后shares1000。

![](img/dfafbddcd82dbd439f37451d2d11f4bd_60.png)

![](img/dfafbddcd82dbd439f37451d2d11f4bd_61.png)

![](img/dfafbddcd82dbd439f37451d2d11f4bd_62.png)

这边我仍然frameA。没有改成B。那么我们就可以看到这样的方案就会把他们的这些运算作为一个做了很少量的一个重复，呃，可以封装出更多的更复杂的一些算法。

那可能我value是不是还可能再加一些priameter？

![](img/dfafbddcd82dbd439f37451d2d11f4bd_64.png)

呃，再加一些参数，再加一些别的方案跟它进行对比。那么这就是我们的函数，我们后面很可能会碰到一些别的运算方案。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_66.png)

会用到函数，甚至包括你们写作业的时候，那么大家会对它对这个函数熟悉的话，对使用pyython会有很大的帮助。那么这是我们的第一节课，谢谢各位。



![](img/dfafbddcd82dbd439f37451d2d11f4bd_68.png)