指令以寄存器作为目标时，对于生成小于8 字节结果的指令，寄存器中剩下的字节会怎么样
1. 生成1 字节和2 字节数字的指令会保持剩下的字节不变
2. 生成4 字节数字的指令会把高位4 个字节置为0
后面这条规则是作为从IA32 到x86-64 的扩展的一部分而采用的。