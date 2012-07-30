
clang c语言前端
llvm-gcc

成功的关键是性能和适应能力

http://www.drdobbs.com/architecture-and-design/the-design-of-llvm/240001128

1. [Mac OS X 背后的故事（八）三好学生Chris Lattner的LLVM编译工具链](http://www.programmer.com.cn/9436/)
- 编译器已经学会了上面所介绍的内存管理规则，会自动在编译程序时把这些代码插进去。
- LLVM作者 Chris Lattner ()
	- 他的硕士毕业论文提出了一套完整的在编译时、链接时、运行时甚至是在闲置时优化程序的编译思想，直接奠定了LLVM的基础。
	- 2000年LLVM开始开发，2005年Apple雇了Chris Lattner
	- GCC的代码耦合度太高，不好独立，而且越是后期的版本，代码质量越差
	- Mac OS X 10.6 Snow Leopard 完全得益于LLVM的技术
	- Grand Centrual Dispatch所用到的“代码块”语法， 这被很多人看作是带lambda的C
	- LLVM自身的新前端——Clang
	- 错误提示更精确
	- 既然你能发现我漏写了release，你为什么不能帮我自动加上呢？于是ARC被集成进Clang
	- 原生支持调试多线程程序的调试器LLDB
	- C++0x标准
	- libc++则原生支持C++0x
	- BSD代码整体要比GNU的高一些，GNU代码永无休止地出现各种严重的安全问题
	- GPL协议第三版发布时，和FreeBSD的协议甚至是冲突的。这也正是为什么FreeBSD中包含的GNU的C++运行库还是2007年以GPLv2发布的老版本，而不是支持C++0x的但依GPLv3协议发布的新版本。
	

1. [Linus Torvalds的短视](http://www.programmer.com.cn/6617/)
- Apple重要的是利益而不是折腾，即使是开源也是利益驱动。
- 像类似Linux开发组那样自以为是但代码又写得差的开源项目，Apple事后也遇到不少，比如GCC编译器项目组[1]。虽然大把钞票扔进去，在先期能够解决一些问题，但时间长了这群人总和Apple过不去，并以自己在开源世界的地位恫吓之，最终Apple由于受不了这些项目组人员的态度、协议、代码质量，觉得还不如自己造轮子来得方便，因此Apple推动了类似LLVM这样宏伟的项目，并且在短短几年内，使其成为最领先的开源软件技术。这无异于扇了Linux小组、GCC小组一记响亮的耳光。

1. 2007-07-25-LLVM-2.0-and-Beyond.pdf
	
