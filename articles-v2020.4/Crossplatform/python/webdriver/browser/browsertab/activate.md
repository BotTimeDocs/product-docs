
# BrowserTab.activate

```python
def activate(
        self,
        is_topmost: bool = True
    ) -> None
```  

激活浏览器选项卡。

**参数:**  
    &emsp;**is_topmost**: bool    
        &emsp;&emsp; 它定义是否将浏览器窗口设置在最顶部。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# activate the tab
chrome_tab.activate()
```