# 满优惠测试用例

###一、添加

| 测试场景                                                    | 预期结果                         |
| ----------------------------------------------------------- | -------------------------------- |
| 所有参数全部填写（活动时间，标题，优惠券面额，门槛金额...） | 正确添加                         |
| 参数为空的场景（活动时间，标题，优惠券面额，门槛金额...）   | 相应值错误返回结果               |
| 活动截止时间大于活动起始时间                                | 活动起始时间不能大于活动结束时间 |
| 活动的起始时间为2018年1月1号                                | 活动起始时间必须大于当前时间     |
| 没有登录                                                    | 无权限                           |

###二、修改

| 测试场景                                                    | 预期结果                                 |
| ----------------------------------------------------------- | ---------------------------------------- |
| 所有参数全部填写（活动时间，标题，优惠券面额，门槛金额...） | 正确添加                                 |
| 参数为空的场景（活动时间，标题，优惠券面额，门槛金额...）   | 相应值错误返回结果                       |
| 活动截止时间大于活动起始时间                                | 活动起始时间不能大于活动结束时间         |
| 活动的起始时间为2018年1月1号                                | 活动起始时间必须大于当前时间             |
| 活动已经开始了，修改优惠券                                  | 优惠券活动已经开始，不能进行编辑删除操作 |
| 登录另外一个商家账号，去修改本商家优惠券信息                | 无权操作                                 |
| 没有登录                                                    | 无权限                                   |


###三、删除

| 测试场景                               | 预期结果                           |
| -------------------------------------- | ---------------------------------- |
| 活动已经开始了，删除活动               | 活动已经开始，不能进行编辑删除操作 |
| 登录另外一个商家账号，去删除本商家活动 | 无权操作                           |
| 没有登录                               | 无权限                             |

###四、读取一行数据

| 测试场景                               | 预期结果 |
| -------------------------------------- | -------- |
| 登录另外一个商家账号，去读取本商家活动 | 无权操作 |
| 没有登录                               | 无权限   |






