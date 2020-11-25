# 手机登录测试用例

## 数据准备

一、开启测试模式

## 测试用例

一、短信验证码为空校验

| sms_code | mobile      | message            |
| -------- | ----------- | ------------------ |
|          | 18234124444 | 短信验证码不能为空 |

预期

> code：004
>
> message：短信验证码不能为空

二、短信验证码错误校验

| sms_code | mobile      | message          |
| -------- | ----------- | ---------------- |
| 123123   | 18234124444 | 短信验证码错误！ |

预期

> code：107
>
> message：短信验证码错误！

三、手机号码格式校验

| sms_code | mobile    | message          |
| -------- | --------- | ---------------- |
| 1111     | 182341244 | 短信验证码错误！ |

预期

> code：107
>
> message：短信验证码错误！

四、正确校验

| sms_code | mobile      | message |
| -------- | ----------- | ------- |
| 1111     | 18234124444 |         |

预期

> http状态：200