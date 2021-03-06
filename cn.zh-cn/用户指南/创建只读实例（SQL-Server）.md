# 创建只读实例<a name="rds_03_0011"></a>

## 操作场景<a name="s9f95e14048064f63a1d9be0c9f685f07"></a>

只读实例用于增强主实例的读能力，减轻主实例负载。

华为云关系型数据库实例创建成功后，可根据业务需要创建只读实例。

>![](public_sys-resources/icon-note.gif) **说明：**   
>账户余额大于等于0元，才可新增只读实例。  
>一个主实例中，最多可以增加5个只读实例。  
>目前，云数据库SQL Server仅2017企业版的实例支持新增只读实例。  

## 操作步骤<a name="s738501c07aa4426eaeea764d9297251d"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“实例管理“页面，选择指定的实例，单击“更多 \> 创建只读”，进入“服务选型”页面。

    您也可在实例的“基本信息“页面，单击实例拓扑图中，主实例下方的添加按钮![](figures/添加只读-17.png)，创建只读实例。

5.  在“服务选型”页面，填选实例相关信息后，单击“立即创建“。

    **表 1**  基本信息

    <a name="table64274465191013"></a>
    <table><thead align="left"><tr id="row10238256191013"><th class="cellrowborder" valign="top" width="17.669999999999998%" id="mcps1.2.3.1.1"><p id="p45227061191215"><a name="p45227061191215"></a><a name="p45227061191215"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="82.33%" id="mcps1.2.3.1.2"><p id="p39513321191215"><a name="p39513321191215"></a><a name="p39513321191215"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1566273919197"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="p6072235519197"><a name="p6072235519197"></a><a name="p6072235519197"></a>当前区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="p1956370319197"><a name="p1956370319197"></a><a name="p1956370319197"></a>只读实例默认与主实例在同一区域。</p>
    </td>
    </tr>
    <tr id="row15611204134715"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="p6818201134720"><a name="p6818201134720"></a><a name="p6818201134720"></a>实例名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="p40771789134814"><a name="p40771789134814"></a><a name="p40771789134814"></a>实例名称的长度在4~64个字符之间，必须以字母开头，可包含大写字母、小写字母、数字、中划线或下划线，不能包含其他特殊字符。</p>
    </td>
    </tr>
    <tr id="row16096253164355"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="p4480828164359"><a name="p4480828164359"></a><a name="p4480828164359"></a>数据库引擎</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="p11852143122115"><a name="p11852143122115"></a><a name="p11852143122115"></a>默认与主实例的数据库引擎一致，不可更改。</p>
    </td>
    </tr>
    <tr id="row56400291164351"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="p45320621164359"><a name="p45320621164359"></a><a name="p45320621164359"></a>数据库版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="p611818314226"><a name="p611818314226"></a><a name="p611818314226"></a>默认与主实例的数据库版本一致，不可更改。</p>
    </td>
    </tr>
    <tr id="row986226171118"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="p5363100191215"><a name="p5363100191215"></a><a name="p5363100191215"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><div class="p" id="p114913522132"><a name="p114913522132"></a><a name="p114913522132"></a>华为云关系型数据库服务支持在同一个可用区内，或者跨可用区部署数据库主实例和只读实例，只读实例的选择和主实例可用区对应情况：<a name="ul17956749161310"></a><a name="ul17956749161310"></a><ul id="ul17956749161310"><li>相同，主实例和只读实例会部署在同一个可用区。</li><li>不同，主实例和只读实例会部署在不同的可用区，提高可靠性。</li></ul>
    </div>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  规格与存储

    <a name="table5231736819158"></a>
    <table><thead align="left"><tr id="row5678434919158"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p48655908191548"><a name="p48655908191548"></a><a name="p48655908191548"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p48814496191548"><a name="p48814496191548"></a><a name="p48814496191548"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row440922819158"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p19368524191620"><a name="p19368524191620"></a><a name="p19368524191620"></a>性能规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p3612111215507"><a name="p3612111215507"></a><a name="p3612111215507"></a>实例的CPU和内存。不同性能规格对应不同连接数和最大IOPS。</p>
    <p id="p781114612508"><a name="p781114612508"></a><a name="p781114612508"></a>关于性能规格详情，请参见<a href="https://support.huaweicloud.com/productdesc-rds/rds_01_0029.html" target="_blank" rel="noopener noreferrer">数据库实例规格</a>。</p>
    <p id="p5429821515"><a name="p5429821515"></a><a name="p5429821515"></a></p>
    <p id="p12042810516"><a name="p12042810516"></a><a name="p12042810516"></a></p>
    <p id="p4689621196"><a name="p4689621196"></a><a name="p4689621196"></a></p>
    <p id="p860165515523"><a name="p860165515523"></a><a name="p860165515523"></a>创建成功后可进行规格变更，请参见<a href="https://support.huaweicloud.com/usermanual-rds/zh-cn_topic_scale_rds.html" target="_blank" rel="noopener noreferrer">变更实例的CPU和内存规格</a>。</p>
    <p id="p4610514532"><a name="p4610514532"></a><a name="p4610514532"></a></p>
    <p id="p19542517536"><a name="p19542517536"></a><a name="p19542517536"></a></p>
    <p id="p38285458348"><a name="p38285458348"></a><a name="p38285458348"></a></p>
    <p id="p162810522252"><a name="p162810522252"></a><a name="p162810522252"></a>对于在专属计算集群上的实例，性能规格只支持通用增强型。</p>
    </td>
    </tr>
    <tr id="row373765819158"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p3335747191620"><a name="p3335747191620"></a><a name="p3335747191620"></a>存储类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1720172914352"><a name="p1720172914352"></a><a name="p1720172914352"></a>实例的存储类型决定实例的读写速度。最大吞吐量越高，读写速度越快。</p>
    <a name="ul1898975217346"></a><a name="ul1898975217346"></a><ul id="ul1898975217346"><li>超高I/O：最大吞吐量350MB/s</li></ul>
    <div class="note" id="note10322185155413"><a name="note10322185155413"></a><a name="note10322185155413"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p13798414122611"><a name="p13798414122611"></a><a name="p13798414122611"></a>选择<span class="uicontrol" id="uicontrol13165326121312"><a name="uicontrol13165326121312"></a><a name="uicontrol13165326121312"></a>“专属存储”</span>的用户默认只显示购买专属分布式存储服务时选择的存储类型。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row5103267419158"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p4000592019158"><a name="p4000592019158"></a><a name="p4000592019158"></a>存储空间</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p253463643920"><a name="p253463643920"></a><a name="p253463643920"></a>您申请的存储空间会有必要的文件系统开销，这些开销包括索引节点和保留块，以及数据库运行必需的空间。</p>
    <p id="p5480144445014"><a name="p5480144445014"></a><a name="p5480144445014"></a>只读实例的存储空间大小默认与主实例一致。</p>
    </td>
    </tr>
    <tr id="row1745919202459"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p595744141914"><a name="p595744141914"></a><a name="p595744141914"></a>磁盘加密</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><a name="ul133881550588"></a><a name="ul133881550588"></a><ul id="ul133881550588"><li>不加密：未开启加密功能。</li><li>加密：提高数据安全性，对性能有一定影响。<p id="p1950185719127"><a name="p1950185719127"></a><a name="p1950185719127"></a>密钥名称：选择或创建密钥，该密钥是最终租户密钥。</p>
    <div class="note" id="note2431518191315"><a name="note2431518191315"></a><a name="note2431518191315"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul36901923165110"></a><a name="ul36901923165110"></a><ul id="ul36901923165110"><li>实例创建成功后，不可修改磁盘加密状态，且无法更改密钥。存放在对象存储服务上的备份数据不会被加密。</li><li><span>华为云关系型数据库</span>实例创建成功后，请勿禁用或删除正在使用的密钥，否则会导致<span>华为云关系型数据库</span>服务不可用，数据无法恢复。</li><li>创建密钥可参考《数据加密服务用户指南》的“创建密钥”章节内容。</li></ul>
    </div></div>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  网络

    <a name="table37304444569"></a>
    <table><thead align="left"><tr id="row1273164417563"><th class="cellrowborder" valign="top" width="18.81%" id="mcps1.2.3.1.1"><p id="p0966175011569"><a name="p0966175011569"></a><a name="p0966175011569"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="81.19%" id="mcps1.2.3.1.2"><p id="p2731144465614"><a name="p2731144465614"></a><a name="p2731144465614"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1073164415564"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.2.3.1.1 "><p id="p77311441563"><a name="p77311441563"></a><a name="p77311441563"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.19%" headers="mcps1.2.3.1.2 "><p id="p13731104420562"><a name="p13731104420562"></a><a name="p13731104420562"></a>和主实例相同。</p>
    </td>
    </tr>
    <tr id="row1173114475611"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.2.3.1.1 "><p id="p1273115449568"><a name="p1273115449568"></a><a name="p1273115449568"></a>子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.19%" headers="mcps1.2.3.1.2 "><p id="p1731174415614"><a name="p1731174415614"></a><a name="p1731174415614"></a>和主实例相同，创建只读实例时RDS会自动为您配置内网地址，您也可输入子网号段内未使用的内网地址，实例创建成功后该内网地址暂不可修改。</p>
    </td>
    </tr>
    <tr id="row573117446566"><td class="cellrowborder" valign="top" width="18.81%" headers="mcps1.2.3.1.1 "><p id="p573164465611"><a name="p573164465611"></a><a name="p573164465611"></a>内网安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.19%" headers="mcps1.2.3.1.2 "><p id="p18524934105811"><a name="p18524934105811"></a><a name="p18524934105811"></a>和主实例相同。</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  在“规格确认”页面，进行信息确认。
    -   如果需要重新选择，单击“上一步”，回到服务选型页面修改基本信息。
    -   信息确认无误，单击“提交“，下发新增只读实例请求。

7.  只读实例创建成功后，用户可以在“实例管理”页面，选择只读实例所对应的实例，单击![](figures/下拉选择.png)对其进行查看和管理。

    您也可以在基本信息页面的“实例拓扑图“中，单击只读实例的名称，进入该只读实例的“基本信息“页面，对其进行查看和管理。

    您可以通过“任务中心“查看详细进度和结果。具体请参见[任务中心](https://support.huaweicloud.com/usermanual-rds/rds_05_0007.html)。


