# MySQL参数修改注意事项<a name="rds_08_00001"></a>

数据库参数是数据库系统运行的关键配置信息，设置不合适的参数值可能会影响业务。本文列举了一些重要参数说明，更多参数详细说明，请参见**[MySQL官网](http://dev.mysql.com/doc/refman/5.6/en/server-system-variables.html)**。

## 修改敏感参数<a name="section37541120104511"></a>

若干参数相关说明如下：

-   “lower\_case\_table\_names“

    **云数据库默认值**：“1“。

    **作用**：该参数表示创建数据库及表时，表存储是否大小写敏感。设置为默认值“1“，表示创建数据库及表时，默认小写，不区分大小写，设置为“0“时，则存储与查询均区分大小写。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >8.0版本不支持修改该参数。  

    **影响：**修改数据库主实例默认参数值时，用户需要手动同步修改只读实例、灾备实例、通过备份恢复至目标实例的参数。当主实例区分大小写，而只读实例、灾备实例、通过备份恢复至目标实例不区分大小写时，比如主实例先后创建两张表，表名分别为  “abc“、“Abc “时，会导致数据同步、数据恢复异常，原因为“abc“表名已存在。

-   “innodb\_flush\_log\_at\_trx\_commit“

    **云数据库默认值：**“1“。

    **作用**：该参数控制提交操作在严格遵守ACID合规性和高性能之间的平衡。设置为默认值“1“，是为了保证完整的ACID，每次提交事务时，把事务日志从缓存区写到日志文件中，并刷新日志文件的数据到磁盘上；当设为“0“时，每秒把事务日志缓存区的数据写入日志文件，并刷新到磁盘；如果设为“2“，每次提交事务都会把事务日志从缓存区写入日志文件，每隔一秒左右会刷新到磁盘。

    **影响**：参数设置为非默认值“1“时，降低了数据安全性，在系统崩溃的情况下，可能导致数据丢失。

-   “sync\_binlog“

    **云数据库默认值**：“1“。

    **作用**：该参数控制MySQL服务器将二进制日志同步到磁盘的频率。设置为默认值“1“，表示MySQL每次事务提交，binlog同步写入磁盘，是最安全的设置；设置为“0“时，表示MySQL不控制binlog的刷新，由文件系统自己控制其缓存的刷新。此时的性能最好，但风险最大，因为一旦断电或操作系统崩溃，在“binlog\_cache“中的所有binlog信息都会被丢失。

    **影响**：参数设置为非默认值“1“时，降低了数据安全性，在系统崩溃的情况下，可能导致binlog丢失。


## 修改性能参数<a name="section5602829104512"></a>

若干参数相关说明如下：

-   “innodb\_spin\_wait\_delay“和“query\_alloc\_block\_size“依赖于实例的规格，设置过大时，可能会影响数据库的使用。
-   “key\_buffer\_size“参数值设置较小（小于4096），参数值将修改失败。
-   “max\_connections“参数值设置较小，将影响数据库访问。
-   “innodb\_buffer\_pool\_size“、“max\_connections“和“back\_log“参数依赖于实例的规格，实例规格不同对应其默认值也不同。因此，这些参数在用户未设置前显示为“default“。
-   “innodb\_io\_capacity\_max“、“innodb\_io\_capacity“参数依赖于磁盘类型，用户未设置前显示为“default“。

## 联动参数<a name="section79251840141810"></a>

-   “character\_set\_server“：修改该参数的值， 系统会联动调整“collation\_server“、“character\_set\_database“,和“collation\_database“的取值。

    其中，字符序“character\_set\_server“跟字符集“collation\_server“存在对应关系，比如针对MySQL 5.7而言，“character\_set\_server“为“latin1“时，对应的“collation\_server“默认值为“latin1\_swedish\_ci“，此时“collation\_server“的取值区间为以“latin1“开头的字符序。

-   “innodb\_io\_capacity“：该参数的取值必须小于等于“innodb\_io\_capacity\_max“的取值。 比如“innodb\_io\_capacity\_max“为“2000“， 则“innodb\_io\_capacity“最大设置为“2000“。
-   “innodb\_buffer\_pool\_size“： 该参数受“innodb\_buffer\_pool\_chunk\_size “\*  “innodb\_buffer\_pool\_instances“的影响，为两参数乘积的整数倍向上取值。 比如“innodb\_buffer\_pool\_chunk\_size“为“134217728“，“ innodb\_buffer\_pool\_instances“为“1“，那“innodb\_buffer\_pool\_size“必须大于等于“134217728“。

## 其他参数<a name="section1829410587914"></a>

-   “max\_prepared\_stmt\_count“：准备大量的语句会消耗服务器的内存资源，参数设置较小，会带来潜在的“拒绝服务”的风险，建议您根据业务情况，调整该参数的值。
-   如下参数的输入会根据内核规则对取值进行对应的调整。调整的规则如下所示：
    -   “key\_cache\_age\_threshold“会自动调整为100的倍数。
    -   “join\_buffer\_size“和“key\_cache\_block\_size“会自动调整为128的倍数。
    -   “query\_cache\_size“、“query\_prealloc\_size“、“innodb\_log\_buffer\_size“和“max\_allowed\_packet “、“thread\_stack “会自动调整为1024的倍数。
    -   “read\_buffer\_size“、“read\_rnd\_buffer\_size“、“binlog\_cache\_size “、“binlog\_stmt\_cache\_size “会自动调整为4096的倍数。
    -   “data\_buffer\_size“、“log\_buffer\_size“、“shared\_pool\_size“、“temp\_buffer\_size “会自动调整为1048576的倍数。


