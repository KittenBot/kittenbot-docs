# RFID魔块

RFID

![](./images/10_04.png)

![](./images/10_05.png)

此模块可以对套件配套的RFID卡或者空白RFID卡进行读写，用于权限验证的DIY制作。

配套RFID卡内存为1K，有16个分区，每个分区有3个数据块可进行写入。



## 详细介绍



![](./images/10_03.png)

## 参数介绍

- 支持电压： 3V-5V
- 尺寸：56mm X 56mm X 16mm
- 接口：PH2.0 4PIN端子 ，引脚服从GVAB排布
- 感应距离：≤3CM
- 感应到卡，指示灯Card会亮。模块有读写操作，指示灯Working会闪烁。


对应Makecode编程界面：

Makecode在线地址：https://makecode.microbit.org/beta#editor

加载Powerbrick插件地址：https://github.com/KittenBot/pxt-powerbrick


## 使用注意事项

- RFID需要避免在强磁下使用，避免干扰。
- RFID卡与模块之间不能有金属片阻挡，否则会无法进行数据读写。
- RFID卡在写入大量数据时速度较慢，请注意是否写入完成后，再把RFID卡取走。
- 常规的公交卡、地铁卡是无法进行写入（因为卡被加密了），但可以读取UID号（每一张卡都有唯一的ID号），可用于权限鉴别的制作。

## RFID魔块检测演示

当检测到其他卡时，不开门，并MP3魔块发出警告“你是谁？”

当检测到合格卡是，电机运转，门打开，MP3魔块发出欢迎回来的声音

当小车车进门后，超声波检测到，门关上

![](./images/IMG_2583.GIF)

## 编程介绍

RFID模块必须接到**I2C接口**上！因为它属于高级模块！

RFID模块必须接到**I2C接口**上！因为它属于高级模块！

RFID模块必须接到**I2C接口**上！因为它属于高级模块！


### RFID写入编程

将hello写在RFID卡中的S1区的B0块中

![](./images/10_01.png)

### RFID读出编程

读取RFID卡中的S1区的B0块中的数据
![](./images/10_02.png)

### 读取RFID卡的“身份”——UUID

每个人手上的RFID卡的UUID都不一样，读出你手上的UUID，并记录下来

![](./images/10_06.png)

### 判别UUID

由于每张RFID卡的UUID都不一样，一般我们可以用做识别卡的作用，程序如下

一般普通的什么会员卡，低端的卡的RFID卡是可以被我们模块读到的，一些高级卡则不能（协议格式不一样）。

![](./images/10_07.png)