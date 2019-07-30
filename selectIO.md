http://xilinx.eetrend.com/d6-xilinx/article/2017-11/12257.html
在FPGA IOB内部，Pad输出之前，内置上下拉电阻。且可以通过Passive Pull-up/Pull-down模块控制两个MOS管的导通与否来控制是否使能上下拉电阻。  
内部连接Pad的分别有一个Input Buffer和Output Buffer。其中Input Buffer对外应该始终呈现高阻状态，同时可以将Pad上的电平通过Input Buffer传到I1和I2，或者是下部的FF。Output Buffer有两个控制信号，分别是Slew Rate Control，用来控制输出信号的Slew Rate；另一个是三态控制信号T，可以控制Output Buffer输出高阻。

内部输出信号Out，可以通过上半部分的FF，经Output Clock同步后打出，也可以直接连接到Output buffer的输入端，直接输出。

同样Input Buffer的输出，可以直接连接到I1和I2，也可以经过下半部分的FF，经过input clock的同步之后输出到内部总线上。
