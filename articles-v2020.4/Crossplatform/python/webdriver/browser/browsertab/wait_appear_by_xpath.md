
# BrowserTab.wait_appear_by_xpath
```python
def wait_appear_by_xpath(
        self,
        xpath: str,
        wait_timeout: int = 30
    ) -> WebElement
```  

在活动浏览器中，等待元素由给定的 XPath 出现。

**参数:**  
- **xpath[Required]**: str     
    - 要查找的元素的 XPath。
- **wait_timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;[WebElement](webelement.md) 对象，如果元素未显示，则为 None 。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

#  wait element appear by XPath
webelement = chrome_tab.wait_appear_by_xpath("//*[@id=\"sb_form_q\"]")
if webelement:
    webelement.highlight()

```