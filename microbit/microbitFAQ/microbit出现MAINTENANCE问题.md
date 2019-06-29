# MICROBIT盘符变为MAINTENANCE的原因及恢复方法

正常情况下，Micorbit与电脑连接后是出现MICROBIT的盘符，表明可正常烧写程序
（请注意，虽然烧写的方式是将.hex文件拷贝进盘符，但所拷贝的文件并不会被看到，也就是说MICROBIT盘符内始终应该只有DETAILS.TXT和MICROBIT.HTM两个文件）

![](./images/c1.png)

**一旦盘符变为了MAINTENANCE，意味着你的bit进入了维护模式，有以下两种原因**

![](./images/c3.png)

- 在插上USB的同时按下了复位按键自主进入到了维护模式（重新拔插后恢复）
- 在使用bit的拔插过程中固件丢失（无法自动回到正常状态）


在固件丢失的这种情况下，我们只需要重新烧入固件即可恢复  
    
小喵为你准备好了：[点击下载](http://cdn.kittenbot.cn/microbit/0253_kl26z_microbit_0x8000.hex)


**烧入方法**

![](./images/c4.png)

之后看到进度条走完后就能恢复令你感到安心的MICROBIT盘了~


