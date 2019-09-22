## 借贷宝
### 接口：发起借贷宝信息查询
>路由 api/task/jdb/{mobile}
> mobile|string(11)|手机号

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
account|string(30)|登录账号
password|string(30)|登录密码

>返回数据data说明

参数名|类型|说明
---|:--:|---:
captcha|string(10)|NEEDED 需要前台向服务器发送验证码，如果无返回该字段则不需要验证码

### 接口：发送登录手机验证码到服务器

> 路由 api/task/taobao/{mobile}/captcha
> mobile|string(11)|手机号

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
captcha|string(10)|发送到手机的验证码

>无返回数据data说明

### 接口：查询已经获取到的用户数据

> 路由 api/task/taobao/{mobile}
> mobile|string(11)|手机号

>方法 GET

>无参数

>返回数据data说明
```
待完成
```
