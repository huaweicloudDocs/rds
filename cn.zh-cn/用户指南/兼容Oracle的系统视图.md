# 兼容Oracle的系统视图<a name="rds_04_0003"></a>

本章节介绍了在PostgreSQL11开源版本的基础上，PostgreSQL增强版新增兼容Oracle  12c的系统视图。

**表 1**  系统视图

<a name="table76291533121113"></a>
<table><thead align="left"><tr id="row16629113316114"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p1762923361114"><a name="p1762923361114"></a><a name="p1762923361114"></a>超级管理员</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p1962913341117"><a name="p1962913341117"></a><a name="p1962913341117"></a>DBA</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p9629933131113"><a name="p9629933131113"></a><a name="p9629933131113"></a>USER</p>
</th>
</tr>
</thead>
<tbody><tr id="row146294339115"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p2629173312114"><a name="p2629173312114"></a><a name="p2629173312114"></a>ALL_ALL_TABLES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6629103311116"><a name="p6629103311116"></a><a name="p6629103311116"></a>DBA_ALL_TABLES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p662923317114"><a name="p662923317114"></a><a name="p662923317114"></a>-</p>
</td>
</tr>
<tr id="row7298313253"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p3645733181120"><a name="p3645733181120"></a><a name="p3645733181120"></a>ALL_COL_COMMENTS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1264583371118"><a name="p1264583371118"></a><a name="p1264583371118"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p179801614141918"><a name="p179801614141918"></a><a name="p179801614141918"></a>USER_COL_COMMENTS</p>
</td>
</tr>
<tr id="row1162993351115"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p262913361111"><a name="p262913361111"></a><a name="p262913361111"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1962993341112"><a name="p1962993341112"></a><a name="p1962993341112"></a>DBA_DATA_FILES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p9629153319118"><a name="p9629153319118"></a><a name="p9629153319118"></a>-</p>
</td>
</tr>
<tr id="row26291033191115"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p062983318111"><a name="p062983318111"></a><a name="p062983318111"></a>ALL_DIRECTORIES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p126291833171118"><a name="p126291833171118"></a><a name="p126291833171118"></a>DBA_DIRECTORIES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p762920334116"><a name="p762920334116"></a><a name="p762920334116"></a>-</p>
</td>
</tr>
<tr id="row1762914334114"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1351973103713"><a name="p1351973103713"></a><a name="p1351973103713"></a>ALL_INDEXES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p362916331113"><a name="p362916331113"></a><a name="p362916331113"></a>DBA_INDEXES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p17629173351111"><a name="p17629173351111"></a><a name="p17629173351111"></a>USER_INDEXES</p>
</td>
</tr>
<tr id="row362983361117"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p930614506456"><a name="p930614506456"></a><a name="p930614506456"></a>ALL_JOBS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1464543316115"><a name="p1464543316115"></a><a name="p1464543316115"></a>DBA_JOBS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p16645933201110"><a name="p16645933201110"></a><a name="p16645933201110"></a>USER_JOBS</p>
</td>
</tr>
<tr id="row12262172116255"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p4605202110194"><a name="p4605202110194"></a><a name="p4605202110194"></a>ALL_OBJECTS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p12957153217154"><a name="p12957153217154"></a><a name="p12957153217154"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p13957103251510"><a name="p13957103251510"></a><a name="p13957103251510"></a>USER_OBJECTS</p>
</td>
</tr>
<tr id="row9796419152317"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1379619197232"><a name="p1379619197232"></a><a name="p1379619197232"></a>ALL_PROCEDURES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1179631911235"><a name="p1179631911235"></a><a name="p1179631911235"></a>DBA_PROCEDURES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1979631912319"><a name="p1979631912319"></a><a name="p1979631912319"></a>USER_PROCEDURES</p>
</td>
</tr>
<tr id="row1364563381113"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p2645193312115"><a name="p2645193312115"></a><a name="p2645193312115"></a>ALL_SOURCE</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1964523311116"><a name="p1964523311116"></a><a name="p1964523311116"></a>DBA_SOURCE</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p36457339117"><a name="p36457339117"></a><a name="p36457339117"></a>USER_SOURCE</p>
</td>
</tr>
<tr id="row881704516156"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p0817104514154"><a name="p0817104514154"></a><a name="p0817104514154"></a>ALL_SEQUENCES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p9817445111518"><a name="p9817445111518"></a><a name="p9817445111518"></a>DBA_SEQUENCES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p87753212168"><a name="p87753212168"></a><a name="p87753212168"></a>USER_SEQUENCES</p>
</td>
</tr>
<tr id="row7114204411153"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p15114844141510"><a name="p15114844141510"></a><a name="p15114844141510"></a>ALL_TABLES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p10114164441512"><a name="p10114164441512"></a><a name="p10114164441512"></a>DBA_TABLES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p0114194414154"><a name="p0114194414154"></a><a name="p0114194414154"></a>USER_TABLES</p>
</td>
</tr>
<tr id="row13410104271510"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p24101642181511"><a name="p24101642181511"></a><a name="p24101642181511"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p041014220152"><a name="p041014220152"></a><a name="p041014220152"></a>DBA_TABLESPACES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p74101422158"><a name="p74101422158"></a><a name="p74101422158"></a>USER_TABLESPACE</p>
</td>
</tr>
<tr id="row106451340141517"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1864513406156"><a name="p1864513406156"></a><a name="p1864513406156"></a>ALL_TAB_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p2645184081515"><a name="p2645184081515"></a><a name="p2645184081515"></a>DBA_TAB_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p12645144031511"><a name="p12645144031511"></a><a name="p12645144031511"></a>USER_TAB_COLUMNS</p>
</td>
</tr>
<tr id="row68001038141510"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p11800193811158"><a name="p11800193811158"></a><a name="p11800193811158"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p118002387153"><a name="p118002387153"></a><a name="p118002387153"></a>DBA_TRIGGERS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1480073815158"><a name="p1480073815158"></a><a name="p1480073815158"></a>USER_TRIGGERS</p>
</td>
</tr>
<tr id="row139721136191515"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p15570155161810"><a name="p15570155161810"></a><a name="p15570155161810"></a>ALL_USERS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6972836141515"><a name="p6972836141515"></a><a name="p6972836141515"></a>DBA_USERS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p159721365157"><a name="p159721365157"></a><a name="p159721365157"></a>-</p>
</td>
</tr>
<tr id="row81769358152"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p15176163581519"><a name="p15176163581519"></a><a name="p15176163581519"></a>ALL_VIEWS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p117615357159"><a name="p117615357159"></a><a name="p117615357159"></a>DBA_VIEWS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1017613510154"><a name="p1017613510154"></a><a name="p1017613510154"></a>USER_VIEWS</p>
</td>
</tr>
<tr id="row178001256163711"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p780020561374"><a name="p780020561374"></a><a name="p780020561374"></a>ALL_IND_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1180025620379"><a name="p1180025620379"></a><a name="p1180025620379"></a>DBA_IND_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p6800165623711"><a name="p6800165623711"></a><a name="p6800165623711"></a>USER_IND_COLUMNS</p>
</td>
</tr>
<tr id="row135540318216"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p15971183918301"><a name="p15971183918301"></a><a name="p15971183918301"></a>ALL_TAB_PARTITIONS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p255510310214"><a name="p255510310214"></a><a name="p255510310214"></a>DBA_TAB_PARTITIONS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p55551834210"><a name="p55551834210"></a><a name="p55551834210"></a>USER_TAB_PARTITIONS</p>
</td>
</tr>
<tr id="row9823185927"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p188234517211"><a name="p188234517211"></a><a name="p188234517211"></a>ALL_PART_TABLES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p118236513218"><a name="p118236513218"></a><a name="p118236513218"></a>DBA_PART_TABLES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1382345424"><a name="p1382345424"></a><a name="p1382345424"></a>USER_PART_TABLES</p>
</td>
</tr>
<tr id="row1552611313573"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1152612315710"><a name="p1152612315710"></a><a name="p1152612315710"></a>ALL_PART_KEY_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p105271535572"><a name="p105271535572"></a><a name="p105271535572"></a>DBA_PART_KEY_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p11527939572"><a name="p11527939572"></a><a name="p11527939572"></a>USER_PART_KEY_COLUMNS</p>
</td>
</tr>
<tr id="row2074131718446"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p16368141811445"><a name="p16368141811445"></a><a name="p16368141811445"></a>ALL_PART_INDEXES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p2037720238444"><a name="p2037720238444"></a><a name="p2037720238444"></a>DBA_PART_INDEXES</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1347262716443"><a name="p1347262716443"></a><a name="p1347262716443"></a>USER_PART_INDEXES</p>
</td>
</tr>
<tr id="row9243675719"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1124186125710"><a name="p1124186125710"></a><a name="p1124186125710"></a>ALL_TAB_SUBPARTITIONS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p32416612578"><a name="p32416612578"></a><a name="p32416612578"></a>DBA_TAB_SUBPARTITIONS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p16241962576"><a name="p16241962576"></a><a name="p16241962576"></a>USER_TAB_SUBPARTITIONS</p>
</td>
</tr>
<tr id="row1031898155719"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p1031858105713"><a name="p1031858105713"></a><a name="p1031858105713"></a>ALL_SUBPART_KEY_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p93181865713"><a name="p93181865713"></a><a name="p93181865713"></a>DBA_SUBPART_KEY_COLUMNS</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p17318118205720"><a name="p17318118205720"></a><a name="p17318118205720"></a>USER_SUBPART_KEY_COLUMNS</p>
</td>
</tr>
</tbody>
</table>

**表 2**  普通视图

<a name="table5300133464316"></a>
<table><thead align="left"><tr id="row17300133416436"><th class="cellrowborder" valign="top" width="35.23%" id="mcps1.2.3.1.1"><p id="p128131814339"><a name="p128131814339"></a><a name="p128131814339"></a>视图名称</p>
</th>
<th class="cellrowborder" valign="top" width="64.77000000000001%" id="mcps1.2.3.1.2"><p id="p8300234164312"><a name="p8300234164312"></a><a name="p8300234164312"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row130013418433"><td class="cellrowborder" valign="top" width="35.23%" headers="mcps1.2.3.1.1 "><p id="p730053454314"><a name="p730053454314"></a><a name="p730053454314"></a>V$SESSION</p>
</td>
<td class="cellrowborder" valign="top" width="64.77000000000001%" headers="mcps1.2.3.1.2 "><p id="p13001734184315"><a name="p13001734184315"></a><a name="p13001734184315"></a>展示了与当前会话相关的信息，如SID，username等。</p>
</td>
</tr>
<tr id="row11657522153320"><td class="cellrowborder" valign="top" width="35.23%" headers="mcps1.2.3.1.1 "><p id="p6657202215333"><a name="p6657202215333"></a><a name="p6657202215333"></a>NLS_SESSION_PARAMETERS</p>
</td>
<td class="cellrowborder" valign="top" width="64.77000000000001%" headers="mcps1.2.3.1.2 "><p id="p8657122212334"><a name="p8657122212334"></a><a name="p8657122212334"></a>展示了当前会话的NLS参数及取值。</p>
</td>
</tr>
<tr id="row193121921163111"><td class="cellrowborder" valign="top" width="35.23%" headers="mcps1.2.3.1.1 "><p id="p1312182118311"><a name="p1312182118311"></a><a name="p1312182118311"></a>V$SESSION_LONGOPS</p>
</td>
<td class="cellrowborder" valign="top" width="64.77000000000001%" headers="mcps1.2.3.1.2 "><p id="p1031272183111"><a name="p1031272183111"></a><a name="p1031272183111"></a>显示运行时间超过6秒的数据库操作的状态。</p>
</td>
</tr>
</tbody>
</table>

