# 导入数据<a name="TOPIC_0142028465"></a>

通过弹性云服务器或可访问华为云关系型数据库的设备，用相应客户端连接华为云关系型数据库实例，将导出的SQL文件导入到华为云关系型数据库。

>![](public_sys-resources/icon-notice.gif) **注意：**   
>如果源数据库中包含触发器、存储过程、函数或事件调用，则需确保导入前设置目标数据库参数log\_bin\_trust\_function\_creators=ON。  

## 操作步骤<a name="sc8ce0df9edf34e0dbe1320e28a53cd7c"></a>

1.  导入元数据到华为云关系型数据库。

    先用mysql工具连接华为云关系型数据库实例，输入密码后，再执行导入命令。

    \#  **mysql -f -h** _<RDS\_ADDRESS\>_ **-P** <_DB\_PORT_\> **-u** root **-p < **_<BACKUP\_DIR\>_**/dump-defs.sql**

    -   RDS\_ADDRESS为华为云关系型数据库实例的IP地址。
    -   DB\_PORT为当前数据库实例的端口。
    -   BACKUP\_DIR为“dump-defs.sql”所在目录。

    示例如下：

    **\[root@ecs-zyc-0815-2 ~\]\# mysql -f -h 172.16.66.198 -P 3306 -u root -p < dump-defs.sql**

    **Enter password:**

2.  导入数据到华为云关系型数据库。

    \#  **mysql -f -h** _<RDS\_ADDRESS\>_ **-P** <_DB\_PORT_\> **-u** root **-p** **< **_<BACKUP\_DIR\>_**/dump-data.sql**

    -   RDS\_ADDRESS为华为云关系型数据库实例的IP地址。
    -   DB\_PORT为当前数据库实例的端口。
    -   BACKUP\_DIR为“dump-data.sql”所在目录。

    示例如下：

    **\[root@ecs-zyc-0815-2 ~\]\# mysql -f -h 172.16.66.198 -P 3306 -u root -p < dump-data.sql**

    **Enter password:**

3.  查看迁移结果。

    **mysql\> show databases;**

    示例中，名为my\_db的数据库已经被导入了：

    ```
    mysql> show databases;
    +--------------------+
    | Database           |
    +--------------------+
    | information_schema |
    | my_db              |
    | mysql              |
    | performance_schema |
    +--------------------+
    4 rows in set (0.00 sec)
    ```


