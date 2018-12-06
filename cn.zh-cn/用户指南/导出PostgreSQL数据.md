# 导出数据<a name="TOPIC_0142028617"></a>

要将已有的PostgreSQL数据库迁移到华为云关系型数据库，需要先对它进行导出。

>![](public_sys-resources/icon-notice.gif) **注意：**   
>-   相应导出工具需要与数据库引擎版本匹配。  
>-   数据库迁移为离线迁移，您需要停止使用源数据库的应用程序。  

## 操作步骤<a name="section25586269104740"></a>

1.  登录[PostgreSQL迁移准备](PostgreSQL迁移准备.md)的[1](迁移准备-2.md#li61751156194257)中准备的弹性云服务器，或可访问华为云关系型数据库的设备。
2.  使用pg\_dump将源数据库导出至SQL文件。

    **pg\_dump** **--username=**_<DB\_USER\>_**_ _--host=**_<DB\_ADDRESS\>_** --port=**_<DB\_PORT\> _**--format=plain --file=**_<BACKUP\_FILE\>_ _<DB\_NAME\>_

    -   DB\_USER为数据库用户。
    -   DB\_ADDRESS为数据库地址。
    -   DB\_PORT为数据库端口。
    -   BACKUP\_FILE为要导出的文件名称。
    -   DB\_NAME为要迁移的数据库名称。

    根据命令提示输入数据库密码。

    示例如下：

    **\[rds@localhost ~\]$ pg\_dump --username=root --host=192.168.151.18 --port=**5432**  --format=plain --file=backup.sql my\_db**

    **Password for user root:**

    命令执行完会生成“backup.sql”文件，如下：

    \[rds@localhost ~\]$ ll backup.sql

    ```
    -rw-r-----. 1 rds rds 2714 Sep 21 08:23 backup.sql
    ```


