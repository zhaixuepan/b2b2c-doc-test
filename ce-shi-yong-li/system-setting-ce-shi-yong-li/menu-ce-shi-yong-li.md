# 菜单管理测试用例

## 添加菜单测试

| 测试项           | 预期code | 预期消息                     |
| ---------------- | -------- | ---------------------------- |
| 父菜单id为空校验 | 004 | 父菜单id不能为空             |
| 菜单标题为空校验 | 004 | 菜单标题不能为空             |
| 菜单唯一标识为空校验 | 004 | 菜单唯一标识不能为空         |
| 权限表达式为空校验 | 004 | 权限表达式不能为空           |
| 父菜单为负数校验 | 004 | 父菜单必须为数字且不能为负数 |
| 父级菜单不存在校验 | 003 | 父级菜单不存在|
| 正确校验 | 200 |  |
| 菜单唯一标识重复校验 | 913 | 菜单唯一标识重复 |
| 菜单级别限制测试 | 914 | 菜单级别最多为3级|

## 修改菜单测试
| 测试项           | 预期code | 预期消息                     |
| ---------------- | -------- | ---------------------------- |
| 父菜单id为空校验 | 004 | 父菜单id不能为空             |
| 菜单标题为空校验 | 004 | 菜单标题不能为空             |
| 菜单唯一标识为空校验 | 004 | 菜单唯一标识不能为空         |
| 权限表达式为空校验 | 004 | 权限表达式不能为空           |
| 父菜单为负数校验 | 004 | 父菜单必须为数字且不能为负数 |
| 父级菜单不存在校验 | 003 | 父级菜单不存在|
| 当前菜单不存在校验 | 003 | 当前菜单不存在|
| 正确校验 | 200 |  |
| 菜单唯一标识重复校验 | 913 | 菜单唯一标识重复 |
| 菜单级别限制测试 | 914 | 菜单级别最多为3级|

## 删除菜单测试
| 测试项           | 预期code | 预期消息                     |
| ---------------- | -------- | ---------------------------- |
| 当期菜单不存在校验 | 003 | 当前菜单不存在      |
| 正确校验 | 200 |              |