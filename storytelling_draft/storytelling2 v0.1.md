# <center>Storytelling</center>

### Background

-----

Product hunt 是一个致力于发现产品闪光点的网站，个人和官方可以上传他们的产品到平台上供大众投票。Andrew Thompson and collaborators created a dataset of 76,000+ tech products. The dataset includes the name, description, launch date, upvote count, and other details for every product from 2014 to 2021 in the platform’s sitemap. 一些对于数据可视化小有研究的创作者们为这个数据集创建了一份可视化方案。The datasets are available here: https://components.one/datasets/product-hunt-products



### Introduction: Why is this story so appealing?

----

我们的生活中充斥着各种各样的产品，有时候我们会头疼于哪一款产品更适合我们。比如，当我们想要安装一款游戏平台时，使用steam还是origin似乎很难去抉择；当我们需要寻找一款简单但又可靠的文本编辑器时，我们往往对市面上眼花缭乱的各类产品中难以抉择。研究者为我们提供的这个可视化方案可以帮助我们更好的对产品选择有一个新的认识。Product hunt上的产品很多，你几乎可以找到所有你日常使用的产品，例如我现在在编写报告使用的编辑器 **Typora** 也可以轻易的在Product hunt上找到 。

![]()

(插入所有图片)



![]()



（插入typora图片）



### Beginning: How products are displayed and what can we get from the plot?

-----

![](D:\OneDrive - childishcherry\桌面\Rplot.png)

该可视化方案针对2014-2022年数据集中产品的点赞数进行了展示，变量有时间，点赞数和rank。每一个点都代表着一个不同的产品。其中横轴是产品发布的时间，时间以年为单位，范围从2014-2022。纵轴是点赞数，坐标轴不规则，分别展示了100，1000，10000的纵轴坐标。同时，rank代表了时间段点赞数的排名，也就是说，rank1代表同期点赞数第一的产品，rank2代表同期点赞数第二的产品。作者将可视化按照rank进行了分类从而创建了多个子图。我们先将旧图进行了复现，复现图如下:

![]()

（此处插入图片）



### Development: Awesome troubles in the graph

-----

但是在观察中，我们发现了问题，

首先，用户更需要并非不同类产品在同期的对比，这样的对比对于数据开发者来说可能有意义，但是对于用户来说毫无意义。

其次，图中展示了太多的数据点以及数据点之间的堆叠，众多的标签，这不符合简单性原则，按照proximity原则，在不仔细阅读的情况下，阅读者可能会将复杂堆叠的数据点误认为是一些相同类别的产品，实际上，他们并不相关。

第三，图中曲线的使用并没有附上标签，这就导致了歧义，用户可能会疑惑于曲线的真实含义，这违反了cognitive theory。





### Climax：See what can we do to improve it!

-----

首先，我们将分组的依据由不同类产品在同期的对比转换到相同类型的产品在所有时间段的的对比。这样，用户就可以更好的在他所需要的产品类型里面进行选择。

其次，关于数据点之间的堆叠和标签过多的问题。我们首先改变了点的颜色，颜色选自于http://colormind.io/这个网站，这个网站上的配色是深度学习某摄影机或者影视作品中提取出来的颜色。其次，为了解决堆叠问题，我们将点设定65~95的不透明值，以此来展示点的堆叠性。此外，由于大量数据点的意义不大，我们将突出的点与其他的点进行了区分，方便用户跟好的找到需要的应用。

最后，我们将均值和置信区间在图中显示出来，用来突出极个别优秀应用于众多应用的区别，以及数据的堆叠强弱。





### End of the story:  Let's see the amazing achievements! 

-----

（此处放新图）

新图介绍：

该可视化方案针对2014-2022年数据集中产品的点赞数进行了展示，变量有时间，点赞数和产品类别。其中横轴是时间，时间以年为单位，范围从2014-2022。纵轴是点赞数，坐标轴呈线性表示，分别展示了0到5000的纵轴坐标。同时，产品类别代表了该产品的定位和可用于的系统，分别为design tools，developer tools, iphone, mac, windows, other。我们将可视化按照类别标签进行了分类从而创建了多个子图。

获取内容：











### Conclusion

-------











