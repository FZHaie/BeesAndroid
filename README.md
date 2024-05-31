# BeesAndroid

[![License](https://img.shields.io/github/issues/BeesX/BeesAndroid.svg)](https://jitpack.io/#BeesX/BeesAndroid)
[![Stars](https://img.shields.io/github/stars/BeesX/BeesAndroid.svg)](https://jitpack.io/#BeesX/BeesAndroid)
[![Stars](https://img.shields.io/github/forks/BeesX/BeesAndroid.svg)](https://jitpack.io/#BeesX/BeesAndroid)
[![Forks](https://img.shields.io/github/issues/BeesX/BeesAndroid.svg)](https://jitpack.io/#BeesX/BeesAndroid)

## 项目介绍

**关于BeesX开源技术小组**

> Bees（蜜蜂），取义蜜蜂精神求实、合作与奉献，也即BeesX开源技术小组的宗旨，求真务实，合作奉献，本小组旨在通过提供一系列的工具、方法与文档，帮助更多的无线开发工程师理解和掌握无线开发技术。

BeesAndroid项目于2018年3月6日同步上线，该项目的前身是[android-open-source-project-analysis](https://github.com/guoxiaoxing/android-open-source-project-analysis)，这个项目提供了一系列的Android系统源码分析文章，收到了良好的反馈。但是一个人的力量是有限的，因此将其推成团体项目BeesAndroid，项目采用GPL协议，在保护作者知识产权的基础上，最大化的做到开源与开放，如果有什么问题和意见欢迎提交issue，也欢迎大家参与到本项目中来。

**关于BeesAndroid项目**<br />

> [BeesAndroid](https://github.com/BeesAndroid/BeesAndroid)项目提供了一系列的工具、理论分析与方法论，旨在降低Android系统源码的阅读门槛，让读者更好的理解Android系统的设计与实现。第一次阅览本系列文章，请参见[导读](https://www.yuque.com/beesx/beesandroid/uufhxo)，更多文章请参见[文章目录](https://github.com/BeesX/BeesAndroid)。

- [掘金博客](https://juejin.im/user/5886d699128fe1006c455fb6)
- [在线书籍](https://www.yuque.com/beesx/beesandroid/px0ka4)

**代码版本**

- 分支：[android-7.0.0_r34](https://cs.android.com/android/platform/superproject/+/android-7.0.0_r34:)
- 版本：Nougat
- 支持设备：Nexus 6

![image.png](https://cdn.nlark.com/yuque/0/2020/png/279116/1589094049155-48b48ffb-fae2-49dd-ba38-0fd715dca04f.png#align=left&display=inline&height=325&margin=%5Bobject%20Object%5D&name=image.png&originHeight=650&originWidth=1913&size=160749&status=done&style=none&width=956.5)

**分析思路**

Android是一个庞大的系统，Android Framework只是对系统的一个封装，里面还牵扯到JNI、C++、Java虚拟机、Linux系统内核、指令集等。面对如此庞大的系统，我们得有一定的 章法去阅读源码，否则就会只见树木不见森林，陷入卷帙浩繁的细节与琐碎之中。<br />

- 善于抓住主线和支线，主线指的就是Android系统的各个模块，支线就是这个模块从上值下各个层级中的重要元素，逐一分析，直至探究到模块的最根源层。
- 不要去记录那些API调用链，绘制一个序列图理清思路即可，Android Framework中有很多复杂的API调用链，你去关注这些东西，用处不大。你需要学会的是跟踪调用链和梳理流程的 技巧，思考一下作者是怎么找到关键入口的，核心的实现在什么地方。
- 要善于思考，要多问为什么，面对一个模块，你要去思考这个模块解决了什么问题，这个问题的本质是什么，为什么这么解决，如果让我来写，我会怎么设计。事实上不管是是计算机还是 手机，从CPU、到内存、到操作系统、到应用层，看似纷繁复杂，但问题的本质无非就是这么几种：时间片怎么分配？线程/进程怎么调度？通信的机制是什么？只是在不同的场景下加了具体 的优化，但问题的本质没有改变，我们要善于抓住本质。
- 要善于去粗存精，Android Framework也是人写的，有精华也有糟粕，并不是每行代码你都需要问个为什么，很多时候没有那么多为什么，只是当时那种情况下就那样设计了。但是 对于关键函数我们要去深究它的实现细节。

在正式阅读本系列文章之前，请先阅读导读相关内容，这会帮助你更加快捷的理解文章内容

- [导读](https://www.yuque.com/beesx/beesandroid/uufhxo)

你也可以先阅读关于Android系统的概述，让你有Android系统的设计有个整体的把握。

- [Android系统设计概述](https://www.yuque.com/beesx/beesandroid/lk9rug)
- [Android系统设计原则与设计模式](https://www.yuque.com/beesx/beesandroid/vxai8u)

欢迎提交Issue与PR，为帮助我们更好的维护此项目，请先阅读wiki里的相关规范。

- [Wiki](https://github.com/BeesAndroid/BeesAndroid/wiki)

## 文章目录

### 导读

- [Android源码阅读指南](https://www.yuque.com/beesx/beesandroid/uufhxo#37d355bc)
- [Android系统设计概述](https://www.yuque.com/beesx/beesandroid/lk9rug)
- [Android系统与设计模式](https://www.yuque.com/beesx/beesandroid/vxai8u)

### 串讲

#### 渲染机制

- [聊一聊Android的渲染机制](https://www.yuque.com/beesx/beesandroid/qh7ohm)
- [聊一聊Chromium的渲染机制](https://www.yuque.com/beesx/beesandroid/yqrpg3)
- [聊一聊小程序的渲染机制](https://www.yuque.com/beesx/beesandroid/lhdb28)
- [聊一聊Flutter渲染机制](https://www.yuque.com/beesx/beesandroid/qr16m0)

### Android系统简介

- [Android系统简介](https://www.yuque.com/beesx/beesandroid/pq4y3r)

### Android应用原理

- [Android应用系统](https://www.yuque.com/beesx/beesandroid/vqsfzs)
  - [Android应用上下文Context](https://www.yuque.com/beesx/beesandroid/hy6ghk)
  - [Android应用主线程ActivityThread](https://www.yuque.com/beesx/beesandroid/sh1ig9)
  - [Android组件注册表AndroidManifest](https://www.yuque.com/beesx/beesandroid/wftabs)
- [Android视图系统](https://www.yuque.com/beesx/beesandroid/bx3aos)
  - [Android应用视图View](https://www.yuque.com/beesx/beesandroid/tgmglv)
  - [Android应用窗口Window](https://www.yuque.com/beesx/beesandroid/zcqcbu)
- [Android组件系统](https://www.yuque.com/beesx/beesandroid/sss5iv)
- [Android多媒体系统](https://www.yuque.com/beesx/beesandroid/cvtizc)
- [Android浏览器系统](https://www.yuque.com/beesx/beesandroid/nmh2oh)

### Android系统原理

- [Android的进程与线程](https://www.yuque.com/beesx/beesandroid/melzk5)
  - [线程通信的桥梁Handler](https://www.yuque.com/beesx/beesandroid/ewlw6g)
  - [进程通信的桥梁Binder](https://www.yuque.com/beesx/beesandroid/xomd5v)
- [Android系统进程启动流程](https://www.yuque.com/beesx/beesandroid/vhwgnp)
- [Android组件管理服务AWS](https://www.yuque.com/beesx/beesandroid/hl45fu)
- [Android窗口管理服务WMS](https://www.yuque.com/beesx/beesandroid/vo3gnn)
- [Android界面绘制服务SurfaceFlinger](https://www.yuque.com/beesx/beesandroid/di94uy)
- [Android OpenGL ES原理](https://www.yuque.com/beesx/beesandroid/ute8fx)
- [Android应用程序编译与打包](https://www.yuque.com/beesx/beesandroid/kwvy6i)
- [Android虚拟机ART](https://www.yuque.com/beesx/beesandroid/vle3ac)
- [Android系统安全机制](https://www.yuque.com/beesx/beesandroid/fp65ci)

### Android系统工具

- [Android编译系统Jack](https://www.yuque.com/beesx/beesandroid/pembyq)
- [Android打包脚本Gradle](https://www.yuque.com/beesx/beesandroid/qsyn3s)
- [Android系统调试工具](https://www.yuque.com/beesx/beesandroid/mv93wu)

欢迎关注我们
