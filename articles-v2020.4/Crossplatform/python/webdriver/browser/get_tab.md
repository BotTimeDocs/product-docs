
# browser.get_tab

```python
def get_tab(self, title: str = '', url: str = '') -> BrowserTab
```  

ET 选项卡按指定的标题和/或 URL。

**参数:**  
- **title**: str   
    - 标题字符串，目标网页的标题，支持通配符。
- **url**: str  
    - URL 字符串，目标网页的 URL，支持通配符。

**返回:**  
    &emsp;[BrowserTab](./browsertab/browsertab.md) 对象，可以在浏览器选项卡中执行以下操作：find_element、find_elements、关闭、刷新等。

**例子:**
***
```python
from clicknium import clicknium as cc

browser = cc.chrome.browsers[0]
# by tile and url
browser.get_tab("bing", "https://cn.bing.com/")

# by title only
browser.get_tab("bing")

# by url only
browser.get_tab(url = "https://cn.bing.com/")

# by title with wildcard
browser.get_tab("bi*", "https://cn.bing.com/")
```