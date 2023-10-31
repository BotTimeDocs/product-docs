# mouselocation
MouseLocation 类用于定义鼠标操作在目标元素上的位置，用于[click](./click.md), [double_click](./double_click.md), [mouse_up](./mouse_up.md) and [mouse_down](./mouse_down.md).**

**参数:**  
- **Location**: Location  
    - 要执行鼠标操作的目标元素的相对位置。可用值为“居中”、“左-上”、“左-下”、“右-上”和“右-下”，默认值为“居中”。
- **Xoffset**: int   
    - 设置相对于“位置”的 x 方向偏移（以像素为单位）。默认值 为 0。
- **Yoffset**: int  
    - 设置相对于“位置”的 y 方向偏移（以像素为单位）。默认值为 0。
- **Xrate**: float  
    - 设置相对于“位置”的 x 方向偏移（以目标元素宽度的百分比表示）。默认值为 0。
- **Yrate**: float  
    - 设置相对于位置的 y 方向偏移（以目标元素高度的百分比表示）。默认值为 0。

**附注**:
>仓位计算可以说明如下：
>
> ![sample1](../../../img/location-center-offset.png)
> ![sample2](../../../img/location-lefttop-offset.png)
    
**定义:**
```python
    class MouseLocation(object):

     def __init__(self, location: Literal["center", "left-top", "left-bottom", "right-top","right-bottom"] = Location.Center, xoffset=0, yoffset=0, xrate=0, yrate=0):
        self.Location = location
        self.Xoffset = xoffset
        self.Yoffset = yoffset
        self.Xrate = xrate
        self.Yrate = yrate
     
```