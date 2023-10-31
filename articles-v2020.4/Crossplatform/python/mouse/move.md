

# clicknium.mouse.move

```python
def move(
        self,
        x: int, 
        y: int
    ) -> None
```  

将鼠标光标移动到 X 和 Y 整数坐标。


**参数:**  
- **x[Required]**: int  
    - 定义 X 整数坐标。
<br/>
- **y[Required]**: int  
    - 定义 Y 整数坐标。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# Move the mouse to position (100,100)
cc.mouse.move(100,100)

```