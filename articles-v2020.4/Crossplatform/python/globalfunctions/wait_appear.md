
# clicknium.wait_appear
```python
def wait_appear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> UiElement
```

等待 UI 元素出现并在指定的超时内返回它。

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp;定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q
    &emsp;**locator_variables**: dict   
        定位器变量，设置为在定位器中初始化参数，例如：`{ "row": 1,  "column": 1}`
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; 等待出现的超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;[UiElement](./../uielement/uielement.md) 对象，如果元素未显示，则为 None


**例子:**
***
```python
from clicknium import clicknium as cc, locator

#wait element appear
cc.wait_appear(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.wait_appear(locator.notepad.notepad.document_151, variables)
```