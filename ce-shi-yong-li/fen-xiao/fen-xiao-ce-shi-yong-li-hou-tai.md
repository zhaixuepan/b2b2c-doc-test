# 分销测试用例-后台

## 分销模版管理

### 获取模版列表

#### 无参数获取列表

API		/backend/distribution/commission-tpl

参数	无

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 1,
      "tpl_name": "模版1",
      "tpl_describe": "",
      "switch_model": "MANUAL",
      "profit": 999,
      "num": 1,
      "cycle": 111,
      "grade1": 1,
      "grade2": 5,
      "is_default": 1
    },
    {
      "id": 2,
      "tpl_name": "模版2",
      "tpl_describe": "",
      "switch_model": "MANUAL",
      "profit": 9999,
      "num": 2,
      "cycle": 222,
      "grade1": 2,
      "grade2": 4,
      "is_default": 0
    },
    {
      "id": 3,
      "tpl_name": "模版3",
      "tpl_describe": "",
      "switch_model": "MANUAL",
      "profit": 99991,
      "num": 3,
      "cycle": 555,
      "grade1": 3,
      "grade2": 3,
      "is_default": 0
    },
    {
      "id": 4,
      "tpl_name": "模版4",
      "tpl_describe": "",
      "switch_model": "AUTOMATIC",
      "profit": 99992,
      "num": 4,
      "cycle": 333,
      "grade1": 4,
      "grade2": 2,
      "is_default": 0
    },
    {
      "id": 5,
      "tpl_name": "模版5",
      "tpl_describe": "",
      "switch_model": "AUTOMATIC",
      "profit": 99993,
      "num": 5,
      "cycle": 444,
      "grade1": 5,
      "grade2": 1,
      "is_default": 0
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 5
}
```

#### 分页参数获取列表

API		/backend/distribution/commission-tpl

参数	page_size=2&page_no=2

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 3,
      "tpl_name": "模版3",
      "tpl_describe": "",
      "switch_model": "MANUAL",
      "profit": 99991,
      "num": 3,
      "cycle": 555,
      "grade1": 3,
      "grade2": 3,
      "is_default": 0
    },
    {
      "id": 4,
      "tpl_name": "模版4",
      "tpl_describe": "",
      "switch_model": "AUTOMATIC",
      "profit": 99992,
      "num": 4,
      "cycle": 333,
      "grade1": 4,
      "grade2": 2,
      "is_default": 0
    }
  ],
  "page_no": 2,
  "page_size": 2,
  "data_total": 5
}
```

### 获取某个模版

#### 路径参数1 获取模版

API		/backend/distribution/commission-tpl/{tplId}

参数	1

请求类型	GET

响应	

```
{
  "id": 1,
  "tpl_name": "模版1",
  "tpl_describe": "",
  "switch_model": "MANUAL",
  "profit": 999,
  "num": 1,
  "cycle": 111,
  "grade1": 1,
  "grade2": 5,
  "is_default": 1
}
```

#### 路径参数 999 获取不存在模版

API		/backend/distribution/commission-tpl/{tplId}

参数	999

请求类型	GET

响应	

```
无
```

### 新增模版

#### 标准新增

API			/backend/distribution/commission-tpl

参数	tplName=测试模版&tplDescribe=模版描述switchModel=MANUAL&profit=999.99&num=999&grade1=1&grade2=2&isDefault=1

请求类型		POST

响应		

```
{
  "id": 0,
  "tpl_name": "测试模版",
  "tpl_describe": "模版描述",
  "switch_model": "MANUAL",
  "profit": 999.99,
  "num": 999,
  "grade1": 1,
  "grade2": 2,
  "is_default": 1
}
```

#### 参数缺少

API			/backend/distribution/commission-tpl

请求类型		POST

响应		

```
{
  "code": "004",
  "message": "切换模式不能为空 "
}
```

```
{
  "code": "004",
  "message": "下线人数 不能为空"
}
```

```
{
  "code": "004",
  "message": "相差1级返利金额 不能为空"
}
```

```
{
  "code": "004",
  "message": "相差2级返利金额 不能为空"
}
```

```
{
  "code": "004",
  "message": "利润要求不能为空"
}
```

```
{
  "code": "004",
  "message": "模版名称不能为空"
}
```

```
{
  "code": "004",
  "message": "默认参数不能为空"
}
```



### 修改模版

#### 标准参数

API			/backend/distribution/commission-tpl/1

参数	tplName=修改模版名称&tplDescribe=修改模版描述switchModel=MANUAL&profit=999&num=100&grade1=3&grade2=6&isDefault=1

请求类型		PUT

响应		

```
{
  "id": 0,
  "tpl_name": "修改模版名称",
  "tpl_describe": "修改模版描述",
  "switch_model": "MANUAL",
  "profit": 999,
  "num": 100,
  "grade1": 3,
  "grade2": 6,
  "is_default": 1
}
```

#### 

#### 参数缺少

API			/backend/distribution/commission-tpl/1

请求类型		PUT

响应		

```
{
  "code": "004",
  "message": "切换模式不能为空 "
}
```

```
{
  "code": "004",
  "message": "下线人数 不能为空"
}
```

```
{
  "code": "004",
  "message": "相差1级返利金额 不能为空"
}
```

```
{
  "code": "004",
  "message": "相差2级返利金额 不能为空"
}
```

```
{
  "code": "004",
  "message": "利润要求不能为空"
}
```

```
{
  "code": "004",
  "message": "模版名称不能为空"
}
```

```
{
  "code": "004",
  "message": "默认参数不能为空"
}
```

### 删除模版

API		/backend/distribution/commission-tpl/2

参数	2（路径参数）

响应	

```
200
```

#### 删除模版，模版不存在

API		/backend/distribution/commission-tpl/9999

参数	9999（路径参数）

响应	

```
{
  "code": "1000",
  "message": "分销业务异常，请稍后重试。"
}
```



## 分销模版升级日志

### 升级日志列表

#### 无参数获取列表

API		/backend/distribution/upgradelog

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 1,
      "member_id": 1,
      "member_name": "liushuai",
      "type": "手动",
      "old_tpl_id": 1,
      "old_tpl_name": "1",
      "new_tpl_id": 2,
      "new_tpl_name": "1",
      "create_time": 1528133650
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 1
}
```

### 升级日志列表

#### 会员参数参数获取列表

API		/backend/distribution/upgradelog?member_name=test

请求类型	GET

响应	

```
{
  "data": [],
  "page_no": 1,
  "page_size": 10,
  "data_total": 0
}
```

## 提现申请

### 提现获取列表

API		/backend/distribution/withdraw/apply

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 1,
      "apply_money": 10,
      "status": "已转账",
      "member_id": 1,
      "member_name": "test1",
      "apply_remark": "1",
      "inspect_remark": "转账备注",
      "transfer_remark": "转账备注",
      "apply_time": 1528159424,
      "inspect_time": 1528724535,
      "transfer_time": 1528724845
    },
    {
      "id": 2,
      "apply_money": 10,
      "status": "审核失败",
      "member_id": 2,
      "member_name": "test2",
      "apply_remark": "1",
      "inspect_remark": "审核备注",
      "transfer_remark": null,
      "apply_time": 1528159424,
      "inspect_time": 1528724863,
      "transfer_time": 0
    },
    {
      "id": 3,
      "apply_money": 10,
      "status": "审核成功",
      "member_id": 1,
      "member_name": "test1",
      "apply_remark": "1",
      "inspect_remark": "审核备注",
      "transfer_remark": null,
      "apply_time": 1528159432,
      "inspect_time": 1528724561,
      "transfer_time": 0
    },
    {
      "id": 4,
      "apply_money": 10,
      "status": "申请中",
      "member_id": 2,
      "member_name": "test2",
      "apply_remark": "1",
      "inspect_remark": null,
      "transfer_remark": null,
      "apply_time": 1528159642,
      "inspect_time": 0,
      "transfer_time": 0
    },
    {
      "id": 5,
      "apply_money": 123,
      "status": "申请中",
      "member_id": 1,
      "member_name": "test1",
      "apply_remark": "13123",
      "inspect_remark": null,
      "transfer_remark": null,
      "apply_time": 1528333714,
      "inspect_time": 0,
      "transfer_time": 0
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 5
}
```





### 审核提现申请

#### 审核提现

API		/backend/distribution/withdraw/auditing

请求类型	POST

响应	

> 状态值：200

#### 重复申请

```
{
  "code": "1002",
  "message": "提现申请不可以重复操作。"
}
```

#### 错误的状态参数

```
{
  "code": "1000",
  "message": "分销业务异常，请稍后重试。"
}
```

#### 不存在的申请

```
{
  "code": "1004",
  "message": "错误的提现申请。"
}
```

### 提现转账

#### 提现转账

API		/backend/distribution/withdraw/account/end

请求类型	POST

响应	

> 状态值：200

#### 重复申请

```
{
  "code": "1002",
  "message": "提现申请不可以重复操作。"
}
```

#### 错误的参数

```
{
  "code": "1000",
  "message": "分销业务异常，请稍后重试。"
}
```

#### 不存在的申请

```
{
  "code": "1004",
  "message": "错误的提现申请。"
}
```





## 总结算单

API		/backend/distribution/bill/total

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 1,
      "start_time": 1527782400,
      "end_time": 1530374399,
      "order_count": 1,
      "final_money": 100,
      "push_money": 300,
      "order_money": 10000,
      "return_order_money": 200,
      "return_order_count": 1,
      "return_push_count": 1,
      "sn": "TOTAL123"
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 1
}
```

#### 

## 会员结算单

### 无总结算单参数的异常请求

API		/backend/distribution/bill/member

请求类型	GET

响应	

```
{
  "code": "1000",
  "message": "分销业务异常，请稍后重试。"
}
```

### 普通请求

API		/backend/distribution/bill/member

参数	total_id=1

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
    },
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
  "data_total": 2
}
```

#### 

### 普通请求追加会员名

API		/backend/distribution/bill/member

参数	total_id=1&member_name=1

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

#### 

## 分销商管理

### 无总结算单参数的异常请求

API		/backend/distribution/member

请求类型	GET

响应	

```
{
  "data": [
    {
      "id": 1,
      "lv1_id": null,
      "lv2_id": null,
      "name": "test1",
      "current_tpl_name": "1",
      "downline": 1,
      "rebate_total": 0,
      "item": null
    },
    {
      "id": 2,
      "lv1_id": 1,
      "lv2_id": null,
      "name": "test2",
      "current_tpl_name": "默认模版",
      "downline": 1,
      "rebate_total": 0,
      "item": null
    },
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
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 3
}
```



## 修改分销商模版

### 无会员id参数的异常请求

API		/backend/distribution/member/tpl

请求类型	POST

响应

```
{
  "code": "1011",
  "message": "参数不足!"
}
```

### 无模版id参数的异常请求

API		/backend/distribution/member/tpl

请求类型	POST

响应

```
{
  "code": "1011",
  "message": "参数不足!"
}

```

### 普通请求

API		/backend/distribution/member/tpl

请求类型	POST

响应

> 状态值 200





## 分销设置

### 分销设置参数获取

API		/settings/distribution

请求类型	GET

响应

```
{
  "cycle": 30,
  "goods_model": 0
}
```

### 分销设置参数设置

API		/settings/distribution?cycle=120&goods_model=1

请求类型	POST

响应

```
{
  "cycle": 120,
  "goods_model": 1
}
```



## 分销统计

### 分销订单金额统计

#### 无会员id

API		/backend/distribution/statistic/order

请求类型	GET

响应

```
{
	"code":"1011","message":"参数不足!"
}
```

#### 普通请求

API		/backend/distribution/statistic/order?member_id=1

请求类型	GET

响应

```
{
  "xAxis": [
    "1",
    "2",
    "3",
    "4",
    "5",
    "6",
    "7",
    "8",
    "9",
    "10",
    "11",
    "12"
  ],
  "yAxis": [],
  "series": {
    "name": "订单金额统计",
    "data": [
      "0",
      "0",
      "0",
      "0",
      "0",
      "30000.00",
      "0",
      "0",
      "0",
      "0",
      "0",
      "0"
    ],
    "localName": []
  }
}
```



### 分销订单数量统计

#### 无会员id

API		/backend/distribution/statistic/count

请求类型	GET

响应

```
{
	"code":"1011","message":"参数不足!"
}
```

#### 普通请求

API		/backend/distribution/statistic/count?member_id=1

请求类型	GET

响应

```
{
  "xAxis": [
    "1",
    "2",
    "3",
    "4",
    "5",
    "6",
    "7",
    "8",
    "9",
    "10",
    "11",
    "12"
  ],
  "yAxis": [],
  "series": {
    "name": "订单数量统计",
    "data": [
      "0",
      "0",
      "0",
      "0",
      "0",
      "1",
      "0",
      "0",
      "0",
      "0",
      "0",
      "0"
    ],
    "localName": []
  }
}
```



### 分销订单返现统计

#### 无会员id

API		/backend/distribution/statistic/order

请求类型	GET

响应

```
{
	"code":"1011","message":"参数不足!"
}
```

#### 普通请求

API		/backend/distribution/statistic/order?member_id=1

请求类型	GET

响应

```
{
  "xAxis": [
    "1",
    "2",
    "3",
    "4",
    "5",
    "6",
    "7",
    "8",
    "9",
    "10",
    "11",
    "12"
  ],
  "yAxis": [],
  "series": {
    "name": "订单提成统计",
    "data": [
      "0.0",
      "0.0",
      "0.0",
      "0.0",
      "50.0",
      "0.0",
      "0.0",
      "0.0",
      "0.0",
      "0.0",
      "0.0",
      "0"
    ],
    "localName": []
  }
}
```



## 店铺返现统计

API		/backend/distribution/statistic/push/seller

请求类型	GET

响应

```
{
  "data": [
    {
      "push_money": 100,
      "seller_name": "test",
      "seller_id": "1"
    },
    {
      "push_money": 150,
      "seller_name": "test2",
      "seller_id": "2"
    }
  ],
  "page_no": 1,
  "page_size": 10,
  "data_total": 2
}
```