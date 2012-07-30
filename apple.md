
# mac os x

## Mac OS X 背后的故事（一）

http://www.douban.com/group/topic/23658084/

1. [（一）力挽狂澜的Ellen Hancock](http://www.programmer.com.cn/6727/)
- Ellen Hancock让苹果放弃Copland转而购买NeXT的关键人物。
- 20世纪80年代，卖可乐的John Sculley成为Apple的CEO，随之Steve Jobs被轰出Apple。
- 短期目标， 长期目标，在可预见的未来都无法实现的长期的目标。
- Mac OS的开发团队马上就被分成两个组，一个叫蓝组，目标是在1991年，发布一个关于Mac OS的更新版本；另一个叫粉组，和蓝组同时工作，计划在1993年，发布一个全新的操作系统。
- 和IBM合作的Taligent项目
- Copland将使用微内核技术，只做任务和内存分配。
- Mac OS的所有用户界面功能将成为一个独立的框架，称为蓝盒（Blue Box）
- Tanenbaum-Torvalds笔战
- 类似Mach微内核的系统往往难产，GNU/Mach + Hurd之类的项目做到现在经过了20年，仍未成事
- Apple几乎所有开发组的成员都来添乱。大家都说自己做的东西很重要，一定要加入Copland开发组，使Copland成为一个无法维护的项目。
- Steve Jobs把信得过的人（很多是前NeXT员工）拉拢到周围，开始新政，而同Gil Amelio有关的Ellen Hancock则在人事变动中被疏远。

1. （三）Mach之父Avie Tevanian
- 20世纪90年代末Apple都没有做出内存保护技术
- Mach是一个受Accent启发而搞出的Unix兼容系统。
- IOKit其实就是个DriverKit的翻版。
- Universal Binary技术，可以一个Mach-O文件同时包含Intel和PowerPC的指令。
- 1996年，Apple和OSF曾经合作，把Mach移到PowerPC Mac上，再把Linux作为单一的服务跑在Mach上，这个项目叫做MkLinux。
- PowerPC版的Mach被叫作osfmk分支，也正是现在Mac OS X中用的分支。
- 库：libkern libsa pexpert 
- Mac OS X的内核完全形成，形成BSD、IOKit、Mach osfmk三足鼎立的态势，并有pexpert、libkern、libsa作为基础。Apple称它的内核杰作为XNU。 http://www.opensource.apple.com/source/xnu/xnu-123.5/

1. （四）政客的跨界 
- 纪录片《An Inconvenient Truth》（《难以忽视的真相》）
- 苹果公司向来重视演讲，也是各大企业中最会通过演讲来营销产品的公司。

1. （五）Jean-Marie Hullot 的天才天才發明 Interface Builder 
- SOS，用Lisp语言编写，ExperTelligence开发了一种叫做ExperLisp的方言，SOS即用此语言写成
- http://en.wikipedia.org/wiki/Interface_Builder
- 在NeXT工作期间，他使用Objective-C和NeXTSTEP框架重写了SOS，命名为Interface Builder。
- 开发者拖拽鼠标，将控件可提供的动作（IBAction）和另一个对象的接口（IBOutlet）连在一起， 则建立了一个绑定。
- Interface Builder和Cocoa可以比后来出现的Microsoft Visual Studio或Qt Designer等软件走得更远——只要是对象，Interface Builder就能够操控它们，不需要一定是一个界面的控件。
- http://www.youtube.com/watch?v=j02b8Fuz73A

1. （六）Cordell Ratzlaff 引发的 Aqua 革命（上）
- Aqua是Mac OS X Public Beta全新用户界面
- 不思进取
- 界面语言不明确

1. （七）上善若水下﹣﹣Cordell Ratzlaff 引發的 Aqua 革命 
- 设计其实是有关产品如何工作的学问
- 防止窗口或其他界面元素的堆积 Exposé Dock Mission Control
- “最大化”一个窗口没有实际意义，Mac OS X没有所谓的“最大化”，取而代之的是自动计算后调整窗口到所需大小的“最适化按钮”。
- 关闭一个窗口的含意也不该是关闭一个程序，而只应是结束目前的内容。
- 继李维《Borland 传奇》
- 吴军《浪潮之巅》

1. （八）三好學生 Chris Lattner 的 LLVM 編譯工具鏈 
- [llvm]()

1. （九） ﹣﹣ 半導體的豐收上
- Andy-Bill定律，分别以Intel和Microsoft总裁的名字命名
- NeXT的Mach内核所支持的Mach-O二进制文件格式引入了一种叫fat binary的特性，说白了就是在一个平台架构上分别交叉编译所有平台的二进制格式文件，然后把每个文件都打包成一个文件。
- Mac OS X 10.4最终支持四个平台的BSD系统调用——32位Power PC、64位PowerPC、32位 x86和64位x86_64。
- 发者用Carbon迁移老程序，用Cocoa开发新程序
- 苹果向64位处理器的迁移花了整整6年时间,4个发行版

1. （十） ﹣﹣ 半導體的豐收中
- 开机按住6和4强制加载64位内核
- GCD和传统线程—锁机制的区别来了。传统的方式按劳分配，强调程序自由独立地管理，妄想通过“无形的手”把系统资源平均分配，走的是资本主义市场经济的道路。而GCD按需分配，真正实现了社会主义计划经济管理模式。
- 分配管理线程的运行库libdispatch
- 很多开发者亲切地称呼块语法的C扩展为“带lambda的C”。
- GCD支持的Ruby 实现MacRuby就能在多核处理器上高效执行

1. （十一） ﹣﹣ 半導體的豐收下 
- 图像处理有时需要对着色器进行编程以实现一些特效
- 流体力学. 它是用纳维斯托克斯方程【注：把牛顿第二定律和质量守恒应用到流体后，所得到的偏微分方程】
- 皮克斯动画工作室的《寻找尼莫》中的海洋流动和水花等，都是使用纳维斯托克斯方程来模拟的。
- 对于一个几何空间进行网格化，每个网格中的流体，都可以列出纳维斯托克斯方程，把这些方程联立起来进行求解，即可得到各点的温度、压力、湿度、速度等流体信息。
- Mark Harris《GPU Gems》
- GPGPU （General Purposed Graphics Processing Unit）
- 新一代的语言对比Cg，去掉了对于渲染相关的知识要求，独立于图形学之外，是纯粹的普通语言，比如变量不再是像素、顶点、面等类型，而是C/C++语言开发者喜闻乐见的浮点数组、整形数组等。
- CUDA（Compute Unified Device Architecture）
- ATI Stream SDK
- OpenCL （Open Computing Language）
- 苹果在借鉴他人技术并把他人技术改得更棒这一点上是出了名的
- 我用OpenCL编写科学计算程序时，大量时间是在重启电脑而不是写程序。


