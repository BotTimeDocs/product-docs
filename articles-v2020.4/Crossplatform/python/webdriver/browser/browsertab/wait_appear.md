---
sidebar_position: 11
sidebar_label: wait_appear
---
# BrowserTab.wait_appear
```python
def wait_appear(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> WebElement
```  

等待网页的指定元素在给定的超时内出现。

>**附注:**  
`BrowserTab.wait_appear`与 [clicknium.wait_appear](Ma/doc/references/python/globalfunctions/wait_appear.md) 在查找 UI 元素时有所不同。
>- `clicknium.wait_appear()` 适用于 Web 和窗口 UI 元素，不限于特定范围。
>- `clicknium.chrome.open("https://bing.com").wait_appear()` 将在其父网页中定位元素。 

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string, 定位器字符串，目标 UI 元素的定位器的访问路径，例如：'locator.chrome.bing.search_sb_form_q', 定位器存储为  chrome, 定位器名称为search_sb_form_q.
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables, 定位器变量，设置为在定位器中初始化参数，例如：`{ "row": 1,  "column": 1}`
    &emsp;**wait_timeout**: int  
        &emsp;&emsp;  等待操作超时，单位为秒，默认值为 30 秒。 

**返回:**  
    &emsp;[WebElement](webelement.md) 对象，如果元素未显示，则为 None 。 

**例:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# wait element appear
element = chrome_tab.wait_appear(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
element = chrome_tab.wait_appear(locator.chrome.bing.search_sb_form_q, variables)

```