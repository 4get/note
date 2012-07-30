Apple 使用 LLVM 在不支持全部 OpenGL 特性的 GPU (Intel 低端显卡) 上生成代码 (JIT)，令程序仍然能够正常运行。之后 LLVM 与 GCC 的集成过程引发了一些不快，GCC 系统庞大而笨重，而 Apple 大量使用的 Objective-C 在 GCC 中优先级很低。此外 GCC 作为一个纯粹的编译系统，与 IDE 配合很差。加之许可证方面的要求，Apple 无法使用修改版的 GCC 而闭源。于是 Apple 决定从零开始写 C family 的前端，也就是基于 LLVM 的 Clang 了。

http://www.oschina.net/p/clang

