# Bridge

![](Bridge/01.png)



![](Bridge/02.png)



## 简介

Bridge是喵家推出一个款D51高性能主控板，它具有UNO的外形与引脚排布，板子尾部还带有类似Microbit的金手指，可插在Microbit相关的扩展板（Robotbit、IObit）进行使用。

软件上，它可以在Aruduino IED、Makecode Arcade平台、Makecode Maker平台上使用，支持图形化编程与MicroPython编程，因此取名为Bridge(桥)，连接各个平台的桥梁。





## 技术参数

主控芯片：ATSAMD51J19  ARM Cortex-M4

板子尺寸：77.8x53.3mmx13mm

重量：26.5g

自带传感器：

- 光敏传感器
- 温度传感器
- 加速度传感器 
- 可编程RGB灯（芯片脚PB22）
- 可编程LED（13脚）

2MByte SPI FLASH

2.54mm排针排母接口编程口

Microbit金手指可编程接口

机械安装孔位：符合UNO安装孔的形状尺寸与位置尺寸，直径3的通孔



## 供电方式

USB供电：5V，最大驱动电流1A

DC电源供电：6-12V，最大驱动电流3A



## 接口说明

Microbit金手指接口

数字IO口：D0-D13、A0-A5

模拟IO口：A0-A5  

20路PWM

1个SPI接口

1个SWD接口

1个SD卡槽

1个kittenbot wifi接口

![](Bridge/03.png)

![](Bridge/04.png)



## 特色

引脚接口和板子形状尺寸兼容UNO，支持UNO的扩展板

支持多个平台编程，Makecode Arcade平台、Makecode Maker平台Aruduino IED上使用

加上Arcade Shield可扩展为 Arcade平台的游戏机

以U盘形式进行下载，下载方便

支持MicroPython编程



## 编程平台

暂时推荐使用Makecode Arcade平台，使用方式与喵比特一致，点击下载时，选择D5主控板，如图

https://arcade.makecode.com/#editor

![](Bridge/06.png)



maker makecode平台

http://maker.kittenbot.cn/



新建项目，选择Kittenbot-Bridge板子

![](Bridge/07.png)



编程界面如下

![](Bridge/08.png)



这里编写了一个控制板子自带的RGB灯的程序，点击下载即可。

![](Bridge/09.png)



## Arduino 使用

待续~

心急的用户可以参考Arduin的D51板子使用

https://learn.adafruit.com/adafruit-metro-m4-express-featuring-atsamd51/setup