# 创建SAP HANA节点<a name="saphana_02_0024"></a>

SAP HANA运行在HANA云服务器上。需要根据部署场景，创建一台或多台HANA云服务器，用于部署SAP  HANA软件。

请参见方案和数据规划相关章节，确定HANA云服务器数量及相关规划信息。

## 操作步骤<a name="section28521827213651"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0113383875.jpg)图标，选择区域和项目。
3.  单击“服务列表 \> 计算 \> 弹性云服务器“，进入“弹性云服务器“管理界面。
4.  在右侧界面中，单击“购买弹性云服务器“，系统弹出购买弹性云服务器的界面。
5.  根据界面提示，输入参数信息，如[表1](#table15048540213231)所示。

    **表 1**  HANA云服务器参数说明

    <a name="table15048540213231"></a>
    <table><thead align="left"><tr id="row36609903213231"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p11338703213231"><a name="p11338703213231"></a><a name="p11338703213231"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p46019721213231"><a name="p46019721213231"></a><a name="p46019721213231"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row49191815173125"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p56583456173136"><a name="p56583456173136"></a><a name="p56583456173136"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p19857206173136"><a name="p19857206173136"></a><a name="p19857206173136"></a>按需求选择计费方式，推荐使用“包年/包月”。</p>
    </td>
    </tr>
    <tr id="row23050208213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p43115582213231"><a name="p43115582213231"></a><a name="p43115582213231"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p2701244213231"><a name="p2701244213231"></a><a name="p2701244213231"></a>指定云服务器所在的可用分区，必须是支持SAP HANA的可用分区，请根据实际需要选择。</p>
    </td>
    </tr>
    <tr id="row45743662213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p6125286213231"><a name="p6125286213231"></a><a name="p6125286213231"></a>规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p42732086153926"><a name="p42732086153926"></a><a name="p42732086153926"></a>单击“超大内存型”，请根据实际需要选择，规格可参见<a href="SAP-HANA节点规划.md">SAP HANA节点规划</a>中的说明。</p>
    </td>
    </tr>
    <tr id="row35173131213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p27861758213231"><a name="p27861758213231"></a><a name="p27861758213231"></a>镜像</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p44344974213231"><a name="p44344974213231"></a><a name="p44344974213231"></a>请选择<span class="parmvalue" id="parmvalue42209921213231"><a name="parmvalue42209921213231"></a><a name="parmvalue42209921213231"></a>“公共镜像”</span>，选择对应的SAP HANA云服务器镜像。</p>
    </td>
    </tr>
    <tr id="row50316870213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p48122725213231"><a name="p48122725213231"></a><a name="p48122725213231"></a>磁盘</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p4699356994429"><a name="p4699356994429"></a><a name="p4699356994429"></a><span class="keyword" id="keyword13338175120815"><a name="keyword13338175120815"></a><a name="keyword13338175120815"></a>单节点</span>（无HA或HA场景）部署时，共需要一块系统盘和多块用户数据盘。</p>
    <p id="p1235031294247"><a name="p1235031294247"></a><a name="p1235031294247"></a>磁盘具体要求请参见<a href="SAP-HANA节点规划.md">SAP HANA节点规划</a>的说明。</p>
    <p id="p2659803510710"><a name="p2659803510710"></a><a name="p2659803510710"></a>若有特殊需求需要额外的磁盘，可单击<span class="uicontrol" id="uicontrol5651416510711"><a name="uicontrol5651416510711"></a><a name="uicontrol5651416510711"></a>“增加一块数据盘”</span>增加磁盘。</p>
    </td>
    </tr>
    <tr id="row48683788213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p50198650213231"><a name="p50198650213231"></a><a name="p50198650213231"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p20485142213231"><a name="p20485142213231"></a><a name="p20485142213231"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的VPC。</p>
    </td>
    </tr>
    <tr id="row51059121213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p35500916213231"><a name="p35500916213231"></a><a name="p35500916213231"></a>网卡</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p4738665295657"><a name="p4738665295657"></a><a name="p4738665295657"></a>请根据<a href="网络信息规划.md">网络信息规划</a>确定网卡个数。</p>
    <p id="p6539770695657"><a name="p6539770695657"></a><a name="p6539770695657"></a>若需添加，可单击<span class="uicontrol" id="uicontrol5170844995657"><a name="uicontrol5170844995657"></a><a name="uicontrol5170844995657"></a>“增加一块网卡”</span>增加磁盘。</p>
    <p id="p43255455213231"><a name="p43255455213231"></a><a name="p43255455213231"></a>。</p>
    <div class="note" id="note1047955195455"><a name="note1047955195455"></a><a name="note1047955195455"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul4699691895927"></a><a name="ul4699691895927"></a><ul id="ul4699691895927"><li>单节点部署（无HA）：无需添加扩展网卡。</li><li>单节点部署（HA）：添加扩展网卡后，执行去勾选“安全组不生效”。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row64611127173410"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2931256173422"><a name="p2931256173422"></a><a name="p2931256173422"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p36105188173422"><a name="p36105188173422"></a><a name="p36105188173422"></a>请使用<a href="申请子网并设置安全组.md">申请子网并设置安全组</a>中对应的安全组。</p>
    </td>
    </tr>
    <tr id="row57254421213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p56878911213231"><a name="p56878911213231"></a><a name="p56878911213231"></a>弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p43789078213231"><a name="p43789078213231"></a><a name="p43789078213231"></a>选择“暂不购买”。</p>
    </td>
    </tr>
    <tr id="row63518364213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p45527748213231"><a name="p45527748213231"></a><a name="p45527748213231"></a>密钥对</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p408090217431"><a name="p408090217431"></a><a name="p408090217431"></a>仅在<span class="parmname" id="parmname2507893617459"><a name="parmname2507893617459"></a><a name="parmname2507893617459"></a>“登录方式”</span>为<span class="parmvalue" id="parmvalue28317711753"><a name="parmvalue28317711753"></a><a name="parmvalue28317711753"></a>“密钥对”</span>时生效。</p>
    <p id="p37949614213231"><a name="p37949614213231"></a><a name="p37949614213231"></a>指使用SSH密钥证书作为HANA云服务器的鉴权方式。请先单击<span class="uicontrol" id="uicontrol63868947213231"><a name="uicontrol63868947213231"></a><a name="uicontrol63868947213231"></a>“查看密钥对”</span>，在<span class="wintitle" id="wintitle6204208115115"><a name="wintitle6204208115115"></a><a name="wintitle6204208115115"></a>“密钥对”</span>页面创建密钥。</p>
    <p id="p6002207213231"><a name="p6002207213231"></a><a name="p6002207213231"></a>需要指出的是，SAP HANA、SAP HANA Studio和NAT Server所使用的云服务器，必须指定同一份密钥，否则会导致后续SAP HANA无法正常安装。</p>
    <div class="note" id="note29781834213231"><a name="note29781834213231"></a><a name="note29781834213231"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p54019863213231"><a name="p54019863213231"></a><a name="p54019863213231"></a>如果您直接从下拉列表中选择已有的SSH密钥证书，请确保您已在本地获取该文件，否则，将影响您正常登录HANA云服务器。</p>
    <p id="p16416719213231"><a name="p16416719213231"></a><a name="p16416719213231"></a>若需要创建密钥，则其创建方法为：</p>
    <p id="p56622565104527"><a name="p56622565104527"></a><a name="p56622565104527"></a>单击<span class="uicontrol" id="uicontrol23993134104528"><a name="uicontrol23993134104528"></a><a name="uicontrol23993134104528"></a>“查看密钥对”</span>后，在弹出的界面中单击<span class="uicontrol" id="uicontrol23175868104528"><a name="uicontrol23175868104528"></a><a name="uicontrol23175868104528"></a>“创建密钥对”</span>，输入密钥名称后单击<span class="uicontrol" id="uicontrol5587916104528"><a name="uicontrol5587916104528"></a><a name="uicontrol5587916104528"></a>“确定”</span>，并在系统弹出的提示框中单击<span class="uicontrol" id="uicontrol45442781104528"><a name="uicontrol45442781104528"></a><a name="uicontrol45442781104528"></a>“确定”</span>，然后根据提示信息查看并保存私钥即可。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row38100638213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2686057213231"><a name="p2686057213231"></a><a name="p2686057213231"></a>云服务器组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p40701004213231"><a name="p40701004213231"></a><a name="p40701004213231"></a>此参数需要单击<span class="parmname" id="parmname16244066213231"><a name="parmname16244066213231"></a><a name="parmname16244066213231"></a>“高级配置”</span>后面的<span class="uicontrol" id="uicontrol11978874213231"><a name="uicontrol11978874213231"></a><a name="uicontrol11978874213231"></a>“现在配置”</span>，展开页面后才能看到。</p>
    <p id="p30764723213231"><a name="p30764723213231"></a><a name="p30764723213231"></a>用于指定HANA云服务器的服务器组。系统在创建云服务器时，会将属于同一个服务器组的HANA云服务器，创建在不同的物理主机上，以保证HANA云服务器运行的可靠性。</p>
    <p id="p8447055213231"><a name="p8447055213231"></a><a name="p8447055213231"></a>因此，需要根据具体的场景来确定策略：</p>
    <a name="ul51289541213231"></a><a name="ul51289541213231"></a><ul id="ul51289541213231"><li>单节点无HA：不需要指定<span class="parmvalue" id="parmvalue44497904104822"><a name="parmvalue44497904104822"></a><a name="parmvalue44497904104822"></a>“云服务器组”</span>。</li><li>单节点HA：两台HANA云服务器必须属于同一个<span class="parmvalue" id="parmvalue49163341105024"><a name="parmvalue49163341105024"></a><a name="parmvalue49163341105024"></a>“云服务器组”</span>。</li></ul>
    <div class="note" id="note26154017213231"><a name="note26154017213231"></a><a name="note26154017213231"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p58952685213231"><a name="p58952685213231"></a><a name="p58952685213231"></a>如果还没有云服务器组，则其创建方法为：</p>
    <p id="p28873974102037"><a name="p28873974102037"></a><a name="p28873974102037"></a>单击<span class="uicontrol" id="uicontrol58539178102037"><a name="uicontrol58539178102037"></a><a name="uicontrol58539178102037"></a>“查看云服务器组”</span>，在弹出的界面上，单击<span class="uicontrol" id="uicontrol57090557102037"><a name="uicontrol57090557102037"></a><a name="uicontrol57090557102037"></a>“创建云服务器组”</span>，输入云服务器组名称后单击<span class="uicontrol" id="uicontrol44052968102037"><a name="uicontrol44052968102037"></a><a name="uicontrol44052968102037"></a>“确定”</span>即可。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row4479816792621"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p477289192621"><a name="p477289192621"></a><a name="p477289192621"></a>代理名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p8772953172935"><a name="p8772953172935"></a><a name="p8772953172935"></a>此参数需要单击<span class="parmname" id="parmname11847714172935"><a name="parmname11847714172935"></a><a name="parmname11847714172935"></a>“高级配置”</span>后面的<span class="uicontrol" id="uicontrol39520565172935"><a name="uicontrol39520565172935"></a><a name="uicontrol39520565172935"></a>“现在配置”</span>，展开页面后才能看到。</p>
    <p id="p3974612292815"><a name="p3974612292815"></a><a name="p3974612292815"></a>选择代理后可以使被委托方通过该代理获取临时访问公有云的凭据。</p>
    <p id="p20178347203358"><a name="p20178347203358"></a><a name="p20178347203358"></a>Data Provider是公有云平台的指标收集器，用于收集SAP NetWeaver系统中ECS和CES的关键性能数据并将其呈现给SAP应用。当SAP HANA与SAP NetWeaver共同部署时，需要指定<span class="parmvalue" id="parmvalue20192102125719"><a name="parmvalue20192102125719"></a><a name="parmvalue20192102125719"></a>“DataproviderAccess”</span>代理。</p>
    <p id="p302445192925"><a name="p302445192925"></a><a name="p302445192925"></a>需要先以租户管理员的身份登录公有云管理控制台后，创建名为<span class="parmvalue" id="parmvalue906896993019"><a name="parmvalue906896993019"></a><a name="parmvalue906896993019"></a>“DataproviderAccess”</span>的代理后，再在此处使用该代理。</p>
    <div class="note" id="note28755827144024"><a name="note28755827144024"></a><a name="note28755827144024"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p57475853144024"><a name="p57475853144024"></a><a name="p57475853144024"></a>在公有云管理控制台，单击<span class="menucascade" id="menucascade47520632144024"><a name="menucascade47520632144024"></a><a name="menucascade47520632144024"></a>“<span class="uicontrol" id="uicontrol25032510144024"><a name="uicontrol25032510144024"></a><a name="uicontrol25032510144024"></a>管理与部署</span> &gt; <span class="uicontrol" id="uicontrol23965998144024"><a name="uicontrol23965998144024"></a><a name="uicontrol23965998144024"></a>统一身份认证服务</span>”</span>后，在左侧单击<span class="menucascade" id="menucascade14367395144024"><a name="menucascade14367395144024"></a><a name="menucascade14367395144024"></a>“<span class="uicontrol" id="uicontrol62197692144024"><a name="uicontrol62197692144024"></a><a name="uicontrol62197692144024"></a>委托</span>”</span>，然后在右侧单击<span class="uicontrol" id="uicontrol22908324144024"><a name="uicontrol22908324144024"></a><a name="uicontrol22908324144024"></a>“创建委托”</span>创建。</p>
    <p id="p4848331144024"><a name="p4848331144024"></a><a name="p4848331144024"></a>参数说明如下：</p>
    <a name="ul43634987144024"></a><a name="ul43634987144024"></a><ul id="ul43634987144024"><li>委托名称：DataProviderAccess</li><li>委托类型：云服务</li><li>云服务：ECS BMS</li><li>持续时间：使用默认值。</li><li>权限选择：选择本云服务器所在的“所属区域”对应的“项目”，单击“修改”，配置“基本 &gt; Tenant Guest”权限。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row27226109172820"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p40938486172824"><a name="p40938486172824"></a><a name="p40938486172824"></a>云服务器名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p27683032172824"><a name="p27683032172824"></a><a name="p27683032172824"></a>云服务器名称。</p>
    <p id="p47820702172824"><a name="p47820702172824"></a><a name="p47820702172824"></a>在批量创建云服务器时，每台云服务器的<span class="parmname" id="parmname27733135172824"><a name="parmname27733135172824"></a><a name="parmname27733135172824"></a>“云服务器名称”</span>会根据填写的参数值自动递增。比如填写的是<span class="parmvalue" id="parmvalue48271630172824"><a name="parmvalue48271630172824"></a><a name="parmvalue48271630172824"></a>“hana”</span>，第一台云服务器为<span class="parmvalue" id="parmvalue31791491172824"><a name="parmvalue31791491172824"></a><a name="parmvalue31791491172824"></a>“hana-0001”</span>，第二台云服务器为&nbsp;<span class="parmvalue" id="parmvalue17687967172824"><a name="parmvalue17687967172824"></a><a name="parmvalue17687967172824"></a>“hana-0002”</span>，以此类推。</p>
    <p id="p24973979172824"><a name="p24973979172824"></a><a name="p24973979172824"></a>关于主机名的长度和字符的更多信息，参见SAP Note 611361。</p>
    </td>
    </tr>
    <tr id="row6057181693343"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2835583893347"><a name="p2835583893347"></a><a name="p2835583893347"></a>购买时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1512151993347"><a name="p1512151993347"></a><a name="p1512151993347"></a>根据实际需要选择购买时长。</p>
    </td>
    </tr>
    <tr id="row53689322213231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p38074930111716"><a name="p38074930111716"></a><a name="p38074930111716"></a>数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p59404795213231"><a name="p59404795213231"></a><a name="p59404795213231"></a>根据实际填写。</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“立即购买“，在弹出的界面中，勾选“我已经阅读并同意《华为镜像免责声明》”，单击“去支付”。
7.  单击“确认付款“。
8.  系统返回“弹性云服务器“管理界面，可在右侧界面的“任务状态“后面，查看当前创建任务的状态。

    HANA云服务器创建完成后，在右侧界面的服务器列表中可查看到对应的服务器。

9.  根据需要，继续创建其他HANA云服务器。
10. 修改所有HANA云服务器的“root“帐号密码。

    “root“帐号密码非常重要，请务必牢记密码。同时请确保所有的HANA云服务器，“root“帐号密码保持一致。

    1.  通过密钥，登录到SAP HANA云服务器。
    2.  修改“root“帐号密码。

        **passwd**

        按照界面提示，输入密码并进行确认。



