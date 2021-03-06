# 格式化磁盘<a name="saphana_02_0041"></a>

单节点部署场景下，SAP HANA节点的数据磁盘需要进行格式化，并挂载到相应的目录后，才能被正常使用。

## 操作步骤<a name="se1837915431647048e017c4175c77f45"></a>

**E1、E2型弹性云服务器磁盘格式化**

1.  登录SAP HANA节点。

    使用PuTTY软件，以“root“帐号和密钥文件（“.ppk“文件）为鉴权方式，登录绑定了弹性IP的NAT Server，并通过SSH协议，跳转到SAP HANA节点。

2.  <a name="li59311527223019"></a>查看未格式化的磁盘

    在命令行界面，执行以下命令，查看未格式化的磁盘。

    **fdisk -l**

    根据磁盘空间大小，确定/usr/sap卷、Data卷、Log卷、Shared卷的磁盘。

3.  创建磁盘目录。

    **mkdir -p /hana/log /hana/data /hana/shared /hana/backup /usr/sap**

4.  格式化磁盘和逻辑卷，此处磁盘以“dev/xvdb”、“dev/xvdc”、“dev/xvdd”和“dev/xvde”为例。

    **mkfs.xfs** _/dev/xvdb_

    **mkfs.xfs** _/dev/xvdc_

    **mkfs.xfs** _/dev/xvdd_

    **mkfs.xfs** _/dev/xvde_

5.  将磁盘的挂载关系写入“/etc/fstab”文件中。
    1.  查看磁盘的UUID。

        **blkid**

    2.  获取在[创建SFS](创建SFS.md#li105431713125218)时查询到的共享路径，此处以“_PublicCloudAddress:/share-d6c6d9e2_”为例。
    3.  将磁盘对应的UUID或共享路径的挂载关系写入“/etc/fstab”文件中，此处UUID仅为示例。

        **echo "UUID=**_ba1172ee-39b2-4d28-89b8-282ebabfe8f4_ **/hana/data xfs defaults 0 0" \>\>/etc/fstab**

        **echo "UUID=**_d21734c9-44c0-45f7-a37d-02232e97fd3b_ **/hana/log xfs defaults 0 0" \>\>/etc/fstab**

        **echo "UUID=**_191b5369-9544-432f-9873-1beb2bd01de5_ **/hana/shared xfs defaults 0 0" \>\>/etc/fstab**

        **echo "UUID=**_5591b568-6324-475d-9654-1_e97f_bd0_2eba__ **/usr/sap xfs defaults 0 0" \>\>/etc/fstab**

        **echo "**__PublicCloudAddress_:/share-d6c6d9e2_ **/hana/backup nfs noatime,nodiratime,rdirplus,vers=3,wsize=1048576,rsize=1048576,noacl,nocto,proto=tcp,async 0 0" \>\>/etc/fstab**


6.  <a name="li4264133362317"></a>挂载所有磁盘。

    **mount -a**

7.  格式化另外一台服务器的磁盘。

    在本机通过SSH协议跳转到另外一台SAP HANA节点，参见[2](#li59311527223019)～[6](#li4264133362317)进行磁盘格式化操作。


**ET2、E3型弹性云服务器磁盘格式化**

1.  登录SAP  HANA节点。

    使用PuTTY软件，以“root“帐号和密钥文件（“.ppk“文件）为鉴权方式，登录绑定了弹性IP的NAT Server，并通过SSH协议，跳转到SAP HANA节点。

2.  <a name="li2330923895910"></a>查看未格式化的磁盘

    在命令行界面，执行以下命令，查看未格式化的磁盘。

    **fdisk -l**

    根据磁盘空间大小，确定/usr/sap卷、Data卷、Log卷、Shared卷的磁盘。

3.  创建磁盘目录。

    **mkdir -p /hana/log /hana/data /hana/shared /hana/backup /usr/sap**

4.  执行LVM功能划分Data卷，此处以“dev/vdb”和“dev/vdc”为例。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >ET2型弹性云服务器磁盘名称以“dev/xvdb”和“dev/xvdc”为例。  

    1.  创建物理卷。

        **pvcreate** _/dev/__vdb_ _/dev/vdc_

    2.  创建卷组。

        **vgcreate vghana** _/dev/__vdb /dev/vdc_

    3.  查询卷组的可用容量信息。

        **vgdisplay vghana**

    4.  创建逻辑卷，此处以2块EVS卷为例。

        **lvcreate -n lvhanadata -i** _2_ **-I** _256_ **-L** _348G_ **vghana**


5.  格式化磁盘和逻辑卷，此处磁盘以“dev/vdd”、“dev/vde”和“dev/vdf”为例。

    **mkfs.xfs** _/dev/vdd_

    **mkfs.xfs** _/dev/vde_

    **mkfs.xfs** _/dev/vdf_

    **mkfs.xfs /dev/mapper/vghana-lvhanadata**

6.  将磁盘的挂载关系写入“/etc/fstab”文件中。
    1.  查看磁盘的UUID。

        **blkid**

    2.  获取在[创建SFS](创建SFS.md#li105431713125218)时查询到的共享路径，此处以“_PublicCloudAddress:/share-d6c6d9e2_”为例。
    3.  将磁盘对应的UUID或共享路径的挂载关系写入“/etc/fstab”文件中，此处UUID仅为示例。

        **echo "UUID=**_ba1172ee-39b2-4d28-89b8-282ebabfe8f4_ **/hana/data xfs defaults 0 0" \>\>/etc/fstab**

        **echo "UUID=**_d21734c9-44c0-45f7-a37d-02232e97fd3b_ **/hana/log xfs defaults 0 0" \>\>/etc/fstab**

        **echo "UUID=**_191b5369-9544-432f-9873-1beb2bd01de5_ **/hana/shared xfs defaults 0 0" \>\>/etc/fstab**

        **echo "UUID=**_191b5369-9544-432f-9873-1beb2bd01de5_ **/usr/sap xfs defaults 0 0" \>\>/etc/fstab**

        **echo "**_PublicCloudAddress:/share-d6c6d9e2_ **/hana/backup nfs noatime,nodiratime,rdirplus,vers=3,wsize=1048576,rsize=1048576,noacl,nocto,proto=tcp,async 0 0" \>\>/etc/fstab**


7.  <a name="li5836476310114"></a>挂载所有磁盘。

    **mount -a**

8.  格式化另外一台服务器的磁盘。

    在本机通过SSH协议跳转到另外一台SAP HANA节点，参见[2](#li2330923895910)～[7](#li5836476310114)进行磁盘格式化操作。


