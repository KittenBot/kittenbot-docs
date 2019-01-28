# 喵家IOT服务器快速入门

喵家专门针对IOT做了一个服务器，有了这个服务器，你就可以把数据传到服务器上，然后从外网（全球各地能上网的地方进行查看你推送的数据），根据MQTT的协议，我们的物理层上的设备就配置好了。

服务器你将直接用喵家的服务器

联网设备就是你的Microbit+wifi模块

## 注册服务器账号

登录www.kittenbot.cn/bbs 喵家论坛注册一个账号。配图可能有所变动，请根据实际情况为准
![](./images/Microbit_IoT01.png)

十分钟后（所以你提前拥有喵家账号是有好处的），用你的账号密码登录
www.kittenbot.cn
![](./images/Microbit_IoT02.png)

## 喵家IOT服务器话题注册

选择IoT控制面板
![](./images/Microbit_IoT03.png)

这就是IoT控制面板主界面，我们新建一个话题
![](./images/Microbit_IoT04.png)

输入话题名称，格式一般为/+英文，例如/CCFIVE,记住话题是全服务器唯一的，如果申请不成功，有可能你申请的话题已经被其他人用了，请更换另外一个。

![](./images/Microbit_IoT05.png)

话题成功创建,记住这个话题，这个话题后面编程需要用到
![](./images/Microbit_IoT06.png)

