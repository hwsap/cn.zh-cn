# 配置iSCSI（跨AZ部署HA）<a name="saphana_02_0074"></a>

## 操作场景<a name="section43028771171332"></a>

该操作只在跨AZ部署HA场景下才需要执行。

EVS无法实现跨AZ磁盘共享，所以在跨AZ部署HA场景中，需要规划三台弹性云服务器，在每台云服务器上各绑定一块SCSI盘并配置iSCSI用作SBD卷。云服务器配置如[表1](#table56428126113627)所示。

如果系统内SAP NetWeaver跨3个AZ，则每个AZ内创建一台云服务器。如果系统内SAP NetWeaver跨2个AZ，则其中一个AZ内创建一台云服务器，另一个AZ内创建两台云服务器且这三台云服务器必须属于同一个云服务器组。

**表 1**  云服务器配置

<a name="table56428126113627"></a>
<table><tbody><tr id="row20051718113627"><th class="firstcol" valign="top" width="16.17%" id="mcps1.2.3.1.1"><p id="p55079186113627"><a name="p55079186113627"></a><a name="p55079186113627"></a>操作系统</p>
</th>
<td class="cellrowborder" valign="top" width="83.83%" headers="mcps1.2.3.1.1 "><p id="p32229043113627"><a name="p32229043113627"></a><a name="p32229043113627"></a>SUSE Linux Enterprise Server (SLES) 12 SP1</p>
</td>
</tr>
<tr id="row21625934113627"><th class="firstcol" valign="top" width="16.17%" id="mcps1.2.3.2.1"><p id="p6870255113627"><a name="p6870255113627"></a><a name="p6870255113627"></a>规格</p>
</th>
<td class="cellrowborder" valign="top" width="83.83%" headers="mcps1.2.3.2.1 "><p id="p58390385151531"><a name="p58390385151531"></a><a name="p58390385151531"></a>s1.medium（1 vCPUs，4 GB内存）</p>
</td>
</tr>
<tr id="row42360666113627"><th class="firstcol" valign="top" width="16.17%" id="mcps1.2.3.3.1"><p id="p8661934113627"><a name="p8661934113627"></a><a name="p8661934113627"></a>磁盘</p>
</th>
<td class="cellrowborder" valign="top" width="83.83%" headers="mcps1.2.3.3.1 "><p id="p30528017113627"><a name="p30528017113627"></a><a name="p30528017113627"></a>系统盘：普通IO。</p>
<p id="p4370299145929"><a name="p4370299145929"></a><a name="p4370299145929"></a>数据盘：普通IO，10GB，SCSI，非共享盘。</p>
</td>
</tr>
</tbody>
</table>

## 前提条件<a name="section10115228171341"></a>

已成功创建三台弹性云服务器。

## 操作步骤<a name="section48857287171351"></a>

**软件安装**

>![](public_sys-resources/icon-note.gif) **说明：**   
>安装软件前请更新软件源。命令如下：  
>**zypper ar --refresh**_软件源网络地址_  

1.  执行以下命令，在服务端\(三台云服务器\)安装open-iscsi。

    **zypper in open-iscsi yast2-iscsi-lio-server targetcli**

2.  执行以下命令，在客户端（SAP HANA节点）安装open-iscsi。

    **zypper in open-iscsi**


**服务端配置**

1.  登录其中一台服务端云服务器。
2.  <a name="li57951583172559"></a>执行以下命令，配置服务自启动。

    **systemctl enable targetcli**

    **systemctl enable target**

3.  <a name="li15717292191850"></a>使用/dev/sda盘，创建一个iblock设备，名称为stonith\_bd，

    **targetcli /backstores/iblock create stonith\_bd** _/dev/sda_

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >_/dev/sda_为数据盘盘符，请根据实际情况配置。  

4.  查询iSCSI的iqn号。

    **iscsi-iname**

    回显如下所示：

    ```
    iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5
    ```

5.  指定查询到的的iqn号来创建target。

    **targetcli /iscsi create  _查询到的iqn号_**

    回显如下所示：

    ```
    server:~ # targetcli /iscsi create iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5
    Created target iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5.
    Selected TPG Tag 1.
    Created TPG 1.
    ```

6.  <a name="li2828904594221"></a>创建lun

    **targetcli /iscsi/**_iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_**/tpg1/luns create** _/backstores/iblock/stonith\_bd_

    回显如下所示：

    ```
    server:~ # targetcli /iscsi/iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5/tpg1/luns create /backstores/fileio/stonith_bd
    Selected LUN 0.
    Created LUN 0.
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   _iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_是iqn编号 ，可通过**targetcli ls**命令查看  
    >-   _/backstores/iblock/stonith\_bd_ 为[5](#li15717292191850)创建的iblock设备。  

7.  创建portal。

    **targetcli /iscsi/**_iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_**/tpg1/portals create**

    回显如下所示：

    ```
    server:~ # targetcli /iscsi/iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5/tpg1/portals create
    Using default IP port 3260
    Automatically selected IP address 192.168.124.10.
    Created network portal 192.168.124.10:3260.
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >**/**_iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_为[8](#li2828904594221)中的iqn编号 。  

8.  创建ACL。
    1.  查看initiatorname.iscsi文件，获取InitiatorName。

        **cat /etc/iscsi/initiatorname.iscsi**

        ```
        server:~ #cat /etc/iscsi/initiatorname.iscsi
        InitiatorName=iqn.1996-04.de.suse:01:f3cdb3b6ea6a
        ```

    2.  使用正确的InitiatorName，创建ACL。

        **targetcli /iscsi/**_iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_**/tpg1/acls create** _iqn.1996-04.de.suse:01:f3cdb3b6ea6a_


9.  关闭鉴权。

    **targetcli /iscsi/**_iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_**/tpg1 set attribute authentication=0**

10. <a name="li1273213710027"></a>保存配置。

    **targetcli saveconfig**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如果报错，请根据提示找到报错位置，将括号里的“.aslist\(\)“删除，然后重新保存配置。  

11. 登录另两台服务端云服务器，重复执行[4](#li57951583172559)到[12](#li1273213710027)完成三台云服务器的服务端配置。

**客户端配置**

1.  <a name="li2832593910361"></a>登录一台SAP HANA节点，挂载一台服务端的iSCSI盘。

    **iscsiadm -m discovery -t sendtargets -p** _10.0.3.250_**:3260**

    **iscsiadm -m node -p** _10.0.3.250_**:3260 --login**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   _10.0.3.250_为服务端IP地址，3260为iSCSI的默认端口。  
    >-   需要挂载三台服务端的iSCSI盘。  
    >-   可以通过**fdisk –l**命令查看到新增的磁盘。  

2.  <a name="li63245585104441"></a>设置iSCSI开机自动挂载。

    **iscsiadm -m node -T** _iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_ **-p 10.0.3.250 --op update -n node.startup -v automatic**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   _iqn.2003-01.org.linux-iscsi.scsi-0003.x8664:sn.38370da481a5_为[8](#li2828904594221)中的iqn编号 。  
    >-   _10.0.3.250_为服务端IP地址。  

3.  登录其他SAP HANA节点，重复执行[14](#li2832593910361)到[15](#li63245585104441)，完成所有客户端配置。

