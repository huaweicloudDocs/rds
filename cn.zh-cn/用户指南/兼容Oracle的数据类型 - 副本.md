# 兼容Oracle的数据类型<a name="rds_04_0004"></a>

本章节介绍了在PostgreSQL11开源版本的基础上，PostgreSQL增强版新增兼容Oracle  12c的数据类型。

**表 1**  数据类型

<a name="table1154324117547"></a>
<table><thead align="left"><tr id="row135419416549"><th class="cellrowborder" valign="top" width="41.83%" id="mcps1.2.3.1.1"><p id="p25414414546"><a name="p25414414546"></a><a name="p25414414546"></a>数据类型名称</p>
</th>
<th class="cellrowborder" valign="top" width="58.17%" id="mcps1.2.3.1.2"><p id="p11541341195412"><a name="p11541341195412"></a><a name="p11541341195412"></a>数据类型</p>
</th>
</tr>
</thead>
<tbody><tr id="row05421041165419"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p5798468588"><a name="p5798468588"></a><a name="p5798468588"></a>变长字符串类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p19542204135419"><a name="p19542204135419"></a><a name="p19542204135419"></a>VARCHAR2，NVARCHAR2</p>
</td>
</tr>
<tr id="row195421141105417"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p19542194165414"><a name="p19542194165414"></a><a name="p19542194165414"></a>十进制浮点数类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p854234115542"><a name="p854234115542"></a><a name="p854234115542"></a>DECIMAL</p>
</td>
</tr>
<tr id="row20542144110543"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p19542041115416"><a name="p19542041115416"></a><a name="p19542041115416"></a>双精度二进制浮点类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p95421741115415"><a name="p95421741115415"></a><a name="p95421741115415"></a>BINARY_DOUBLE</p>
</td>
</tr>
<tr id="row754284117547"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p4542184125415"><a name="p4542184125415"></a><a name="p4542184125415"></a>二进制数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p154210417548"><a name="p154210417548"></a><a name="p154210417548"></a>RAW</p>
</td>
</tr>
<tr id="row10543114118541"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p05422041115410"><a name="p05422041115410"></a><a name="p05422041115410"></a>二进制大对象类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p15434416543"><a name="p15434416543"></a><a name="p15434416543"></a>BLOB</p>
</td>
</tr>
<tr id="row10543194114548"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p1254374119545"><a name="p1254374119545"></a><a name="p1254374119545"></a>字符大对象类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p55438412547"><a name="p55438412547"></a><a name="p55438412547"></a>CLOB</p>
</td>
</tr>
<tr id="row16267121917432"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p726719192439"><a name="p726719192439"></a><a name="p726719192439"></a>字节字符大对象类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p192671619204319"><a name="p192671619204319"></a><a name="p192671619204319"></a>NCLOB</p>
</td>
</tr>
<tr id="row10601553566"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p15611755165615"><a name="p15611755165615"></a><a name="p15611755165615"></a>数字类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p06113556562"><a name="p06113556562"></a><a name="p06113556562"></a>NUMBER</p>
</td>
</tr>
<tr id="row13435155795612"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p343515714568"><a name="p343515714568"></a><a name="p343515714568"></a>变长字符串类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p1543575755616"><a name="p1543575755616"></a><a name="p1543575755616"></a>NVARACHAR</p>
</td>
</tr>
<tr id="row3816959165617"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p6816165915616"><a name="p6816165915616"></a><a name="p6816165915616"></a>Unicode字符数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p48161859135615"><a name="p48161859135615"></a><a name="p48161859135615"></a>NCHAR</p>
</td>
</tr>
<tr id="row936714269570"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p43678260573"><a name="p43678260573"></a><a name="p43678260573"></a>三十二位浮点型数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p13367192616571"><a name="p13367192616571"></a><a name="p13367192616571"></a>BINARY_FLOAT</p>
</td>
</tr>
<tr id="row1772434218571"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p20724164214575"><a name="p20724164214575"></a><a name="p20724164214575"></a>长整型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p1572414220574"><a name="p1572414220574"></a><a name="p1572414220574"></a>LONG</p>
</td>
</tr>
<tr id="row123921245105717"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p43921458577"><a name="p43921458577"></a><a name="p43921458577"></a>XML数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p33921045145710"><a name="p33921045145710"></a><a name="p33921045145710"></a>XMLType</p>
</td>
</tr>
<tr id="row4854164715714"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p4854247165714"><a name="p4854247165714"></a><a name="p4854247165714"></a>本地时间戳数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p388613252004"><a name="p388613252004"></a><a name="p388613252004"></a>TIMESTAMP WITH LOCAL TIME ZONE</p>
</td>
</tr>
<tr id="row9788173745418"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p97891837115410"><a name="p97891837115410"></a><a name="p97891837115410"></a>PL/SQL整型溢出翻转数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p172831055145410"><a name="p172831055145410"></a><a name="p172831055145410"></a>BINARY_INTEGER</p>
</td>
</tr>
<tr id="row2177440105419"><td class="cellrowborder" valign="top" width="41.83%" headers="mcps1.2.3.1.1 "><p id="p5177124055412"><a name="p5177124055412"></a><a name="p5177124055412"></a>PL/SQL整型溢出错误数据类型</p>
</td>
<td class="cellrowborder" valign="top" width="58.17%" headers="mcps1.2.3.1.2 "><p id="p101771240195411"><a name="p101771240195411"></a><a name="p101771240195411"></a>PLS_INTEGER</p>
</td>
</tr>
</tbody>
</table>

