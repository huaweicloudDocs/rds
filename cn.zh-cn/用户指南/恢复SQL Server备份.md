# 恢复备份<a name="TOPIC_0142028312"></a>

## 操作场景<a name="section51567119122258"></a>

华为云关系型数据库支持使用已有的自动和手动备份恢复实例数据，可恢复到备份被创建时的状态。

账户余额大于等于0元，才可恢复到新实例。

## 操作步骤<a name="section51247315503"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“备份管理”页面，选择需要恢复的备份，单击“恢复“。

    根据该手动备份所在实例是否存在，进行操作：

    -   存在，继续[5](#li74461528135319)。
    -   不存在，则不可恢复到当前实例，需跳过[5](#li74461528135319)，执行[6](#li12452192818531)。

5.  <a name="li74461528135319"></a>选择需要的恢复方式，单击“确定”。

    -   新实例

        跳转到“恢复到新实例”的服务选型页面，为用户重新创建一个和该备份数据相同的实例。恢复成功的新实例是一个独立的实例，与原有实例没有关联。如果需要使用只读实例，请重新创建。

        -   数据库引擎与原实例相同，数据库端口默认为1433，以上参数皆不可重置。
        -   数据库版本支持从低版本恢复到高版本，详见[表1](#tce62e50f07a144febaabc0d35c49238e)。

            **表 1**  恢复支持的版本规则

            <a name="tce62e50f07a144febaabc0d35c49238e"></a>
            <table><thead align="left"><tr id="ra3da2b955520453a8e1736ef8774e592"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="af33f67f083394780b4c6b0179b8967c8"><a name="af33f67f083394780b4c6b0179b8967c8"></a><a name="af33f67f083394780b4c6b0179b8967c8"></a>原数据库版本</p>
            </th>
            <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0086557163_p148277267543"><a name="zh-cn_topic_0086557163_p148277267543"></a><a name="zh-cn_topic_0086557163_p148277267543"></a>可恢复到的版本</p>
            </th>
            </tr>
            </thead>
            <tbody><tr id="re00d17ab3dbe4ad7b7d92b9e65882753"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="afb5a9a2e56254c55862284e708068e0f"><a name="afb5a9a2e56254c55862284e708068e0f"></a><a name="afb5a9a2e56254c55862284e708068e0f"></a>2008 R2 WEB</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0086557163_p151700575920"><a name="zh-cn_topic_0086557163_p151700575920"></a><a name="zh-cn_topic_0086557163_p151700575920"></a>2008 R2 WEB</p>
            <p id="ad9c216b9a6c54bf984224e9960f13fb3"><a name="ad9c216b9a6c54bf984224e9960f13fb3"></a><a name="ad9c216b9a6c54bf984224e9960f13fb3"></a>2008 R2企业版 </p>
            </td>
            </tr>
            <tr id="r557859ffa28c49b18ef7af7b422b743b"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0086557163_p99214617595"><a name="zh-cn_topic_0086557163_p99214617595"></a><a name="zh-cn_topic_0086557163_p99214617595"></a>2008 R2企业版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="ac6ecb0c607ad483f85d97fc225e61f3e"><a name="ac6ecb0c607ad483f85d97fc225e61f3e"></a><a name="ac6ecb0c607ad483f85d97fc225e61f3e"></a>2008 R2企业版 </p>
            </td>
            </tr>
            <tr id="r582e42dcedd0483192be9ac4712a313b"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="acda7428929264346af4abd4f1c6f60b1"><a name="acda7428929264346af4abd4f1c6f60b1"></a><a name="acda7428929264346af4abd4f1c6f60b1"></a>2014 WEB</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="a9ec8c147ff2647428f6dcc0ab2165256"><a name="a9ec8c147ff2647428f6dcc0ab2165256"></a><a name="a9ec8c147ff2647428f6dcc0ab2165256"></a>2014 WEB</p>
            <p id="a83caba3d8fde4eaeb04b83c8c33343ee"><a name="a83caba3d8fde4eaeb04b83c8c33343ee"></a><a name="a83caba3d8fde4eaeb04b83c8c33343ee"></a>2014标准版 </p>
            <p id="zh-cn_topic_0086557163_p49810551116"><a name="zh-cn_topic_0086557163_p49810551116"></a><a name="zh-cn_topic_0086557163_p49810551116"></a>2014企业版 </p>
            </td>
            </tr>
            <tr id="rfac7f06e596a464c8694cfb51003ec8f"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0086557163_p3524791705"><a name="zh-cn_topic_0086557163_p3524791705"></a><a name="zh-cn_topic_0086557163_p3524791705"></a>2014标准版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0086557163_p04601614604"><a name="zh-cn_topic_0086557163_p04601614604"></a><a name="zh-cn_topic_0086557163_p04601614604"></a>2014标准版 </p>
            <p id="a2c7a47d4d2f4462f8406f3bf5da7ad0c"><a name="a2c7a47d4d2f4462f8406f3bf5da7ad0c"></a><a name="a2c7a47d4d2f4462f8406f3bf5da7ad0c"></a>2014企业版 </p>
            </td>
            </tr>
            <tr id="r3d5faa13e81b48769cc1791062e6daf0"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="a0eb9e6f56ec64060b3f314f6032d0d20"><a name="a0eb9e6f56ec64060b3f314f6032d0d20"></a><a name="a0eb9e6f56ec64060b3f314f6032d0d20"></a>2014企业版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0086557163_p186343201806"><a name="zh-cn_topic_0086557163_p186343201806"></a><a name="zh-cn_topic_0086557163_p186343201806"></a>2014企业版 </p>
            </td>
            </tr>
            <tr id="r606febfa89a84d3aafce1137209ee0c8"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="ae2dd9531409644a0ba3da3a17619908c"><a name="ae2dd9531409644a0ba3da3a17619908c"></a><a name="ae2dd9531409644a0ba3da3a17619908c"></a>2016 WEB</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="aa4b3b9a1a3bc4421adbc3fd8ce7bf60d"><a name="aa4b3b9a1a3bc4421adbc3fd8ce7bf60d"></a><a name="aa4b3b9a1a3bc4421adbc3fd8ce7bf60d"></a>2016 WEB</p>
            <p id="zh-cn_topic_0086557163_p59246291304"><a name="zh-cn_topic_0086557163_p59246291304"></a><a name="zh-cn_topic_0086557163_p59246291304"></a>2016标准版 </p>
            <p id="a6c209bf0343a48699e4a402da614ff7f"><a name="a6c209bf0343a48699e4a402da614ff7f"></a><a name="a6c209bf0343a48699e4a402da614ff7f"></a>2016企业版 </p>
            </td>
            </tr>
            <tr id="r3579cab8a55d4294a106d20fef531c26"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="a4cd26f8984f64954b015af61a82ef6e1"><a name="a4cd26f8984f64954b015af61a82ef6e1"></a><a name="a4cd26f8984f64954b015af61a82ef6e1"></a>2016标准版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0086557163_p06405436014"><a name="zh-cn_topic_0086557163_p06405436014"></a><a name="zh-cn_topic_0086557163_p06405436014"></a>2016标准版</p>
            <p id="a35e48f4b2524406fa0a69dfa8d37c735"><a name="a35e48f4b2524406fa0a69dfa8d37c735"></a><a name="a35e48f4b2524406fa0a69dfa8d37c735"></a>2016企业版 </p>
            </td>
            </tr>
            <tr id="r4012e6bbad9445ff9b5ee178b76863eb"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="a7996632c1cb3490aa2d45af83e6f71e0"><a name="a7996632c1cb3490aa2d45af83e6f71e0"></a><a name="a7996632c1cb3490aa2d45af83e6f71e0"></a>2016企业版</p>
            </td>
            <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0086557163_p77341511808"><a name="zh-cn_topic_0086557163_p77341511808"></a><a name="zh-cn_topic_0086557163_p77341511808"></a>2016企业版 </p>
            </td>
            </tr>
            </tbody>
            </table>

        -   其他参数，用户需设置，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0053089697.md)。
        -   新实例创建成功后，系统会自动执行一次全量备份。

    -   当前实例

        >![](public_sys-resources/icon-notice.gif) **注意：**   
        >恢复到当前实例会导致实例数据被覆盖，且恢复过程中实例将不可用。  

        在“实例管理”页面，可查看该实例状态为“恢复中”。无需执行[6](#li12452192818531)。


    恢复成功后，若当前实例已开启自动备份策略，系统会自动执行一次全量备份。反之则不会执行全量备份。

6.  <a name="li12452192818531"></a>恢复到新实例。

    跳转到“恢复到新实例”的服务选型页面，为用户重新创建一个和该备份数据相同的实例。恢复成功的新实例是一个独立的实例，与原有实例没有关联。如果需要使用只读实例，请在新实例上重新创建。

    -   数据库引擎和数据库版本，与原实例相同，数据库端口默认为1433，以上参数皆不可重置。
    -   其他参数，用户需设置，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0053089697.md)。

    新实例创建成功后，系统会自动执行一次全量备份。


