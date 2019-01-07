# IObit简介

## 购买链接

__转到淘宝购买__----------→[IObit](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4002-17001215033.32.1df7762exi5M0c&id=567838559503)

## 产品名称   
IObit，IO是指（input、output），IObit从名字可以看出，它主要是做引脚转出的作用，适合一些狂热的DIY爱好者，希望能自主使用所有IO口。   
## 适合人群   
已经对Microbit有所了解，也清楚Microbit的引脚定义，希望低成本做一些作品的用户。   

## 配送清单   
IObit X1   

## 产品简介   
这是一款Microbit低廉的扩展板，专门用于Microbit的IO口引出，已经将Microbit上所有io资源引出，同时板载上还自带蜂鸣器，通过跳线帽与P0引脚相连接，可以通过跳线帽对P0引脚进行释放。体积小，非常适合Microbit的小项目。   

## 产品特色   
- 体积小，非常适合DIY   
- IO口全部引出    
- 自带蜂鸣器，可以直接使用Makecode中的音乐模块播放音乐，无需外接喇叭   
- 带有乐高兼容的插销孔，与M3螺丝安装孔，方便固定扩展板   
- 以黄红黑区分的3PIN接口，特征明显不易插错，方便接插市面上的传感器    
- 喵家用心设计的丝印   

## 产品参数   
长x宽x高：57mmx37mmx12mm   
净重：16.4g   
![](./images/iobitSize.png)   

## 技术参数    
- 供电方式：供电从Microbit的usb口供入，或者Microbit的电池座供入   
- 工作电压：3V   
- 输出电流：40ma（不要用IO口驱动大电流器件，容易烧坏Microbit，如果要驱动大电流器件请使用RobotbitV2.0）   
- 串口引出：串口可进行IO口映射   
![](./images/40.png)   
- I2C口引出：19、20引脚只能作为I2C功能引脚使用，不能作为普通IO口读写，因为microbit底层写死了   
- spi口引出；14、15（IO口可读写）   

## 使用方式
编程方式：Makecode/Kittenblock(基于Scratch3.0)   
配合硬件：Microbit   
产品详细的学习资料地址：http://learn.kittenbot.cn/zh_CN/latest/mainboards/IObit%E7%AE%80%E4%BB%8B.html   

## 具体使用   
使用上与Microbit编程是一致的，因为本身IObit上没有带任何的驱动芯片（除了蜂鸣器）   
一般配合IObit来使用的积木块就是操作IO口，实际市面上很多传感器，都是返回一个高低电平，或者一个模拟值。或者是执行器，microbit需要输出高低电平。如果对此方面不熟悉的朋友，可以搜索网易云课堂 小喵科技，对应找到arduino的教程，里面大概解释了常用市面上传感器是怎么使用个，原理都是一样的。
### 配合常用积木块——引脚   
使用积木块前，必须先了解清楚你所用的电子模块的控制方式或者读取方式   
![](./images/35.png)   

### 数字读   
大部分新手都会掉坑掉在这里，因为他们经常在初始化的时候忽略了设置上拉或者下拉。所以电平状态读取一次后就失灵了。   
所以这里必须要注意下，microbit本身默认不帮忙设置上下拉，需要自己进行设置。
![](./images/36.png)   

### 模拟读   
对了应对模拟读，因为模拟读会返回0-1023的数值，用点阵屏显示总是会不方便。所以这里利用了小喵家出品的Makecode离线版特有的串口调试功能
![](./images/37.png)   

### 数字写   
数字读这里无需设置上下拉   
![](./images/38.png)   

### 模拟写   
模拟写一般会用到循环结构体   
![](./images/39.png)   

常用IO口操作就是这4种，大家掌握好后，应对市面上常用传感器没有问题。另外一个要注意下，市面上传感器有5v和3.3V兼容的。但是有一部分只能工作在5V中。例如淘宝卖得很烂那种蓝色超声波，只能工作在5V中，如果接上IObit，读回来的数字永远为0，因为模块没有正常工作！   


## IObit硬件介绍：
[![CQwl1e.jpg](https://s1.ax1x.com/2018/04/23/CQwl1e.jpg)](https://imgchr.com/i/CQwl1e)
### 电源指示灯
如果Microbit的usb口插上数据线供电后，指示灯亮红色，没供电不亮灯

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
如果你Microbit还没入入门,先入门Microbit，这个是操作前提。小喵科技已经为你准备好贴心的[Microbit手把手入门视频教程](https://bbs.kittenbot.cn/forum.php?mod=viewthread&tid=201&highlight=Microbit%2B%CA%D3%C6%B5)

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
 - 如果使用引脚的高低电平读的功能，必须设置引脚上下拉   
![](./images/36.png)   
 - 如果把P0作为普通IO口使用必须拔掉跳线帽，否则蜂鸣器会响或者IO读取数值不正常
 - 供电建议从Microbit的usb口进行供电，或者Microbit上的3V电机座接口。IObit上的3.3V与GND最高只能外部接3.3V电源
 - 使用与Microbit点阵的共用引脚（如3、4、5、6、7、8、9、10、11），记得在软件上把点阵屏禁用掉，否则会有点阵屏乱亮的现象
 - 不要使用IO19、20，19和20是不能当做IO口来使用的，虽然makecode软件上显示可以使用，实际是用不了的！只能用于I2C通讯
 - IObit供电上不能使用3.7V锂电池包，**插上去一定会把Microbit烧坏**
 - **禁止放在金属制品上使用，以免短路**