# 创建SAP HANA Studio Server<a name="saphana_02_0026"></a>

在SAP HANA系统中，需要创建一台弹性云服务器，用于运行SAP  HANA Studio软件。

## 操作步骤<a name="section854176102817"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0113383875.jpg)图标，选择区域和项目。
3.  单击“服务列表 \> 计算 \> 弹性云服务器“，进入“弹性云服务器“管理界面。
4.  在右侧界面中，单击“购买弹性云服务器“，系统弹出创建弹性云服务器的界面。
5.  输入参数信息，如[表1](#table5714121922432)所示。

    **表 1**  弹性云服务器参数说明

    <a name="table5714121922432"></a>
    <table><thead align="left"><tr id="row2404207722432"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p5678179322432"><a name="p5678179322432"></a><a name="p5678179322432"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p3592250922432"><a name="p3592250922432"></a><a name="p3592250922432"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2180120822432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p4980637811139"><a name="p4980637811139"></a><a name="p4980637811139"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2477731311139"><a name="p2477731311139"></a><a name="p2477731311139"></a>根据实际选择，建议选择“包年/包月”。</p>
    </td>
    </tr>
    <tr id="row4628863622432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p62582762172350"><a name="p62582762172350"></a><a name="p62582762172350"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p5538918522432"><a name="p5538918522432"></a><a name="p5538918522432"></a>指定云服务器所在的可用分区，请根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row3214653422432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2391227617246"><a name="p2391227617246"></a><a name="p2391227617246"></a>vCPU和内存</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p4265059922432"><a name="p4265059922432"></a><a name="p4265059922432"></a>在“全部系列”下选择“s1.xlarge”（4 vCPUs，16 GB内存）</p>
    </td>
    </tr>
    <tr id="row1075206722432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p37379988172410"><a name="p37379988172410"></a><a name="p37379988172410"></a>镜像</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p54384244191338"><a name="p54384244191338"></a><a name="p54384244191338"></a>选择<span class="parmvalue" id="parmvalue43047620191338"><a name="parmvalue43047620191338"></a><a name="parmvalue43047620191338"></a>“公共镜像”</span>，并根据需要选择具体的镜像。</p>
    </td>
    </tr>
    <tr id="row3825419922432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p3433085172415"><a name="p3433085172415"></a><a name="p3433085172415"></a>磁盘</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1289984122432"><a name="p1289984122432"></a><a name="p1289984122432"></a>系统盘，80GB。</p>
    <p id="p119321048473"><a name="p119321048473"></a><a name="p119321048473"></a>磁盘具体要求请参见<a href="其他节点规划.md">其他节点规划</a>的说明。</p>
    </td>
    </tr>
    <tr id="row2479579522432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p4856704810403"><a name="p4856704810403"></a><a name="p4856704810403"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6575797522432"><a name="p6575797522432"></a><a name="p6575797522432"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的虚拟私有云。</p>
    </td>
    </tr>
    <tr id="row3518875095937"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p6375405595946"><a name="p6375405595946"></a><a name="p6375405595946"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6380484595946"><a name="p6380484595946"></a><a name="p6380484595946"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的安全组。</p>
    </td>
    </tr>
    <tr id="row560641522432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p3035152172423"><a name="p3035152172423"></a><a name="p3035152172423"></a>网卡</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1332528622432"><a name="p1332528622432"></a><a name="p1332528622432"></a>根据<a href="网络信息规划.md">网络信息规划</a>选择相应的网卡。</p>
    </td>
    </tr>
    <tr id="row4685898022432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p44704893172428"><a name="p44704893172428"></a><a name="p44704893172428"></a>弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p14935784104159"><a name="p14935784104159"></a><a name="p14935784104159"></a>根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row1036992122432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p53040779104122"><a name="p53040779104122"></a><a name="p53040779104122"></a>带宽</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p63698060104240"><a name="p63698060104240"></a><a name="p63698060104240"></a>仅在<span class="parmname" id="parmname1723177104318"><a name="parmname1723177104318"></a><a name="parmname1723177104318"></a>“弹性IP”</span>参数选择为<span class="parmvalue" id="parmvalue39814096104329"><a name="parmvalue39814096104329"></a><a name="parmvalue39814096104329"></a>“现在购买”</span>时，需要指定，请根据实际需要指定。</p>
    </td>
    </tr>
    <tr id="row5580458522432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p58467902104710"><a name="p58467902104710"></a><a name="p58467902104710"></a>密钥对</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p408090217431"><a name="p408090217431"></a><a name="p408090217431"></a>仅在<span class="parmname" id="parmname2507893617459"><a name="parmname2507893617459"></a><a name="parmname2507893617459"></a>“登录方式”</span>为<span class="parmvalue" id="parmvalue28317711753"><a name="parmvalue28317711753"></a><a name="parmvalue28317711753"></a>“密钥对”</span>时生效。</p>
    <p id="p24969197191558"><a name="p24969197191558"></a><a name="p24969197191558"></a>指使用SSH密钥证书作为弹性云服务器的鉴权方式。请先单击<span class="uicontrol" id="uicontrol9239073191558"><a name="uicontrol9239073191558"></a><a name="uicontrol9239073191558"></a>“查看密钥对”</span>，在<span class="wintitle" id="wintitle10167478191558"><a name="wintitle10167478191558"></a><a name="wintitle10167478191558"></a>“密钥对”</span>页面创建密钥。</p>
    <p id="p3219656622432"><a name="p3219656622432"></a><a name="p3219656622432"></a>需要指出的是，SAP HANA、<span class="keyword" id="keyword1453953974918"><a name="keyword1453953974918"></a><a name="keyword1453953974918"></a>SAP HANA Studio</span>和NAT Server所使用的云服务器，必须指定同一份密钥，否则会导致后续SAP HANA无法正常安装。</p>
    <div class="note" id="note897399022432"><a name="note897399022432"></a><a name="note897399022432"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p2133364522432"><a name="p2133364522432"></a><a name="p2133364522432"></a>如果您直接从下拉列表中选择已有的SSH密钥证书，请确保您已在本地获取该文件，否则，将影响您正常登录弹性云服务器。</p>
    <p id="p5778507922432"><a name="p5778507922432"></a><a name="p5778507922432"></a>如果您在SSH密钥页面创建密钥，则其创建方法为：</p>
    <p id="p26269104192317"><a name="p26269104192317"></a><a name="p26269104192317"></a>单击<span class="uicontrol" id="uicontrol61495284192318"><a name="uicontrol61495284192318"></a><a name="uicontrol61495284192318"></a>“查看密钥对”</span>后，在弹出的界面中单击<span class="uicontrol" id="uicontrol1341147192318"><a name="uicontrol1341147192318"></a><a name="uicontrol1341147192318"></a>“创建密钥对”</span>，输入密钥名称后单击<span class="uicontrol" id="uicontrol38172364192318"><a name="uicontrol38172364192318"></a><a name="uicontrol38172364192318"></a>“确定”</span>，并在系统弹出的提示框中单击<span class="uicontrol" id="uicontrol44584082192318"><a name="uicontrol44584082192318"></a><a name="uicontrol44584082192318"></a>“确定”</span>，然后根据提示信息查看并保存私钥即可。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row3942762211129"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p5792122111146"><a name="p5792122111146"></a><a name="p5792122111146"></a>云服务器名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6110733811146"><a name="p6110733811146"></a><a name="p6110733811146"></a>云服务器的名称。</p>
    </td>
    </tr>
    <tr id="row230140451121"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p521983391121"><a name="p521983391121"></a><a name="p521983391121"></a>购买时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2071031121"><a name="p2071031121"></a><a name="p2071031121"></a>根据实际选择。</p>
    </td>
    </tr>
    <tr id="row4380500922432"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p12910061172441"><a name="p12910061172441"></a><a name="p12910061172441"></a>数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p5522209922432"><a name="p5522209922432"></a><a name="p5522209922432"></a>1</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“立即购买“，在弹出的界面中，勾选“我已经阅读并同意《华为镜像免责声明》”，单击“去支付”。
7.  单击“确认付款“。
8.  系统返回“弹性云服务器“管理界面，可在右侧界面的“任务状态“后面，查看当前创建任务的状态。

    弹性云服务器创建完成后，在右侧界面的服务器列表中可查看到对应的服务器。


