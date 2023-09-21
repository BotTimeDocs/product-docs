---
sidebar_position: 13
sidebar_label: scroll
---
# WebElement.scroll

```python
def scroll(
        self,
        delta_x: int = 0,
        delta_y: int = 0,
        timeout: int = 30
    ) -> None
```   

使用滚动条滚动目标元素。

**参数:**  
    &emsp;**delta_x**: int   
        &emsp;&emsp;  要水平滚动的像素。
    &emsp;**delta_y**: int   
        &emsp;&emsp; 要垂直滚动的像素。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。


**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.clicknium.com")

# scroll the element
web_element = chrome_tab.find_element(locator.chrome.clicknium.products_panel)
web_element.scroll(0, 500)
```