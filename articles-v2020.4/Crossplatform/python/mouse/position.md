---
sidebar_position: 7
sidebar_label: position
---

# clicknium.mouse.position

```python 
def position(
        self
    ) -> Tuple[int,int]
```

获取鼠标光标的位置。

**参数:**  
    &emsp;None   

**返回:**  
    &emsp;鼠标光标的当前 X 和 Y 坐标。


**例:**
***
```python
from clicknium import clicknium as cc

# get the position of the mouse cursor
x,y = cc.mouse.position()
print("X integer coordinate is ", x)
print("Y integer coordinate is ", y)
```