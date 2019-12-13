# MicroPython-API 

## 电机  

`robotbit.motot(电机序号， 速度， 运行时间)`   

```python
import robotbit
robotbit.motor(0, 255, 0)  
# 电机序号：0(所有电机)，1~4(分别对应M1A,M1B,M2A,M2B)  
# 速度：-255~255,负数为反转  
# 运行时间：表示一定ms后电机停止，设为0则电机不会停止  
```  

`robotbit.motorstop(电机序号)` 

```python
import robotbit
robotbit.motorstop(0)
# 电机序号： 立刻停下对应电机，0(所有电机)，1~4(对应M1A M1B M2A M2B)
``` 

## 舵机 

`robotbit.servo(舵机序号， 舵机角度)`  

```python
import robotbit 
robotbit.servo(0, 90)  
# 舵机序号：0~7分别对应S1~S8  
# 舵机角度：0~180 对应的是普通9g小舵机(180°转程的那种)
# 如果使用的是喵家geekservo(-45~225°)和2KG(0~360°舵机)参照下述  

# geekservo 
robotbit.servo(0, int((舵机角度-90)/1.5+90)) 
# 2KG  
robotbit.servo(0, int((舵机角度-180)*50/9+1500))  
``` 

## 步进电机  

`robotbit.stepper(步进电机M1角度，步进电机M2角度)`  

```python   
import robotbit
robotbit.stepper(0, 360) 
# 步进电机在达到设定角度的运转时间内，程序会卡死在这里
# 360表示步进电机转动一圈360°，这里的步进电机参照为28byj  

``` 

## 超声波 


`robotbit.sonar(引脚)` 

```python
import microbit
import robotbit
robotbit.sonar(microbit.pin1)
#  超声波(兼容喵家的猫耳朵超声波，一般的HC-04超声波请把TRIG和ECHO短接)  

```

## RGB 

```python   
import microbit  
import neopixel 

np = neopixel.NeoPixel(microbit.pin16, 4)
# robotbit上的RGB灯是由microbit的pin16脚控制，所以这里定义引脚为pin16，且需要用到的RGB数量为板载的4颗  

np[0] = (255, 0, 0)
# 设置第1颗RGB灯的颜色为红色。3个参数分别对应Red,Green,Blue。1~4颗RGB灯对应的np[参数]为0~3

np.show()
# 将你定义好的颜色显示出来，如果不加这一句，RGB是不会显示的哦。  

```

## 蜂鸣器 

这个使用的是microbit的官方库，固定为P0引脚

`music.pitch(频率， 持续时间)`

[点击下载频率音调对照表](https://kittenbot.oss-cn-shanghai.aliyuncs.com/ToneList.txt) 

```python   
import music 
music.pitch(262， 500) 
# 这是中音区的DO，响500ms  

```

`music.play(note)   # note = NOTE[octave][:duration]`  

```python  
import music 
music.play('c4:4') 
# c4:1对应的是octave:duration(八度：持续时间)，影响持续时间的因素有2点：ticks和bpm
# 默认的duration的系数 = 600000/bpm/ticks ，而默认bpm = 120，ticks = 4， 所以c4:1为第四八度DO响500ms
# 如果music.play('c')效果是跟c4:4一样的，原因是默认的octave=4， duration=4
# 当然music库内还内置了一些编好的旋律，比如music.play(music.FUNK)  

```  

可供选择的内置旋律有：  

DADADADUM、ENTERTAINER、PRELUDE、ODE、NYAN、RINGTONE、FUNK、BLUES、BIRTHDAY、WEDDING、FUNERAL、PUNCHLINE、PYTHON、BADDY、CHASE、BA_DING、WAWAWAWAA、JUMP_UP、JUMP_DOWN、POWER_UP、POWER_DOWN  

可以跑一下官方的例子，播一段有趣快乐的旋律  
```python  
from microbit import *
import music

# play Prelude in C.
notes = [
    'c4:1', 'e', 'g', 'c5', 'e5', 'g4', 'c5', 'e5', 'c4', 'e', 'g', 'c5', 'e5', 'g4', 'c5', 'e5',
    'c4', 'd', 'a', 'd5', 'f5', 'a4', 'd5', 'f5', 'c4', 'd', 'a', 'd5', 'f5', 'a4', 'd5', 'f5',
    'b3', 'd4', 'g', 'd5', 'f5', 'g4', 'd5', 'f5', 'b3', 'd4', 'g', 'd5', 'f5', 'g4', 'd5', 'f5',
    'c4', 'e', 'g', 'c5', 'e5', 'g4', 'c5', 'e5', 'c4', 'e', 'g', 'c5', 'e5', 'g4', 'c5', 'e5',
    'c4', 'e', 'a', 'e5', 'a5', 'a4', 'e5', 'a5', 'c4', 'e', 'a', 'e5', 'a5', 'a4', 'e5', 'a5',
    'c4', 'd', 'f#', 'a', 'd5', 'f#4', 'a', 'd5', 'c4', 'd', 'f#', 'a', 'd5', 'f#4', 'a', 'd5',
    'b3', 'd4', 'g', 'd5', 'g5', 'g4', 'd5', 'g5', 'b3', 'd4', 'g', 'd5', 'g5', 'g4', 'd5', 'g5',
    'b3', 'c4', 'e', 'g', 'c5', 'e4', 'g', 'c5', 'b3', 'c4', 'e', 'g', 'c5', 'e4', 'g', 'c5',
    'a3', 'c4', 'e', 'g', 'c5', 'e4', 'g', 'c5', 'a3', 'c4', 'e', 'g', 'c5', 'e4', 'g', 'c5',
    'd3', 'a', 'd4', 'f#', 'c5', 'd4', 'f#', 'c5', 'd3', 'a', 'd4', 'f#', 'c5', 'd4', 'f#', 'c5',
    'g3', 'b', 'd4', 'g', 'b', 'd', 'g', 'b', 'g3', 'b3', 'd4', 'g', 'b', 'd', 'g', 'b'
]

music.play(notes)  

```








