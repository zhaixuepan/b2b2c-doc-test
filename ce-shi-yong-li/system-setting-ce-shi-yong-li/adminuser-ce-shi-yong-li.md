# 管理员测试用例

## 登录

| 测试项             | 预期code | 预期消息           |
| ------------------ | -------- | ------------------ |
| 用户名为空测试     | 004      | 用户名不能为空     |
| 密码为空测试       | 004      | 密码不能为空       |
| 图片验证码为空测试 | 004      | 图片验证码不能为空 |
| uuid为空测试       | 004      | uuid不能为空       |
| 图片校验码错误校验 | 107      | 图片验证码错误     |
| 账号密码错误校验   | 918      | 管理员账号密码错误 |
| 正确校验   | 200      |  |



## 刷新token

一、refresh_token为空校验

调起刷新token api 参数refresh_token为空

预期

> code：004
>
> message:刷新token不能为空

二、refresh_token失效测试
1、将refresh_token失效时间定为20秒。

2、获取refresh_token后将refresh_token延长时间21秒。

3、执行查看返回结果

预期

> code：109
>
> message:当前token已经失效

三、refresh_token在缓存中不存在-用户登出测试

1、获取refresh_token后将refresh_token在缓存中移除。

2、执行查看结果。

预期

> code：110
>
> message:当前管理员已经退出

四、正确返回actress_token测试

携带正确refresh_token执行查看返回结果。

预期

> http状态：200
>
> 正确返回当前用户的accress_token