---
sidebar_position: 20
sidebar_label: goto
---
# BrowserTab.goto

```python
def goto(
        self,
        url: str,
        is_wait_complete: bool = True,
        timeout: int = 30
    ) -> None
```  

将当前选项卡重定向到指定的 URL。

**参数:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp; 网站网址，例如： <https://www.bing.com>.  
    &emsp;**is_wait_complete**: bool = True  
        &emsp;&emsp; is_wait_complete 设置为定义是否等待浏览器选项卡完全加载。默认值为 True。
    &emsp;**timeout**: int  
        &emsp;&emsp;  操作超时，单位为秒，默认值为 30 秒。 

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# naviage to another website
chrome_tab.goto("https://google.com")
```