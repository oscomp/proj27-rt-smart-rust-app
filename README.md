# proj27-rt-smart-rust-app
### 项目名称

在RT-Thread Smart上支持rust语言编写的用户态程序

### 项目描述

RT-Thread Smart（简称rt-smart）是适用于嵌入式平台的实时操作系统。

目前RT-Thread Smart的用户态应用程序只支持C/C++程序，它使用musl libc。而随着嵌入式生态的发展，我们认为在rt-smart上运行Rust语言的应用程序也是相当重要的。本项目旨在为rt-smart增加Rust语言用户程序支持。

### 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道

### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

蒋周奇（洛佳）
* github [luojia65](https://github.com/luojia65)
* email me@luojia.cc

### 难度

中等

### 特征

* rt-smart支持ARM Cortex-A9的QEMU版本
* 实现rt-smart的Rust语言支持

### License

* [Apache-2.0](https://opensource.org/licenses/Apache-2.0)

## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

### 第一题：Rust语言支持库

* 编译并运行rt-smart操作系统。编译一个最小的Rust语言程序，使之能在rt-smart操作系统上运行；
* 查阅rt-smart的文档和资料，了解其中可用的系统调用。查阅rt-smart与编译器有关的文档，了解rt-smart遵守的调用约定；
* 选择一个系统调用的模块，制作一个封装和处理这部分系统调用的库。依赖于这个库，用户可以编写应用于rt-smart操作系统的应用程序，并使用里面的系统调用。请参考[libtock-rs](https://github.com/tock/libtock-rs)。

### 第二题：制作一个到rt-smart的Rust编译目标

* 查阅Rust语言相关的资料，了解Rust语言目前支持哪些平台。Rust语言是否拥有面向嵌入式操作系统专门的编译目标？请举例；
* 作为一个独立的平台，rt-smart提供平台相关的开发方法。请为Rust编译器添加一个名为“aarch64-rt-smart”的编译目标。使用该目标得到的二进制程序，能直接应用到rt-smart支持的平台上；
* 请将第一题的成果视作标准库的一部分，选择一个系统调用的模块，为aarch64-rt-smart添加std标准库对应模块的代码。

### 第三题：Rust生态中的rt-smart平台

* 许多的库实现和平台有关系，这些库通常需要特定的操作系统功能支持。比如num_cpus，它在不同平台上调用不同的系统调用，达到列出CPU核数量的功能。查阅资料，列出几个这样的库。您可能需要浏览[crates.io](https://crates.io/)或[lib.rs](https://lib.rs/)。
* 选择一个Rust生态中的库，为其添加代码，使之能支持rt-smart操作系统的相关功能。
