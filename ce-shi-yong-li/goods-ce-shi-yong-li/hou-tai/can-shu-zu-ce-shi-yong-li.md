# 参数组测试用例

---
#####管理员登录
#### 一、添加参数组

| 场景| 预期| 
| :--- | :--- | 
| 参数组名称为空| 提示参数组名称不能为空 | 
| 关联分类为空| 提示关联的分类不能为空|
| 关联一个不存在的分类| 提示关联分类不存在|

#### 二、修改参数组

> 添加一个参数组，状态200

| 场景| 预期| 
| :--- | :--- | 
| 参数组名称为空| 提示参数组名称不能为空 | 
| 要修改的参数组不存在| 提示参数组不存在 | 
| 正确修改| 状态200| 


#### 三、上下移
| 场景| 预期| 
| :--- | :--- | 
| 排序传值关键字不正确| 提示排序传值关键字不正确 | 
| 要移动的参数组不存在| 提示参数组不存在|
| 正确操作| 状态200|











