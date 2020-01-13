# 策略语法：RBAC<a name="rds_sqlserver_07_0005"></a>

## 策略结构<a name="rds_07_0005_zh-cn_topic_0172661628_section63036484"></a>

策略结构包括：策略版本号（Version）、策略授权语句（Statement）和策略依赖（Depends）。

**图 1**  策略结构<a name="rds_07_0005_zh-cn_topic_0172661628_fig16313497"></a>  
![](figures/策略结构-5.png "策略结构-5")

## 策略语法<a name="rds_07_0005_zh-cn_topic_0172661628_section30457452"></a>

给用户组选择策略时，单击策略下方的![](figures/下拉按钮.png)，可以查看策略的详细内容，如下以RDS的“RDS Administraor”为例，说明RBAC策略语法。

**图 2**  RBAC策略语法<a name="rds_07_0005_fig793143722616"></a>  


![](figures/zh-cn_image_0217606953.png)

```
{
        "Version": "1.0",
        "Statement": [
                {
                        "Action": [
                                "rds:rds:*"
                        ],
                        "Effect": "Allow"
                }
        ],
        "Depends": [
                {
                        "catalog": "BASE",
                        "display_name": "Server Administrator"
                },
                {
                        "catalog": "BASE",
                        "display_name": "Tenant Guest"
                }
        ]
}
```

## 参数说明<a name="rds_07_0005_section1348102233720"></a>

-   Version：策略的版本号，RBAC策略版本为“1.0”，细粒度策略版本为“1.1”。
-   Statement：策略的授权语句，包含Action（授权项）和Effect（作用），Action和Effect结合构成用户具备的权限。
    -   Action（授权项）：操作权限，格式为：服务名:资源类型:操作

        "rds:rds:\*"：表示对RDS的所有操作，其中RDS为服务名；“\*”为通配符，表示对RDS资源可以执行所有操作。

    -   Effect（作用）：定义Action中的操作权限是否允许执行。Allow：允许；Deny：拒绝。

-   Depends：策略的依赖关系，给用户组授予该策略时，需要同时勾选依赖的权限，否则该策略不会生效。
    -   catalog：依赖的策略的所属服务。
    -   display\_name：依赖的策略的名称，“RDS Administraor”依赖Base服务的“Server Administrator”和“Tenant Guest”策略。


