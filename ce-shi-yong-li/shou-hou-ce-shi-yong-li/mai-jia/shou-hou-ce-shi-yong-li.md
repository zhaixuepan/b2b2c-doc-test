# 售后测试用例

---
#####买家登录
####一、买家申请退款


| 场景| 预期|
| :--- | :--- |
| 参数必填校验| 提示参数必填 |
| 订单无效性校验(不存在的或不属于当前会员的订单)| 订单不存在 |
| 商品无效性校验| 商品不存在 |
| 退款方式不支持原路退回则退款账号必填校验| 提示退款方式必填|
| 正确性校验| 退款信息与数据库查询相符且退款单状态为申请中 |

#### 二、买家申请退货

| 场景| 预期|
| :--- | :--- |
| 参数必填校验| 提示参数必填 |
| 订单无效性校验(不存在的或不属于当前会员的订单)| 订单不存在 |
| 商品无效性校验| 商品不存在 |
| 售后商品数量不能大于购买数量| 提示申请售后货品数量不能大于购买数量 |
| 退款方式不支持原路退回则退款账号必填校验| 提示退款方式必填|
| 正确性校验| 退款信息与数据库查询相符且退款单状态为申请中 |
#### 三、买家取消已付款的订单

| 场景| 预期|
| :--- | :--- |
| 订单无效性校验| 提示订单不存在 |
| 不是已支付状态的订单不允许操作| 提示操作不允许 |
| 退款方式不支持原路退回则退款账号必填校验| 提示退款方式必填|




