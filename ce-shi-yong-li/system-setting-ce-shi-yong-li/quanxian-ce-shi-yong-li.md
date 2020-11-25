# 权限测试用例

## 权限测试

| 测试项                 | 预期状态 | 预期消息 |
| ---------------------- | -------- | -------- |
| token错误校验          | 001      | 无权访问 |
| 不携带token校验         | 001      | 无权访问 |
| 商品管理员访问系统设置 | 001 | 无权访问 |
| 商品管理员访问商品模块 | 200 | 正常访问 |
| 超级管理员访问商品模块 | 200 | 正常访问 |
