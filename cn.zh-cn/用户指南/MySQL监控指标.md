# 监控指标<a name="TOPIC_0142028286"></a>

-   弹性云服务器相关指标，如[表1](支持的监控指标.md#table2501556415126)所示。
-   数据库指标监控项，如[表1](#table43985037223835)所示。

    **表 1**  数据库性能监控列表

    <a name="table43985037223835"></a>
    <table><thead align="left"><tr id="row25689427223835"><th class="cellrowborder" valign="top" width="23.09%" id="mcps1.2.4.1.1"><p id="p468860223835"><a name="p468860223835"></a><a name="p468860223835"></a>指标名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.59%" id="mcps1.2.4.1.2"><p id="p6254701223835"><a name="p6254701223835"></a><a name="p6254701223835"></a>含义</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.32%" id="mcps1.2.4.1.3"><p id="p26374149144035"><a name="p26374149144035"></a><a name="p26374149144035"></a>取值范围</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row10406843223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p50464019155458"><a name="p50464019155458"></a><a name="p50464019155458"></a>数据库总连接数</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p61053772155458"><a name="p61053772155458"></a><a name="p61053772155458"></a>该指标用于统计试图连接到MySQL服务器的总连接数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p26949924144035"><a name="p26949924144035"></a><a name="p26949924144035"></a>≥0counts</p>
    </td>
    </tr>
    <tr id="row64943162223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p15023367155458"><a name="p15023367155458"></a><a name="p15023367155458"></a>当前活跃连接数</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p8933214155458"><a name="p8933214155458"></a><a name="p8933214155458"></a>该指标用于统计当前打开的连接的数量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p35460230144035"><a name="p35460230144035"></a><a name="p35460230144035"></a>≥0counts</p>
    </td>
    </tr>
    <tr id="row27006401223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p2753484155458"><a name="p2753484155458"></a><a name="p2753484155458"></a>QPS</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p21705627155458"><a name="p21705627155458"></a><a name="p21705627155458"></a>该指标用于统计平均每秒SQL语句查询次数，包含存储过程。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p53706368144035"><a name="p53706368144035"></a><a name="p53706368144035"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row60163003223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p52819295155458"><a name="p52819295155458"></a><a name="p52819295155458"></a>TPS</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p50504464155458"><a name="p50504464155458"></a><a name="p50504464155458"></a>该指标用于统计平均每秒事务执行次数，包含提交的和回退的。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p55248571144035"><a name="p55248571144035"></a><a name="p55248571144035"></a>≥0transactions/s</p>
    </td>
    </tr>
    <tr id="row23281439223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p42097092155458"><a name="p42097092155458"></a><a name="p42097092155458"></a>缓冲池利用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p54421330155458"><a name="p54421330155458"></a><a name="p54421330155458"></a>该指标用于统计InnoDB缓存中脏数据与数据比例。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p45949279144035"><a name="p45949279144035"></a><a name="p45949279144035"></a>0～1</p>
    </td>
    </tr>
    <tr id="row20645801223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p11811403155458"><a name="p11811403155458"></a><a name="p11811403155458"></a>缓冲池命中率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p17199550155458"><a name="p17199550155458"></a><a name="p17199550155458"></a>该指标用于统计读命中与读请求数比例。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p45863697151735"><a name="p45863697151735"></a><a name="p45863697151735"></a>0～1</p>
    </td>
    </tr>
    <tr id="row14303006223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p56223942155458"><a name="p56223942155458"></a><a name="p56223942155458"></a>缓冲池脏块率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p57845434155458"><a name="p57845434155458"></a><a name="p57845434155458"></a>该指标用于统计使用的页与InnoDB缓存中数据总数比例。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p8669853151737"><a name="p8669853151737"></a><a name="p8669853151737"></a>0～1</p>
    </td>
    </tr>
    <tr id="row13168267223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p24955091155458"><a name="p24955091155458"></a><a name="p24955091155458"></a>InnoDB读取吞吐量</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p8096497155458"><a name="p8096497155458"></a><a name="p8096497155458"></a>该指标用于统计Innodb平均每秒读字节数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p25810124144035"><a name="p25810124144035"></a><a name="p25810124144035"></a>≥0bytes/s</p>
    </td>
    </tr>
    <tr id="row49724805223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p63875864155458"><a name="p63875864155458"></a><a name="p63875864155458"></a>InnoDB写入吞吐量</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p6562458155458"><a name="p6562458155458"></a><a name="p6562458155458"></a>该指标用于统计Innodb平均每秒写字节数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p10245281144035"><a name="p10245281144035"></a><a name="p10245281144035"></a>≥0bytes/s</p>
    </td>
    </tr>
    <tr id="row53029737223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p19303040155458"><a name="p19303040155458"></a><a name="p19303040155458"></a>InnoDB文件读取频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p20042417155458"><a name="p20042417155458"></a><a name="p20042417155458"></a>该指标用于统计Innodb平均每秒从文件中读的次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p56490176151937"><a name="p56490176151937"></a><a name="p56490176151937"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row53402269223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p48298882155458"><a name="p48298882155458"></a><a name="p48298882155458"></a>InnoDB文件写入频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p19895355155458"><a name="p19895355155458"></a><a name="p19895355155458"></a>该指标用于统计Innodb平均每秒向文件中写的次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p54773733151939"><a name="p54773733151939"></a><a name="p54773733151939"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row39304652223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p8199514155458"><a name="p8199514155458"></a><a name="p8199514155458"></a>InnoDB日志写请求频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p60180869155458"><a name="p60180869155458"></a><a name="p60180869155458"></a>该指标用于统计平均每秒的日志写请求数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p37939841151942"><a name="p37939841151942"></a><a name="p37939841151942"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row7501613223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p49765709155458"><a name="p49765709155458"></a><a name="p49765709155458"></a>InnoDB日志物理写频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p4490596155458"><a name="p4490596155458"></a><a name="p4490596155458"></a>该指标用于统计平均每秒向日志文件的物理写次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p38575203151945"><a name="p38575203151945"></a><a name="p38575203151945"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row44284348223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p52419560155458"><a name="p52419560155458"></a><a name="p52419560155458"></a>InnoDB日志fsync()写频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p18125942155458"><a name="p18125942155458"></a><a name="p18125942155458"></a>该指标用于统计平均每秒向日志文件完成的fsync()写数量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p25287176151947"><a name="p25287176151947"></a><a name="p25287176151947"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row49609854223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p60474432155458"><a name="p60474432155458"></a><a name="p60474432155458"></a>临时表数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p66590814155458"><a name="p66590814155458"></a><a name="p66590814155458"></a>该指标用于统计MySQL执行语句时在硬盘上自动创建的临时表的数量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p19035156144035"><a name="p19035156144035"></a><a name="p19035156144035"></a>≥0tables</p>
    </td>
    </tr>
    <tr id="row43274176223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p24995122155458"><a name="p24995122155458"></a><a name="p24995122155458"></a>Key Buffer利用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p11339019155458"><a name="p11339019155458"></a><a name="p11339019155458"></a>该指标用于统计MyISAM Key buffer的利用率。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p65452677144035"><a name="p65452677144035"></a><a name="p65452677144035"></a>0～1</p>
    </td>
    </tr>
    <tr id="row59745367223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p11754660155458"><a name="p11754660155458"></a><a name="p11754660155458"></a>Key Buffer写命中率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p12603376155458"><a name="p12603376155458"></a><a name="p12603376155458"></a>该指标用于统计MyISAM Key buffer写命中率。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p66622144035"><a name="p66622144035"></a><a name="p66622144035"></a>0～1</p>
    </td>
    </tr>
    <tr id="row58348769223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p61056193155458"><a name="p61056193155458"></a><a name="p61056193155458"></a>Key Buffer读命中率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p46604620155458"><a name="p46604620155458"></a><a name="p46604620155458"></a>该指标用于统计MyISAM Key buffer读命中率。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p5396456144035"><a name="p5396456144035"></a><a name="p5396456144035"></a>0～1</p>
    </td>
    </tr>
    <tr id="row278785223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p17683264155458"><a name="p17683264155458"></a><a name="p17683264155458"></a>MyISAM硬盘写入频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p23058275155458"><a name="p23058275155458"></a><a name="p23058275155458"></a>该指标用于统计平均每秒向磁盘写入索引的次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p34459819144035"><a name="p34459819144035"></a><a name="p34459819144035"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row20335270223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p32266909155458"><a name="p32266909155458"></a><a name="p32266909155458"></a>MyISAM硬盘读取频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p63482818155458"><a name="p63482818155458"></a><a name="p63482818155458"></a>该指标用于统计平均每秒从磁盘读取索引的次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p39781934144035"><a name="p39781934144035"></a><a name="p39781934144035"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row65570115223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p40967517155458"><a name="p40967517155458"></a><a name="p40967517155458"></a>MyISAM缓冲池写入频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p30034558155458"><a name="p30034558155458"></a><a name="p30034558155458"></a>该指标用于统计平均每秒向缓冲池写入索引的请求次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p1111193144035"><a name="p1111193144035"></a><a name="p1111193144035"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row3860247223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p17703757155458"><a name="p17703757155458"></a><a name="p17703757155458"></a>MyISAM缓冲池读取频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p24718197155458"><a name="p24718197155458"></a><a name="p24718197155458"></a>该指标用于统计平均每秒从缓冲池读取索引的请求次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p22897813144035"><a name="p22897813144035"></a><a name="p22897813144035"></a>≥0counts/s</p>
    </td>
    </tr>
    <tr id="row42060902223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p34390210155458"><a name="p34390210155458"></a><a name="p34390210155458"></a>Delete语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p34143626155458"><a name="p34143626155458"></a><a name="p34143626155458"></a>该指标用于统计平均每秒Delete语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p42783561144035"><a name="p42783561144035"></a><a name="p42783561144035"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row22289597223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p60424153155458"><a name="p60424153155458"></a><a name="p60424153155458"></a>Insert语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p62518252155458"><a name="p62518252155458"></a><a name="p62518252155458"></a>该指标用于统计平均每秒Insert语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p42916446144035"><a name="p42916446144035"></a><a name="p42916446144035"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row39412273223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p8887224155458"><a name="p8887224155458"></a><a name="p8887224155458"></a>Insert_Select语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p48776526155458"><a name="p48776526155458"></a><a name="p48776526155458"></a>该指标用于统计平均每秒Insert_Select语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p53680124144035"><a name="p53680124144035"></a><a name="p53680124144035"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row54174368223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p57499082155458"><a name="p57499082155458"></a><a name="p57499082155458"></a>Replace语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p26914095155458"><a name="p26914095155458"></a><a name="p26914095155458"></a>该指标用于统计平均每秒Replace语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p53122762144035"><a name="p53122762144035"></a><a name="p53122762144035"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row64047853223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p24587526155458"><a name="p24587526155458"></a><a name="p24587526155458"></a>Replace_Selection语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p45432595155458"><a name="p45432595155458"></a><a name="p45432595155458"></a>该指标用于统计平均每秒Replace_Selection语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p7976432144035"><a name="p7976432144035"></a><a name="p7976432144035"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row41679943223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p35692328155458"><a name="p35692328155458"></a><a name="p35692328155458"></a>Select语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p5397447155458"><a name="p5397447155458"></a><a name="p5397447155458"></a>该指标用于统计平均每秒Select语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p41783202152527"><a name="p41783202152527"></a><a name="p41783202152527"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row8489825223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p42425333155458"><a name="p42425333155458"></a><a name="p42425333155458"></a>Update语句执行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p13899937155458"><a name="p13899937155458"></a><a name="p13899937155458"></a>该指标用于统计平均每秒Update语句执行次数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p28275581152531"><a name="p28275581152531"></a><a name="p28275581152531"></a>≥0queries/s</p>
    </td>
    </tr>
    <tr id="row12517818223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p66724474155458"><a name="p66724474155458"></a><a name="p66724474155458"></a>行删除速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p35973308155458"><a name="p35973308155458"></a><a name="p35973308155458"></a>该指标用于统计平均每秒从InnoDB表删除的行数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p22422197152538"><a name="p22422197152538"></a><a name="p22422197152538"></a>≥0rows/s</p>
    </td>
    </tr>
    <tr id="row27652310223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p52084812155458"><a name="p52084812155458"></a><a name="p52084812155458"></a>行插入速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p58120254155458"><a name="p58120254155458"></a><a name="p58120254155458"></a>该指标用于统计平均每秒向InnoDB表插入的行数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p13942312152541"><a name="p13942312152541"></a><a name="p13942312152541"></a>≥0rows/s</p>
    </td>
    </tr>
    <tr id="row15525762223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p23972552155458"><a name="p23972552155458"></a><a name="p23972552155458"></a>行读取速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p62728597155458"><a name="p62728597155458"></a><a name="p62728597155458"></a>该指标用于统计平均每秒从InnoDB表读取的行数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p17903033152543"><a name="p17903033152543"></a><a name="p17903033152543"></a>≥0rows/s</p>
    </td>
    </tr>
    <tr id="row6576404223835"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p28011092155458"><a name="p28011092155458"></a><a name="p28011092155458"></a>行更新速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p54305973155458"><a name="p54305973155458"></a><a name="p54305973155458"></a>该指标用于统计平均每秒向InnoDB表更新的行数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p65416599152545"><a name="p65416599152545"></a><a name="p65416599152545"></a>≥0rows/s</p>
    </td>
    </tr>
    <tr id="row146627554447"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p11791172473715"><a name="p11791172473715"></a><a name="p11791172473715"></a>连接数使用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p14791224123719"><a name="p14791224123719"></a><a name="p14791224123719"></a>该指标用于统计当前已用的MySQL连接数占总连接数的百分比。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p76871531184"><a name="p76871531184"></a><a name="p76871531184"></a>0~100%</p>
    </td>
    </tr>
    <tr id="row1346295944410"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p13441112711377"><a name="p13441112711377"></a><a name="p13441112711377"></a>复制时延</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p1144152793720"><a name="p1144152793720"></a><a name="p1144152793720"></a>该指标用户展示MySQL主从关系中，从节点的数据复制时延。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p184415276375"><a name="p184415276375"></a><a name="p184415276375"></a>≥0Seconds</p>
    </td>
    </tr>
    <tr id="row1172514284517"><td class="cellrowborder" valign="top" width="23.09%" headers="mcps1.2.4.1.1 "><p id="p9891330173716"><a name="p9891330173716"></a><a name="p9891330173716"></a>慢日志个数统计</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.59%" headers="mcps1.2.4.1.2 "><p id="p168921306379"><a name="p168921306379"></a><a name="p168921306379"></a>该指标展示每分钟MySQL产生慢日志的数量。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.32%" headers="mcps1.2.4.1.3 "><p id="p1289210305371"><a name="p1289210305371"></a><a name="p1289210305371"></a>≥Counts/Minute</p>
    </td>
    </tr>
    </tbody>
    </table>


