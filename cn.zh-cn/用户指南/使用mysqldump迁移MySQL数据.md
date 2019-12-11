# 使用mysqldump迁移MySQL数据<a name="zh-cn_topic_migration_mysql"></a>

## 迁移准备<a name="section8743122116813"></a>

华为云关系型数据库服务支持开启公网访问功能，通过弹性公网IP进行访问。您也可通过弹性云服务器的内网访问华为云关系型数据库。

1.  准备弹性云服务器或可通过公网访问华为云关系型数据库。
    -   通过弹性云服务器连接华为云关系型数据库实例，需要创建一台弹性云服务器。

        创建并连接弹性云服务器，请参见[如何创建和连接ECS](http://support.huaweicloud.com/rds_faq/rds_faq_0057.html)。

    -   通过公网地址连接华为云关系型数据库实例，需具备以下条件。
        1.  先对华为云关系型数据库实例绑定公网地址，如何绑定公网地址，请参见[绑定弹性公网IP](绑定和解绑弹性公网IP.md#section3199593620428)。
        2.  保证本地设备可以访问华为云关系型数据库实例绑定的公网地址。

2.  在准备的弹性云服务器或可访问华为云关系型数据库的设备上，安装MySQL客户端。

    请参见[如何安装MySQL客户端](http://support.huaweicloud.com/rds_faq/rds_faq_0027.html)。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >该弹性云服务器或可访问华为云关系型数据库的设备需要安装和RDS MySQL数据库服务端相同版本的数据库客户端，MySQL数据库或客户端会自带mysqldump和mysql工具。  


## 导出数据<a name="section692873015104"></a>

要将源数据库迁移到华为云关系型数据库，需要先对其进行导出。

>![](public_sys-resources/icon-notice.gif) **须知：**   
>-   相应导出工具需要与数据库引擎版本匹配。  
>-   数据库迁移为离线迁移，您需要停止使用源数据库的应用程序。  

1.  登录已准备的弹性云服务器，或可访问华为云关系型数据库的设备。
2.  <a name="li16251172911136"></a>使用mysqldump将元数据导出至SQL文件。

    >![](public_sys-resources/icon-notice.gif) **须知：**   
    >MySQL数据库是华为云关系型数据库服务管理所必须的数据库，导出元数据时，禁止指定**--all-database**参数，否则会造成数据库故障。  

    **mysqldump** **--databases** <_DB\_NAME_\> **--single-transaction --order-by-primary --hex-blob --no-data --routines --events --set-gtid-purged=OFF** -u <_DB\_USER_\> **-p -h** <_DB\_ADDRESS_\> **-P **<_DB\_PORT_\> **|sed -e 's/DEFINER\[ \]\*=\[ \]\*\[^\*\]\*\\\*/\\\*/' -e 's/DEFINER\[ \]\*=.\*FUNCTION/FUNCTION/' -e 's/DEFINER\[ \]\*=.\*PROCEDURE/PROCEDURE/' -e 's/DEFINER\[ \]\*=.\*TRIGGER/TRIGGER/' -e 's/DEFINER\[ \]\*=.\*EVENT/EVENT/' \>** _<BACKUP\_FILE\>_

    -   DB\_NAME为要迁移的数据库名称。
    -   DB\_USER为数据库用户。
    -   DB\_ADDRESS为数据库地址。
    -   DB\_PORT为数据库端口。
    -   BACKUP\_FILE为导出生成的文件名称_。_

    根据命令提示输入数据库密码。

    示例如下：

    **mysqldump --databases rdsdb --single-transaction --order-by-primary --hex-blob --no-data --routines --events --set-gtid-purged=OFF -u root -p -h 192.168.151.18 -P 3306 |sed -e 's/DEFINER\[ \]\*=\[ \]\*\[^\*\]\*\\\*/\\\*/' -e 's/DEFINER\[ \]\*=.\*FUNCTION/FUNCTION/' -e 's/DEFINER\[ \]\*=.\*PROCEDURE/PROCEDURE/' -e 's/DEFINER\[ \]\*=.\*TRIGGER/TRIGGER/' -e 's/DEFINER\[ \]\*=.\*EVENT/EVENT/' \> dump-defs.sql**

    **Enter password:**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >若使用的mysqldump低于5.6版本，需要去掉“--set-gtid-purged=OFF”。  

    命令执行完会生成“dump-defs.sql”文件，如下：

    ```
    [rds@localhost ~]$ ll dump-defs.sql
    -rw-r-----. 1 rds rds 2714 Sep 21 08:23 dump-defs.sql
    ```

3.  使用mysqldump将数据导出至SQL文件。

    >![](public_sys-resources/icon-notice.gif) **须知：**   
    >MySQL数据库是华为云关系型数据库服务管理所必须的数据库，导出元数据时，禁止指定**--all-database**参数，否则会造成数据库故障。  

    **mysqldump --databases** <_DB\_NAME_\> **--single-transaction --hex-blob --set-gtid-purged=OFF --no-create-info --skip-triggers** **-u** <_DB\_USER_\> **-p** **-h** <_DB\_ADDRESS_\> **-P** <_DB\_PORT_\> **-r** <_BACKUP\_FILE_\>

    以上命令的参数说明如[2](#li16251172911136)所示。

    根据命令提示输入数据库密码。

    示例如下：

    **mysqldump --databases rdsdb --single-transaction --hex-blob --set-gtid-purged=OFF --no-create-info --skip-triggers -u root -p -h 192.168.151.18 -P  **3306**  -r dump-data.sql**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >若使用的mysqldump低于5.6版本，需要去掉“--set-gtid-purged=OFF”。  

    命令执行完会生成“dump-data.sql”文件，如下：

    ```
    [rds@localhost ~]$ ll dump-data.sql
    -rw-r-----. 1 rds rds 2714 Sep 21 08:23 dump-data.sql
    ```


## 导入数据<a name="section9816229161211"></a>

通过弹性云服务器或可访问华为云关系型数据库的设备，用相应客户端连接华为云关系型数据库实例，将导出的SQL文件导入到华为云关系型数据库。

>![](public_sys-resources/icon-notice.gif) **须知：**   
>如果源数据库中包含触发器、存储过程、函数或事件调用，则需确保导入前设置目标数据库参数log\_bin\_trust\_function\_creators=ON。  

1.  导入元数据到华为云关系型数据库。

    先用mysql工具连接华为云关系型数据库实例，输入密码后，再执行导入命令。

    \#  **mysql -f -h** _<RDS\_ADDRESS\>_ **-P** <_DB\_PORT_\> **-u** root **-p < **_<BACKUP\_DIR\>_**/dump-defs.sql**

    -   RDS\_ADDRESS为华为云关系型数据库实例的IP地址。
    -   DB\_PORT为当前数据库实例的端口。
    -   BACKUP\_DIR为“dump-defs.sql”所在目录。

    示例如下：

    **\# mysql -f -h 172.16.66.198 -P 3306 -u root -p < dump-defs.sql**

    **Enter password:**

2.  导入数据到华为云关系型数据库。

    \#  **mysql -f -h** _<RDS\_ADDRESS\>_ **-P** <_DB\_PORT_\> **-u** root **-p** **< **_<BACKUP\_DIR\>_**/dump-data.sql**

    -   RDS\_ADDRESS为华为云关系型数据库实例的IP地址。
    -   DB\_PORT为当前数据库实例的端口。
    -   BACKUP\_DIR为“dump-data.sql”所在目录。

    示例如下：

    **\# mysql -f -h 172.16.66.198 -P 3306 -u root -p < dump-data.sql**

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


