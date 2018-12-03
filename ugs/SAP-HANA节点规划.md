# SAP HANA节点规划<a name="saphana_02_0012"></a>

在不同的场景下，SAP公司对HANA服务器的规格有明确的要求。

>![](public_sys-resources/icon-note.gif) **说明：**   
>需要指出的是，除了下述描述的规格之外，应用层SAP Netweaver所在服务器的时区，应与SAP HANA节点的时区保持一致。  

## SoH场景规格<a name="section3462842621474"></a>

SoH场景是指SAP HANA配合SAP公司的商务套件（如ERP、CRM等）使用的场景。在该场景下，SAP HANA提供OLTP功能，关注SAP HANA的处理时延。

华为云上提供的经SAP官方认证的HANA云服务器规格如[表1](#table1521611461217)和[表4](#table961494014280)所示。对于非生产系统，华为云上提供的云服务器如[表2](#table14480263125)和[表3](#table1598061213439)所示。

**表 1**  E1型弹性云服务器的规格

<a name="table1521611461217"></a>
<table><thead align="left"><tr id="row522918146123"><th class="cellrowborder" valign="top" width="27.51%" id="mcps1.2.5.1.1"><p id="p1823314143125"><a name="p1823314143125"></a><a name="p1823314143125"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.78%" id="mcps1.2.5.1.2"><p id="p1023741491212"><a name="p1023741491212"></a><a name="p1023741491212"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.83%" id="mcps1.2.5.1.3"><p id="p1523912142121"><a name="p1523912142121"></a><a name="p1523912142121"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="p14242101491220"><a name="p14242101491220"></a><a name="p14242101491220"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row026610142124"><td class="cellrowborder" rowspan="2" valign="top" width="27.51%" headers="mcps1.2.5.1.1 "><p id="p625315081220"><a name="p625315081220"></a><a name="p625315081220"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.78%" headers="mcps1.2.5.1.2 "><p id="p72691914151217"><a name="p72691914151217"></a><a name="p72691914151217"></a>16</p>
</td>
<td class="cellrowborder" valign="top" width="28.83%" headers="mcps1.2.5.1.3 "><p id="p32726148128"><a name="p32726148128"></a><a name="p32726148128"></a>470</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="p6276201411123"><a name="p6276201411123"></a><a name="p6276201411123"></a>e1.4xlarge</p>
</td>
</tr>
<tr id="row7279121491212"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p19284614101218"><a name="p19284614101218"></a><a name="p19284614101218"></a>32</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p728731410124"><a name="p728731410124"></a><a name="p728731410124"></a>940</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p62909146123"><a name="p62909146123"></a><a name="p62909146123"></a>e1.8xlarge</p>
</td>
</tr>
</tbody>
</table>

**表 2**  E2型弹性云服务器的规格

<a name="table14480263125"></a>
<table><thead align="left"><tr id="row5492763124"><th class="cellrowborder" valign="top" width="27.51%" id="mcps1.2.5.1.1"><p id="p1649510601220"><a name="p1649510601220"></a><a name="p1649510601220"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.78%" id="mcps1.2.5.1.2"><p id="p44991561121"><a name="p44991561121"></a><a name="p44991561121"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.83%" id="mcps1.2.5.1.3"><p id="p450313651213"><a name="p450313651213"></a><a name="p450313651213"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="p175065661217"><a name="p175065661217"></a><a name="p175065661217"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row4509126121214"><td class="cellrowborder" valign="top" width="27.51%" headers="mcps1.2.5.1.1 "><p id="p1951410614123"><a name="p1951410614123"></a><a name="p1951410614123"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.78%" headers="mcps1.2.5.1.2 "><p id="p45185651217"><a name="p45185651217"></a><a name="p45185651217"></a>12</p>
</td>
<td class="cellrowborder" valign="top" width="28.83%" headers="mcps1.2.5.1.3 "><p id="p1652116161211"><a name="p1652116161211"></a><a name="p1652116161211"></a>256</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="p1052414613126"><a name="p1052414613126"></a><a name="p1052414613126"></a>e2.3xlarge</p>
</td>
</tr>
</tbody>
</table>

**表 3**  ET2型弹性云服务器的规格

<a name="table1598061213439"></a>
<table><thead align="left"><tr id="row1011513174315"><th class="cellrowborder" valign="top" width="27.51%" id="mcps1.2.5.1.1"><p id="p31891310435"><a name="p31891310435"></a><a name="p31891310435"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.78%" id="mcps1.2.5.1.2"><p id="p2241813124311"><a name="p2241813124311"></a><a name="p2241813124311"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.83%" id="mcps1.2.5.1.3"><p id="p2311913194310"><a name="p2311913194310"></a><a name="p2311913194310"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="p636213174315"><a name="p636213174315"></a><a name="p636213174315"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row1842121364312"><td class="cellrowborder" rowspan="3" valign="top" width="27.51%" headers="mcps1.2.5.1.1 "><p id="p1347141318438"><a name="p1347141318438"></a><a name="p1347141318438"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.78%" headers="mcps1.2.5.1.2 "><p id="p55219139437"><a name="p55219139437"></a><a name="p55219139437"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="28.83%" headers="mcps1.2.5.1.3 "><p id="p12649137431"><a name="p12649137431"></a><a name="p12649137431"></a>128</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="p14691613154314"><a name="p14691613154314"></a><a name="p14691613154314"></a>et2.2xlarge.16</p>
</td>
</tr>
<tr id="row13721613184318"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1479191315439"><a name="p1479191315439"></a><a name="p1479191315439"></a>18</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p48591315437"><a name="p48591315437"></a><a name="p48591315437"></a>256</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p8892131432"><a name="p8892131432"></a><a name="p8892131432"></a>et2.4xlarge.14</p>
</td>
</tr>
<tr id="row13920136432"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p189913139439"><a name="p189913139439"></a><a name="p189913139439"></a>36</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p16104313164315"><a name="p16104313164315"></a><a name="p16104313164315"></a>512</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p1810913137437"><a name="p1810913137437"></a><a name="p1810913137437"></a>et2.8xlarge.14</p>
</td>
</tr>
</tbody>
</table>

**表 4**  E3型弹性云服务器的规格

<a name="table961494014280"></a>
<table><thead align="left"><tr id="row862514020281"><th class="cellrowborder" valign="top" width="27.700000000000003%" id="mcps1.2.5.1.1"><p id="p313515359416"><a name="p313515359416"></a><a name="p313515359416"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.559999999999999%" id="mcps1.2.5.1.2"><p id="p513512353418"><a name="p513512353418"></a><a name="p513512353418"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.860000000000003%" id="mcps1.2.5.1.3"><p id="p11135835164117"><a name="p11135835164117"></a><a name="p11135835164117"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="p91511935154115"><a name="p91511935154115"></a><a name="p91511935154115"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row46541340102814"><td class="cellrowborder" rowspan="2" valign="top" width="27.700000000000003%" headers="mcps1.2.5.1.1 "><p id="p2015116358413"><a name="p2015116358413"></a><a name="p2015116358413"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.559999999999999%" headers="mcps1.2.5.1.2 "><p id="p141681735134116"><a name="p141681735134116"></a><a name="p141681735134116"></a>28</p>
</td>
<td class="cellrowborder" valign="top" width="28.860000000000003%" headers="mcps1.2.5.1.3 "><p id="p716863510413"><a name="p716863510413"></a><a name="p716863510413"></a>348</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="p91681635174119"><a name="p91681635174119"></a><a name="p91681635174119"></a>e3.7xlarge.12</p>
</td>
</tr>
<tr id="row1866694010286"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p17182735104114"><a name="p17182735104114"></a><a name="p17182735104114"></a>56</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p11182143512418"><a name="p11182143512418"></a><a name="p11182143512418"></a>696</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p91821135194120"><a name="p91821135194120"></a><a name="p91821135194120"></a>e3.14xlarge.12</p>
</td>
</tr>
</tbody>
</table>

## BWoH场景规格<a name="section49570224214749"></a>

BWoH场景是指SAP HANA配合SAP公司的BusinessWarehouse使用的场景。在该场景下，SAP HANA提供OLAP功能，支持大量的数据在SAP HANA中进行快速计算和分析，关注SAP HANA的处理性能以及SAP HANA节点之间的网络带宽。

华为云上提供的经SAP官方认证的HANA云服务器规格如[表5](#table55950414144826)和[表7](#table988319560)所示。对于非生产系统，华为云上提供的云服务器如[表6](#table76551938134417)所示。

**表 5**  E2型弹性云服务器的规格

<a name="table55950414144826"></a>
<table><thead align="left"><tr id="row48953446144826"><th class="cellrowborder" valign="top" width="27.51%" id="mcps1.2.5.1.1"><p id="p5806155144826"><a name="p5806155144826"></a><a name="p5806155144826"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.78%" id="mcps1.2.5.1.2"><p id="p536524144826"><a name="p536524144826"></a><a name="p536524144826"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.83%" id="mcps1.2.5.1.3"><p id="p43458515144826"><a name="p43458515144826"></a><a name="p43458515144826"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="p30478789144826"><a name="p30478789144826"></a><a name="p30478789144826"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row37544296144826"><td class="cellrowborder" rowspan="2" valign="top" width="27.51%" headers="mcps1.2.5.1.1 "><p id="p8879586152129"><a name="p8879586152129"></a><a name="p8879586152129"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.78%" headers="mcps1.2.5.1.2 "><p id="p41293276144842"><a name="p41293276144842"></a><a name="p41293276144842"></a>18</p>
</td>
<td class="cellrowborder" valign="top" width="28.83%" headers="mcps1.2.5.1.3 "><p id="p56421054144842"><a name="p56421054144842"></a><a name="p56421054144842"></a>445</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="p6702648144842"><a name="p6702648144842"></a><a name="p6702648144842"></a>e2.4xlarge</p>
</td>
</tr>
<tr id="row17727033144826"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p54392720144842"><a name="p54392720144842"></a><a name="p54392720144842"></a>36</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p43734223144842"><a name="p43734223144842"></a><a name="p43734223144842"></a>890</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p52811170144842"><a name="p52811170144842"></a><a name="p52811170144842"></a>e2.9xlarge</p>
</td>
</tr>
</tbody>
</table>

**表 6**  ET2型弹性云服务器的规格

<a name="table76551938134417"></a>
<table><thead align="left"><tr id="row14684193814447"><th class="cellrowborder" valign="top" width="27.51%" id="mcps1.2.5.1.1"><p id="p196925385444"><a name="p196925385444"></a><a name="p196925385444"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.78%" id="mcps1.2.5.1.2"><p id="p1469917385443"><a name="p1469917385443"></a><a name="p1469917385443"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.83%" id="mcps1.2.5.1.3"><p id="p18704103804411"><a name="p18704103804411"></a><a name="p18704103804411"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="p87121380443"><a name="p87121380443"></a><a name="p87121380443"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row177188382443"><td class="cellrowborder" rowspan="3" valign="top" width="27.51%" headers="mcps1.2.5.1.1 "><p id="p20726203844417"><a name="p20726203844417"></a><a name="p20726203844417"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.78%" headers="mcps1.2.5.1.2 "><p id="p573263834415"><a name="p573263834415"></a><a name="p573263834415"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="28.83%" headers="mcps1.2.5.1.3 "><p id="p37391438134410"><a name="p37391438134410"></a><a name="p37391438134410"></a>128</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="p57451038204417"><a name="p57451038204417"></a><a name="p57451038204417"></a>et2.2xlarge.16</p>
</td>
</tr>
<tr id="row127481938154418"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1175311382444"><a name="p1175311382444"></a><a name="p1175311382444"></a>18</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p775833814411"><a name="p775833814411"></a><a name="p775833814411"></a>256</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p876273874416"><a name="p876273874416"></a><a name="p876273874416"></a>et2.4xlarge.14</p>
</td>
</tr>
<tr id="row14764163814447"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p777011388446"><a name="p777011388446"></a><a name="p777011388446"></a>36</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p77751338184412"><a name="p77751338184412"></a><a name="p77751338184412"></a>512</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p18779163874413"><a name="p18779163874413"></a><a name="p18779163874413"></a>et2.8xlarge.14</p>
</td>
</tr>
</tbody>
</table>

**表 7**  E3型弹性云服务器的规格

<a name="table988319560"></a>
<table><thead align="left"><tr id="saphana_02_0012_row862514020281"><th class="cellrowborder" valign="top" width="27.700000000000003%" id="mcps1.2.5.1.1"><p id="saphana_02_0012_p313515359416"><a name="saphana_02_0012_p313515359416"></a><a name="saphana_02_0012_p313515359416"></a>分类</p>
</th>
<th class="cellrowborder" valign="top" width="15.559999999999999%" id="mcps1.2.5.1.2"><p id="saphana_02_0012_p513512353418"><a name="saphana_02_0012_p513512353418"></a><a name="saphana_02_0012_p513512353418"></a>vCPU</p>
</th>
<th class="cellrowborder" valign="top" width="28.860000000000003%" id="mcps1.2.5.1.3"><p id="saphana_02_0012_p11135835164117"><a name="saphana_02_0012_p11135835164117"></a><a name="saphana_02_0012_p11135835164117"></a>内存 (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="27.88%" id="mcps1.2.5.1.4"><p id="saphana_02_0012_p91511935154115"><a name="saphana_02_0012_p91511935154115"></a><a name="saphana_02_0012_p91511935154115"></a>规格名称</p>
</th>
</tr>
</thead>
<tbody><tr id="saphana_02_0012_row46541340102814"><td class="cellrowborder" rowspan="2" valign="top" width="27.700000000000003%" headers="mcps1.2.5.1.1 "><p id="saphana_02_0012_p2015116358413"><a name="saphana_02_0012_p2015116358413"></a><a name="saphana_02_0012_p2015116358413"></a>超大内存型</p>
</td>
<td class="cellrowborder" valign="top" width="15.559999999999999%" headers="mcps1.2.5.1.2 "><p id="saphana_02_0012_p141681735134116"><a name="saphana_02_0012_p141681735134116"></a><a name="saphana_02_0012_p141681735134116"></a>28</p>
</td>
<td class="cellrowborder" valign="top" width="28.860000000000003%" headers="mcps1.2.5.1.3 "><p id="saphana_02_0012_p716863510413"><a name="saphana_02_0012_p716863510413"></a><a name="saphana_02_0012_p716863510413"></a>348</p>
</td>
<td class="cellrowborder" valign="top" width="27.88%" headers="mcps1.2.5.1.4 "><p id="saphana_02_0012_p91681635174119"><a name="saphana_02_0012_p91681635174119"></a><a name="saphana_02_0012_p91681635174119"></a>e3.7xlarge.12</p>
</td>
</tr>
<tr id="saphana_02_0012_row1866694010286"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="saphana_02_0012_p17182735104114"><a name="saphana_02_0012_p17182735104114"></a><a name="saphana_02_0012_p17182735104114"></a>56</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="saphana_02_0012_p11182143512418"><a name="saphana_02_0012_p11182143512418"></a><a name="saphana_02_0012_p11182143512418"></a>696</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="saphana_02_0012_p91821135194120"><a name="saphana_02_0012_p91821135194120"></a><a name="saphana_02_0012_p91821135194120"></a>e3.14xlarge.12</p>
</td>
</tr>
</tbody>
</table>

## 操作系统和磁盘要求<a name="section31573146194054"></a>

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   Log卷、Data卷、Shared卷、Backup卷均为SAP HANA要求提供的卷。  
>-   共享盘为一种磁盘种类，可以绑定给多台云服务器使用，而非共享盘则为普通磁盘，只能绑定一台云服务器使用。  

**表 8**  HANA云服务器操作系统要求（单节点）

<a name="table277447592121"></a>
<table><thead align="left"><tr id="row5546933692121"><th class="cellrowborder" valign="top" width="22.37%" id="mcps1.2.3.1.1"><p id="p3761029592121"><a name="p3761029592121"></a><a name="p3761029592121"></a>场景</p>
</th>
<th class="cellrowborder" valign="top" width="77.63%" id="mcps1.2.3.1.2"><p id="p200103916476"><a name="p200103916476"></a><a name="p200103916476"></a>规格</p>
</th>
</tr>
</thead>
<tbody><tr id="row1672211892121"><td class="cellrowborder" valign="top" width="22.37%" headers="mcps1.2.3.1.1 "><p id="p1231430092121"><a name="p1231430092121"></a><a name="p1231430092121"></a>操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="77.63%" headers="mcps1.2.3.1.2 "><p id="p20792500102136"><a name="p20792500102136"></a><a name="p20792500102136"></a>SUSE Linux Enterprise Server (SLES) 12 SP1 for SAP及以上</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>在同AZ HA场景中。需要为一台SAP HANA节点创建一个EVS卷用作SBD，创建完之后再绑定给另外一台SAP HANA节点。  
>在跨AZ HA场景中，无需为SAP HANA创建SBD卷，该场景下SBD卷的创建请参考[配置iSCSI（跨AZ部署HA）](配置iSCSI（跨AZ部署HA）.md)。  

**表 9**  E1、E2型服务器磁盘格式要求（单节点）

<a name="table99251547151416"></a>
<table><thead align="left"><tr id="row3937114714145"><th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.1"><p id="p14943144741413"><a name="p14943144741413"></a><a name="p14943144741413"></a>磁盘</p>
</th>
<th class="cellrowborder" valign="top" width="31%" id="mcps1.2.5.1.2"><p id="p1694604718148"><a name="p1694604718148"></a><a name="p1694604718148"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1094974717142"><a name="p1094974717142"></a><a name="p1094974717142"></a>共享方式</p>
</th>
<th class="cellrowborder" valign="top" width="35%" id="mcps1.2.5.1.4"><p id="p3953154710140"><a name="p3953154710140"></a><a name="p3953154710140"></a>大小</p>
</th>
</tr>
</thead>
<tbody><tr id="row3958174731419"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p496714717140"><a name="p496714717140"></a><a name="p496714717140"></a>OS卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p43182214211"><a name="p43182214211"></a><a name="p43182214211"></a><span class="parmvalue" id="parmvalue168235141819"><a name="parmvalue168235141819"></a><a name="parmvalue168235141819"></a>“超高IO(时延优化)”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p93921943201714"><a name="p93921943201714"></a><a name="p93921943201714"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><p id="p99791747151418"><a name="p99791747151418"></a><a name="p99791747151418"></a>-</p>
</td>
</tr>
<tr id="row1898118475149"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p159861847121413"><a name="p159861847121413"></a><a name="p159861847121413"></a>Log卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p13377193811212"><a name="p13377193811212"></a><a name="p13377193811212"></a><span class="parmvalue" id="parmvalue219263010181"><a name="parmvalue219263010181"></a><a name="parmvalue219263010181"></a>“超高IO(时延优化)”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p9372132314151"><a name="p9372132314151"></a><a name="p9372132314151"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><a name="ul1499984717142"></a><a name="ul1499984717142"></a><ul id="ul1499984717142"><li>当内存小于或等于512GB时，Log卷的大小为内存的一半，如果数值存在小数位时向上取整。</li><li>当内存大于512GB时，Log卷的大小为512GB。</li></ul>
</td>
</tr>
<tr id="row771393158"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p19721931516"><a name="p19721931516"></a><a name="p19721931516"></a>Data卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p19576121012229"><a name="p19576121012229"></a><a name="p19576121012229"></a><span class="parmvalue" id="parmvalue12698122714185"><a name="parmvalue12698122714185"></a><a name="parmvalue12698122714185"></a>“超高IO(时延优化)”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p13711123131513"><a name="p13711123131513"></a><a name="p13711123131513"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><p id="p16596191120268"><a name="p16596191120268"></a><a name="p16596191120268"></a>推荐值为内存空间大小的1.2倍或以上</p>
</td>
</tr>
<tr id="row4141448111413"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p19191948141418"><a name="p19191948141418"></a><a name="p19191948141418"></a>Shared卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p4535931202212"><a name="p4535931202212"></a><a name="p4535931202212"></a><span class="parmvalue" id="parmvalue0733162371810"><a name="parmvalue0733162371810"></a><a name="parmvalue0733162371810"></a>“超高IO(时延优化)”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p33701723101513"><a name="p33701723101513"></a><a name="p33701723101513"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><p id="p1753375102613"><a name="p1753375102613"></a><a name="p1753375102613"></a>推荐值为内存空间大小的1.2倍或以上</p>
</td>
</tr>
<tr id="row143784811147"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1401948161413"><a name="p1401948161413"></a><a name="p1401948161413"></a>Backup卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p339216191353"><a name="p339216191353"></a><a name="p339216191353"></a>SFS</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p13408151953511"><a name="p13408151953511"></a><a name="p13408151953511"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><p id="p1352848101411"><a name="p1352848101411"></a><a name="p1352848101411"></a>推荐值为内存空间大小的三倍或以上</p>
</td>
</tr>
<tr id="row25416481145"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p76044813145"><a name="p76044813145"></a><a name="p76044813145"></a>SBD卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p181451319201515"><a name="p181451319201515"></a><a name="p181451319201515"></a><span class="parmvalue" id="parmvalue1637372120215"><a name="parmvalue1637372120215"></a><a name="parmvalue1637372120215"></a>“超高IO(时延优化)”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p2368223131513"><a name="p2368223131513"></a><a name="p2368223131513"></a>共享盘（SCSI接口）</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><p id="p17787486143"><a name="p17787486143"></a><a name="p17787486143"></a>10GB</p>
</td>
</tr>
<tr id="row14600114091910"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p560094020199"><a name="p560094020199"></a><a name="p560094020199"></a>/usr/sap卷</p>
</td>
<td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.5.1.2 "><p id="p1737217386186"><a name="p1737217386186"></a><a name="p1737217386186"></a><span class="parmvalue" id="parmvalue437519381181"><a name="parmvalue437519381181"></a><a name="parmvalue437519381181"></a>“超高IO(时延优化)”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1060024091911"><a name="p1060024091911"></a><a name="p1060024091911"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.5.1.4 "><p id="p460014061919"><a name="p460014061919"></a><a name="p460014061919"></a>50GB</p>
</td>
</tr>
</tbody>
</table>

**表 10**  ET2型服务器磁盘格式要求（单节点）

<a name="table19272184713476"></a>
<table><thead align="left"><tr id="row19292184718472"><th class="cellrowborder" valign="top" width="20.002000200020003%" id="mcps1.2.5.1.1"><p id="p1830094715470"><a name="p1830094715470"></a><a name="p1830094715470"></a>磁盘</p>
</th>
<th class="cellrowborder" valign="top" width="20.002000200020003%" id="mcps1.2.5.1.2"><p id="p1330704719474"><a name="p1330704719474"></a><a name="p1330704719474"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="20.002000200020003%" id="mcps1.2.5.1.3"><p id="p5315184718475"><a name="p5315184718475"></a><a name="p5315184718475"></a>共享方式</p>
</th>
<th class="cellrowborder" valign="top" width="39.99399939993999%" id="mcps1.2.5.1.4"><p id="p203224474470"><a name="p203224474470"></a><a name="p203224474470"></a>大小</p>
</th>
</tr>
</thead>
<tbody><tr id="row5330164720470"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p53401647184712"><a name="p53401647184712"></a><a name="p53401647184712"></a>OS卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p20347164716474"><a name="p20347164716474"></a><a name="p20347164716474"></a><span class="parmvalue" id="parmvalue113511547144710"><a name="parmvalue113511547144710"></a><a name="parmvalue113511547144710"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p163572477479"><a name="p163572477479"></a><a name="p163572477479"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p113621947184717"><a name="p113621947184717"></a><a name="p113621947184717"></a>-</p>
</td>
</tr>
<tr id="row133648474478"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p14369447104715"><a name="p14369447104715"></a><a name="p14369447104715"></a>Log卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p1837719475475"><a name="p1837719475475"></a><a name="p1837719475475"></a><span class="parmvalue" id="parmvalue13380144754714"><a name="parmvalue13380144754714"></a><a name="parmvalue13380144754714"></a>“超高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p4133181419423"><a name="p4133181419423"></a><a name="p4133181419423"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p19420649161216"><a name="p19420649161216"></a><a name="p19420649161216"></a>请参考<a href="#saphana_02_0012__table19532115345717">表11</a></p>
</td>
</tr>
<tr id="row320012151214"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p62785100129"><a name="p62785100129"></a><a name="p62785100129"></a>Data卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p11622192114125"><a name="p11622192114125"></a><a name="p11622192114125"></a><span class="parmvalue" id="parmvalue3622421181210"><a name="parmvalue3622421181210"></a><a name="parmvalue3622421181210"></a>“超高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p16811203212120"><a name="p16811203212120"></a><a name="p16811203212120"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p120014141212"><a name="p120014141212"></a><a name="p120014141212"></a>创建EVS卷利用LVM的功能做软分区处理分配Data卷，所需规格请参考<a href="#saphana_02_0012__table19532115345717">表11</a></p>
</td>
</tr>
<tr id="row3417194710474"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p15424204724713"><a name="p15424204724713"></a><a name="p15424204724713"></a>Shared卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p104311747134714"><a name="p104311747134714"></a><a name="p104311747134714"></a><span class="parmvalue" id="parmvalue114351477475"><a name="parmvalue114351477475"></a><a name="parmvalue114351477475"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p1344174710479"><a name="p1344174710479"></a><a name="p1344174710479"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p1170545912255"><a name="p1170545912255"></a><a name="p1170545912255"></a>推荐值为内存空间大小的1.2倍或以上</p>
</td>
</tr>
<tr id="row18450144711474"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p645544719470"><a name="p645544719470"></a><a name="p645544719470"></a>Backup卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p10460114764711"><a name="p10460114764711"></a><a name="p10460114764711"></a>SFS</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p1947364764717"><a name="p1947364764717"></a><a name="p1947364764717"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p74806474473"><a name="p74806474473"></a><a name="p74806474473"></a>推荐值为内存空间大小的三倍或以上</p>
</td>
</tr>
<tr id="row348494716478"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p74891647124712"><a name="p74891647124712"></a><a name="p74891647124712"></a>SBD卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p41663181789"><a name="p41663181789"></a><a name="p41663181789"></a><span class="parmvalue" id="parmvalue91021325121713"><a name="parmvalue91021325121713"></a><a name="parmvalue91021325121713"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p550984715478"><a name="p550984715478"></a><a name="p550984715478"></a>共享盘（SCSI接口）</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p145178478474"><a name="p145178478474"></a><a name="p145178478474"></a>10GB</p>
</td>
</tr>
<tr id="row9218152059"><td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.1 "><p id="p4324181758"><a name="p4324181758"></a><a name="p4324181758"></a>/usr/sap卷</p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.2 "><p id="p73613181059"><a name="p73613181059"></a><a name="p73613181059"></a><span class="parmvalue" id="parmvalue638118754"><a name="parmvalue638118754"></a><a name="parmvalue638118754"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20.002000200020003%" headers="mcps1.2.5.1.3 "><p id="p8415183517"><a name="p8415183517"></a><a name="p8415183517"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="39.99399939993999%" headers="mcps1.2.5.1.4 "><p id="p146118155"><a name="p146118155"></a><a name="p146118155"></a>50GB</p>
</td>
</tr>
</tbody>
</table>

**表 11**  ET2型服务器推荐的Log和Data卷配置

<a name="table19532115345717"></a>
<table><thead align="left"><tr id="row1354875335710"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="p1856317534571"><a name="p1856317534571"></a><a name="p1856317534571"></a>规格</p>
</th>
<th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.2"><p id="p1756325385717"><a name="p1756325385717"></a><a name="p1756325385717"></a>Log卷大小</p>
</th>
<th class="cellrowborder" valign="top" width="37%" id="mcps1.2.4.1.3"><p id="p175638533579"><a name="p175638533579"></a><a name="p175638533579"></a>Data卷大小</p>
</th>
</tr>
</thead>
<tbody><tr id="row95631653125718"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p5909142155918"><a name="p5909142155918"></a><a name="p5909142155918"></a>et2.2xlarge.16</p>
</td>
<td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.2 "><p id="p85781753135714"><a name="p85781753135714"></a><a name="p85781753135714"></a>100GB</p>
</td>
<td class="cellrowborder" valign="top" width="37%" headers="mcps1.2.4.1.3 "><p id="p16595125345717"><a name="p16595125345717"></a><a name="p16595125345717"></a>推荐2*200GB的EVS卷</p>
</td>
</tr>
<tr id="row759545317572"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p143620735915"><a name="p143620735915"></a><a name="p143620735915"></a>et2.4xlarge.14</p>
</td>
<td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.2 "><p id="p1261045315711"><a name="p1261045315711"></a><a name="p1261045315711"></a>200GB</p>
</td>
<td class="cellrowborder" valign="top" width="37%" headers="mcps1.2.4.1.3 "><p id="p86101353165711"><a name="p86101353165711"></a><a name="p86101353165711"></a>推荐2*250GB的EVS卷</p>
</td>
</tr>
<tr id="row1661055312579"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p050211469589"><a name="p050211469589"></a><a name="p050211469589"></a>et2.8xlarge.14</p>
</td>
<td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.2 "><p id="p1762545313576"><a name="p1762545313576"></a><a name="p1762545313576"></a>512GB</p>
</td>
<td class="cellrowborder" valign="top" width="37%" headers="mcps1.2.4.1.3 "><p id="p1362517537579"><a name="p1362517537579"></a><a name="p1362517537579"></a>推荐2*400GB的EVS卷</p>
</td>
</tr>
</tbody>
</table>

**表 12**  E3型服务器磁盘格式要求（单节点）

<a name="table314916251164"></a>
<table><thead align="left"><tr id="row816518251563"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p2169162511614"><a name="p2169162511614"></a><a name="p2169162511614"></a>磁盘</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p51739251865"><a name="p51739251865"></a><a name="p51739251865"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p01782254615"><a name="p01782254615"></a><a name="p01782254615"></a>共享方式</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p141831725861"><a name="p141831725861"></a><a name="p141831725861"></a>大小</p>
</th>
</tr>
</thead>
<tbody><tr id="row1718692516617"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p819019254612"><a name="p819019254612"></a><a name="p819019254612"></a>OS卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p13194725566"><a name="p13194725566"></a><a name="p13194725566"></a><span class="parmvalue" id="parmvalue71951254618"><a name="parmvalue71951254618"></a><a name="parmvalue71951254618"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p21983251362"><a name="p21983251362"></a><a name="p21983251362"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p152041525165"><a name="p152041525165"></a><a name="p152041525165"></a>-</p>
</td>
</tr>
<tr id="row2206202510620"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p172118251616"><a name="p172118251616"></a><a name="p172118251616"></a>Log卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p5215225661"><a name="p5215225661"></a><a name="p5215225661"></a><span class="parmvalue" id="parmvalue921632510612"><a name="parmvalue921632510612"></a><a name="parmvalue921632510612"></a>“超高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p240204664214"><a name="p240204664214"></a><a name="p240204664214"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p1754834244411"><a name="p1754834244411"></a><a name="p1754834244411"></a>请参考<a href="#saphana_02_0012__table15747103341">表13</a></p>
</td>
</tr>
<tr id="row966332119380"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1266310216384"><a name="p1266310216384"></a><a name="p1266310216384"></a>Data卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p1442814340387"><a name="p1442814340387"></a><a name="p1442814340387"></a><span class="parmvalue" id="parmvalue042816344384"><a name="parmvalue042816344384"></a><a name="parmvalue042816344384"></a>“超高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p163285012421"><a name="p163285012421"></a><a name="p163285012421"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p18187940104310"><a name="p18187940104310"></a><a name="p18187940104310"></a>创建EVS卷利用LVM的功能做软分区处理分配Data卷，所需规格请参考<a href="#saphana_02_0012__table15747103341">表13</a></p>
</td>
</tr>
<tr id="row923352513620"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p5237142517618"><a name="p5237142517618"></a><a name="p5237142517618"></a>Shared卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p15240182511611"><a name="p15240182511611"></a><a name="p15240182511611"></a><span class="parmvalue" id="parmvalue82421425863"><a name="parmvalue82421425863"></a><a name="parmvalue82421425863"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p32473255610"><a name="p32473255610"></a><a name="p32473255610"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p415632018246"><a name="p415632018246"></a><a name="p415632018246"></a>推荐值为内存空间大小的1.2倍或以上</p>
</td>
</tr>
<tr id="row172529252615"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p3255142511617"><a name="p3255142511617"></a><a name="p3255142511617"></a>Backup卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p82597258612"><a name="p82597258612"></a><a name="p82597258612"></a>SFS</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p19262925164"><a name="p19262925164"></a><a name="p19262925164"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p152666251862"><a name="p152666251862"></a><a name="p152666251862"></a>推荐值为内存空间大小的三倍或以上</p>
</td>
</tr>
<tr id="row826812252068"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p62721255610"><a name="p62721255610"></a><a name="p62721255610"></a>SBD卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p1427814251769"><a name="p1427814251769"></a><a name="p1427814251769"></a><span class="parmvalue" id="parmvalue5280142519617"><a name="parmvalue5280142519617"></a><a name="parmvalue5280142519617"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p152868251164"><a name="p152868251164"></a><a name="p152868251164"></a>共享盘（SCSI接口）</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p132893251610"><a name="p132893251610"></a><a name="p132893251610"></a>10GB</p>
</td>
</tr>
<tr id="row13291425563"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p152941925869"><a name="p152941925869"></a><a name="p152941925869"></a>/usr/sap卷</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p32971025765"><a name="p32971025765"></a><a name="p32971025765"></a><span class="parmvalue" id="parmvalue113016258613"><a name="parmvalue113016258613"></a><a name="parmvalue113016258613"></a>“高I/O”</span></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p73051325364"><a name="p73051325364"></a><a name="p73051325364"></a>非共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p19309192516611"><a name="p19309192516611"></a><a name="p19309192516611"></a>100GB</p>
</td>
</tr>
</tbody>
</table>

**表 13**  E3型服务器推荐的Log和Data卷配置

<a name="table15747103341"></a>
<table><thead align="left"><tr id="row127631408349"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="p276790133414"><a name="p276790133414"></a><a name="p276790133414"></a>规格</p>
</th>
<th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.2"><p id="p298212565318"><a name="p298212565318"></a><a name="p298212565318"></a>Log卷大小</p>
</th>
<th class="cellrowborder" valign="top" width="37%" id="mcps1.2.4.1.3"><p id="p12783180143416"><a name="p12783180143416"></a><a name="p12783180143416"></a>Data卷大小</p>
</th>
</tr>
</thead>
<tbody><tr id="row87996003413"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p845854911116"><a name="p845854911116"></a><a name="p845854911116"></a>e3.7xlarge.12</p>
</td>
<td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.2 "><p id="p2982659535"><a name="p2982659535"></a><a name="p2982659535"></a>200GB</p>
</td>
<td class="cellrowborder" valign="top" width="37%" headers="mcps1.2.4.1.3 "><p id="p581414013410"><a name="p581414013410"></a><a name="p581414013410"></a>推荐2*250GB的EVS卷</p>
</td>
</tr>
<tr id="row14828120133420"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p164681149101115"><a name="p164681149101115"></a><a name="p164681149101115"></a>e3.14xlarge.12</p>
</td>
<td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.2 "><p id="p29821656530"><a name="p29821656530"></a><a name="p29821656530"></a>512GB</p>
</td>
<td class="cellrowborder" valign="top" width="37%" headers="mcps1.2.4.1.3 "><p id="p18843140193417"><a name="p18843140193417"></a><a name="p18843140193417"></a>推荐2*450GB的EVS卷</p>
</td>
</tr>
</tbody>
</table>

