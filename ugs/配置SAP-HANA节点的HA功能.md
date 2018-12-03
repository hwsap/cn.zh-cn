# 配置SAP HANA节点的HA功能<a name="saphana_02_0051"></a>

通过配置脚本，实现SAP HANA节点的HA功能（即HAE功能），提高SAP  HANA节点的可靠性。

仅在SAP HANA节点的操作系统为SUSE Linux Enterprise Server \(SLES\) 12 SP1 for SAP及以上时支持自动切换，才需要配置该脚本。

在跨AZ部署HA场景中，需要规划三台云服务器，并将磁盘配置iSCSI实现共享存储用作SBD卷。详情请参考[配置iSCSI（跨AZ部署HA）](配置iSCSI（跨AZ部署HA）.md)。

## 前提条件<a name="section60116077105642"></a>

已在SAP HANA节点之间进行过相互的SSH跳转操作。

## 操作步骤<a name="section26679172112337"></a>

1.  将SBD卷绑定给另外一台SAP HANA节点。

    因为在创建其中一台SAP HANA节点时，绑定了SBD卷，因此需要将这个SBD卷，绑定给另外一台SAP HANA节点。

    1.  在管理控制台，单击“服务列表 \> 计算  \>  弹性云服务器“后，单击左侧“弹性云服务器“，在右侧可看到所有的云服务器。
    2.  根据云服务器名称，找到已绑定SBD卷的服务器，并单击云服务器的名称。
    3.  在弹出的详细信息列表中，在“云硬盘“页签上，找到SBD卷对应的磁盘，并单击数据盘。
    4.  <a name="li13794543224950"></a>在弹出的数据盘详细信息中，查看该数据盘的“挂载点“并记录，然后单击数据盘“ID“上的超链接。
    5.  在弹出的界面中，单击“挂载点“，单击“挂载“，弹出“挂载磁盘“界面
    6.  在“挂载磁盘“界面上，选中要绑定到的另外一台云服务器，并确保绑定到该云服务器的“挂载点“与[1.d](#li13794543224950)中的“挂载点“一致，完成磁盘的绑定。

2.  创建浮动IP。
    1.  在管理控制台，单击“服务列表 \> 计算  \>  弹性云服务器“，并单击左侧的“弹性云服务器“，进入“弹性云服务器“管理界面。
    2.  找到一台SAP HANA节点，并单击云服务器的名称，弹出云服务器的详细信息。
    3.  单击“网卡“页签，在云服务器的业务/管理平面网卡后，单击“管理私有IP地址“，弹出“虚拟IP地址“界面。
    4.  单击“申请虚拟IP地址“分配规划的浮动IP地址，在分配好的浮动IP栏单击“绑定服务器“，绑定给所需的云服务器，重复执行绑定操作给其他云服务器。

3.  下载脚本和配置文件。
    1.  使用PuTTY软件，以“root“帐号和密钥文件（“.ppk“文件）为鉴权方式，登录绑定了弹性IP的NAT Server，并通过SSH协议，跳转到待作为主节点的SAP HANA节点。
    2.  下载脚本和配置文件。

        **wget https://obs-sap.obs.myhwclouds.com/hana/cfgandscript/ha\_auto\_script.zip -P /hana/shared**


    1.  解压文件

        **cd /hana/shared**

        **unzip  **ha\_auto\_script**.zip**


4.  修改配置文件。

    **vi /hana/shared/**ha\_auto\_script**/hana\_ha.cfg**

    配置文件参数请根据实际信息进行填写，示例及说明如下：

    ```
    [masterNode]
    # Host name of the active node
    masterName=hana001                                                         
    # Heartbeat IP address of the active node
    masterHeartbeatIP1=10.0.4.2
    masterHeartbeatIP2=                             
                                                                            
    [slaveNode]
    # Host name of the standby node
    slaveName=hana002                                           
    # Heartbeat IP address of the standby node
    slaveHeartbeatIP1=10.0.4.3
    slaveHeartbeatIP2=                                         
    
    [trunkInfo]                                                                              
    # Floating IP address of SAP HANA
    hanaBusinessIP=10.0.3.103                                                                                                                                                                                                           
    [hanaInfo]                                                        
    # SBD volume path
    SBDDevice=/dev/sdc,/dev/sdd,/dev/sde                                                    
    # SAP HANA administrator account
    hanaUser=s00adm                                            
    # SAP HANA instance number
    InstanceNumber=00
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >此脚本支持配置双心跳网络平面功能，在配置此功能时需要将业务/客户端平面IP地址分别添加到脚本中的“masterHeartbeatIP2“和“slaveHeartbeatIP2“参数后。  
    >跨AZ场景中，需要将SBDDevice设置为三台云服务器上的SBD盘符。例如：SBDDevice=/dev/sbd1,/dev/sbd2,/dev/sbd3。  

5.  检查配置文件填写是否符合要求。

    **cd  **ha\_auto\_script****

    **chmod +x hana\_auto\_ha.sh**

6.  执行脚本。

    **sh hana\_auto\_ha.sh**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   脚本运行出错时会报错并退出，再次运行脚本之前，请务必使用**sh hana\_auto\_ha.sh unconf**  命令进行手动回退，且需要根据SBD卷的最新盘符配置“ha\_auto.cfg“文件。  
    >-   主备节点发生切换后，需要在切换后的备节点重新配置才能使HA机制生效，方法如下：  
    >    1 在备节点上，切换到管理员模式。  
    >    **su - <_SID_\>adm**  
    >    2 停止备节点。  
    >    **HDB stop**  
    >    3 将备节点注册到主节点上。  
    >    参数“secondary“配置为当前主节点的主机名，参数“site\_name“与切换前主节点定义（在配置System Replication时定义）的名称保持一致。  
    >    **hdbnsutil -sr\_register --remoteHost=<**_**secondary**_**\> --remoteInstance=<i**_**nstance\_number**_**\> --replicationMode=sync --name=<**_**site\_name**_**\>**  
    >    4 清理原主节点（即当前备节点）上的资源。  
    >    “rsc\_SAPHana\_SLE\_HDB00“为资源名称举例，可通过**crm\_mon - r1**查询获取，参数“primary“配置为当前备节点的主机名。  
    >    **exit**  
    >    **crm resource cleanup <**_**rsc\_SAPHana\_SLE\_HDB00**_**\> <**_**primary**_**\>**  

    配置成功后，返回报文如下：

    ```
    Online: [ hana001 hana002 ]
    
    Full list of resources:
    
     Clone Set: cln_SAPHanaTopology_SLE_HDB00 [rsc_SAPHanaTopology_SLE_HDB00]
         Started: [ hana001 hana002 ]
     rsc_ip_SLE_HDB00?(ocf::heartbeat:IPaddr2):?Started hana001
     stonith-sbd?(stonith:external/sbd):?Started hana001
     Master/Slave Set: msl_SAPHana_SLE_HDB00 [rsc_SAPHana_SLE_HDB00]
         Masters: [ hana001 ]
         Slaves: [ hana002 ]
    All Complete!
    
    ```

7.  在SAP HANA Studio上重新接入SAP HANA。
8.  在SAP HANA Studio上，将已接入的两个SAP HANA节点删除，重新通过SAP HANA节点的浮动IP地址，将SAP HANA节点接入，并配置备份路径。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >HA功能配置完成后，HAE会管理资源，请不要使用其他方式启动或停止资源。如果需要手动执行一些测试或者修改操作，请先将集群进入维护模式。  
    >**crm configure property maintenance-mode=true**  
    >修改完成后再退出维护模式。  
    >**crm configure property maintenance-mode=false**  
    >如果需要对节点进行关机或者重启等操作，请先手动关闭集群服务。  
    >**systemctl stop pacemaker**  


