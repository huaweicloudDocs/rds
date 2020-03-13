# 兼容Oracle的预定义参数<a name="rds_04_0012"></a>

本章节介绍了在PostgreSQL11开源版本的基础上，PostgreSQL增强版新增兼容Oracle 12c的预定义参数。

**表 1**  兼容Oracle的预定义参数

<a name="table14545131315401"></a>
<table><thead align="left"><tr id="row65451313154018"><th class="cellrowborder" valign="top" width="34.8%" id="mcps1.2.3.1.1"><p id="p115451313104019"><a name="p115451313104019"></a><a name="p115451313104019"></a>预定义参数</p>
</th>
<th class="cellrowborder" valign="top" width="65.2%" id="mcps1.2.3.1.2"><p id="p12545101313400"><a name="p12545101313400"></a><a name="p12545101313400"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row0545101314017"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p6116643162815"><a name="p6116643162815"></a><a name="p6116643162815"></a>NLS_DATE_FORMAT</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p01781383293"><a name="p01781383293"></a><a name="p01781383293"></a>日期格式定义参数。</p>
</td>
</tr>
<tr id="row354517136409"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p20116343172814"><a name="p20116343172814"></a><a name="p20116343172814"></a>NLS_DATE_LANGUAGE</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p8116164362816"><a name="p8116164362816"></a><a name="p8116164362816"></a>日期语言定义参数。</p>
</td>
</tr>
<tr id="row10362185713113"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p158052191916"><a name="p158052191916"></a><a name="p158052191916"></a>NLS_DUAL_CURRENCY</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p89785171111"><a name="p89785171111"></a><a name="p89785171111"></a>区域名称定义参数，影响本地货币符号显示格式；</p>
</td>
</tr>
<tr id="row12561141364018"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p4116343202820"><a name="p4116343202820"></a><a name="p4116343202820"></a>NLS_CURRENCY</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p1211617432283"><a name="p1211617432283"></a><a name="p1211617432283"></a>货币符号定义参数。</p>
</td>
</tr>
<tr id="row21311058427"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p113211581213"><a name="p113211581213"></a><a name="p113211581213"></a>NLS_TIME_FORMAT</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p1513213581625"><a name="p1513213581625"></a><a name="p1513213581625"></a>不带时区的时间格式定义参数。</p>
</td>
</tr>
<tr id="row4597100531"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p195971401531"><a name="p195971401531"></a><a name="p195971401531"></a>NLS_TIME_TZ_FORMAT</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p1559714017314"><a name="p1559714017314"></a><a name="p1559714017314"></a>带时区的时间格式定义参数。</p>
</td>
</tr>
<tr id="row785983211316"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p0475175682814"><a name="p0475175682814"></a><a name="p0475175682814"></a>NLS_TIMESTAMP_FORMAT</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p1853818092915"><a name="p1853818092915"></a><a name="p1853818092915"></a>不带时区的时间戳格式定义参数。</p>
</td>
</tr>
<tr id="row206917211316"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p116922021139"><a name="p116922021139"></a><a name="p116922021139"></a>NLS_TIMESTAMP_TZ_FORMAT</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p146923215314"><a name="p146923215314"></a><a name="p146923215314"></a>带时区的时间戳格式定义参数。</p>
</td>
</tr>
<tr id="row175434033"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p47541441538"><a name="p47541441538"></a><a name="p47541441538"></a>NLS_NUMERIC_CHARACTERS</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p7754641238"><a name="p7754641238"></a><a name="p7754641238"></a>十进制数分组分割符定义参数。</p>
</td>
</tr>
<tr id="row15944151446"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p18951615545"><a name="p18951615545"></a><a name="p18951615545"></a>NLS_ISO_CURRENCY</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p10956157413"><a name="p10956157413"></a><a name="p10956157413"></a>区域名称定义参数，影响ISO货币符号显示格式。</p>
</td>
</tr>
<tr id="row74615121545"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p204611712747"><a name="p204611712747"></a><a name="p204611712747"></a>NLS_TERRITORY</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p114612121414"><a name="p114612121414"></a><a name="p114612121414"></a>区域名称定义参数，会根据区域货币与数字显示格式重置NLS_CURRENCY、NLS_ISO_CURRENCY、NLS_NUMERIC_CHARACTERS参数值。</p>
</td>
</tr>
<tr id="row1296826332"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p2968561739"><a name="p2968561739"></a><a name="p2968561739"></a>NLS_LANGUAGE</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p1096814611314"><a name="p1096814611314"></a><a name="p1096814611314"></a>区域语言定义参数。</p>
</td>
</tr>
<tr id="row29971022515"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p899711221214"><a name="p899711221214"></a><a name="p899711221214"></a>NLS_LENGTH_SEMANTICS</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p499752210113"><a name="p499752210113"></a><a name="p499752210113"></a>指定字符串字段定义时的默认长度单位，取值范围：BYTE，CHAR；</p>
</td>
</tr>
<tr id="row298617551740"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p1698716552414"><a name="p1698716552414"></a><a name="p1698716552414"></a>NLS_SORT</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p69561751457"><a name="p69561751457"></a><a name="p69561751457"></a>指定本地字符集排序规则。</p>
</td>
</tr>
<tr id="row633505810418"><td class="cellrowborder" valign="top" width="34.8%" headers="mcps1.2.3.1.1 "><p id="p23359586412"><a name="p23359586412"></a><a name="p23359586412"></a>NLS_COMP</p>
</td>
<td class="cellrowborder" valign="top" width="65.2%" headers="mcps1.2.3.1.2 "><p id="p233505820417"><a name="p233505820417"></a><a name="p233505820417"></a>指定会话级范围查找或排序操作的排序规则。</p>
</td>
</tr>
</tbody>
</table>

