# 获取token<a name="zh-cn_topic_0032347790"></a>

RDS API的访问需经过签名认证，当RDS API采用Token认证方式来完成认证鉴权时，需要获取用户Token，并在调用接口时增加“X-Auth-Token”到业务接口请求消息头中。

获取Token，请参见《统一身份认证服务API参考》的“获取用户Token”章节，请求响应成功后在响应消息头中包含的“X-Subject-Token”的值即为Token值。

curl命令获取Token具体如下所示：

```
curl -X POST $TOKEN_URL -H "Content-Type: application/json" -d '{"auth": {"identity": {"methods": ["password"], "password": {"user": {"name": "'"$OS_USERNAME"'", "password": "'"$OS_PASSWORD"'", "domain": {"name": "'"$OS_DOMAINNAME"'"}}}}, "scope": {"project":{"name":"'"$OS_REGIONCODE"'","domain":{"name":"'"$OS_DOMAINNAME"'"}}}}}'
```

正确响应如下所示：

```
{
    "token": {
        "expires_at": "2016-06-21T10:02:13.752000Z",
        "issued_at": "2016-06-20T10:02:13.752000Z",
        "methods": [
            "password"
        ],
        "project": {
            "name": "projectname",
            "id": "project_id",
            "domain": {
                "name": "domainname",
                "id": "domainid"
            }
        },
        "user": {
            "domain": {
                "name": "domainname",
                "id": "domainid"
            },
            "id": "userid",
            "name": "username"
        },
        "catalog": [],
        "roles": [
            {
                "name": "rolesname1",
                "id": " rolesid1"
            },
            {
                "id": " rolesid2",
                "name": " rolesname2"
            }
        ]
    }
}
```

