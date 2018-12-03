# 创建SFS<a name="saphana_02_0075"></a>

在SAP HANA系统中，Backup卷由SFS提供时，需要创建一个SFS，提供共享路径给SAP  HANA节点。

## 操作步骤<a name="section146737317815"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0113383875.jpg)图标，选择区域和项目。
3.  单击“服务列表 \> 存储 \> 弹性文件服务“，进入“弹性文件服务”管理界面。
4.  在右侧界面中，单击“创建文件系统”，系统弹出创建文件系统的界面。
5.  输入参数信息，如[表1](#table14401713165211)所示。

    **表 1**  弹性云服务器参数说明

    <a name="table14401713165211"></a>
    <table><thead align="left"><tr id="row19543171335217"><th class="cellrowborder" valign="top" width="35%" id="mcps1.2.3.1.1"><p id="p1054361305217"><a name="p1054361305217"></a><a name="p1054361305217"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="65%" id="mcps1.2.3.1.2"><p id="p95431813195218"><a name="p95431813195218"></a><a name="p95431813195218"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1854341385217"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.3.1.1 "><p id="p15543171319523"><a name="p15543171319523"></a><a name="p15543171319523"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.3.1.2 "><p id="p105431913125211"><a name="p105431913125211"></a><a name="p105431913125211"></a>文件服务名称。</p>
    <p id="p17543151314524"><a name="p17543151314524"></a><a name="p17543151314524"></a>比如填写的是“sfs-backup”。</p>
    </td>
    </tr>
    <tr id="row1454331315215"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.3.1.1 "><p id="p2543121385217"><a name="p2543121385217"></a><a name="p2543121385217"></a>可用分区</p>
    </td>
    <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.3.1.2 "><p id="p85431513185212"><a name="p85431513185212"></a><a name="p85431513185212"></a>指定文件服务所在的可用分区，请根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row4543191315213"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.3.1.1 "><p id="p9543131335216"><a name="p9543131335216"></a><a name="p9543131335216"></a>类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.3.1.2 "><p id="p1354316137526"><a name="p1354316137526"></a><a name="p1354316137526"></a>文件服务类型，选择“NFS”。</p>
    </td>
    </tr>
    <tr id="row1754361325210"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.3.1.1 "><p id="p14543161395217"><a name="p14543161395217"></a><a name="p14543161395217"></a>虚拟私有云（VPC）</p>
    </td>
    <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.3.1.2 "><p id="p55431913165220"><a name="p55431913165220"></a><a name="p55431913165220"></a>请选择SAP HANA对应的虚拟私有云。</p>
    </td>
    </tr>
    <tr id="row054381315214"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.3.1.1 "><p id="p8543131313523"><a name="p8543131313523"></a><a name="p8543131313523"></a>总容量</p>
    </td>
    <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.3.1.2 "><p id="p654351375210"><a name="p654351375210"></a><a name="p654351375210"></a>单个文件系统的最大容量。具体要求请参见<a href="SAP-HANA节点规划.md">SAP HANA节点规划</a>的说明。</p>
    </td>
    </tr>
    <tr id="row1543111311524"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.3.1.1 "><p id="p754371315528"><a name="p754371315528"></a><a name="p754371315528"></a>数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.3.1.2 "><p id="p115431013145215"><a name="p115431013145215"></a><a name="p115431013145215"></a>1</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“确定“，等待任务创建成功，完成文件系统创建。
7.  返回“弹性文件服务”管理界面，根据文件系统名称找到已创建的文件系统，并在“共享路径”栏查询共享路径。
8.  登录SAP HANA节点查看“/etc/resolv.conf”文件是否配置DNS服务器的IP地址，如未配置需将DNS服务器的IP地址写入“/etc/resolv.conf”文件。

