# the-difference-between-include-and-class-and-import
  
    @class解决循环引用的问题
    
    @class一般用于头文件中声明某个类的实例变量的时候用到.它只是声明,至于内部的实现是没有告诉编译器的. 那么要在. M 文件中使用的时候,还是要在.m 文件中@ import   (例如代理)
		
    #import 用于头文件不仅引用.同时将内部实现告诉编译器.这样子的话,最好不要再.h 文件中过多使用@ import,或造成编译时间过长,加重编译负担. (遵循代理协议)

    #include 基本跟# import一样,只是#import 不会导致交叉编译.
    
    (交叉编译:简单地说,就是在一个平台上生成了另一个平台的可执行代码.其实交叉编译是和嵌入式系统同步发展起来的)
