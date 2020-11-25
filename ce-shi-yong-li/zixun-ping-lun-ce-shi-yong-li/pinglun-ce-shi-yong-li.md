# 评论测试用例

---
#####会员登录
#### 一、提交评论

| 场景| 预期|
| :--- | :--- |
|订单编号为空 | 提示订单编号不能为空 | 
|发货速度评分为空或值不正确| 提示请选择发货速度评分或发货速度评分有误 | 
|描述相符度评分为空或值不正确| 提示请选择描述相符度评分或描述相符度评分有误 | 
|描述服务评分为空或值不正确| 提示请选择描述服务评分或描述服务评分有误 | 
|商品评论为空| 提示商品评论不能为空 | 
|商品评分为空或值不正确| 提示商品评分不能为空或值不正确| 
|要评论的商品为空| 提示评论的商品不能为空| 
|不存在或者不是我的订单| 提示无权限| 
|订单中不存在的商品| 提示无权限| 
|正确添加| 状态200 |
|不是可评论的状态| 提示无权限| 


#### 二、查询我的评论列表

> 返回状态200

---

#####商家登录
#### 一、回复评论

| 场景| 预期|
| :--- | :--- |
|回复内容为空 | 提示回复内容不能为空 | 
|不存在的评论，或者不是属于我的评论| 提示无权限 | 
|正确回复| 状态200 | 
|重复回复| 提示不能重复回复 |

#### 二、查询我的评论列表

> 返回状态200

---

#####管理员登录
#### 一、查询评论列表

> 返回状态200

#### 二、删除评论
1. 两条评论数据
2. 删除后变成一条

> 返回状态200

















