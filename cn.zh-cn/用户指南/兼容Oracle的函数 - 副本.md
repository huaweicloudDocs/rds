# 兼容Oracle的函数<a name="rds_04_0002"></a>

本章节介绍了在PostgreSQL11开源版本的基础上，PostgreSQL增强版新增兼容Oracle  12c的内置函数和高级函数包。

**表 1**  内置函数

<a name="table46646518463"></a>
<table><thead align="left"><tr id="row16664195115466"><th class="cellrowborder" valign="top" width="40.43%" id="mcps1.2.3.1.1"><p id="p1366495117466"><a name="p1366495117466"></a><a name="p1366495117466"></a>内置函数</p>
</th>
<th class="cellrowborder" valign="top" width="59.57%" id="mcps1.2.3.1.2"><p id="p16664175184617"><a name="p16664175184617"></a><a name="p16664175184617"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1582205304811"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p94281947195913"><a name="p94281947195913"></a><a name="p94281947195913"></a>add_months(date,integer)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1282265394812"><a name="p1282265394812"></a><a name="p1282265394812"></a>返回date加上integer的值，返回值为DATE类型。</p>
</td>
</tr>
<tr id="row9434129165913"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p64343925919"><a name="p64343925919"></a><a name="p64343925919"></a>appendchildxml(XMLType_instance, XPath_string, value_expr[, namespace_string])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1043429145916"><a name="p1043429145916"></a><a name="p1043429145916"></a>在XMLType类型数据XMLType_instance指定位置XPath_string处追加value_expr节点，其中namespace_string用于描述XPath_string的命名空间信息。</p>
</td>
</tr>
<tr id="row5983329165019"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p398316290501"><a name="p398316290501"></a><a name="p398316290501"></a>asciistr(string)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p498342918508"><a name="p498342918508"></a><a name="p498342918508"></a>返回给定字符串string对应的ASCII值，不支持非ASCII字符。</p>
</td>
</tr>
<tr id="row153801052145015"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p638019529509"><a name="p638019529509"></a><a name="p638019529509"></a>bin_to_num(expr_list)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p93800523506"><a name="p93800523506"></a><a name="p93800523506"></a>将expr_list中的二进制串转换为对应的十进制数，返回值类型为NUMBER。</p>
</td>
</tr>
<tr id="row106642051184611"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1455118219522"><a name="p1455118219522"></a><a name="p1455118219522"></a>bitand(number1,number2)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p17551621145217"><a name="p17551621145217"></a><a name="p17551621145217"></a>返回number1和number2按位与的值，返回值为BIT类型。</p>
</td>
</tr>
<tr id="row796116112512"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p14961642515"><a name="p14961642515"></a><a name="p14961642515"></a>convert(char, dest_char_set[, source_char_set])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p11829612112517"><a name="p11829612112517"></a><a name="p11829612112517"></a>将source_char_set字符集编码格式的输入字符串char，转换为dest_char_set字符集编码格式，该函数只在服务端生效。</p>
</td>
</tr>
<tr id="row15854161711315"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1585411178315"><a name="p1585411178315"></a><a name="p1585411178315"></a>cosh(n)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p118540171334"><a name="p118540171334"></a><a name="p118540171334"></a>返回参数n的双曲余弦值；</p>
</td>
</tr>
<tr id="row46646515468"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p48532515567"><a name="p48532515567"></a><a name="p48532515567"></a>decode(expr,search1, result1[[,search2, result2],......][, default])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1466425194616"><a name="p1466425194616"></a><a name="p1466425194616"></a>将expr表达式值依次与所有search表达式（search1，search2......）进行比较，如果与searchn进行匹配，则返回resultn，否则返回default。如果没有default，返回null。</p>
</td>
</tr>
<tr id="row1466435104615"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p119343213562"><a name="p119343213562"></a><a name="p119343213562"></a>empty_blob()</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p5664195111465"><a name="p5664195111465"></a><a name="p5664195111465"></a>返回一个空BLOB类型。</p>
</td>
</tr>
<tr id="row666415112466"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p8136101813562"><a name="p8136101813562"></a><a name="p8136101813562"></a>hextoraw(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p186641151204618"><a name="p186641151204618"></a><a name="p186641151204618"></a>将十六进制字符串转换为RAW类型的值。</p>
</td>
</tr>
<tr id="row11835123104714"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1283514313471"><a name="p1283514313471"></a><a name="p1283514313471"></a>instrb(string, substring[, position[, occurrence]])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p28352313477"><a name="p28352313477"></a><a name="p28352313477"></a>返回从字符string的第position位置开始，第occurrence次出现的子串substring起始位置，默认从字符串string首部开始第一次出现的位置。</p>
</td>
</tr>
<tr id="row2664105104611"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p169641814155619"><a name="p169641814155619"></a><a name="p169641814155619"></a>last_day(date)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1066413516469"><a name="p1066413516469"></a><a name="p1066413516469"></a>返回date所在月的最后一天。</p>
</td>
</tr>
<tr id="row1666465117467"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p7395180311"><a name="p7395180311"></a><a name="p7395180311"></a>lengthb(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p8664155184610"><a name="p8664155184610"></a><a name="p8664155184610"></a>返回char字符的字节长度，char支持的类型为所有字符串类型（如CHAR, VARCHAR2, NCHAR, NVARCHAR2等）或可隐式转换为字符串的类型（如integer等）。</p>
</td>
</tr>
<tr id="row45531930505"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1155415301202"><a name="p1155415301202"></a><a name="p1155415301202"></a>listagg(measure_expr[, 'delimiter']) within group(order_by_clause) [over query_partition_clause]</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p14554103015015"><a name="p14554103015015"></a><a name="p14554103015015"></a>将query_partition_clause分组中的每个列表达式measure_expr值按order_by_clause规则排序后，再合并成一行，值之间使用delimiter分隔符进行分割。</p>
</td>
</tr>
<tr id="row20958513135119"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p189586132518"><a name="p189586132518"></a><a name="p189586132518"></a>lnnvl(condition)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1395871310513"><a name="p1395871310513"></a><a name="p1395871310513"></a>返回条件表达式condition的取反值，返回类型为BOOLEAN。</p>
</td>
</tr>
<tr id="row153905360517"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p2390123614511"><a name="p2390123614511"></a><a name="p2390123614511"></a>mod(n2, n1)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p113902036158"><a name="p113902036158"></a><a name="p113902036158"></a>支持除数为0的情况，即当n1为0时，直接返回n2。</p>
</td>
</tr>
<tr id="row154331469523"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p143394612524"><a name="p143394612524"></a><a name="p143394612524"></a>months_between(date1, date2)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p5433846195218"><a name="p5433846195218"></a><a name="p5433846195218"></a>返回date1与date2之间相差的月数，当date2早于date1，返回值为负数。</p>
</td>
</tr>
<tr id="row8880133017515"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1288093065118"><a name="p1288093065118"></a><a name="p1288093065118"></a>nanvl(n2, n1)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p98801304515"><a name="p98801304515"></a><a name="p98801304515"></a>当单精度或双精度浮点数n2的值为NAN，则返回n1，否则返回n2。</p>
</td>
</tr>
<tr id="row581074710449"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p18810144718448"><a name="p18810144718448"></a><a name="p18810144718448"></a>nchr(number)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1281012478449"><a name="p1281012478449"></a><a name="p1281012478449"></a>返回本地字符集中二进制与number相等的字符。</p>
</td>
</tr>
<tr id="row8167135411512"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1216725495117"><a name="p1216725495117"></a><a name="p1216725495117"></a>new_time(date, timezone1, timezone2)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p111675547512"><a name="p111675547512"></a><a name="p111675547512"></a>返回timezone1的date时间对应的timezone2的时间，返回值类型为DATE。</p>
</td>
</tr>
<tr id="row1642914815526"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p58635171256"><a name="p58635171256"></a><a name="p58635171256"></a>next_day(date, char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p457511531532"><a name="p457511531532"></a><a name="p457511531532"></a>返回date后的第一个自然日（包括工作日、休息日和节假日），返回值为DATE类型。</p>
</td>
</tr>
<tr id="row8791138482"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p479830487"><a name="p479830487"></a><a name="p479830487"></a>numtodsinterval(n, interval_unit)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p72503974820"><a name="p72503974820"></a><a name="p72503974820"></a>根据INTERVAL数据类型单元interval_unit（取值范围：'DAY'、'HOUR'、'MINUTE'、'SECOND'），将数字n转换为数据类型INTERVAL DAY TO SECOND。</p>
</td>
</tr>
<tr id="row237422020207"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p103758205204"><a name="p103758205204"></a><a name="p103758205204"></a>numtoyminterval(n, 'interval_unit')</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p2375102012202"><a name="p2375102012202"></a><a name="p2375102012202"></a>将数字n按照指定单位interval_unit转为数据类型INTERVAL YEAR TO MONTH，其中interval_unit取值为：YEAR、MONTH。</p>
</td>
</tr>
<tr id="row13210301848"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1429301143"><a name="p1429301143"></a><a name="p1429301143"></a>nlssort(char[, nlsparam])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p202730148"><a name="p202730148"></a><a name="p202730148"></a>按照nlsparam指定的排序字符集对字符串char进行排序，默认使用char字符串字符集排序；</p>
</td>
</tr>
<tr id="row199880121313"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1898861210111"><a name="p1898861210111"></a><a name="p1898861210111"></a>nls_upper(char[, nlsparam])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p2098881210114"><a name="p2098881210114"></a><a name="p2098881210114"></a>根据nlsparam指定的排序规则将字符串char中的字母转换为大写，其中char字符串类型为CHAR, VARCHAR2, NCHAR, NVARCHAR2,CLOB或NCLOB，nlsparam的取值为'NLS_SORT = sort'。</p>
</td>
</tr>
<tr id="row1375417152014"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p37549152114"><a name="p37549152114"></a><a name="p37549152114"></a>nls_lower(char[, nlsparam])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p575410151119"><a name="p575410151119"></a><a name="p575410151119"></a>根据nlsparam指定的排序规则将字符串char中的字母转换为小写，其中char字符串类型为CHAR, VARCHAR2, NCHAR, NVARCHAR2,CLOB或NCLOB，nlsparam的取值为'NLS_SORT = sort'。</p>
</td>
</tr>
<tr id="row857665913517"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p2799174411318"><a name="p2799174411318"></a><a name="p2799174411318"></a>nvl(expr1, expr2)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p20576259195119"><a name="p20576259195119"></a><a name="p20576259195119"></a>返回expr1, expr2中第一个非空值。</p>
</td>
</tr>
<tr id="row18422853145011"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p204227532506"><a name="p204227532506"></a><a name="p204227532506"></a>rawtohex(raw)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1442215537504"><a name="p1442215537504"></a><a name="p1442215537504"></a>将RAW类型的值转换为十六进制字符串。</p>
</td>
</tr>
<tr id="row11808724195213"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1580822420524"><a name="p1580822420524"></a><a name="p1580822420524"></a>regexp_count(source_char, pattern, position, match_param)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p880813247524"><a name="p880813247524"></a><a name="p880813247524"></a>返回指定字符串source_char中的指定位置position开始，匹配正则表达式模式pattern的次数。其中，match_param参数会影响正则表达式匹配规则，比如match_param='i'忽略大小写等。</p>
</td>
</tr>
<tr id="row2876151415436"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p387671414435"><a name="p387671414435"></a><a name="p387671414435"></a>regexp_instr(source_char, pattern[, position[, occurrence[, return_opt[, match_param[, subexpr]]]]])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p726753584411"><a name="p726753584411"></a><a name="p726753584411"></a>该函数拓展了INSTR函数的功能，允许使用正则表达式匹配，返回值类型为INTEGER。</p>
<a name="ul2610121664515"></a><a name="ul2610121664515"></a><ul id="ul2610121664515"><li>position表示查找起始位置。</li><li>occurrence表示查找pattern在source_char的第几次出现。</li><li>return_opt：<a name="ul19875117134612"></a><a name="ul19875117134612"></a><ul id="ul19875117134612"><li>取值为0表示返回模式匹配的起始位置。</li><li>取值为1表示返回模式匹配的结束位置。</li></ul>
</li><li>match_param表示正则表达式模式匹配控制参数，如区分大小写等。</li><li>subexpr表示正则表达式分组匹配的组号。</li></ul>
</td>
</tr>
<tr id="row182531812194615"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p52531121462"><a name="p52531121462"></a><a name="p52531121462"></a>regexp_like(source_char, pattern[,match_param])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p2253191211463"><a name="p2253191211463"></a><a name="p2253191211463"></a>source_char为字符串表达式，pattern为正则表达式，match_param为正则表达式控制参数，返回字符串source_char是否可按照正则表达式pattern进行匹配。</p>
</td>
</tr>
<tr id="row031394817507"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1313164855016"><a name="p1313164855016"></a><a name="p1313164855016"></a>regexp_substr(source_char, pattern[,position[,occurrence[,match_param[,subexpr]]]])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p2052335019918"><a name="p2052335019918"></a><a name="p2052335019918"></a>按正则表达式在source_char字符串中匹配子字符串。</p>
<a name="ul98616536920"></a><a name="ul98616536920"></a><ul id="ul98616536920"><li>source_char为查找的输入字符串，支持所有字符串类型（如CHAR, VARCHAR2, NCHAR, NVARCHAR2等）或可隐式转换为字符串的类型（如integer等）。</li><li>pattern为子字符串匹配的正则表达式。</li><li>position为指定匹配的起始字符位置。</li><li>occurrence为pattern在source_char出现的次数。</li><li>match_parameter为正则表达式控制参数。</li><li>subexpr为pattern的第几个子表达式，范围为0~9。</li></ul>
</td>
</tr>
<tr id="row1180015462299"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p8800846112912"><a name="p8800846112912"></a><a name="p8800846112912"></a>raise_application_error(errnum, errmsg)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p68831532299"><a name="p68831532299"></a><a name="p68831532299"></a>将错误码errnum与错误消息errmsg输出到客户端。</p>
</td>
</tr>
<tr id="row3184175215417"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p8184115218543"><a name="p8184115218543"></a><a name="p8184115218543"></a>remainder(n2, n1)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p118413524545"><a name="p118413524545"></a><a name="p118413524545"></a>返回n2/n1的余数，类似于mod，区别在于，mod取余时用了floor处理，而remainder使用round处理。返回值类型为NUMERIC或双精度浮点数（由入参类型决定）。</p>
</td>
</tr>
<tr id="row1968906183914"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p176891161396"><a name="p176891161396"></a><a name="p176891161396"></a>round(date, fmt)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1951914193910"><a name="p1951914193910"></a><a name="p1951914193910"></a>按照fmt指定的日期格式对date进行四舍五入处理，返回值类型为DATE。如果省略fmt，则返回最近的一天。</p>
</td>
</tr>
<tr id="row1166475116468"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p366415104613"><a name="p366415104613"></a><a name="p366415104613"></a>round(n,precision)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p183387439118"><a name="p183387439118"></a><a name="p183387439118"></a>返回n的四舍五入值，precision为精度值。</p>
</td>
</tr>
<tr id="row35718134511"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1658121310514"><a name="p1658121310514"></a><a name="p1658121310514"></a>scn_to_timestamp(number)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p05841313520"><a name="p05841313520"></a><a name="p05841313520"></a>返回SCN号number产生的最近时间戳；</p>
</td>
</tr>
<tr id="row990056172416"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p790015618245"><a name="p790015618245"></a><a name="p790015618245"></a>sinh(n)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1933961592414"><a name="p1933961592414"></a><a name="p1933961592414"></a>返回数字n的双曲正弦值，当n类型为BINARY_FLOAT，返回类型BINARY_DOUBLE，否则返回值类型为NUMERIC。</p>
</td>
</tr>
<tr id="row1460061705015"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p132858251117"><a name="p132858251117"></a><a name="p132858251117"></a>substr(char,position[,substring_length])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p560041714506"><a name="p560041714506"></a><a name="p560041714506"></a>返回char字符串中第position个字符开始，长度为substring_length的子字符串。若不指定substring_length，则截取到字符串结尾。</p>
</td>
</tr>
<tr id="row360982635810"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1660982655814"><a name="p1660982655814"></a><a name="p1660982655814"></a>substrb(char, position[, substring_length])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1360919264582"><a name="p1360919264582"></a><a name="p1360919264582"></a>返回char字符串中第position个字节开始，长度为substring_length字节的子字符串。若不指定substring_length，则截取到字符串结尾。</p>
</td>
</tr>
<tr id="row12301755134920"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1730165514915"><a name="p1730165514915"></a><a name="p1730165514915"></a>sys_context(namespace, parameter)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1330155584917"><a name="p1330155584917"></a><a name="p1330155584917"></a>返回指定参数parameter在命名空间namespace下的值，返回值类型为VARCHAR2。</p>
</td>
</tr>
<tr id="row4486104413458"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p54861144144515"><a name="p54861144144515"></a><a name="p54861144144515"></a>sys_guid()</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p11486144114513"><a name="p11486144114513"></a><a name="p11486144114513"></a>返回RAW类型的全局唯一标识。</p>
</td>
</tr>
<tr id="row115571450856"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p14557125016520"><a name="p14557125016520"></a><a name="p14557125016520"></a>sys_connect_by_path(column, char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p11557150452"><a name="p11557150452"></a><a name="p11557150452"></a>仅适用于CONNECT BY查询，返回column列的根节点；</p>
</td>
</tr>
<tr id="row17440251666"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p114482518619"><a name="p114482518619"></a><a name="p114482518619"></a>tanh(n)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p124410251868"><a name="p124410251868"></a><a name="p124410251868"></a>返回参数n的双曲正切值；</p>
</td>
</tr>
<tr id="row1364151216518"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p664181225118"><a name="p664181225118"></a><a name="p664181225118"></a>to_blob(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1064151220515"><a name="p1064151220515"></a><a name="p1064151220515"></a>将char字符串转换为BLOB类型，char支持的类型为所有字符串类型（如CHAR, VARCHAR2, NCHAR, NVARCHAR2等）或可隐式转换为字符串的类型（如integer等）。</p>
</td>
</tr>
<tr id="row13192142614"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p128827311266"><a name="p128827311266"></a><a name="p128827311266"></a>to_binary_float(expr)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p11321427264"><a name="p11321427264"></a><a name="p11321427264"></a>将数字字符串expr转换为单精度float类型。</p>
</td>
</tr>
<tr id="row1077712616264"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1477817616261"><a name="p1477817616261"></a><a name="p1477817616261"></a>to_binary_double(expr)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p9778176182612"><a name="p9778176182612"></a><a name="p9778176182612"></a>将数字字符串expr转换为双精度float类型。</p>
</td>
</tr>
<tr id="row1453272712114"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1453314276217"><a name="p1453314276217"></a><a name="p1453314276217"></a>to_clob(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p9260134252117"><a name="p9260134252117"></a><a name="p9260134252117"></a>将char字符串转换为CLOB数据类型。</p>
</td>
</tr>
<tr id="row205711423274"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p014462720313"><a name="p014462720313"></a><a name="p014462720313"></a>to_char(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p18513423165115"><a name="p18513423165115"></a><a name="p18513423165115"></a>增加char支持的类型：char、character、varchar。</p>
</td>
</tr>
<tr id="row174501628125113"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1450102835117"><a name="p1450102835117"></a><a name="p1450102835117"></a>to_date(char[,fmt])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p11450182811519"><a name="p11450182811519"></a><a name="p11450182811519"></a>将char时间字符串按照fmt格式转换为date数据类型，char支持的类型有CHAR、VARCHAR2、NCHAR、 NVARCHAR2、TIMESTAMP。如果省略fmt，则char必须采用DATE数据类型的默认格式。</p>
</td>
</tr>
<tr id="row925111182714"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p9251311102713"><a name="p9251311102713"></a><a name="p9251311102713"></a>to_dsinterval('sql_format' | 'ds_iso_format')</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1920882772717"><a name="p1920882772717"></a><a name="p1920882772717"></a>将SQL标准（如'100 00:00:00'）或ISO标准（如'P100DT05H'）的时间字符串转换为数据类型INTERVAL DAY TO SECOND。</p>
</td>
</tr>
<tr id="row3458853114611"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p84591053164618"><a name="p84591053164618"></a><a name="p84591053164618"></a>to_multi_byte(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p17459155314465"><a name="p17459155314465"></a><a name="p17459155314465"></a>将单字节字符char转换成对应的多字节字符。</p>
</td>
</tr>
<tr id="row19654181819451"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p265461817459"><a name="p265461817459"></a><a name="p265461817459"></a>to_number(expr)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p2065412184457"><a name="p2065412184457"></a><a name="p2065412184457"></a>将expr表达式值转换为number类型。</p>
</td>
</tr>
<tr id="row671111181304"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p5164152093010"><a name="p5164152093010"></a><a name="p5164152093010"></a>to_number(expr, fmt, 'nlsparam')</p>
<p id="p516420205308"><a name="p516420205308"></a><a name="p516420205308"></a></p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p371191863014"><a name="p371191863014"></a><a name="p371191863014"></a>按照指定格式fmt转换expr字符串为数字，返回类型为NUMBER，其中nlsparam为国际化语言参数，支持的参数分别为：NLS_NUMERIC_CHARACTERS、NLS_CURRENCY、NLS_ISO_CURRENCY。</p>
</td>
</tr>
<tr id="row87466461785"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p15746646488"><a name="p15746646488"></a><a name="p15746646488"></a>to_timestamp(char[,fmt])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p458441091415"><a name="p458441091415"></a><a name="p458441091415"></a>将char时间字符串按照fmt格式转换为timestamp数据类型，char支持的类型有CHAR、VARCHAR2、NCHAR、 NVARCHAR2、TIMESTAMP。如果省略fmt，则char必须采用TIMESTAMP数据类型的默认格式。</p>
</td>
</tr>
<tr id="row198471556172818"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1086818113234"><a name="p1086818113234"></a><a name="p1086818113234"></a>to_single_byte(char)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p18868141112311"><a name="p18868141112311"></a><a name="p18868141112311"></a>将多字节输入字符串转换为单字节字符串。</p>
</td>
</tr>
<tr id="row52958317285"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p629513152817"><a name="p629513152817"></a><a name="p629513152817"></a>to_yminterval('sql_format' | 'ym_iso_format')</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p102954317286"><a name="p102954317286"></a><a name="p102954317286"></a>将SQL标准(如'01-02')或ISO标准（如'P1Y2M'）的时间字符串转换为数据类型INTERVAL MONTH TO YEAR。</p>
</td>
</tr>
<tr id="row18662145715618"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p19662157665"><a name="p19662157665"></a><a name="p19662157665"></a>timestamp_to_scn(timestamp)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p1266255713612"><a name="p1266255713612"></a><a name="p1266255713612"></a>根据时间戳timestamp返回系统变更号SCN；</p>
</td>
</tr>
<tr id="row94075233820"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p240717215386"><a name="p240717215386"></a><a name="p240717215386"></a>trunc(date[, fmt])</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p32351891389"><a name="p32351891389"></a><a name="p32351891389"></a>按照fmt指定的日期格式对date进行截断处理，返回值类型为DATE。如果省略fmt，则默认日期格式为'DDD'。</p>
</td>
</tr>
<tr id="row5922959154613"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p129221159144613"><a name="p129221159144613"></a><a name="p129221159144613"></a>tz_offset({time_zone_name | '{+|-}hh:mi'})</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p9922195914464"><a name="p9922195914464"></a><a name="p9922195914464"></a>返回指定时区的偏移量，返回值类型VARCHAR2，参数可以是时区名time_zone_name或者'{+|-}hh:mi'格式字符串。</p>
</td>
</tr>
<tr id="row1346184111476"><td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.3.1.1 "><p id="p1461241124719"><a name="p1461241124719"></a><a name="p1461241124719"></a>value(correlation_variable)</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.3.1.2 "><p id="p3461144124711"><a name="p3461144124711"></a><a name="p3461144124711"></a>以对象表的方式返回correlation_variable所关联标的记录行，返回类型为correlation_variable所关联的对象表。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  兼容Oracle的高级函数包

<a name="table14545131315401"></a>
<table><thead align="left"><tr id="row65451313154018"><th class="cellrowborder" valign="top" width="42.54%" id="mcps1.2.3.1.1"><p id="p115451313104019"><a name="p115451313104019"></a><a name="p115451313104019"></a>高级函数包</p>
</th>
<th class="cellrowborder" valign="top" width="57.46%" id="mcps1.2.3.1.2"><p id="p12545101313400"><a name="p12545101313400"></a><a name="p12545101313400"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row14545201312403"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p1453292714409"><a name="p1453292714409"></a><a name="p1453292714409"></a>DBMS_OUTPUT.PUT(item)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p1753252716403"><a name="p1753252716403"></a><a name="p1753252716403"></a>将item字符串放入本地缓冲区；item为所有可以转换为字符串的类型。</p>
</td>
</tr>
<tr id="row0545101314017"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p2053292774019"><a name="p2053292774019"></a><a name="p2053292774019"></a>DBMS_OUTPUT.PUT_LINE(item)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p75321227134011"><a name="p75321227134011"></a><a name="p75321227134011"></a>将item字符串放入本地缓冲区，然后将整个本地缓冲区的内容整体输出；item为所有可以转换为字符串的类型。</p>
</td>
</tr>
<tr id="row354517136409"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p7516122711409"><a name="p7516122711409"></a><a name="p7516122711409"></a>DBMS_RANDOM.SEED(val)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p12516112794016"><a name="p12516112794016"></a><a name="p12516112794016"></a>val为生成随机数的种子，可为字符串和数字类型。</p>
</td>
</tr>
<tr id="row12561141364018"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p165782049164016"><a name="p165782049164016"></a><a name="p165782049164016"></a>DBMS_RANDOM.VALUE([low,high])</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p8578134913409"><a name="p8578134913409"></a><a name="p8578134913409"></a>返回low和high之间长度为16位的随机数，如果不指定low和high的范围，则默认范围为0~1。</p>
</td>
</tr>
<tr id="row179311473719"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p1793847679"><a name="p1793847679"></a><a name="p1793847679"></a>dbms_lob.getlength(lob_loc {clob|blob})</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p179318471379"><a name="p179318471379"></a><a name="p179318471379"></a>返回lob_loc指定的LOB对象长度；</p>
</td>
</tr>
<tr id="row149890442717"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p16989134420714"><a name="p16989134420714"></a><a name="p16989134420714"></a>dbms_lob.read(lob_loc, amount, offset, buffer)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p29891244973"><a name="p29891244973"></a><a name="p29891244973"></a>从指定偏移offset读取LOB对象lob_loc指定长度amount的内容写入缓冲区buffer；</p>
</td>
</tr>
<tr id="row8414115811213"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p1841410582219"><a name="p1841410582219"></a><a name="p1841410582219"></a>dbms_lob.write(lob_loc, amount, offset, buffer)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p2414165815216"><a name="p2414165815216"></a><a name="p2414165815216"></a>将buffer缓冲器的内容写入大对象lob_loc缓冲区（并不影响所引用的大对象），从offset开始写入长度为amount。</p>
</td>
</tr>
<tr id="row9143936834"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p31431336432"><a name="p31431336432"></a><a name="p31431336432"></a>utl_raw.cast_to_raw(char)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p1881511401132"><a name="p1881511401132"></a><a name="p1881511401132"></a>将VARCHAR2类型字符串char转换为RAW类型，返回值类型为RAW。</p>
</td>
</tr>
<tr id="row6784101213315"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p878419121736"><a name="p878419121736"></a><a name="p878419121736"></a>utl_raw.length(raw)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p15487141815310"><a name="p15487141815310"></a><a name="p15487141815310"></a>返回raw数据类型的字节长度，返回值类型为NUMBER。</p>
</td>
</tr>
<tr id="row13269103530"><td class="cellrowborder" valign="top" width="42.54%" headers="mcps1.2.3.1.1 "><p id="p16269123634"><a name="p16269123634"></a><a name="p16269123634"></a>utl_raw.cast_from_binary_integer(n, endianess)</p>
</td>
<td class="cellrowborder" valign="top" width="57.46%" headers="mcps1.2.3.1.2 "><p id="p188551441412"><a name="p188551441412"></a><a name="p188551441412"></a>按照endianess指定的内存对齐方式将整数n转换为RAW类型，其中endianess取值分别为：</p>
<a name="ul8450910542"></a><a name="ul8450910542"></a><ul id="ul8450910542"><li>1，大端对齐；</li><li>2，小端对齐；</li><li>3，按机器对齐方式；</li></ul>
</td>
</tr>
</tbody>
</table>

