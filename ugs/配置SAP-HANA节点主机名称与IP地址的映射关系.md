# 配置SAP HANA节点主机名称与IP地址的映射关系<a name="saphana_02_0030"></a>

在SAP HANA的安装过程中，安装程序使用主机名称来进行通信。因此需要配置主机名称和IP地址的映射关系。

## 操作步骤<a name="section18158679194519"></a>

1.  使用PuTTY软件，以“root“帐号和密钥文件（“.ppk“文件）为鉴权方式，登录绑定了弹性IP的NAT Server，并通过SSH协议，跳转到一台待安装SAP HANA的服务器。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >在集群场景下，跳转到第一台待安装SAP HANA的服务器上。后续安装SAP HANA时，将在该服务器上执行相应的安装操作。  

2.  进入命令行界面，执行以下命令，进入hosts文件。

    **vi /etc/hosts**

3.  按“i”键，进入编辑模式，将所有的SAP HANA节点的主机名称和IP地址写入到hosts文件中。

    -   此处的IP地址，单节点无HA部署时为SAP HANA节点上业务/客户端平面的IP地址，单节点HA部署时为System Replication平面的IP地址。
    -   Full-Quallified-Hostname和Short-Hostname均为服务器的host名称，例如“hana001”

    格式为：**IP-Address Full-Quallified-Hostname Short-Hostname**

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >在同一套SAP HANA系统中，要将所有SAP HANA节点的IP地址和主机名称的映射关系，写入到hosts文件中。  

    以两台SAP HANA节点HA部署，使用System Replication平面的IP地址为“10.0.4.2“～“10.0.4.3“为例。

    编辑后的内容示例如下

    ```
    ...   
    10.0.4.2 hana001 hana001
    10.0.4.3 hana002 hana002
    ```

4.  编辑完成后，按“Esc”键，输入“:x”，按“Enter”键后退出。
5.  （可选）将已配置过“/etc/hosts”文件传送给其他SAP HANA节点。

    命令格式如下：

    **scp /etc/hosts 对端IP地址:/etc/hosts**

    仅在单节点HA场景下需要操作。

    验证SAP HANA节点之间的SSH跳转。

    在待安装SAP HANA的节点上，通过SSH跳转到所有SAP HANA节点包括当前节点，确保跳转功能正常。

    假设对端的SAP HANA节点主机名称为hana002。

    **ssh hana002**


