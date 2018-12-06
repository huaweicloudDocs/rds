# 编辑参数<a name="TOPIC_0142028463"></a>

为确保华为云关系型数据库服务发挥出最优性能，用户可根据业务需求对用户创建的参数组里边的参数进行调整。

## 批量修改<a name="s58aa43af74584cb4a56cb9ed879e5778"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“参数组管理“页面，在“自定义“页签选择目标参数组，单击参数组名称。
5.  根据需要修改相关参数值。

    **参数相关说明如下：**

    -   各参数的详细说明请参见[MySQL官网](http://dev.mysql.com/doc/refman/5.6/en/server-system-variables.html)。
    -   innodb\_spin\_wait\_delay和query\_alloc\_block\_size依赖于实例的规格，设置过大时，可能会导致数据库的使用受到影响。
    -   key\_buffer\_size参数值设置较小（小于4096），参数值修改将失败。

        max\_connections参数值设置较小，将影响数据库访问。

    -   innodb\_buffer\_pool\_size、max\_connections和back\_log参数依赖于实例的规格，实例规格不同对应其默认值也不同。因此，这些参数在用户未设置前显示为“default“。

        innodb\_io\_capacity\_max、innodb\_io\_capacity参数依赖于磁盘类型，用户未设置前显示为“default“。


    **可进行的操作如下：**

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >参数组修改后，不会立即应用到当前使用的实例，您需要进行应用操作才可生效，具体操作请参见[应用参数组](应用参数组.md)。  

    -   单击“保存”，在弹出框中单击“确定”，保存修改。
    -   单击“取消”，放弃本次设置。
    -   单击“预览”，可对比参数修改前和修改后的值。

    参数修改完成后，您可单击“参数修改历史“查看参数的修改详情。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >有关参数组状态，请参见[状态](https://support.huaweicloud.com/productdesc-rds/zh-cn_topic_0032472291.html)中的参数组状态内容。  
    >对于某些运行参数修改，您需在实例列表中，选择对应的实例，单击实例名称，在“基本信息”页签中查看参数组状态，如果显示“等待重启“，则需重启关联的实例使之生效。  
    >-   修改主实例的某些参数（如果是主备实例，备实例的参数也会被同步修改），需重启主实例使之生效。  
    >-   修改只读实例的某些参数，需要重启该只读实例使之生效。  


## 修改当前实例的参数组<a name="section8672172212597"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“实例管理“页面，选择指定的实例，单击实例名称。
5.  在“参数修改“页签，修改相应参数。

    **参数相关说明如下：**

    -   各参数的详细说明请参见[MySQL官网](http://dev.mysql.com/doc/refman/5.6/en/server-system-variables.html)。
    -   key\_buffer\_size参数值设置较小（小于4096），参数值修改将失败。

        max\_connections参数值设置较小，将影响数据库访问。

    -   
    **可进行的操作如下：**

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >参数组修改后，会立即应用到当前实例。  
    >有关参数组状态，请参见[状态](https://support.huaweicloud.com/productdesc-rds/zh-cn_topic_0032472291.html)中的参数组状态内容。  
    >根据参数列表中“是否需要重启“提示，进行相应操作：  
    >-   是：在实例列表中，查看“运行状态“，如果显示“参数组变更，等待重启“，则需重启实例使之生效。  
    >-   否：无需重启，立即生效。  

    -   单击“保存”，在弹出框中单击“确定”，保存修改。
    -   单击“取消”，放弃本次设置。
    -   单击“预览”，可对比参数修改前和修改后的值。

    参数修改完成后，您可单击“参数修改历史“查看参数的修改详情。


