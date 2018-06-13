# kblock简介 #

kblock是小喵科技出品可以在手机上进行图形化编程的APP，如同电脑端的kittenblock一样使用功能积木块搭建自己想要的程序。与电脑端的kittenblock图形化编程相比除了少了舞台那部分的积木编程，其他的逻辑编程和硬件编程，都保持了原汁原味，方便用户进行学习，无缝连接，减少学习成本。因此kblock的优势就体现在这里。   
另外，kblock还有一个很重要的特点：
作为“APP万能制作器”   
降低用户的DIY难度，是小喵科技一直努力的方向。积木块编程解决了用户编程的难度，可以对喵家体系的控制板或者市面上常用的硬件进行控制。现在已经进入了智能手机时代，用户需要是用手机对硬件进行控制。   
kblock这个万能的“APP万能制作器”应运而生：   
你无需再学多一门java语言来进行制作APP！   
你无需再学APP Inventor2进行积木块！   
   
只需要你会简单的Scratch编程，你一样能作出好玩的“APP”

具体过程：
在电脑端的kittenblock中舞台DIY你的APP界面，舞台中的每一个角色就是对应APP上的控件（例如触发按钮），每个角色背后就对应就是控制硬件的图形块代码，最后编程完毕后，kittenblock生成二维码，再用Kblock APP二维码扫描即可扫描到手机上。
</p>
# app详情 #
<ol>
## 下载方式 ##
<p>安卓端:打开手机豌豆荚，搜索kblock或者kittenbot <br/>苹果端: 搜索kittenbot</p> <br/>

## kblock第一界面（Scratch播放器界面介绍) ##
<p>内容概述： <br>  
  ①.硬件选择 <br>②.手机端与硬件（机器人）连接方式 <br>③.默认项目示例 <br> ④.二维码生成手机控制app</p>
![](https://i.imgur.com/EqCVAVJ.png)<br/><br/>
### 目前kblock只支持3种硬件，分别是kittenbot，MiniLFR，以及未列出的microbit   

![](https://i.imgur.com/1wJ41Jg.png)<br><br>
![](https://i.imgur.com/KzG4nWp.png)<br/><br/>
### 选择硬件后可以针对性连接，连接的方式分为两种，一是kittenbot和MiniLFR的连接使用wifi模块，microbit的连接使用蓝牙   

![](https://i.imgur.com/2y4UdBM.png)<br><br/>
<p>wifi的连接:<br>按照如下插上wifi模块后，打开kblock参考指引教程<br>
![](https://i.imgur.com/zf7qLvf.jpg)<br>
![](https://i.imgur.com/v33spnE.jpg)<br>
![](https://i.imgur.com/Ldybf1M.png)<br>
<p>一切准备就绪后，出现如下wifi，点击连接<br>
![](https://i.imgur.com/KWYJ4Zo.png)<br><br>
<p>如果你手上有Microbit，蓝牙的连接请按照如下步骤：
<p>进入makecode（makecode离线版） 新建一个项目<br>
![](https://i.imgur.com/S3JmEbg.png)
<p>在添加软件包中添加蓝牙<br>
![](https://i.imgur.com/yn5ben1.png)
![](https://i.imgur.com/0y4z4QI.png)<br>
<p>项目设定——蓝牙无密码(选中第一项让任何人都可以连接Microbit蓝牙功能)<br>
![](https://i.imgur.com/3mdJeHq.png)<br>
90%的用户都会选错这个选项，注意箭头和红色框，选上面那个！！！<br>
![](https://i.imgur.com/PROr1uf.png)<br>
<p>开始进行正式编程，把“发生事件”拖出来<br>
![](https://i.imgur.com/I8Ym0xF.png)
![](https://i.imgur.com/iLZ2izI.png)<br>
<p>我们用了“发生事件”这个高级模块，这个是microbit内部操作系统的信号事件（Fiber Event）
目前Kittenblock支持DPAD Controller下的事件<br>
![](https://i.imgur.com/QX1Ffwg.png)<br>
<p>编写完成，下载到Microbit板子上（将hex保存到microbit板子上）<br>
<p>一定要确保程序已经下载到板子上，不然蓝牙会搜索不出来的<br>
![](https://i.imgur.com/gcPoBVp.png)<br>
<p><strong style="color:red;">提示：</strong><br>如果你还想用Robotbit与蓝牙插件一起用可以这样操作：
添加Robotbit的独立插件pxt-robotbitnopixel（没有RGB灯，因为RGB灯会与和蓝牙冲突）
在添加包那里直接输入这个地址<br>
[https://github.com/KittenBot/pxt-robotbitnopixel](https://github.com/KittenBot/pxt-robotbitnopixel)<br>
![](https://i.imgur.com/QWUoCjS.png)<br>
<p>接着我们打开手机蓝牙功能，不同的手机打开蓝牙方便不一样，对应操作<br>
<p>如果上述步骤没错，我们在kblock中就可以看到如下蓝牙<br>
![](https://i.imgur.com/CVS0EJX.png)<br>
### 给出的默认示例   

![](https://i.imgur.com/9IsbPto.png)<br>
<p>区分为kittenbot和MiniLFR的不同硬件，请左上角选择对应硬件使用示例，如选定kittenbot就只能使用如下两种示例<br/>
![](https://i.imgur.com/02Mo9a1.png)<br>

<p>使用前，主控板必须恢复出厂固件！！可以用过电脑pc端软件进行固件恢复<br/>
<p>使用前，主控板必须恢复出厂固件！！可以用过电脑pc端软件进行固件恢复<br/>
<p>使用前，主控板必须恢复出厂固件！！可以用过电脑pc端软件进行固件恢复<br/>
<p>打开后点击图中旗子就可以直接简单控制你的kittenbot了<br/>
<p>补充说明：Kittenbot遥控对应——kittenbot需要装成直流电机模式，按下方的方向键就可以控制小车的运动方向<br/>
<p>补充说明：Kittenbot画图——kittenbot需要装成步进电机模式，按上方的数字小车就会开始画对应的N角形<br/>
![](https://i.imgur.com/x27Mwvy.png)<br>
### 二维码下载到手机    

![](https://i.imgur.com/TtIltmG.png)<br>
<p>在kittenblock上编好功能块后扫二维码的方式加载到手机端直接使用，但需要扫码时确保电脑与手机在同一wifi网络<br> 
![](https://i.imgur.com/am4J5t9.png)<br>
![](https://i.imgur.com/j2budZv.jpg)
## kblock第二界面（快速编程界面介绍) ##
<p>首先在已有的硬件中选择,以kittenbot为例</p><br/>
![](https://i.imgur.com/7UaoVS9.png)<br>
<p>在快速编程界面新建项目</p>
![](https://i.imgur.com/OVbto1h.png) <br>
<p>此时编程界面就只有kittenbot功能积木块。该界面右上角的小门图标是退出，左下角的开始键是执行</p>
![](https://i.imgur.com/o9QwDZH.png) <br/>
## kblock第三界面（信息界面介绍) ##
![](https://i.imgur.com/TME3GpD.png)<br/>
<p>①.FAQ为常见问题解答<br>
<p>②.固件更新：</strong>选择好硬件后，确定与硬件wifi已连上后可以点击进行无线固件更新，有时候会失败,请多试几次,如下是选择了MiniLFR小车，更新固件成功示意图</p><br/>
![](https://i.imgur.com/TvuV0aH.png)<br>
<p>③.加入路由器网路：给出了wifi模块连接家里路由器指引方案(一般无需关心)<br>
<p>④.显示启动指引：关闭的话开启kblock时自动跳出的wifi连接指引便不会出现
![](https://i.imgur.com/6KnSF5o.png)<br>

