# Web 自动化测试

## 开发流程说明
1. 利用基于 pyppeteer 启动匹配版本号的Chrome浏览器，再打开想要打开的网页
2. 利用Python编写基于ChromeDriver的代码来控制Web网页元素
3. 得到页面的内容，保存它用?

## 开发环境（以开发机为例）
1. 操作系统：Mac 10.14.6 (18G95)
2. 依赖框架：[Pyppeteer](https://github.com/miyakogi/pyppeteer/ )
3. 开发语言：Python3.7
>选择pyppeteer是因为可以完全模拟人手动的操作，不会被识别为机器操作
## Python3的requirements.txt
```
pyquery==1.4.0
opencv_python==4.1.1.26
pyppeteer==0.0.25
selenium==3.141.0
numpy==1.17.2
requests==2.22.0
Pillow==6.1.0
app==0.0.1
beautifulsoup4==4.8.0
```
## 开发准备
1. 按上面的要求安装相应的包就行
2. pip3 uninstall websockets
3. pip3 install websockets==6.0
> pyppeteer 运行时有一个bug，需要跑在6.0下面才不会有问题

## 具体开发流程
1. 初始化页面
   ```
        async def init(self):
            self.browser = await launch(
                headless=False,
                userDataDir="./userdata", #可以保存登录信息，不需要再次登录
                args=["--disable-infobars", f"--window-size={self.width},{self.height}"]
            )
            # noinspection PyAttributeOutsideInit
            self.page = await self.browser.newPage()
            await self.page.setViewport({"width": self.width, "height": self.height})
            await self.page.goto(
                "https://www.jiaduobao.com/login"
            )
   ```

2. 在页面上查找元素
    
    * 使用JavaScript语句，await self.page.evaluate 执行JS语句，进行操作或者是返回属性
    ```
        await self.page.evaluate(
            'document.getElementById("J_Static2Quick").click()'
        )
        await self.page.evaluate(
            'document.querySelector("#baseInfoSet a").text'
        )
        
    ```

3. 输入数据
    * 使用 pyppeteer查找元素并且输入
    ```
    await page.type('#UserName', 'username', {'delay': 50})
    await page.type('#Password', , {'delay': 50})
   
   ```
