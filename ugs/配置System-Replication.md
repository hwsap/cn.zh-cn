# 配置System Replication<a name="saphana_02_0050"></a>

完成单节点HA的安装之后，需要配置System Replication功能。

>![](public_sys-resources/icon-note.gif) **说明：**   
>跨AZ/跨Region容灾场景中需要配置Multitier System Replication，在保证HA节点间的SR配置成功后，可进行Multitier System Replication的配置。  
>配置方案：HA备节点设置为Primary节点，DR节点设置为Secondary节点，与HA备节点进行数据同步。其中Multitier System Replication的配置模式为async。方案详情请参见[《SAP HANA高可用及灾备指南》](https://support.huaweicloud.com/hag-saphana/saphana_09_0008.html)。  

## 前提条件<a name="section47712019205457"></a>

-   在配置HA功能之前，必须已在两个SAP HANA节点上配置了备份机制并已进行了数据库的备份，操作请参见[配置备份路径](配置备份路径（单节点HA）.md)。
-   在配置HA功能前，务必确认已在[配置SAP HANA节点主机名称与IP地址的映射关系](配置SAP-HANA节点主机名称与IP地址的映射关系.md)中，已将两个SAP  HANA节点的IP和主机名称的映射关系，都写入两个SAP HANA节点的“/etc/hosts“文件中。

## 操作步骤<a name="section2015312113737"></a>

1.  配置主节点
    1.  使用PuTTY软件，以“root“帐号和密钥文件（“.ppk“文件）为鉴权方式，登录绑定了弹性IP的NAT Server，并通过SSH协议，跳转到待作为主节点的服务器。
    2.  在命令行界面，执行以下命令，进入管理员模式。

        **su - $**_**SID**_**adm**

        例如

        **su - s00adm**

        屏幕回显示例如下：

        ```
        hana001:/hana/shared/S00/HDB00>   
        ```

    3.  执行以下命令，将SAP HANA节点设置为主节点。

        命令格式如下，其中“siteA“为主节点的命名，自行定义即可。

        **hdbnsutil -sr\_enable --name=**_**siteA**_

        例如，主节点命名为“hana001“，则命令行如下：

        **hdbnsutil -sr\_enable --name=hana001**


2.  配置备节点
    1.  通过SSH跳转，登录另外一台SAP HANA节点。
    2.  执行以下命令，进入管理员模式。

        **su - $**_**SID**_**adm**

        例如

        **su - s00adm**

        屏幕回显示例如下：

        ```
        hana002:/hana/shared/S00/HDB00>  
        ```

    3.  执行以下命令，停止SAP HANA数据库。

        **HDB stop**

    4.  执行以下命令，打开System Replication功能。

        命令格式如下，其中“remoteHostName“为主节点的主机名称，“remoteInstanceNumber“为主节点的实例编号。“SiteB“为备节点的命名，自行定义即可。

        **hdbnsutil -sr\_register --remoteHost=_remoteHostName_  --remoteInstance=_remoteInstanceNumber_  --replicationMode=sync --name=_siteB_**

        例如，“remoteHostName“为“hana001“，“remoteInstanceNumber“为“00“，“SiteB“为“hana002“，则命令行如下：

        **hdbnsutil -sr\_register --remoteHost=hana001 --remoteInstance=00 --replicationMode=sync --name=hana002**

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >-   使用SAP HANA 2.0安装包时，如出现主备节点SSFS\_S00.DAT、SSFS\_S00.KEY两个文件差异，请参考SAP官方文档[SAP Note 2369981](https://launchpad.support.sap.com/#/notes/0002369981)解决。  
        >-   跨AZ容灾场景的Multitier System Replication配置模式为async，即“replicationMode=async“。  

    5.  启动SAP HANA数据库。

        **HDB start**


3.  查看SAP HANA系统的System Replication状态。
    1.  在主节点的命令行界面，管理员模式下，执行以下命令：

        **hdbnsutil -sr\_state**

        系统回显示例如下：

        ```
        checking for active or inactive nameserver ...
        System Replication State
        ~~~~~~~~~~~~~~~~~~~~~~~~
        mode: primary
        site id: 1
        site name: hana001
        Host Mappings:
        ~~~~~~~~~~~~~
        hana001 -> [hana001] hana001
        hana001 -> [hana002] hana002
        done.
        ```

    2.  在SAP HANA Studio上，查看主节点的状态信息。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >在实际应用场景下，业务端软件已与SAP HANA连接，若执行了手工切换SAP HANA节点的操作，需要在业务端软件侧同步修改SAP HANA节点对应的IP地址，并重启业务端软件。  



