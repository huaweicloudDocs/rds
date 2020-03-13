# RDS授权分类<a name="rds_10_0003"></a>

**表 1**  公共查询

<a name="table782223314258"></a>
<table><thead align="left"><tr id="row78229334252"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p1782219338251"><a name="p1782219338251"></a><a name="p1782219338251"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p1682211336250"><a name="p1682211336250"></a><a name="p1682211336250"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p9822113392516"><a name="p9822113392516"></a><a name="p9822113392516"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p582283313258"><a name="p582283313258"></a><a name="p582283313258"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row582293322518"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p882211339256"><a name="p882211339256"></a><a name="p882211339256"></a>查询数据库引擎版本</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p2822193318259"><a name="p2822193318259"></a><a name="p2822193318259"></a>无需授权</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul89517542814"></a><a name="ul89517542814"></a><ul id="ul89517542814"><li>支持：</li></ul>
<p id="p49517572817"><a name="p49517572817"></a><a name="p49517572817"></a><strong id="b1995165112819"><a name="b1995165112819"></a><a name="b1995165112819"></a>IAM</strong>项目(Project)</p>
<a name="ul11951115162818"></a><a name="ul11951115162818"></a><ul id="ul11951115162818"><li>支持：</li></ul>
<p id="p209519532820"><a name="p209519532820"></a><a name="p209519532820"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p10823113312254"><a name="p10823113312254"></a><a name="p10823113312254"></a>GET /v3/{projectId}/datastores/{database_name}</p>
</td>
</tr>
<tr id="row282318334257"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p3823833112510"><a name="p3823833112510"></a><a name="p3823833112510"></a>查询数据库规格</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p2823193392514"><a name="p2823193392514"></a><a name="p2823193392514"></a>无需授权</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul897617303334"></a><a name="ul897617303334"></a><ul id="ul897617303334"><li>支持：</li></ul>
<p id="p1397703010338"><a name="p1397703010338"></a><a name="p1397703010338"></a><strong id="b697713014331"><a name="b697713014331"></a><a name="b697713014331"></a>IAM</strong>项目(Project)</p>
<a name="ul1797723019332"></a><a name="ul1797723019332"></a><ul id="ul1797723019332"><li>支持：</li></ul>
<p id="p89774308332"><a name="p89774308332"></a><a name="p89774308332"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p178231233122511"><a name="p178231233122511"></a><a name="p178231233122511"></a>GET /v3/{project_id}/flavors/{database_name}?version_name={version_name}</p>
</td>
</tr>
<tr id="row1082393332513"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p128232033182511"><a name="p128232033182511"></a><a name="p128232033182511"></a>查询数据库存储规格</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p6823033202516"><a name="p6823033202516"></a><a name="p6823033202516"></a>无需授权</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul6298958203310"></a><a name="ul6298958203310"></a><ul id="ul6298958203310"><li>支持：</li></ul>
<p id="p1429935812333"><a name="p1429935812333"></a><a name="p1429935812333"></a><strong id="b16299175815337"><a name="b16299175815337"></a><a name="b16299175815337"></a>IAM</strong>项目(Project)</p>
<a name="ul7299115863315"></a><a name="ul7299115863315"></a><ul id="ul7299115863315"><li>支持：</li></ul>
<p id="p029965813338"><a name="p029965813338"></a><a name="p029965813338"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p188231533112517"><a name="p188231533112517"></a><a name="p188231533112517"></a>GET /v3/{project_id}/storage-type/{database_name}?version_name={version_name}</p>
</td>
</tr>
</tbody>
</table>

**表 2**  实例管理

<a name="table16408163223412"></a>
<table><thead align="left"><tr id="row16409153203418"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p4409132113420"><a name="p4409132113420"></a><a name="p4409132113420"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p3409193293416"><a name="p3409193293416"></a><a name="p3409193293416"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p1409332163411"><a name="p1409332163411"></a><a name="p1409332163411"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p13409163217343"><a name="p13409163217343"></a><a name="p13409163217343"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row940910328345"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p134098324349"><a name="p134098324349"></a><a name="p134098324349"></a>创建数据库实例</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p12573205345917"><a name="p12573205345917"></a><a name="p12573205345917"></a>rds:instance:create</p>
<p id="p20355357173820"><a name="p20355357173820"></a><a name="p20355357173820"></a>（创建加密实例需要在项目上配置KMS Administrator权限。）</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1828847133916"></a><a name="ul1828847133916"></a><ul id="ul1828847133916"><li>支持：</li></ul>
<p id="p7283470391"><a name="p7283470391"></a><a name="p7283470391"></a><strong id="b128134713911"><a name="b128134713911"></a><a name="b128134713911"></a>IAM</strong>项目(Project)</p>
<a name="ul228124713918"></a><a name="ul228124713918"></a><ul id="ul228124713918"><li>支持：</li></ul>
<p id="p182854718393"><a name="p182854718393"></a><a name="p182854718393"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p7409163213418"><a name="p7409163213418"></a><a name="p7409163213418"></a>POST /v3/{project_id}/instances</p>
</td>
</tr>
<tr id="row4409113243419"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p16409113219342"><a name="p16409113219342"></a><a name="p16409113219342"></a>变更数据库实例的规格</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1274127504"><a name="p1274127504"></a><a name="p1274127504"></a>rds:instance:modifySpec</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul381160134314"></a><a name="ul381160134314"></a><ul id="ul381160134314"><li>支持：</li></ul>
<p id="p781119084312"><a name="p781119084312"></a><a name="p781119084312"></a><strong id="b188111905439"><a name="b188111905439"></a><a name="b188111905439"></a>IAM</strong>项目(Project)</p>
<a name="ul1881112054315"></a><a name="ul1881112054315"></a><ul id="ul1881112054315"><li>支持：</li></ul>
<p id="p081260194319"><a name="p081260194319"></a><a name="p081260194319"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p144094321346"><a name="p144094321346"></a><a name="p144094321346"></a>POST /v3/{project_id}/instances/{instance_id}/action</p>
</td>
</tr>
<tr id="row440993217346"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p124095321345"><a name="p124095321345"></a><a name="p124095321345"></a>扩容数据库实例的磁盘空间</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p19409163263411"><a name="p19409163263411"></a><a name="p19409163263411"></a>rds:instance:extendSpace</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul87015284310"></a><a name="ul87015284310"></a><ul id="ul87015284310"><li>支持：</li></ul>
<p id="p157162204311"><a name="p157162204311"></a><a name="p157162204311"></a><strong id="b18714254313"><a name="b18714254313"></a><a name="b18714254313"></a>IAM</strong>项目(Project)</p>
<a name="ul12711627435"></a><a name="ul12711627435"></a><ul id="ul12711627435"><li>支持：</li></ul>
<p id="p10716213435"><a name="p10716213435"></a><a name="p10716213435"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1409193223418"><a name="p1409193223418"></a><a name="p1409193223418"></a>POST /v3/{project_id}/instances/{instance_id}/action</p>
</td>
</tr>
<tr id="row940903217346"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p24095320340"><a name="p24095320340"></a><a name="p24095320340"></a>单机转主备实例</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p199318201605"><a name="p199318201605"></a><a name="p199318201605"></a>rds:instance:singleToHa</p>
<p id="p99328140391"><a name="p99328140391"></a><a name="p99328140391"></a>（加密实例需要在项目上配置KMS Administrator权限。）</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul524483134316"></a><a name="ul524483134316"></a><ul id="ul524483134316"><li>支持：</li></ul>
<p id="p142445318434"><a name="p142445318434"></a><a name="p142445318434"></a><strong id="b1524412344320"><a name="b1524412344320"></a><a name="b1524412344320"></a>IAM</strong>项目(Project)</p>
<a name="ul182448354313"></a><a name="ul182448354313"></a><ul id="ul182448354313"><li>支持：</li></ul>
<p id="p152441438436"><a name="p152441438436"></a><a name="p152441438436"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1341015325345"><a name="p1341015325345"></a><a name="p1341015325345"></a>POST /v3/{project_id}/instances/{instance_id}/action</p>
</td>
</tr>
<tr id="row174101632123419"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1041093217349"><a name="p1041093217349"></a><a name="p1041093217349"></a>重启数据库实例</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p841043213410"><a name="p841043213410"></a><a name="p841043213410"></a>rds:instance:restart</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1191964134313"></a><a name="ul1191964134313"></a><ul id="ul1191964134313"><li>支持：</li></ul>
<p id="p12919194184311"><a name="p12919194184311"></a><a name="p12919194184311"></a><strong id="b29191345432"><a name="b29191345432"></a><a name="b29191345432"></a>IAM</strong>项目(Project)</p>
<a name="ul17919114124316"></a><a name="ul17919114124316"></a><ul id="ul17919114124316"><li>支持：</li></ul>
<p id="p491954114312"><a name="p491954114312"></a><a name="p491954114312"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p3410193213348"><a name="p3410193213348"></a><a name="p3410193213348"></a>POST /v3/{project_id}/instances/{instance_id}/action</p>
</td>
</tr>
<tr id="row124101132153415"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p941013219348"><a name="p941013219348"></a><a name="p941013219348"></a>删除数据库实例</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1584317471016"><a name="p1584317471016"></a><a name="p1584317471016"></a>rds:instance:delete</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul683316142167"></a><a name="ul683316142167"></a><ul id="ul683316142167"><li>支持：</li></ul>
<p id="p1083311410167"><a name="p1083311410167"></a><a name="p1083311410167"></a><strong id="b12833914181612"><a name="b12833914181612"></a><a name="b12833914181612"></a>IAM</strong>项目(Project)</p>
<a name="ul4833151412164"></a><a name="ul4833151412164"></a><ul id="ul4833151412164"><li>支持：</li></ul>
<p id="p28338144162"><a name="p28338144162"></a><a name="p28338144162"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1141043283418"><a name="p1141043283418"></a><a name="p1141043283418"></a>DELETE /v3/{project_id}/instances/{instance_id}</p>
</td>
</tr>
<tr id="row890915364018"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p19910553114012"><a name="p19910553114012"></a><a name="p19910553114012"></a>查询数据库实例列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1291065311404"><a name="p1291065311404"></a><a name="p1291065311404"></a>rds:instance:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul3201647172520"></a><a name="ul3201647172520"></a><ul id="ul3201647172520"><li>支持：</li></ul>
<p id="p2021247122516"><a name="p2021247122516"></a><a name="p2021247122516"></a><strong id="b132115477259"><a name="b132115477259"></a><a name="b132115477259"></a>IAM</strong>项目(Project)</p>
<a name="ul221144712515"></a><a name="ul221144712515"></a><ul id="ul221144712515"><li>支持：</li></ul>
<p id="p17216473255"><a name="p17216473255"></a><a name="p17216473255"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p16910115314015"><a name="p16910115314015"></a><a name="p16910115314015"></a>GET /v3/{project_id}/instances</p>
</td>
</tr>
<tr id="row1564915215315"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p96491295318"><a name="p96491295318"></a><a name="p96491295318"></a>绑定和解绑弹性公网IP</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p166491529535"><a name="p166491529535"></a><a name="p166491529535"></a>rds:instance:modifyPublicAccess</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul739318463543"></a><a name="ul739318463543"></a><ul id="ul739318463543"><li>支持：</li></ul>
<p id="p43931746115412"><a name="p43931746115412"></a><a name="p43931746115412"></a><strong id="b17393146155410"><a name="b17393146155410"></a><a name="b17393146155410"></a>IAM</strong>项目(Project)</p>
<a name="ul9393246105417"></a><a name="ul9393246105417"></a><ul id="ul9393246105417"><li>支持：</li></ul>
<p id="p539464617546"><a name="p539464617546"></a><a name="p539464617546"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p19649132145317"><a name="p19649132145317"></a><a name="p19649132145317"></a>PUT /v3/{project_id}/instances/{instance_id}/public-ip</p>
</td>
</tr>
<tr id="row1658943353618"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p125901733133614"><a name="p125901733133614"></a><a name="p125901733133614"></a>修改数据库实例密码</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p5590133311361"><a name="p5590133311361"></a><a name="p5590133311361"></a>rds:password:update</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul137111117371"></a><a name="ul137111117371"></a><ul id="ul137111117371"><li>支持：</li></ul>
<p id="p1671141113377"><a name="p1671141113377"></a><a name="p1671141113377"></a><strong id="b147121133715"><a name="b147121133715"></a><a name="b147121133715"></a>IAM</strong>项目(Project)</p>
<a name="ul1771131193713"></a><a name="ul1771131193713"></a><ul id="ul1771131193713"><li>支持：</li></ul>
<p id="p571161153720"><a name="p571161153720"></a><a name="p571161153720"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p340821711371"><a name="p340821711371"></a><a name="p340821711371"></a>PUT /v3/{project_id}/instances/{instance_id}/password</p>
</td>
</tr>
</tbody>
</table>

**表 3**  参数配置

<a name="table15662154114810"></a>
<table><thead align="left"><tr id="row176775434816"><th class="cellrowborder" valign="top" width="25.522552255225524%" id="mcps1.2.5.1.1"><p id="p13767125418487"><a name="p13767125418487"></a><a name="p13767125418487"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="24.74247424742474%" id="mcps1.2.5.1.2"><p id="p27671544481"><a name="p27671544481"></a><a name="p27671544481"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25.492549254925496%" id="mcps1.2.5.1.3"><p id="p1376765411489"><a name="p1376765411489"></a><a name="p1376765411489"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="24.242424242424242%" id="mcps1.2.5.1.4"><p id="p6767554104814"><a name="p6767554104814"></a><a name="p6767554104814"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row39341118114016"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p493531824011"><a name="p493531824011"></a><a name="p493531824011"></a>获取参数模板列表</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p3936171816403"><a name="p3936171816403"></a><a name="p3936171816403"></a>rds:param:list</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul6583191817419"></a><a name="ul6583191817419"></a><ul id="ul6583191817419"><li>支持：</li></ul>
<p id="p3584111810414"><a name="p3584111810414"></a><a name="p3584111810414"></a><strong id="b358415189417"><a name="b358415189417"></a><a name="b358415189417"></a>IAM</strong>项目(Project)</p>
<a name="ul1158416187417"></a><a name="ul1158416187417"></a><ul id="ul1158416187417"><li>支持：</li></ul>
<p id="p1858431811419"><a name="p1858431811419"></a><a name="p1858431811419"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p1693681810401"><a name="p1693681810401"></a><a name="p1693681810401"></a>GET /v3/{project_id}/configurations</p>
</td>
</tr>
<tr id="row7140113964115"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p114113913411"><a name="p114113913411"></a><a name="p114113913411"></a>创建参数模板</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p1714193918414"><a name="p1714193918414"></a><a name="p1714193918414"></a>rds:param:create</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul8960194754111"></a><a name="ul8960194754111"></a><ul id="ul8960194754111"><li>支持：</li></ul>
<p id="p15960647194112"><a name="p15960647194112"></a><a name="p15960647194112"></a><strong id="b1196017477412"><a name="b1196017477412"></a><a name="b1196017477412"></a>IAM</strong>项目(Project)</p>
<a name="ul13960147204110"></a><a name="ul13960147204110"></a><ul id="ul13960147204110"><li>支持：</li></ul>
<p id="p19960647194113"><a name="p19960647194113"></a><a name="p19960647194113"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p1614193919416"><a name="p1614193919416"></a><a name="p1614193919416"></a>POST /v3/{project_id}/configurations</p>
</td>
</tr>
<tr id="row45921715164220"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p195921215104217"><a name="p195921215104217"></a><a name="p195921215104217"></a>修改参数模板参数</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p145921015114210"><a name="p145921015114210"></a><a name="p145921015114210"></a>rds:param:modify</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul1071762824216"></a><a name="ul1071762824216"></a><ul id="ul1071762824216"><li>支持：</li></ul>
<p id="p1717122817429"><a name="p1717122817429"></a><a name="p1717122817429"></a><strong id="b12717192810424"><a name="b12717192810424"></a><a name="b12717192810424"></a>IAM</strong>项目(Project)</p>
<a name="ul071732884210"></a><a name="ul071732884210"></a><ul id="ul071732884210"><li>支持：</li></ul>
<p id="p0717628154216"><a name="p0717628154216"></a><a name="p0717628154216"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p1259261512424"><a name="p1259261512424"></a><a name="p1259261512424"></a>PUT /v3/{project_id}/configurations/{config_id}</p>
</td>
</tr>
<tr id="row1575310595431"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p11562115446"><a name="p11562115446"></a><a name="p11562115446"></a>应用参数模板</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p71561110444"><a name="p71561110444"></a><a name="p71561110444"></a>rds:param:apply</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul415611164418"></a><a name="ul415611164418"></a><ul id="ul415611164418"><li>支持：</li></ul>
<p id="p1215613118449"><a name="p1215613118449"></a><a name="p1215613118449"></a><strong id="b01569154419"><a name="b01569154419"></a><a name="b01569154419"></a>IAM</strong>项目(Project)</p>
<a name="ul15156121204413"></a><a name="ul15156121204413"></a><ul id="ul15156121204413"><li>支持：</li></ul>
<p id="p4156191154417"><a name="p4156191154417"></a><a name="p4156191154417"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p1215616112449"><a name="p1215616112449"></a><a name="p1215616112449"></a>PUT /v3/{project_id}/configurations/{config_id}/apply</p>
</td>
</tr>
<tr id="row107027114419"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p12751628184411"><a name="p12751628184411"></a><a name="p12751628184411"></a>修改指定实例的参数</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p1527513282443"><a name="p1527513282443"></a><a name="p1527513282443"></a>rds:param:modify</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul10275828114412"></a><a name="ul10275828114412"></a><ul id="ul10275828114412"><li>支持：</li></ul>
<p id="p62753288447"><a name="p62753288447"></a><a name="p62753288447"></a><strong id="b162751128114418"><a name="b162751128114418"></a><a name="b162751128114418"></a>IAM</strong>项目(Project)</p>
<a name="ul1727692815447"></a><a name="ul1727692815447"></a><ul id="ul1727692815447"><li>支持：</li></ul>
<p id="p72761028144418"><a name="p72761028144418"></a><a name="p72761028144418"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p20276182814413"><a name="p20276182814413"></a><a name="p20276182814413"></a>PUT /v3/{project_id}/instances/{instance_id}/configurations</p>
</td>
</tr>
<tr id="row4767105413489"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p1076725420485"><a name="p1076725420485"></a><a name="p1076725420485"></a>获取指定实例的参数模板</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p67981758205717"><a name="p67981758205717"></a><a name="p67981758205717"></a>rds:param:list</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul5768125414488"></a><a name="ul5768125414488"></a><ul id="ul5768125414488"><li>支持：</li></ul>
<p id="p1276855464818"><a name="p1276855464818"></a><a name="p1276855464818"></a><strong id="b11768175412488"><a name="b11768175412488"></a><a name="b11768175412488"></a>IAM</strong>项目(Project)</p>
<a name="ul18768195484818"></a><a name="ul18768195484818"></a><ul id="ul18768195484818"><li>支持：</li></ul>
<p id="p77682542484"><a name="p77682542484"></a><a name="p77682542484"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p13768165414480"><a name="p13768165414480"></a><a name="p13768165414480"></a>GET /v3/{project_id}/instances/{instance_id}/configurations</p>
</td>
</tr>
<tr id="row08781252114411"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p158781552124416"><a name="p158781552124416"></a><a name="p158781552124416"></a>获取指定参数模板的参数</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p387913522449"><a name="p387913522449"></a><a name="p387913522449"></a>rds:param:list</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul175811884519"></a><a name="ul175811884519"></a><ul id="ul175811884519"><li>支持：</li></ul>
<p id="p959158144513"><a name="p959158144513"></a><a name="p959158144513"></a><strong id="b65968194516"><a name="b65968194516"></a><a name="b65968194516"></a>IAM</strong>项目(Project)</p>
<a name="ul14595813456"></a><a name="ul14595813456"></a><ul id="ul14595813456"><li>支持：</li></ul>
<p id="p0591683455"><a name="p0591683455"></a><a name="p0591683455"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p148792526445"><a name="p148792526445"></a><a name="p148792526445"></a>GET /v3/{project_id}/configurations/{config_id}</p>
</td>
</tr>
<tr id="row168871289458"><td class="cellrowborder" valign="top" width="25.522552255225524%" headers="mcps1.2.5.1.1 "><p id="p1088717282458"><a name="p1088717282458"></a><a name="p1088717282458"></a>删除参数模板</p>
</td>
<td class="cellrowborder" valign="top" width="24.74247424742474%" headers="mcps1.2.5.1.2 "><p id="p148871284459"><a name="p148871284459"></a><a name="p148871284459"></a>rds:param:delete</p>
</td>
<td class="cellrowborder" valign="top" width="25.492549254925496%" headers="mcps1.2.5.1.3 "><a name="ul124856376456"></a><a name="ul124856376456"></a><ul id="ul124856376456"><li>支持：</li></ul>
<p id="p04855379459"><a name="p04855379459"></a><a name="p04855379459"></a><strong id="b194850376454"><a name="b194850376454"></a><a name="b194850376454"></a>IAM</strong>项目(Project)</p>
<a name="ul54851237114516"></a><a name="ul54851237114516"></a><ul id="ul54851237114516"><li>支持：</li></ul>
<p id="p11485163764513"><a name="p11485163764513"></a><a name="p11485163764513"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="24.242424242424242%" headers="mcps1.2.5.1.4 "><p id="p0887152811454"><a name="p0887152811454"></a><a name="p0887152811454"></a>DELETE /v3/{project_id}/configurations/{config_id}</p>
</td>
</tr>
</tbody>
</table>

**表 4**  备份与恢复

<a name="table6650112174818"></a>
<table><thead align="left"><tr id="row1765119123488"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p99557543588"><a name="p99557543588"></a><a name="p99557543588"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p159551454135814"><a name="p159551454135814"></a><a name="p159551454135814"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p1955154205813"><a name="p1955154205813"></a><a name="p1955154205813"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p4955135415581"><a name="p4955135415581"></a><a name="p4955135415581"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row36515125482"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p19651112104812"><a name="p19651112104812"></a><a name="p19651112104812"></a>设置自动备份策略</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1465191234811"><a name="p1465191234811"></a><a name="p1465191234811"></a>rds:instance:modifyBackupPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul187231518311"></a><a name="ul187231518311"></a><ul id="ul187231518311"><li>支持：</li></ul>
<p id="p1672385111312"><a name="p1672385111312"></a><a name="p1672385111312"></a><strong id="b672355120318"><a name="b672355120318"></a><a name="b672355120318"></a>IAM</strong>项目(Project)</p>
<a name="ul167239511031"></a><a name="ul167239511031"></a><ul id="ul167239511031"><li>支持：</li></ul>
<p id="p77238519316"><a name="p77238519316"></a><a name="p77238519316"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1665171244811"><a name="p1665171244811"></a><a name="p1665171244811"></a>PUT /v3/{project_id}/instances/{instance_id}/backups/policy</p>
</td>
</tr>
<tr id="row16651191215489"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1651151219488"><a name="p1651151219488"></a><a name="p1651151219488"></a>查询自动备份策略</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p126511912144810"><a name="p126511912144810"></a><a name="p126511912144810"></a>rds:instance:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul36996521639"></a><a name="ul36996521639"></a><ul id="ul36996521639"><li>支持：</li></ul>
<p id="p1570019521334"><a name="p1570019521334"></a><a name="p1570019521334"></a><strong id="b107007521231"><a name="b107007521231"></a><a name="b107007521231"></a>IAM</strong>项目(Project)</p>
<a name="ul147001652233"></a><a name="ul147001652233"></a><ul id="ul147001652233"><li>支持：</li></ul>
<p id="p1770019523314"><a name="p1770019523314"></a><a name="p1770019523314"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1265110127481"><a name="p1265110127481"></a><a name="p1265110127481"></a>GET /v3/{project_id}/instances/{instance_id}/backups/policy</p>
</td>
</tr>
<tr id="row365118123484"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1465121254820"><a name="p1465121254820"></a><a name="p1465121254820"></a>创建手动备份</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p206511312114816"><a name="p206511312114816"></a><a name="p206511312114816"></a>rds:backup:create</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul03339547319"></a><a name="ul03339547319"></a><ul id="ul03339547319"><li>支持：</li></ul>
<p id="p1033313541312"><a name="p1033313541312"></a><a name="p1033313541312"></a><strong id="b73338541130"><a name="b73338541130"></a><a name="b73338541130"></a>IAM</strong>项目(Project)</p>
<a name="ul63334547313"></a><a name="ul63334547313"></a><ul id="ul63334547313"><li>支持：</li></ul>
<p id="p13331454238"><a name="p13331454238"></a><a name="p13331454238"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p7652131284818"><a name="p7652131284818"></a><a name="p7652131284818"></a>POST /v3/{project_id}/backups</p>
</td>
</tr>
<tr id="row11259193015010"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p426023018016"><a name="p426023018016"></a><a name="p426023018016"></a>获取备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1026016301302"><a name="p1026016301302"></a><a name="p1026016301302"></a>rds:backup:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1943917559313"></a><a name="ul1943917559313"></a><ul id="ul1943917559313"><li>支持：</li></ul>
<p id="p243910553319"><a name="p243910553319"></a><a name="p243910553319"></a><strong id="b1343910551631"><a name="b1343910551631"></a><a name="b1343910551631"></a>IAM</strong>项目(Project)</p>
<a name="ul64390553319"></a><a name="ul64390553319"></a><ul id="ul64390553319"><li>支持：</li></ul>
<p id="p124391755536"><a name="p124391755536"></a><a name="p124391755536"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1026015301305"><a name="p1026015301305"></a><a name="p1026015301305"></a>GET /v3/{project_id}/backups?instance_id={instance_id}</p>
</td>
</tr>
<tr id="row1057018371304"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p157015376011"><a name="p157015376011"></a><a name="p157015376011"></a>获取备份下载链接</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1957018372018"><a name="p1957018372018"></a><a name="p1957018372018"></a>rds:backup:download</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1058810564316"></a><a name="ul1058810564316"></a><ul id="ul1058810564316"><li>支持：</li></ul>
<p id="p3589185619317"><a name="p3589185619317"></a><a name="p3589185619317"></a><strong id="b19589756637"><a name="b19589756637"></a><a name="b19589756637"></a>IAM</strong>项目(Project)</p>
<a name="ul2058918561532"></a><a name="ul2058918561532"></a><ul id="ul2058918561532"><li>支持：</li></ul>
<p id="p4589195617311"><a name="p4589195617311"></a><a name="p4589195617311"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p257043713012"><a name="p257043713012"></a><a name="p257043713012"></a>GET /v3/{project_id}/backup-files?backup_id={backup_id}</p>
</td>
</tr>
<tr id="row619816356014"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p11198735601"><a name="p11198735601"></a><a name="p11198735601"></a>删除手动备份</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p14198113517018"><a name="p14198113517018"></a><a name="p14198113517018"></a>rds:backup:delete</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1419113584320"></a><a name="ul1419113584320"></a><ul id="ul1419113584320"><li>支持：</li></ul>
<p id="p11191958231"><a name="p11191958231"></a><a name="p11191958231"></a><strong id="b619110587318"><a name="b619110587318"></a><a name="b619110587318"></a>IAM</strong>项目(Project)</p>
<a name="ul3191155814314"></a><a name="ul3191155814314"></a><ul id="ul3191155814314"><li>支持：</li></ul>
<p id="p1519118589312"><a name="p1519118589312"></a><a name="p1519118589312"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1119814351009"><a name="p1119814351009"></a><a name="p1119814351009"></a>DELETE /v3/{project_id}/backups/{backup_id}</p>
</td>
</tr>
<tr id="row4884143216019"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1788418321207"><a name="p1788418321207"></a><a name="p1788418321207"></a>查询可恢复时间段</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1288410321009"><a name="p1288410321009"></a><a name="p1288410321009"></a>rds:instance:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1053595912310"></a><a name="ul1053595912310"></a><ul id="ul1053595912310"><li>支持：</li></ul>
<p id="p0536175911315"><a name="p0536175911315"></a><a name="p0536175911315"></a><strong id="b1253618594320"><a name="b1253618594320"></a><a name="b1253618594320"></a>IAM</strong>项目(Project)</p>
<a name="ul95365591537"></a><a name="ul95365591537"></a><ul id="ul95365591537"><li>支持：</li></ul>
<p id="p45361959536"><a name="p45361959536"></a><a name="p45361959536"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p18841132804"><a name="p18841132804"></a><a name="p18841132804"></a>GET /v3/{project_id}/instances/{instance_id}/restore-time</p>
</td>
</tr>
<tr id="row14112939226"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p211223919217"><a name="p211223919217"></a><a name="p211223919217"></a>恢复到新实例</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p8393351115820"><a name="p8393351115820"></a><a name="p8393351115820"></a>rds:instance:create</p>
<p id="p646922710397"><a name="p646922710397"></a><a name="p646922710397"></a>（加密实例需要在项目上配置KMS Administrator权限。）</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1752440645"></a><a name="ul1752440645"></a><ul id="ul1752440645"><li>支持：</li></ul>
<p id="p16524140348"><a name="p16524140348"></a><a name="p16524140348"></a><strong id="b115246015415"><a name="b115246015415"></a><a name="b115246015415"></a>IAM</strong>项目(Project)</p>
<a name="ul1252411017412"></a><a name="ul1252411017412"></a><ul id="ul1252411017412"><li>支持：</li></ul>
<p id="p16524604414"><a name="p16524604414"></a><a name="p16524604414"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1111213391725"><a name="p1111213391725"></a><a name="p1111213391725"></a>POST /v3/{project_id}/instances</p>
</td>
</tr>
<tr id="row15969114111214"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1996964110217"><a name="p1996964110217"></a><a name="p1996964110217"></a>恢复到已有或当前实例</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p49691241826"><a name="p49691241826"></a><a name="p49691241826"></a>rds:instance:restoreInPlace</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1751615114417"></a><a name="ul1751615114417"></a><ul id="ul1751615114417"><li>支持：</li></ul>
<p id="p14516419410"><a name="p14516419410"></a><a name="p14516419410"></a><strong id="b145161412049"><a name="b145161412049"></a><a name="b145161412049"></a>IAM</strong>项目(Project)</p>
<a name="ul25161111944"></a><a name="ul25161111944"></a><ul id="ul25161111944"><li>支持：</li></ul>
<p id="p9516121542"><a name="p9516121542"></a><a name="p9516121542"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p7969541724"><a name="p7969541724"></a><a name="p7969541724"></a>POST /v3/{project_id}/instances/recovery</p>
</td>
</tr>
</tbody>
</table>

**表 5**  获取日志信息

<a name="table59608555620"></a>
<table><thead align="left"><tr id="row99611755563"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p188401135716"><a name="p188401135716"></a><a name="p188401135716"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p17840831678"><a name="p17840831678"></a><a name="p17840831678"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p198401312720"><a name="p198401312720"></a><a name="p198401312720"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p58411531874"><a name="p58411531874"></a><a name="p58411531874"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row10961145516614"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p596112551166"><a name="p596112551166"></a><a name="p596112551166"></a>查询数据库错误日志</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p99619551065"><a name="p99619551065"></a><a name="p99619551065"></a>rds:log:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul158616495714"></a><a name="ul158616495714"></a><ul id="ul158616495714"><li>支持：</li></ul>
<p id="p15861549777"><a name="p15861549777"></a><a name="p15861549777"></a><strong id="b98618491778"><a name="b98618491778"></a><a name="b98618491778"></a>IAM</strong>项目(Project)</p>
<a name="ul11871549579"></a><a name="ul11871549579"></a><ul id="ul11871549579"><li>支持：</li></ul>
<p id="p98714491074"><a name="p98714491074"></a><a name="p98714491074"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p59614551062"><a name="p59614551062"></a><a name="p59614551062"></a>GET /v3/{project_id}/instances/{instance_id}/errorlog?start_date={start_date}&amp;end_date={end_date}</p>
</td>
</tr>
<tr id="row896115559619"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p17961055965"><a name="p17961055965"></a><a name="p17961055965"></a>查询数据库慢日志</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p109611055867"><a name="p109611055867"></a><a name="p109611055867"></a>rds:log:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul82318505714"></a><a name="ul82318505714"></a><ul id="ul82318505714"><li>支持：</li></ul>
<p id="p82411501273"><a name="p82411501273"></a><a name="p82411501273"></a><strong id="b9240504714"><a name="b9240504714"></a><a name="b9240504714"></a>IAM</strong>项目(Project)</p>
<a name="ul9241508719"></a><a name="ul9241508719"></a><ul id="ul9241508719"><li>支持：</li></ul>
<p id="p1424750370"><a name="p1424750370"></a><a name="p1424750370"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p11961855869"><a name="p11961855869"></a><a name="p11961855869"></a>GET /v3/{project_id}/instances/{instance_id}/slowlog?start_date={start_date}&amp;end_date={end_date}</p>
</td>
</tr>
<tr id="row1342191810556"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p734341816554"><a name="p734341816554"></a><a name="p734341816554"></a>设置审计日志策略</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1134391885512"><a name="p1134391885512"></a><a name="p1134391885512"></a>rds:auditlog:operate</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1471713319568"></a><a name="ul1471713319568"></a><ul id="ul1471713319568"><li>支持：</li></ul>
<p id="p6717113105617"><a name="p6717113105617"></a><a name="p6717113105617"></a><strong id="b167176313569"><a name="b167176313569"></a><a name="b167176313569"></a>IAM</strong>项目(Project)</p>
<a name="ul1671719375614"></a><a name="ul1671719375614"></a><ul id="ul1671719375614"><li>支持：</li></ul>
<p id="p12717139565"><a name="p12717139565"></a><a name="p12717139565"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1343111810551"><a name="p1343111810551"></a><a name="p1343111810551"></a>PUT</p>
<p id="p135359212564"><a name="p135359212564"></a><a name="p135359212564"></a>/v3/{project_id}/instances/{instance_id}/auditlog-policy</p>
</td>
</tr>
<tr id="row8747925125517"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p224412412560"><a name="p224412412560"></a><a name="p224412412560"></a>查询审计日志策略</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p174715252552"><a name="p174715252552"></a><a name="p174715252552"></a>rds:auditlog:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul47173385617"></a><a name="ul47173385617"></a><ul id="ul47173385617"><li>支持：</li></ul>
<p id="p97171233569"><a name="p97171233569"></a><a name="p97171233569"></a><strong id="b1271712314569"><a name="b1271712314569"></a><a name="b1271712314569"></a>IAM</strong>项目(Project)</p>
<a name="ul371718319569"></a><a name="ul371718319569"></a><ul id="ul371718319569"><li>支持：</li></ul>
<p id="p9717439561"><a name="p9717439561"></a><a name="p9717439561"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p2748125145511"><a name="p2748125145511"></a><a name="p2748125145511"></a>GET</p>
<p id="p36631455717"><a name="p36631455717"></a><a name="p36631455717"></a>/v3/{project_id}/instances/{instance_id}/auditlog-policy</p>
</td>
</tr>
<tr id="row9216321125510"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p8216172115511"><a name="p8216172115511"></a><a name="p8216172115511"></a>获取审计日志列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p16216162115510"><a name="p16216162115510"></a><a name="p16216162115510"></a>rds:auditlog:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1064116516569"></a><a name="ul1064116516569"></a><ul id="ul1064116516569"><li>支持：</li></ul>
<p id="p66411358562"><a name="p66411358562"></a><a name="p66411358562"></a><strong id="b126411535610"><a name="b126411535610"></a><a name="b126411535610"></a>IAM</strong>项目(Project)</p>
<a name="ul19641185115618"></a><a name="ul19641185115618"></a><ul id="ul19641185115618"><li>支持：</li></ul>
<p id="p146416515619"><a name="p146416515619"></a><a name="p146416515619"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p15216202145514"><a name="p15216202145514"></a><a name="p15216202145514"></a>GET</p>
<p id="p476774316571"><a name="p476774316571"></a><a name="p476774316571"></a>/v3/{project_id}/instances/{instance_id}/auditlog?start_time={start_time}&amp;end_time={end_time}&amp;offset={offset}&amp;limit={limit}</p>
</td>
</tr>
<tr id="row16459122312559"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p13459623105511"><a name="p13459623105511"></a><a name="p13459623105511"></a>生成审计日志下载链接</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1745962325518"><a name="p1745962325518"></a><a name="p1745962325518"></a>rds:auditlog:download</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul15641125205614"></a><a name="ul15641125205614"></a><ul id="ul15641125205614"><li>支持：</li></ul>
<p id="p11641205165610"><a name="p11641205165610"></a><a name="p11641205165610"></a><strong id="b464112555617"><a name="b464112555617"></a><a name="b464112555617"></a>IAM</strong>项目(Project)</p>
<a name="ul36411518566"></a><a name="ul36411518566"></a><ul id="ul36411518566"><li>支持：</li></ul>
<p id="p164245105620"><a name="p164245105620"></a><a name="p164245105620"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p8459112315554"><a name="p8459112315554"></a><a name="p8459112315554"></a>POST</p>
<p id="p7222127125818"><a name="p7222127125818"></a><a name="p7222127125818"></a>/v3/{project_id}/instances/{instance_id}/auditlog-links</p>
</td>
</tr>
</tbody>
</table>

**表 6**  管理数据库和用户（MySQL）

<a name="table1390035014816"></a>
<table><thead align="left"><tr id="row5901175017815"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p175081791491"><a name="p175081791491"></a><a name="p175081791491"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p185081293915"><a name="p185081293915"></a><a name="p185081293915"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p19508199294"><a name="p19508199294"></a><a name="p19508199294"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p115080915916"><a name="p115080915916"></a><a name="p115080915916"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row169012502813"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1490110508814"><a name="p1490110508814"></a><a name="p1490110508814"></a>创建数据库</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p69018508817"><a name="p69018508817"></a><a name="p69018508817"></a>rds:database:create</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul44711427201618"></a><a name="ul44711427201618"></a><ul id="ul44711427201618"><li>支持：</li></ul>
<p id="p1647152741613"><a name="p1647152741613"></a><a name="p1647152741613"></a><strong id="b847192710166"><a name="b847192710166"></a><a name="b847192710166"></a>IAM</strong>项目(Project)</p>
<a name="ul147132713165"></a><a name="ul147132713165"></a><ul id="ul147132713165"><li>支持：</li></ul>
<p id="p15471727101610"><a name="p15471727101610"></a><a name="p15471727101610"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p199011650683"><a name="p199011650683"></a><a name="p199011650683"></a>POST /v3/{project_id}/instances/{instance_id}/database</p>
</td>
</tr>
<tr id="row1490155020813"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p3901205019817"><a name="p3901205019817"></a><a name="p3901205019817"></a>查询数据库列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p169011750780"><a name="p169011750780"></a><a name="p169011750780"></a>rds:database:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul16556122821616"></a><a name="ul16556122821616"></a><ul id="ul16556122821616"><li>支持：</li></ul>
<p id="p0557228171618"><a name="p0557228171618"></a><a name="p0557228171618"></a><strong id="b855718288164"><a name="b855718288164"></a><a name="b855718288164"></a>IAM</strong>项目(Project)</p>
<a name="ul1955722871610"></a><a name="ul1955722871610"></a><ul id="ul1955722871610"><li>支持：</li></ul>
<p id="p955722816166"><a name="p955722816166"></a><a name="p955722816166"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p159019501689"><a name="p159019501689"></a><a name="p159019501689"></a>GET /v3/{project_id}/instances/{instance_id}/database/detail?page={page}&amp;limit={limit}</p>
</td>
</tr>
<tr id="row290118508817"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p189019501383"><a name="p189019501383"></a><a name="p189019501383"></a>查询指定用户的已授权数据库</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p169013501186"><a name="p169013501186"></a><a name="p169013501186"></a>rds:database:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul64561729151610"></a><a name="ul64561729151610"></a><ul id="ul64561729151610"><li>支持：</li></ul>
<p id="p0456162913167"><a name="p0456162913167"></a><a name="p0456162913167"></a><strong id="b144561529131612"><a name="b144561529131612"></a><a name="b144561529131612"></a>IAM</strong>项目(Project)</p>
<a name="ul645682918169"></a><a name="ul645682918169"></a><ul id="ul645682918169"><li>支持：</li></ul>
<p id="p15456202931617"><a name="p15456202931617"></a><a name="p15456202931617"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p10901650889"><a name="p10901650889"></a><a name="p10901650889"></a>GET /v3/{project_id}/instances/{instance_id}/db_user/database?user-name={user-name}&amp;page={page}&amp;limit={limit}</p>
</td>
</tr>
<tr id="row690116506818"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p9901250983"><a name="p9901250983"></a><a name="p9901250983"></a>删除数据库</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p590185010810"><a name="p590185010810"></a><a name="p590185010810"></a>rds:database:drop</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul633743011616"></a><a name="ul633743011616"></a><ul id="ul633743011616"><li>支持：</li></ul>
<p id="p233720304163"><a name="p233720304163"></a><a name="p233720304163"></a><strong id="b53371230161615"><a name="b53371230161615"></a><a name="b53371230161615"></a>IAM</strong>项目(Project)</p>
<a name="ul17337143041610"></a><a name="ul17337143041610"></a><ul id="ul17337143041610"><li>支持：</li></ul>
<p id="p193377308167"><a name="p193377308167"></a><a name="p193377308167"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p290116509819"><a name="p290116509819"></a><a name="p290116509819"></a>DELETE /v3/{project_id}/instances/{instance_id}/database/{db_name}</p>
</td>
</tr>
<tr id="row1890195016812"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p8901105019819"><a name="p8901105019819"></a><a name="p8901105019819"></a>创建数据库用户</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p990116501080"><a name="p990116501080"></a><a name="p990116501080"></a>rds:databaseUser:create</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul868923113167"></a><a name="ul868923113167"></a><ul id="ul868923113167"><li>支持：</li></ul>
<p id="p66891731111618"><a name="p66891731111618"></a><a name="p66891731111618"></a><strong id="b1268963120165"><a name="b1268963120165"></a><a name="b1268963120165"></a>IAM</strong>项目(Project)</p>
<a name="ul10689143161610"></a><a name="ul10689143161610"></a><ul id="ul10689143161610"><li>支持：</li></ul>
<p id="p968973131611"><a name="p968973131611"></a><a name="p968973131611"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p390115502812"><a name="p390115502812"></a><a name="p390115502812"></a>POST /v3/{project_id}/instances/{instance_id}/db_user</p>
</td>
</tr>
<tr id="row1190110506819"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p16901185016818"><a name="p16901185016818"></a><a name="p16901185016818"></a>查询数据库用户列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p59017507814"><a name="p59017507814"></a><a name="p59017507814"></a>rds:databaseUser:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul148953326167"></a><a name="ul148953326167"></a><ul id="ul148953326167"><li>支持：</li></ul>
<p id="p889683217164"><a name="p889683217164"></a><a name="p889683217164"></a><strong id="b3896193212163"><a name="b3896193212163"></a><a name="b3896193212163"></a>IAM</strong>项目(Project)</p>
<a name="ul689653219169"></a><a name="ul689653219169"></a><ul id="ul689653219169"><li>支持：</li></ul>
<p id="p98964326165"><a name="p98964326165"></a><a name="p98964326165"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1590117501289"><a name="p1590117501289"></a><a name="p1590117501289"></a>GET /v3/{project_id}/instances/{instance_id}/db_user/detail?page={page}&amp;limit={limit}</p>
</td>
</tr>
<tr id="row326264631118"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1226213468118"><a name="p1226213468118"></a><a name="p1226213468118"></a>查询指定数据库的已授权用户</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p3262846121118"><a name="p3262846121118"></a><a name="p3262846121118"></a>rds:databaseUser:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul188721133121612"></a><a name="ul188721133121612"></a><ul id="ul188721133121612"><li>支持：</li></ul>
<p id="p48731733121612"><a name="p48731733121612"></a><a name="p48731733121612"></a><strong id="b1887323321615"><a name="b1887323321615"></a><a name="b1887323321615"></a>IAM</strong>项目(Project)</p>
<a name="ul19873153317168"></a><a name="ul19873153317168"></a><ul id="ul19873153317168"><li>支持：</li></ul>
<p id="p1487315335163"><a name="p1487315335163"></a><a name="p1487315335163"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p12263154613113"><a name="p12263154613113"></a><a name="p12263154613113"></a>GET /v3/{project_id}/instances/{instance_id}/database/db_user?db-name={db-name}&amp;page={page}&amp;limit={limit}</p>
</td>
</tr>
<tr id="row13416194410114"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p4416154418119"><a name="p4416154418119"></a><a name="p4416154418119"></a>删除数据库用户</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p194161244191118"><a name="p194161244191118"></a><a name="p194161244191118"></a>rds:databaseUser:drop</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul202791935151616"></a><a name="ul202791935151616"></a><ul id="ul202791935151616"><li>支持：</li></ul>
<p id="p728014358169"><a name="p728014358169"></a><a name="p728014358169"></a><strong id="b928083541614"><a name="b928083541614"></a><a name="b928083541614"></a>IAM</strong>项目(Project)</p>
<a name="ul2280133518160"></a><a name="ul2280133518160"></a><ul id="ul2280133518160"><li>支持：</li></ul>
<p id="p1528023517167"><a name="p1528023517167"></a><a name="p1528023517167"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p2416154411113"><a name="p2416154411113"></a><a name="p2416154411113"></a>DELETE /v3/{project_id}/instances/{instance_id}/db_user/{user_name}</p>
</td>
</tr>
<tr id="row862042121111"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p36210429112"><a name="p36210429112"></a><a name="p36210429112"></a>授权数据库帐号</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p16211428117"><a name="p16211428117"></a><a name="p16211428117"></a>rds:databasePrivilege:grant</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul313483611615"></a><a name="ul313483611615"></a><ul id="ul313483611615"><li>支持：</li></ul>
<p id="p213423621618"><a name="p213423621618"></a><a name="p213423621618"></a><strong id="b131345368162"><a name="b131345368162"></a><a name="b131345368162"></a>IAM</strong>项目(Project)</p>
<a name="ul12134103618168"></a><a name="ul12134103618168"></a><ul id="ul12134103618168"><li>支持：</li></ul>
<p id="p1213414364165"><a name="p1213414364165"></a><a name="p1213414364165"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p6621842121117"><a name="p6621842121117"></a><a name="p6621842121117"></a>POST /v3/{project_id}/instances/{instance_id}/db_privilege</p>
</td>
</tr>
<tr id="row7796153981119"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p18797173912113"><a name="p18797173912113"></a><a name="p18797173912113"></a>解除数据库帐号权限</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p6797739121117"><a name="p6797739121117"></a><a name="p6797739121117"></a>rds:databasePrivilege:revoke</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul112381137121612"></a><a name="ul112381137121612"></a><ul id="ul112381137121612"><li>支持：</li></ul>
<p id="p3238337201616"><a name="p3238337201616"></a><a name="p3238337201616"></a><strong id="b723814371162"><a name="b723814371162"></a><a name="b723814371162"></a>IAM</strong>项目(Project)</p>
<a name="ul1123813751615"></a><a name="ul1123813751615"></a><ul id="ul1123813751615"><li>支持：</li></ul>
<p id="p162381337141615"><a name="p162381337141615"></a><a name="p162381337141615"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p679703991117"><a name="p679703991117"></a><a name="p679703991117"></a>DELETE /v3/{project_id}/instances/{instance_id}/db_privilege</p>
</td>
</tr>
</tbody>
</table>

**表 7**  标签管理

<a name="table5868113316811"></a>
<table><thead align="left"><tr id="row198695338813"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p1586913335818"><a name="p1586913335818"></a><a name="p1586913335818"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p1986953313816"><a name="p1986953313816"></a><a name="p1986953313816"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p1386919331688"><a name="p1386919331688"></a><a name="p1386919331688"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p10869203315817"><a name="p10869203315817"></a><a name="p10869203315817"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row11869193311814"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1786923315813"><a name="p1786923315813"></a><a name="p1786923315813"></a>批量添加删除标签</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p20869633485"><a name="p20869633485"></a><a name="p20869633485"></a>rds:instance:dealTag</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul1887016338811"></a><a name="ul1887016338811"></a><ul id="ul1887016338811"><li>支持：</li></ul>
<p id="p487017331884"><a name="p487017331884"></a><a name="p487017331884"></a><strong id="b128708332086"><a name="b128708332086"></a><a name="b128708332086"></a>IAM</strong>项目(Project)</p>
<a name="ul1987013310811"></a><a name="ul1987013310811"></a><ul id="ul1987013310811"><li>支持：</li></ul>
<p id="p787015331484"><a name="p787015331484"></a><a name="p787015331484"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p13870163310815"><a name="p13870163310815"></a><a name="p13870163310815"></a>POST /v3/{project_id}/instances/{instance_id}/tags/action</p>
</td>
</tr>
<tr id="row42035991711"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1820416910172"><a name="p1820416910172"></a><a name="p1820416910172"></a>查询项目标签</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p12042913173"><a name="p12042913173"></a><a name="p12042913173"></a>rds:tag:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul108515181816"></a><a name="ul108515181816"></a><ul id="ul108515181816"><li>支持：</li></ul>
<p id="p14853116187"><a name="p14853116187"></a><a name="p14853116187"></a><strong id="b11869119187"><a name="b11869119187"></a><a name="b11869119187"></a>IAM</strong>项目(Project)</p>
<a name="ul78614111815"></a><a name="ul78614111815"></a><ul id="ul78614111815"><li>支持：</li></ul>
<p id="p17861211185"><a name="p17861211185"></a><a name="p17861211185"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p14204169101717"><a name="p14204169101717"></a><a name="p14204169101717"></a>GET</p>
<p id="p236702912186"><a name="p236702912186"></a><a name="p236702912186"></a>/v3/{project_id}/tags</p>
</td>
</tr>
</tbody>
</table>

**表 8**  任务功能

<a name="table142088242180"></a>
<table><thead align="left"><tr id="row17208202410185"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p158110336182"><a name="p158110336182"></a><a name="p158110336182"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p1581183314186"><a name="p1581183314186"></a><a name="p1581183314186"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p758163311811"><a name="p758163311811"></a><a name="p758163311811"></a>授权范围</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p205811433191811"><a name="p205811433191811"></a><a name="p205811433191811"></a>对应API接口</p>
</th>
</tr>
</thead>
<tbody><tr id="row1020842411819"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p16208102420188"><a name="p16208102420188"></a><a name="p16208102420188"></a>获取任务信息</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p52089246181"><a name="p52089246181"></a><a name="p52089246181"></a>rds:task:list</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><a name="ul98177232191"></a><a name="ul98177232191"></a><ul id="ul98177232191"><li>支持：</li></ul>
<p id="p17817923201918"><a name="p17817923201918"></a><a name="p17817923201918"></a><strong id="b108171823201919"><a name="b108171823201919"></a><a name="b108171823201919"></a>IAM</strong>项目(Project)</p>
<a name="ul1881717235192"></a><a name="ul1881717235192"></a><ul id="ul1881717235192"><li>支持：</li></ul>
<p id="p208176234198"><a name="p208176234198"></a><a name="p208176234198"></a>企业项目(Enterprise Project)</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p920982471820"><a name="p920982471820"></a><a name="p920982471820"></a>GET /v3/{project_id}/jobs?id={id}</p>
</td>
</tr>
</tbody>
</table>

