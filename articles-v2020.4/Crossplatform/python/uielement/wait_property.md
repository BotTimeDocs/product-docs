# wait_property
```python
def wait_property(
        self,
        name: str, 
        value: str, 
        wait_timeout: int = 30
    ) -> bool
```  

等待目标元素的属性在指定的超时内成为预期值。

**参数:**  
    &emsp;**name[Required]**: str  
        &emsp;&emsp; 属性名称，不同的 UI 元素可能支持不同的属性。
  

    &emsp;**value[Required]**: str  
        &emsp;&emsp; Expected property value.  
    &emsp;**timeout**: int  
        &emsp;&emsp; Wait timeout for the operation, the unit is second, and the default value is 30 seconds. 

**返回:**  
    &emsp;bool，如果 UI 元素存在且其属性值为预期值，则返回 True，否则返回 False。

**例子:**
***
```python
from clicknium import clicknium as cc, locator

tab = cc.chrome.open("https://bing.com")

tab.find_element(locator.chrome.bing.search_sb_form).wait_property("aria-expanded", "true")

```