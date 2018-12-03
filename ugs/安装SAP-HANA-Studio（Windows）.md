# 安装SAP HANA Studio（Windows）<a name="saphana_02_0034"></a>

SAP HANA  Studio提供对SAP HANA的管理功能。完成SAP  HANA节点的部署后，需要安装SAP HANA Studio，并将SAP HANA节点纳入到SAP HANA Studio中管理。

本节介绍在Windows操作系统上安装SAP HANA Studio。

## 前提条件<a name="section1553389185034"></a>

-   已准备好相关的资源，具体请参见资源准备相关章节。
-   已完成弹性云服务器的创建和磁盘格式化，并已完成SAP HANA的安装。
-   已关闭待安装SAP HANA Studio的云服务器上的防火墙。
-   已在待安装SAP HANA Studio的云服务器上打开允许远程登录的功能。

## 操作步骤<a name="section2292411011547"></a>

1.  以RDP协议，通过弹性IP地址，登录SAP HANA Studio的云服务器。

    登录待安装SAP HANA Studio的云服务器时，请以“Administrator“帐号，并以[获取Windows弹性云服务器的密码](获取Windows弹性云服务器的密码.md)中获取的密码登录。

2.  将从SAP官网获取的安装包传至待安装SAP HANA Studio的云服务器。
3.  解压安装包，进入到SAP HANA Studio所在的目录。
4.  在Windows界面下，进入到SAP HANA Studio安装文件包目录下，双击安装文件“hdbsetup.exe“，打开安装引导界面。
5.  选择安装路径，单击“Next“。
6.  在“Select Features“界面上，勾选待安装的Features，单击“Next“。

    建议选择所有Features。

7.  在“Review & Confirm“界面上确认所有信息无误后，单击“Install“。
8.  系统弹出安装界面，进行安装。安装完成后，提示“You have successfully installed the SAP HANA Studio.“。
9.  单击“Finish“，关闭安装向导界面。

