---
sidebar_position: 8
sidebar_label: is_existing
---
# BrowserTab.is_existing
```python
def is_existing(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool
```  

 检查网页的指定元素是否存在。

>**附注:**  
`BrowserTab.is_existing` 与查找 UI 元素时 [clicknium.is_existing](Ma/doc/references/python/globalfunctions/is_existing.md) 的方法不同。
>- `clicknium.is_existing()` 适用于 Web 和窗口 UI 元素，不限于特定范围。
>- `clicknium.chrome.open("https://bing.com").is_existing()` 将在其父网页中定位元素。

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string, 定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q。
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables,定位器变量，设置为在定位器中初始化参数，例如：`{ "row": 1,  "column": 1}`
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;如果 UI 元素存在，则返回 True，否则返回 False

**例:**
***
```python
from clicknium import clicknium as cc, locator, ui

chrome_tab = cc.chrome.open("https://bing.com")

# check element if exist
chrome_tab.is_existing(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
chrome_tab.is_existing(locator.chrome.bing.search_sb_form_q, variables)
```