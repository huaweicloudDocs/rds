# 数据库安全设置<a name="zh-cn_topic_0045111183"></a>

## 密码复杂度要求<a name="section7110857165544"></a>

-   华为云关系型数据库服务Console端数据库密码复杂度，请参见[购买实例](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0046585384.html)中的数据库配置表格。
-   华为云关系型数据库实例数据库对在客户端新创建的数据库用户，设置了密码安全策略：
    -   密码最小长度为8个字符。
    -   密码中必须含有字母和非字母，其中，非字母包括数字和特殊字符。
    -   密码不得包含用户名。


## 创建用户建议<a name="section20152425171620"></a>

用户在使用CREATE USER或CREATE ROLE命令时，建议指定VALID UNTIL 'timestamp' 参数（timestamp为过期时间戳），设置用户密码的过期时间。

## 访问数据库对象建议<a name="section1874185013263"></a>

用户在访问数据库对象时，建议指定数据库对象的schema名，以防止特定场景下的“[特洛伊木马](https://wiki.postgresql.org/wiki/A_Guide_to_CVE-2018-1058%3A_Protect_Your_Search_Path)”攻击。

## 帐户说明<a name="section3063981715951"></a>

您在创建PostgreSQL数据库实例时，系统会自动为实例创建如下系统帐户（用户不可使用），用于给数据库实例提供完善的后台运维管理服务。

>![](public_sys-resources/icon-notice.gif) **须知：**   
>如果试图删掉、重命名、修改这些帐户的密码和权限，会导致出错，请谨慎操作。  

-   rdsAdmin：管理帐户，拥有最高的superuser权限，用于查询和修改实例信息、故障排查、迁移、恢复等操作。
-   rdsRepl：复制帐户，用于备实例或只读实例在主实例上同步数据。
-   rdsBackup：备份帐户，用于后台的备份。
-   rdsMetric：指标监控帐户，用于watchdog采集数据库状态数据。

