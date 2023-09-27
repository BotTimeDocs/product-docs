# hover
```python
def hover(self, timeout: int = 30) -> None
```  

将鼠标悬停在元素上，鼠标将移动到元素上并停留一段时间。

**参数:**    
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例子:**
***
- 将鼠标悬停在 Web 元素上
  
![sample](../../../img/hover_sample1.png)  

```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.li_dots_overflow).hover()
# the menu is displayed after hovering over the button
```
  
![sample](../../../img/hover_sample2.png) 