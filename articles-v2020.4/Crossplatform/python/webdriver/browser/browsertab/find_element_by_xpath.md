
# BrowserTab.find_element_by_xpath
```python
def find_element_by_xpath(
        self,
        xpath: str
    ) -> WebElement
```  

在活动浏览器中，通过给定的 XPath 查找元素。

**参数:**  
- **xpath[Required]**: str     
    - 要查找的元素的 XPath。

**返回:**  
    &emsp;[WebElement](webelement.md) 对象。
**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# find element by XPath
webelement = chrome_tab.find_element_by_xpath("//*[@id=\"sb_form_q\"]")
webelement.highlight()

```