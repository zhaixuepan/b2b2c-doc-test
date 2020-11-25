# 超卖压测测试用例

## 序言

由于代码被多人修复，为保障被大家修改的代码不会造成超卖问题，特意提供这样一个文档，来制定和促销库存、商品库存 相关的测试用例。

每位开发者开发完与库存，促销相关模块，需要认真执行此测试用例，保证不出现问题才可以提交。



## 示例还原数据sql

```sql
use trade;
TRUNCATE table es_trade;
TRUNCATE table es_order;
TRUNCATE table es_order_items;
TRUNCATE table es_order_log;
TRUNCATE table es_order_meta;
TRUNCATE table es_order_out_status;
TRUNCATE table es_goods_snapshot;

#这里设置各个值需要与活动内容相对应，具体指需要自行处理	
update es_seckill set start_day = 1564070400 where seckill_id = 15;
update es_seckill_apply set time_line =1,start_day=1564070400, sold_quantity=5 where apply_id = 224;
update es_promotion_goods set start_time =1564095600,end_time = 1564153200,num=5 where pg_id = 338;

                                   
use goods;
update es_goods set quantity=10 ,enable_quantity=10 ;
update  es_goods_sku set quantity=10 ,enable_quantity=10 ;

use member;
delete from es_member where member_id!=57;
```



以上内容关键值获取：

```java
package com.enation.app.javashop.consumer.shop;

import com.enation.app.javashop.framework.util.DateUtil;

/**
 * DataGenerate
 * @author Chopper
 * @version v1.0
 * @since v7.0
 * 2019-07-29 4:05 PM
 */
public class DataGenerate {

    public static void main(String[] args) {

        long today = DateUtil.startOfTodDay();
        System.out.println("start_day:"+today);
        System.out.println("time_line:"+1);
        System.out.println("start_time:"+today);
        System.out.println("end_time:"+(today+60*60*24-100));
    }


}

```



## 示例压测Jmeter脚本

[脚本 右键另存为](./http.jmx)



## 注意事项

> 1、测试模式
> 2、把发送短信验证码的代码注释掉
> 3、找一个商品，记住skuid并修改请求的发送参数
> 4、一轮压测不能大于999，如果超过1000的压测，需要自行修改脚本 



## 场景描述

> 场景1:商品A参与秒杀活动x，商品A库存为10，参与秒杀的库存为5，压测后成交5笔秒杀活动订单，其余订单出库失败。
>
> 场景2:商品A参与秒杀活动x，商品A库存为10，参与秒杀的库存为15，压测后成交10笔秒杀活动订单，其余订单出库失败。
>
> 场景3:商品A、B 参与秒杀活动X，商品A、B库存分别为 10、20，参与秒杀的库存分别为3、10，购物车同时加入A、B两商品，压测后，成交3笔秒杀价格订单，其余订单出库失败。



