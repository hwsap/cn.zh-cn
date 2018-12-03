# 配置SSH跳转权限<a name="saphana_02_0029"></a>

为了实现通过NAT Server可使用SSH协议跳转到SAP HANA节点的功能，以及SAP  HANA节点和NAT Server互相通过SSH协议跳转的功能，需要配置云服务器之间的互信。

## 操作步骤<a name="section11956953142555"></a>

1.  上传密钥文件到NAT Server。
    1.  在本地PC上，生成登录NAT Server的密钥文件。

        在创建NAT Server时，指定了NAT Server的证书密钥文件（“.pem“文件）。

        需要通过该密钥文件，生成密钥文件（“.ppk“文件）。请参见[SSH密钥方式登录Linux弹性云服务器（SSH方式）](SSH密钥方式登录Linux弹性云服务器（SSH方式）.md)中的相关描述生成密钥文件。

    2.  在本地PC上，安装WinSCP软件。
    3.  上传证书私钥文件（.pem文件）。

        使用WinSCP软件，以“root“帐号，以密钥文件（“.ppk“文件）为鉴权方式，将证书私钥文件（“.pem“文件），通过弹性IP地址，上传到NAT Server的“/usr“目录。

    4.  使用PuTTY软件，以“root“帐号和密钥文件（“.ppk“文件）为鉴权方式，登录NAT Server。
    5.  将证书私钥文件（.pem文件）复制到“/root/.ssh“目录，并改名为“id\_rsa“。

        假设原来的私钥名称为“private.pem“

        **cp /usr/private.pem /root/.ssh/id\_rsa**

        **cd /root/.ssh/**

        **chmod 600 id\_rsa**


2.  将本机上的私钥和“authorized\_keys“文件，通过业务/客户端平面IP地址，分发给除SAP HANA Studio之外的所有服务器。

    命令格式如下：

    **scp /root/.ssh/id\_rsa 对端的IP地址:/root/.ssh/id\_rsa**

    **scp /root/.ssh/authorized\_keys 对端的IP地址:/root/.ssh/**

    例如，对端IP地址为“10.0.3.102“：

    **scp /root/.ssh/id\_rsa 10.0.3.102:/root/.ssh/id\_rsa**

    **scp /root/.ssh/authorized\_keys 10.0.3.102:/root/.ssh/**

3.  验证跳转功能

    在NAT Server上，通过SSH跳转到除SAP HANA Studio之外的所有服务器上，确保跳转功能正常。

    以跳转到一台SAP HANA服务器为例，假设SAP HANA服务器的业务/客户端平面IP地址为“10.0.3.2“

    **ssh 10.0.3.2**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >进行跳转后，需要从对端跳转回NAT Server，并继续验证NAT Server跳转到其他节点的功能。  
    >首次跳转时会显示fingerprint信息，并提示“Are you sure you want to continue connecting \(yes/no\)?”，此时，需要输入“yes”并继续执行跳转。  


