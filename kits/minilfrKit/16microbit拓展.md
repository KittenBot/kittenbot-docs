# 玩转microbit拓展编程  

miniLFR是一款Arduino小车，它能够使用kittenblock，Arduino IDE进行编程。顺应着目前的STEM教学潮流，microbit是一款更适合中小学学生学习的硬件，它在makecode平台的编程方式更更易理解。所以这款microbit Adapter将miniLFR和microbit紧密结合在一起。  

![](https://s2.ax1x.com/2019/09/06/nuqdP0.jpg)   


## 装配 

**准备材料** 

请自备螺丝刀  

![](https://s2.ax1x.com/2019/09/06/nuXEKU.jpg)  

**Step1：**  

车头部分，将前一排3根针脚对准插入，另外一列4根插针即随之插稳

![](https://s2.ax1x.com/2019/09/06/nujkFA.jpg)   

**Step2：**  

固定microbit，组装完成  

![](https://s2.ax1x.com/2019/09/06/nuxi8I.jpg)  

## 开始编程  

**Step1：准备miniLFR固件程序** 

由于miniLFR与microbit结合的编程，是以串口通讯的形式。也就是说，microbit编程只负责发固定的M串口指令给miniLFR，另外的执行程序就需要固定在miniLFR内部，此时只需要在kittenblock中恢复固件来将这个固定的通讯执行程序下载到miniLFR下。  

按照如下操作下载程序：  
- 首先连接USB与miniLFR  

![](https://s2.ax1x.com/2019/09/06/nKkHeI.jpg)

- 打开kittenblock并选择miniLFR2.0，连接串口 

![](https://s2.ax1x.com/2019/09/06/nKF4rn.jpg)  
![](https://s2.ax1x.com/2019/09/06/nKF75T.jpg)  

`如果你接上USB发现这里并搜不到串口，可能是没有串口驱动，按下面图示下载CH340串口驱动`  

![](https://s2.ax1x.com/2019/09/06/nKkFRe.jpg)  

- 点击恢复固件按钮下载固件程序到miniLFR 

![](https://s2.ax1x.com/2019/09/06/nKklRg.jpg)  

**Step2：microbit端编程** 

- 连接USB与microbit 

![](https://s2.ax1x.com/2019/09/06/nKALu9.jpg)  

- 结合microbit的编程我们在makecode上有插件支持。
    - 登录在线版[makecode](https://makecode.microbit.org) 
    - 或使用喵家离线版makecode  [点击下载](https://cdn.kittenbot.cn/makecode/makecode-v5%20Setup%203.6.0.exe)  

- 加载插件

![](https://s2.ax1x.com/2019/09/06/nKP9IS.jpg)  

插件地址：https://github.com/KittenBot/pxt-minilfr

![](https://s2.ax1x.com/2019/09/06/nKPZq0.jpg)   

- 认识积木块   

![](https://s2.ax1x.com/2019/09/06/nKKpdJ.jpg)  
![](https://s2.ax1x.com/2019/09/06/nKQnPA.jpg) 
![](https://s2.ax1x.com/2019/09/06/nKlEQ0.jpg)  

- 编程演示：microbit按键控制车头灯和RGB点亮 

![](https://s2.ax1x.com/2019/09/06/nKlIlq.jpg)   


## 扩展应用  

你可以使用另外一块microbit对其进行遥控，实现遥控小车的效果，同样也可以使用呱比特手柄提升遥控体验。  

`这里有2.4G无线遥控的体验程序可供下载`   [点击下载](https://cdn.kittenbot.cn/microbitEx/minilfr%E6%96%B0%E7%89%88makecode%E7%A8%8B%E5%BA%8F.rar)

## 注意：

- 编程时一定要将【初始化】积木块放在开机下 
- 如果发现其他步骤都没问题，下载了程序后操作没反应，试一下重开miniLFR电源  
















