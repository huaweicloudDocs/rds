# 查询SQL Server可用字符集<a name="rds_05_0010"></a>

## 功能介绍<a name="section4284989"></a>

查询SQL Server字符集列表。

-   调用接口前，您需要了解API  [认证权证](认证鉴权.md)。
-   调用接口前，您需要提前获取到[地区和终端节点](http://developer.huaweicloud.com/endpoint)，即下文中的Endpoint值。

## URI<a name="section38564907"></a>

-   URI格式

    GET https://\{_Endpoint_\}/v3/\{project\_id\}/collations

-   URI样例

    https://rds.cn-north-1.myhuaweicloud.com/v3/0483b6b16e954cb88930a360d2c4e663/instances/dsfae23fsfdsae3435in01/collations

-   参数说明

    **表 1**  参数说明

    <a name="table65777232"></a>
    <table><thead align="left"><tr id="row46529701"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p10809459"><a name="p10809459"></a><a name="p10809459"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p3150961"><a name="p3150961"></a><a name="p3150961"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p53901255"><a name="p53901255"></a><a name="p53901255"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row3925534"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p49532829"><a name="p49532829"></a><a name="p49532829"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p52736237"><a name="p52736237"></a><a name="p52736237"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p43776822"><a name="p43776822"></a><a name="p43776822"></a>租户在某一region下的project ID。</p>
    <p id="p178064411566"><a name="p178064411566"></a><a name="p178064411566"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section1390010340492"></a>

无

## 响应消息<a name="section36749739"></a>

-   正常响应要素说明

    **表 2**  要素说明

    <a name="table17474517"></a>
    <table><thead align="left"><tr id="row16146366"><th class="cellrowborder" valign="top" width="26.38%" id="mcps1.2.4.1.1"><p id="p32787233"><a name="p32787233"></a><a name="p32787233"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.29%" id="mcps1.2.4.1.2"><p id="p38520254"><a name="p38520254"></a><a name="p38520254"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33%" id="mcps1.2.4.1.3"><p id="p33132859"><a name="p33132859"></a><a name="p33132859"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1625804435012"><td class="cellrowborder" valign="top" width="26.38%" headers="mcps1.2.4.1.1 "><p id="p1165525810503"><a name="p1165525810503"></a><a name="p1165525810503"></a>collations</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.29%" headers="mcps1.2.4.1.2 "><p id="p116551958135013"><a name="p116551958135013"></a><a name="p116551958135013"></a>List&lt;String&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="p16655115865012"><a name="p16655115865012"></a><a name="p16655115865012"></a>字符集信息列表。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   正常响应样例：

    ```
    {
    	"charSets": ["Chinese_PRC_CI_AS", "SQL_Latin1_General_CP1_CI_AS", "French_BIN", "Chinese_PRC_Stroke_BIN", "Chinese_PRC_CI_AI"]
    }
    ```

-   异常响应

    请参见[异常请求结果](异常请求结果.md)。


## 状态码<a name="section4778540915440"></a>

请参见[状态码](状态码.md)。

## 错误码<a name="section946032144017"></a>

请参见[错误码](错误码.md)。

