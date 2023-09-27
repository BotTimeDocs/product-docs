
# BrowserTab.wait_disappear_by_css_selector
```python
def wait_disappear_by_css_selector(
        self,
        css_selector: str,
        wait_timeout: int = 30
    ) -> bool
```  

在活动浏览器中，等待元素被给定的 CSS 选择器消失。
**参数:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp;  用于查找元素的 CSS 选择器。
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。  

**返回:**  
    &emsp;bool, 如果元素在给定的超时内消失，则返回 True，否则返回 False。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element disappear by CSS selector
result = chrome_tab.wait_disappear_by_css_selector("#sb_form_q", wait_timeout=5)
print(result)

```