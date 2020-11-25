# 商品分析，商品详情

商品详情，获取近30天销售数据

所有参数为空，店铺1登录，seller_id为3

**提示：商品分类id不可为空**

cat_id=0，其他参数为空，店铺1登录，seller_id为3

```json
{"data":[{"goods_name":"测试商品1",
          "numbers":1,
          "price":99.00,
          "total_price":99.00},
         {"goods_name":"测试商品2",
          "numbers":2,
          "price":199.00,
          "total_price":398.00}],
 "page_no":1,
 "page_size":10,
 "data_total":2}
```

cat_id=0，goods_name=测试，店铺1登录，seller_id为3

```json
{"data":[{"goods_name":"测试商品1",
          "numbers":1,
          "price":99.00,
          "total_price":99.00},
         {"goods_name":"测试商品2",
          "numbers":2,
          "price":199.00,
          "total_price":398.00},
         {"goods_name":"测试商品3",
          "numbers":3,
          "price":123.00,
          "total_price":369.00}],
 "page_no":1,
 "page_size":10,
 "data_total":3}
```

cat_id=1，page_no=1,page_size=10,goods_name=测试，店铺1登录，seller_id为3

**返回2条名称包含“测试”的商品数据**

cat_id=0，goods_name=测试，店铺2登录，seller_id为4

```json
{"data":[{"goods_name":"测试商品4",
          "numbers":1,
          "price":123.00,
          "total_price":123.00}],
 "page_no":1,
 "page_size":10,
 "data_total":1}
```

