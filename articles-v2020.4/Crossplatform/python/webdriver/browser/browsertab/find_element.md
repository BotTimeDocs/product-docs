
# BrowserTab.find_element
```python
def find_element(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {}
    ) -> WebElement
```  

返回由给定定位器定义的 Web 元素。

>**附注:**  
使用以下方法，
`BrowserTab.find_element` 与查找 UI 元素时 [clicknium.find_element](Ma/doc/references/python/globalfunctions/find_element.md) 的方法不同。  
>- `clicknium.find_element()` 适用于 Web 和窗口 UI 元素，不限于特定范围。
>- `clicknium.chrome.open("https://bing.com").find_element()` 将在其父网页中找到该元素。

**参数:**  
- **locator[Required]**: str | _Locator   
    - locator string,  定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q。
- **locator_variables**: dict  
    - locator variables,  定位器变量，设置为在定位器中初始化参数，例如：`{ "row": 1,  "column": 1}`

**返回:**  
    &emsp;[WebElement](webelement.md) 对象。

**例:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# find element
webelement = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
webelement = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q, variables)
```