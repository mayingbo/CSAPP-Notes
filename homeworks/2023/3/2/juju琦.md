## 虚拟内存-缺页

DRAM缓存不命中称为缺页。 就是已分配未缓存的状态。例如：查找vp3缺页后，会触发一个缺页异常，
缺页异常会在主存中寻找一个牺牲页（pp3）,同时复制vp3(虚拟地址)到牺牲页pp3（物理地址），
并更新页表和返回。 当因为缺页而中断的程序接到这个返回后，重新执行这个程序。

书中 图9-6,9-7
