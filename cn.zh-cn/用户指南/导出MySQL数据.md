# 导出数据<a name="TOPIC_0142028468"></a>

要将源数据库迁移到华为云关系型数据库，需要先对其进行导出。

>![](public_sys-resources/icon-notice.gif) **注意：**   
>-   相应导出工具需要与数据库引擎版本匹配。  
>-   数据库迁移为离线迁移，您需要停止使用源数据库的应用程序。  

## 操作步骤<a name="sd659c64912e04acc972cddbcd75924dd"></a>

1.  登录[MySQL迁移准备](MySQL迁移准备.md)的[1](迁移准备.md#l397559913ff346e6a360003eb2c81dbf)中准备的弹性云服务器，或可访问华为云关系型数据库的设备。
2.  <a name="lfeedfcaf45434d148cdf23d2b57303dd"></a>使用mysqldump将元数据导出至SQL文件。

    >![](public_sys-resources/icon-notice.gif) **注意：**   
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

    >![](public_sys-resources/icon-notice.gif) **注意：**   
    >MySQL数据库是华为云关系型数据库服务管理所必须的数据库，导出元数据时，禁止指定**--all-database**参数，否则会造成数据库故障。  

    **mysqldump --databases** <_DB\_NAME_\> **--single-transaction --hex-blob --set-gtid-purged=OFF --no-create-info --skip-triggers** **-u** <_DB\_USER_\> **-p** **-h** <_DB\_ADDRESS_\> **-P** <_DB\_PORT_\> **-r** <_BACKUP\_FILE_\>

    以上命令的参数说明如[2](#lfeedfcaf45434d148cdf23d2b57303dd)所示。

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


