# Microbit&Robotbit巡线壁障小车说明  
  
## 材料  
  
- 钣金底座 x1
- 橡胶轮子 x2  
- Microbit x1
- Robotbit x1
- 18650电池 x1
- TT电机 x2
- 9g小舵机 x1
- 5路巡线模块 x1
- 猫头超声波 x1
- 转接板 x1
- 电路板支撑柱 x4
- 支撑柱螺丝 x4
- M3螺丝 若干
- M4螺丝/螺母 x2
- 万象轮 x2
- 杜邦线 若干
- 螺丝刀 x1

![](./images/cailiao_1.png)    
  
## 组合过程    
  
**零件拼装**  
 
1.将9g从背面顶上来，并用舵机包里的细长螺丝和螺母固定住  

![](./images/zuhe_1.png)  
  
2.将固定支架卡在舵机转头上，并随即测试②，③步骤的旋转极限角度是否相同，来保证①的位置处于居中的90度
   
![](./images/zuhe_2.png)    

![](./images/zuhe_3.png) 
  
3.取下支撑架子，与转接板用螺丝固定好 
  
![](./images/zuhe_4.png)    
  
4.将组合好的转接板插在舵机转头上，并用舵机包里的小螺丝拧紧固定
 
![](./images/zuhe_5.png)   
  
5.TT马达将螺丝从外部拧上，螺母在内部固定 
  
![](./images/zuhe_6.png)    
  
6.装5路巡线模块小技巧
  
![](./images/zuhe_7.png)  
  
![](./images/zuhe_8.png)  
  
7.装上两颗万向轮  
  
![](./images/zuhe_9.png)    
  
8.Robotbit的固定准备
  
![](./images/zuhe_10.png)  
  
![](./images/zuhe_11.png)  
  
**接线**  
1.猫头超声波接线    

![](./images/jiexian_1.png)    
  
2.3路巡线及其他接线
  
![](./images/jiexian_2.png)    
  
**整品展示**   
  
![](./images/b_show.gif)
  
## 编程  
  
**3路巡线编程**    
  
![](./images/x_chengxu.png)  
![](./images/x_chengxu2.png)  
  
**超声波避障编程**  
  
![](./images/c_chengxu1.png) 
![](./images/c_chengxu2.png)  
  
## 展示  
  
**3路巡线**   
  
![](./images/xunxian.gif)   
  
**超声波避障**  
  
![](./images/chaosheng.gif)  
  
## 巡线避障进阶  
  
**一键开启关闭小车&一键切换巡线避障功能**  
   
![](./images/jinjie1.png)  
![](./images/jinjie2.png)  
![](./images/jinjie3.png)  
![](./images/jinjie4.png)  

**注：**

- 一切准备就绪后，插上电池，你需要做的第一件事情就是激活电源 
![](./images/jihuo.png)   
  
- 关于TT电机的接线，当红对+/黑对-时，程序中给定速度为正数时轮子是顺时针转，而小车向前必须是右轮顺时针，左轮逆时针，但如果想让程序如下还能保持向前走，也就是必须要让其中一个电机反接。即右轮正接，左轮反接。

![](./images/tt_zhuyi.png)  

- 如果你发现你的小车不正常，请一定重新检查你的接线是否与上述一样，以及程序的设置是否相同     

- 当使用到P0脚时，一定要将旁边的跳线帽拔掉并妥善保管，因为P0是跟蜂鸣器复用的  

如果上述提示都无法解决你的问题，请加入小喵科技QQ交流群：568084773咨询
  


  
