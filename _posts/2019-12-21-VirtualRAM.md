---
layout:     post                    # 使用的布局(不需要改)
title:      强烈建议各大电脑厂商推出虚拟内存参数的功能            # 标题
subtitle:   大家好,我是秦始皇,其实我并没有死.我找到了长生不老药活到了现在,我的葬礼是个骗局,其实我埋葬了大量的财富.我现在手机没流量了,谁给我充100元话费,待我打个滴滴去咸阳,保你荣华富贵. #副标题
date:       2019-12-21 00:00:00 GMT+0800             # 时间
author:     Zen                 # 作者
header-img: img/photo/jiuzhaigou.webp    #这篇文章标题背景图片
catalog: False                       # 是否归档
tags:                               #标签
    - 杂谈
---

我说的这个功能,只是欺骗电脑使用者和一些娱乐为主的跑分软件,有些人不在乎数据真不真,看着高兴就行,管他3750H极限32G内存呢,写个128G大家都高兴
----

对于大多数人,他们不会使用redis等基于内存的kv非结构化数据库,大多数人也不会使用连续申请5G以上内存的程序(就算有,由于局部性原理,程序不知道申请的是连续物理内存还是和页面文件拼在一起的内存块),况且Windows有分页文件,linux\unix有swap,大多数号称需要大内存的只是需要空出来看的,而不是拿来用,他们只是想在各大跑分软件上看到自己的数字非常大,在娱乐大师上看到自己打败了国内百分之几的电脑,

----
最近又看到娱乐大师在搞笑了

![娱乐大师](https://raw.githubusercontent.com/zhangyiming748/zhangyiming748.github.io/master/img/EntertainmentMaster.jpg)<center>国产自主研发高仿AMD CPU 比龙芯什么的高级多了</center>

没看到笑点的自己去查查3550H配的什么型号显卡核心

----
学生党最大的问题,是特别容易被"性能思维"带偏
明明自己绩点最高,为什么成绩比自己差的同学能拿到比自己薪水高的Offer?
明明有些人智商一般,为什么就是比自己提拔得快?
为什么自己明明很努力,周围的朋友却还是围在家里有钱的同学身边?
为什么呢?
因为社会看中的是功能而不是"性能"
性能是跑分跑出来的,测试测出来的,写在元器件性能表上的
功能是用户用出来的,实际体验出来的,浸透在使用场景里的
性能体现在孤立的测试中,如考试,如跑分
功能提现在现实的场景里,如领导力,执行效率,人脉资源
学生最大的问题就是考试考多了,以为生活就是一连串测试拼起来,每道题都拿高分自己就走上人生巅峰了
然后推己及人,拿着这种思路看待这个世界,瞬间发现许多人都是傻子,都在交智商税,都在被下属蒙蔽,都在被渣男套路,都在被品牌欺骗,众生皆醉自己独醒
这时候微博上突然冒出来个"讲良心,跟自己交朋友"的企业,突然觉得心理距离被拉近,终于找到了懂自己的人,要赶紧贴上去抱团,让世界知道自己的精明
几千块钱的电子消费品,谁成天关心它跑分如何,元件价钱几何?
卡不卡我用一下不就知道了?
拍照好不好看拍一下不就知道了?
续航时间/充电速度,用下来不就明白了?
非要掐着秒表算续航,看着成本算利润,拿着色卡测相机,才叫理性消费才是聪明人?
大家都有正事儿要办,都有恋爱要谈,闲得慌呢成天拆分成熟的工业品测这儿测那儿的?手工业时代来的?
所以说,只要一款产品,价格在市场合理范围内,其功能解决了消费者的问题,提供了优秀的方案,大家用起来舒心,玩儿起来称手,拿起来有面儿,就成功了,谁没事闲得慌拿着算盘算成本??谁?还不就是有些没啥事儿干的学生呗
同样的道理,哪家公司靠你的绩点产生效益?哪个领导需要你的智商测试分数来帮他干活?哪个同学不想认识一些家里资源关系丰富的朋友?
为什么总觉得考得好就等于有能力就该拿个高工资?
分数能产生GDP还是能搞定客户关系?
我真的很好奇学生群体里的这部分人
是游戏不好打吗还是社团不好玩吗?
是篮球不激烈吗还是妹子很好追?
是论文很好写吗还是四六级很简单?
为什么成天要去计较别人买了贵的手机呢?
你是想去消协还是物价局?
是正好学了微电子还是供应链管理?
其中心态,看破不说破,自己领会.
----
言归正传
不知道用过电脑的人有没有这样的疑问:
```
我用2G内存的电脑占用内存1.75G
换到8G内存的电脑占用7.75
为什么不是之前占用的量了
我买8G内存电脑就是为了看到空闲的7.25G内存的
内存是我花钱买的
你们这些非亲非故的软件凭什么占用?
```
之前真的不知道大多数的电脑使用者为什么在追求大内存

经常接触者这类人让我明白

数大就是美

有些人觉得到从专业角度说不过我,那就人身攻击好了,你们随意

最后,还是先给这些人泼冷水吧 就当是冰桶挑战了

我用来工作的电脑,MacBookPro2019款,定制32G内存,开机内存照样占用80%以上,可怕吧?大内存实际上就是把命中率更低的文件尽量的也放在内存里,调用的时候更快,系统费尽心思预测你接下来要用的东西搬到内存里来,让你加载更快,有些人不但不领情还用了各种伪技巧继续清空内存
钱是你的,但是不是你买了一款电脑还来吹毛求疵(pi)的
没人强迫你买,就像郭德刚说的:
`内行要是去和外行辩论,那就是外行.比如我对火箭科学家说:你那火箭不行,燃料不好.我认为得选精煤,水洗煤不好.如果那科学家要是拿正眼看我一眼,那他就输了`
