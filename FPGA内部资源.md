组合逻辑的选择器，比较器之内的电路会根据其输入输出的功能生成对应的查找表（look up table），查找表又是什么？简单的我们可以理解为数字电路里面的真值表，也就是你只需要关心它的输入输出，不会去管这个中间经过了多少运算。最后根据查找表取出对应的结果就可以。这就是我们最常用的可配置逻辑块了。  
FPGA内部的RAM，我们IP核调用的RAM的属于BRAM，我们用的寄存器属于DRAM。
在complier中原语例话的时间比IP核消耗时间较少。因为verilogIP核由.v文件和.ngc文件构成。.v文件只是一些接口，实质内容存在于.ngc文件中，在综合编译过程中还要调用.ngc文件。浪费时间。

1.FPGA 是一堆晶体管，你可以把它们连接（wire up）起来做出任何你想要的电路。它就像一个纳米级面包板。使用 FPGA 就像芯片流片，但是你只需要买这一张芯片就可以搭建不一样的设计，作为交换，你需要付出一些效率上的代价
它实际上是一个通过路由网络（routing network）连接的查找表 2D 网格，以及一些算术单元和内存。FPGA 可以模拟任意电路，但它们实际上只是在模仿，就像软件电路仿真器模拟电路一样。
https://www.cs.cornell.edu/~asampson/blog/fpgaabstraction.html
