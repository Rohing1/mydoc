### 兰大一keepalived演练

 现在内网2台机器； 想让你们帮忙验证下 keepalived 功能。
验证的内网服务 测试点：
1、内网某个服务挂了（交易服务、对账服务， 系统服务 ）；自动切换，并且能正常运行；

对账 && 交易服务 && 系统服务 

内主已经断了

![image-20250702144717379](C:\Users\pytc\AppData\Roaming\Typora\typora-user-images\image-20250702144717379.png)

内备

![image-20250702144942855](C:\Users\pytc\AppData\Roaming\Typora\typora-user-images\image-20250702144942855.png)

1.需要访问194.1.3.82:9007/system-server/test/



2、redis挂了，切换；



3、mysql挂了，切换；



4、nginx挂了，切换；内主挂了 vip跑到内备

![image-20250702165442874](C:\Users\pytc\AppData\Roaming\Typora\typora-user-images\image-20250702165442874.png)

5、内主是否每日本机备份；有

![image-20250702165750501](C:\Users\pytc\AppData\Roaming\Typora\typora-user-images\image-20250702165750501.png)

6、内备是否实时同步内主数据、是否每日自动本机备份；有

![image-20250702165710436](C:\Users\pytc\AppData\Roaming\Typora\typora-user-images\image-20250702165710436.png)









7、keepalived切换后，数据库是否正常使用，切换后内备为主机，如何让内主为主机的步骤；

我们需要确保这个服务器的稳定下；

