# 测试用例所需基础数据

## 商品

| 商品id | 商品名 | 价格 | 真实库存 | 可用库存 | 店铺 | 运费 | 重量（kg\) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| xx | A | 100 | 100 | 100 | 食品酒水 | 包邮 | 0 |
| xx | B | 50 | 100 | 100 | 食品酒水 | 包邮 | 1 |
| xx | C | 20 | 100 | 100 | 自营 | 包邮 | 1 |
| xx | A1 | 100 | 100 | 100 | 食品酒水 | A模板 | 1.5 |
| xx | B1 | 50 | 100 | 100 | 食品酒水 | B模板 | 0 |
| xx | C1 | 20 | 100 | 100 | 自营 | C模板 | 0 |
| xx | D1 | 10 | 100 | 100 | 自营 | B模板 | 2.3 |
| xx | E1 | 10 | 100 | 100 | 食品酒水 | B模板 | 2.3 |



注：0重量商品是为了测试可能出现的被0除的错误

## 运费模板

| 模板名称 | 规则 | 首重/件 | 运费 | 续重/件 | 续重/件费 | 配送范围 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| A | 计重 | 1kg | 10  元 | 0.5kg | 5元 | 河北全省 |
| B | 计件 | 2件 | 15元 | 1件 | 8元 | 山西全省 |
| C | 计重 | 1kg | 20  元 | 0.5kg | 7元 | 西藏全省 |

## 会员

| 模板名称 | 规则 |  角色 |
| :--- | :--- | :--- |
| test | 111111 | 买家 |
| food | 11111 | 卖家 |



