
# BrowserTab.wait_disappear
```python
def wait_disappear(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool
```  

等待网页的指定元素在给定的超时内消失。

>**附注:**  
`BrowserTab.wait_disappear`与 [clicknium.wait_disappear](Ma/doc/references/python/globalfunctions/wait_disappear.md) 在查找 UI 元素时有所不同。
>- `clicknium.wait_disappear()`适用于 Web 和窗口 uielement，不限于特定范围。
>- `clicknium.chrome.open("https://bing.com").wait_disappear()` 将在其父网页中查找元素。
**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string,  定位器字符串，目标 UI 元素的定位器的访问路径，例如：'locator.chrome.bing.search_sb_form_q', 定位器存储为  chrome, 定位器名称为search_sb_form_q. 
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; 定位器变量，设置为在定位器中初始化参数，例如： `{ "row": 1,  "column": 1}`
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; 等待操作超时，单位为秒，默认值为 30 秒。


**返回:**  
    &emsp;bool,如果元素在给定的超时内消失，则返回 True，否则返回 False。 

**例:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# wait element disappear
chrome_tab.wait_disappear(locator.chrome.bing.search_sb_form_q)

# parametric locator
variables = {"name":"test"}
chrome_tab.wait_disappear(locator.chrome.bing.search_sb_form_v, variables)

```