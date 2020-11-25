# 商品收藏排行前50

商家登录。

统计商品收藏量前50个商品，按收藏数量降序排列。

## 一、图表数据

查询图表数据

```json
{"xAxis":["1","2"],
 "yAxis":[],
 "series":{"name":"收藏数",
           "data":["1221","99"],
           "localName":["测试商品3","测试商品1"]
          }
}
```



## 二、表格数据

查询表格数据，参数page_no为1，page_size为10

```json
{"data":[{"goods_name":"测试商品3",
          "price":123.00,
          "favorite_num":1221},
         {"goods_name":"测试商品1",
          "price":99.00,
          "favorite_num":99}],
 "pageNo":1,
 "pageSize":10,
 "dataTotal":2}
```

