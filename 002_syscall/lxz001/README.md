## 说说你对系统调用的理解？

答：系统调用是系统整合硬件功能，提供给我们操作硬件的接口，而避免直接操纵硬件的复杂操作。

## Linux 平台 x86 架构的系统调用指令是什么？x64 呢？Arm 架构 Linux 平台的系统调用指令是什么？

答：Linux 平台上，x86 架构系统调用指令是 `int 0x80` 还有`sysenter`指令，x64是`syscall`,
Arm是`svc`。

## 你还能列举几个系统调用的例子出来吗？你是从哪里找到它们的？

答：比如 `close``stat``fstat`,在系统调用表。

## `open` 函数的系统调用号是多少？`read` 呢？你是从哪里找到它们的？

答：在x64架构,`open`是2，`read`是0。在系统调用表。
    在x86架构,`open`是5，`read`是3。

## `malloc` 是系统调用吗？为什么？

答：不是，它是封装好的函数，通过`brk``mmap`系统调用去获取内存。

## 你使用什么命令来查看系统调用的文档？

答 ：less /usr/include/asm/unistd_64.h 查看x64的全部系统调用对应的系统调用号，
     man 2 name  查看单个系统调用，

## 你觉得学习系统编程会对你有何帮助？

答：我可能以后是做这个，靠这个吃饭，如果不做这个，也是知识储备，更多的了解操作系统