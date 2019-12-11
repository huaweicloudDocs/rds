# 兼容Oracle的隐式类型转换<a name="rds_04_0005"></a>

本章节介绍了在PostgreSQL11开源版本的基础上，PostgreSQL增强版新增兼容Oracle  12c的隐式类型转换。

-   定长字符串类型CHARACTER与NUMERIC，INT4，INT8，FLOAT4，FLOAT8之间相互转换。
-   变长字符串类型VARCHAR与NUMERIC，INT4，INT8，FLOAT4，FLOAT8之间相互转换。
-   文本类型TEXT与NUMERIC，INT2，INT4，INT8，FLOAT4，FLOAT8之间相互转换。
-   短整形INT2转换为CHARACTER，VARCHAR。
-   二进制大对象BLOB与二进制RAW之间相互转换。

