# 导入数据<a name="TOPIC_0142028482"></a>

通过弹性云服务器或可访问华为云关系型数据库的设备，用相应客户端连接华为云关系型数据库实例，将导出的SQL文件导入到华为云关系型数据库。

## 操作步骤<a name="section23456595105438"></a>

1.  确保导入的目标数据库已存在。

    如果不存在，执行以下命令创建数据库：

    **\# psql --host=**_<RDS\_ADDRESS\>_ **--port=**<_DB\_PORT_\> **--username=**_root_ **--dbname=postgres** **-c "create database** _<DB\_NAME\>_;"

    -   RDS\_ADDRESS为RDS实例的IP地址。
    -   DB\_PORT为当前数据库实例的端口。
    -   DB\_NAME为要导入的数据库名称。

2.  将导出的文件导入到华为云关系型数据库。

    **\# psql --host=**_<RDS\_ADDRESS\>_** --port=**<_DB\_PORT_\> **--username=**_root_ **--dbname=**_<DB\_NAME\>_ **--file=**_<BACKUP\_DIR\>_/backup.sql

    -   RDS\_ADDRESS为华为云关系型数据库实例的IP地址。
    -   DB\_PORT为当前数据库实例的端口。
    -   DB\_NAME为要导入的目标数据库名称，请确保该数据库已存在。
    -   BACKUP\_DIR为“backup.sql”所在目录。

    根据命令提示输入华为云关系型数据库实例的密码。

    示例如下：

    **\# psql --host=172.16.66.198 --port=****5432****  --username=root --dbname=my\_db --file=backup.sql**

    **Password for user root:**

3.  查看迁移结果，如下。

    **my\_db=\> \\l my\_db**

    示例中，名为my\_db的数据库已经被导入了：

    ```
    my_db=> \l my_db
    List of databases
    Name  | Owner | Encoding | Collate     | Ctype       | Access privileges
    ------+-------+----------+-------------+-------------+-----------
    my_db | root  | UTF8     | en_US.UTF-8 | en_US.UTF-8 | 
    (1 row)
    ```


