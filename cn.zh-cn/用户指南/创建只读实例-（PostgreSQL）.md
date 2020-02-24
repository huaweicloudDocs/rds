# 创建只读实例<a name="rds_add_read_replica_pg"></a>

## 操作场景<a name="s9f95e14048064f63a1d9be0c9f685f07"></a>

只读实例用于增强主实例的读能力，减轻主实例负载。

华为云关系型数据库单实例或主备实例创建成功后，可根据业务需要创建只读实例。

>![](public_sys-resources/icon-note.gif) **说明：**   
>账户余额大于等于0元，才可新增只读实例。  
>一个主实例中，最多可以增加5个只读实例。  

## 操作步骤<a name="s738501c07aa4426eaeea764d9297251d"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“实例管理“页面，选择指定的实例，单击操作列的“更多 \> 创建只读”，进入“服务选型”页面。

    您也可在实例的“基本信息“页面，单击实例拓扑图中，主实例下方的添加按钮![](figures/添加只读-13.png)，创建只读实例。

5.  在“服务选型”页面，填选实例相关信息后，单击“立即创建“。

    **表 1**  基本信息

    <a name="table374110104381"></a>
    <table><thead align="left"><tr id="rb89ee2680ad341c88d3dae6ce26e0bbb"><th class="cellrowborder" valign="top" width="17.669999999999998%" id="mcps1.2.3.1.1"><p id="a8e1ea4dccadf43b3a23421bc1ce2268a"><a name="a8e1ea4dccadf43b3a23421bc1ce2268a"></a><a name="a8e1ea4dccadf43b3a23421bc1ce2268a"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="82.33%" id="mcps1.2.3.1.2"><p id="a9fa63d1ff45b4610bf73a3eb62e4ba87"><a name="a9fa63d1ff45b4610bf73a3eb62e4ba87"></a><a name="a9fa63d1ff45b4610bf73a3eb62e4ba87"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="re985d3e83e2940f0a844662d774985b3"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="a7f6c93c6dc024e75a7ad763abeeed623"><a name="a7f6c93c6dc024e75a7ad763abeeed623"></a><a name="a7f6c93c6dc024e75a7ad763abeeed623"></a>当前区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="adf7fc0c3b6b34f4a9a4c808ffbc9bc96"><a name="adf7fc0c3b6b34f4a9a4c808ffbc9bc96"></a><a name="adf7fc0c3b6b34f4a9a4c808ffbc9bc96"></a>只读实例默认与主实例在同一区域。</p>
    </td>
    </tr>
    <tr id="r09dbcd8e7d9145e290afbbf334c988bd"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="ac7855025749c41a6af6984e088f66e3b"><a name="ac7855025749c41a6af6984e088f66e3b"></a><a name="ac7855025749c41a6af6984e088f66e3b"></a>实例名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="aa4aaba6d2e084151aee6f1772bc7b2bd"><a name="aa4aaba6d2e084151aee6f1772bc7b2bd"></a><a name="aa4aaba6d2e084151aee6f1772bc7b2bd"></a>实例名称的长度在4~64个字符之间，必须以字母开头，可包含大写字母、小写字母、数字、中划线或下划线，不能包含其他特殊字符。</p>
    </td>
    </tr>
    <tr id="r9d09bfd516b14798a4888b86d7fed5fa"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="a15abca176028499babd933b839090f5e"><a name="a15abca176028499babd933b839090f5e"></a><a name="a15abca176028499babd933b839090f5e"></a>数据库引擎</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="a696cfb29bbb1496797619e0489df6aeb"><a name="a696cfb29bbb1496797619e0489df6aeb"></a><a name="a696cfb29bbb1496797619e0489df6aeb"></a>默认与主实例的数据库引擎一致，不可更改。</p>
    </td>
    </tr>
    <tr id="r216f7256942a42eaa3bd6c7bcbabe851"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="aa85ac38952924c36baa8e440d145831f"><a name="aa85ac38952924c36baa8e440d145831f"></a><a name="aa85ac38952924c36baa8e440d145831f"></a>数据库版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0104704897_p611818314226"><a name="zh-cn_topic_0104704897_p611818314226"></a><a name="zh-cn_topic_0104704897_p611818314226"></a>默认与主实例的数据库版本一致，不可更改。</p>
    </td>
    </tr>
    <tr id="r36a71173a2eb4727927e38f116c29a9c"><td class="cellrowborder" valign="top" width="17.669999999999998%" headers="mcps1.2.3.1.1 "><p id="a9633693a57b745308b99fd0f21c81c5e"><a name="a9633693a57b745308b99fd0f21c81c5e"></a><a name="a9633693a57b745308b99fd0f21c81c5e"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="82.33%" headers="mcps1.2.3.1.2 "><div class="p" id="zh-cn_topic_0104704897_p114913522132"><a name="zh-cn_topic_0104704897_p114913522132"></a><a name="zh-cn_topic_0104704897_p114913522132"></a>华为云关系型数据库服务支持在同一个可用区内或者跨可用区部署数据库主实例和只读实例，只读实例的选择和主实例可用区对应情况：<a name="u726b397bae614cd382ea471215ca9a96"></a><a name="u726b397bae614cd382ea471215ca9a96"></a><ul id="u726b397bae614cd382ea471215ca9a96"><li>相同，主实例和只读实例会部署在同一个可用区。</li><li>不同，主实例和只读实例会部署在不同的可用区，提高可靠性。</li></ul>
    </div>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  规格与存储

    <a name="table1347794173811"></a>
    <table><thead align="left"><tr id="reea1444f54b7482fa3815dbe9dbe634f"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="aa1e09dcf216a440b94469aaae6b72510"><a name="aa1e09dcf216a440b94469aaae6b72510"></a><a name="aa1e09dcf216a440b94469aaae6b72510"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="ab0911e657d3b4abcb1fd222aa87e3624"><a name="ab0911e657d3b4abcb1fd222aa87e3624"></a><a name="ab0911e657d3b4abcb1fd222aa87e3624"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r00fdd9f8134240838d06a3321a77c2ce"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="a5859384263c14ec894f66ca225c4b2b1"><a name="a5859384263c14ec894f66ca225c4b2b1"></a><a name="a5859384263c14ec894f66ca225c4b2b1"></a>性能规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="a6dd1e8437a244c7993a0392e5905ae97"><a name="a6dd1e8437a244c7993a0392e5905ae97"></a><a name="a6dd1e8437a244c7993a0392e5905ae97"></a>实例的CPU和内存。不同性能规格对应不同连接数和最大IOPS。</p>
    <p id="zh-cn_topic_0104704897_p781114612508"><a name="zh-cn_topic_0104704897_p781114612508"></a><a name="zh-cn_topic_0104704897_p781114612508"></a>关于性能规格详情，请参见<a href="https://support.huaweicloud.com/productdesc-rds/zh-cn_topic_0043898355.html" target="_blank" rel="noopener noreferrer">数据库实例规格</a>。</p>
    <p id="zh-cn_topic_0104704897_p5429821515"><a name="zh-cn_topic_0104704897_p5429821515"></a><a name="zh-cn_topic_0104704897_p5429821515"></a></p>
    <p id="zh-cn_topic_0104704897_p12042810516"><a name="zh-cn_topic_0104704897_p12042810516"></a><a name="zh-cn_topic_0104704897_p12042810516"></a></p>
    <p id="zh-cn_topic_0104704897_p4689621196"><a name="zh-cn_topic_0104704897_p4689621196"></a><a name="zh-cn_topic_0104704897_p4689621196"></a></p>
    <p id="zh-cn_topic_0104704897_p860165515523"><a name="zh-cn_topic_0104704897_p860165515523"></a><a name="zh-cn_topic_0104704897_p860165515523"></a>创建成功后可进行规格变更，请参见<a href="https://support.huaweicloud.com/usermanual-rds/zh-cn_topic_scale_rds.html" target="_blank" rel="noopener noreferrer">变更实例的CPU和内存规格</a>。</p>
    <p id="zh-cn_topic_0104704897_p4610514532"><a name="zh-cn_topic_0104704897_p4610514532"></a><a name="zh-cn_topic_0104704897_p4610514532"></a></p>
    <p id="zh-cn_topic_0104704897_p19542517536"><a name="zh-cn_topic_0104704897_p19542517536"></a><a name="zh-cn_topic_0104704897_p19542517536"></a></p>
    <p id="zh-cn_topic_0104704897_p38285458348"><a name="zh-cn_topic_0104704897_p38285458348"></a><a name="zh-cn_topic_0104704897_p38285458348"></a></p>
    <p id="p12755194085317"><a name="p12755194085317"></a><a name="p12755194085317"></a>对于在专属计算集群上的实例，性能规格只支持通用增强型。</p>
    </td>
    </tr>
    <tr id="rd48db41ccd0a42aaace73aa321ded210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="a7665201e013c448889b5c690a28838ed"><a name="a7665201e013c448889b5c690a28838ed"></a><a name="a7665201e013c448889b5c690a28838ed"></a>存储类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="a2fa36ff2f41d443d95434fc47d037a38"><a name="a2fa36ff2f41d443d95434fc47d037a38"></a><a name="a2fa36ff2f41d443d95434fc47d037a38"></a>实例的存储类型决定实例的读写速度。最大吞吐量越高，读写速度越快。</p>
    <a name="ul1995202413543"></a><a name="ul1995202413543"></a><ul id="ul1995202413543"><li>超高I/O：最大吞吐量350MB/s</li></ul>
    <div class="note" id="na8cf7543966c40e8b6b9e6dae66b9542"><a name="na8cf7543966c40e8b6b9e6dae66b9542"></a><a name="na8cf7543966c40e8b6b9e6dae66b9542"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="u0feebaf7275141479561a0ffac8ae532"></a><a name="u0feebaf7275141479561a0ffac8ae532"></a><ul id="u0feebaf7275141479561a0ffac8ae532"><li>选择<span class="uicontrol" id="u9a8f9a2be6204beca68a501fa92b2f7d"><a name="u9a8f9a2be6204beca68a501fa92b2f7d"></a><a name="u9a8f9a2be6204beca68a501fa92b2f7d"></a>“专属存储”</span>的用户默认只显示购买专属分布式存储服务时选择的存储类型。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="rc2c662af50844f29956928f7f7936b37"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="a36c5159435ea4e93931bb4045e68b67e"><a name="a36c5159435ea4e93931bb4045e68b67e"></a><a name="a36c5159435ea4e93931bb4045e68b67e"></a>存储空间</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0104704897_p253463643920"><a name="zh-cn_topic_0104704897_p253463643920"></a><a name="zh-cn_topic_0104704897_p253463643920"></a>您申请的存储空间会有必要的文件系统开销，这些开销包括索引节点和保留块，以及数据库运行必需的空间。</p>
    <p id="p9481145015"><a name="p9481145015"></a><a name="p9481145015"></a>只读实例的存储空间大小默认与主实例一致。</p>
    </td>
    </tr>
    <tr id="row15865034273"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0104704897_p595744141914"><a name="zh-cn_topic_0104704897_p595744141914"></a><a name="zh-cn_topic_0104704897_p595744141914"></a>磁盘加密</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><a name="u2597363a1b7143ff970ab2e4246958f6"></a><a name="u2597363a1b7143ff970ab2e4246958f6"></a><ul id="u2597363a1b7143ff970ab2e4246958f6"><li>不加密：未开启加密功能。</li><li>加密：提高数据安全性，对性能有一定影响。<p id="a17a16a1c2ad94e0792279ac47f7fae8e"><a name="a17a16a1c2ad94e0792279ac47f7fae8e"></a><a name="a17a16a1c2ad94e0792279ac47f7fae8e"></a>密钥名称：选择或创建密钥，该密钥是最终租户密钥。</p>
    <div class="note" id="n84f031fa78db48518e67cda11ff5ea41"><a name="n84f031fa78db48518e67cda11ff5ea41"></a><a name="n84f031fa78db48518e67cda11ff5ea41"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="uc8be307a454d46a08874a85a21814a71"></a><a name="uc8be307a454d46a08874a85a21814a71"></a><ul id="uc8be307a454d46a08874a85a21814a71"><li>实例创建成功后，不可修改磁盘加密状态，且无法更改密钥。存放在对象存储服务上的备份数据不会被加密。</li><li><span>华为云关系型数据库</span>实例创建成功后，请勿禁用或删除正在使用的密钥，否则会导致<span>华为云关系型数据库</span>服务不可用，数据无法恢复。</li><li>创建密钥可参考《数据加密服务用户指南》的“创建密钥”章节内容。</li></ul>
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
    <td class="cellrowborder" valign="top" width="81.19%" headers="mcps1.2.3.1.2 "><p id="p1731174415614"><a name="p1731174415614"></a><a name="p1731174415614"></a>和主实例相同，创建只读实例时RDS会自动为您配置内网地址，您也可输入子网号段内未使用的内网地址，实例创建成功后该内网地址可修改。</p>
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


