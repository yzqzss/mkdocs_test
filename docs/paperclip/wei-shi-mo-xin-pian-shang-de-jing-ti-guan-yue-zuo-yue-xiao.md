# 为什么芯片上的晶体管越做越小

九月的最后一天，我们发布了一支[《如何在纳米尺度雕刻芯片》](http://mp.weixin.qq.com/s?__biz=MzA3NDM1MjUwNg==&mid=2247488778&idx=1&sn=885e6df615c3d9cce87ff6a6a4b5466c&chksm=9f00471fa877ce0962de299d6c5263bd8052a8126b99a1ddb980dc694c373a3afc4d35350846&scene=21#wechat_redirect)，展现芯片制造的工艺和难点。在评论区，我们收到了一个有趣的提问：为什么一定要把晶体管做小？

今天，我们就将重点聚焦到芯片里最基础的结构——晶体管，并试图解答：制约晶体管越做越小的因素，究竟是什么？

这是世界上第一支三极晶体管的复制品，大约有一个苹果那么大。和其他一些简单的电子元件一起，可以组成一个晶体管收音机。

![img](https://mmbiz.qpic.cn/mmbiz_gif/SlOqFKqEO4F89iaAISrNsQewhFq3eznMIicQ7o4BYcpp7lBMIKkzfafYkBwJhPAGHfXVY3jdHdm3OROFjS1EkCJw/640?wx_fmt=gif)

今天，数字电路中最常见的晶体管被称为 MOSFET，简化一下大概长这样，尺寸缩小到以纳米为计。你的手机和电脑里的芯片，都是由数十亿个这样的晶体管组成的。依照电流产生的不同方式，可分为 N 型和 P 型。

![img](https://i.loli.net/2021/10/24/QnyUfOxMDa5q4lG.gif)

在 1965 年到 1975 年，英特尔的创始人高登·摩尔（Gordon Moore）指出，芯片中的晶体管数量大概每两年翻一番。由于芯片通常采用平面工艺，相对应地，晶体管的尺寸每两年也在缩小约 30%。

尺寸，代表着晶体管的技术节点。起初，它用栅极长度来表示，如果这个长度为 90 nm，那每平方毫米的芯片大概能容纳约一百四十五万个这样的晶体管。

尽管这只是一个经验性预测，却被半导体行业精确地执行了 40 余年。为什么晶体管需要越做越小？

![img](https://i.loli.net/2021/10/24/oMQment4AzlH8qK.png)

回答这个问题之前，首先要知道 MOSFET 晶体管是如何工作的。

它本质上是一个开关，其中的栅极，决定了源极 S 和漏极 D 之间能否导通。

以 N 型晶体管为例，栅极、介电层和底部的 P 型硅衬底组成了一个简单的电容器。当栅极没有加电压的时候，S 和 D 中间的沟道电子很少，因此电阻比较大，S 和 D 无法导通；而当栅极加一个正电压的时候，由于电场的吸引，电子聚集在 S 和 D 之间的沟道内，因此电阻减小，S 和 D 导通。

![img](https://i.loli.net/2021/10/24/N9mesx6SAbUpuqX.gif)

如果把一个 N 型 MOSFET 和一个 P 型 MOSFET 以下图的方式组合在一起，就构成了一个简单的反相器电路，用来实现最基本的「非」逻辑运算，比如输入 0 输出 1，输入 1 则输出 0。多个类似的逻辑模块的组合就可以实现基础的加减法乃至导弹姿态控制这样的复杂计算。

![img](https://i.loli.net/2021/10/24/j6wntyTA9zJXYvB.png)

显而易见，要实现这么复杂的功能，肯定需要很多个晶体管。因此，必须把晶体管做得足够小，才能塞进你的电脑机箱。

不过，还有比这更重要的原因在驱使晶体管不断变小——我们需要提高晶体管的开关速度。

以晶体管最重要的应用 CPU 为例，晶体管的开关速度限制了 CPU 的运算速度。

根据电容器充电原理，开关导通速度和电容大小相关。电容越大，充电时间越长，开关导通速度越慢。所以，我们需要减小电容，从而提高运算速度。

![img](https://i.loli.net/2021/10/24/2qM6ZcDETdPCb3t.png)

从上面这个公式可以看出，减小电容可以通过三种方式：增加介电层厚度，改变介电常数，和减小面积。

但介电层厚度太大，会导致沟道内的电场不够强，不足以导通；改变介电常数需要更换介电材料，相当长的时间里可供选择的介电材料非常有限。

因此，唯一可行的方法就是减小面积，也就是减小沟道长度和宽度。于是，晶体管遵循这一策略一直缩小。正准备迈向 22 nm 节点时，问题出现了。

当沟道长度小于一定值，栅极对于沟道的控制能力下降。以 N 型 MOSFET 为例，在栅极没有加压时，沟道处于关断状态。此时，漏极电压为 10 mV，不论是长沟道还是短沟道，电子在跨越栅极时都需要更高的能量，像翻越一座高山。

![img](https://i.loli.net/2021/10/24/y7kWEcNYHVL8ro9.png)

而当漏极电压增大到 1 V 时，短沟道的电子跨越栅极所需的能量大大减少，让晶体管直接从关断变成导通。以往横亘的高山被削平，电子的流动再也不受限制了。

![img](https://i.loli.net/2021/10/24/UE7w4ul1qvjnB2c.png)

到了这个地步，晶体管还能再更小吗？

加州大学伯克利分校的胡正明教授给出了肯定的答案，他在世纪之交提出 FinFET（鳍式场效应晶体管）的概念，进一步激发了晶体管的潜能。

![img](https://i.loli.net/2021/10/24/RONrIqyUKCtVk74.png)

通过将沟道向上延展，变成一个类似鱼鳍的形状，使得栅极可以从三个方向对沟道施加电场，从而保证即便沟道长度很小，也能有效地控制开关。从 22 nm 以下的晶体管器件开始，基本上都采用了这一结构。

随着结构的变化以及工艺的进步，今天，工艺名称已经不再和栅极长度完全对应。比如台积电的 7 nm 工艺制造的晶体管，栅极长度约 24 nm，每平方毫米芯片上排布着约九千六百五十万个晶体管。

同时由于电感和电阻的增加，令缩小尺寸带来的开关速度提升愈发不明显，算力的提升主要依靠增加单位面积的晶体管数量，这就是为什么你的 CPU 主频和十年前的没有什么差别，但核心数量则一直在增加。这也从另一个方面要求晶体管尺寸做得更小。

![img](https://i.loli.net/2021/10/24/DstvrAIyHajENXZ.png)

除了提高运算速度，我们也希望 CPU 里的晶体管在完成每一个运算的同时，消耗尽可能少的电。

电都花在哪儿了呢？

观察晶体管的开关方式，可以发现能量主要消耗在两个地方：一个是开关时对栅极 G 电容的充放电；另一个是导通时源极 S 和漏极 D 之间的电阻消耗，以及关断期间的漏电流。

其中栅极 G 上的开关损耗可以表示为下面这道公式。能量损耗与电容、开关频率和工作电压的平方成正比，在必须提高开关速度且不能改变工作电压的情况下，只能尽量减小电容来降低损耗。

![img](https://i.loli.net/2021/10/24/9RMxkLSzyrIT3aN.png)

于是，缩小尺寸就成为提高运算速度和降低功耗的不二法门。

为了实现变小变快的愿景，过去几十年间，全世界最顶尖的工程师在这个无法直接用肉眼观测的世界里不断钻研。除了以上提到的速度和功耗，加工成本、导线互联的延迟和损耗、散热效率等众多复杂的原因也在共同影响着晶体管的发展。

今天，一块不到一平方厘米的空间，容纳着数以百亿计的晶体管，也集成着人类的群体智慧，不断改变你的生活方式。

![img](https://mmbiz.qpic.cn/mmbiz_gif/SlOqFKqEO4F89iaAISrNsQewhFq3eznMILibO9b9MFzmaD60VMokjZcxj8AwrBUWqBxzwgpzXgIxsibph06HqHiatg/640?wx_fmt=gif)

\-

> 封面图来源：
>
> Tomizak, Flickr.
>
> 参考资料：
>
> [1] Ytterdal, T., Cheng, Y., & Fjeldly, T. A. (2003). Device Modeling for Analog and RF CMOS Circuit Design. Wiley.
>
> [2] Hisamoto, D., et al. (2000). FinFET—A Self-Aligned Double-Gate MOSFET Scalable to 20 nm. IEEE TRANSACTIONS ON ELECTRON DEVICES, 47(12), 2320-2325.
>
> [3] Amirtharajah, R. (2008). EEC 216 Lecture #1: CMOS Power Dissipation and Trends. University of California, 28-33.