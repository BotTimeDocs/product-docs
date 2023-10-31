# child

```python
def child(self, index: int)
```  

获取带有索引的子元素。

> **附注:**
>- 指数从 0 开始。

**参数:**    
- **index[Required]**: int  
    -  指定的索引，获取第 n 个子项


**返回:**  
    &emsp;[UiElement](./uielement.md) 对象（如果找到），如果找不到，则为 None

**例子:**

```python
from clicknium import clicknium as cc, locator, ui
    
ele = ui(locator.chrome.bing.li_dots_overflow)
first_child = ele.child(0)
```