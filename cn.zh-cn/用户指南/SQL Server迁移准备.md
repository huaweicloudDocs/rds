# 迁移准备<a name="TOPIC_0142028503"></a>

华为云关系型数据库服务支持开启公网访问功能，通过EIP进行访问。您也可通过弹性云服务器的内网访问华为云关系型数据库。

## 准备工作<a name="s32210f489e7e409686e0552214872d9c"></a>

1.  <a name="l6e46e3850fe34fbda0637de5f66614a6"></a>准备弹性云服务器或可公网访问华为云关系型数据库。
    -   通过弹性云服务器连接华为云关系型数据库实例，需要创建一台弹性云服务器。

        创建并连接弹性云服务器，请参见[如何创建和连接ECS](http://support.huaweicloud.com/rds_faq/rds_faq_0057.html)。

    -   通过公网地址连接华为云关系型数据库实例，需具备以下条件。
        1.  先对华为云关系型数据库实例绑定公网地址，如何绑定公网地址，请参见[绑定弹性公网IP](绑定和解绑弹性公网IP.md#section3199593620428)。
        2.  保证本地设备可以访问华为云关系型数据库绑定的公网地址。


2.  在[1](#l6e46e3850fe34fbda0637de5f66614a6)中的弹性云服务器或可访问华为云关系型数据库的设备上，安装Microsoft SQL Server客户端。

    请参见[如何安装SQL Server Management Studio](http://support.huaweicloud.com/rds_faq/rds_faq_0032.html)。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >请安装不低于SQL Server数据库版本的SQL Server Management Studio工具。  


