像Linux LD程序这样的静态链接器以一组可重定位目标文件和命令行参数作为输入， 生成一个完全链接的、、可以加载和允许的可执行目标文件作为输出。  
输入的可重定位目标文件由各种不同的代码和数据节组成， 每一节都是一个连续的字节序列。  

为了构造可执行文件， 链接器必须完成2个主要任务：

- 符号解析。 目标文件定义和引用符号，每个符号对应于一个函数，一个全局变量或一个静态变量（既C语言中任何以static属性声明的变量）。  
符号解析的母的是将每个符号引用正好和一个符号定义关联起来。
    
- 重定位。   编译器和汇编器生成从地址0开始的代码和数据节。  链接器通过把每个符号定义与一个内存位置关联起来，从而重定位这些节， 
然后修改所有对这些符号的引用， 使得它们指向这个内存位置。  链接器使用汇编器产生的重定位条目的详细指令，不加甄别地执行这样的重定位。
