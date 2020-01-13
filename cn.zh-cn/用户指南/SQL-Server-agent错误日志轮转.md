# SQL Server agent错误日志轮转<a name="rds_09_0011"></a>

## 操作场景<a name="section3887921161312"></a>

使用存储过程关闭当前的SQL Server代理错误日志文件，并循环SQL Server代理错误日志扩展编号（就像重新启动服务器）。 新的 SQL Server 代理错误日志包含一个表示已创建新日志的行。

## 前提条件<a name="section167991936101313"></a>

成功连接RDS for SQL Server实例。通过SQL Server客户端连接目标实例，具体操作请参见[通过公网连接SQL Server实例](https://support.huaweicloud.com/qs-rds/rds_03_0007.html)。

## 操作步骤<a name="section16873185113134"></a>

执行以下命令，循环SQL Server代理错误日志。

**EXEC \[msdb\].\[dbo\].\[rds\_cycle\_agent\_errorlog\]**

执行成功后，系统将会如下提示：

```
HW_RDS_Process_Successful_Completed
```

