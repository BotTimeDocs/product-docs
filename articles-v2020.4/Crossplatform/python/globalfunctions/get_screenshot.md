
# clicknium.get_screenshot
```python
def get_screenshot(image_file: str) -> None
```

将当前窗口的屏幕截图保存到图像文件。

**参数:**  
    &emsp;**image_file[Required]**: str   
        &emsp;&emsp;保存图像的文件路径

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc

cc.get_screenshot("D:\\screenshot.png")

```