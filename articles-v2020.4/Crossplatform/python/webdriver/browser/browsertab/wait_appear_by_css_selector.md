
# BrowserTab.wait_appear_by_css_selector
```python
def wait_appear_by_css_selector(
        self,
        css_selector: str,
        wait_timeout: int = 30
    ) -> WebElement
```  

在活动浏览器中，等待给定的 CSS 选择器显示元素。

**参数:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; 用于查找元素的 CSS 选择器。 
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;[WebElement](webelement.md) 对象，如果元素未显示，则为 None 。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element appear by CSS selector
webelement = chrome_tab.wait_appear_by_css_selector("#sb_form_q")
if webelement:
    webelement.highlight()

```