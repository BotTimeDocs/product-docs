
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
    &emsp;**x[Required]**: int  
        &emsp;&emsp; 定义 X 整数坐标。
<br/>
    &emsp;**y[Required]**: int  
        &emsp;&emsp; 定义 Y 整数坐标。
<br/>
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; 定义鼠标按钮的位置，默认值为左按钮。
<br/>
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; 修改键（“Alt”、“Ctrl”、“Shift”、“Win”）要随单击一起按下，默认值为 None。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# preform double click on position (100,100)
cc.mouse.double_click(100,100)

```