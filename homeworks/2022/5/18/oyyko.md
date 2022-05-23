线程安全：

指的是：当被多个并发线程反复调用的时候，会一直产生正确的结果。

不安全：

1. 不保护共享变量的函数
2. 保持跨越多个调用的状态的函数
3. 返回指向静态变量的指针的函数
4. 调用线程不安全函数的函数

## 可重入函数

特点：当被多个线程调用的时候，不会引用任何共享数据。

可重入一定线程安全

线程安全不一定可重入