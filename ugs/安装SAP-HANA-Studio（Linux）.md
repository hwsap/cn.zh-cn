# 安装SAP HANA Studio（Linux）<a name="saphana_02_0035"></a>

SAP HANA Studio提供对SAP HANA的管理功能。完成SAP  HANA节点的部署后，需要安装SAP HANA Studio，并将SAP HANA节点纳入到SAP HANA Studio中管理。

本节介绍在Linux操作系统上安装SAP HANA Studio。

## 前提条件<a name="section1553389185034"></a>

-   已准备好相关的资源，具体请参见资源准备相关章节。
-   已完成弹性云服务器的创建和磁盘格式化，并已完成SAP HANA的安装。
-   已关闭待安装SAP HANA Studio的云服务器上的防火墙。

## 操作步骤<a name="section2292411011547"></a>

1.  以“root“帐号和密钥文件登录绑定了弹性IP的SAP HANA Studio。
2.  将从SAP官网获取的安装包传至待安装SAP HANA Studio的云服务器的**/hana/shared**目录下并解压。

    进入到安装文件所在的目录。例如，安装文件在“/DATA\_UNITS/HDB\_STUDIO\_LINUX\_X86\_64“下

    **cd /DATA\_UNITS/HDB\_STUDIO\_LINUX\_X86\_64**

3.  给安装文件所在的目录配置权限。

    假设解压后的文件目录为“HDB\_STUDIO\_LINUX\_X86\_64“。

    **chmod 777 -R HDB\_STUDIO\_LINUX\_X86\_64**

4.  执行下述命令，进入到安装目录，并执行安装。系统弹出SAP HANA Studio安装界面。

    **./hdbsetup**

5.  <a name="li2577252022187"></a>选择安装路径，单击“Next“。
6.  在“Select Features“界面上，勾选待安装的Features，单击“Next“。

    建议选择所有Features。

7.  在“Review & Confirm“界面上确认所有信息无误后，单击“Install“。
8.  系统弹出安装界面，进行安装。安装完成后，提示“You have successfully installed the SAP HANA Studio.“。
9.  单击“Finish“，关闭安装向导界面。
10. <a name="li716794012226"></a>进入[5](#li2577252022187)选择的安装路径，编辑hdbstudio.ini文件，在后面增加参数配置GTK版本。

    **vi hdbstudio.ini**

    增加如下参数：

    **--launcher.GTK\_version**

    **2**

    示例如下：

    ```
    -startup
    plugins/org.eclipse.equinox.launcher_1.3.201.v20161025-1711.jar
    --launcher.library
    plugins/org.eclipse.equinox.launcher.gtk.linux.x86_64_1.1.401.v20161122-1740
    --launcher.GTK_version
    2
    --launcher.XXMaxPermSize
    512m
    ```

11. （可选）如未配置**[10](#li716794012226)**，需在linux上启动hdbstudio之前执行以下操作。

    **export SWT\_GTK3=0**

    **./hdbstudio**


