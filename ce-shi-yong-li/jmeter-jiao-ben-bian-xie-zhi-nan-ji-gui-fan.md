# **Jmeter脚本编写指南及规范**

## 1 脚本地址：

svn://newsvn.javamall.com.cn/product/javamall/trunk/docs/testscript

## 2 脚手架（template.jmx）

template.jmx是为编写脚本提供的一个模板：

![](/assets/jmx模板.png)



#### 一、在这里已经定义了大部分所需的环境，直接在简单控制器里添加http请求即可。

#### 二、可以使用的变量：

1.server:域名或ip

2.port:端口号

3.location:虚拟目录

#### 三、请求示例

 ![](/assets/jmeter请求示例.png)

#### 四、导出Fragment\(测试片断\)

#### 在简单控制器上右键：

![](/assets/jmeter导出测试片段.png)



导出后以便测试人员合并在总的测试计划中

## 3 总测试计划\(v64.jmx\)

v64.jmx是一个包含了所有计划的片断的总测试计划：

 ![](/assets/jmeter总测试计划.png)

用来进行整体测试，其中的变量及其它配置和脚手架一致

## 4 规范

#### 一、脚本存放svn目录

svn://newsvn.javamall.com.cn/product/javamall/trunk/docs/testscript

#### 二、命名规范

1.脚本以&lt;业务名&gt;+.jmx命名,业务名必须是中文

2.请求以&lt;请求名&gt;命名，必须是中文

#### 三、提交规范

1.确保提交的Jmx可用，自洽，请求不出现500

如果某些测试场景存在bug还未修复，可以先禁用，再提交

2.脚手架及总体测试计划不要提交

都是在本地调试用的，普通开发人员只提交测试片断即可，总体测试计划由专门的人维护、提交

# 5 jmeter指南

#### 一、新建线程组

![](/assets/jmeter新建线程组.png)



线程数如无特殊需要为1即可

![](/assets/jmeter新建线程组2.png)



#### 二、为线程组添加“用户自定义变量”：

![](/assets/jmeter新建线程组3.png)

![](/assets/jmeter新建线程组4.png)

![](/assets/jmeter新建线程组5.png)

#### 三、添加一个简单控制器

![](/assets/jmeter添加简单控制器.png)



这个元件的目的是为了请求顺序执行

#### 四、添加http请求

![](/assets/jmeter添加http请求.png)

#### 五、包含控制器

![](/assets/jmeter添加包含控制器.png)

#### 六、断言（此方法兼备复杂式的环境）

1.流程中为某个需要的api建立循环控制器

![](/assets/jmeter添加循环控制器.png)

2.循环控制器增加HTTP请求

![](/assets/jmeter添加循环控制器2.png)

3.根据上面的HTTP请求的api，可以知道需要的参数，创建csv文件，并设置参数。

具体设置csv文件的方法，参考：

[https://www.cnblogs.com/dinghanhua/p/5647398.html](https://www.cnblogs.com/dinghanhua/p/5647398.html)

注1：filename：测试数据存放路径，若与jmx脚本同一路径可写为相对路径。

注2：csv文件中必须有”断言文本”参数。

参考csv文件：

![](/assets/jmeter参考csv文件.png)



4.根据csv文件中的行数，设置循环控制器的循环次数。

![](/assets/jmeter根据断言设置循环次数.png)

5.增加响应断言

![](/assets/jmeter增加断言响应.png)

![](/assets/jmeter增加响应断言2.png)



6.增加断言结果

![](/assets/增加断言结果.png)

#### 七、规范：

include路径要用/，而不能用\

