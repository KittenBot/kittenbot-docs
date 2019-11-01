# WIFI魔块

- WIFI是无线通讯中关键的媒介，它的出现赋予了能量魔块新的生机及更多的可能性。其中前段时间比较火爆的物联网IOT(Internet of Things)，就是通过WIFI对各个传感器信息进行采集并远程控制执行器做出合乎需求的动作。而如今正一触即发的AIOT（A1人工智能+IOT物联网），更是将IOT和人工智能相结合，不再完全依赖认为做出判断，继而由机器代为管理各种事务。 

- 将wifi与kittenblock中实用的AI插件进行结合，所诞生的项目可能是：人脸识别门禁系统，宠物喂食管家，智能家居系列，停车场管理系统等等


## 接线  

- WIFI魔块-> 主控盒 Port2  

- 电池盒->主控盒 电源接口（WIFI模块需要电池供电否则电流不足）  

- 接线图

![](https://s2.ax1x.com/2019/09/03/nk6vfe.jpg)   

## 调试  

**Step1：**  

加载插件积木块,并认识积木块功能
 
![](https://s2.ax1x.com/2019/09/03/nkgYUf.jpg)  

![](https://s2.ax1x.com/2019/09/03/nkgt58.jpg)  

![](https://s2.ax1x.com/2019/09/04/nV3SBj.jpg)

**Step2：**  

打开IOT面板，建立MQTT话题，以喵家自己的MQTT服务器为例(免费开放给大家使用)   

- 进入IOT网址：[https://iot.kittenbot.cn](https://iot.kittenbot.cn)   
- 新建话题： 新建的话题名字是全网唯一的，如果别人注册过那么你只好换一个名字了。这里我们用mes为例     
![](https://s2.ax1x.com/2019/09/04/nV3sxS.jpg)    

(如果你新建的话题不希望公开，则可以填写后面的登录用户名和密码) 

**Step3：** 

搭建一个调试程序，并上传到microbit，目的是将microbit通过wifi模块接上IOT服务器  

![](https://s2.ax1x.com/2019/09/04/nVDFe0.jpg)   

![](https://s2.ax1x.com/2019/09/04/nVJEgf.jpg)   

`程序上传完成后，观察wifi模块的RGB灯，会又红~蓝~绿，当保持亮绿灯后，就连上了路由器，此时我们在IOT控制台的话题下看看订阅设备是否有新设备出现`

**Step4：**   

选到订阅的话题mes，拉到页面最下端，点击①的刷新，如果看到出现了程序设定的ID名称robot01，则成功连上MQTT服务器，可以开始通讯了。  

`设备ID可以自行定义，但不可使用中文和数字开头` 

![](https://s2.ax1x.com/2019/09/04/nVryHx.jpg)  

**Step5：**   

正式调试话题的通讯

- 话题发送消息调试：  

按一下microbit的按键A,在数据显示的表单下选择`消息`，并刷新一下，可以看到出现了一条来自ID：robot01 发送的helloIot

![](https://s2.ax1x.com/2019/09/04/nVy40I.jpg) 

- 话题接收调试：  

网页端发送消息给microbit，程序设定，当microbit接收到ok后，显示√，如下图完成后，点击发送，观察microbit现象。

![](https://s2.ax1x.com/2019/09/04/nVc8RU.jpg)  






























