
# browser.maximize

```python
def maximize(self) -> None
```  

最大化浏览器窗口。

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc

# get browser with type chrome
browser = cc.chrome.browsers[0]

# maximize the browser window
browser.maximize()
```