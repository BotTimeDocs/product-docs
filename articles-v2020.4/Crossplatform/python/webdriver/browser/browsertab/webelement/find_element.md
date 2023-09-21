---
sidebar_position: 3
sidebar_label: find_element
---
# WebElement.find_element
```python
def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> WebElement
```  

返回由给定定位器locator定义的 Web 元素。

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; locator string, 目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q。
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; locator variables, 设置为在定位器中初始化参数，例如：eg: `{ "row": 1,  "column": 1}`
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;[WebElement](webelement.md) 对象。

**例:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# find element
webelement = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)

# find sub element   
subelement = webelement.find_element(locator.chrome.bing.search_icon)

```