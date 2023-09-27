
# WebElement.set property

```python
def set_property(
        self,
        name: str,
        value: str,
        timeout: int = 30
    ) -> None
```  

设置 Web 元素的属性值。

**参数:**  
- **name[Required]**: str  
    -  属性名称，不同的 UI 元素可能支持不同的属性。请参考 [Automation Concepts](concepts.md) ，根据 UI 元素类型检查属性。 
- **value[Required]**: str  
    - 属性值。
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc, locator

chrome_tab = cc.chrome.open("https://bing.com")

# set the web propery with specified value
chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).set_property("tag", "search_tag")
```