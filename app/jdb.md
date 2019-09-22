## 借贷宝
### 接口：发起淘宝信息查询
>路由 api/task/jdb

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
mobile|string(11)|手机号

>返回数据data说明

参数名|类型|说明
---|:--:|---:
qrcode|string(255)|需要使用手机淘宝扫码的登录二维码，有效期40秒

### 查询淘宝信息

>路由 api/task/taobao/{mobile} 
>
>mobile为用户手机号

>方法 GET

>返回数据data说明

参数名|类型|说明
---|:--:|---:




## 无忧借条
### 接口：发起信息查询
>路由 api/task/wy

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
mobile|string(11)|手机号
account|string(30)|登录账号
password|string(30)|登录密码

>返回数据data说明

参数名|类型|说明
---|:--:|---:



