# 将数据库实例恢复到指定时间点<a name="zh-cn_topic_0053089726"></a>

## 操作场景<a name="section3037032812838"></a>

华为云关系型数据库服务支持使用已有的自动备份，恢复实例数据到指定时间点。

账户余额大于等于0元，才可恢复到新实例。

## 背景<a name="section88314283419"></a>

开启操作保护的用户，在进行敏感操作时，通过进行二次认证再次确认您的身份，进一步提高帐号安全性，有效保护您安全使用云产品。关于如何开启操作保护，具体请参考《统一身份认证服务用户指南》的内容。

当用户在某个时间点删除了某个数据库，或者修改了某个数据库的一些记录时，用户需要只对该数据库实例进行恢复，而不需要将整个实例进行恢复。您可以根据需要恢复库表。

## 操作步骤<a name="section116671682181"></a>

1.  [登录云数据库](https://support.huaweicloud.com/qs-rds/rds_login.html)。
2.  在“实例管理“页面，选择指定的实例，单击实例名称。
3.  在左侧导航栏中选择“备份恢复“页签，单击“恢复到指定时间点“。
4.  在“恢复到指定时间点“弹出框中，填选相关信息，单击“确定“。
    1.  选择恢复日期，可恢复的时间区间，输入该恢复时间区间内的一个恢复时间点。
    2.  选择恢复方式，若选择恢复到当前实例，且您已开启操作保护，在“恢复到指定时间点“弹框，单击“去验证“，跳转至验证页面，单击“免费获取验证码“，正确输入验证码并单击“认证“，验证页面自动关闭。
        -   恢复到新实例

            跳转到“恢复到新实例”的服务选型页面：

            -   数据库引擎和数据库端口，与原实例相同，数据库端口为默认值1433，以上参数皆不可修改。
            -   数据库版本支持从低版本恢复到高版本，详见[表1](#table543751181314)。

                **表 1**  恢复支持的版本规则

                <a name="table543751181314"></a>
                <table><thead align="left"><tr id="row54615118137"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p1848105111137"><a name="p1848105111137"></a><a name="p1848105111137"></a>原数据库版本</p>
                </th>
                <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p650175112134"><a name="p650175112134"></a><a name="p650175112134"></a>可恢复到的版本</p>
                </th>
                </tr>
                </thead>
                <tbody><tr id="row352651141320"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p125325111319"><a name="p125325111319"></a><a name="p125325111319"></a>2008 R2 web</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1154451191317"><a name="p1154451191317"></a><a name="p1154451191317"></a>2008 R2 WEB</p>
                <p id="p1556165110134"><a name="p1556165110134"></a><a name="p1556165110134"></a>2008 R2 企业版 </p>
                </td>
                </tr>
                <tr id="row1366551101310"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p36765115132"><a name="p36765115132"></a><a name="p36765115132"></a>2008 R2 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1970135171315"><a name="p1970135171315"></a><a name="p1970135171315"></a>2008 R2 企业版 </p>
                </td>
                </tr>
                <tr id="row675145131315"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14761516137"><a name="p14761516137"></a><a name="p14761516137"></a>2012 web版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p157745118133"><a name="p157745118133"></a><a name="p157745118133"></a>2012 web版</p>
                <p id="p127845121311"><a name="p127845121311"></a><a name="p127845121311"></a>2012 标准版</p>
                <p id="p1079155141313"><a name="p1079155141313"></a><a name="p1079155141313"></a>2012 企业版</p>
                </td>
                </tr>
                <tr id="row880125121314"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p2821251151315"><a name="p2821251151315"></a><a name="p2821251151315"></a>2012 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p17838517133"><a name="p17838517133"></a><a name="p17838517133"></a>2012 标准版</p>
                <p id="p483251171317"><a name="p483251171317"></a><a name="p483251171317"></a>2012 企业版</p>
                </td>
                </tr>
                <tr id="row58445118131"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p128635181312"><a name="p128635181312"></a><a name="p128635181312"></a>2012 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1287155110135"><a name="p1287155110135"></a><a name="p1287155110135"></a>2012 企业版</p>
                </td>
                </tr>
                <tr id="row18871051151319"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p148811514135"><a name="p148811514135"></a><a name="p148811514135"></a>2014 web</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p19015171313"><a name="p19015171313"></a><a name="p19015171313"></a>2014 web</p>
                <p id="p139005171317"><a name="p139005171317"></a><a name="p139005171317"></a>2014 标准版 </p>
                <p id="p1292551181311"><a name="p1292551181311"></a><a name="p1292551181311"></a>2014 企业版 </p>
                </td>
                </tr>
                <tr id="row199419511130"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p596651161318"><a name="p596651161318"></a><a name="p596651161318"></a>2014 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8996515136"><a name="p8996515136"></a><a name="p8996515136"></a>2014 标准版 </p>
                <p id="p410165151318"><a name="p410165151318"></a><a name="p410165151318"></a>2014 企业版 </p>
                </td>
                </tr>
                <tr id="row1210325113130"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p11040519135"><a name="p11040519135"></a><a name="p11040519135"></a>2014 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1710775151317"><a name="p1710775151317"></a><a name="p1710775151317"></a>2014 企业版 </p>
                </td>
                </tr>
                <tr id="row810912517138"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4111135115130"><a name="p4111135115130"></a><a name="p4111135115130"></a>2016 web</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9112351151318"><a name="p9112351151318"></a><a name="p9112351151318"></a>2016 web</p>
                <p id="p15113751141311"><a name="p15113751141311"></a><a name="p15113751141311"></a>2016 标准版 </p>
                <p id="p19115135116138"><a name="p19115135116138"></a><a name="p19115135116138"></a>2016 企业版 </p>
                </td>
                </tr>
                <tr id="row011715510139"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p131184519136"><a name="p131184519136"></a><a name="p131184519136"></a>2016 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p612025161310"><a name="p612025161310"></a><a name="p612025161310"></a>2016 标准版</p>
                <p id="p171221651121311"><a name="p171221651121311"></a><a name="p171221651121311"></a>2016 企业版 </p>
                </td>
                </tr>
                <tr id="row9124651171315"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p312511518134"><a name="p312511518134"></a><a name="p312511518134"></a>2016 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p512815518130"><a name="p512815518130"></a><a name="p512815518130"></a>2016 企业版 </p>
                </td>
                </tr>
                <tr id="row19130165121313"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1413110517130"><a name="p1413110517130"></a><a name="p1413110517130"></a>2017 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p11132205118132"><a name="p11132205118132"></a><a name="p11132205118132"></a>2017 企业版</p>
                </td>
                </tr>
                </tbody>
                </table>

            -   存储空间大小默认和原实例相同，且必须大于或等于原实例存储空间大小，数据库密码需重新设置。
            -   其他参数默认，用户可设置，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0053089697.md)。
            -               -   
        -   恢复到当前实例

            >![](public_sys-resources/icon-notice.gif) **注意：**   
            >恢复到当前实例会导致当前实例的全部数据被覆盖，并且恢复过程中数据库不可用。  

        -   恢复到已有实例

            >![](public_sys-resources/icon-notice.gif) **注意：**   
            >-   恢复到已有实例会导致实例数据被覆盖，且恢复过程中实例将不可用。  
            >-   请确保目标实例的存储空间大于或等于当前实例，否则会导致任务下发失败。  

            选择目标实例，单击“下一步“。

            **图 1**  恢复到已有实例<a name="fig123128437496"></a>  
            ![](figures/恢复到已有实例-8.png "恢复到已有实例")


    3.  勾选需要恢复的数据库，您可以根据需要，自定义恢复后的新数据库名。如果恢复到的新数据库名未填写，默认为您恢复到原数据库。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >-   新数据库名不能与原数据库重名。  
        >-   新数据库名不能包含rdsadmin、master、msdb、tempdb、model或resource字段（不区分大小写）。  
        >-   数据库名称长度在1\~128个字符之间，包含字母、数字或下划线，不能包含其他特殊字符。  


5.  查看恢复结果。
    -   恢复到新实例

        RDS会为您重新创建一个和该备份数据相同的实例。可看到实例由“创建中“变为“正常“，说明恢复成功。

        恢复成功的新实例是一个独立的实例，与原有实例没有关联。

    -   恢复到当前实例
    -   在“实例管理”页面，可查看该实例下所有实例状态为“恢复中”，恢复完成后，实例状态由“恢复中”变为“正常”。

        用户可在界面上看到一个新的可恢复时间区间，且该时间区间与原时间区间有一段时间差（即恢复占用的时间）。

    -   恢复到已有实例

        在“实例管理”页面，可查看该实例下所有实例状态为“恢复中”，恢复完成后，实例状态由“恢复中”变为“正常”。



