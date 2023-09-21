---
sidebar_position: 5
sidebar_label: close
---
# browser.close

```python
def close(self, is_force: bool = False) -> None
```  

关闭浏览器。

**参数:**  
    &emsp;**is_force**: bool，强制关闭浏览器.    

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# close the browser
chrome_tab.browser.close()

# open ie browser
ie_tab = cc.ie.open("https://www.bing.com")

# close the browser
ie_tab.browser.close(true)
```