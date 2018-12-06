# 查询API版本信息<a name="zh-cn_topic_0032347779"></a>

## 功能介绍<a name="section50404481154838"></a>

查询API指定版本信息。

## URI<a name="section36318247154838"></a>

-   URI格式

    PATH：/rds/\{versionId\}

    Method：GET

-   参数说明

    **表 1**  参数说明

    <a name="table4657088"></a>
    <table><thead align="left"><tr id="row60083059"><th class="cellrowborder" valign="top" width="27.689999999999998%" id="mcps1.2.4.1.1"><p id="p34889605"><a name="p34889605"></a><a name="p34889605"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.04%" id="mcps1.2.4.1.2"><p id="p7485743"><a name="p7485743"></a><a name="p7485743"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.269999999999996%" id="mcps1.2.4.1.3"><p id="p2365466"><a name="p2365466"></a><a name="p2365466"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row29710333152450"><td class="cellrowborder" valign="top" width="27.689999999999998%" headers="mcps1.2.4.1.1 "><p id="p54604978152455"><a name="p54604978152455"></a><a name="p54604978152455"></a>versionId</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.04%" headers="mcps1.2.4.1.2 "><p id="p60927123152455"><a name="p60927123152455"></a><a name="p60927123152455"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p36149969152455"><a name="p36149969152455"></a><a name="p36149969152455"></a>API版本号，区分大小写，取值：v1。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section47398739154838"></a>

N/A

## 正常响应<a name="section59724852154838"></a>

-   要素说明

    **表 2**  要素说明

    <a name="table62971306105515"></a>
    <table><thead align="left"><tr id="row21185732105515"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p19221610105536"><a name="p19221610105536"></a><a name="p19221610105536"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p13446610105536"><a name="p13446610105536"></a><a name="p13446610105536"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p15433610105536"><a name="p15433610105536"></a><a name="p15433610105536"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row24371359105515"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p59749643105536"><a name="p59749643105536"></a><a name="p59749643105536"></a>versions</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p7882916105536"><a name="p7882916105536"></a><a name="p7882916105536"></a>列表数据结构，请参见<a href="#zh-cn_topic_0032347779__table57914909154838">表3</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p42392997105536"><a name="p42392997105536"></a><a name="p42392997105536"></a>API版本详细信息列表。</p>
    </td>
    </tr>
    <tr id="row3452848511416"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p4534392511416"><a name="p4534392511416"></a><a name="p4534392511416"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p4897932611416"><a name="p4897932611416"></a><a name="p4897932611416"></a>列表数据结构，请参见<a href="#zh-cn_topic_0032347779__table57914909154838">表3</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p790243911416"><a name="p790243911416"></a><a name="p790243911416"></a>API版本详细信息列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  versions字段数据结构说明

    <a name="table57914909154838"></a>
    <table><thead align="left"><tr id="row17905664154838"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p41072674154838"><a name="p41072674154838"></a><a name="p41072674154838"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p38552284154838"><a name="p38552284154838"></a><a name="p38552284154838"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p35727319154838"><a name="p35727319154838"></a><a name="p35727319154838"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row8231739154838"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p62791086154838"><a name="p62791086154838"></a><a name="p62791086154838"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p52913243154838"><a name="p52913243154838"></a><a name="p52913243154838"></a>String。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p58114280154838"><a name="p58114280154838"></a><a name="p58114280154838"></a>API版本号。</p>
    </td>
    </tr>
    <tr id="row83118291298"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p2684540212911"><a name="p2684540212911"></a><a name="p2684540212911"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p2699394512911"><a name="p2699394512911"></a><a name="p2699394512911"></a>列表数据结构，请参见<a href="#zh-cn_topic_0032347779__table630875915440">表4</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1568933512911"><a name="p1568933512911"></a><a name="p1568933512911"></a>对应该API版本的链接信息，该字段为空。</p>
    </td>
    </tr>
    <tr id="row53266474154838"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p19617131154838"><a name="p19617131154838"></a><a name="p19617131154838"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p45483744154838"><a name="p45483744154838"></a><a name="p45483744154838"></a>String。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p60304625154838"><a name="p60304625154838"></a><a name="p60304625154838"></a>版本状态。</p>
    </td>
    </tr>
    <tr id="row5870720154838"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p5766344154838"><a name="p5766344154838"></a><a name="p5766344154838"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p64420704154838"><a name="p64420704154838"></a><a name="p64420704154838"></a>String。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p50694512154838"><a name="p50694512154838"></a><a name="p50694512154838"></a>版本更新时间。</p>
    <p id="p53597429154838"><a name="p53597429154838"></a><a name="p53597429154838"></a>格式为“yyyy-mm-dd Thh:mm:ssZ”。</p>
    <p id="p12614817154838"><a name="p12614817154838"></a><a name="p12614817154838"></a>其中，T指某个时间的开始；Z指UTC时间。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  links字段数据结构说明

    <a name="table630875915440"></a>
    <table><thead align="left"><tr id="row4191288815440"><th class="cellrowborder" valign="top" width="26.529999999999998%" id="mcps1.2.4.1.1"><p id="p3950073415440"><a name="p3950073415440"></a><a name="p3950073415440"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="39.800000000000004%" id="mcps1.2.4.1.2"><p id="p4544288515440"><a name="p4544288515440"></a><a name="p4544288515440"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.67%" id="mcps1.2.4.1.3"><p id="p5699506015440"><a name="p5699506015440"></a><a name="p5699506015440"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5319717215440"><td class="cellrowborder" valign="top" width="26.529999999999998%" headers="mcps1.2.4.1.1 "><p id="p1400369315440"><a name="p1400369315440"></a><a name="p1400369315440"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.800000000000004%" headers="mcps1.2.4.1.2 "><p id="p6055731815440"><a name="p6055731815440"></a><a name="p6055731815440"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.2.4.1.3 "><p id="p619568715440"><a name="p619568715440"></a><a name="p619568715440"></a>对应该API的URL，该字段为""。</p>
    </td>
    </tr>
    <tr id="row5576118615440"><td class="cellrowborder" valign="top" width="26.529999999999998%" headers="mcps1.2.4.1.1 "><p id="p2036224315440"><a name="p2036224315440"></a><a name="p2036224315440"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.800000000000004%" headers="mcps1.2.4.1.2 "><p id="p3872902515440"><a name="p3872902515440"></a><a name="p3872902515440"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.67%" headers="mcps1.2.4.1.3 "><p id="p5004333115440"><a name="p5004333115440"></a><a name="p5004333115440"></a>取值为“self”，表示href为本地链接。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
      "version": {
        "id": "v1",
        "links": [],
        "status": "CURRENT",
        "updated": "2017-02-07T17:34:02Z"
      },
      "versions": {
        "id": "v1",
        "links": [],
        "status": "CURRENT",
        "updated": "2017-02-07T17:34:02Z"
      }
    }
    ```


## 异常响应<a name="section5382712154838"></a>

请参见[异常请求结果](异常请求结果.md)。

