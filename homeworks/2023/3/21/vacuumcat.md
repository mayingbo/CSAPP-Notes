4.5.8 流水线控制逻辑
逻辑必须要处理四种情况：加载/使用冒险，处理ret，异常，预测错误的分支。
1. 特殊控制情况所期望的处理
加载使用冒险的情况比较简单，只需要处理mrmovq和popq两种情况即可。当这两条指令任意一条处于执行阶段，并且需要该目的寄存器的指令正处于译码阶段时，我们要将第二条指令阻塞在译码阶段，并在下一个周期插入一个气泡。这个重点在于发现冒险的情况。
ret指令则是停顿三个周期。
至于处理异常的情况，可以看图4-63，通过插入气泡，暂停指令，可以让异常指令之前的指令都完成，而后面的指令对程序员可见状态没有影响。
2.发现特殊控制条件
略。
3. 流水线控制机制
暂停与气泡的区别，暂停是停止更新状态，气泡相当于nop
4.控制条件的组合
略。
p319
