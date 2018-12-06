# 将数据库实例恢复到指定时间点<a name="TOPIC_0142028602"></a>

## 操作场景<a name="section3037032812838"></a>

华为云关系型数据库服务支持使用已有的自动备份，恢复实例数据到指定时间点。

账户余额大于等于0元，才可恢复到新实例。

## 背景<a name="section88314283419"></a>

开启操作保护的用户，在进行敏感操作时，通过进行二次认证再次确认您的身份，进一步提高帐号安全性，有效保护您安全使用云产品。关于如何开启操作保护，具体请参考《统一身份认证服务用户指南》的内容。

## 操作步骤<a name="section116671682181"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“实例管理“页面，选择指定的实例，单击实例名称。
5.  在“备份恢复“页签，单击“恢复到指定时间点“。
6.  选择需要恢复的时间区间，选择或输入该恢复时间区间内的一个恢复时间点，选择恢复方式，若选择恢复到当前实例，且您已开启操作保护，在“恢复到指定时间点“弹框，单击“去验证“，跳转至验证页面，单击“免费获取验证码“，正确输入验证码并单击“认证“，验证页面自动关闭。单击“确定”。
    -   恢复到新实例

        跳转到“恢复到新实例”的服务选型页面：

        -   数据库引擎和数据库端口，与原实例相同，不可修改。
        -   数据库版本支持从低版本恢复到高版本，详见[表1](#table128279260542)。

            **表 1**  恢复支持的版本规则

            <a name="table128279260542"></a>
            <table><thead align="left"><tr id="row1827172618547"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p8827026105418"><a name="p8827026105418"></a><a name="p8827026105418"></a>原数据库版本</p>
            </th>
            <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p148277267543"><a name="p148277267543"></a><a name="p148277267543"></a>可恢复到的版本</p>
            </th>
            </tr>
            </thead>
            <tbody><tr id="row1782722614541"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p17747114017402"><a name="p17747114017402"></a><a name="p17747114017402"></a>2008 R2 WEB</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p151700575920"><a name="p151700575920"></a><a name="p151700575920"></a>2008 R2 WEB</p>
            <p id="p1417345165915"><a name="p1417345165915"></a><a name="p1417345165915"></a>2008 R2企业版 </p>
            </td>
            </tr>
            <tr id="row1682892685419"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p99214617595"><a name="p99214617595"></a><a name="p99214617595"></a>2008 R2企业版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1832711552590"><a name="p1832711552590"></a><a name="p1832711552590"></a>2008 R2企业版 </p>
            </td>
            </tr>
            <tr id="row1032819018581"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p20268912154019"><a name="p20268912154019"></a><a name="p20268912154019"></a>2014 WEB</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9761135919595"><a name="p9761135919595"></a><a name="p9761135919595"></a>2014 WEB</p>
            <p id="p1276295955913"><a name="p1276295955913"></a><a name="p1276295955913"></a>2014标准版 </p>
            <p id="p49810551116"><a name="p49810551116"></a><a name="p49810551116"></a>2014企业版 </p>
            </td>
            </tr>
            <tr id="row1855235217576"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3524791705"><a name="p3524791705"></a><a name="p3524791705"></a>2014标准版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p04601614604"><a name="p04601614604"></a><a name="p04601614604"></a>2014标准版 </p>
            <p id="p18460161418010"><a name="p18460161418010"></a><a name="p18460161418010"></a>2014企业版 </p>
            </td>
            </tr>
            <tr id="row2836457115710"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1632317191904"><a name="p1632317191904"></a><a name="p1632317191904"></a>2014企业版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p186343201806"><a name="p186343201806"></a><a name="p186343201806"></a>2014企业版 </p>
            </td>
            </tr>
            <tr id="row89341541575"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p16698154683910"><a name="p16698154683910"></a><a name="p16698154683910"></a>2016 WEB</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1292152915012"><a name="p1292152915012"></a><a name="p1292152915012"></a>2016 WEB</p>
            <p id="p59246291304"><a name="p59246291304"></a><a name="p59246291304"></a>2016标准版 </p>
            <p id="p1992415291402"><a name="p1992415291402"></a><a name="p1992415291402"></a>2016企业版 </p>
            </td>
            </tr>
            <tr id="row1882816269549"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1260511426018"><a name="p1260511426018"></a><a name="p1260511426018"></a>2016标准版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p06405436014"><a name="p06405436014"></a><a name="p06405436014"></a>2016标准版</p>
            <p id="p1464110430017"><a name="p1464110430017"></a><a name="p1464110430017"></a>2016企业版 </p>
            </td>
            </tr>
            <tr id="row3427249175712"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14654175019014"><a name="p14654175019014"></a><a name="p14654175019014"></a>2016企业版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p77341511808"><a name="p77341511808"></a><a name="p77341511808"></a>2016企业版 </p>
            </td>
            </tr>
            </tbody>
            </table>

        -   数据库密码需重新设置。
        -   其他参数默认和原实例设置相同，用户可修改。

    -   恢复到当前实例

        >![](public_sys-resources/icon-notice.gif) **注意：**   
        >恢复到当前实例会导致实例数据被覆盖，且还原过程中实例将不可用。  


7.  查看恢复结果。

    -   恢复到新实例，为用户重新创建一个和该备份数据相同的实例。可看到实例由“创建中“变为“正常“，说明恢复成功。

        恢复成功的新实例是一个独立的实例，与原有实例没有关联。如需使用只读实例，请重新在该实例上进行创建。

    -   恢复到当前实例，在“实例管理”页面，可查看该实例下所有实例状态为“恢复中”，恢复完成后，实例状态由“恢复中”变为“正常”。

        用户可在界面上看到一个新的可恢复时间区间，且该时间区间与原时间区间有一段时间差（即恢复占用的时间）。


    创建或恢复完成后，系统会自动执行一次全量备份。


