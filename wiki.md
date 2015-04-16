---
layout: wiki
title: Crazepony Wiki
---

<div class="jumbotron">
    <p class="lead">这里是CrazePony的维基百科。我们提供DIY一个属于你自己四轴飞行器的文档，也提供对CrazePony四轴飞行器进行二次开发的指导。 </p>
</div>

* [入手试飞教程](wiki/user-guide.html)
* [组装维修教程](wiki/assemble-guide.html)
* [散件组装教程--5.0版本](wiki/assemble-guide-5-0.html)
* [入手试飞教程--5.0版本](wiki/user-guide-5-0.html)
* [散件组装教程--4.1版本](wiki/assemble-guide-4-1.html)
* [入手试飞教程--4.1版本](wiki/user-guide-4-1.html)

<h2>开发指南</h2>
* [windows下开发环境搭建—裸机版本](wiki/setup-environment-in-windows-none.html)
* [windows下开发环境搭建—FreeRTOS版本](wiki/setup-environment-in-windows.html)
* [linux下开发环境搭建](wiki/setup-environment-in-linux.html)
* [J-Link的使用及常见问题](wiki/jlink-debug.html)
* [Crazepony Android客户端](wiki/crazepony-android-client.html)
* [固件烧写](wiki/flash-firmware.html)
* [Crazepony上位机使用](wiki/param-assistant-manual.html)

<h2>Crazepony原理讲解</h2>
* [Crazepony器件选型总览及说明](wiki/ic-readme.html)
* [Crazepony硬件原理讲解](wiki/hardware-base.html)
* [Crazepony软件框架讲解](wiki/software-base.html)
* [Crazepony软件开发经验总结](wiki/software-experience.html)

<h2>四轴飞行器算法讲解</h2>
<p>姿态解算是指把陀螺仪、加速度计、罗盘等数据融合在一起，得出飞行器的空中姿态，也叫做姿态融合。姿态解算的过程，涉及到传感器数据读取与滤波，四元数与旋转，姿态解算框架，长期融合/快速融合。</p>
* [姿态解算简介](wiki/attitude-algorithm.html)
* [姿态的数学表示方法](wiki/attitude-math.html)
* [姿态的测量](wiki/attitude-measure.html)
* [姿态解算流程](wiki/attitude-algorithm-flow-graph.html)
* [软件姿态解算](wiki/software-algorithm.html)
* [硬件姿态解算](wiki/hardware-algorithm.html)
* [四元数](wiki/quaternions.html)
* [三轴陀螺仪和三轴加速度计MPU6050](wiki/mpu6050.html)
* [气压计MS5611](wiki/ms5611.html)
* [PID算法](wiki/algorithm-pid.html)

<h2>四轴飞行器</h2>
<p>开源硬件，创客是Crazepony成长的土壤。Crazepony也愿意更加积极的参与到创客活动中，给大家带来乐趣。</p>

* [四轴飞行器历史回顾](wiki/quadcopter-history.html)
* [开源四轴飞行器](wiki/opensource-quadcopter.html)
* [四轴飞行器明星产品](wiki/quadcopter-star.html)

<h2>航模基本概念扫盲</h2>
<p>四轴飞行器有其特有的力学结构，这部分是四轴结构的基本知识和组装。</p>
* [航模常用术语](wiki/copter-terminology.html)
* [大四轴 VS 小四轴](wiki/large-small-quadcopter.html)
* [三维中pitch，yaw，roll的区别](wiki/pitch-yaw-roll.html)
* [四轴飞行器的空气动力原理](wiki/quadcopter-aerodynamic.html)

<h2>四轴飞行器基本组成部分</h2>
* [航模电机](wiki/motor-aircraft-model.html)
* [电机驱动控制](wiki/motor-control-ic.html)
* [航模桨叶](wiki/propeller.html)
* [飞行控制器-主控MCU](wiki/main-controller-mcu.html)
* [飞行控制器——传感器](wiki/main-controller-sensor.html)
* [航模遥控器](wiki/remote-controller-2-4.html)
* [遥控器——蓝牙通信](wiki/remote-controller-bt.html)


<h2>Crazyflie</h2>
<p>Crazyflie使用了实时嵌入式操作系统FreeRTOS。相比于uCOS，FreeRTOS是完全开源免费的，而uCOS在商业上的应用是要收费的。作为一个轻量级的操作系统，功能包括：任务管理、时间管理、信号量、消息队列、内存管理、记录功能等，可基本满足较小系统的需要。下面介绍FreeRTOS的基本框架，在STM32上的移植等。</p>
* [FreeRTOS简介](wiki/freertos-intro.html)
* [介绍几个常用的宏的作用](wiki/macro-controls.html)
* [固件系统流程框架](wiki/system-flow-graph.html)
* [通信协议](wiki/comm-protocol.html)

<h2>手把手教你做穿越机H250</h2>
<p>H250是采用经典的碳纤机架组装的一款四轴飞行器，由于机架呈H型结构，故称之为H250。以其重量轻、体积小，续航时间长，易改装、控制灵活，又被誉为穿越机。H250与大四轴相比凸显为成本低，体积小，能穿梭楼道、丛里之间，亦可挂载GPS、图传数传设备，可谓具备大四轴的所有性能；与微型四轴飞行器对比，动力足速度快，抗干扰能力强，改装不受局限性，可实现空中特技飞行，足以体现暴力特点。
无论你是新手还是“老鸟”，H250终将属于你！！对于新手来说，入门要求低，飞控CC3D配置操作简单的地面站，支持新手向导配置，硬件配置为缩小版的大四轴，原理及架构更容易理解；对于一个久沙场的“老鸟”而言，CC3D支持自定义配参，调参配置不同飞行模式，穿越神器的快速、灵活定能享受不一样的爽飞体验。</p>
* [H250的材料列表](wiki/h250-list.html)
* [H250的组装](wiki/h250-assemble.html)
* [H250的调试和试飞](wiki/h250-debug.html)
* [H250的图传](wiki/h250-fpv.html)
* [H250的配置](wiki/h250-config.html)

<h2>Crazepony5.1版本</h2>
* [Crazepony5.1软件结构](wiki/softmain.html)

<h2>其他</h2>
* [Crazepony的板型及结构](wiki/crazepony-construct.html)
* [源代码的文件编码和文件格式](wiki/source-setting.html)
* [如何参与站点建设](wiki/wiki-help.html)
* [jekyll的安装和使用](wiki/jekyll-intro.html)
* [windows下github配置](wiki/windows-git-intro.html)
