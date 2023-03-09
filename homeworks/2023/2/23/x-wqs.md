分配器的要求和目标：
显示分配器必须要在相当严格的约束条件下工作：
处理任意请求序列，立即响应请求，只使用堆，对齐块，不修改已分配的块。
目标1：最大化吞吐率。目标2：最大化内存利用率。

造成堆利用率低的主要原因是：碎片现象。当虽然有未使用的内存但不能用来满足分配请求时，发生这种现象。有两种：内部碎片和外部碎片。
一个块是有一个字的头部、有效载荷，以及一些额外的填充组成的。头部编码了这个块的大小，以及这个快是已分配还是空闲的（a=1,0)