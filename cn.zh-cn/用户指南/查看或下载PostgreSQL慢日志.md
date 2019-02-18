# 查看或下载慢日志<a name="slow_query_log-pg"></a>

## 操作场景<a name="section61232893165332"></a>

慢查询日志用来记录执行时间超过当前慢日志阈值“log\_min\_duration\_statement“（默认为1秒）的语句，您可以通过慢查询日志的日志明细、统计分析情况，查找出执行效率低的语句，进行优化。您也可以下载慢查询日志进行业务分析。

华为云关系型数据库服务支持以下执行语句类型：

-   SELECT
-   INSERT
-   UPDATE
-   DELETE
-   CREATE
-   DROP
-   ALTER
-   DO
-   CALL
-   COPY

## 参数解析<a name="section121471583582"></a>

**表 1**  PostgreSQL慢查询相关的参数解析

<a name="table1455312241604"></a>
<table><thead align="left"><tr id="row1755318241201"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p455311242020"><a name="p455311242020"></a><a name="p455311242020"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p15534249012"><a name="p15534249012"></a><a name="p15534249012"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row145532241400"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p26741582414"><a name="p26741582414"></a><a name="p26741582414"></a>log_min_duration_statement</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p13674185817412"><a name="p13674185817412"></a><a name="p13674185817412"></a>设置最小执行时间，执行时间大于等于这个值的语句都将被记录。默认为1秒。</p>
</td>
</tr>
</tbody>
</table>

## 查看日志明细<a name="section467223910567"></a>

1.  [登录云数据库](https://support.huaweicloud.com/qs-rds/rds_login.html)。
2.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
3.  在左侧导航栏单击“慢日志“，选择“日志明细“页签，查看慢SQL语句的详细信息。

    慢日志功能支持查看指定执行语句类型或时间段的慢日志记录。


## 统计分析慢日志<a name="section12190525710"></a>

1.  [登录云数据库](https://support.huaweicloud.com/qs-rds/rds_login.html)。
2.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
3.  在左侧导航栏单击“慢日志“，选择“统计分析“页签，查看详细信息。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >慢日志的“统计分析“页签中显示的SQL语句只是同一模式的SQL语句中的一个，作为示例，并不会列出所有的SQL语句。例如：先后执行了语句"select sleep\(1\)"和"select sleep\(2\)"，则它们同属于模式"select sleep\(N\)"，慢查询日志的结果中只会显示SQL语句"select sleep\(1\)"。  


## 下载慢日志<a name="section759312713359"></a>

1.  [登录云数据库](https://support.huaweicloud.com/qs-rds/rds_login.html)。
2.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
3.  在左侧导航栏单击“慢日志“，选择“下载“页签，对状态为“准备完成”的日志文件，单击操作列中的“下载”，下载慢日志。

    **图 1**  下载慢日志<a name="fig711785217548"></a>  
    ![](figures/下载慢日志-6.png "下载慢日志-6")

    -   系统会自动加载下载准备任务，加载时长受日志文件大小及网络环境影响。

        -   下载准备过程中，日志文件状态显示为“准备中...”。
        -   下载准备完成，日志文件状态显示为“准备完成”。
        -   下载准备工作失败，日志文件状态显示为“异常”。

        “准备中...“和“异常“状态的日志文件不支持下载。

    -   下载链接有效期为5分钟。如果超时，提示用户下载链接已失效，是否重新下载。若需重新下载，单击“确定”，否则单击“取消”。


