# 授权登录测试用例

---
#####认证中心
#### 一、PC端发起信任登录

| 场景| 预期|
| :--- | :--- |
| 无| 无 |

#### 二、WAP端发起信任登录

| 场景| 预期|
| :--- | :--- |
| 无| 无 |

#### 三、信任登录统一回调

| 场景| 预期|
| :--- | :--- |
| 无| 无 |

#### 四、会员中心账号绑定回调地址

| 场景| 预期|
| :--- | :--- |
| 无| 无 |

####五、登录绑定

| 场景| 预期|
| :--- | :--- |
| 参数必填校验| 提示参数必填 |
| 验证码错误| 图片验证码错误|
| 用户名密码错误| 提示账号密码错误|
| 正确性校验(已绑定会员发起绑定)| 返回会员已绑定状态值|
| 正确性校验(未绑定会员发起绑定)| 返回会员登录成功状态值|

####六、WAP发送手机验证码

| 场景| 预期|
| :--- | :--- |
| 参数必填校验| 提示参数必填 |
| 图片验证码校验| 提示图片验证码错误 |

####七、WAP登录绑定

| 场景| 预期|
| :--- | :--- |
| 参数必填校验| 提示参数必填 |
| 图片验证码校验| 提示图片验证码错误 |
| 正确性校验(已绑定会员发起绑定)| 返回会员已绑定状态值|
| 正确性校验(未绑定会员发起绑定)| 返回会员登录成功状态值|

#####买家端
####一、账号绑定
| 场景| 预期|
| :--- | :--- |
| 无| 无 |
####二、会员解绑操作

| 场景| 预期|
| :--- | :--- |
| 未绑定会员发起此操作| 提示会员未绑定相关账号 |
| 30天内重复进行解绑操作| 提示30天内不可重复解绑 |
| 正确性校验| 查询会员绑定授权id为空|
####三、登录绑定openid

| 场景| 预期|
| :--- | :--- |
| 传递无效的uuid| 提示授权超时，请重新授权 |
| redis存储uuid失效| 提示授权超时，请重新授权 |
| 正确性校验| 返回绑定成功相关状态值|
####四、注册绑定openid

| 场景| 预期|
| :--- | :--- |
| 传递无效的uuid| 提示授权超时，请重新授权 |
| redis存储uuid失效| 提示授权超时，请重新授权 |
| 正确性校验| 返回绑定成功相关状态值|
#####后台

####一、编辑授权登录参数

| 场景| 预期|
| :--- | :--- |
| 无| 无 |