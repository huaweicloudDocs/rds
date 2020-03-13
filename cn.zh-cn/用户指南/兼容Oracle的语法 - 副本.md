# 兼容Oracle的语法<a name="rds_04_0008"></a>

本章节介绍了在PostgreSQL11开源版本的基础上，PostgreSQL增强版新增兼容Oracle  12c的语法。

-   支持ORACLE的CREATE SEQUENCE语法。
-   支持ORACLE的CREATE/ALTER DATABASE语法。
-   支持ORACLE的CREATE/ALTER VIEW语法。
-   支持ORACLE的CREATE TABLE语法。
-   支持ORACLE的CREATE TABLESPACE语法。
-   支持ORACLE的CLUSTER语法。
-   支持FORALL语法；
-   支持ORACLE的CREATE/DROP DIRECTORY语法。
-   支持ALTER TABLE ADD CONSTRAINT USING INDEX语法；
-   支持INSERT INTO语句的目标列名可以使用表名或表别名修饰。
-   支持非分区表的ROWNUM伪列；
-   支持字段表达式创建索引：CREATE INDEX ON COLUMN\_EXPR；
-   支持ALTER TABLE...MODIFY修改表字段。
-   支持VARCHAR、CHARACTER数据类型指定长度单位。
-   支持TYPE/NAME/VERSION/VALUE/INTERVAL作为别名。
-   支持ORACLE的存储过程语法。
-   支持ORACLE的DATE数据类型。
-   支持ORACLE的HASH、RANGE、LIST分区表创建语法。
-   支持MERGE操作语法：

    ```
    MERGE [HINT] INTO table_name USING ({subquery | table_name | view_name}) alias ON (condition) merge_update_clause merge_insert_clause;
    ```

-   支持时间间隔操作语法：

    ```
    INTERVAL YEAR TO MONTH,INTERVAL DAY (l) TO SECOND (P);
    ```

-   支持CREATE TRIGGER带BODY体语法：

    ```
    CREATE TRIGGER name... {DECLARE ... BEGIN | BEGIN} body END;
    ```

-   支持存储过程游标语法：

    ```
    CURSOR cursor_name [ parameter_list ] IS select_statement, TYPE type_name IS REF CURSOR;
    ```

-   支持存储过程游标变量：

    ```
    SQL%ISOPEN,SQL%FOUND,SQL%NOTFOUND,SQL%ROWCOUNT,cursor%ISOPEN,cursor%FOUND,cursor%NOTFOUND,cursor%ROWCOUNT;
    ```

-   支持定时任务高级包：

    ```
    DBMS_JOB.SUBMIT,DBMS_JOB.ISUBMIT,DBMS_JOB.REMOVE,DBMS_JOB.BROKEN,DBMS_JOB.CHANGE,DBMS_JOB.WHAT,DBMS_JOB.NEXT_DATE,DBMS_JOB.INTERVAL;
    ```

-   支持CREATE USER语法：

    ```
    {DEFAULT COLLATION | DEFAULT TABLESPACE | [LOCAL] TEMPORARY TABLESPACE} Clause;
    ```

-   支持修改会话属性：

    ```
    ALTER SESSION SET param_name = value;
    ```

-   支持匿名块。
-   支持存储过程跨模式访问。
-   存储过程支持SQLCODE内置变量；
-   存储过程语法兼容增强：支持以存储过程名作为结束标签，支持FOR VAR IN SELECT-CLAUSE，LOOP循环允许指定结束标签名，支持in参数指定默认值；
-   支持子查询不指定别名。
-   CREATE SEQUENCE支持NOCYCLE。
-   CREATE/ALTER USER语法中允许使用IDENTIFIED BY关键字替代PASSWORD关键字。
-   UPDATE SET语法中允许指定表名或别名修饰。
-   UPDATE SET支持单字段\(columnname\)=\(value\)语法。
-   ALTER TABLE兼容MODIFY NOT NULL语法和ENABLE语法。
-   空字符串和NULL等价。
-   序列操作新增语法：sequencCURRVAL，sequencNEXTVAL。
-   创建用户时支持同时创建同名schema。
-   删除表记录语法中FROM关键字。
-   支持XML数据类型伪列COLUMN\_VALUE。
-   支持外连接运算符（+）;
-   支持数据类型INTERVAL与数字之间的运算操作：+、-、\>、<、\>=、<=、<\>；
-   兼容分区表的DML操作：SELECT、INSERT、UPDATE、DELETE；
-   分区表支持二级分区；
-   分区表支持以表达式作为分区边界；
-   兼容触发器DDL：支持使用schema修饰等；
-   兼容时间格式IYY；
-   兼容CREATE/ALTER MATERIALIZED VIEW语法；
-   兼容CREATE TYPE语法；
-   兼容create profile语法；
-   兼容列约束的enable/disable语法；
-   兼容分区表指定tablespace options语法；
-   兼容DROP TABLE tablename \[CASCADE CONSTRAINTS\] \[PURGE\]语法；
-   兼容存储过程动态SQL语法EXECUTE IMMEDIATE，当前版本不支持带DECLARE申明的匿名块动态执行；
-   兼容FUNCTION定义；
-   支持CONNECT BY查询：支持伪列LEVEL、CONNECT\_BY\_ROOT、CONNECT\_BY\_ISLEAF；支持函数sys\_connect\_by\_path；支持CONNECT\_BY\_ROOT操作；支持ORDER SIBLINGS；
-   兼容TIME数据类型精度；
-   支持虚拟列:column\_name datatype \[GENERATED ALWAYS\] AS \(expression\) \[VIRTUAL\]；
-   兼容一维数组的定义：CREATE OR REPLACE TYPE array\_name AS VARRAY \(len\) OF typename；
-   兼容一维数组的访问：array\_name.extend, array\_name.count, array\_name.first, array\_name.last；
-   ROLLUP、CUBE、GROUPING SETS分组查询支持grouping\_id\(\[expr1\[, expr2\[, ...exprn\]\]\]\)和group\_id\(\)；
-   兼容无分组字段返回的排序查询语句：SELECT SUM\(colname\) FROM tbl ORDER BY colname；

