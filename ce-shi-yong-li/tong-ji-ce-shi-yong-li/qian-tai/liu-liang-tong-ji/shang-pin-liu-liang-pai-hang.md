# 商品流量排行

商家登录。

商品流量分析，获取时间周期内，流量排行前30的商品的流量数据。



| 场景                                             | 预期                                                         | 备注                   |
| ------------------------------------------------ | ------------------------------------------------------------ | ---------------------- |
| 无参数                                           | 提示：时间周期不可为空                                       |                        |
| 日期类型为day                                    | 提示：日期类型填写错误                                       |                        |
| 日期类型为YEAR，其他参数为空                     | {"xAxis":["0","1"],"yAxis":[],"series":{"name":"访问量","data":["300","150"],"localName":["华为","苹果"]}} |                        |
| 日期类型为YEAR，年份为空，月份为当前月份         | {"xAxis":["0","1"],"yAxis":[],"series":{"name":"访问量","data":["300","150"],"localName":["华为","苹果"]}} | 数据应与上一个相同     |
| 日期类型为MONTH，其他为空                        | {"xAxis":["0"],"yAxis":[],"series":{"name":"访问量","data":["300"],"localName":["华为"]}} |                        |
| 日期类型为MONTH，year为当前年份，month为当前月份 | {"xAxis":["0"],"yAxis":[],"series":{"name":"访问量","data":["300"],"localName":["华为"]}} | 数据应与上一个相同     |
| 日期类型为MONTH，year为空，month为当前年份       | 提示：按月查询时，月份不为空，年份亦不可为空                 |                        |
| 日期类型为MONTH，year为1980，月份为当前月份      | 提示：无此年份相关数据                                       | 保证库里没有1980年月表 |

无参数

**提示：时间周期不可为空**

日期类型为day

**提示：日期类型填写错误**

日期类型为YEAR，其他参数为空

```json
{
    "xAxis":["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "14", "15", "16", "17", "18", "19", "20", "21", "22", "23", "24", "25", "26", "27", "28", "29", "30"],
    "yAxis":[],
    "series":{"name":"访问量",
              "data":["300", "150", null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null],
              "localName":["华为", "苹果", null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null]
             }
}
```

日期类型为YEAR，年份为空，月份为当前月份

**与上一条数据相同**

日期类型为MONTH，其他为空

```json
{
    "xAxis":["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "14", "15", "16", "17", "18", "19", "20", "21", "22", "23", "24", "25", "26", "27", "28", "29", "30"],
    "yAxis":[],
    "series":{"name":"访问量",
              "data":["300", null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null],
              "localName":["华为", null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null, null]
             }
}
```

日期类型为MONTH，year为当前年份，month为当前月份

**与上一条数据相同**

日期类型为MONTH，year为空，month为当前年份

**提示：按月查询时，月份不为空，年份亦不可为空**

日期类型为MONTH，year为1980，月份为当前月份(保证库里没有1980年月表)

**提示：无此年份相关数据**