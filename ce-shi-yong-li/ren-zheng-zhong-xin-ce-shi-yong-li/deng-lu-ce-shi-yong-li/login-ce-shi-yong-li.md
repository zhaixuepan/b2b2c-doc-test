# 登录测试用例

## 数据准备

一、开启测试模式

## 测试用例

一、用户名为空校验

| username | password | captcha | uuid   | message        |
| -------- | -------- | ------- | ------ | -------------- |
|          | 123123   | 1111    | 52c260 | 用户名不能为空 |
预期

> code：004
>
> message：用户名不能为空

二、密码为空校验

| username | password | captcha | uuid   | message      |
| -------- | -------- | ------- | ------ | ------------ |
| haobeck  |          | 1111    | 52c260 | 密码不能为空 |

预期

> code：004
>
> message：密码不能为空

三、验证码为空校验

| username | password | captcha | uuid   | message            |
| -------- | -------- | ------- | ------ | ------------------ |
| haobeck  | 123123   |         | 52c260 | 图片验证码不能为空 |

预期

> code：004
>
> message：图片验证码不能为空

四、uuid为空校验

| username | password | captcha | uuid | message      |
| -------- | -------- | ------- | ---- | ------------ |
| haobeck  | 123123   | 1111    |      | uuid不能为空 |

预期

> code：004
>
> message：uuid不能为空

五、图片验证码错误校验

| username | password | captcha | uuid   | message          |
| -------- | -------- | ------- | ------ | ---------------- |
| haobeck  | 123123   | 2222    | 52c260 | 图片验证码错误！ |

预期

> code：107
>
> message：图片验证码错误！

六、账号错误校验

| username | password | captcha | uuid   | message        |
| -------- | -------- | ------- | ------ | -------------- |
| beckhao  | 123123   | 1111    | 52c260 | 账号密码错误！ |

预期

> code：107
>
> message：账号密码错误！

七、密码错误校验

| username | password | captcha | uuid   | message        |
| -------- | -------- | ------- | ------ | -------------- |
| haobeck  | 111111   | 1111    | 52c260 | 账号密码错误！ |

预期

> code：107
>
> message：账号密码错误！

八、手机号码和密码正确登录校验

| username    | password | captcha | uuid   | message |
| ----------- | -------- | ------- | ------ | ------- |
| 18234124444 | 123123   | 1111    | 52c260 |         |

预期

> http状态：200

九、账号和密码正确登录校验

| username | password | captcha | uuid   | message |
| -------- | -------- | ------- | ------ | ------- |
| haobeck  | 123123   | 1111    | 52c260 |         |

预期

> http状态：200