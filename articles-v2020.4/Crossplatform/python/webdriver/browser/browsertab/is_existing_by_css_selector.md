---
sidebar_position: 10
sidebar_label: is_existing_by_css_selector
---
# BrowserTab.is_existing_by_css_selector
```python
def is_existing_by_css_selector(
        self,
        css_selector: str,
        timeout: int = 30
    ) -> bool
```  

在活动浏览器中，通过给定的 CSS 选择器检查 UI 元素是否存在。

**参数:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; 用于查找元素的 CSS 选择器。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。 

**返回:**  
    &emsp;如果 UI 元素存在，则返回 True，否则返回 False

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# check element if exist by CSS selector
result = chrome_tab.is_existing_by_css_selector("#sb_form_q")
print(result)

```