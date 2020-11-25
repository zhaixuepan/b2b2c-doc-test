# 商品分析，热卖商品

#### 下单金额排行前30的商品，分页数据

无参数

**提示：日期类型及年份不可为空**

按月查询时，月份为空

**提示：按月查询时，月份不可为空**

按年查询，当前年份

```json
{"data":[{"goods_name":"测试商品2",
          "goods_id":2,
          "price":199.00,
          "sum":398.00},
         {"goods_name":"测试商品3",
          "goods_id":3,
          "price":123.00,
          "sum":369.00},
         {"goods_name":"测试商品1",
          "goods_id":1,
          "price":99.00,
          "sum":99.00}],
 "page_no":1,
 "page_size":30,
 "data_total":3}
```

按月查询，当前月份

```json
{"data":[{"goods_name":"测试商品2",
          "goods_id":2,
          "price":199.00,
          "sum":398.00},
         {"goods_name":"测试商品3",
          "goods_id":3,
          "price":123.00,
          "sum":369.00},
         {"goods_name":"测试商品1",
          "goods_id":1,
          "price":99.00,
          "sum":99.00}],
 "page_no":1,
 "page_size":30,
 "data_total":3}
```



#### 下单量排行前30的商品，分页数据

无参数

**提示：日期类型及年份不可为空**

按月查询时，月份为空

**提示：按月查询时，月份不可为空**

按年查询，当前年份

```json
{"data":[{"goods_name":"测试商品3",
          "goods_id":3,
          "all_num":3},
         {"goods_name":"测试商品2",
          "goods_id":2,
          "all_num":2},
         {"goods_name":"测试商品1",
          "goods_id":1,
          "all_num":1}],
 "page_no":1,
 "page_size":30,
 "data_total":3}
```

按月查询，当前月份

```json
{"data":[{"goods_name":"测试商品3",
          "goods_id":3,
          "all_num":3},
         {"goods_name":"测试商品2",
          "goods_id":2,
          "all_num":2},
         {"goods_name":"测试商品1",
          "goods_id":1,
          "all_num":1}],
 "page_no":1,
 "page_size":30,
 "data_total":3}
```

#### 下单金额排行前30的商品，图表数据

按年查询，1980年，保证无法查询出数据，看是否有空指针等问题

```json
{"xAxis":[],"yAxis":[],"series":{"name":"总金额","data":[],"localName":[]}}
```

按年查询，当前年份

```json
{"xAxis":["1","2","3"],
 "yAxis":[],
 "series":{"name":"总金额",
           "data":["398.00","369.00","99.00"],
           "localName":["测试商品2","测试商品3","测试商品1"]
          }
}
```

按月查询，当前月份

```json
{"xAxis":["1","2","3"],
 "yAxis":[],
 "series":{"name":"总金额",
           "data":["398.00","369.00","99.00"],
           "localName":["测试商品2","测试商品3","测试商品1"]
          }
}
```

#### 下单量排行前30的商品，图表数据

按年查询，1980年，保证无法查询出数据，看是否有空指针等问题

```json
{"xAxis":[],"yAxis":[],"series":{"name":"下单量","data":[],"localName":[]}}
```

按年查询，当前年份

```json
{"xAxis":["1","2","3"],
 "yAxis":[],
 "series":{"name":"下单量",
           "data":["3","2","1"],
           "localName":["测试商品3","测试商品2","测试商品1"]
          }
}
```

按月查询，当前月份

```json
{"xAxis":["1","2","3"],
 "yAxis":[],
 "series":{"name":"下单量",
           "data":["3","2","1"],
           "localName":["测试商品3","测试商品2","测试商品1"]
          }
}
```

