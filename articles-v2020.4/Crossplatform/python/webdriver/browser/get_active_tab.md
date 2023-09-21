---
sidebar_position: 2
sidebar_label: get_active_tab
---
# browser.get_active_tab

```python
def get_active_tab(self) -> BrowserTab
```  

获取浏览器的当前活动选项卡。

**返回:**  
    &emsp;[BrowserTab](./browsertab/browsertab.md) 对象，可以在浏览器选项卡中执行以下操作：find_element、find_elements、关闭、刷新等。

**例子:**
***
```python
from clicknium import clicknium as cc

# get browser with type chrome
browser = cc.chrome.browsers[0]

# get active tab
tab = browser.get_active_tab()

# get tab's title
title = tab.title
print(title)
```