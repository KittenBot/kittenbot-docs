# 玩转贱鼠矩阵屏 #  
贱鼠矩阵屏是一款16x8微型点阵屏，3V到5V供电，轻便小巧的屏身能点亮你的意图，实现diy中简单图像表情，汉字，字符等的显示
## 贱鼠矩阵屏模块硬件示意图

![](./juzhen/resume2.png)  

![](./juzhen/shiyitu.png)  

## 贱鼠矩阵屏模块接线

**为了避免接错线烧坏，一定要先接线再开电源!** 

**有转接板的接线方法:**  

robotbit——转接板  

- 3V或5V——V
- SDA——2
- GND——G
- SCL——1  

![](./juzhen/zhuanjie.png)  

**直连接线方法:**  

robotbit——贱鼠矩阵屏 

- 3V或5V—VCC
- SDA——SDA
- GND——GND
- SCL——SCL

![](./juzhen/zhilian.png)  

## 编程
使用小喵科技离线版makecode的如下添加robotbit软件包  

![](./light/jiabao.png)  

使用官方在线版makecode的如下添加robotbit软件包  

![](./light/zaixian.png)  

使用makecode离线版进行编程，编程示例如下  

![](./juzhen/makecode.png)    

将程序加载到板子里  

![](./juzhen/xiazai.png)    

上图的编程坐标是根据下图的坐标编排来进行的  

![](./juzhen/dianzhenfenbu.png)  

**下载**

![](./chaoshengbo/xiazai.png)  
 

## 效果展示

接好线，并恢复固件后下载编好的程序，可以看到矩阵屏上出现了KB两个字符  

![](./juzhen/xiaoguo.png)


如果操作不成功，请检查：

- 检查接线是否正确   
- 需要接电源5V

如果以上都不能解决问题，请联系小喵科技，热诚为你服务<br>
