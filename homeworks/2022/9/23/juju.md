### **\## 08-05-02-01接收信号的流程**

当内核把进程从内核模式切换到用户模式时，它会检查进程的未被阻塞的待处理信号的集合，

          如果这个集合为空，那么内核将**控制**传递到进程的逻辑控制流中的下一条指令。

          如果这个集合是非空的，那么内核选择集合中的某个信号并且强制进程接收信号，然后进程对信号会采取某种行为。一旦进程完成了这个行为，那么控制就传递回进程的逻辑控制流的下一条指令。 
内核控制进程对信号进行处理， 首先进行判断，如果带处理信号集合为空，内核会将控制转移到下一条指令。

           如果待处理信号集合不为空，那么内核操作进程对待处理信号采取某种行为，这种行为可能是忽略、终止、挂起信号。处理完这种信号后，接着将控制传递给逻辑控制流的下一个指令。

\-出处：《深入理解计算机系统》-P531 chapter 8.5.3