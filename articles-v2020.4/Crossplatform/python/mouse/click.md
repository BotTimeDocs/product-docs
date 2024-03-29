
# clicknium.mouse.click

```python
def click(
        self, 
        x: int, 
        y: int, 
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        delay: int = 0
    ) -> None
```  

使用指定的鼠标按钮执行单击。

**参数:**  
- **x[Required]**: int  
    - 定义 X 整数坐标。
<br/>
- **y[Required]**: int  
    - 定义 Y 整数坐标。
<br/>
- **mouse_button**: MouseButton  
        &emsp;&emsp;定义鼠标按钮的位置，默认值为左按钮。
<br/>
- **modifier_key**: ModifierKey  
    - 修改键（“Alt”、“Ctrl”、“Shift”、“Win”）要随单击一起按下，默认值为 None。
<br/>
- **delay**: int  
        &emsp;&emsp;定义鼠标按下和鼠标向上之间的等待时间，单位为秒，默认值设置为 0 秒。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# preform click on position (100,100)
cc.mouse.click(100,100)

```