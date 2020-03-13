# 创建用户并授权使用RDS<a name="rds_pg_07_0002"></a>

如果您需要对您所拥有的RDS进行精细的权限管理，您可以使用[统一身份认证服务](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)（Identity and Access Management，简称IAM），通过IAM，您可以：

-   根据企业的业务组织，在您的华为云账号中，给企业中不同职能部门的员工创建IAM用户，让员工拥有唯一安全凭证，并使用RDS资源。
-   根据企业用户的职能，设置不同的访问权限，以达到用户之间的权限隔离。
-   将RDS资源委托给更专业、高效的其他华为云账号或者云服务，这些账号或者云服务可以根据权限进行代运维。

如果华为云账号已经能满足您的要求，不需要创建独立的IAM用户，您可以跳过本章节，不影响您使用RDS服务的其它功能。

本章节为您介绍对用户授权的方法，操作流程如[图1](#rds_07_0002_zh-cn_topic_0172661625_fig15451536531)所示。

## 前提条件<a name="rds_07_0002_zh-cn_topic_0172661625_section25675773"></a>

-   “RDS ReadOnlyAccess”属于策略，请先在IAM控制台中开通基于策略的访问控制公测，开通方法请参见：[申请基于策略的访问控制公测](https://support.huaweicloud.com/usermanual-iam/iam_01_019.html)。
-   给用户组授权之前，请您了解用户组可以添加的RDS系统策略，并结合实际需求进行选择，RDS支持的系统权限，请参见：[RDS系统策略](https://support.huaweicloud.com/productdesc-rds/rds_01_0017.html)。若您需要对除RDS之外的其它服务授权，IAM支持服务的所有策略请参见[权限策略](https://support.huaweicloud.com/usermanual-permissions/iam_01_0001.html)。

## 示例流程<a name="rds_07_0002_zh-cn_topic_0172661625_section10309404"></a>

**图 1**  给用户授权RDS权限流程<a name="rds_07_0002_zh-cn_topic_0172661625_fig15451536531"></a>  
![](figures/给用户授权RDS权限流程.png "给用户授权RDS权限流程")

1.  <a name="rds_07_0002_zh-cn_topic_0172661625_li10176121316284"></a>[创建用户组并授权](https://support.huaweicloud.com/usermanual-iam/iam_03_0001.html)

    在IAM控制台创建用户组，并授予关系型数据库只读权限“RDS ReadOnlyAccess”。

2.  [创建用户并加入用户组](https://support.huaweicloud.com/usermanual-iam/iam_02_0001.html)

    在IAM控制台创建用户，并将其加入[1](#rds_07_0002_zh-cn_topic_0172661625_li10176121316284)中创建的用户组。

3.  [用户登录](https://support.huaweicloud.com/usermanual-iam/iam_01_0552.html)并验证权限

    新创建的用户登录控制台，切换至授权区域，验证权限：

    -   在“服务列表”中选择云数据库 RDS，进入RDS主界面，单击右上角“购买关系型数据库”，尝试购买关系型数据库，如果无法购买关系型数据库（假设当前权限仅包含RDS ReadOnlyAccess），表示“RDS ReadOnlyAccess”已生效。
    -   在“服务列表”中选择除云数据库 RDS外（假设当前策略仅包含RDS ReadOnlyAccess）的任一服务，若提示权限不足，表示“RDS ReadOnlyAccess”已生效。


