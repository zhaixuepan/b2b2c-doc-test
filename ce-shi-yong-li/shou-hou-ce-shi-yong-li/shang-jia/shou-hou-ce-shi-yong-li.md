# 售后测试用例

---
#####卖家登录
####一、卖家审核售后申请


| 场景| 预期|
| :--- | :--- |
| 参数必填校验| 提示参数必填 |
| 退款单无效性校验(不存在的或不属于当前会员的) | 提示退款单不存在 |
| 退款状态为申请中的退款单才允许操作| 提示操作不允许|
| 卖家修改退款金额不能大于支付金额| 提示退款金额不能大于支付金额 |
| 正确性校验(退款且支持原路退回且成功)| 退款状态变为退款中 |
| 正确性校验(退款且不支持原路退回)| 退款状态变为审核通过 |
| 正确性校验(退货申请审核)| 退款状态变为审核通过 |
| 正确性校验(原路退回退款失败校验)| 退款状态变为退款失败 |

#### 二、卖家货品入库

| 场景| 预期|
| :--- | :--- |
| 退款单有效性校验(不存在的或不属于当前会员的)| 提示退款单不存在 |
| 退款单状态为审核通过且申请为退货申请才允许次操作| 提示操作不允许|
| 入库失败校验| 提示商品入库失败，请刷新后重新操作 |
| 正确性校验(支持原路退回且成功)| 退款单状态变为退款中 |
| 正确性校验(不支持原路退回)| 退款单状态变为退货入库 |
| 正确性校验(支持原路退回且失败)| 退款单状态变为退款失败 |
#### 三、卖家退款

| 场景| 预期|
| :--- | :--- |
| 退款单有效性校验(不存在的或不属于当前会员的)| 提示退款单不存在 |
| 退款单状态为退货入库且订单为货到付款才允许操作| 提示操作不允许|
| 正确性校验| 退款单状态变为已完成 |



