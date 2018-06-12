# IObit简介

![](./IObit.jpg)


## IObit硬件介绍：
[![CQwl1e.jpg](https://s1.ax1x.com/2018/04/23/CQwl1e.jpg)](https://imgchr.com/i/CQwl1e)
### 电源指示灯
Microbit上供电，指示灯亮红色，没供电不亮灯

----------

### P0蜂鸣器跳帽
跳帽IObit默认是插上的，在Makecode中使用音乐分栏积木即可进行编程，发出声音，平时上电是不会有声音的

跳帽旁边的小黑块是一个无源贴片蜂鸣器


----------


### 3Pin IO口引出
已经将Microbit中所有引脚引出，没有任何保留（PS：Microbit上没有P17与P18，并不是IObit没有引出）

黄色对应不同的IO引脚

红色对应3.3V

黑色对应GND


----------


### 40P Microbit卧式插座
体积紧凑型插座

----------


### 板子安装孔与固定孔
最外侧两个孔直径大概4.8MM，兼容乐高摩擦销，间距48mm
最内侧两个孔直径大概3.1MM，可用普通M3螺丝拧紧，间距大概32mm

----------


### 板子背后有丝印
详解解释了每个IO口复用了一些功能
[![CQwQpD.jpg](https://s1.ax1x.com/2018/04/23/CQwQpD.jpg)](https://imgchr.com/i/CQwQpD)
[![CNVLZT.md.jpg](https://s1.ax1x.com/2018/05/04/CNVLZT.md.jpg)](https://imgchr.com/i/CNVLZT)
----------


## IObit编程使用：
如果你Microbit还没入入门,先入门Microbit，这个是操作前提。小喵科技已经为你准备好贴心的[Microbit手把手入门视频教程](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=201&highlight=Microbit%2B%CA%D3%C6%B5)

### P0蜂鸣器
在Makecode中直接使用音乐积木块即可
![CQ0056.png](https://s1.ax1x.com/2018/04/23/CQ0056.png)

### P0引脚使用
如使用P0记得拔掉跳线帽（可以将跳线帽插一边，防止丢了）
[![CQ0dV1.jpg](https://s1.ax1x.com/2018/04/23/CQ0dV1.jpg)](https://imgchr.com/i/CQ0dV1)

### IO口释放
这里写了两个示例：
模拟读写：
P1接了一个旋钮电位器（你也可以接任意的模拟传感器）
P16接了一个9g舵机（注意舵机接线）
实验现象：
拧动P1的电位器，P16的舵机会对应转动角度
[![CQ0UbR.png](https://s1.ax1x.com/2018/04/23/CQ0UbR.png)](https://imgchr.com/i/CQ0UbR)

数字读写：
P9接了按键模块（测试数字读）
P3、P4、P6分别都接了LED灯（测试数字写）
实验现象：
按键P9的按键模块（或者Microbit上的A键B键），可以看到P3、P4、P6的灯分别切换亮
[![CQ0wUx.png](https://s1.ax1x.com/2018/04/23/CQ0wUx.png)](https://imgchr.com/i/CQ0wUx)

### 如何使用5V电子模块
标号1为5V电子模块
标号2为5V电源（或者任意板子上的5V电源）

**只需要共地即可，注意灯泡那根黑色线**

![CQBAd1.jpg](https://s1.ax1x.com/2018/04/23/CQBAd1.jpg)

## IObit使用注意事项

 - IObit的IO口驱动能力很弱，IO口电流不足200ma，请勿接大电流器件（例如大舵机MG995、直流电机），**否则会烧坏Microbit**，使用前必须完全了解清楚你所使用的器件电流情况
 - IObit只能驱动1路9g小舵机，2路以上会发抖（电流不够），如果你想驱动多路9g舵机，请选择Robotbit，自带驱动芯片，驱动能力足 [Robotbit购买地址](https://item.taobao.com/item.htm?spm=a230r.1.14.14.1b224327xxF4Jq&id=559862615142&ns=1&abbucket=4#detail)
 - 如果把P0作为普通IO口使用必须拔掉跳线帽，否则蜂鸣器会响或者IO读取数值不正常
 - 供电建议从Microbit的usb口进行供电，或者Microbit上的3V电机座接口。IObit上的3.3V与GND最高只能外部接3.3V电源
 - 使用与Microbit点阵的共用引脚（如3、4、5、6、7、8、9、10、11），记得在软件上把点阵屏禁用掉，否则会有点阵屏乱亮的现象
 - 不要使用IO19、20，19和20是不能当做IO口来使用的，虽然makecode软件上显示可以使用，实际是用不了的！只能用于I2C通讯
 - IObit供电上不能使用3.7V锂电池包，**插上去一定会把Microbit烧坏**
 - **禁止放在金属制品上使用，以免短路**
