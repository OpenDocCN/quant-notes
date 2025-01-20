# 【量化交易】Python入门之数据分析【2／4】｜ 金融工程 量化金融 - P2：2-1. Python数据分析：Module2 - Pandas Series - Devils-Advocate - BV1RdHAemERq

各位好，从module two开始，我们进入pas的学习。pas是一个非常重要的数据包，不管是做量化还是金融还是数据分析，它。有点像我们用的excel，它是一个面板数据。

那么我们首先inport了一下padas。好，然后我先做几个数据吧。我们以实物来做案例。你们可以有。Tomato。Banana。And apple。pandas数据里面呢有一个很重要的部分。

就是pandas series。 series有点像我们之前用的numbyny array。但是呢它的区别。很快大家就会看到。首先，panda series它是有前面的这个索引。

还有它的on这边我由我没给它这个列名，所以它是unname的，但是它是由索引和列名组成。那它也可以是一些数字。



![](img/772fd6094608feb31d2241903369e593_1.png)

![](img/772fd6094608feb31d2241903369e593_2.png)

呃，一样的，前面这边是string，这边是integer。或者呢。他可以是如果我们遇到。嗯。比如说tomato，banana。And none。这种。空指应该怎么处理呢？

panace series animalsimal。

![](img/772fd6094608feb31d2241903369e593_4.png)

那这里如果是它在 string，它会直接显示nun，但如果它是数字的话，会有一些变化。Numbers12。别人给他一个闹。PD series。Numbers。



![](img/772fd6094608feb31d2241903369e593_6.png)

那么我们会可以看到这边是NAN。那NAN和nun是一样的吗？我们可以inport一下n派。

![](img/772fd6094608feb31d2241903369e593_8.png)

因为只有n派的数据名。可以存在NAN比如说这里NAN这这两个是类似的东西。但是如果NAN和nun之间是一样的吗？



![](img/772fd6094608feb31d2241903369e593_10.png)

那其实不一样的，你可以看到它是显示是false。那NAN和NAN之间是一样的吗？它甚至也是不一样的。

![](img/772fd6094608feb31d2241903369e593_12.png)

也是falcese。所以那怎么判断？就是假如我数据中间它有个。有个这种NANvalue，我们应该怎么判断呢？我们需要用到numb派的n派 is none。



![](img/772fd6094608feb31d2241903369e593_14.png)

![](img/772fd6094608feb31d2241903369e593_15.png)

这样子来判断就是。n派的is known这个函数来判断MP点NAA，也就是这里的NAN它是否是一个空值。那么现在我再给一些数据。



![](img/772fd6094608feb31d2241903369e593_17.png)

Sports。我们有tennis对应USAbaseball，对应japan，soccer对brazil。那么我把它给放到一个。



![](img/772fd6094608feb31d2241903369e593_19.png)

pannda series里面去。

![](img/772fd6094608feb31d2241903369e593_21.png)

你可以看到S。它已经进入了一个面板数据。那么我们可以看一下它的索引值S到的index，这是我们查到的索引，就tens baseball ands。然后这边的USAjapan，brail就对应它的值。

这边之所以这边是值。

![](img/772fd6094608feb31d2241903369e593_23.png)

No。我可以把它换一个索引吗？比如。比如说S等于PD等于sious。Yeah。我把它换成我不用sporturs了。我比如说我把它换成动物tiger。Paandnda。Panda， not pandas。

boxox，然后呢我对应的index。index变成。USa。China。

![](img/772fd6094608feb31d2241903369e593_25.png)

Canada。

![](img/772fd6094608feb31d2241903369e593_27.png)

这边我们相当于重填了数据，我们把这个animals填成了它的值，然后它的index填成了它的。

![](img/772fd6094608feb31d2241903369e593_29.png)

嗯，所以。这是直接在serious里填，相相对于我们这边使用的。

![](img/772fd6094608feb31d2241903369e593_31.png)

使用的一个字典形式。

![](img/772fd6094608feb31d2241903369e593_33.png)

![](img/772fd6094608feb31d2241903369e593_34.png)

相比于我们用字典把它变成了一个pennda series，我们还可以做什么呢？我们还有没有别的办法来做一个pen series，那也是有的。S等于PD series。我们可以给他。Tiger。

Panda。Fox。and它的索引index。USa。China。嗯，这边我都用了双引号，所以这边最好也用双引号china。



![](img/772fd6094608feb31d2241903369e593_36.png)

And Canada。这样子也能得出一个带索引的pada theory。

![](img/772fd6094608feb31d2241903369e593_38.png)

![](img/772fd6094608feb31d2241903369e593_39.png)

那我如果混用呢？Sports。我把这个拷贝下来。

![](img/772fd6094608feb31d2241903369e593_41.png)

然后我再拿这个。

![](img/772fd6094608feb31d2241903369e593_43.png)

但是呢这里我把它的index给换一下。index我换成。不这边用这边我直接用sports，我把我相当于先把这个填充进来，然后呢我们再来。



![](img/772fd6094608feb31d2241903369e593_45.png)

那我们是否可以用index，就是我们只选择前面的。

![](img/772fd6094608feb31d2241903369e593_47.png)

比如说我字典，但是我有一个字典，但是我只想选择字典里面的某一些值。我先把这个sports填充到字，就是这个字典填充到serious里面。但是我并不想要这么多，就是全部的数据。

我可以选择baseball ands，然后把这个删掉。那我是不是只选择了后面两个呢？我们来看一下它会不会报错。



![](img/772fd6094608feb31d2241903369e593_49.png)

那是可以的。这边比如说我们选择了baseball ands，它对应japan、 Brazilz，而我们忽略了tennis USA。



![](img/772fd6094608feb31d2241903369e593_51.png)