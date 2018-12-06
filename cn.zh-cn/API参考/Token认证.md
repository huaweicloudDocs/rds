# Token认证<a name="zh-cn_topic_0032347804"></a>

## 应用场景<a name="section50237402"></a>

当您使用Token认证方式完成认证鉴权时，需要获取用户Token并在调用接口时增加“X-Auth-Token”到业务接口请求消息头中。

本节介绍如何调用接口完成Token认证。

## 调用接口步骤<a name="section49483440"></a>

1.  发送“POST https://**_IAM__的Endpoint_**/v3/auth/tokens”请求。

    获取IAM的Endpoint以及消息体中的区域名称，请参见[地区和终端节点](http://developer.huaweicloud.com/dev/endpoint)。

    **表 1**  Header说明

    <a name="table18389930"></a>
    <table><thead align="left"><tr id="row24749807"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p58577354"><a name="p58577354"></a><a name="p58577354"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p47145209"><a name="p47145209"></a><a name="p47145209"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p60665573"><a name="p60665573"></a><a name="p60665573"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p14964341"><a name="p14964341"></a><a name="p14964341"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4152081"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p774306"><a name="p774306"></a><a name="p774306"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p62718864"><a name="p62718864"></a><a name="p62718864"></a>发送的实体的MIME类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p47063234"><a name="p47063234"></a><a name="p47063234"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p54025633"><a name="p54025633"></a><a name="p54025633"></a>application/json</p>
    </td>
    </tr>
    </tbody>
    </table>

    请求内容示例如下：

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >下面示例代码中的斜体字需要替换为实际内容，详细情况请参见《统一身份认证服务API参考》。  

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "password"
                ],
                "password": {
                    "user": {
                        "name": "username",
                        "password": "password",
                        "domain": {
                            "name": "domainname"
                        }
                    }
                }
            },
            "scope": {
                "project": {
                   "name": "regioncode"
                 }
            }
        }
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >请求体中的regioncode，请参见[地区和终端节点](http://developer.huaweicloud.com/dev/endpoint)。  

2.  <a name="l42831c3bf37f47e6be9863d6ec3c4642"></a>获取Token，请参见《统一身份认证服务API参考》的“获取用户Token”章节。请求响应成功后在响应消息头中包含的“X-Subject-Token”的值即为Token值。
3.  从Token的响应结构体中可以获取到对应的project\_id（部分URI需要填入project\_id）。Token响应结构体示例如下：

    ```
    {
        "token": {
            "expires_at": "2016-06-24T07:42:43.907000Z",
            "issued_at": "2016-06-23T07:42:43.907000Z",
            "methods": [
                "password"
            ],
            "project": {
                "name": "projectname",
                "id": "project_id",
                "domain": {
                    "name": "domainname",
                    "id": "domainid",
                    "xdomain_type": "xdomaintype",
                    "xdomain_id": "xdomainid"
                }
            },
            "user": {
                "domain": {
                    "name": "domainname",
                    "id": "domainid",
                    "xdomain_type": "xdomaintype",
                    "xdomain_id": "xdomainid"
                },
                "id": "userid",
                "name": "username"
            },
            "catalog": [],
            "roles": [
                {
                    "name": "rolesname1",
                    "id": "rolesid1"
                },
                {
                    "id": "rolesid2",
                    "name": "rolesname2"
                }
            ]
        }
    }
    ```

4.  调用业务接口，在请求消息头中增加“X-Auth-Token”，“X-Auth-Token”的取值为[2](#l42831c3bf37f47e6be9863d6ec3c4642)中获取的Token。

