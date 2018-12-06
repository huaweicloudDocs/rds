# 导出数据<a name="TOPIC_0142028554"></a>

要将已有SQL Server数据库迁移到华为云关系型数据库，需要先对其进行导出。

>![](public_sys-resources/icon-notice.gif) **注意：**   
>-   相应导出工具需要与数据库引擎版本匹配。  
>-   数据库迁移为离线迁移，您需要停止使用源数据库的应用程序。  

## 操作步骤<a name="sd2fc4ea68dfe4afc8f241cd215249765"></a>

1.  登录[SQL-Server迁移准备](SQL-Server迁移准备.md)的[1](迁移准备-11.md#l6e46e3850fe34fbda0637de5f66614a6)中准备的弹性云服务器，或可访问华为云关系型数据库的设备。
2.  使用SQL Server Management Studio生成表、视图等数据库对象脚本。

    1.  使用SQL Server Management Studio连接数据库。
    2.  在“Object Explorer”中，展开Databases，打开源数据库的上下文，选择要导出的数据库，右键单击菜单，选择“Tasks”，单击“Generate Script”。此时将显示向导。
    3.  在“Choose Objects”页面选择要导出的对象的定义，单击“Next”。
    4.  在“Set Scripting Options”页面，选择“Save script to a specificel location”，在“File name”中选择导出文件放置的路径，单击“Next”。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >-   选择“Single file”将所有对象保存到一个文件中。  
        >-   选择“Single file per object”为每个对象保留到一个文件。  

    5.  单击“Next”。
    6.  单击“Finish”，完成导出。
    7.  使用“SQL Server Management Studio”打开导出的SQL文件。
    8.  修改文件中第一行USE \[DATABASE\]，把\[DATABASE\]修改为对应的数据库名称，然后保存。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >有关Generate Script，请参见微软官方文档[Generate and Publish Scripts Wizard](https://docs.microsoft.com/en-us/sql/relational-databases/scripting/generate-and-publish-scripts-wizard)。  

3.  使用bcp将源数据库的数据导出至TXT文件。

    **bcp **_dbname.schema\_name.table\_name_** out** _C:\\test\\table\_name.txt_ **-n** **-S** localhost **-U** _username_ **-b** _2000_

    -   -n使用数据的本机（数据库）数据类型执行大容量复制操作。
    -   -S为bcp工具连接Microsoft SQL Server实例的连接地址。
    -   -U为数据库用户名。
    -   -b为每批导入数据的行数。

    根据命令提示输入数据库密码。

    示例如下：

    **C:\\test\>bcp test.dbo.t1 out c:\\test\\t1.txt -n -S localhost -U rdsuser -b 2000**

    **Enter password:**

    命令执行完会生成“t1.txt”文件，如下：

    ```
    C:\test>$ dir t1.txt
    2017/03/27  11:51         22 t1.txt
    ```

    循环上面步骤导出数据库中其他表的数据。


