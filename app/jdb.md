## 借贷宝
### 接口：发起借贷宝信息查询
>路由 api/task/jdb/{mobile}
> 
> mobile请替换成用户的手机号，{}号需要去除

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
account|string(30)|登录账号
password|string(30)|登录密码
captcha|string(10)|用户收到的 手机验证码（第一次请求该接口，不需要传该参数，<br>用户收到了验证码之后，再调用该接口一次，需要带上该参数）


>返回数据data说明

```
注意：因为验证码的时效性 30 秒左右 
```

### 接口：发送登录手机验证码到服务器（可选单独的接口发送验证码）

> 路由 api/task/taobao/{mobile}/captcha
> 
> mobile请替换成用户的手机号，{}号需要去除

>方法 POST

>参数

参数名|类型|说明
---|:--:|---:
captcha|string(10)|发送到手机的验证码

>无返回数据data说明

### 接口：查询已经获取到的用户数据

> 路由 api/task/taobao/{mobile}
> 
> mobile请替换成用户的手机号，{}号需要去除

>方法 GET

>无参数

>返回数据data说明
```
待完成
```
