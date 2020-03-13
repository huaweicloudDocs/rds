# 查看或下载慢日志<a name="slow_query_log-sqlserver"></a>

## 操作场景<a name="zh-cn_topic_0171818656_section12909141294214"></a>

慢查询日志用来记录执行时间超过当前慢日志阈值“long\_query\_time“（默认是1秒）的语句，您可以通过慢查询日志的日志明细，查找出执行效率低的语句，进行优化。您也可以下载慢查询日志进行业务分析。

## 参数解析<a name="zh-cn_topic_0171818656_section16601112910434"></a>

**表 1**  SQL Server慢查询相关的参数解析

<a name="zh-cn_topic_0171818656_table1455312241604"></a>
<table><thead align="left"><tr id="zh-cn_topic_0171818656_row1755318241201"><th class="cellrowborder" valign="top" width="22.79%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0171818656_p455311242020"><a name="zh-cn_topic_0171818656_p455311242020"></a><a name="zh-cn_topic_0171818656_p455311242020"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="77.21000000000001%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0171818656_p15534249012"><a name="zh-cn_topic_0171818656_p15534249012"></a><a name="zh-cn_topic_0171818656_p15534249012"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0171818656_row145532241400"><td class="cellrowborder" valign="top" width="22.79%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0171818656_p26741582414"><a name="zh-cn_topic_0171818656_p26741582414"></a><a name="zh-cn_topic_0171818656_p26741582414"></a>long_query_time</p>
</td>
<td class="cellrowborder" valign="top" width="77.21000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0171818656_p121871817112119"><a name="zh-cn_topic_0171818656_p121871817112119"></a><a name="zh-cn_topic_0171818656_p121871817112119"></a>大于等于此时间记录慢查询日志，精度可达微秒级别，默认为1s，当SQL语句执行时间超过此数值时，就会被记录到慢日志中。</p>
<p id="zh-cn_topic_0171818656_p0668124910584"><a name="zh-cn_topic_0171818656_p0668124910584"></a><a name="zh-cn_topic_0171818656_p0668124910584"></a>您可以根据自己的需要，修改当前实例慢日志阈值，具体步骤如下：</p>
<a name="zh-cn_topic_0171818656_ol2197921185015"></a><a name="zh-cn_topic_0171818656_ol2197921185015"></a><ol id="zh-cn_topic_0171818656_ol2197921185015"><li>登录管理控制台。</li><li>单击管理控制台左上角的<a name="zh-cn_topic_0192953815_image192529212293"></a><a name="zh-cn_topic_0192953815_image192529212293"></a><span><img id="zh-cn_topic_0192953815_image192529212293" src="figures/Region灰色图标.png"></span>，选择区域和项目。</li><li>选择<span class="menucascade" id="zh-cn_topic_0192953815_menucascade101697154439"><a name="zh-cn_topic_0192953815_menucascade101697154439"></a><a name="zh-cn_topic_0192953815_menucascade101697154439"></a>“<span class="uicontrol" id="zh-cn_topic_0192953815_uicontrol1516981574315"><a name="zh-cn_topic_0192953815_uicontrol1516981574315"></a><a name="zh-cn_topic_0192953815_uicontrol1516981574315"></a>数据库</span> &gt; <span class="uicontrol" id="zh-cn_topic_0192953815_uicontrol3169131511438"><a name="zh-cn_topic_0192953815_uicontrol3169131511438"></a><a name="zh-cn_topic_0192953815_uicontrol3169131511438"></a>云数据库 RDS</span>”</span>。进入云数据库 RDS信息页面。</li><li>在“实例管理”页面，选择目标实例，单击实例名称，进入实例的<span class="uicontrol" id="zh-cn_topic_0171818656_uicontrol95294162414"><a name="zh-cn_topic_0171818656_uicontrol95294162414"></a><a name="zh-cn_topic_0171818656_uicontrol95294162414"></a>“基本信息”</span>页面。</li><li>在左侧导航栏单击<span class="menucascade" id="menucascade1092116465395"><a name="menucascade1092116465395"></a><a name="menucascade1092116465395"></a>“<span class="uicontrol" id="uicontrol19211046193919"><a name="uicontrol19211046193919"></a><a name="uicontrol19211046193919"></a>日志管理</span>”</span>，在<span class="uicontrol" id="uicontrol199218461398"><a name="uicontrol199218461398"></a><a name="uicontrol199218461398"></a>“慢日志”</span>页签，在<span class="parmname" id="zh-cn_topic_0171818656_parmname867921612919"><a name="zh-cn_topic_0171818656_parmname867921612919"></a><a name="zh-cn_topic_0171818656_parmname867921612919"></a>“当前慢日志阈值(long_query_time)”</span>处，单击<a name="zh-cn_topic_0171818656_image3857343615410"></a><a name="zh-cn_topic_0171818656_image3857343615410"></a><span><img id="zh-cn_topic_0171818656_image3857343615410" src="figures/kwx318612-GAUSS-DBaaS-image-71b3f418-b0b2-4306-9c75-bb4bae6c3f33.png" width="21.945" height="15.06225"></span>，修改慢日志阈值。<a name="zh-cn_topic_0171818656_ul1137218215315"></a><a name="zh-cn_topic_0171818656_ul1137218215315"></a><ul id="zh-cn_topic_0171818656_ul1137218215315"><li>单击 <a name="zh-cn_topic_0171818656_image12216421202217"></a><a name="zh-cn_topic_0171818656_image12216421202217"></a><span><img id="zh-cn_topic_0171818656_image12216421202217" src="figures/端口提交-57.png" width="19.950000000000003" height="9.289252000000001"></span>，提交修改。</li><li>单击<a name="image20569827512"></a><a name="image20569827512"></a><span><img id="image20569827512" src="figures/x-wc-file-zh-cn_image_0068207022.png"></span>，取消修改。</li></ul>
<div class="note" id="zh-cn_topic_0171818656_note199097234317"><a name="zh-cn_topic_0171818656_note199097234317"></a><a name="zh-cn_topic_0171818656_note199097234317"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0171818656_p2912923123111"><a name="zh-cn_topic_0171818656_p2912923123111"></a><a name="zh-cn_topic_0171818656_p2912923123111"></a>建议设置为1s。锁等待时间并不计算在执行时间内。</p>
</div></div>
</li></ol>
</td>
</tr>
</tbody>
</table>

## 查看慢日志<a name="zh-cn_topic_0171818656_section10218113118539"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
5.  在左侧导航栏单击“日志管理“，在“慢日志“页签，单击![](figures/关闭按钮-58.png)，开启SQL Server慢日志功能。
6.  <a name="zh-cn_topic_0171818656_li654810813132"></a>在“慢日志”页面，记录所生成的慢日志文件名。

    **图 1**  SQL Server慢日志<a name="zh-cn_topic_0171818656_fig1792202301011"></a>  
    ![](figures/SQL-Server慢日志.png "SQL-Server慢日志")

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >打开慢日志搜集功能会对当前实例的性能产生一定影响。  

7.  通过SQL Server客户端连接目标实例，具体操作请参见[通过公网连接SQL Server实例](https://support.huaweicloud.com/qs-rds/rds_03_0007.html)。
8.  目标实例连接成功后，通过执行如下sql查看慢日志详情。

    **select \* from ::fn\_trace\_gettable\(‘D:\\SQLTrace\\audit\\**_XXX_**’, default\)**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >_XXX_为[6](#zh-cn_topic_0171818656_li654810813132)中所记录的慢日志文件名。  

    查看慢日志详情，示例如下：

    **select \* from ::fn\_trace\_gettable\(‘D:\\SQLTrace\\audit\\SQLTrace.trc’, default\)**

    查看慢日志结果如[图2](#zh-cn_topic_0171818656_fig19196129142415)所示。

    **图 2**  慢日志详情<a name="zh-cn_topic_0171818656_fig19196129142415"></a>  
    ![](figures/慢日志详情.png "慢日志详情")


## 下载慢日志<a name="zh-cn_topic_0171818656_section1021714251349"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/Region灰色图标.png)，选择区域和项目。
3.  选择“数据库  \>  云数据库 RDS“。进入云数据库 RDS信息页面。
4.  在“实例管理”页面，选择目标实例，单击实例名称，进入实例的“基本信息“页签。
5.  在左侧导航栏单击“日志管理“，在“慢日志“页签，单击![](figures/关闭按钮-58.png)，开启SQL Server慢日志功能。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >打开慢日志搜集功能会对当前实例的性能产生一定影响。  

6.  <a name="zh-cn_topic_0171818656_li121912551908"></a>选择目标日志文件，单击操作列中的“下载“。
    1.  系统会在“下载“弹出框中自动加载下载准备任务，加载时长受日志文件大小及网络环境影响。
        -   下载准备过程中，状态显示为“准备中...”。
        -   下载准备完成，状态显示为“准备完成”。
        -   下载准备工作失败，状态显示为“异常”。

    2.  在“下载“弹出框中，对于“准备完成“的日志文件，单击“确定“，下载慢日志。单击“取消“，则不下载慢日志文件，直接返回下载页签。

        下载链接有效期为5分钟。如果超时，提示用户下载链接已失效，关闭窗口后执行[6](#zh-cn_topic_0171818656_li121912551908)重新下载日志文件。



