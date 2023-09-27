
# clicknium.wait_disappear

```python
def wait_disappear(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        wait_timeout: int = 30
    ) -> bool
```

等待 UI 元素在指定的超时内消失。

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; 定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q。
<br/>
    &emsp;**locator_variables**: dict  
        &emsp;&emsp;  定位器变量，设置为在定位器中初始化参数，例如： `{ "row": 1,  "column": 1}`
<br/>
    &emsp;**wait_timeout**: int  
        &emsp;&emsp; 等待消失的超时，单位为秒，默认值为 30 秒。
<br/>

**返回:** bool  
    &emsp;如果元素在超时内消失，则返回 True，否则返回 False。


**例子:**
***
```python
from clicknium import clicknium as cc, locator

#wait element disappear
cc.wait_disappear(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.wait_disappear(locator.notepad.notepad.document_151, variables)
```