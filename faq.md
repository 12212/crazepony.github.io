---
layout: faq
title: faq
---

## Crazepony四轴飞行器相关

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;Crazepony四轴飞行器是否入手即飞？

Crazepony四轴飞行器是入手即飞的。只需要安装桨叶，遥感冒等配件就可以体验飞行的乐趣了。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;Crazepony四轴飞行器是否针对有电子设计基础的伙伴提供深度DIY套件。

对于有电子设计基础和愿意DIY的伙伴，我们提供飞控主板，遥控器等套件。我们将会尽快整理出DIY套件清单和DIY的实例以供大家参考。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;无法垂直起飞的问题
小伙伴在拿到四轴飞行器试飞的时候，遇到无法垂直起飞的问题，可以从下面4个方面循序渐进，依次改进。

* 电机是否装正了，是否有偏的问题，或者电机轴位置被缠住了（一般是头发，我们就遇到）。
* 整个四轴的重心问题，主要是由于电池位置。你可以根据情况稍稍移动电池位置，改变其重心。
* 通过上面办法要做到完全的垂直起飞还是比较难。但是你可以再起飞的时候稍稍带一点方向遥杆，体验飞行应该是没有问题。我们基本上是做到这一步。
* 进一步的调试方法，那就是遥杆的归中值。也就是说，微调遥杆中间值。有一个上海的伙伴已经这样做了，并且和我们进行了沟通，他在飞控固件中对遥感数据的接收，加入了一个校正偏移量。另外一个方法就是到遥控器上修改，其实很多玩具四轴就是这样做的。就是在遥控器上有4个小按键，用于微调遥感归中值。在我们crazepony遥控器的左下角有几个按键没有焊接，那就可以预留这个作用的。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;飞控代码未使用RTOS
现在我们提供的稳定的飞控代码没有使用OS，全部是自己写的，并非网上流传的基于另外的四轴项目修改而来。

当然，我们尝试着把crazyflie的飞控代码（带有FreeRTOS操作系统）移植到我们的平台上来。但是没有完全弄好，当时为了学习crazyflie做过一些功课，参考Crazepony百科的最后[Crazyflie部分](http://www.crazepony.com/wiki.html)。对于想学习RTOS的朋友，建议阅读这部分代码，其软件架构/思路都非常优雅。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;Crazepony的尺寸是怎么样的？

Crazepony的长宽都是100mm，中间还有两处螺丝孔，可以用来安装桨叶保护圈（保护圈需要自己DIY）。

![](/assets/img/crazepony-size.jpg)

## 四轴飞行器相关

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;我是新手，如何入门？

参考[DIY四轴飞行器如何入门？](2014/07/31/diy-quadcopter.html)，这是介绍关于如何玩四轴的，以及大小四轴的区别。


### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;玩大四轴好呢，还是小四轴？

参考[DIY四轴飞行器如何入门？](2014/07/31/diy-quadcopter.html)，这是介绍关于如何玩四轴的，以及大小四轴的区别。

大小四轴除了大小不一样之外，在技术上主要区别在动力系统。参考文档[航模电机](http://www.crazepony.com/wiki/motor-aircraft-model.html)和[电机驱动控制](http://www.crazepony.com/wiki/motor-control-ic.html)。


### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;四轴飞行器的难点在哪里？

四轴飞行器是一种微型空中智能机器人，技术覆盖电子/机械/通信/计算机/自动化等多个学科领域。

其中最为复杂的在于飞行控制部分，参考文档[飞行控制器-主控MCU](http://www.crazepony.com/wiki/main-controller-mcu.html)。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;能否使用普通电池代替航模电池
现在提供的380mAh电池不够飞，能否使用手机电池等代理。回答是，不行。因为手机电池放电电流不够，需要专门的航模电池。电池上有个参数叫做放电倍率。例如crazepony使用的是是25c，这里的25c就是指的放电倍率为25C(5.0A)。也就是能够提供5A左右的电流。

crazepony上的一个716空心杯电机在工作时，大概需要700mA的电流。那么单单4个电机工作的电流，就需要2.8A。所以我们选用了能够提供5A电流的航模电池。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;关于调参软件，上位机

调参一般是一个锦上贴花的事情，四轴复杂在于飞控中的姿态结算和pid控制。可以看看crazyflie的调参协议，很有参考价值的。

我在看crazyflie的过程中，做了[部分笔记](http://www.crazepony.com/wiki/comm-protocol.html)。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;拥有一个遥控器，能够自制接收机嘛？

要自制接收机，就需要对该厂商遥控器的编码进行破解。例如crazyflie就支持ESky的遥控器，因为该遥控器的编码被大神破解并且公开。所以有人专门争对这个提供了接收机代码包。详见[Crazyflie笔记](http://www.crazepony.com/wiki/comm-protocol.html)。

## V4.1版本存在的问题

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;U10元器件没有贴片
U10是电子罗盘，我们还没有调试好，所以统一都还没有贴。没有调试好的原因，一是因为电路设计问题。另外，电子罗盘是磁场敏感元器件，很容易受到电机的影响。

### <i class="fa fa-arrow-right"></i>&nbsp;&nbsp;遥控器无法充电的问题
有小伙伴反应，遥控器无法充电。具体现象为充电的时候红色LED是半暗半亮状态，导致无法充电。最后发现是遥控器上是r7虚焊。如果有小伙伴也遇到这个问题，可以补焊一下。以后我们在发出之前会重点检查类似的问题。

如果有类似虚焊的问题，请告诉我们。感谢@张培鲲（海南）为我们指出这个问题。

<hr>

## Craze粉丝贡献榜单
Crazepony出来之后，很多网友建言献策，默默的为四轴的成长添砖加瓦。众人拾柴火焰高，有小伙伴提出Crazepony的改进意见，有小伙伴指出百科文档中的错误，还有小伙伴为Crazepony的推广不遗余力……

<table class="table table-bordered table-hover">
  <thead>
    <tr>
      <th>网络ID/姓名</th>
      <th>贡献内容</th>
      <th>备注</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ooo @610645105</td>
      <td>提出百科文档中的错误：<a href="https://github.com/Crazepony/crazepony.github.io/commit/4f95259939399d11b0d2852eed54b8afe7a567a1">4f9525</a></td>
      <td></td>
    </tr>
    <tr>
      <td>前面的风景会更好 @735661895</td>
      <td>百科文档：<a href="https://github.com/Crazepony/crazepony.github.io/commit/9f7dd03c12828adfe62f6f87393e8bc5b65db66c">9f7dd0</a></td>
      <td></td>
    </tr>
    <tr>
      <td>﹎仰望情空ぷ @781650550</td>
      <td>百科文档：<a href="https://github.com/Crazepony/crazepony.github.io/commit/5fa4fe0c9d02a5ea579ceb44a6a9e88c03fbd4d9">5fa4fe</a></td>
      <td></td>
    </tr>
    <tr>
        <td>( ´ ▽ ` )ﾉOwl猫头鹰 @765198459</td><td> 分享Crazepony参与源码纠错</td>
        <td></td>
    </tr>
    <tr>
        <td>宇智波 佥源  @862750667</td><td> 分享Crazepony</td>
        <td><a href="http://www.eeboard.com/bbs/thread-37979-1-1.html">爱板网的帖子</a></td>
    </tr>
    <tr>
        <td>沉迷学习无法自拔的seven  @495154953</td><td> 网站视频 编辑哥哥</td>
        <td></td>
    </tr>
    <tr>
        <td>哼嘿哈嘿哈  @137859310</td><td> 积极参与源码的纠错</td>
        <td></td>
    </tr>
    <tr>
        <td>dajianli @447949135</td><td> 积极分享Crazepony</td>
        <td></td>
    </tr>
    <tr>
        <td>lovingflying  @1143615270</td>
        <td> Crazepony核心算法改善</td>
        <td></td>
    </tr>
    <tr>
        <td>曾航（深圳）</td>
        <td>1.遥控器需要添加微调的按钮<br>2.电池应该用薄一点的双面胶，不要露出电池外面</td>
        <td>第二条已经解决，使用了汽车玻璃上用的透明双面胶<br>第一条将会在下一版本中改进</td>
    </tr>
    <tr>
        <td>张培鲲（海南）</td>
        <td>1.开关按键容易坏的问题<br>2.提出了使用螺丝锁定电机套的办法<br>3.发现并且解决了遥控器无法充电问题</td>
        <td>开关按键已经跟换了新的物料<br>遥控器无法充电问题解决</td>
    </tr>
  </tbody>
</table>

