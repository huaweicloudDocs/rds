# 迁移准备<a name="TOPIC_0142028301"></a>

PostgreSQL支持逻辑备份。您可使用pg\_dump逻辑备份功能，导出备份文件，再通过psql导入到RDS中，实现将PostgreSQL的数据导入到华为云关系型数据库中。

华为云关系型数据库服务支持开启公网访问功能，通过EIP进行访问。您也可通过弹性云服务器的内网访问华为云关系型数据库。

## 准备工作<a name="section15764126154156"></a>

1.  <a name="li61751156194257"></a>准备弹性云服务器或可公网访问华为云关系型数据库。
    -   通过弹性云服务器连接华为云关系型数据库实例，需要创建一台弹性云服务器。

        创建并连接弹性云服务器，请参见[如何创建和连接ECS](http://support.huaweicloud.com/rds_faq/rds_faq_0057.html)。

    -   通过公网地址连接华为云关系型数据库实例，需具备以下条件。
        1.  先对华为云关系型数据库实例绑定公网地址，如何绑定公网地址，请参见[绑定弹性公网IP](绑定和解绑弹性公网IP.md#section3199593620428)。
        2.  保证本地设备可以访问华为云关系型数据库绑定的公网地址。


2.  在[1](#li61751156194257)中的弹性云服务器或可访问华为云关系型数据库的设备上，安装PostgreSQL客户端。

    请参见[如何安装PostgreSQL客户端](http://support.huaweicloud.com/rds_faq/rds_faq_0029.html)。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >该弹性云服务器或可访问华为云关系型数据库的设备上需要安装和RDS PostgreSQL数据库服务端相同版本的数据库客户端，PostgreSQL数据库或客户端会自带pg\_dump和psql工具。  


