测试所需数据：

订单数据表

| 主键id | 订单编号     | 会员id | 会员名称     | 店铺id | 店铺名称     | 订单状态 | 支付状态 | 订单价格 | 商品数量 | 省id | 市id | 创建时间   |
| ------ | :----------- | ------ | --------- | ------ | --------- | -------- | -------- | -------- | -------- | ---- | ---- | ---------- |
| 1      | 201801 | 1      | 测试用户1     | 3     | 测试店铺1     | COMPLETE | YES      | 497.00 | 2        | 1    | 1    | 当前时间 |
| 2 | 201802 | 1 | 测试用户1 | 3 | 测试店铺1 | COMPLETE | YES | 369.00 | 2 | 1 | 1 | 当前时间 |
| 3 | 201803 | 2 | 测试用户2 | 4 | 测试店铺2 | COMPLETE | YES | 123.00 | 1 | 1 | 1 | 当前时间 |

商品数据表

| 主键id | 商品id | 商品名称  | 品牌id | 商品分类id | 商品分类路径                | 店铺id | 店铺分组id | 商品价格 | 收藏数量 | 是否上架 |
| ------ | ------ | --------- | ------ | ---------- | --------------------------- | ------ | ---------- | -------- | -------- | -------- |
| 1      | 1      | 测试商品1 | 1      | 1          | &#124;0&#124;1&#124;3&#124; | 3      | 1          | 99.00    | 99       | 1        |
| 2      | 2      | 测试商品2 | 2      | 1          | &#124;0&#124;1&#124;3&#124; | 3      | 2          | 199.00   | 199      | 1        |
| 3      | 3      | 测试商品3 | 2      | 2          | &#124;0&#124;1&#124;2&#124;     | 3      | 2          | 123.00   | 123.00   | 1        |
| 4      | 4      | 测试商品4 | 2      | 2          | &#124;0&#124;1&#124;2&#124; | 4      | 2          | 123.00   | 123.00   | 1        |

