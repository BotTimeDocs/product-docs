# get_property
```python
def get_property(
        self,
        name: str,
        timeout: int = 30
    ) -> str
``` 

获取目标元素的属性值。

**参数:**   
- **name [Required]**: str  
    - 属性名称，不同的 UI 元素可能支持不同的属性。
- **timeout**: int  
    -  操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;str

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui
    
tag = ui(locator.chrome.bing.search_sb_form_q).get_property("tag")
```