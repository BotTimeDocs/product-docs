# get_position
```python
def get_position(self, timeout: int = 30) -> ElementPosition
```

获取目标元素的位置。

**参数:**   
- **timeout**: int  
    - 获取目标元素的位置。

**返回:**  
    &emsp;ElementPosition 对象，类定义如下：
```python
    class ElementPosition:

    def __init__(self, left, top, right, bottom):
        self.Left = left
        self.Top = top
        self.Right = right
        self.Bottom = bottom
```

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui
from json
    
position = ui(locator.chrome.bing.search_sb_form_q).get_position()
print(position.__dict__)

# output: {"Left": 420, "Top": 294, "Right": 931, "Bottom": 339}

```