# 设置SQL Server默认语言<a name="rds_11_0005"></a>

## 操作背景<a name="section220211518283"></a>

“default language“参数指定登录的默认语言，每种语言对应一个“langid“值，您可通过查询“sys.syslanguages“兼容性视图来获取“langid“的值。有关sys.syslanguages \(Transact-SQL\)介绍，请参见官方文档[sys.syslanguages \(Transact-SQL\)](https://docs.microsoft.com/zh-cn/sql/relational-databases/system-compatibility-views/sys-syslanguages-transact-sql?view=sql-server-2017)。

更多介绍请参见官方文档[配置默认语言服务器配置选项](https://docs.microsoft.com/zh-cn/sql/database-engine/configure-windows/configure-the-default-language-server-configuration-option?view=sql-server-2017)。

RDS for SQL Server支持修改默认语言，您可以根据业务需求修改创建的数据库参数模板中的“default language“参数值，来设置SQL Server默认语言。

## 实例参数修改<a name="section138813101315"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“实例管理“页面，选择指定的实例，单击实例名称，进入实例的基本信息页面。
5.  在左侧导航栏中选择“参数修改“，在“参数“页签搜索框中输入“default language“进行搜索。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   “default language“选项。使用“default language“选项为所有新创建的登录指定默认语言。  
    >-   “default language“参数默认的设置是“0”，表示默认语言为“英文”。  

6.  设置“default language“参数值。

    将参数值设置为“30”，单击“保存“，在弹出框中单击“是“保存本次修改，设置SQL Server默认语言为“简体中文”。

7.  修改完成后可以在“参数修改历史“页签下查看“default language“  参数已经修改成功。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >SQL Server默认语言修改成功后，参数设置立即生效，无需重启实例。  


## 自定义参数模板参数修改<a name="section206907435218"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“参数模板管理“页面的“自定义“页签，选择目标参数模板，单击参数模板名称。
5.  在“参数“页签搜索框中输入“default language“进行搜索。
6.  设置“default language“参数值。

    将参数值设置为“30”，单击“保存“，在弹出框中单击“是“保存本次修改，设置SQL Server默认语言为“简体中文”。

7.  修改完成后可以在“参数修改历史“页签下查看“default language“  参数已经修改成功。
8.  如果需要应用到实例的参数模板为用户自己创建的参数模板时，在“自定义“页签的目标参数模板单击“更多\>应用”。
9.  在弹出框中，选择或输入所需应用的实例，单击“确定”。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   一个参数模板可被应用到一个或多个实例。  
    >-   对于某些参数模板重置后，您需在实例列表中，查看状态，如果显示“参数模板变更，等待重启“，则需重启关联的实例使之生效。  
    >-   修改主实例的某些参数（如果是主备实例，备实例的参数也会被同步修改），需重启主实例使之生效。  
    >-   修改只读实例的某些参数，需要重启该只读实例使之生效。  

10. 参数模板应用成功后，您可以在“参数模板管理“页面的“自定义“页签，选择目标参数模板，单击“更多\>应用记录”。

