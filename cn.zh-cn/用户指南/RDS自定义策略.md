# RDS自定义策略<a name="rds_07_0003"></a>

如果系统预置的RDS权限，不满足您的授权要求，可以创建自定义策略。自定义策略中可以添加的授权项（Action）请参考[策略及授权项说明](https://support.huaweicloud.com/api-rds/rds_10_0002.html)。

目前华为云支持以下两种方式创建自定义策略：

-   可视化视图创建自定义策略：无需了解策略语法，按可视化视图导航栏选择云服务、操作、资源、条件等策略内容，可自动生成策略。
-   JSON视图创建自定义策略：可以在选择策略模板后，根据具体需求编辑策略内容；也可以直接在编辑框内编写JSON格式的策略内容。

具体创建步骤请参见：[创建自定义策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html)。本章为您介绍常用的RDS自定义策略样例。

## RDS自定义策略样例<a name="zh-cn_topic_0172661626_section7689721"></a>

-   示例1：授权用户创建RDS实例

    ```
    {
    	"Version": "1.1",
    	"Statement": [{
    		"Effect": "Allow",
    		"Action": ["rds:instance:create"]
    	}]
    }
    ```

-   示例2：拒绝用户删除RDS实例

    拒绝策略需要同时配合其他策略使用，否则没有实际作用。用户被授予的策略中，一个授权项的作用如果同时存在Allow和Deny，则遵循Deny优先。

    如果您给用户授予RDS FullAccess的系统策略，但不希望用户拥有RDS FullAccess中定义的删除RDS实例，您可以创建一条拒绝删除云服务的自定义策略，然后同时将RDS FullAccess和拒绝策略授予用户，根据Deny优先原则，则用户可以对RDS实例执行除了删除RDS实例外的所有操作。拒绝策略示例如下：

    ```
    {
    	"Version": "1.1",
    	"Statement": [{
    		"Action": ["rds:instance:delete"],
    		"Effect": "Deny"
    	}]
    }
    ```


