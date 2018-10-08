# Armourbit

![](./images/01_03.png)

Microbit的一款扩展配件，是能量魔块体系的主控盒，打通Microbit与各种能量魔块的连接，采用4PIN防反接端子口，自带蜂鸣器，两路电机驱动，八路舵机驱动。对电路板进行全包裹，全方位保护更安全，适合编程教育的使用场景。

## 详细介绍

![](./images/03_01.png)

## 参数介绍

- 电压：3.3V（板载不带5V电压）
- 尺寸：61mm X 61mm X 23mm
- 接口：PH2.0 4PIN端子 ，引脚服从GVAB排布
- 
对应Makecode编程界面：
Makecode在线地址：https://makecode.microbit.org/beta#editor
加载Powerbrick插件地址：https://github.com/KittenBot/pxt-powerbrick


## 引脚分布

![](./images/03_02.png)

- 新手用户无需记住Port口对应的引脚，只需记住对应port口使用即可。
- 使用Port5-Port7口需关闭LED点阵屏功能（如图）才能进行使用
- Port4口没有模拟读取功能（温湿度的土壤水位魔块不能使用）

（因为Port5-Port7引脚与Microbit点阵屏复用了）

![](./images/03_03.png)


## 使用注意事项

- 舵机接口只能使用蓝色的9g小舵机或Geekservo舵机，禁止插接大电流舵机。
- 直流电机接口只适用于喵家TT电机或Geekservo电机，禁止插接大电流电机。
- 蜂鸣器与Microbit的P0复用，使用时需检查底部的拨动开关是否打开。
- 使用各个模块、电机、舵机，必须接Powerbrick电池盒，否则因为电流不足，导致模块使用不正常。

## 编程介绍

### 点阵屏编程

![](./images/03_04.png)

### 按键编程

![](./images/03_08.png)

### 蜂鸣器编程

![](./images/03_05.png)

### 直流电机编程

![](./images/03_06.png)

### 舵机编程

![](./images/03_07.png)