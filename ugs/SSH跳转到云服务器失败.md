# SSH跳转到云服务器失败<a name="saphana_02_0063"></a>

## 问题描述<a name="section17904250171325"></a>

在一台Linux操作系统的云服务器上，通过SSH跳转到其他Linux操作系统的云服务器时，提示跳转失败。

界面提示信息示例如下：

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
The fingerprint for the RSA key sent by the remote host is
2c:d0:17:8a:82:4c:23:d6:14:be:d0:1d:88:8b:8b:03 [MD5].
Please contact your system administrator.
Add correct host key in /root/.ssh/known_hosts to get rid of this message.
Offending ECDSA key in /root/.ssh/known_hosts:1
You can use following command to remove all keys for this IP:
ssh-keygen -R fanhana-0002 -f /root/.ssh/known_hosts
RSA host key for fanhana-0002 has changed and you have requested strict checking.
Host key verification failed.

```

## 可能原因<a name="section50053646171330"></a>

跳转到的目标云服务器上的OpenSSH被重装了、IP地址或主机名称发生变化，或其他原因，导致跳转失败。

## 处理方法<a name="section38560614171337"></a>

通过删除本端的“known\_hosts“文件，解决此问题。

1.  在本云服务器上，以“root“用户，进入到命令行界面。
2.  删除“known\_hosts“文件。

    **rm /root/.ssh/known\_hosts**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >删除文件后，重新以SSH跳转到目标云服务器时，会显示fingerprint信息，并提示“Are you sure you want to continue connecting \(yes/no\)?“，此时，需要输入“yes“并继续执行跳转。  


