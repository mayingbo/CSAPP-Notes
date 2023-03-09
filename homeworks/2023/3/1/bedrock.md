符号和符号表

每一个可重定位目标模块m都包含一个符号表，其包含定义和引用的符号信息：

由m模块定义而被其他模块引用的全局符号。全局链接器对应于非静态的C函数和全局变量。

由其他模块定义而被m模块引用的全局符号,也称之为外部符号。对应于其他模块定义的非静态的C函数和全局变量。

只能被模块m定义和引用的局部符号（非局部变量）。对应于m中带static属性的C函数和全局变量。