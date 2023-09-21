---
sidebar_position: 15
sidebar_label: wait_disappear_by_xpath
---
# BrowserTab.wait_disappear_by_xpath
```python
def wait_disappear_by_xpath(
        self,
        xpath: str,
        wait_timeout: int = 30
    ) -> bool
```  

在活动浏览器中，等待元素在给定的 XPath 中消失。

**参数:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; 要查找的元素的 XPath。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;bool, 如果元素在给定的超时内消失，则返回 True，否则返回 False。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# wait element disappear by XPath
result = chrome_tab.wait_disappear_by_xpath("//*[@id=\"sb_form_q\"]", wait_timeout=5)
print(result)

```