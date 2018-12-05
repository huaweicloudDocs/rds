# 导入数据<a name="TOPIC_0142028213"></a>

通过弹性云服务器或可访问华为云关系型数据库的设备，用相应客户端连接华为云关系型数据库实例，将导出的SQL文件导入到华为云关系型数据库。

>![](public_sys-resources/icon-notice.gif) **注意：**   
>如果源数据库中包含全文索引信息，则在华为云关系型数据库上需要手动重建。  

## 操作步骤<a name="sdc50ea3392c942fcadd8fac0d7d89861"></a>

1.  使用sqlcmd将数据库对象定义导入。

    SQL Server数据库或客户端会自带该工具，命令如下：

    \>**sqlcmd -S** "_server_" **-d** _database_  **-U** _login\_id_ **-i** _inputfile_

    -   -S为RDS实例的IP地址和端口。
    -   -d为要导入的数据库名。
    -   -U为登录数据库的用户名。
    -   -i为要运行的SQL文件。

    根据命令提示输入数据库密码。

    示例如下：

    **\>sqlcmd -S "10.65.60.79,8636" -d test -U rdsuser -i C:\\test\\objects.sql**

    **Enter password:**

2.  使用bcp导入数据。

    \>**bcp** _dbname.schema\_name.table\_name_ **in** _C:\\test\\table\_name.txt_ **-n -S** _Server_ **-U** _username_ **-b** _2000_

    -   -in为将导入文件所在路径。
    -   -n使用数据的本机（数据库）数据类型执行大容量复制操作。
    -   -S为bcp工具连接Microsoft SQL Server实例的连接地址。
    -   -U为数据库用户名。
    -   -b为每批导入数据的行数。

    根据命令提示输入数据库密码。

    示例如下：

    **C:\\test\>bcp test.dbo.t1 in c:\\test\\t1.txt -n -S "10.65.60.79,8636" -U rdsuser -b 2000**

    **Enter password:**


