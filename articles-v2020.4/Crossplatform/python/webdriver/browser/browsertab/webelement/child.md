---
sidebar_position: 1
---
# child
```python
def child(self, index: int)
```  

获取带有索引的子元素。

> **附注:**
>- 索引从 0 开始。

**参数:**    
    &emsp;**index[Required]**: int  
        &emsp;&emsp; 指定的索引，获取第 n 个子项

**返回:**  
    &emsp;[WebElement](webelement.md) 对象（如果找到）或 None （如果未找到）



```python
from clicknium import clicknium as cc, locator, ui
    
chrome_tab = cc.chrome.open("https://bing.com")

# get web element
ele = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)

# get element's first child
first_child = ele.child[0]
```