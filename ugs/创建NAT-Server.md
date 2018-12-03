# 创建NAT Server<a name="saphana_02_0028"></a>

在SAP HANA系统中，需要创建一台弹性云服务器，用于作为NAT  Server，用户可通过访问该服务器后，再通过ssh协议跳转到SAP  HANA节点进行故障诊断、问题定位等处理。

## 操作步骤<a name="section854176102817"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0113383875.jpg)图标，选择区域和项目。
3.  单击“服务列表 \> 计算 \> 弹性云服务器“，进入“弹性云服务器“管理界面。
4.  在右侧界面中，单击“购买弹性云服务器“，系统弹出创建弹性云服务器的界面。
5.  根据界面提示输入参数信息，如[表1](#table170336122514)所示。

    **表 1**  弹性云服务器参数说明

    <a name="table170336122514"></a>
    <table><thead align="left"><tr id="row2517923322514"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p5662853922514"><a name="p5662853922514"></a><a name="p5662853922514"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p2350898022514"><a name="p2350898022514"></a><a name="p2350898022514"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6645201511515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p5497520211536"><a name="p5497520211536"></a><a name="p5497520211536"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2380639311536"><a name="p2380639311536"></a><a name="p2380639311536"></a>根据实际选择，建议选择“包年/包月”。</p>
    </td>
    </tr>
    <tr id="row560038322514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p62582762172350"><a name="p62582762172350"></a><a name="p62582762172350"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6012028622514"><a name="p6012028622514"></a><a name="p6012028622514"></a>指定云服务器所在的可用分区，请根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row1106986222514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2391227617246"><a name="p2391227617246"></a><a name="p2391227617246"></a>规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p5730347522514"><a name="p5730347522514"></a><a name="p5730347522514"></a>在“全部系列”下选择“s1.medium”（1 vCPUs，4GB内存）或更大的规格。</p>
    </td>
    </tr>
    <tr id="row6513603522514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p37379988172410"><a name="p37379988172410"></a><a name="p37379988172410"></a>镜像</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p34745730195316"><a name="p34745730195316"></a><a name="p34745730195316"></a>选择<span class="parmvalue" id="parmvalue45189879195316"><a name="parmvalue45189879195316"></a><a name="parmvalue45189879195316"></a>“公共镜像”</span>，并根据需要选择具体的镜像。</p>
    </td>
    </tr>
    <tr id="row6670880022514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p3433085172415"><a name="p3433085172415"></a><a name="p3433085172415"></a>磁盘</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p828010522514"><a name="p828010522514"></a><a name="p828010522514"></a>系统盘，40GB。</p>
    <p id="p950415804812"><a name="p950415804812"></a><a name="p950415804812"></a>磁盘具体要求请参见<a href="其他节点规划.md">其他节点规划</a>的说明。</p>
    </td>
    </tr>
    <tr id="row5759543722514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p4856704810403"><a name="p4856704810403"></a><a name="p4856704810403"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p5953487322514"><a name="p5953487322514"></a><a name="p5953487322514"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的虚拟私有云。</p>
    </td>
    </tr>
    <tr id="row676000810533"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1832942310539"><a name="p1832942310539"></a><a name="p1832942310539"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p828825610539"><a name="p828825610539"></a><a name="p828825610539"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的安全组。</p>
    </td>
    </tr>
    <tr id="row2270448322514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p3035152172423"><a name="p3035152172423"></a><a name="p3035152172423"></a>网卡</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6076113022514"><a name="p6076113022514"></a><a name="p6076113022514"></a>根据<a href="网络信息规划.md">网络信息规划</a>选择相应的网卡。</p>
    </td>
    </tr>
    <tr id="row5387068122514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p44704893172428"><a name="p44704893172428"></a><a name="p44704893172428"></a>弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p905975195357"><a name="p905975195357"></a><a name="p905975195357"></a>根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row4974424222514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p53040779104122"><a name="p53040779104122"></a><a name="p53040779104122"></a>带宽</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1304169322514"><a name="p1304169322514"></a><a name="p1304169322514"></a>仅在绑定弹性IP后，需要配置。用于指定弹性IP对应的通信通道的网络带宽，请根据需要选择，例如30M。</p>
    <p id="p26858828195421"><a name="p26858828195421"></a><a name="p26858828195421"></a>仅在<span class="parmname" id="parmname26103566195421"><a name="parmname26103566195421"></a><a name="parmname26103566195421"></a>“弹性IP”</span>参数选择为<span class="parmvalue" id="parmvalue36057227195421"><a name="parmvalue36057227195421"></a><a name="parmvalue36057227195421"></a>“现在购买”</span>时，需要指定，请根据实际需要指定。</p>
    </td>
    </tr>
    <tr id="row2832308422514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p58467902104710"><a name="p58467902104710"></a><a name="p58467902104710"></a>密钥对</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p408090217431"><a name="p408090217431"></a><a name="p408090217431"></a>仅在<span class="parmname" id="parmname2507893617459"><a name="parmname2507893617459"></a><a name="parmname2507893617459"></a>“登录方式”</span>为<span class="parmvalue" id="parmvalue28317711753"><a name="parmvalue28317711753"></a><a name="parmvalue28317711753"></a>“密钥对”</span>时生效。</p>
    <p id="p24969197191558"><a name="p24969197191558"></a><a name="p24969197191558"></a>指使用SSH密钥证书作为弹性云服务器的鉴权方式。请先单击<span class="uicontrol" id="uicontrol9239073191558"><a name="uicontrol9239073191558"></a><a name="uicontrol9239073191558"></a>“查看密钥对”</span>，在<span class="wintitle" id="wintitle10167478191558"><a name="wintitle10167478191558"></a><a name="wintitle10167478191558"></a>“密钥对”</span>页面创建密钥。</p>
    <p id="p5992276622514"><a name="p5992276622514"></a><a name="p5992276622514"></a>需要指出的是，SAP HANA、SAP HANA Studio和NAT Server所使用的云服务器，必须指定同一份密钥，否则会导致后续SAP HANA无法正常安装。</p>
    <div class="note" id="note4840292822514"><a name="note4840292822514"></a><a name="note4840292822514"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p243398822514"><a name="p243398822514"></a><a name="p243398822514"></a>如果您直接从下拉列表中选择已有的SSH密钥证书，请确保您已在本地获取该文件，否则，将影响您正常登录弹性云服务器。</p>
    <p id="p2190589622514"><a name="p2190589622514"></a><a name="p2190589622514"></a>如果您在SSH密钥页面创建密钥，则其创建方法为：单击<span class="uicontrol" id="uicontrol61495284192318"><a name="uicontrol61495284192318"></a><a name="uicontrol61495284192318"></a>“查看密钥对”</span>后，在弹出的界面中单击<span class="uicontrol" id="uicontrol1341147192318"><a name="uicontrol1341147192318"></a><a name="uicontrol1341147192318"></a>“创建密钥对”</span>，输入密钥名称后单击<span class="uicontrol" id="uicontrol38172364192318"><a name="uicontrol38172364192318"></a><a name="uicontrol38172364192318"></a>“确定”</span>，并在系统弹出的提示框中单击<span class="uicontrol" id="uicontrol44584082192318"><a name="uicontrol44584082192318"></a><a name="uicontrol44584082192318"></a>“确定”</span>，然后根据提示信息查看并保存私钥即可。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row191542011057"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p441574710510"><a name="p441574710510"></a><a name="p441574710510"></a>云服务器名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2213121710510"><a name="p2213121710510"></a><a name="p2213121710510"></a>云服务器名称。</p>
    </td>
    </tr>
    <tr id="row350046622514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1265312622514"><a name="p1265312622514"></a><a name="p1265312622514"></a>数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1827031422514"><a name="p1827031422514"></a><a name="p1827031422514"></a>1</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“立即购买“，在弹出的界面中，勾选“我已经阅读并同意《华为镜像免责声明》”，单击“去支付”。
7.  单击“确认付款“。
8.  系统返回“弹性云服务器“管理界面，可在右侧界面的“任务状态“后面，查看当前创建任务的状态。

    弹性云服务器创建完成后，在右侧界面的服务器列表中可查看到对应的服务器。


