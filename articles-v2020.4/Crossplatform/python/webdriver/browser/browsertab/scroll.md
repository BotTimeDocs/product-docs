
# BrowserTab.scroll

```python
def scroll(
        self,
        delta_x: int = 0,
        delta_y: int = 0
    ) -> None
```  

使用滚动条滚动当前浏览器选项卡。

**参数:**  
- **delta_x**: int   
    -  像素以水平滚动。.  
- **delta_y**: int   
    - 像素以垂直滚动。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.clicknium.com")

# scroll tab
chrome_tab.scroll(0, 500)
```