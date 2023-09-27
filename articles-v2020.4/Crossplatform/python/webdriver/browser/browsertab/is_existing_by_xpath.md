
# BrowserTab.is_existing_by_xpath
```python
def is_existing_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> bool
```  

在活动浏览器中，检查给定的 XPath 是否存在 UI 元素。

**参数:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; 要查找的元素的 XPath。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;如果 UI 元素存在，则返回 True，否则返回 False

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# check element if exist by XPath
result = chrome_tab.is_existing_by_xpath("//*[@id=\"sb_form_q\"]")
print(result)

```