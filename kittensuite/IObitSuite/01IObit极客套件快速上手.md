# 01 IObit使用说明

IObit扩展板将Microbit上的所有IO口都引出来，但由于Microbit上的引脚与点阵屏，蜂鸣器，按键复用，所以如果想用Microbit上的所有引脚，就意味着这些复用的功能就无法使用，具体引脚的复用功能见下图

![](https://s2.ax1x.com/2019/09/02/nC36Fe.jpg)

P3,P4,P6,P7,P9,P10与点阵屏上的LED灯复用

P5,P11与Microbit上的A,B按键复用

P19,P20为I2C接口，不可做普通IO用

P13,P14,P15与SPI接口复用

P0与蜂鸣器复用

以上的复用引脚意味着两个功能只能2选1，

如果要选用与LED点阵复用的引脚，那么就需要关闭LED点阵

![](https://s2.ax1x.com/2019/09/02/nC3gWd.jpg)

另外P0,P1,P2,P3,P4,P10为模拟IO口，可读写模拟传感器

