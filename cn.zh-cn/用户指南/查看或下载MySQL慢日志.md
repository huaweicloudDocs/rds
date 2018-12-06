# 查看或下载慢日志<a name="TOPIC_0142028251"></a>

## 操作场景<a name="section61232893165332"></a>

慢查询日志用来记录执行时间超过当前慢日志阈值“long\_query\_time“（默认是1秒）的语句，您可以通过慢查询日志的日志明细、统计分析情况，查找出执行效率低的语句，进行优化。您也可以下载慢查询日志进行业务分析。

华为云关系型数据库服务支持以下执行语句类型：

-   SELECT
-   INSERT
-   UPDATE
-   DELETE
-   CREATE

## 参数解析<a name="section121471583582"></a>

**表 1**  MySQL慢查询相关的参数解析

<a name="table1455312241604"></a>
<table><thead align="left"><tr id="row1755318241201"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p455311242020"><a name="p455311242020"></a><a name="p455311242020"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p15534249012"><a name="p15534249012"></a><a name="p15534249012"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row145532241400"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p175533249020"><a name="p175533249020"></a><a name="p175533249020"></a>slow_query_log</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p1919174811719"><a name="p1919174811719"></a><a name="p1919174811719"></a>是否开启慢查询，0或者OFF为关闭，1或者ON为开启。默认值为ON，即为开启状态。</p>
</td>
</tr>
<tr id="row165533247017"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p155318242002"><a name="p155318242002"></a><a name="p155318242002"></a>slow_query_log_file</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p10553202412016"><a name="p10553202412016"></a><a name="p10553202412016"></a>指定慢查询日志存放路径。</p>
</td>
</tr>
<tr id="row35531624400"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p555392411010"><a name="p555392411010"></a><a name="p555392411010"></a>long_query_time</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p15370439216"><a name="p15370439216"></a><a name="p15370439216"></a>大于等于此时间记录慢查询日志，精度可达微秒级别，默认为1s。当设置为0时表示记录所有查询记录。建议设置为1s。注意：锁等待时间并不计算在执行时间内。</p>
</td>
</tr>
<tr id="row195531424101"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p8553132412010"><a name="p8553132412010"></a><a name="p8553132412010"></a>log_queries_not_using_indexes</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p35534249014"><a name="p35534249014"></a><a name="p35534249014"></a>是否记录未使用索引的查询，默认OFF。</p>
</td>
</tr>
<tr id="row455332412019"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p155535249010"><a name="p155535249010"></a><a name="p155535249010"></a>log_throttle_queries_not_using_indexes</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p45532243012"><a name="p45532243012"></a><a name="p45532243012"></a>每分钟允许写入到慢查询日志的未使用索引的语句，默认为0。</p>
</td>
</tr>
<tr id="row15745241532"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p85755242033"><a name="p85755242033"></a><a name="p85755242033"></a>log_slow_admin_statements</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p257510246312"><a name="p257510246312"></a><a name="p257510246312"></a>是否记录管理类指令，默认为OFF。</p>
</td>
</tr>
</tbody>
</table>

## 查看日志明细<a name="section467223910567"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
5.  在“慢日志  \>  日志明细“页签，查看慢SQL语句的详细信息。

    **图 1**  慢日志明细<a name="fig3667171913514"></a>  
    ![](figures/慢日志明细.png "慢日志明细")

    -   可选择查看不同时间段的慢日志记录。
    -   对于无法完全显示的“描述”，鼠标悬停查看完整信息。


## 统计分析慢日志<a name="section12190525710"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
5.  在“慢日志  \>  统计分析“页签，查看详细信息。

    **图 2**  慢日志统计分析<a name="fig314542335419"></a>  
    ![](figures/慢日志统计分析.png "慢日志统计分析")

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >“慢日志  \>  统计分析“页签中显示的SQL语句只是同一模式的SQL语句中的一个，作为示例，并不会列出所有的SQL语句。例如：先后执行了语句"select sleep\(11\)"和"select sleep\(12\)"，则它们同属于模式"select sleep\(N\)"，慢查询日志的结果中只会显示SQL语句"select sleep\(11\)"。  


## 下载慢日志<a name="section759312713359"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/region.png)，选择区域和项目。

    您可选择自己的专属计算集群（Dedicated Computing Cluster，简称DCC）。

3.  选择“数据库  \>  关系型数据库“，进入关系型数据库信息页面。
4.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
5.  在“慢日志  \>  下载“页签，对状态为“准备完成”的日志文件，单击操作列的“下载“，下载慢日志。

    **图 3**  下载慢日志<a name="fig711785217548"></a>  
    ![](figures/下载慢日志.png "下载慢日志")

    -   系统会自动加载下载准备任务，加载时长受日志文件大小及网络环境影响。

        -   下载准备过程中，日志文件状态显示为“准备中...”。
        -   下载准备完成，日志文件状态显示为“准备完成”。
        -   下载准备工作失败，日志文件状态显示为“异常”。

        “准备中...“和“异常“状态的日志文件不支持下载。

    -   当需要下载的文件大于50MB时，需要通过客户端工具OBS Browser进行下载。
    -   下载链接有效期为15分钟。如果超时，提示用户下载链接已失效，是否重新下载。若需重新下载，单击“确定”，否则单击“取消”。


