---
sidebar_position: 23
sidebar_label: close
---
# BrowserTab.close

```python
def close(self) -> None
```  

关闭浏览器选项卡。如果没有打开的选项卡，浏览器也将关闭。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# close the tab
chrome_tab.close()
```