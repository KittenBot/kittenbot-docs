# Microbit底层固件更新  
  
关于Microbit底层固件需要更新是为了解决一些老板子经常性程序无法下载或失败的问题。目前的最新固件版本是0243，下面请按照步骤详细操作。  
  
## 查看手中Microbit底层固件版本的方法    
   
首先确保USB接线接上，点开MICROBOT盘
 
![](./images/c1.png)    
    
点开DETAILS.TXT记事本，带Version后面跟的就是版本号。

![](./images/c2.png)  
  
  
## 更新底层固件方法  
 
![](./images/x1.png)  
  
这里把超链接给你了，[直接点击下载需要更新的固件](https://mbed-media.mbed.com/filer_public/1d/fd/1dfd4113-9c05-43c3-9889-c021e1fb32ba/0243_kl26z_microbit_0x8000.hex) 

拔掉USB线，按住Microbit的复位按钮，一直按住的同时插上USB线，如下图，原本的MICROBIT盘会变成MAINTENANCE即表明已经进入维护模式，此时才可以松开复位按钮  


![](./images/b1.png)

![](./images/c3.png)    
    
这个时候Microbit是以存储设备存在，点开MAINTENANCE盘，将给你的.hex最新固件按照下图方式直接拖进去即可，不要操作，等待一会儿看到盘符又变回MICROBIT说明完成更新

![](./images/c4.png)  
  
最后再次按照上述步骤查看版本确保更新成功    
    
  
  

如果操作不成功，请检查：  

- 固件下载网址：[https://www.mbed.com/en/platform/hardware/prototyping-production/daplink/daplink-on-kl26z/](https://www.mbed.com/en/platform/hardware/prototyping-production/daplink/daplink-on-kl26z/)  
- 是否串口正常
- 是否成功进入了维护模式  

如果以上都不能解决问题，请联系小喵科技，热诚为你服务
  


  
