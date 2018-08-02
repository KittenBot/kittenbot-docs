# 多脚兽说明  

## 适用人群 

小学生/家长/爱好者

## 配送清单

原装风能怪物一盒    

喵家风能怪物打印件一套   
 
MICROBIT X 1    

ROBOTBIT X1    

18650锂电池 X1  

TT马达电机（焊接好线） X2  

乐高插销 X4  

TT马达安装螺丝M3x25 X4  

自攻螺丝十字圆头带垫M2.3x8 X14  

喵家螺丝刀 X1  
 
## 产品简介

曾经荷兰人发明的风能怪兽携机械美和风能驱动的特色突然出现在人们的视野，但因其过于庞大的体型，仅仅在留下了惊叹和羡煞后便淡出了视线。直到如今我们认为这种创意的消逝实在可惜，它那完美的机械联动若能不受风能驱动所必要的体型要求拘束，而是配上电控的主流，再重回人们的视线，不仅传承这种美也一并结合编程的创客思维，让你能在体验到趣味的基础上培养编程逻辑，那这款全新的多脚兽产品是在适合不过了。


## 产品特色

- 图形化编程趣味编程
- 机械设计美学
- 自制diy锻炼动手能力
- 掌握齿轮联动原理

## 产品参数

长x宽x高：  225mm x 160mm x 180mm

净重： 262.6g

毛重：根据包裹最终大小决定

## 技术参数

- 电压：额定5V
- 电流：1A
- 板载全彩可编程RGB灯
- 可编程蜂鸣器
- 18650-3.7V可充锂电池

## 组合过程

1.关键部分，此处原本相接固定，后期应剪掉凸出部分与图中保持一致  

![](./images/p1.png)   
  
2.按图组装喵家风能怪物打印件    

![](./images/p2.png)
![](./images/p3.png) 
   
3.将组装好的打印件与机械支架组合并固定    

![](./images/p4.png)
![](./images/p5.png)   
 
4.给TT电机安装插销  

![](./images/p6.png)
![](./images/p7.png)   
 
5.TT电机固定到支架上  

![](./images/p8.png)
![](./images/p9.png)    

6.LEGO插销固定到robotbit支撑台的平面一侧，支撑台卡主机械支架中心并固定  
 
![](./images/p10.png)
![](./images/p11.png) 
   
7.TT电机与Robotbit接线如图     

![](./images/p12.png)
![](./images/p13.png)  
  
8.Robotbit和支撑台的组装如图  
   
![](./images/p14.png)  
    
9.完成——成品展示  
  
![](./images/p15.png)    

## 使用环境

编程方式：Kittenblock(基于Scratch3.0)/Makecode可连接硬件：Microbit


## 使用方法  

- 编程方式：Kittenblock(基于Scratch3.0)/Arduino/Makecode
- 兼容硬件（配合硬件，或者配套什么使用）：可配合两块microbit通过2.4G通讯使用
- 小喵教程集合地址：learn.kittenbot.cn
- 小喵论坛地址：kittenbot.cn/bbs
- 网易云课堂：搜索小喵科技
- 更多的实时讨论，请加入爱上小喵科技官方Q群：568084773

以下使用的是小喵科技出品的离线版Makecode无需网络    
(Makecode+Robot:bit extension package)

![](./images/dm1.png)

下载链接：[http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=156&extra=page%3D1](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=156&extra=page%3D1)
    
要使用TT电机编程，需要先在Makecode上安装Robotbit插件，安装方法如下：
如图先在设置中找到添加包，找到robotbit单击即可    

![](./images/dm2.png) 
![](./images/dm3.png)  

加载完后我们可以看到2组新增的编程积木    

![](./images/m4.png)    


**简单的向前走**

按照上述接线图解法。从Robotbit中拉出电机积木块   
 
![](./images/m5.png)    

点图中标识部分选择下拉框按如图选择   
 
![](./images/m6.png)  

**有趣的玩法（基于2.4G控制多脚兽运动，需要两块microbit)**  

从Radio中拉出如图所示积木块，并保持默认值1，并放置在开始执行下用以初始化    

![](./images/m7.png)
![](./images/m8.png)     
   
分别从Input、Radio中拉出积木块并组合起来

实现效果：按下microbit上A按钮通过2.4G发送字符串A  
 
![](./images/m9.png)
![](./images/m10.png)
![](./images/m11.png)   
   
如图步骤取出积木块    

![](./images/m12.png)
![](./images/m13.png)
![](./images/m14.png)
![](./images/m15.png)    

准备好上述积木之后，配合之前已经熟悉过的电机积木块，组成如下图的程序块   

![](./images/m16.png)    

综上，下图所示就是一个简单的2.4G控制多脚兽向前走的一个小例子    

![](./images/m17.png)    

使用上述技巧，可以拓展多个方案  
实现效果：按下A（前进）；按下B（后退）；A、B同时按下（停止）；控制端microbit左倾斜、右倾斜分别实现左转右转  
    
![](./images/m18.png)    

上述程序中的倾斜事件积木块如下   

![](./images/m19.png)
![](./images/m20.png)    

## 展示 
  
![](./images/s1.png)    

## 注意事项

- 多脚兽机械零件拼装中一定要确保两部分合并时三脚架底边中间突出部分不相连  
- TT电机接线必须按照范例，如需更改自行修改程序，请确保使用同一组接口如A+/A-  
- 电机要运动起来speed绝对值最好在50-255间，且越大越快  
- 2.4G的玩法需要两个microbit实现  
- 更多的有关资料及有趣玩法请参照：  

Robotbit：[http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=114&extra=page%3D1](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=114&extra=page%3D1)  

Microbit： [http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=104&extra=page%3D1](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=104&extra=page%3D1)

_本产品只适用于14岁以上的儿童进行独立使用，8~14岁儿童请在家长或者老师的陪同下进行使用。
如使用前请按照小喵官方资料指导下进行使用，不要随便接插电路，切勿外接大电流舵机，大电流电机，以免烧毁电路板。
注意不要在金属表面，或者导电的物体上使用，以免短路
请避免在潮湿和有水的地方使用，以免短路
电路板或者机械上含有细小物件请不要吞食，请放在儿童接触不到的地方妥善保管_