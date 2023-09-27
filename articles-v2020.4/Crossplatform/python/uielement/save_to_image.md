# save_to_image

```python
def save_to_image(
        self,
        image_file: str,
        img_width: int = 0,
        img_height: int = 0,
        xoffset: int = 0,
        yoffset: int  = 0,
        timeout: int = 30
    ) -> None
```

将目标元素的屏幕截图保存到具有指定大小和偏移量的文件。


**参数：**   

- **image_file[Required]**: str  
    - 保存图像的文件路径。  
- **img_width**: int  
    - 指定屏幕截图宽度。默认值为目标元素的宽度。 
- **img_height**: int  
    - 特别的截图高度。默认值为目标元素的高度。 
- **xoffset**:  int  
    - X 轴与目标元素左上角的偏移。
- **yoffset**: int  
    - Y 轴与目标元素左上角的偏移。 
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。 

**返回：**  
    &emsp;None

**例：**
***
```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.search_sb_form_q).save_to_image("D:\\screenshot.png")
```