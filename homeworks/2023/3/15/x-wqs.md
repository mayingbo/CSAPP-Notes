将变量映射到内存。
多线程的C程序中变量根据它们的存储类型被映射到虚拟内存：
全局变量，定义在函数之外的变量，运行时，虚拟内存的读写区域只包含每个全局变量的一个实例。
本地自动变量，定义在函数内部，但没有static，在运行时，每个线程的栈都包含它自己的所有本地自动变量的实例
本地静态变量，定义在函数内部有static，虚拟内存的读写区域只包含在程序中声明的每个本地静态变量的一个实例

当它的一个实例被一个以上的线程引用，称变量是共享的。

信号量，非负整数值的全局变量。P、V确保了正在运行的程序不可能进入一个状态，正确初始化了的信号量有一个负值。信号量不变性。确保对共享变量的互斥访问。将每个共享变量和一个信号量联系起来，用P、V操作将相应的临界区包围起来。互斥锁，P互斥锁加锁，V互斥锁解锁。生产者-消费者，读者-写者。基于预线程化的并发服务器，利用生产者-消费者模型降低开销。
