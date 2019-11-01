# 两路寻线魔块

![](./images/07_03.png)

此模块上有两路寻线传感器，返回高低电平值，遇到黑线上的对应寻线传感器的背面的红LED灯会灭，触发后，返回数值0。

## 详细介绍

![](./images/07_01.png)

## 参数介绍

- 支持电压： 3V-5V
- 尺寸：56mm X 24mm X 25mm
- 接口：PH2.0 4PIN端子 ，引脚服从GVAB排布
- 类型：数字传感器，按下按键，事件为真

对应Makecode编程界面：

Makecode在线地址：https://makecode.microbit.org/beta#editor

加载Powerbrick插件地址：https://github.com/KittenBot/pxt-powerbrick

## 注意事项

- 寻线传感器安装高度需要在检测范围内，并且地面是非强反光面。
- 使用前需要调整寻线模块距离地面黑线的高度。

## 巡线魔块插接演示

桌面上贴上黑胶布，用巡线魔块去检测，当A巡线器检测到黑线吗，

![](./images/IMG_2570.GIF)

## 编程介绍

### 按键检测编程

![](./images/07_02.png)