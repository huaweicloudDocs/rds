# 监控指标<a name="TOPIC_0142028429"></a>

-   弹性云服务器相关监控指标，如[表1](支持的监控指标.md#table2501556415126)所示。
-   数据库指标监控项，如[表1](#table1713309394622)所示。

**表 1**  数据库性能监控列表

<a name="table1713309394622"></a>
<table><thead align="left"><tr id="row4051084894640"><th class="cellrowborder" valign="top" width="31%" id="mcps1.2.4.1.1"><p id="p6558327694716"><a name="p6558327694716"></a><a name="p6558327694716"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="49%" id="mcps1.2.4.1.2"><p id="p1064513594716"><a name="p1064513594716"></a><a name="p1064513594716"></a>含义</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.3"><p id="p5694961594716"><a name="p5694961594716"></a><a name="p5694961594716"></a>取值范围</p>
</th>
</tr>
</thead>
<tbody><tr id="row1636834294622"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p57410223163524"><a name="p57410223163524"></a><a name="p57410223163524"></a>使用中的数据库连接数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p38892230163720"><a name="p38892230163720"></a><a name="p38892230163720"></a>该指标用于统计用户连接到数据库的连接数量。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p63262927163720"><a name="p63262927163720"></a><a name="p63262927163720"></a>≥0counts</p>
</td>
</tr>
<tr id="row1339224914275"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p18337561283"><a name="p18337561283"></a><a name="p18337561283"></a>平均每秒事务数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p122131051163319"><a name="p122131051163319"></a><a name="p122131051163319"></a>该指标用于统计数据库每秒启动的事务数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p24621238772"><a name="p24621238772"></a><a name="p24621238772"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row93921049132713"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p683318561287"><a name="p683318561287"></a><a name="p683318561287"></a>平均每秒batch数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1721335113315"><a name="p1721335113315"></a><a name="p1721335113315"></a>该指标用于统计每秒收到的Transact-SQL命令批数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p1748864414712"><a name="p1748864414712"></a><a name="p1748864414712"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row7391449162715"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p383417561885"><a name="p383417561885"></a><a name="p383417561885"></a>每秒登录次数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p3214105193312"><a name="p3214105193312"></a><a name="p3214105193312"></a>该指标用于统计每秒启动的登录总数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p98714191089"><a name="p98714191089"></a><a name="p98714191089"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row439194913273"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p1983465614812"><a name="p1983465614812"></a><a name="p1983465614812"></a>每秒登出次数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1221435143317"><a name="p1221435143317"></a><a name="p1221435143317"></a>该指标用于统计每秒启动的注销操作总数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p41202819811"><a name="p41202819811"></a><a name="p41202819811"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row939004982710"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p1114212616103"><a name="p1114212616103"></a><a name="p1114212616103"></a>缓存命中率</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1221485111339"><a name="p1221485111339"></a><a name="p1221485111339"></a>该指标用于统计在缓冲区高速缓存中找到而不需要从磁盘中读取的页的百分比。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p76871531184"><a name="p76871531184"></a><a name="p76871531184"></a>0~100%</p>
</td>
</tr>
<tr id="row739054914270"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p5152160107"><a name="p5152160107"></a><a name="p5152160107"></a>平均每秒SQL编译数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1421455103316"><a name="p1421455103316"></a><a name="p1421455103316"></a>该指标用于统计每秒SQL的编译数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p19925791397"><a name="p19925791397"></a><a name="p19925791397"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row838964942719"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p1515286151018"><a name="p1515286151018"></a><a name="p1515286151018"></a>平均每秒SQL重编译数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1121415133320"><a name="p1121415133320"></a><a name="p1121415133320"></a>该指标用于统计每秒语句重新编译的次数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p13768133920"><a name="p13768133920"></a><a name="p13768133920"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row11389144962714"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p131532613106"><a name="p131532613106"></a><a name="p131532613106"></a>每秒全表扫描数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p521485153313"><a name="p521485153313"></a><a name="p521485153313"></a>该指标用于统计每秒不受限制的完全扫描数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p105745319917"><a name="p105745319917"></a><a name="p105745319917"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row15388149202712"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p315314617106"><a name="p315314617106"></a><a name="p315314617106"></a>每秒用户错误数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p221435163318"><a name="p221435163318"></a><a name="p221435163318"></a>该指标用于统计每秒用户错误数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p145946343911"><a name="p145946343911"></a><a name="p145946343911"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row338764912275"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p715356181017"><a name="p715356181017"></a><a name="p715356181017"></a>每秒闩锁等待数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1221405117332"><a name="p1221405117332"></a><a name="p1221405117332"></a>该指标用于统计每秒未能立即授予的闩锁请求数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p1559120394917"><a name="p1559120394917"></a><a name="p1559120394917"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row338714913276"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p1174518448236"><a name="p1174518448236"></a><a name="p1174518448236"></a>每秒锁等待次数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p1021445111331"><a name="p1021445111331"></a><a name="p1021445111331"></a>该指标用于统计每秒要求调用者等待的锁请求数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p5218185116217"><a name="p5218185116217"></a><a name="p5218185116217"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row33861349142720"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p3745104422318"><a name="p3745104422318"></a><a name="p3745104422318"></a>每秒锁请求次数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p9214351153313"><a name="p9214351153313"></a><a name="p9214351153313"></a>该指标用于统计锁管理器每秒请求的新锁和锁转换数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p28611954162117"><a name="p28611954162117"></a><a name="p28611954162117"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row33851949112719"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p77452044102317"><a name="p77452044102317"></a><a name="p77452044102317"></a>每秒锁超时次数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p92141151103310"><a name="p92141151103310"></a><a name="p92141151103310"></a>该指标用于统计每秒超时的锁请求数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p944595802116"><a name="p944595802116"></a><a name="p944595802116"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row12385114915278"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p07451244152312"><a name="p07451244152312"></a><a name="p07451244152312"></a>平均锁等待延迟</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p13214451143316"><a name="p13214451143316"></a><a name="p13214451143316"></a>该指标用于统计每个导致等待的锁请求的平均等待时间（毫秒）。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p124068382212"><a name="p124068382212"></a><a name="p124068382212"></a>≥0ms</p>
</td>
</tr>
<tr id="row8384114912275"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p17745134418237"><a name="p17745134418237"></a><a name="p17745134418237"></a>每秒死锁次数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p20221135183314"><a name="p20221135183314"></a><a name="p20221135183314"></a>该指标用于统计每秒导致死锁的锁请求数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p186936182220"><a name="p186936182220"></a><a name="p186936182220"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row203831749112717"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p122122217243"><a name="p122122217243"></a><a name="p122122217243"></a>每秒检查点写入Page数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p822115515333"><a name="p822115515333"></a><a name="p822115515333"></a>该指标用于统计刷新所有脏页的检查点或其他操作每秒刷新到磁盘的页数。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p13189062418"><a name="p13189062418"></a><a name="p13189062418"></a>≥0counts/s</p>
</td>
</tr>
<tr id="row1038211493270"><td class="cellrowborder" valign="top" width="31%" headers="mcps1.2.4.1.1 "><p id="p82112262411"><a name="p82112262411"></a><a name="p82112262411"></a>慢查询数</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.2 "><p id="p7912145213338"><a name="p7912145213338"></a><a name="p7912145213338"></a>该指标用于统计当前正在执行的慢查询数目。</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.3 "><p id="p593212920247"><a name="p593212920247"></a><a name="p593212920247"></a>≥0counts</p>
</td>
</tr>
</tbody>
</table>

