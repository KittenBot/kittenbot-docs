# 喵家蓝牙适配器4.0   
## 产品名称：   
蓝牙适配器4.0   

图片后面再补   

适用人群：Microbit拥有者   

## 配送清单：   
蓝牙适配器4.0 X1   

## 产品简介：   
此蓝牙适配器是用于电脑上，usb蓝牙4.0适配器。   
它可实现电脑与其他具有蓝牙协议的设备连接。如Microbit、手机等等

## 产品特色：   
- 支持Microbit的蓝牙通讯下载、乐高的EV3蓝牙通讯下载   
- 标准蓝牙4.0规范，双模式传输，向下兼容蓝牙2.0、2.1、3.0规范   
- 双模低功耗，低延迟，极速连接灯。   

## 产品参数：   
- 传输距离：10米（无阻隔）    
- 传输速率：3Mbps，支持文件、音频高速传输   
- 支持系统：window xp、win7、win8、win10   
- 长x宽x高：2cmx1.5cmx0.6cm   
- 净重：15g   
- 毛重：根据包裹最终大小决定   

## 技术参数：   
- 工作电压：5V DC   
- 待机电流：0.4uA（当被连接时）   
- 工作电流：22mA（具体根据工作模式）   
- 工作环境要求：-20°C——+70°C   
- 工作湿度要求：10%——90%   
- 技术认证：RoHS、CE、FCC、BQB   

## 使用环境：
编程方式：Kittenblock(基于Scratch3.0)/Makecode   
可连接硬件：Microbit   

## 具体使用方法：
### 喵家蓝牙设备器插上电脑
会提示你安装新硬件，确认安装即可。   
如果没有提示安装硬件，这个也没有关系。（因为下一步我们要用其他驱动来替换这个驱动）   

### 替换驱动
下载此 [https://zadig.akeo.ie/](https://zadig.akeo.ie/downloads/zadig-2.4.exe) 工具   
如果你电脑安装了杀毒软件，杀毒软件会将它识别为病毒...你记得找回来，或者下载前先关闭杀毒软件。

### 设置更新驱动
下载完成后，双击打开   
![](./bledongle/12.png)   
打开后的界面如图   
![](./bledongle/06.png)   
选择Options——List ALL Devives   
![](./bledongle/07.png)   

在中间的下拉栏找到我们的喵家特色蓝牙设备器CSR8510...，它对应的USB ID一定是**0A12 0001**   
一定不能选错!   
一定不能选错!   
一定不能选错!   
否则搞错驱动就会变砖，无法驱动了。   
![](./bledongle/08.png)   
![](./bledongle/01.png)   

之后点击Install Driver就行了，静静等待它自动完成。   
![](./bledongle/10.png)   

这个驱动安装只需要做一遍，如果后面你蓝牙设备更换usb口，有可能windows又安装成官方的驱动。
不用担心，只需要重复上面步骤即可。   

### 刷入MIT官方的microbit固件

点击下面地址下载hex固件，并将其复制到microbit的u盘盘符上。
[http://cdn.kittenbot.cn/microbit/scratch-microbit-1.0.hex](http://cdn.kittenbot.cn/microbit/scratch-microbit-1.0.hex)

该固件由MIT官方开发，目前还没有开源。大家可以前往[https://scratch.mit.edu/microbit](https://scratch.mit.edu/microbit)查看最新更新情况。   

### 固件成功刷入现象   
烧录了后，Microbit点阵屏会滚动一个字符串，这个就是你的蓝牙ID,不用记，没什么用的。

### Kittenblock内使用
打开最新的Kittenblock (1.76+)
如果驱动安装正确并插着电脑上，我们在通信接口下可以看到蓝牙dongle设备。   
（无需点击，因为点击了也不会有反应，只是软件提示你已经找到喵家usb蓝牙设备器）


![](./bledongle/02.png)

在Kittenblock左下角打开扩展插件，并在弹出的窗口中找到Micro:bit插件。这个插件由MIT官方提供和开发，我们只是在kittenblock内部对接了蓝牙dongle设备。（Kittenblock是最勤奋的搬运工，给大家带来最新黑科技~）

![](./bledongle/03.png)

加载插件后在插件顶端找到硬件连接按钮

![](./bledongle/04.png)

点击打开microbit设备搜索框。找出硬件后选择“connect”   
如果找不到microbit请点击“Refresh”   
如果找不到microbit请点击“Refresh”   
如果找不到microbit请点击“Refresh”   
如果找不到Microbit蓝牙，肯定是你没有刷MIT官方提供的microbit固件。回去上面看刷MIT固件的步骤   

![](./bledongle/05.png)

连接上后可以试试拖动一些方块到工作区看看效果~

![](./bledongle/blemicrobit.gif)


## 产品详细的学习资料地址：   
http://learn.kittenbot.cn/zh_CN/latest/electronics/USB%E8%93%9D%E7%89%99%E9%80%82%E9%85%8D%E5%99%A8.html

## 其他教程   
小喵教程集合地址：learn.kittenbot.cn   
小喵论坛地址：kittenbot.cn/bbs   
网易云课堂：搜索小喵科技   
更多的实时讨论，请加入爱上小喵科技官方Qqun（淘宝不支持Qqun，具体请向客服索要）   


## 注意事项：
**在使用Kittenblock与喵家usb蓝牙适配器的过程中，请勿随意拔掉usb蓝牙适配器，拔掉会导致Kittenblock软件程序崩溃。（嗯啊，就是这么娇气）   
正确做法是，先保存程序后，关闭软件后再拔掉蓝牙适配器**

本产品只适用于14岁以上的儿童进行独立使用，8~14岁儿童请在家长或者老师的陪同下进行使用。   
如使用前请按照小喵官方资料指导下进行使用，不要随便接插电路   
注意不要在金属表面，或者导电的物体上使用，以免短路   
请避免在潮湿和有水的地方使用，以免短路   
电路板或者机械上含有细小物件请不要吞食，请放在儿童接触不到的地方妥善保管   
