# 为什么你的手机读取数据这么慢

这是 2006 年最时尚的智慧型电话——诺基亚 N73，除去系统，手机内部存储空间只有不到 20MB，存几首最流行的《两只蝴蝶》手机就满了。

![img](https://i.loli.net/2021/10/30/u9MXFD45vdYHAie.jpg)

这时就需要一张 miniSD 卡来装下你的照片、游戏、音乐。

![img](https://i.loli.net/2021/10/30/X2uZdaTfsbUigO9.jpg)

2006 年，SD 卡就是插在手机里的U盘，读取或存储用户的各种数据。但数据一多， SD 卡读取起来也相当吃力，翻几张照片就可能让手机卡顿甚至崩溃。

10 年后，再也没人往手机里插内存卡了，取而代之的是一块内置在手机里的闪存，也叫 flash memory，相当于手机的硬盘。

![img](https://i.loli.net/2021/10/30/dqDeZOVWkzQnXx7.jpg)

在 64GB 闪存保底的 2019 年，几乎没人担心放不下照片了，但怎样流畅地读取数据又成为了一个新问题。

单从手机硬件配置入手，流畅地读写数据关系到核心 CPU 处理器、运行内存等，但还得看加持在闪存中的闪存技术。

目前，业界公认的最顶级手机闪存标准是 UFS3.0。前不久发布的一加 7 系列，就全系标配了 UFS3.0 闪存技术，也让一加成为第一家大规模将 UFS3.0 商用的手机品牌。

UFS3.0 究竟是什么？它又能带来什么样的体验？这还得从闪存的数据传输标准说起。

2000 年初，MultiMediaCard 协会提出了手机闪存的首个标准：eMMC(embeddedMulti Media Card)，将控制芯片和闪存颗粒封装在一个芯片内。

![img](https://i.loli.net/2021/10/30/58GbDxZCLdJKg6e.jpg)

在手机处理器处在性能较低的时代，采用并行传输的 eMMC 十分契合当时用户对手机数据的低消费需求。

但在数据量革命性增加的今天，并行传输的 eMMC 有很多先天不足：

在并行传输中，如果并行线路之间的物理性质不一致，例如长度上有细微差别，会导致并行线路中传输的比特不是同时到达接收方，在接收数据时容易出错。

再者，eMMC 只支持同步命令处理，即命令只能一个一个执行，或者一包一包（每个包里面含有若干个命令）执行，前面命令没有执行完成，后面的命令是不能发下去的。

![img](https://i.loli.net/2021/10/30/hOAJVoxscbKD7BU.jpg)

比如手机处理器发出一个写入数据命令 W1 和读取数据命令 R2，就等命令 W1 完成，才能展开读取数据的命令 R2；同样，在发送写入命令 W3 之前，必须等 R2 命令完成。

相当于你的任何操作都要排队进行处理，而这个队伍并不一定是整齐有序的，前方队列稍有失误，后方就会一片混乱，溃不成军。

想象一下，当你正用手机在一场游戏排位赛中紧张酣战，到了最紧张的推水晶时刻。这时甲方爸爸突然发来四十多条修改意见，你手中这部采用 eMMC 闪存技术的手机因为大量数据涌入读写并发执行，游戏瞬间崩溃死机，还坑了排队赛的队友掉星。

在这一系列限制下，即使在 2015 年发布的最新 eMMC5.1 标准，理论带宽能达到 600MB/s 的前提下，也应付不了数据量剧增的读写要求，之后 eMMC 未再更新标准。

![img](https://i.loli.net/2021/10/30/ZoG7Owfh6ryHdzB.jpg)

你的数据总是只增不减，更多的照片、聊天记录、大容量游戏填满了手机的闪存，手机读写变得越来越慢，你不得不通过经常删除冗余资料这种拆东墙补西墙的方法来缓解手机闪存读写性能下降。

在 4G 时代诞生了以下问题：当日益加速的无线网络传输速度遇上跟不上用户需求的闪存读写速度，手机该如何做才能满足人类日渐膨胀的游戏热情以及对高清小视频的强烈需求，成为一道难题。

于是 UFS 诞生了。在2011 年，电子设备工程联合委员会（简称JEDEC）发布了全新的闪存技术标准——“UniversalFlash Storage”，通用闪存存储技术，简称 “UFS”。

![img](https://i.loli.net/2021/10/30/7mauyktd8zRHJQn.jpg)

UFS 是一个为高速传输数据而设计的闪存技术，采用双通道串行方案，再也不需要担心数据传输时互相干扰，能以更大的带宽配合更高频率传输数据，同时读写数据也不再是问题。

与eMMC 相比，UFS是全双工模式，可以同时接受很多命令，并行和乱序执行，谁先完成谁先返回状态。 

![img](https://i.loli.net/2021/10/30/ZeqUXzy3nB5iDxG.jpg)

在 UFS2.0 上，持续读写速度就达到 700M/s 左右，全面超越 eMMC5.1。再者，由于 UFS 的制造工艺要求更高，同容量的 UFS 闪存要比 eMMC 最多贵上 30%。

如此一来，也导致今天很多中低端手机因为成本原因还在使用 eMMC闪存，而 UFS 逐渐成为高端旗舰手机的标配。

在 UFS2.0 之后，更新了 UFS2.1，其数据读取速度达到了 1.5G/s，不过这速度还不够快。

今天的闪存已经步入 UFS3.0 时代。UFS3.0 理论带宽已经达到2.9GB/s，是上一代 UFS2.1 性能的两倍； 工作电压也从 UFS2.1 的2.7-3.6V 降低到 UFS3.0 的 2.5V。

简单来说，就是 UFS3.0 闪存技术有更快的读写速度，更低的功耗。

如果说 eMMC 是人们还在单行道上相互礼让，那么 UFS2.0 是已经开上了双向四车道的水泥高速路，而 UFS2.1 是在双向八车道由沥青铺成的高速公路飞奔，最新的 UFS3.0 则是无数辆蝙蝠侠的蝙蝠战车在上天入地，飞奔而至。

![img](https://i.loli.net/2021/10/30/KBGN3YqkjTWbRUJ.jpg)

纵然有数字上的提升，但以更生活的实际操作场景来说，能让消费者感知 UFS3.0 闪存技术的优势。就拿刚刚在京东 618 中斩获 3000-3999 元价位段单品销量冠军的一加7 为例子讲讲。

![img](https://i.loli.net/2021/10/30/1wingC6hZQMk9rz.jpg)

当你打开进入《和平精英》这类大容量的吃鸡游戏，首先面对的是游戏的加载进度条，这就是在读取手机闪存的游戏数据。

采用了 UFS3.0 闪存技术的一加 7，配合一加工程师们对软件进行的优化，会让这个加载的时间大大缩短，快人一步，率先冲进战场。

在你浏览大容量相册时，以往总会出现相册图片视频的加载速度跟不上，无法显示照片内容的问题。

但在一加 7 上，有了 UFS3.0 闪存技术再经过强大的优化，能够迅速加载并实时反馈，相册滑到哪里就加载到那里，再也不用傻看着黑屏焦急等待自己的照片加载完成了。

口说无凭，再拿出测试数据，才更有说服力：

在科技媒体“科技美学”的测试中，一个 2.03G 的《和平精英》游戏安装包，在 eMMC 机型上需要超过 1 分钟才能安装完成，UFS2.1 机型需要 18 秒，而搭载了 UFS3.0 闪存技术的一加手机仅需 11 秒。

![img](https://i.loli.net/2021/10/30/O5bHCMAJRX2vnZw.gif)

下载安装《和平精英》速度对比评测视频（左起：UFS 3.0, UFS 2.1, UFS 2.0, eMMC 5.1），by 科技美学

有了采用 UFS3.0 闪存技术的一加 7，配合高通骁龙™ 855 移动平台、8GB 的 LPDDR4X 四通道内存等顶级硬件与系统优化，让整机在操作上更流畅，让“快”变得理所当然。

但高效的数据读写更要配合沉浸的体验，一加还针对游戏场景优化升级，比如一加 7 内置的 Fnatic 电竞模式：当你使用一加7进入游戏并开启该模式，来电和通知都将被拒之门外。

同时，一加还针对多款主流游戏进行了专属优化，让一加 7 满帧运行绝大部分游戏，成为你不折不扣的竞技利器。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/U6yRaDu1NaZw1DgSI3ZH5WHia0B8H5fV0SF9iaPGH5ouWLIPzJs1Im7SIgPhYxYicPu0fB09sG6w97JiagLf7WVkjQ/640?wx_fmt=jpeg)

颜值上，一加7也给你满意的答复，在拥有一块高达 6.41 英寸的显示屏的同时，保持了 5.5 英寸手机良好的握感，轻薄圆润，用起来更加得心应手。

这一次，你玩王者荣耀时，再也不用担心队友全部加载到 100%，而你还停留在 10% 龟速加载的尴尬情形，也不用担心突发消息干扰游戏甚至造成卡顿，有了采用 UFS3.0 闪存技术的一加7，从此精彩大不同。