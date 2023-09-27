
# BrowserTab.find_element_by_css_selector
```python
def find_element_by_css_selector(
        self,
        css_selector: str
    ) -> WebElement
```  

在活动浏览器中，通过给定的CSS 选择器查找元素。

**参数:**  
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp;  要查找的元素的 CSS 选择器。

**返回:**  
    &emsp;[WebElement](webelement.md) 对象。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com")

# find element by CSS selector
webelement = chrome_tab.find_element_by_css_selector("#sb_form_q")
webelement.highlight()

```