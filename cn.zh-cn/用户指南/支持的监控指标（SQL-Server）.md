# 支持的监控指标<a name="rds_sqlserver_06_0001"></a>

## 功能说明<a name="section3846020215313"></a>

本节定义了关系型数据库上报云监控的监控指标的命名空间，监控指标列表和维度定义，用户可以通过云监控提供的API接口来检索关系型数据库产生的监控指标和告警信息。

## 命名空间<a name="section1688213153437"></a>

SYS.RDS

## 实例监控指标<a name="section758818457377"></a>

-   弹性云服务器相关指标，如[表1](#zh-cn_topic_0171122394_table2501556415126)所示。

    **表 1**  弹性云服务器性能监控列表

    <a name="zh-cn_topic_0171122394_table2501556415126"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0171122394_row1227696315126"><th class="cellrowborder" valign="top" width="18.01%" id="mcps1.2.7.1.1"><p id="p3333174917503"><a name="p3333174917503"></a><a name="p3333174917503"></a>指标</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.32%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0171122394_p5084337715126"><a name="zh-cn_topic_0171122394_p5084337715126"></a><a name="zh-cn_topic_0171122394_p5084337715126"></a>指标名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="30.48%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0171122394_p2467289315126"><a name="zh-cn_topic_0171122394_p2467289315126"></a><a name="zh-cn_topic_0171122394_p2467289315126"></a>含义</p>
    </th>
    <th class="cellrowborder" valign="top" width="9.4%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0171122394_p5234735015126"><a name="zh-cn_topic_0171122394_p5234735015126"></a><a name="zh-cn_topic_0171122394_p5234735015126"></a>取值范围</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.94%" id="mcps1.2.7.1.5"><p id="p10610125265116"><a name="p10610125265116"></a><a name="p10610125265116"></a>测量对象和监控对象</p>
    </th>
    <th class="cellrowborder" valign="top" width="7.85%" id="mcps1.2.7.1.6"><p id="p3610195212511"><a name="p3610195212511"></a><a name="p3610195212511"></a>监控周期（原始指标）</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0171122394_row5692358915126"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p751061735110"><a name="p751061735110"></a><a name="p751061735110"></a>rds001_cpu_util</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p5490996515126"><a name="zh-cn_topic_0171122394_p5490996515126"></a><a name="zh-cn_topic_0171122394_p5490996515126"></a>CPU使用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p1852217115126"><a name="zh-cn_topic_0171122394_p1852217115126"></a><a name="zh-cn_topic_0171122394_p1852217115126"></a>该指标用于统计测量对象的CPU利用率。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p2390088615126"><a name="zh-cn_topic_0171122394_p2390088615126"></a><a name="zh-cn_topic_0171122394_p2390088615126"></a>0～100%</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p15839192211539"><a name="p15839192211539"></a><a name="p15839192211539"></a>测量对象：弹性云服务器</p>
    <p id="p12839152225312"><a name="p12839152225312"></a><a name="p12839152225312"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p3839622135312"><a name="p3839622135312"></a><a name="p3839622135312"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row21596471996"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p1751031705114"><a name="p1751031705114"></a><a name="p1751031705114"></a>rds003_iops</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p36363015126"><a name="zh-cn_topic_0171122394_p36363015126"></a><a name="zh-cn_topic_0171122394_p36363015126"></a>IOPS</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p2945410815126"><a name="zh-cn_topic_0171122394_p2945410815126"></a><a name="zh-cn_topic_0171122394_p2945410815126"></a>该指标用于统计当前实例，单位时间内系统处理的I/O请求数量（平均值）。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p3697255815126"><a name="zh-cn_topic_0171122394_p3697255815126"></a><a name="zh-cn_topic_0171122394_p3697255815126"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p5839102211536"><a name="p5839102211536"></a><a name="p5839102211536"></a>测量对象：弹性云服务器</p>
    <p id="p883911222532"><a name="p883911222532"></a><a name="p883911222532"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p1783912210536"><a name="p1783912210536"></a><a name="p1783912210536"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1323713512918"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p451061715118"><a name="p451061715118"></a><a name="p451061715118"></a>rds039_disk_util</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p3318453015126"><a name="zh-cn_topic_0171122394_p3318453015126"></a><a name="zh-cn_topic_0171122394_p3318453015126"></a>磁盘利用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p359239415126"><a name="zh-cn_topic_0171122394_p359239415126"></a><a name="zh-cn_topic_0171122394_p359239415126"></a>该指标用于统计测量对象的磁盘利用率。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p2254847415126"><a name="zh-cn_topic_0171122394_p2254847415126"></a><a name="zh-cn_topic_0171122394_p2254847415126"></a>0～100%</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p483912222537"><a name="p483912222537"></a><a name="p483912222537"></a>测量对象：弹性云服务器</p>
    <p id="p783917224533"><a name="p783917224533"></a><a name="p783917224533"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p18839322115316"><a name="p18839322115316"></a><a name="p18839322115316"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1495348415126"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p17510201712511"><a name="p17510201712511"></a><a name="p17510201712511"></a>rds002_mem_util</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p4255025615126"><a name="zh-cn_topic_0171122394_p4255025615126"></a><a name="zh-cn_topic_0171122394_p4255025615126"></a>内存使用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p2401868115126"><a name="zh-cn_topic_0171122394_p2401868115126"></a><a name="zh-cn_topic_0171122394_p2401868115126"></a>该指标用于统计测量对象的内存利用率。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p6646497015126"><a name="zh-cn_topic_0171122394_p6646497015126"></a><a name="zh-cn_topic_0171122394_p6646497015126"></a>0～100%</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p583914222532"><a name="p583914222532"></a><a name="p583914222532"></a>测量对象：弹性云服务器</p>
    <p id="p583942265310"><a name="p583942265310"></a><a name="p583942265310"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p19839172285316"><a name="p19839172285316"></a><a name="p19839172285316"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1515911115126"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p651001719518"><a name="p651001719518"></a><a name="p651001719518"></a>rds004_bytes_in</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p4234088815126"><a name="zh-cn_topic_0171122394_p4234088815126"></a><a name="zh-cn_topic_0171122394_p4234088815126"></a>网络输入吞吐量</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p62108092162725"><a name="zh-cn_topic_0171122394_p62108092162725"></a><a name="zh-cn_topic_0171122394_p62108092162725"></a>该指标用于统计平均每秒从测量对象的所有网络适配器输入的流量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p3498433815126"><a name="zh-cn_topic_0171122394_p3498433815126"></a><a name="zh-cn_topic_0171122394_p3498433815126"></a>≥0bytes/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p384032218537"><a name="p384032218537"></a><a name="p384032218537"></a>测量对象：弹性云服务器</p>
    <p id="p2084042275315"><a name="p2084042275315"></a><a name="p2084042275315"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p168401222125311"><a name="p168401222125311"></a><a name="p168401222125311"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row368717015126"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p14510101714517"><a name="p14510101714517"></a><a name="p14510101714517"></a>rds005_bytes_out</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p221427715126"><a name="zh-cn_topic_0171122394_p221427715126"></a><a name="zh-cn_topic_0171122394_p221427715126"></a>网络输出吞吐量</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p4513871415126"><a name="zh-cn_topic_0171122394_p4513871415126"></a><a name="zh-cn_topic_0171122394_p4513871415126"></a>该指标用于统计平均每秒从测量对象的所有网络适配器输出的流量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p3235719515126"><a name="zh-cn_topic_0171122394_p3235719515126"></a><a name="zh-cn_topic_0171122394_p3235719515126"></a>≥0bytes/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p9840102265318"><a name="p9840102265318"></a><a name="p9840102265318"></a>测量对象：弹性云服务器</p>
    <p id="p188401322105313"><a name="p188401322105313"></a><a name="p188401322105313"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p15840192210538"><a name="p15840192210538"></a><a name="p15840192210538"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1357144291416"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p13510417115110"><a name="p13510417115110"></a><a name="p13510417115110"></a>rds049_disk_read_throughput</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p59436423162135"><a name="zh-cn_topic_0171122394_p59436423162135"></a><a name="zh-cn_topic_0171122394_p59436423162135"></a>硬盘读吞吐量</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p49620984162135"><a name="zh-cn_topic_0171122394_p49620984162135"></a><a name="zh-cn_topic_0171122394_p49620984162135"></a>该指标用于统计每秒从磁盘读取的字节数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p59876806162135"><a name="zh-cn_topic_0171122394_p59876806162135"></a><a name="zh-cn_topic_0171122394_p59876806162135"></a>≥0bytes/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p178401222185312"><a name="p178401222185312"></a><a name="p178401222185312"></a>测量对象：弹性云服务器</p>
    <p id="p11840322165311"><a name="p11840322165311"></a><a name="p11840322165311"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p1884052275314"><a name="p1884052275314"></a><a name="p1884052275314"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row103958469147"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p951061705116"><a name="p951061705116"></a><a name="p951061705116"></a>rds050_disk_write_throughput</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p63245844162132"><a name="zh-cn_topic_0171122394_p63245844162132"></a><a name="zh-cn_topic_0171122394_p63245844162132"></a>硬盘写吞吐量</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p22639760162132"><a name="zh-cn_topic_0171122394_p22639760162132"></a><a name="zh-cn_topic_0171122394_p22639760162132"></a>该指标用于统计每秒写入磁盘的字节数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p21881305162132"><a name="zh-cn_topic_0171122394_p21881305162132"></a><a name="zh-cn_topic_0171122394_p21881305162132"></a>≥0bytes/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p128408220533"><a name="p128408220533"></a><a name="p128408220533"></a>测量对象：弹性云服务器</p>
    <p id="p18840922185312"><a name="p18840922185312"></a><a name="p18840922185312"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p1684012225539"><a name="p1684012225539"></a><a name="p1684012225539"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1144519401149"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p7510217135119"><a name="p7510217135119"></a><a name="p7510217135119"></a>rds051_avg_disk_sec_per_read</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p52754676162127"><a name="zh-cn_topic_0171122394_p52754676162127"></a><a name="zh-cn_topic_0171122394_p52754676162127"></a>硬盘读耗时</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p45270338162127"><a name="zh-cn_topic_0171122394_p45270338162127"></a><a name="zh-cn_topic_0171122394_p45270338162127"></a>该指标用于统计读取磁盘1KB数据所耗时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p43018728162127"><a name="zh-cn_topic_0171122394_p43018728162127"></a><a name="zh-cn_topic_0171122394_p43018728162127"></a>&gt;0ms</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p0840422195312"><a name="p0840422195312"></a><a name="p0840422195312"></a>测量对象：弹性云服务器</p>
    <p id="p1084010224532"><a name="p1084010224532"></a><a name="p1084010224532"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p13840122216538"><a name="p13840122216538"></a><a name="p13840122216538"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1842903718149"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p1451011171518"><a name="p1451011171518"></a><a name="p1451011171518"></a>rds052_avg_disk_sec_per_write</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p50241145162111"><a name="zh-cn_topic_0171122394_p50241145162111"></a><a name="zh-cn_topic_0171122394_p50241145162111"></a>硬盘写耗时</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p43000972162111"><a name="zh-cn_topic_0171122394_p43000972162111"></a><a name="zh-cn_topic_0171122394_p43000972162111"></a>该指标用于统计写入磁盘1KB数据所耗时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p60526687162111"><a name="zh-cn_topic_0171122394_p60526687162111"></a><a name="zh-cn_topic_0171122394_p60526687162111"></a>&gt;0ms</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p484082219538"><a name="p484082219538"></a><a name="p484082219538"></a>测量对象：弹性云服务器</p>
    <p id="p1484022225311"><a name="p1484022225311"></a><a name="p1484022225311"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p10840122211535"><a name="p10840122211535"></a><a name="p10840122211535"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row45617812162113"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p751041795112"><a name="p751041795112"></a><a name="p751041795112"></a>rds047_disk_total_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p4055305162113"><a name="zh-cn_topic_0171122394_p4055305162113"></a><a name="zh-cn_topic_0171122394_p4055305162113"></a>磁盘总大小</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p60044274162113"><a name="zh-cn_topic_0171122394_p60044274162113"></a><a name="zh-cn_topic_0171122394_p60044274162113"></a>该指标用于统计测量对象的磁盘总大小。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p31748024162113"><a name="zh-cn_topic_0171122394_p31748024162113"></a><a name="zh-cn_topic_0171122394_p31748024162113"></a>40GB～4000GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p8840722145310"><a name="p8840722145310"></a><a name="p8840722145310"></a>测量对象：弹性云服务器</p>
    <p id="p15840182225316"><a name="p15840182225316"></a><a name="p15840182225316"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p4840182255319"><a name="p4840182255319"></a><a name="p4840182255319"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row18847359162111"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p1351081715114"><a name="p1351081715114"></a><a name="p1351081715114"></a>rds048_disk_used_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p38243505162117"><a name="zh-cn_topic_0171122394_p38243505162117"></a><a name="zh-cn_topic_0171122394_p38243505162117"></a>磁盘使用量</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p10716207162117"><a name="zh-cn_topic_0171122394_p10716207162117"></a><a name="zh-cn_topic_0171122394_p10716207162117"></a>该指标用于统计测量对象的磁盘使用大小。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p62706478162117"><a name="zh-cn_topic_0171122394_p62706478162117"></a><a name="zh-cn_topic_0171122394_p62706478162117"></a>0GB～4000GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p12840102285318"><a name="p12840102285318"></a><a name="p12840102285318"></a>测量对象：弹性云服务器</p>
    <p id="p208405228537"><a name="p208405228537"></a><a name="p208405228537"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p98408223532"><a name="p98408223532"></a><a name="p98408223532"></a>1分钟</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0171122394_row1111897216238"><td class="cellrowborder" valign="top" width="18.01%" headers="mcps1.2.7.1.1 "><p id="p185101817165120"><a name="p185101817165120"></a><a name="p185101817165120"></a>rds053_avg_disk_queue_length</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.32%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0171122394_p2822150916238"><a name="zh-cn_topic_0171122394_p2822150916238"></a><a name="zh-cn_topic_0171122394_p2822150916238"></a>磁盘平均队列长度</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.48%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0171122394_p424085416238"><a name="zh-cn_topic_0171122394_p424085416238"></a><a name="zh-cn_topic_0171122394_p424085416238"></a>该指标用于统计等待写入测量对象的进程个数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0171122394_p796488816238"><a name="zh-cn_topic_0171122394_p796488816238"></a><a name="zh-cn_topic_0171122394_p796488816238"></a>≥0</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.7.1.5 "><p id="p084020224533"><a name="p084020224533"></a><a name="p084020224533"></a>测量对象：弹性云服务器</p>
    <p id="p1840122135313"><a name="p1840122135313"></a><a name="p1840122135313"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="7.85%" headers="mcps1.2.7.1.6 "><p id="p1284172216534"><a name="p1284172216534"></a><a name="p1284172216534"></a>1分钟</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Microsoft SQL Server数据库性能监控指标，如[\#rds\_sqlserver\_06\_0001/table46701376141844](#table46701376141844)所示。

    **表 2**  数据库监控指标

    <a name="table7786210181813"></a>
    <table><thead align="left"><tr id="row1110071171816"><th class="cellrowborder" valign="top" width="20.169999999999998%" id="mcps1.2.7.1.1"><p id="p109119248589"><a name="p109119248589"></a><a name="p109119248589"></a>指标</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.08%" id="mcps1.2.7.1.2"><p id="p71002113189"><a name="p71002113189"></a><a name="p71002113189"></a>指标名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.42%" id="mcps1.2.7.1.3"><p id="p15100101118182"><a name="p15100101118182"></a><a name="p15100101118182"></a>含义</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.7%" id="mcps1.2.7.1.4"><p id="p3100111191812"><a name="p3100111191812"></a><a name="p3100111191812"></a>取值范围</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.979999999999997%" id="mcps1.2.7.1.5"><p id="p7513420165815"><a name="p7513420165815"></a><a name="p7513420165815"></a>测量对象和监控对象</p>
    </th>
    <th class="cellrowborder" valign="top" width="8.649999999999999%" id="mcps1.2.7.1.6"><p id="p251332015814"><a name="p251332015814"></a><a name="p251332015814"></a>监控周期（原始指标）</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2010071111187"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p13989154075617"><a name="p13989154075617"></a><a name="p13989154075617"></a>rds055_transactions_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p1610061112184"><a name="p1610061112184"></a><a name="p1610061112184"></a>平均每秒事务数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p2100191114187"><a name="p2100191114187"></a><a name="p2100191114187"></a>该指标用于统计数据库每秒启动的事务数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p16100611141818"><a name="p16100611141818"></a><a name="p16100611141818"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p3908429145712"><a name="p3908429145712"></a><a name="p3908429145712"></a>测量对象：数据库</p>
    <p id="p13908102945713"><a name="p13908102945713"></a><a name="p13908102945713"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p8908192945713"><a name="p8908192945713"></a><a name="p8908192945713"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row1710081113180"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p18989184015610"><a name="p18989184015610"></a><a name="p18989184015610"></a>rds056_batch_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p62039184019"><a name="p62039184019"></a><a name="p62039184019"></a>平均每秒batch数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p18100411161813"><a name="p18100411161813"></a><a name="p18100411161813"></a>该指标用于统计每秒收到的Transact-SQL命令批数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p131001511151814"><a name="p131001511151814"></a><a name="p131001511151814"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p69081429105711"><a name="p69081429105711"></a><a name="p69081429105711"></a>测量对象：数据库</p>
    <p id="p12908192925718"><a name="p12908192925718"></a><a name="p12908192925718"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p109088296571"><a name="p109088296571"></a><a name="p109088296571"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row1710012115188"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p11989104017565"><a name="p11989104017565"></a><a name="p11989104017565"></a>rds057_logins_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p1010118112189"><a name="p1010118112189"></a><a name="p1010118112189"></a>每秒登录次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p1410151119185"><a name="p1410151119185"></a><a name="p1410151119185"></a>该指标用于统计每秒启动的登录总数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p6101131120189"><a name="p6101131120189"></a><a name="p6101131120189"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p19908729185714"><a name="p19908729185714"></a><a name="p19908729185714"></a>测量对象：数据库</p>
    <p id="p390832912572"><a name="p390832912572"></a><a name="p390832912572"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p1490819297577"><a name="p1490819297577"></a><a name="p1490819297577"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row9101161181811"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p1098944095610"><a name="p1098944095610"></a><a name="p1098944095610"></a>rds058_logouts_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p9101211161813"><a name="p9101211161813"></a><a name="p9101211161813"></a>每秒登出次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p910131116184"><a name="p910131116184"></a><a name="p910131116184"></a>该指标用于统计每秒启动的注销操作总数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p11101191113181"><a name="p11101191113181"></a><a name="p11101191113181"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p13908132945718"><a name="p13908132945718"></a><a name="p13908132945718"></a>测量对象：数据库</p>
    <p id="p18908102995713"><a name="p18908102995713"></a><a name="p18908102995713"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p290882914579"><a name="p290882914579"></a><a name="p290882914579"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row91014118182"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p4990140175613"><a name="p4990140175613"></a><a name="p4990140175613"></a>rds059_cache_hit_ratio</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p19101611161817"><a name="p19101611161817"></a><a name="p19101611161817"></a>缓存命中率</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p8101171101819"><a name="p8101171101819"></a><a name="p8101171101819"></a>该指标用于统计在缓冲区高速缓存中找到而不需要从磁盘中读取的页的百分比。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p510111112187"><a name="p510111112187"></a><a name="p510111112187"></a>0~100%</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p6908182915577"><a name="p6908182915577"></a><a name="p6908182915577"></a>测量对象：数据库</p>
    <p id="p169080294577"><a name="p169080294577"></a><a name="p169080294577"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p119081229195711"><a name="p119081229195711"></a><a name="p119081229195711"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row51016119188"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p899014408568"><a name="p899014408568"></a><a name="p899014408568"></a>rds060_sql_compilations_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p19830174016"><a name="p19830174016"></a><a name="p19830174016"></a>平均每秒SQL编译数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p13101181117181"><a name="p13101181117181"></a><a name="p13101181117181"></a>该指标用于统计每秒SQL的编译数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p2101151114180"><a name="p2101151114180"></a><a name="p2101151114180"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p9908172915712"><a name="p9908172915712"></a><a name="p9908172915712"></a>测量对象：数据库</p>
    <p id="p139082293571"><a name="p139082293571"></a><a name="p139082293571"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p1590822985714"><a name="p1590822985714"></a><a name="p1590822985714"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row710171171817"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p0990184025614"><a name="p0990184025614"></a><a name="p0990184025614"></a>rds061_sql_recompilations_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p12101111161813"><a name="p12101111161813"></a><a name="p12101111161813"></a>平均每秒SQL重编译数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p510112112185"><a name="p510112112185"></a><a name="p510112112185"></a>该指标用于统计每秒语句重新编译的次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p17101911191813"><a name="p17101911191813"></a><a name="p17101911191813"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p1190812293570"><a name="p1190812293570"></a><a name="p1190812293570"></a>测量对象：数据库</p>
    <p id="p1990832965716"><a name="p1990832965716"></a><a name="p1990832965716"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p13908529195712"><a name="p13908529195712"></a><a name="p13908529195712"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row18101101113182"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p12990154015562"><a name="p12990154015562"></a><a name="p12990154015562"></a>rds062_full_scans_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p5101111141811"><a name="p5101111141811"></a><a name="p5101111141811"></a>每秒全表扫描次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p3101121141820"><a name="p3101121141820"></a><a name="p3101121141820"></a>该指标用于统计每秒不受限制的完全扫描数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p9101161151818"><a name="p9101161151818"></a><a name="p9101161151818"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p17908729175716"><a name="p17908729175716"></a><a name="p17908729175716"></a>测量对象：数据库</p>
    <p id="p4908132925716"><a name="p4908132925716"></a><a name="p4908132925716"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p15908529105719"><a name="p15908529105719"></a><a name="p15908529105719"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row4101171119187"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p1499034035616"><a name="p1499034035616"></a><a name="p1499034035616"></a>rds063_errors_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p610114113182"><a name="p610114113182"></a><a name="p610114113182"></a>每秒用户错误数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p131016115184"><a name="p131016115184"></a><a name="p131016115184"></a>该指标用于统计每秒用户错误数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p1510111117181"><a name="p1510111117181"></a><a name="p1510111117181"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p1290813298575"><a name="p1290813298575"></a><a name="p1290813298575"></a>测量对象：数据库</p>
    <p id="p590910299579"><a name="p590910299579"></a><a name="p590910299579"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p4909429105720"><a name="p4909429105720"></a><a name="p4909429105720"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row141016118187"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p1990740105612"><a name="p1990740105612"></a><a name="p1990740105612"></a>rds064_latch_waits_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p110251114186"><a name="p110251114186"></a><a name="p110251114186"></a>每秒闩锁等待数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p21023112182"><a name="p21023112182"></a><a name="p21023112182"></a>该指标用于统计每秒未能立即授予的闩锁请求数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p11102191110184"><a name="p11102191110184"></a><a name="p11102191110184"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p69091629145713"><a name="p69091629145713"></a><a name="p69091629145713"></a>测量对象：数据库</p>
    <p id="p1890992911570"><a name="p1890992911570"></a><a name="p1890992911570"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p15909122913574"><a name="p15909122913574"></a><a name="p15909122913574"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row2102311121816"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p1299044010564"><a name="p1299044010564"></a><a name="p1299044010564"></a>rds065_lock_waits_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p010241141811"><a name="p010241141811"></a><a name="p010241141811"></a>每秒锁等待次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p71027112185"><a name="p71027112185"></a><a name="p71027112185"></a>该指标用于统计每秒要求调用者等待的锁请求数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p010271116189"><a name="p010271116189"></a><a name="p010271116189"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p79097299571"><a name="p79097299571"></a><a name="p79097299571"></a>测量对象：数据库</p>
    <p id="p189091129155715"><a name="p189091129155715"></a><a name="p189091129155715"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p290972914575"><a name="p290972914575"></a><a name="p290972914575"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row11102211181817"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p39901640135616"><a name="p39901640135616"></a><a name="p39901640135616"></a>rds066_lock_requests_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p0102411111813"><a name="p0102411111813"></a><a name="p0102411111813"></a>每秒锁请求次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p161021311171812"><a name="p161021311171812"></a><a name="p161021311171812"></a>该指标用于统计锁管理器每秒请求的新锁和锁转换数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p11102111121810"><a name="p11102111121810"></a><a name="p11102111121810"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p6909132935712"><a name="p6909132935712"></a><a name="p6909132935712"></a>测量对象：数据库</p>
    <p id="p7909182975715"><a name="p7909182975715"></a><a name="p7909182975715"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p490912975719"><a name="p490912975719"></a><a name="p490912975719"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row12102711141811"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p599024085616"><a name="p599024085616"></a><a name="p599024085616"></a>rds067_timeouts_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p11021611111820"><a name="p11021611111820"></a><a name="p11021611111820"></a>每秒锁超时次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p17102101141812"><a name="p17102101141812"></a><a name="p17102101141812"></a>该指标用于统计每秒超时的锁请求数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p14102161117189"><a name="p14102161117189"></a><a name="p14102161117189"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p1390932918574"><a name="p1390932918574"></a><a name="p1390932918574"></a>测量对象：数据库</p>
    <p id="p1990922935719"><a name="p1990922935719"></a><a name="p1990922935719"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p4909112913578"><a name="p4909112913578"></a><a name="p4909112913578"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row1810214110188"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p18990134045616"><a name="p18990134045616"></a><a name="p18990134045616"></a>rds068_avg_lock_wait_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p11102111121819"><a name="p11102111121819"></a><a name="p11102111121819"></a>平均锁等待延迟</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p1710281119184"><a name="p1710281119184"></a><a name="p1710281119184"></a>该指标用于统计每个导致等待的锁请求的平均等待时间（毫秒）。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p1510261191810"><a name="p1510261191810"></a><a name="p1510261191810"></a>≥0ms</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p990992925716"><a name="p990992925716"></a><a name="p990992925716"></a>测量对象：数据库</p>
    <p id="p1090952955712"><a name="p1090952955712"></a><a name="p1090952955712"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p179098293575"><a name="p179098293575"></a><a name="p179098293575"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row7102911191811"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p20990204011566"><a name="p20990204011566"></a><a name="p20990204011566"></a>rds069_deadlocks_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p1010216113186"><a name="p1010216113186"></a><a name="p1010216113186"></a>每秒死锁次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p710211161814"><a name="p710211161814"></a><a name="p710211161814"></a>该指标用于统计每秒导致死锁的锁请求数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p15102911131814"><a name="p15102911131814"></a><a name="p15102911131814"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p11909152918577"><a name="p11909152918577"></a><a name="p11909152918577"></a>测量对象：数据库</p>
    <p id="p1690922935710"><a name="p1690922935710"></a><a name="p1690922935710"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p990932915577"><a name="p990932915577"></a><a name="p990932915577"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row510241141815"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p399214408567"><a name="p399214408567"></a><a name="p399214408567"></a>rds070_checkpoint_pages_per_sec</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p18102181113189"><a name="p18102181113189"></a><a name="p18102181113189"></a>每秒检查点写入Page数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p510231151818"><a name="p510231151818"></a><a name="p510231151818"></a>该指标用于统计刷新所有脏页的检查点或其他操作每秒刷新到磁盘的页数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p21021011201820"><a name="p21021011201820"></a><a name="p21021011201820"></a>≥0counts/s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p1990932911575"><a name="p1990932911575"></a><a name="p1990932911575"></a>测量对象：数据库</p>
    <p id="p7909122915717"><a name="p7909122915717"></a><a name="p7909122915717"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p490962911570"><a name="p490962911570"></a><a name="p490962911570"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row8102161131812"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p499214401563"><a name="p499214401563"></a><a name="p499214401563"></a>rds077_replication_delay</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p208554469403"><a name="p208554469403"></a><a name="p208554469403"></a>数据同步延迟</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p91025111181"><a name="p91025111181"></a><a name="p91025111181"></a>该指标用于统计主备实例复制延迟，由于SQL Server实例复制延迟都是库级别，每个库各自都在做同步，所以实例级别复制延迟为复制延迟最大的库的值（单机不涉及都为0s）。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p1610212117185"><a name="p1610212117185"></a><a name="p1610212117185"></a>≥0s</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p1890932918576"><a name="p1890932918576"></a><a name="p1890932918576"></a>测量对象：数据库</p>
    <p id="p690919297574"><a name="p690919297574"></a><a name="p690919297574"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p89096297573"><a name="p89096297573"></a><a name="p89096297573"></a>1分钟</p>
    </td>
    </tr>
    <tr id="row11021211131813"><td class="cellrowborder" valign="top" width="20.169999999999998%" headers="mcps1.2.7.1.1 "><p id="p399274015567"><a name="p399274015567"></a><a name="p399274015567"></a>rds054_db_connections_in_use</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.08%" headers="mcps1.2.7.1.2 "><p id="p510218119182"><a name="p510218119182"></a><a name="p510218119182"></a>用户连接数</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.42%" headers="mcps1.2.7.1.3 "><p id="p1810321120185"><a name="p1810321120185"></a><a name="p1810321120185"></a>该指标用于统计当前SQL Server连接数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.7%" headers="mcps1.2.7.1.4 "><p id="p12103611121817"><a name="p12103611121817"></a><a name="p12103611121817"></a>≥0</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.2.7.1.5 "><p id="p1590992912577"><a name="p1590992912577"></a><a name="p1590992912577"></a>测量对象：数据库</p>
    <p id="p14909142965714"><a name="p14909142965714"></a><a name="p14909142965714"></a>监控实例类型：Microsoft SQL Server实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.649999999999999%" headers="mcps1.2.7.1.6 "><p id="p9909132912577"><a name="p9909132912577"></a><a name="p9909132912577"></a>1分钟</p>
    </td>
    </tr>
    </tbody>
    </table>


## 维度<a name="section0114351005"></a>

<a name="table20447661154756"></a>
<table><thead align="left"><tr id="row58418561154756"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p34282994154756"><a name="p34282994154756"></a><a name="p34282994154756"></a>Key</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p25459095154756"><a name="p25459095154756"></a><a name="p25459095154756"></a>Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row66237070144518"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p63602487144518"><a name="p63602487144518"></a><a name="p63602487144518"></a>rds_instance_sqlserver_id</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p51527828144518"><a name="p51527828144518"></a><a name="p51527828144518"></a>Microsoft SQL Server实例ID</p>
</td>
</tr>
</tbody>
</table>

