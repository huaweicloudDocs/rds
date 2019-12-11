# 使用psql命令迁移PostgreSQL数据<a name="zh-cn_topic_0029128106"></a>

## 迁移准备<a name="section182818561660"></a>

PostgreSQL支持逻辑备份。您可使用pg\_dump逻辑备份功能，导出备份文件，再通过psql导入到RDS中，实现将PostgreSQL的数据导入到华为云关系型数据库中。

华为云关系型数据库服务支持开启公网访问功能，通过弹性公网IP进行访问。您也可通过弹性云服务器的内网访问华为云关系型数据库。

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


## 导出数据<a name="section859519371476"></a>

要将已有的PostgreSQL数据库迁移到华为云关系型数据库，需要先对它进行导出。

>![](public_sys-resources/icon-notice.gif) **须知：**   
>-   相应导出工具需要与数据库引擎版本匹配。  
>-   数据库迁移为离线迁移，您需要停止使用源数据库的应用程序。  

1.  登录已准备的弹性云服务器，或可访问华为云关系型数据库的设备。
2.  使用pg\_dump将源数据库导出至SQL文件。

    **pg\_dump** **--username=**_<DB\_USER\>_**_ _--host=**_<DB\_ADDRESS\>_** --port=**_<DB\_PORT\> _**--format=plain --file=**_<BACKUP\_FILE\>_ _<DB\_NAME\>_

    -   DB\_USER为数据库用户。
    -   DB\_ADDRESS为数据库地址。
    -   DB\_PORT为数据库端口。
    -   BACKUP\_FILE为要导出的文件名称。
    -   DB\_NAME为要迁移的数据库名称。

    根据命令提示输入数据库密码。

    示例如下：

    **$ pg\_dump --username=root --host=192.168.151.18 --port=**5432**  --format=plain --file=backup.sql my\_db**

    **Password for user root:**

    命令执行完会生成“backup.sql”文件，如下：

    \[rds@localhost \~\]$ ll backup.sql

    ```
    -rw-r-----. 1 rds rds 2714 Sep 21 08:23 backup.sql
    ```


## 导入数据<a name="section113968181188"></a>

通过弹性云服务器或可访问华为云关系型数据库的设备，用相应客户端连接华为云关系型数据库实例，将导出的SQL文件导入到华为云关系型数据库。

1.  确保导入的目标数据库已存在。

    如果不存在，执行以下命令创建数据库：

    **\# psql --host=**_<RDS\_ADDRESS\>_ **--port=**<_DB\_PORT_\> **--username=**_root_ **--dbname=postgres** **-c **"**create database** _<DB\_NAME\>_;"

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


