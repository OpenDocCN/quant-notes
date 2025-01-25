# python人工智能模型预测股票价格。 股票交易。量化交易。 - P1 - 江南经略 - BV1GNafe4EPw

你好。

![](img/256bce494c35a61d5b5ead7e33144993_1.png)

上次我们使用LSTM模型，针对股票的价格进行了模型训练，这次我们把LSTM模型改成transformer模型，进行训练，算式方法，模型是这几年非常流行的一种网络结构，很多大的语言模型。

大语言模型都是基于transformer进行训练的，例如china g b t chat gr m等等，今天咱们使用transformer，针对骨架做一个模型的训练，大概的步骤有这么几步。

第一步是下载股票的数据，第二步是针对数据做特征提取，第三步是做数据的加载器，第四步是构建我们的传输方本模型，第五步训练，第六步是测试和评估，针对测试集做一个测试和评估，我们看一下代码的文件，往左边看。

第一个是我们的文件放存放数据的文件夹。

![](img/256bce494c35a61d5b5ead7e33144993_3.png)

第二个是配置文件CONFIG，CONFIG里面的input window就是输入X序列的长度。

![](img/256bce494c35a61d5b5ead7e33144993_5.png)

然后说等于七，就是用七天的数据来预测未来一天的数据，out的window就是预测值的序列的长度。

![](img/256bce494c35a61d5b5ead7e33144993_7.png)

10download是下载股票的历史数据。

![](img/256bce494c35a61d5b5ead7e33144993_9.png)

使用的还是b I/O stock，这个在之前讲解过。

![](img/256bce494c35a61d5b5ead7e33144993_11.png)

第一是提取特征值feature，这里使用的是log，然后再取它们的差插值。

![](img/256bce494c35a61d5b5ead7e33144993_13.png)

做这个特征输入特征来大赛此文件，这里面的代码主要是构建数据加载器。

![](img/256bce494c35a61d5b5ead7e33144993_15.png)

为接下来的训练做准备，这里构建了train训练数据和test数据。

![](img/256bce494c35a61d5b5ead7e33144993_17.png)

训练数据占到整个数据的70%以上。

![](img/256bce494c35a61d5b5ead7e33144993_19.png)

一般是80%测试。

![](img/256bce494c35a61d5b5ead7e33144993_21.png)

剩下的所谓测试数据，他们输入是布鲁斯根据input的window来进行确定的。

![](img/256bce494c35a61d5b5ead7e33144993_23.png)

input的window之前我们讲过是等于七，也就是用七天的数据来预预测未来一天的数据。

![](img/256bce494c35a61d5b5ead7e33144993_25.png)

M 0possession。

![](img/256bce494c35a61d5b5ead7e33144993_27.png)

M0，possession行编码模型，这个模型是为了解决transformer中的输入数据，在相同数据的情况下，不同的位置一样，这种情况在这种情况下，如果没有位置的信息。

测试方某容易对相同的数据产生误解，通过测试，有了possessing这个模型信息之后，TRANSFORMAL的正确率提高了将近一个点。



![](img/256bce494c35a61d5b5ead7e33144993_29.png)

M0，测试方法是构建我们网络结构模型模型的。

![](img/256bce494c35a61d5b5ead7e33144993_31.png)

主要网络结构，这里使用了transformer的encoder层，没有使用transformer的decoder层。



![](img/256bce494c35a61d5b5ead7e33144993_33.png)

解码层只使用了编码层，他的解码使用了一个线性映射，也就是把transformer的输出数据，映射到一个数值上。



![](img/256bce494c35a61d5b5ead7e33144993_35.png)

这一个数值就是我们预测的未来一天的收盘价。

![](img/256bce494c35a61d5b5ead7e33144993_37.png)

这里我们来看一下position模型，Possessi。

![](img/256bce494c35a61d5b5ead7e33144993_39.png)

也就是pos encoder这个模型来，信息是如何在transformer中使用的。

![](img/256bce494c35a61d5b5ead7e33144993_41.png)

在former的这个函数中往下看，首先数据进行位置编码，位置编码之后，再把位置编码之后的数据输入到transformer，编码层中去。



![](img/256bce494c35a61d5b5ead7e33144993_43.png)

从而加入了位置编码的信息，M3test这个文件夹主要是额评估和测试使用的。

![](img/256bce494c35a61d5b5ead7e33144993_45.png)

![](img/256bce494c35a61d5b5ead7e33144993_46.png)

M4training就是我们的主要的训练函数。

![](img/256bce494c35a61d5b5ead7e33144993_48.png)

这里使用了这里使用了MS1这个损损失函数。

![](img/256bce494c35a61d5b5ead7e33144993_50.png)

也是计算的函数。

![](img/256bce494c35a61d5b5ead7e33144993_52.png)

它的训练与之前咱们讲的差不多，主要使用的主要使用了优化器和schedule。

![](img/256bce494c35a61d5b5ead7e33144993_54.png)

schedule呢是对学习率的一种修改，不拟合的情况进行对他的学习率进行矫正。

![](img/256bce494c35a61d5b5ead7e33144993_56.png)

M5是M5，predict是我们测试预测的嗯。

![](img/256bce494c35a61d5b5ead7e33144993_58.png)

预测一段数据的一个文件代码。

![](img/256bce494c35a61d5b5ead7e33144993_60.png)

接下来SAM的match就是我们保存的模型，数据整体结构非常清晰。

![](img/256bce494c35a61d5b5ead7e33144993_62.png)

大家看一看就能够看得很明白，代码放在了INTEHP上面，源代码我也会在下面的回复中。

![](img/256bce494c35a61d5b5ead7e33144993_64.png)

把这个链接贴上去。