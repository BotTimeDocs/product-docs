# drag_drop
```python
def drag_drop(
        self,
        xpoint: int = 0,
        ypoint: int = 0,
        speed: int = 50,
        timeout: int = 30
    ) -> None
```  

按住源元素上的鼠标左键，然后移动到目标偏移量并释放鼠标按钮。 

**参数:**  
- **xpoint**: int    
    - 在 X 轴上移动像素。
- **ypoint**: int   
    - 在 Y 轴上移动像素。  
- **speed**: int  
    - 拖动速度，单位为 ms/10px，默认值为 50。
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui

# drag the scroll button right 20 pixels
ui(locator.app.bing.scrollbutton).drag_drop(20, 0)
  
# drag the scroll button down 20 pixels
ui(locator.app.bing.scrollbutton).drag_drop(0, 20)
```

- 拖动记事本的滚动条按钮
向下滚动 50 像素，如下所示： `ui(locator.notepad.thumb_scrollbar).drag_drop(0, 50)`  
![sample1](../../../img/drap_drop_sample1_2.png)  

- 从左向右移动滑块按钮
像这样向右滚动 20 像素： `ui(locator.uiautomationwpfd.thumb_thumb).drag_drop(20, 0)`  
![sample2](../../../img/drap_drop_sample2_2.png)  