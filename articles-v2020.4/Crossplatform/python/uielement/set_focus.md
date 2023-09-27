# set_focus
```python
def set_focus(self, timeout: int = 30) -> None
```  

将目标元素设置为焦点状态。

**参数:**  
- **timeout**: int  
    -  操作超时，单位为秒，默认值为 30 秒。
        
**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.chrome.bing.search_sb_form_q).set_focus()
```