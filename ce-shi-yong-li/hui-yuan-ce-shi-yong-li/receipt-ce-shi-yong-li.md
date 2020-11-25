# 发票测试用例

## 添加发票测试

| 测试项                      | 预期code | 预期消息                                 |
| --------------------------- | -------- | ---------------------------------------- |
| 发票标题为空测试            | 004      | 发票标题不能为空                         |
| 发票内容为空测试            | 004      | 发票内容不能为空                         |
| 是否为默认发票为空测试      | 004      | 是否为默认不能为空                       |
| 是否为默认发票参数错误校验  | 004      | 是否为默认发票参数错误,1为默认,0为不默认 |
| 发票类型为空测试            | 004      | 发票类型不能为空                         |
| 发票类型参数错误校验        | 004      | 发票类型参数错误,1为单位,0为个人         |
| 发票类型为单位 税号必填校验 | 120      | 税号不能为空                             |
| 会员是否存在校验            | 003      | 当前会员不存在                           |
| 正确性校验                  | 200      |                                          |



## 修改发票测试

| 测试项 | 预期code | 预期消息 |
| ---- | ---- | ---- |
| 发票标题为空测试            | 004      | 发票标题不能为空                         |
| 发票内容为空测试            | 004      | 发票内容不能为空                         |
| 是否为默认发票为空测试      | 004      | 是否为默认不能为空                       |
| 是否为默认发票参数错误校验  | 004      | 是否为默认发票参数错误,1为默认,0为不默认 |
| 发票类型为空测试            | 004      | 发票类型不能为空                         |
| 发票类型参数错误校验        | 004      | 发票类型参数错误,1为单位,0为个人         |
| 发票类型为单位 税号必填校验 | 120      | 税号不能为空   |
| 修改不存在的发票 | 002      | 无权操作此发票  |
| 正确校验 | 200      |  |



## 删除发票测试

| 测试项                     | 预期code | 预期消息       |
| -------------------------- | -------- | -------------- |
| 删除不存在或者其他人的发票 | 002      | 无权操作此发票 |
| 正确校验                   | 200      |                |
