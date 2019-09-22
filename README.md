# 犀牛信息查询文档
## 通用返回参数说明 

参数名|类型|说明
---|:--:|---:
code|enum(0,1)|0：无数据<br>1:数据正常
msg|string|返回文字说明
data|string|具体数据，JSON stringify 化了，如果 code == 0，无此字段

### 可查询第三方平台进度

平台名称|平台终端类型|是否可登录|信息完整
---|---|---|---
[淘宝](./app/taobao.md)| Web  | √ | X
[无忧借条](./app/wy.md)| App(Android) | √ | X
[今借到](./app/jjd.md)| Web | √ | X
[借贷宝](./app/jdb.md)| App(Android)| √ | X
[米房](./app/mf.md)| App | X | X
[移动](./app/mobile.md)|   | X | X
[联通](./app/unicom.md)|   | X | X
[电信](./app/telecom/.md)|   | X | X
[和通讯录](./app/htxl.md)|  App(Android) | X| X
