# Robotbit绘图小车说明

#材料

- 钣金底座
- 28byj步进电机 x2
- 轮子 x2
- 万向轮 x2
- Robotbit x1
- Microbit x1
- 螺丝刀 x1
- 电路板支撑架/塑料螺丝 x4
- 卡笔环
- 螺丝/螺母若干


![](./huitu/huitu_cailiao.png)

#组合过程

1.步进电机的固定

![](./huitu/bujin_guding1.png)

![](./huitu/bujin_guding2.png)

2.轮子安装

![](./huitu/lunzi.png)

3.万向轮安装

![](./huitu/wanxiang_guding1.png)

![](./huitu/wanxiang_guding2.png)

4.控制板固定

![](./huitu/guding_2.png)

![](./huitu/guding.png)

5.接着将卡笔装置压进钣金底座

![](./huitu/kabihuan.png)

__接线__

![](./huitu/jiexian_1.png)

__安装好的整体__

![](./huitu/zhengti.png)


## 编程

__简单绘图小车编程__

首先导入Robotbit软件包

![](./huitu/daobao.png)

使用如图积木块对绘图小车进行编程，一般只用到最后2个

![](./huitu/biancheng_huitu.png)

__蓝牙控制绘图小车__

1.microbit上按照如下说明按需求烧录程序

- 由于蓝牙和Robobit带RGB灯的拓展包冲突，所以使用添加如下包

_https://github.com/KittenBot/pxt-robotbitnopixel_

![](./huitu/lanyazhunbei_1.png)

- 添加蓝牙包

![](./huitu/lanyazhunbei_2.png)

- 更改蓝牙设置（这一步很重要，关乎成败）

![](./huitu/lanyazhunbei_3.png)
![](./huitu/lanyazhunbei_4.png)

- 使用高级分栏中控制的事件积木块

![](./huitu/lanyahuitu_1.png)

![](./huitu/lanyahuitu_2.png)

2.手机控制端在kittenblock中程序操作方法
 
- 硬件选择microbit及添加蓝牙拓展包

![](./huitu/kongzhizhunbei_5.png)

![](./huitu/kongzhizhunbei_1.png)
![](./huitu/kongzhizhunbei_2.png)

- 由于手机APP中预设的按键比较简单，上下左右，4个按钮

![](./huitu/shoujiduan_3.png)

想要使用的话如下操作，图中当按下空格键的位置可以下拉选择其他如上下左右

![](./huitu/shoujiduan_4.png)

- 对于如果想要在舞台自己新建点击项目的按照如下操作

![](./huitu/lanyakongzhi_1.png)

选择一个精灵，当然你可以自己设计一个，点击他们后会出现在舞台中，可以自行拖动位置

![](./huitu/lanyakongzhi_2.png)

![](./huitu/lanyakongzhi_3.png)

- 对每个精灵进行按键事件的匹配，分别选择这些精灵进行积木块编程

![](./huitu/lanyakongzhi_4.png)

此处由于舞台中新建的称之为角色，所以我们选择当角色被点击事件

![](./huitu/kongzhizhunbei_3.png)

就这样给每个舞台角色都匹配好了事件后，可以扫码进手机作为控制端程序来控制microbit了

我们先打开手机app，确保蓝牙打开，首先连接microbit蓝牙

![](./huitu/shoujiduan_5.png)
![](./huitu/shoujiduan_6.png)

接下来确保手机和电脑在同一wifi网络下，我们将控制程序扫进app

![](./huitu/erweima_1.png)
![](./huitu/erweima_2.png)

![](./huitu/shoujiduan_2.png)

![](./huitu/shoujiduan_1.png)

程序扫进来后我们点击SAVE并PLAY就可以加载界面了，如下，点击中间绿棋子就可以开始控制你的绘图小车了~

![](./huitu/shoujiduan_7.png)


这里直接给出绘图小车及蓝牙绘图小车的示例程序以供参考：[程序入口](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=366&extra=page%3D1)

## 展示

![](./huitu/huitu_show.gif)

__注：__

- 接线别插反咯，可能会烧
- 如果app中为发现microbit蓝牙，那么请检查microbit端的hex烧录前蓝牙的项目设定选项是否与上述说明一致
- 手机扫码请确保与电脑在同一wifi网络
- kblock手机app请到小喵科技交流群下载 568084773
- kittenblock和makecode离线版请到小喵科技论坛下载[论坛](http://kittenbot.cn/bbs/forum.php?mod=forumdisplay&fid=37)

如果通过上述教程还有无法实现的部分请加入小喵科技交流群咨询：568084773















