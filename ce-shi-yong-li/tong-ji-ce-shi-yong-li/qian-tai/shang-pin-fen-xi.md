测试所需数据

订单数据表

| 主键id | 订单编号 | 买家id | 买家名称  | 卖家id | 卖家名称  | 订单状态 | 支付状态 | 订单价格 | 商品数量 | 收货省份id | 收货城市id | 下单时间         |
| ------ | -------- | ------ | --------- | ------ | --------- | -------- | -------- | -------- | -------- | ---------- | ---------- | ---------------- |
| 1      | 201801   | 1      | 测试用户1 | 3      | 测试店铺1 | COMPLETE | PAY_YES  | 497.00   | 2        | 1          | 1          | 根据当前时间变动 |
| 2      | 201802   | 1      | 测试用户1 | 3      | 测试店铺1 | COMPLETE | PAY_YES  | 369.00   | 2        | 1          | 3          | 根据当前时间变动 |
| 3      | 201803   | 2      | 测试用户2 | 4      | 测试店铺2 | COMPLETE | PAY_YES  | 123.00   | 1        | 2          | 1          | 根据当前时间变动 |



订单商品数据表

| 主键id | 订单编号 | 商品id | 商品名称  | 商品数量 | 商品单价 | 小计   | 分类path                    | 分类id | 下单时间         | 行业id |
| ------ | -------- | ------ | --------- | -------- | -------- | ------ | --------------------------- | ------ | ---------------- | ------ |
| 1      | 201801   | 1      | 测试商品1 | 1        | 99.00    | 99.00  | &#124;0&#124;1&#124;3&#124; | 1      | 根据当前时间变动 | 1      |
| 2      | 201801   | 2      | 测试商品2 | 1        | 199.00   | 199.00 | &#124;0&#124;1&#124;3&#124; | 2      | 根据当前时间变动 | 1      |
| 3      | 201802   | 3      | 测试商品3 | 2        | 123.00   | 246.00 | &#124;0&#124;1&#124;2&#124; | 3      | 根据当前时间变动 | 1      |
| 4      | 201803   | 4      | 测试商品4 | 1        | 123.00   | 123.00 | &#124;0&#124;1&#124;2&#124; | 2      | 根据当前时间变动 | 1      |



商品数据表

| 主键id | 商品id | 商品名称  | 品牌id | 分类id | 分类path    | 商家id | 商家分组id | 商品价格 | 收藏数 | 是否上架 |
| ------ | ------ | --------- | ------ | ------ | ----------- | ------ | ---------- | -------- | ------ | -------- |
| 1      | 1      | 测试商品1 | 1      | 1      | &#124;0&#124;1&#124;3&#124; | 3      | 1          | 99.00    | 99     | 1        |
| 2      | 2      | 测试商品2 | 2      | 1      | &#124;0&#124;1&#124;3&#124; | 3      | 2          | 199.00   | 199    | 1        |
| 3      | 3      | 测试商品3 | 2      | 2      | &#124;0&#124;1&#124;2&#124; | 3      | 2          | 123.00   | 1221   | 1        |
| 4      | 4      | 测试商品4 | 2      | 2      | &#124;0&#124;1&#124;2&#124; | 4      | 2          | 123.00   | 55     | 1        |

