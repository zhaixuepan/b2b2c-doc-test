# 赠品测试用例

###一、添加

| 测试场景                                              | 预期结果       |
| ----------------------------------------------------- | -------------- |
| 所有参数全部填写（赠品名称，库存，图片，赠品金额...） | 正确添加       |
| 参数为空的场景（赠品名称，库存，图片，赠品金额...）   | 相应值错误返回 |

###二、修改

| 测试场景 | 预期结果 |
| -------- | -------- |
| 越权修改 | 无权操作 |
| 参数正确 | 正确修改 |

###三、删除

| 测试场景 | 预期结果 |
| -------- | -------- |
| 越权删除 | 无权操作 |
| 参数正确 | 正确删除 |

###四、读取一个

| 测试场景 | 预期结果 |
| -------- | -------- |
| 越权读取 | 无权操作 |
| 参数正确 | 正确读取 |

