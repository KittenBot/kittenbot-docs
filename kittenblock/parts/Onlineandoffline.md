# 在线模式和离线模式

## 什么是在线模式


- 顾名思义，在线模式就是需要kittenblock或者kblock app需要保持和机器人之间的实时通讯。通信方式包括串口、wifi或者蓝牙。

- 机器人上需要预先烧录在线模式的固件。

- kittenblock通过发送指令给机器人，机器人执行对应指令。


## 什么是离线模式

- 离线模式不需要保持和kittenblock或者app之间的通信。

- 离线模式只能执行固化烧录的程序，更换程序需要重新执行烧录。

- 一般情况下将图形化代码专为C++或者python固化到目标主板上。

## 目标硬件支持情况

### Rosbot和MiniLFR：

支持在线模式和离线模式，通过Kittenblock将图形化代码翻译成Arduino C++代码并烧录到主板上。

### Microbit：

支持在线模式和离线模式，在线模式需要烧录一个空固件到microbit上，具体参看python部分教程。

### Arduino电子体系：

目前离线模式基本完善了，支持市面上大部分传感器模块。在线模式需要自定义生成通信固件，目前正在完善中。


## 在线模式指令集

在线模式指令设计本身参考的是工业上应用相当广泛的CNC指令系统，也就是G代码或者M代码。每一条指令以G或者M打头，后面跟着指令序号，之后是空格分隔开的参数。指令最后以回车换行符结束。

每个指令参数具体含义请参考下面的说明。

### Rosbot

- M0：打印固件版本号
- M1 PIN MODE：设置IO模式，相当于pinMode
- M2 PIN LEVEL：设置数字电平，相当于digitalWrite
- M3 PIN：读取数字电平，相当于digitalRead
- M4 PIN PWM: 模拟输出PWM，相当于analogWrite
- M5 PIN：读模拟信号，相当于analogRead
- M6 PIN frequency duration：蜂鸣器发声，相当于Tone函数
- M7 PIN degree：舵机角度设置（已经取消，请参考后面舵机阵列指令）
- M8：读取外部电源电压
- M9 PIN PIX Red Green Blue：RGB灯显示，参数为引脚、像素位置（0为选中全部像素）、红、绿、蓝
- M10 PIN：按键模块读取，按下返回1
- M11 Brightness：设置RGB灯亮度
- M20 String：点阵屏滚动显示字符串
- M21 Matrix：点阵屏显示阵列16制编码像素，每个位一个像素，共计128个像素（一共16个字节）
- M30 Level1 Level2 Duration：双IO电平设置，主要给MP3模块使用
- M31 Pin1 Pin2 Duration：双IO引脚设置，主要给MP3模块使用
- M100 Index degree speed: 单个步进电机运动控制
- M101 distance: 步进电机小车直线运动，距离单位厘米
- M102 degree: 步进电机小车原地转向，单位度
- M103 diameter degree: 步进电机小车弧线运动，参数为直径和角度
- M104 PPm：设置步进电机小车PPM（pulse per meter，每米脉冲个数，默认15141）
- M105 basewidth：设置步进电机小车轮距
- M200 index speed：设置直流电机速度，index从0到3分别对应M1A到M2B
- M203：停止所有直流电机
- M204 m1 m2 duration：双直流电机速度设置，带延时。（主要用于直流电机小车模式）
- M205 m1 m2 m3 m4：四个直流电机速度设置
- M209 vspeed hspeed rspeed：万向轮小车速度设置，参数分别为：垂直速度、横向速度和转动速度（已经内置了速度映射计算）
- M212 index degree speed：舵机阵列设置。index值0~10对应rosbot主板上4~A3扩展引脚序号
- M220：初始化PS2手柄，手柄接线如下：
```
PS2_DAT A3
PS2_CMD A2
PS2_SEL A1
PS2_CLK A0
```
- M221 axis：读取PS2手柄遥杆值
- M222 button：读取PS2手柄按键值
- M250 trig echo：超声波测距

### MiniLFR

- M0：打印固件版本号
- M1：读取巡线传感器值（校准后的值输出）
- M2：去取当前PID参数设置
- M3 P10.0 I0.015 D1500：设置pid参数，可以只设置某一个具体值，参数前要带上大写参数符号。
- M4 index：读取巡线传感器阈值
- M5 index threshold：设置巡线传感器阈值（由自动校准设置）
- M6 Left Right：设置车头灯亮灭（1位亮，0为灭）
- M7：读取超声波距离，需要插上超声波传感器不然只会返回999
- M8：读取电池电压
- M9 index：读取当前按键状态（1为左键，2为右键）
- M11：读取红外解码值
- M12 code：红外发射编码 (红外解码和发送都是16进制，最长4个字节)
- M13 index red green blue：底部RGB灯颜色设置，参数index（0为全部灯，1为左灯，2位右灯）
- M14 brightness: RGB灯亮度设置
- M15 LCDstring：LCD显示字符串
- M16 index red green blue：猫耳朵超声波RGB灯控制，参数index（0为全部灯，1为左灯，2位右灯）
- M17 notes：蜂鸣器音乐，具体音调定义参考[microbit定义](http://microbit-micropython.readthedocs.io/en/latest/music.html)
- M18 freq duration: 蜂鸣器产生频率，相当于Tone函数
- M19 note: 蜂鸣器播放某一个音符，60位C4，音符序号参考[wiki](https://en.wikipedia.org/wiki/Scientific_pitch_notation#Table_of_note_frequencies)
- M20 String：点阵屏滚动显示字符串
- M21 Matrix：点阵屏显示阵列16制编码像素，每个位一个像素，共计128个像素（一共16个字节）
- M22 index red green blue：RGB灯环控制，参数index（0为全部灯，其余为对应像素位置）
- M30 Level1 Level2 Duration：双IO电平设置，主要给MP3模块使用
- M200 speedleft speedright：左右车轮速度
- M201 x y：遥杆模式下x，y坐标设置（内置映射为左右轮速度）
- M202 speedleft speedright duration：左右车轮速度，带延时
- M209 difference：设置左右轮差速（出厂已经校准过了）
- M210：读取左右轮差速
- M300：左右轮速度校准，需要在i2c口插上陀螺仪模块
- M301：巡线传感器校准，需要放在已经贴好的巡线地图上。
- M999：软复位

指令大体上就这些了，具体可以参考固件源代码，也可在kittenblock点击对应模块后在arduino面板查看具体发送的指令格式。