# 绑定和解绑弹性公网IP<a name="rds_05_0009"></a>

## 功能介绍<a name="section4850156117316"></a>

关系型数据库实例创建成功后，您可以绑定弹性公网IP，在公共网络来访问数据库实例，绑定后也可根据需要解绑。

-   调用接口前，您需要了解API  [认证权证](认证鉴权.md)。
-   调用接口前，您需要提前获取到[地区和终端节点](http://developer.huaweicloud.com/endpoint)，即下文中的Endpoint值。

## 接口约束<a name="section9207631102915"></a>

实例在创建、变更规格、恢复、重启或冻结状态下不能绑定和解绑弹性公网IP。

## URI<a name="section28961517113719"></a>

-   URI格式

    PUT https://\{_Endpoint_\}/v3/\{_project\_id_\}/instances/\{_instance\_id_\}/public-ip

-   URI样例

    https://rds.cn-north-1.myhuaweicloud.com/v3/0483b6b16e954cb88930a360d2c4e663/instances/dsfae23fsfdsae3435in01/public-ip


-   参数说明

    **表 1**  参数说明

    <a name="table4657088"></a>
    <table><thead align="left"><tr id="row60083059"><th class="cellrowborder" valign="top" width="20.93%" id="mcps1.2.4.1.1"><p id="p34889605"><a name="p34889605"></a><a name="p34889605"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.6%" id="mcps1.2.4.1.2"><p id="p7485743"><a name="p7485743"></a><a name="p7485743"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.470000000000006%" id="mcps1.2.4.1.3"><p id="p2365466"><a name="p2365466"></a><a name="p2365466"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row57385070"><td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.1 "><p id="p17679057"><a name="p17679057"></a><a name="p17679057"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.6%" headers="mcps1.2.4.1.2 "><p id="p22717550"><a name="p22717550"></a><a name="p22717550"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.470000000000006%" headers="mcps1.2.4.1.3 "><p id="p28182251"><a name="p28182251"></a><a name="p28182251"></a>租户在某一region下的project ID。</p>
    <p id="p14611855135510"><a name="p14611855135510"></a><a name="p14611855135510"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row2864326155157"><td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.1 "><p id="p41557789155220"><a name="p41557789155220"></a><a name="p41557789155220"></a>instance_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.6%" headers="mcps1.2.4.1.2 "><p id="p10737742155220"><a name="p10737742155220"></a><a name="p10737742155220"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.470000000000006%" headers="mcps1.2.4.1.3 "><p id="p64450739155220"><a name="p64450739155220"></a><a name="p64450739155220"></a>实例ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section3074340117316"></a>

-   参数说明

    **表 2**  参数说明

    <a name="table11236435"></a>
    <table><thead align="left"><tr id="row61525259"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p17490046"><a name="p17490046"></a><a name="p17490046"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p7407659"><a name="p7407659"></a><a name="p7407659"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p63149496"><a name="p63149496"></a><a name="p63149496"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p14835533"><a name="p14835533"></a><a name="p14835533"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row60827539"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1673976224"><a name="p1673976224"></a><a name="p1673976224"></a>public_ip</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p60181840"><a name="p60181840"></a><a name="p60181840"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p42890904"><a name="p42890904"></a><a name="p42890904"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><div class="notice" id="note11283101711450"><a name="note11283101711450"></a><a name="note11283101711450"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p22831817154515"><a name="p22831817154515"></a><a name="p22831817154515"></a><span class="parmname" id="parmname060063018451"><a name="parmname060063018451"></a><a name="parmname060063018451"></a>“is_bind”</span>为<span class="parmvalue" id="parmvalue469673312457"><a name="parmvalue469673312457"></a><a name="parmvalue469673312457"></a>“true”</span>时，<span class="parmname" id="parmname113447119468"><a name="parmname113447119468"></a><a name="parmname113447119468"></a>“public_ip”</span>为必选。</p>
    </div></div>
    <p id="p34251836102211"><a name="p34251836102211"></a><a name="p34251836102211"></a>待绑定的弹性公网IP地址，仅允许使用标准的IP地址格式。</p>
    </td>
    </tr>
    <tr id="row64061440122213"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p10406154032219"><a name="p10406154032219"></a><a name="p10406154032219"></a>public_ip_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p17406840172218"><a name="p17406840172218"></a><a name="p17406840172218"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p1040611403223"><a name="p1040611403223"></a><a name="p1040611403223"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><div class="notice" id="note17664712144613"><a name="note17664712144613"></a><a name="note17664712144613"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p36649124464"><a name="p36649124464"></a><a name="p36649124464"></a><span class="parmname" id="parmname0664111214614"><a name="parmname0664111214614"></a><a name="parmname0664111214614"></a>“is_bind”</span>为<span class="parmvalue" id="parmvalue196641112164616"><a name="parmvalue196641112164616"></a><a name="parmvalue196641112164616"></a>“true”</span>时，<span class="parmname" id="parmname77843264462"><a name="parmname77843264462"></a><a name="parmname77843264462"></a>“public_ip_id”</span>为必选</p>
    </div></div>
    <p id="p8406164016225"><a name="p8406164016225"></a><a name="p8406164016225"></a>弹性公网IP对应的ID，仅允许使用标准的UUID格式。</p>
    </td>
    </tr>
    <tr id="row1877012092316"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p14770170192311"><a name="p14770170192311"></a><a name="p14770170192311"></a>is_bind</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p877017072312"><a name="p877017072312"></a><a name="p877017072312"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p1177019042312"><a name="p1177019042312"></a><a name="p1177019042312"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><a name="ul973361411474"></a><a name="ul973361411474"></a><ul id="ul973361411474"><li>true：绑定弹性公网IP。</li><li>false：解绑弹性公网IP。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    {
        "public_ip":"10.145.51.214",
        "public_ip_id":"8403e9cd-a7fa-4288-8b15-c7ceac1etest",
        "is_bind":true
    }
    ```


## 响应消息<a name="section28521534113742"></a>

-   正常响应

    无。

-   异常响应

    请参见[异常请求结果](异常请求结果.md)。


## 状态码<a name="section0292127142717"></a>

请参见[状态码](状态码.md)。

## 错误码<a name="section162921376276"></a>

请参见[错误码](错误码.md)。

