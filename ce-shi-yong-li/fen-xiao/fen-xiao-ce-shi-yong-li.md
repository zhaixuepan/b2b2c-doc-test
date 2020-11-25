# 分销测试用例-后台

## 下线发展

### 生成推广链接

#### 未登录生成链接

API		/distribution/su/get-short-url

参数	good_id

请求类型	POST

响应	

```
{
  "code": "1001",
  "message": "用户未登录，请登录后重试"
}
```



#### 正常生成链接

API		/distribution/su/get-short-url

参数	good_id

请求类型	POST

响应	

```
{
  "message": "/distribution/su/visit?su=J3Uzea"
}
```





### 短链接验证

#### 错误的短链接访问

API		/distribution/su//visit

参数	su

请求类型	GET

响应	

```
跳转至首页
```



#### 正常生成链接

API		/distribution/su//visit

参数	su

请求类型	GET

响应	

```
跳转至对应的页面
```





## 分销商api

### 获取推荐我的人

API		/distribution/recommend-me

参数	无

请求类型	GET

响应	

```
{
  "message": "没有推广人"
}
```





### 获取我的下线

API		/distribution/lower-list

参数	无

请求类型	GET

响应	

```
[
  {
    "id": 2,
    "lv1_id": 1,
    "lv2_id": null,
    "name": "test2",
    "current_tpl_name": "默认模版",
    "downline": 1,
    "rebate_total": 0,
    "item": [
      {
        "id": 3,
        "lv1_id": 2,
        "lv2_id": 1,
        "name": "test3",
        "current_tpl_name": "默认模版",
        "downline": 0,
        "rebate_total": 0,
        "item": null
      }
    ]
  }
]
```



## 提现

### 提现记录

API		/distribution/withdraw/apply-history

参数	pageSize/pageNo

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 1,
      "apply_money": 10,
      "status": "申请中",
      "member_id": 1,
      "member_name": "test1",
      "apply_remark": "1",
      "inspect_remark": null,
      "transfer_remark": null,
      "apply_time": null,
      "inspect_time": null,
      "transfer_time": null
    },
    {
      "id": 2,
      "apply_money": 10,
      "status": "申请中",
      "member_id": 1,
      "member_name": null,
      "apply_remark": "1",
      "inspect_remark": null,
      "transfer_remark": null,
      "apply_time": 1528159424,
      "inspect_time": 0,
      "transfer_time": 0
    },
    {
      "id": 3,
      "apply_money": 10,
      "status": "申请中",
      "member_id": 1,
      "member_name": null,
      "apply_remark": "1",
      "inspect_remark": null,
      "transfer_remark": null,
      "apply_time": 1528159432,
      "inspect_time": 0,
      "transfer_time": 0
    },
    {
      "id": 4,
      "apply_money": 10,
      "status": "申请中",
      "member_id": 1,
      "member_name": null,
      "apply_remark": "1",
      "inspect_remark": null,
      "transfer_remark": null,
      "apply_time": 1528159642,
      "inspect_time": 0,
      "transfer_time": 0
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 4
}
```

### 提现申请

#### 超出可提现金额

API		/distribution/withdraw/apply-withdraw

参数	apply_money=999999999&remark=13123

请求类型	POST

响应	

```
{
  "code": "1003",
  "message": "申请金额超出可提现金额。"
}
```

#### 正常申请

API		/distribution/withdraw/apply-withdraw

参数	apply_money=999999999&remark=13123

请求类型	POST

响应	

```
{
  "message": "已提交申请"
}
```





### 可提现金额获取

#### 正常申请

API		/distribution/withdraw/apply-withdraw

参数	无

请求类型	GET

响应

```
{
  "message": 867
}
```

### 获取提现银行卡参数

#### 正常申请

API		/distribution/withdraw/params

参数	无

请求类型	GET

响应

```
{
  "member_name": "1",
  "bank_name": "2",
  "opening_num": "3",
  "bank_card": "4"
}
```

### 保存提现银行卡参数

#### 正常申请

API		/distribution/withdraw/params

参数	memberName=1&bankName=2&openingNum=3&bankCard=4

请求类型	POST

响应

```
{
  "member_name": "1",
  "bank_name": "2",
  "opening_num": "3",
  "bank_card": "4"
}
```



## 分销商业绩

### 历史业绩

API		/distribution/bill/history

参数	无

请求类型	GET

响应

```
{
  "data": [
    {
      "total_id": 1,
      "member_id": 1,
      "member_name": "test1",
      "start_time": 1527782400,
      "end_time": 1530374399,
      "final_money": 60,
      "push_money": 120,
      "order_count": 1,
      "order_money": 10000,
      "return_order_money": 5000,
      "return_order_count": 1,
      "return_push_money": 60,
      "sn": "MEMBER111"
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 1
}
```

#### 带有会员id

API		/distribution/bill/history

参数	member_id=2

请求类型	GET

响应

```
{
  "data": [
    {
      "total_id": 1,
      "member_id": 2,
      "member_name": "test2",
      "start_time": 1527782400,
      "end_time": 1530374399,
      "final_money": 40,
      "push_money": 180,
      "order_count": 1,
      "order_money": 20000,
      "return_order_money": 10000,
      "return_order_count": 1,
      "return_push_money": 140,
      "sn": "MEMBER222"
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 1
}
```



### 业绩订单

#### 未登录

API		/distribution/bill/order-list

参数	无

请求类型	GET

响应

```
{
  "code": "1001",
  "message": "用户未登录，请登录后重试"
}
```

#### 登录，带有结算单id

API		/distribution/bill/history

参数	bill_id=2

请求类型	GET

响应

```
{
  "data": [
    {
      "sn": "sn_2222",
      "member_name": "test1",
      "point": "0%",
      "price": 50,
      "orer_price": 30000,
      "create_time": 1530254399
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 1
}
```

#### 登录，带有他人结算单id

API		/distribution/bill/history

参数	bill_id=2&member_id=2

请求类型	GET

响应

```
{
  "data": [
    {
      "sn": "sn_2222",
      "member_name": "test1",
      "point": "0%",
      "price": 100,
      "orer_price": 30000,
      "create_time": 1530254399
    },
    {
      "sn": "sn_333",
      "member_name": "test3",
      "point": "1%",
      "price": 100,
      "orer_price": 20000,
      "create_time": 1530154399
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 2
}
```





### 业绩退货订单

#### 未登录

API		/distribution/bill/sellback-order-list

参数	无

请求类型	GET

响应

```
{
  "code": "1001",
  "message": "用户未登录，请登录后重试"
}
```

#### 登录，带有结算单id

API		/distribution/bill/sellback-order-list

参数	bill_id=2

请求类型	GET

响应

```
{
  "data": [
    {
      "sn": "sn_2222",
      "member_name": "test1",
      "point": "0%",
      "price": 30,
      "orer_price": 30000,
      "create_time": 1530254399
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 1
}
```

#### 登录，带有结算单id，他人id

API		/distribution/bill/sellback-order-list

参数	bill_id=2&member_id=2

请求类型	GET

响应

```
{
  "data": [
    {
      "sn": "sn_2222",
      "member_name": "test1",
      "point": "0%",
      "price": 20,
      "orer_price": 30000,
      "create_time": 1530254399
    },
    {
      "sn": "sn_333",
      "member_name": "test3",
      "point": "0%",
      "price": 0,
      "orer_price": 20000,
      "create_time": 1530154399
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 2
}
```

### 