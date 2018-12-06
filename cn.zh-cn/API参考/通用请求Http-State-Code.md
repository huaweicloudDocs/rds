# 通用请求Http State Code<a name="zh-cn_topic_0032488240"></a>

-   正常

    <a name="t358d4a5dcdc444a0ae5d5746addad086"></a>
    <table><thead align="left"><tr id="r4e3140482c774794a0a30b7cc42e75a3"><th class="cellrowborder" valign="top" width="15.15%" id="mcps1.1.3.1.1"><p id="a74045d193fc749d48bc38ef5ec796ec3"><a name="a74045d193fc749d48bc38ef5ec796ec3"></a><a name="a74045d193fc749d48bc38ef5ec796ec3"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="84.85000000000001%" id="mcps1.1.3.1.2"><p id="afc4cb3188b714151b35f41cb46bbd413"><a name="afc4cb3188b714151b35f41cb46bbd413"></a><a name="afc4cb3188b714151b35f41cb46bbd413"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r83e2bfee354b4f07ac716ec7a50ce6ac"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.1.3.1.1 "><p id="a1f594cf608854e7eb4043ba65b58faa8"><a name="a1f594cf608854e7eb4043ba65b58faa8"></a><a name="a1f594cf608854e7eb4043ba65b58faa8"></a>200</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.85000000000001%" headers="mcps1.1.3.1.2 "><p id="a008f88735a2843bfb7587eb313089c41"><a name="a008f88735a2843bfb7587eb313089c41"></a><a name="a008f88735a2843bfb7587eb313089c41"></a>请求成功。</p>
    </td>
    </tr>
    <tr id="r652bfee643504a68a0fc4a42c525a43d"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0032348717_p99677423540"><a name="zh-cn_topic_0032348717_p99677423540"></a><a name="zh-cn_topic_0032348717_p99677423540"></a>202</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.85000000000001%" headers="mcps1.1.3.1.2 "><p id="ac94b5793706944caa61c99a1afca14f8"><a name="ac94b5793706944caa61c99a1afca14f8"></a><a name="ac94b5793706944caa61c99a1afca14f8"></a>异步请求成功提交（创建实例，创建备份等）。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   异常

    <a name="te8d4132a26d445d1a0dc4fc4d8f34323"></a>
    <table><thead align="left"><tr id="r722db22d59954973bb58c915861501c7"><th class="cellrowborder" valign="top" width="43.43%" id="mcps1.1.3.1.1"><p id="a2d3711ae629044feb186972dd7888a63"><a name="a2d3711ae629044feb186972dd7888a63"></a><a name="a2d3711ae629044feb186972dd7888a63"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.57%" id="mcps1.1.3.1.2"><p id="a47fea807dcc443beacccc63977c085b1"><a name="a47fea807dcc443beacccc63977c085b1"></a><a name="a47fea807dcc443beacccc63977c085b1"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r631b6ae316a64f9b93d66309ca538c87"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a280c5741cceb481fa6f3bd4b8e34e47d"><a name="a280c5741cceb481fa6f3bd4b8e34e47d"></a><a name="a280c5741cceb481fa6f3bd4b8e34e47d"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="ab572970f522f43de82fa9ec3ddf3e148"><a name="ab572970f522f43de82fa9ec3ddf3e148"></a><a name="ab572970f522f43de82fa9ec3ddf3e148"></a>服务器未能处理请求。</p>
    </td>
    </tr>
    <tr id="r85f42209f3504073a09df632b14f61b1"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="af9ca2e93df5e48168b6613a39ac968ac"><a name="af9ca2e93df5e48168b6613a39ac968ac"></a><a name="af9ca2e93df5e48168b6613a39ac968ac"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a10d20f6970f047a1b5a12362e7ecae61"><a name="a10d20f6970f047a1b5a12362e7ecae61"></a><a name="a10d20f6970f047a1b5a12362e7ecae61"></a>被请求的页面需要用户名和密码。</p>
    </td>
    </tr>
    <tr id="r77729da17136497a998d69788b890fda"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a756815e4b1dc4d6586588410144cd746"><a name="a756815e4b1dc4d6586588410144cd746"></a><a name="a756815e4b1dc4d6586588410144cd746"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a782814a9a659431da4f69605507a89ef"><a name="a782814a9a659431da4f69605507a89ef"></a><a name="a782814a9a659431da4f69605507a89ef"></a>对被请求页面的访问被禁止。</p>
    </td>
    </tr>
    <tr id="r8f8ab1aea00745d9ac258eb910ed1d40"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="aaba62536a2434b2ea06b00edc909ac4d"><a name="aaba62536a2434b2ea06b00edc909ac4d"></a><a name="aaba62536a2434b2ea06b00edc909ac4d"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="ab894d89a43fc472f8fc0ba1b69d55cd6"><a name="ab894d89a43fc472f8fc0ba1b69d55cd6"></a><a name="ab894d89a43fc472f8fc0ba1b69d55cd6"></a>服务器无法找到被请求的页面。</p>
    </td>
    </tr>
    <tr id="r8dc5af7dd7e249198a03652545ef0d5a"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a3b1351d5e2e94f3bafa595b05c1b6832"><a name="a3b1351d5e2e94f3bafa595b05c1b6832"></a><a name="a3b1351d5e2e94f3bafa595b05c1b6832"></a>405 Method Not Allowed</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a5c702f29e120421cb643e05d84ee5710"><a name="a5c702f29e120421cb643e05d84ee5710"></a><a name="a5c702f29e120421cb643e05d84ee5710"></a>请求中指定的方法不被允许。</p>
    </td>
    </tr>
    <tr id="r130f3e8eca0343d2a9c8500b9958d880"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a1d2746b543384b629e11a27e7cd176c0"><a name="a1d2746b543384b629e11a27e7cd176c0"></a><a name="a1d2746b543384b629e11a27e7cd176c0"></a>409 Conflict</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a39fb4dc6b8bd4bc4ace1c4965792b622"><a name="a39fb4dc6b8bd4bc4ace1c4965792b622"></a><a name="a39fb4dc6b8bd4bc4ace1c4965792b622"></a>由于冲突，请求无法被完成。</p>
    </td>
    </tr>
    <tr id="r7c8941566af940c0b426ef42e4b700d1"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a11a3fe721bd84e77a50691954368b3fb"><a name="a11a3fe721bd84e77a50691954368b3fb"></a><a name="a11a3fe721bd84e77a50691954368b3fb"></a>413 Request Entity Too Large</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a96df5b5e62544d988f46c19930ac8c9a"><a name="a96df5b5e62544d988f46c19930ac8c9a"></a><a name="a96df5b5e62544d988f46c19930ac8c9a"></a>请求超过资源配额。</p>
    </td>
    </tr>
    <tr id="r7fccf68eac3448f2bbc463f4f43b78f0"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a877d6cff7d9c42ca94e4425554063b98"><a name="a877d6cff7d9c42ca94e4425554063b98"></a><a name="a877d6cff7d9c42ca94e4425554063b98"></a>415 Unsupported Media Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="ada3dd217c6cd4f4abf0173ab06bf0cdd"><a name="ada3dd217c6cd4f4abf0173ab06bf0cdd"></a><a name="ada3dd217c6cd4f4abf0173ab06bf0cdd"></a>请求头中携带的ContentType类型不正确，必须为application/json。</p>
    </td>
    </tr>
    <tr id="row6694549511136"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="p5387605111136"><a name="p5387605111136"></a><a name="p5387605111136"></a>422 Unprocessable Entity</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="p188397811136"><a name="p188397811136"></a><a name="p188397811136"></a>请求中的参数或对象不能被正确识别。</p>
    </td>
    </tr>
    <tr id="rea23c65235c744b783072fcbb4a2f3d9"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a170d319667ab4403810b3434132fef67"><a name="a170d319667ab4403810b3434132fef67"></a><a name="a170d319667ab4403810b3434132fef67"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a0c68b600fcd94ec2a23429f02d3759b2"><a name="a0c68b600fcd94ec2a23429f02d3759b2"></a><a name="a0c68b600fcd94ec2a23429f02d3759b2"></a>请求未完成。服务异常。</p>
    </td>
    </tr>
    <tr id="r6beeecbe12374b0eb072632ef66c02d6"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a320245dd5f24452b9b073656c5625cfe"><a name="a320245dd5f24452b9b073656c5625cfe"></a><a name="a320245dd5f24452b9b073656c5625cfe"></a>501 Not Implemented</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a06359b10519c4fc4807b4b325ba1682d"><a name="a06359b10519c4fc4807b4b325ba1682d"></a><a name="a06359b10519c4fc4807b4b325ba1682d"></a>请求未完成。服务器不支持所请求的功能。</p>
    </td>
    </tr>
    <tr id="r417724dfce2846ba96672c3bfee93331"><td class="cellrowborder" valign="top" width="43.43%" headers="mcps1.1.3.1.1 "><p id="a0822631faf55440dbbe97df43acb20c1"><a name="a0822631faf55440dbbe97df43acb20c1"></a><a name="a0822631faf55440dbbe97df43acb20c1"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.57%" headers="mcps1.1.3.1.2 "><p id="a34ca8a911bb344399804487250ea11e4"><a name="a34ca8a911bb344399804487250ea11e4"></a><a name="a34ca8a911bb344399804487250ea11e4"></a>请求未完成。系统暂时异常。</p>
    </td>
    </tr>
    </tbody>
    </table>


