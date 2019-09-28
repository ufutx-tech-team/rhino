# 犀牛信息查询文档
## 通用返回参数说明 

参数名|类型|说明
---|:--:|---:
code|enum(0,1)|0：无数据<br>1:数据正常
msg|string|返回文字说明
data|string|具体数据，JSON stringify 化了，如果 code == 0，无此字段


## 可查询第三方平台进度

平台名称|平台终端类型|是否可登录|信息内容
---|---|---|---
[淘宝](./app/taobao.md)| Web  | √ | √
[无忧借条](./app/wy.md)| App(Android) | √ | √
[今借到](./app/jjd.md)| Web | √ | X
[借贷宝](./app/jdb.md)| App(Android)| √ | √
[米房](./app/mf.md)| App | X | X
[移动](./app/mobile.md)|   | X | X
[联通](./app/unicom.md)|   | X | X
[电信](./app/telecom/.md)|   | X | X
[和通讯录](./app/htxl.md)|  App(Android) | X| X
[宜信](./app/yx.md)|  Web | X| X



## 技术实现原理
[手机端Android](./tech/app.md)
[电脑端Web](./tech/web.md)

## 平台说明
* 基于LNMP
* PHP的框架为Laravel6.0
* 前端使用Vue
