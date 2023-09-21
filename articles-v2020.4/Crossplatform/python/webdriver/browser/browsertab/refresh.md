---
sidebar_position: 21
sidebar_label: refresh
---
# BrowserTab.refresh

```python
def refresh(self) -> None
```  

刷新当前网页。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# refresh browser tab
chrome_tab.refresh()
```