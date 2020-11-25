# 设置结算参数

###1、设置收货地址
| 测试场景           | 预期结果 |
| ------------------ | -------- |
| 传递会员地址ID     | 正确设置 |
| 传递其它会员地址ID | 无权操作 |

###2、设置支付方式
| 测试场景             | 预期结果 |
| -------------------- | -------- |
| 传递支付方式         | 正确设置 |
| 传递不存在的支付方式 | 参数错误 |

###3、设置发票
| 测试场景           | 预期结果                   |
| ------------------ | -------------------------- |
| 传递正确的发票信息 | 正确设置                   |
| 参数为空的校验     | 根据参数为空返回相应的提示 |

###4、设置备注
| 测试场景     | 预期结果 |
| ------------ | -------- |
| 传递备注信息 | 正确设置 |

###5、设置送货时间
| 测试场景     | 预期结果 |
| ------------ | -------- |
| 传递送货时间 | 正确设置 |

###6、使用优惠券（还未做）

| 测试场景               | 预期结果 |
| ---------------------- | -------- |
| 使用优惠券             | 正确设置 |
| 传递其他会员的优惠券ID | 无权操作 |
