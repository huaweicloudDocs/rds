# 恢复备份<a name="zh-cn_topic_0053089727"></a>

## 操作场景<a name="section51567119122258"></a>

华为云关系型数据库支持使用已有的自动备份和手动备份，将实例数据恢复到备份被创建时的状态。

## 限制条件<a name="section177191741104915"></a>

账户余额大于等于0元，才可恢复到新实例。

## 操作步骤<a name="section51247315503"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“备份管理”页面，选择需要恢复的备份，单击操作列的“恢复“。

    您也可在“实例管理“页面，单击指定的实例名称，在左侧导航栏单击“备份恢复“，在“全量备份”页签下单击目标备份对应的操作列中的“恢复“。

5.  在“恢复到指定时间点“弹出框中，填选相关信息，单击“确定“。
    1.  选择需要的恢复方式。
        -   新实例
        -   跳转到“恢复到新实例”的服务选型页面：
            -   数据库引擎与原实例相同，数据库端口默认为1433，以上参数皆不可修改。
            -   数据库版本支持从低版本恢复到高版本，详见[表1](#table1334944713437)。

                **表 1**  恢复支持的版本规则

                <a name="table1334944713437"></a>
                <table><thead align="left"><tr id="row1134094714310"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p434016479436"><a name="p434016479436"></a><a name="p434016479436"></a>原数据库版本</p>
                </th>
                <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p434016477435"><a name="p434016477435"></a><a name="p434016477435"></a>可恢复到的版本</p>
                </th>
                </tr>
                </thead>
                <tbody><tr id="row934134715438"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p19340154712439"><a name="p19340154712439"></a><a name="p19340154712439"></a>2008 R2 web</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p93401647114313"><a name="p93401647114313"></a><a name="p93401647114313"></a>2008 R2 web</p>
                <p id="p183411547134316"><a name="p183411547134316"></a><a name="p183411547134316"></a>2008 R2 企业版 </p>
                </td>
                </tr>
                <tr id="row334116472437"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p53411147104319"><a name="p53411147104319"></a><a name="p53411147104319"></a>2008 R2 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p17341847184318"><a name="p17341847184318"></a><a name="p17341847184318"></a>2008 R2 企业版 </p>
                </td>
                </tr>
                <tr id="row834117475436"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p12341164784315"><a name="p12341164784315"></a><a name="p12341164784315"></a>2012 web版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8341114712433"><a name="p8341114712433"></a><a name="p8341114712433"></a>2012 web版</p>
                <p id="p4341947154314"><a name="p4341947154314"></a><a name="p4341947154314"></a>2012 标准版</p>
                <p id="p17341184720439"><a name="p17341184720439"></a><a name="p17341184720439"></a>2012 企业版</p>
                </td>
                </tr>
                <tr id="row1234244720438"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p934116479439"><a name="p934116479439"></a><a name="p934116479439"></a>2012 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p19342747174317"><a name="p19342747174317"></a><a name="p19342747174317"></a>2012 标准版</p>
                <p id="p193421947184317"><a name="p193421947184317"></a><a name="p193421947184317"></a>2012 企业版</p>
                </td>
                </tr>
                <tr id="row1234215477432"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p10342124784312"><a name="p10342124784312"></a><a name="p10342124784312"></a>2012 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p16342134716439"><a name="p16342134716439"></a><a name="p16342134716439"></a>2012 企业版</p>
                </td>
                </tr>
                <tr id="row53451947184320"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p12342174712432"><a name="p12342174712432"></a><a name="p12342174712432"></a>2014 web</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p183421947174316"><a name="p183421947174316"></a><a name="p183421947174316"></a>2014 web</p>
                <p id="p18344144774315"><a name="p18344144774315"></a><a name="p18344144774315"></a>2014 标准版 </p>
                <p id="p9345164712438"><a name="p9345164712438"></a><a name="p9345164712438"></a>2014 企业版 </p>
                </td>
                </tr>
                <tr id="row2345184711431"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p16345164774312"><a name="p16345164774312"></a><a name="p16345164774312"></a>2014 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p16345194764320"><a name="p16345194764320"></a><a name="p16345194764320"></a>2014 标准版 </p>
                <p id="p16345144734317"><a name="p16345144734317"></a><a name="p16345144734317"></a>2014 企业版 </p>
                </td>
                </tr>
                <tr id="row43461147204320"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p113461447164311"><a name="p113461447164311"></a><a name="p113461447164311"></a>2014 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1834694764314"><a name="p1834694764314"></a><a name="p1834694764314"></a>2014 企业版 </p>
                </td>
                </tr>
                <tr id="row134815473432"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p734614764311"><a name="p734614764311"></a><a name="p734614764311"></a>2016 web</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1734604744316"><a name="p1734604744316"></a><a name="p1734604744316"></a>2016 web</p>
                <p id="p7348194711431"><a name="p7348194711431"></a><a name="p7348194711431"></a>2016 标准版 </p>
                <p id="p1348144774310"><a name="p1348144774310"></a><a name="p1348144774310"></a>2016 企业版 </p>
                </td>
                </tr>
                <tr id="row63488477431"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p33481476434"><a name="p33481476434"></a><a name="p33481476434"></a>2016 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9348247124317"><a name="p9348247124317"></a><a name="p9348247124317"></a>2016 标准版</p>
                <p id="p334864711431"><a name="p334864711431"></a><a name="p334864711431"></a>2016 企业版 </p>
                </td>
                </tr>
                <tr id="row11348204794311"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p7348154712436"><a name="p7348154712436"></a><a name="p7348154712436"></a>2016 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6348847104312"><a name="p6348847104312"></a><a name="p6348847104312"></a>2016 企业版 </p>
                </td>
                </tr>
                <tr id="row209547378422"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p18889162813310"><a name="p18889162813310"></a><a name="p18889162813310"></a>2017 web版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p68891228163319"><a name="p68891228163319"></a><a name="p68891228163319"></a>2017 web版</p>
                <p id="p155693913812"><a name="p155693913812"></a><a name="p155693913812"></a>2017 标准版</p>
                <p id="p11353194711387"><a name="p11353194711387"></a><a name="p11353194711387"></a>2017 企业版</p>
                </td>
                </tr>
                <tr id="row1327135154212"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1216222683311"><a name="p1216222683311"></a><a name="p1216222683311"></a>2017 标准版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p46001805399"><a name="p46001805399"></a><a name="p46001805399"></a>2017 标准版</p>
                <p id="p8600120143917"><a name="p8600120143917"></a><a name="p8600120143917"></a>2017 企业版</p>
                </td>
                </tr>
                <tr id="row7349647154313"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p193491347194319"><a name="p193491347194319"></a><a name="p193491347194319"></a>2017 企业版</p>
                </td>
                <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1534920476435"><a name="p1534920476435"></a><a name="p1534920476435"></a>2017 企业版</p>
                </td>
                </tr>
                </tbody>
                </table>

            -   存储空间大小默认和原实例相同，且必须大于或等于原实例存储空间大小，数据库密码需重新设置。
            -   其他参数，用户需设置，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0053089697.html)。

        -   当前实例

            >![](public_sys-resources/icon-notice.gif) **须知：**   
            >-   若您已开启高危操作保护，在“身份验证”弹出框中单击“免费获取验证码“，正确输入验证码并单击“确定“，页面自动关闭。  
            >    通过进行二次认证再次确认您的身份，进一步提高帐号安全性，有效保护您安全使用云产品。关于如何开启操作保护，具体请参考《统一身份认证服务用户指南》的内容。  
            >-   如果备份所在的数据库实例已被删除，则不可恢复到当前实例。  
            >-   恢复到当前实例会导致当前实例的全部数据被覆盖，并且恢复过程中数据库不可用。  

        -   恢复到已有实例

            >![](public_sys-resources/icon-notice.gif) **须知：**   
            >-   若您已开启高危操作保护，在“身份验证”弹出框中单击“免费获取验证码“，正确输入验证码并单击“确定“，页面自动关闭。  
            >    通过进行二次认证再次确认您的身份，进一步提高帐号安全性，有效保护您安全使用云产品。关于如何开启操作保护，具体请参考《统一身份认证服务用户指南》的内容。  
            >-   恢复到已有实例会导致实例数据被覆盖，且恢复过程中实例将不可用。  
            >-   只可选择与原实例相同VPC，相同引擎，相同版本或高版本的实例。  
            >-   请确保目标实例的存储空间大于或等于当前实例的存储空间，否则会导致任务下发失败。  
            >-   如果原实例开启TDE，不允许恢复到已有实例。  

            选择目标实例，单击“下一步“。

    2.  勾选需要恢复的数据库，您可以根据需要，自定义恢复后的新数据库名。如果恢复到的新数据库名未填写，默认按原数据库名进行恢复。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >-   新数据库名不能与原数据库重名，重命名恢复之后，使用原库名建立的同义词不可用。  
        >-   新数据库名不能包含rdsadmin、master、msdb、tempdb、model或resource字段（不区分大小写）。  
        >-   数据库名称长度在1\~64个字符之间，包含字母、数字、下划线或中划线，不能包含其他特殊字符。  


6.  查看恢复结果。
    -   恢复到新实例

        RDS会为您重新创建一个和该备份数据相同的实例。可看到实例由“创建中“变为“正常“，说明恢复成功。

        恢复成功的新实例是一个独立的实例，与原有实例没有关联。

    -   恢复到当前实例

        在“实例管理”页面，可查看目标实例状态为“恢复中”，恢复完成后，实例状态由“恢复中”变为“正常”。如果目标实例下存在只读实例，只读实例的状态与目标实例一致。

        对于开启自动备份策略的实例，恢复成功后，会执行一次全量备份。 反之则不会执行全量备份。

    -   恢复到已有实例

        在“实例管理”页面，可查看该实例下所有实例状态为“恢复中”，恢复完成后，实例状态由“恢复中”变为“正常”。



