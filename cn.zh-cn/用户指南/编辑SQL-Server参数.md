# 编辑参数<a name="zh-cn_topic_0053089721"></a>

为确保华为云关系型数据库服务发挥出最优性能，用户可根据业务需求对用户创建的参数组里边的参数进行调整。

>![](public_sys-resources/icon-note.gif) **说明：**   
>系统提供的默认参数组不允许修改，只可单击参数组名进行查看。当用户参数设置不合理导致数据库无法启动时，可参考默认参数组重新配置。  

## 批量修改<a name="s58aa43af74584cb4a56cb9ed879e5778"></a>

1.  [登录云数据库](https://support.huaweicloud.com/qs-rds/rds_login.html)。
2.  在“参数组管理“页面，选择需要编辑的自定义参数组，单击参数组名称。
3.  根据需要修改相关参数。

    **相关参数组说明如下：**

    -   各参数的详细说明请参见[Microsoft SQL Server官网](https://msdn.microsoft.com/zh-cn/library/ms189631.aspx)。
    -   参数remote access，将此选项设置为0（默认值）表示阻止本地存储过程在远程服务器上执行，或远程存储过程在本地服务器上执行。
    -   参数max server memory \(MB\)，服务器内存选项。max server memory的默认值\(MB\)=操作系统内存\(MB\)-520\(MB\)。可为它指定的最小值为16MB。

    **可进行的操作如下：**

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >参数组修改后，不会立即应用到当前使用的实例，您需要进行应用操作才可生效，具体操作请参见[应用参数组](应用参数组.md)。  

    -   单击“保存”，在弹出框中单击“确定”，保存修改。
    -   单击“取消”，放弃本次设置。
    -   单击“预览”，可对比参数修改前和修改后的值。

    参数修改完成后，您可在“参数组管理“页面单击目标参数组名称，然后在左侧导航栏中，单击“参数修改历史“查看参数的修改详情。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >有关参数组状态，请参见[状态](https://support.huaweicloud.com/productdesc-rds/zh-cn_topic_0032472291.html)中的参数组状态内容。  


## 修改当前实例的参数组<a name="section192395951913"></a>

1.  [登录云数据库](https://support.huaweicloud.com/qs-rds/rds_login.html)。
2.  在“实例管理“页面，选择指定的实例，单击实例名称。
3.  在左侧导航栏中选择“参数修改“，在“参数组“页签修改相应参数。

    **参数相关说明如下：**

    -   各参数的详细说明请参见[Microsoft SQL Server官网](https://msdn.microsoft.com/zh-cn/library/ms189631.aspx)。
    -   参数remote access，将此选项设置为0（默认值）表示阻止本地存储过程在远程服务器上执行，或远程存储过程在本地服务器上执行。
    -   参数max server memory \(MB\)，服务器内存选项。max server memory的默认值\(MB\)=操作系统内存\(MB\)-520\(MB\)。可为它指定的最小值为16MB。

    **可进行的操作如下：**

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >参数组修改后，会立即应用到当前实例。  
    >有关参数组状态，请参见[状态](https://support.huaweicloud.com/productdesc-rds/zh-cn_topic_0032472291.html)中的参数组状态内容。  
    >对于某些参数修改后，您需在实例列表中，查看状态，如果显示“参数组变更，等待重启“，则需重启实例使之生效。  
    >-   修改主实例的某些参数（如果是主备实例，备实例的参数也会被同步修改），需重启主实例使之生效。  
    >-   修改只读实例的某些参数，需要重启该只读实例使之生效。  

    -   单击“保存”，在弹出框中单击“确定”，保存修改。
    -   单击“取消”，放弃本次设置。
    -   单击“预览”，可对比参数修改前和修改后的值。

    参数修改完成后，您可在“参数修改“页面，选择“参数修改历史“页签查看参数的修改详情。


