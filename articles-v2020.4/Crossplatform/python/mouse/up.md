

# clicknium.mouse.up

```python
def up(
        self,
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left
    ) -> None
```

将鼠标放在所需位置，然后重新释放鼠标按钮。

**参数:**  
    &emsp;**x[Required]**: int  
        &emsp;&emsp;  定义 X 整数坐标。
    &emsp;**y[Required]**: int  
        &emsp;&emsp; 定义 Y 整数坐标。
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; 定义鼠标按钮的位置，默认值为左按钮。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# release the mouse button up on position (100,100)
cc.mouse.up(100,100)

```