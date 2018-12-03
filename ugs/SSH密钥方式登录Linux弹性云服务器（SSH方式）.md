# SSH密钥方式登录Linux弹性云服务器（SSH方式）<a name="saphana_02_0068"></a>

## 前提条件<a name="scc5214d4af784fd9a810a0a57d4c30c8"></a>

-   已获取该弹性云服务器的密钥文件。
-   弹性云服务器已经绑定弹性IP地址。

-   已配置安全组入方向的访问规则。

## Windows系统<a name="sa5239a049b8d4ebd92b1939747749a3b"></a>

如果您是在Windows操作系统上登录Linux，可以按照下面方式登录弹性云服务器。

以PuTTY为例介绍如何登录弹性云服务器，使用PuTTY登录弹性云服务器前需要先转化私钥格式。

1.  在下面路径中下载PuTTY和PuTTYgen。

    http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >PuTTYgen是密钥生成器，用于创建ssh密钥，生成一对公钥和私钥供PuTTY使用。  

2.  运行PuTTYgen。
3.  在“Actions“区域，单击“Load“，并导入创建弹性云服务器时保存的私钥文件。

    导入时注意确保导入的格式要求为“All files \(\*.\*\)“。

4.  单击“Save private key”。
5.  保存转化后的私钥到本地。例如：kp-123.ppk
6.  运行PuTTY。
7.  选择“Connection \> data”，在Auto-login username处输入：root。
8.  选择“Connection \> SSH \> Auth”，在最下面一个配置项“Private key file for authentication”中，单击“Browse”，选择步骤5转化的密钥。
9.  单击“Session”，在“Host Name \(or IP address\)”下的输入框中输入弹性云服务器的弹性IP地址。
10. 单击“Open”。

    登录弹性云服务器。


## Linux系统<a name="s7e42e58b864e425bbdc21fda5121ad3f"></a>

如果您是在Linux操作系统上登录Linux，可以按照下面方式登录。下面步骤以私钥文件是kp-123.pem为例进行介绍。

1.  在您的linux计算机的命令行中执行如下命令，变更权限。

    chmod 600 /_path_/kp-123

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >上述命令的path为密钥文件的存放路径。  

2.  执行如下命令登录弹性云服务器。

    ssh -i /_path_/kp-123 root@_弹性IP地址_

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   path为密钥文件的存放路径。  
    >-   弹性IP地址为弹性云服务器绑定的弹性IP地址。  


