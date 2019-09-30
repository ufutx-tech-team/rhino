## 无忧借条
### 接口：发起信息认证
> 路由 api/task/wy/{mobile}
> 
> mobile请替换成用户的手机号，{}号需要去除

>方法 POST

>参数说明

参数名|类型|说明
---|:--:|---:
account|string(30)|登录账号
password|string(30)|登录密码


### 接口：查询认证信息

> 路由 api/task/wy/{mobile}
> 
> mobile请替换成用户的手机号，{}号需要去除

>方法 GET

>参数
>返回数据data样例及说明
```
{
    "code": 1,
    "msg": "查询信息结果详情",
    "data": [
        {
            "title": "基本信息",
            "header": [
                {
                    "label": "姓名",
                    "key": "name"
                },
                {
                    "label": "信用",
                    "key": "credit"
                },
                {
                    "label": "现金余额",
                    "key": "cash_amount"
                },
                {
                    "label": "待收金额",
                    "key": "receiver_amount"
                },
                {
                    "label": "待还金额",
                    "key": "repay_amount"
                }
            ],
            "data": {
                "name": "陈彬",
                "credit": "信用评级：A",
                "cash_amount": "5",
                "receiver_amount": "100.02",
                "repay_amount": "0.00"
            }
        },
        {
            "title": "资产概况",
            "header": [
                {
                    "label": "总支出",
                    "key": "total_consume"
                },
                {
                    "label": "总收入",
                    "key": "total_income"
                }
            ],
            "data": {
                "total_consume": "￥100.00",
                "total_income": "￥105.00"
            }
        },
        {
            "title": "借条信息",
            "header": [
                {
                    "label": "说明",
                    "key": "title"
                },
                {
                    "label": "时间",
                    "key": "date_time"
                },
                {
                    "label": "金额",
                    "key": "amount"
                }
            ],
            "data": [
                {
                    "title": "借款给董董",
                    "date_time": "2019-09-21 21:30:42",
                    "amount": "-100.00"
                },
                {
                    "title": "充值成功",
                    "date_time": "2019-09-21 21:29:45",
                    "amount": "+105.00"
                }
            ]
        },
        {
            "title": "认证信息",
            "header": [
                {
                    "label": "手机号",
                    "key": "title"
                },
                {
                    "label": "真实姓名",
                    "key": "real_name"
                },
                {
                    "label": "真实姓名是否认证",
                    "key": "real_name_status"
                },
                {
                    "label": "邮箱",
                    "key": "email"
                },
                {
                    "label": "邮箱是否认证",
                    "key": "email_binded"
                },
                {
                    "label": "身份证号",
                    "key": "id_card"
                },
                {
                    "label": "头像认证",
                    "key": "avatar"
                }
            ],
            "data": {
                "mobile": "170****2527",
                "real_name_status": "已实名",
                "bank": "未绑定",
                "email_binded": "已绑定",
                "real_name": "陈彬",
                "id_card": "3625****1213",
                "avatar": "认证通过",
                "email": "17097232527@163.com"
            }
        },
        {
            "title": "联系人",
            "header": [
                {
                    "label": "姓名",
                    "key": "name"
                },
                {
                    "label": "手机",
                    "key": "mobile"
                }
            ],
            "data": [
                {
                    "name": "陈小二",
                    "mobile": "16675351505"
                },
                {
                    "name": "胡小花",
                    "mobile": "15818544866"
                },
                {
                    "name": "王荣耀",
                    "mobile": "17782191714"
                }
            ]
        }
    ]
}
```

数据项分为三个部分
1. title 这个项目的名称
2. header 这个项目里的字段（label)和数据的key值
3. data 这个项目里的具体数值，与header里面的key值是对应的value关系
   比如最后一段数据为 title 是表示【联系人】的，数据包括 姓名(name) 与 手机号(mobile),那么从data项中，把 name 与 mobile两个数据取出来就行，因为有多条联系人信息，所以以数据的形式展示

