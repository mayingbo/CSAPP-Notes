## P364-368
循环寄存器之间的操作链决定了限制性能的数据相关。

数据流表示中的关键路径只是提供了程序需要周期数的下界。

延迟界限是基本的限制，决定了我们的合并运算能够执行多快。

循环展开：通过增加每次迭代计算的元素数量，减少循环的迭代次数。

对于整数加法，CPE有所改进，得到的延迟界限是1.00。得益于循环开销操作。相对于计算向量和所需要的加法数量，降低开销操作的数量，此时，整数加法的一个周期的延迟	成为了限制性能的因素。其他情况没有性能提高，已经达到了其延迟界限。