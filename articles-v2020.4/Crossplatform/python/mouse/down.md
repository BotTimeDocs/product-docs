

# clicknium.mouse.down

```python
def down(
        self,
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left
    ) -> None
```

将鼠标放在所需位置，然后按下鼠标按钮。

**参数:**  
- **x[Required]**: int  
    - 定义 X 整数坐标。
<br/>
- **y[Required]**: int  
    - 定义 Y 整数坐标。
<br/>
- **mouse_button**: MouseButton  
    - 定义鼠标按钮的位置，默认值为左按钮。 

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# Press the mouse button down on position (100,100)
cc.mouse.down(100,100)

```