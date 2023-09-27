
# clicknium.mouse.double_click

```python
def double_click(
        self, 
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey
    ) -> None
```  

使用指定的鼠标按钮双击。

**参数:**  
- **x[Required]**: int  
    - 定义 X 整数坐标。
<br/>
- **y[Required]**: int  
    - 定义 Y 整数坐标。
<br/>
- **mouse_button**: MouseButton  
    - 定义鼠标按钮的位置，默认值为左按钮。
<br/>
- **modifier_key**: ModifierKey  
    - 修改键（“Alt”、“Ctrl”、“Shift”、“Win”）要随单击一起按下，默认值为 None。

**返回:**  
    &emsp;None

**例:**
***
```python

from clicknium import clicknium as cc

# preform double click on position (100,100)
cc.mouse.double_click(100,100)

```