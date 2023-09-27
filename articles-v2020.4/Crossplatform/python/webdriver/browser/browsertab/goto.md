
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
- **url[Required]**: str   
    - 网站网址，例如： <https://www.bing.com>.  
- **is_wait_complete**: bool = True  
    - is_wait_complete 设置为定义是否等待浏览器选项卡完全加载。默认值为 True。
- **timeout**: int  
    -  操作超时，单位为秒，默认值为 30 秒。 

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