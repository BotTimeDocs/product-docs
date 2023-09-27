# save_to_image
````python 
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

Save target element's screenshot to file with the specified size and offset.

**Parameters:**   
- **image_file[Required]**: str  
    - File path of saved image.  
- **img_width**: int  
    - Specify the screenshot width. Default is the target element's width.  
- **img_height**: int  
    - Speficy the screenshot height. Default is the target element's height.  
- **xoffset**:  int  
    - Offset of X-Axis from the target element's left-top corner.  
- **yoffset**: int  
    - Offset of Y-Axis from the target element's left-top corner.  
- **timeout**: int  
    - Timeout for the operation, the unit is second, and the default value is 30 seconds.  

**Returns:**  
    &emsp;None

**Example:**
***
```python
from clicknium import clicknium as cc, locator, ui
    
ui(locator.chrome.bing.search_sb_form_q).save_to_image("D:\\screenshot.png")
```