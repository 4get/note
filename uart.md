用户使用的是市场常见的USB转串口接头，连接后操作系统默认的是COM4（或其他），但该设备要求必须使用COM1口，如何修改？

[http://support1.lenovo.com.cn/lenovo/wsi/htmls/detail_12608722044535045.html]

1、按照要求安装转接头驱动程序，在“设备管理器/端口”下，可以发现一个“USB Serial Port（COM4）”，如下图：

2、右键单击“USB Serial Port（COM4）”，选择“属性”，如图：

3、选择“Port Settings”选项卡，如图：

4、单击“Advanced…”按钮，如图：

5、单击“COM Port Number”右侧的下拉箭头，选择所需要的端口号，如COM1，单击“OK”。如图：

6、单击“确定”。

7、这时，设备管理器里面“USB Serial Port”的端口号已被修改为“COM1”。如图：

