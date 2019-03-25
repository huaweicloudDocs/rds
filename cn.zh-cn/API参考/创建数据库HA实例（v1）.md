# 创建数据库HA实例（v1）<a name="zh-cn_topic_0032347799"></a>

## 流程图<a name="section19141437145619"></a>

创建数据库HA实例流程同创建数据库单实例流程，具体参见[创建数据库单实例（v1）](创建数据库单实例（v1）.md)。

## 调用样例<a name="section4838185413563"></a>

1.  查询List Datastore Version接口。请参见[调用样例](创建数据库单实例（v1）.md#section191181639185213)中[1](创建数据库单实例（v1）.md#li25441382)。
2.  获取region。请参见[调用样例](创建数据库单实例（v1）.md#section191181639185213)中[2](创建数据库单实例（v1）.md#li952315819528)。
3.  查询List Flavor接口。请参见[调用样例](创建数据库单实例（v1）.md#section191181639185213)中[3](创建数据库单实例（v1）.md#li11317154)。
4.  curl命令创建数据库HA实例的请求如下所示：

    replicationMode值定义为$replicationMode。

    ```
    curl -X POST $SERVER_URL/v1/{project_id}/instances -H "Content-Type: application/json" "X-Auth-Token: $X-Subject-Token" "X-Language: en-us" -d '{"instance": {"name": "tenant-instance-123","datastore": {"type": "MySQL","version": "$version"},"flavorRef": " $flavorId","volume": {"type": "COMMON","size": 100},"region": " $region","availabilityZone": " $availabilityZone","vpc": "$vpc ","nics": {"subnetId": "$subnetid "},"securityGroup": {"id": "bb62ffb9-a37a-4821-92b9-f9e0712e389f"},"backupStrategy": {"startTime": "01:00:00","keepDay": 3} ,"dbRtPd": "Test@123" ,"ha": {"enable": true,"replicationMode": "$replicationMode" } }}'
    ```

    正确响应如下所示：

    ```
    {
        "instance": {
            "id": "b0468a4a-5790-4a4f-8442-9030e52369e6",
            "status": "BUILD",
            "name": "tenant-instance-123",
            "created": "",
            "hostname": "",
            "type": "master",
            "region": "aaa",
            "updated": "",
            "availabilityZone": "bbb",
            "vpc": "f7513b5d-5c48-4332-8f47-a3c29c2613e7",
            "nics": {
                "subnetId": "4a7d3555-6410-4338-8859-2be61d51662a"
            },
            "securityGroup": {
                "id": "bb62ffb9-a37a-4821-92b9-f9e0712e389f"
            },
            "flavor": {
                "id": "bf07a6d4-844a-4023-a776-fc5c5fb71fb4"
            },
            "volume": {
                "type": "ULTRAHIGH",
                "size": 100
            },
            "extendparam": {
                "jobs": [
                    {
                        "id": "8a3eb75e5577819f0155778220600001"
                    },
                    {
                        "id": "ae3081675564ddf5357564f64a560025"
                    }
                ]
            },
            "backupStrategy": {
                "startTime": "01:00:00",
                "keepDays": 3
            },
            "slaveId": "9405d8b8-a87d-4531-bd3a-e504c8434281",
            "ha": {
                "replicationMode": "async"
            }
        }
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >响应样例中参数“region”和“availabilityZone”的值为示例值。  
    >创建数据库HA实例返回实例信息列表中，若主机status为FAILED，则在调用Show Database Instance Details以及Delete Database Instance接口时需要使用备机ID。  


