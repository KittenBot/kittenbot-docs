# 05 使用Geekservo灰色舵机

## 接线

舵机有三根线，黄色线为信号线，红色线为电源线，棕色下为地线，接线方式如下图，我这里接在P1口，你如可以接在其他的IO口，但需要注意Microbit上的引脚复用IO

![](https://s2.ax1x.com/2019/09/02/nC8A61.jpg)

## 编程

用IObit控制舵机角度只能用脉冲的方法控制，600us为-45度，1500us为90度，2400为225度

![](https://s2.ax1x.com/2019/09/02/nPSU61.jpg)

注意：  
 
- 用IObit驱动Geekservo舵机是需要外接一个USB供电  
- 脉冲的功能只有makecode上有，所以是建议用makecode平台完成