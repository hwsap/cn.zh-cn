# 在SAP HANA Studio上接入SAP HANA<a name="saphana_02_0048"></a>

在SAP HANA Studio上接入SAP HANA节点后，才能对SAP  HANA节点进行管理。此处以在Windows上安装的SAP HANA Studio上的操作为例介绍操作。

## 操作步骤<a name="sea2fdb4d8ee94d37ab8d6701a03cc766"></a>

1.  打开SAP HANA Studio软件。

    在Studio所在的云服务器操作系统上，单击“开始  \>  SAP HANA  \>  SAP HANA Studio“，系统打开SAP HANA Studio的管理界面，并弹出“Workspace Launcher“对话框，如[图1](#fig1888187224055)所示。

    **图 1**  Workspace Launcher界面<a name="fig1888187224055"></a>  
    ![](figures/Workspace-Launcher界面.jpg "Workspace-Launcher界面")

2.  设置好“Workspace“的目录后，勾选“Use this as the default and do not ask me again“，并单击“OK“。
3.  系统弹出“Security Storage“对话框，如[图2](#fig41112285224055)所示。单击“No“。

    **图 2**  Security Storage对话框界面<a name="fig41112285224055"></a>  
    ![](figures/Security-Storage对话框界面.jpg "Security-Storage对话框界面")

4.  在“Overview“界面上，单击“Open Administration Console“，进入“SAP HANA Administration Console“界面。
5.  <a name="li5088100224055"></a>在“System“下，右键单击，如[图3](#fig29888977224055)所示。

    **图 3**  SAP HANA管理控制台界面<a name="fig29888977224055"></a>  
    ![](figures/SAP-HANA管理控制台界面.jpg "SAP-HANA管理控制台界面")

6.  选择“Add System“，系统弹出“Specify System“界面，如[图4](#fig48130366224055)所示，输入相应的参数。

    关键参数说明如下：

    -   Host Name：填写SAP HANA云服务器的业务/客户端平面IP地址。
    -   Instance Number：填写SAP HANA节点上的实例编号。
    -   Mode：根据实际需求选择模式，需要指出的是SAP HANA 2.0时只能选择“Multiple containers“，并根据实际需求选择租户DB或系统DB。

    **图 4**  Specify System界面示例<a name="fig48130366224055"></a>  
    ![](figures/Specify-System界面示例.jpg "Specify-System界面示例")

7.  单击“Next“，系统弹出“System“界面，如[图5](#fig44232239224055)所示。选择“Authentication by database user“，并输入用户名和密码。

    用户名和密码为安装SAP HANA软件时设置的数据库用户名和密码。用户名固定为“SYSTEM“。

    **图 5**  System界面示例<a name="fig44232239224055"></a>  
    ![](figures/System界面示例.jpg "System界面示例")

8.  单击“Next“，然后单击“Finish“，SAP HANA Studio自动连接数据库。

    若连接失败，请检查SAP HANA节点上的数据库实例是否已处于运行状态。

9.  在“SAP HANA Administration Console“界面的“System“下，双击要检查的节点。
10. <a name="li420373224055"></a>在右侧界面中，单击“Landscape“页签，查看SAP HANA节点上的各个进程状态，如[图6](#fig14959789224055)所示。

    绿色表示状态正常。

    **图 6**  Landscape界面示例<a name="fig14959789224055"></a>  
    ![](figures/Landscape界面示例.jpg "Landscape界面示例")

11. 在SAP HANA Studio上，接入另外一台SAP HANA节点。

    请参见[5](#li5088100224055)～[10](#li420373224055)，将另外一台SAP HANA节点接入到SAP HANA Studio。


