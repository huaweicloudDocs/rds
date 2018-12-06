# 监控指标<a name="TOPIC_0142028205"></a>

-   弹性云服务器相关监控指标，如[表1](支持的监控指标.md#table2501556415126)所示。
-   数据库指标监控项，如[表1](#table1713309394622)所示。

**表 1**  数据库性能监控列表

<a name="table1713309394622"></a>
<table><thead align="left"><tr id="row4051084894640"><th class="cellrowborder" valign="top" width="27.79%" id="mcps1.2.4.1.1"><p id="p6558327694716"><a name="p6558327694716"></a><a name="p6558327694716"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="52.65%" id="mcps1.2.4.1.2"><p id="p1064513594716"><a name="p1064513594716"></a><a name="p1064513594716"></a>含义</p>
</th>
<th class="cellrowborder" valign="top" width="19.56%" id="mcps1.2.4.1.3"><p id="p5694961594716"><a name="p5694961594716"></a><a name="p5694961594716"></a>取值范围</p>
</th>
</tr>
</thead>
<tbody><tr id="row1636834294622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p5076732794622"><a name="p5076732794622"></a><a name="p5076732794622"></a>事务日志使用量</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p1851285794622"><a name="p1851285794622"></a><a name="p1851285794622"></a>事务日志所占用的磁盘空间。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p2314647694622"><a name="p2314647694622"></a><a name="p2314647694622"></a>≥0MB</p>
</td>
</tr>
<tr id="row2945631294622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p3715105494622"><a name="p3715105494622"></a><a name="p3715105494622"></a>复制插槽使用量</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p5644543494622"><a name="p5644543494622"></a><a name="p5644543494622"></a>复制插槽文件所占磁盘容量。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p867740994622"><a name="p867740994622"></a><a name="p867740994622"></a>≥0MB</p>
</td>
</tr>
<tr id="row1759849394622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p1619180394622"><a name="p1619180394622"></a><a name="p1619180394622"></a>数据库连接数</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p3646763394622"><a name="p3646763394622"></a><a name="p3646763394622"></a>当前连接到数据库的连接数量。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p108829694622"><a name="p108829694622"></a><a name="p108829694622"></a>≥0counts</p>
</td>
</tr>
<tr id="row5517056694622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p3963083794622"><a name="p3963083794622"></a><a name="p3963083794622"></a>事务最大已使用ID数</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p5598121794622"><a name="p5598121794622"></a><a name="p5598121794622"></a>事务最大已使用ID。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p3818468994622"><a name="p3818468994622"></a><a name="p3818468994622"></a>≥0counts</p>
</td>
</tr>
<tr id="row5356870094622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p4409743094622"><a name="p4409743094622"></a><a name="p4409743094622"></a>事务日志生成速率</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p1512209794622"><a name="p1512209794622"></a><a name="p1512209794622"></a>平均每秒生成的事务日志大小。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p1693035794622"><a name="p1693035794622"></a><a name="p1693035794622"></a>≥0MB/s</p>
</td>
</tr>
<tr id="row6130817694622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p6701523294622"><a name="p6701523294622"></a><a name="p6701523294622"></a>最滞后副本滞后量</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p5952469294622"><a name="p5952469294622"></a><a name="p5952469294622"></a>多个副本中最滞后副本（依据接收到的WAL数据）滞后量。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p5677074194622"><a name="p5677074194622"></a><a name="p5677074194622"></a>≥0MB</p>
</td>
</tr>
<tr id="row4681001194622"><td class="cellrowborder" valign="top" width="27.79%" headers="mcps1.2.4.1.1 "><p id="p3351458694622"><a name="p3351458694622"></a><a name="p3351458694622"></a>复制时延</p>
</td>
<td class="cellrowborder" valign="top" width="52.65%" headers="mcps1.2.4.1.2 "><p id="p3032697894622"><a name="p3032697894622"></a><a name="p3032697894622"></a>副本滞后时延。</p>
</td>
<td class="cellrowborder" valign="top" width="19.56%" headers="mcps1.2.4.1.3 "><p id="p4056613894622"><a name="p4056613894622"></a><a name="p4056613894622"></a>≥0ms</p>
</td>
</tr>
</tbody>
</table>

