# 树莓派版本Kittenblock



### 前记

在2019年深圳makerfaire我们特意准备了基于树莓派和人体骨骼追踪的机器人，但是由于展位的人实在太大，而且机器人第一天上午关节舵机就阵亡了。但是能在树莓派上跑的kittenblock却引起了现场很多观众的注意，我们也多花了一点心思将kittenblock优化到在树莓派下完整的运行。

### 特点

* 完整移植于pc版本的kittenblock，保留了pc版本所有特性，包括所有AI功能和各种插件。
* 支持树莓派自带的摄像头输入
* 支持从ROSBOT直接供电（完美解决树莓派4的type-c供电门问题），并且可以直接串口通信

### 安装

* 首先需要准备树莓派3或4，SD卡在8G或以上，安装raspbian系统。

* 打开命令行，从下面地址下载树莓派版本的kittenblock:

  `wget http://cdn.kittenbot.cn/kittenblock.tar.bz2`

* 解压下载的安装包

  `tar xvf kittenblock.tar.bz2`

* 解压完成后会多出来一个名字为 `rasp_kblock`的文件夹

* 进入这个文件夹，在根目录下有一个可执行脚本

  `./kittenblock.sh`

* 略等片刻就可以看到kittenblock启动了
* Have Fun~