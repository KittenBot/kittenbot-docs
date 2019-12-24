# Nanobit



## 简介

Nanobit是喵家推出一款兼容Makecode编程编程平台的mini主控板，主打DIY制作，因形状酷似Arduino的Nano板子，因此命名为Nanobit。

Nanobit可兼容市面上的Arduino Nano的扩展板，方便通用模块的插件，降低制作成本。

Nanobit中的编程下载器是与主板拼接在一起。在DIY制作作品完成后期，可以进行掰断分离处理，可以使作品电路更加小巧。



## 技术参数

Nanobit硬件参数主控芯片：nRF51822  ARM Cortex-M0

尺寸：18.3x75x17mm

重量：6.9g 



- 可编程资源：

  无线通讯，2.4G和蓝牙功能

  加速度传感器

  指南针传感器

  温度传感器

  可编程LED灯（P15）

  可编程A/B按键

  可编程IO口

  I2C接口



- 引脚排布兼容arduino Nano



- 支持USB 盘符形式下载程序



![](images/16.png)



## 供电方式

USB供电电压：5V

锂电池供电PH2.0接口：3.7-4.2V

Vin脚输入电压：3.3-5V

主控芯片工作电压：3.3V



## 接口说明

![17](images/17.png)



## 引脚说明



![](images/nano_4.png)



## 特色

- 兼容makecode平台的迷你主控板

- 采用常规的2.54间距的针脚形式，方便插接面包板与传感器

- 引脚兼容Nano板子，可以使用Nano的扩展板

- I2C接口兼容市面上常用的OLED引脚顺序，即插即用

- 带锂电池接口，可插接常规锂电池

- 主板与编程下载器采用可掰断设计，降低用户制作成本。




## Nanobit VS Nano

|         Nanobit          |      VS      |       Nano       |
| :----------------------: | :----------: | :--------------: |
|   更简单易用的Makecode   |     平台     |    ArduinoIDE    |
|       自动识别U盘        |     驱动     | 需要安装串口驱动 |
|    蓝牙与2.4G无线功能    |   无线功能   | 无，需要自行扩展 |
|          AB按键          |   板载按键   | 无，需要自行扩展 |
| 有，软件有直接调用的积木 | 陀螺仪指南针 | 无，需要自行扩展 |
|            有            |  锂电池接口  |        无        |
|     串口引脚随便映射     |     串口     |     固定引脚     |

![](images/nano_5.png)



简单总结：Arduino Nano虽然便宜，但它仅仅只是芯片板子，你需要自己去扩展传感器。

而喵家的Nanobit集成度更高，手上门槛也更低，更适合普通用户。





## 编程平台

编程平台：**Makecode**

编程地址：https://github.com/KittenBot/pxt-nanobit



插件情况如图所示：

除了加载Nanobit的主插件，还自动加载OLED插件，Nanobit与Microbit相比缺少了5x5点阵，但预留I2C接口，使用OLED模块更加方便。

![](images/01.png)

![](images/02.png)



## 具体使用

### 插上Nanobit

![](images/05.png)



电脑会显示Nanobit的盘符。（首次插上会提示自动安装驱动，与Microbit类似）

如果无法显示,一般是**USB数据线或者电脑USB口不良导致**的，请自行更换USB线或者更换电脑进行尝试

![](images/04.png)

### 加载插件

打开Makecode，加载Nanobit插件，地址如下：

https://github.com/KittenBot/pxt-nanobit

除了点阵屏相关的积木块(点阵显示、光敏)，其它积木块的使用方式与Microbit使用的一致。

![](images/03.png)



### OLED屏幕显示

![](images/nano_6.png)



这里接了0.91寸的OLED（128x32像素）

![](images/07.png)



下载后的实物现象。虽然相比Microbit少了5x5点阵，但是插着OLED屏，你会感觉到OLED非常好用。再也不用等待字符串流动才能看到结果了。

![](images/06.png)



OLED分栏积木块介绍

![](images/18.png)



## 简单示例与现象

![](images/nano_7.png)

![](images/nano_8.png)

![](images/nano_9.png)



## 显示中文

众所周知Microbit里是没有中文字库，但是我们可以用取巧的办法，把字以图片的方式绘制出来后，显示在对应的位置上。



此实现需要MakecodeV5离线版本实现

加载Nanobit插件后



- 选择屏幕编辑器

![](images/nano_10.png)



- 输入你要的文字，一次只输入一个，别忘记渲染

![](images/nano_11.png)



- 点击生成，与返回

![](images/nano_12.png)



- 这里我编写了一个是显示中文与温度变量的程序：

编程不难，只需要理清字符之间的位置关系

![](images/nano_13.png)



### IO模拟读写

Nanobit的引脚定义与Microbit的引脚定义一致。可以直接通过引脚分栏，对IO进行数字与模拟读写。

Nanobit上有些引脚如Row3、Row2..等等，这些引脚在Microbit的引脚分栏中是没有的，大家需要注意下，我们挑一些有的引脚进行使用即可。

![](images/09.png)



引脚分栏如下：

![](images/10.png)



数字写，模拟读，模拟写，一般不会有什么问题。

新手需要注意的是，**数字读，需要设置上拉**（Microbit也是一样）

![](images/11.png)



我在P0口接了一个按键，当按键按下时，控制Nanobit上的Link灯亮。对应的程序如下：

**Nanobit上Link灯是接在P15**上

![](images/12.png)



## 插上Nano的扩展板

大家可能发现Nanobit的引脚排布比较乱，是因为它的体积限制，只能迁就PCB布线，不过这也算是一种Geek风格吧。为了方便大家引脚插件，我们做了Nano的IO扩展板的引脚映射。

![****](images/13.png)

使用这些积木块就感觉引脚排布舒服多了，因为底层进行了映射。切记数字读，还是需要设置上拉或者下拉。

另外,如果你配合nano的扩展板进行使用，模拟读需要注意下，如果给Nanobit供电，nano扩展板上的V只有2.7V，换句话说，即使电位器拧到拧到最大也不会出现255的数值。

![](images/14.png)



## Nanobit配合扩展板使用注意要点





因为喵家把Nanobit本身定位一个极客的主控板，因此没有特意给Nanobit做个专门的扩展板。但是我们可以用Arduino Nano的扩展板。由于Arduino Nano的IO电压为5V，因此使用上和喵家Nano（3.3V）稍有区别。

- 外部DC头插入的电压不能超过5V。注意Nanobit的板子IO电压为3.3V，如果你使用Nano的扩展板，外部DC头插入的电压不能超过5V，如果超过5V会烧坏Nanobit。

![](images/19.png)



- 如果配合扩展板使用，接入5V外部电源后，V的电压为5V

![](images/20.png)



- 扩展上读取模拟值，模块需要接3.3V，才能得到比较准确的值（Nanobit的模拟读电压基准就是3.3V）如图：
 ![](images/21.png)



- 使用扩展板5V供电时，请勿！请勿插上！Nanobit的锂电包，5V电源会直接供给锂电包，过压会导致锂电包直接进入保护模式。
![](images/22.png)







## 外接锂电池

推荐使用喵家锂电池包，带外壳完全可靠。（**锂电池包不能用于Microbit的电池接口，会烧坏Microbit**）

Nanobit上**没有集成锂电充电电路**，因此锂电包充电需要外部进行充电。可以用专用的锂电充电模块，或者你想简单点，可以直接用喵比特，喵比特上含有充电电路，可以给锂电包进行充电。

![](images/08.png)

![](images/15.png)

## 关于仿真器

仿真器是通用的cmsis-dap仿真器设备，自动usb串口设备功能。可用于一般通用开发，例如keil和gdb。
目前拖拽式下载功能只支持目标硬件nrf51822 (micro:bit的mcu)



## 仿真器引脚定义

![](images/24.png)



## 将仿真器与nanobit分离使用 

首先需要注意，要分离使用请确保手头有工具，需要**自行焊接排母** ，产品不含排母座

![](images/nano_1.png)  

准备2排排母，自行剪切处理如图焊接  

![](images/nano_2.png)   

按照如下方向插在nanobit的排针上，即可使用

![](images/nano_3.png) 

用于下载程序，供电以及复位程序都是OK的，下载完程序后可拔掉，单独给nanobit供电即可跑程序，另外仿真器请自行保管好。

