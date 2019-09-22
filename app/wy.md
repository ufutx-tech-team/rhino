## 无忧借条
### 接口：发起信息认证
> 路由 api/task/wy/{mobile}
> mobile|string(11)|手机号

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
account|string(30)|登录账号
password|string(30)|登录密码


### 接口：查询认证信息

> 路由 api/task/wy/{mobile}
> mobile|string(11)|手机号

>方法 GET

>参数
>返回数据data说明
```
{
    "code": 1,
    "msg": "msg.info_detail",
    "data": {
        "id": 3,
        "mobile": "17097232527", 用户手机号
        "customer_id": null,
        "base": { 基本信息
            "name": "陈彬", 姓名
            "credit": "信用评级：A", 信誉等级
            "cash_amount": "5", 现金余额
            "receiver_amount": "100.02", 待回收金额
            "repay_amount": "0.00" 待支付金额
        },
        "loan": { 借贷概况
            "total_consume": "￥100.00", 共支出金额
            "total_income": "￥105.00" 共消费金额
        },
        "borrow": [ 借贷列表
            {
                "title": "借款给董海纳",
                "date_time": "2019-09-21 21:30:42",
                "amount": "-100.00"
            },
            {
                "title": "充值成功",
                "date_time": "2019-09-21 21:29:45",
                "amount": "+105.00"
            }
        ],
        "identification": null, 认证列表
        "contact": null, 联系人列表
        "created_at": "1569115529", 第一次数据爬取时间戳
        "updated_at": "1569115732", 最后一次数据更新时间戳
    }
}

```


