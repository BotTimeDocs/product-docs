---
sidebar_position: 3
sidebar_label: new_tab
---
# browser.new_tab

```python
def new_tab(self, url: str, is_wait_complete: bool = True, timeout: int = 30) -> BrowserTab
```  

在当前浏览器中打开一个新选项卡。

**参数:**  
    &emsp;**url[Required]**: str   
        &emsp;&emsp;  网址字符串，目标网站网址，例如： <https://www.bing.com>.  
    &emsp;**is_wait_complete**: bool  
        &emsp;&emsp;  is_wait_complete，是否等待选项卡完成加载，默认值为 True。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;[BrowserTab](./browsertab/browsertab.md) 对象，可以在浏览器选项卡中执行以下操作：find_element、find_elements、关闭、刷新等。

**例子:**
***
```python
from clicknium import clicknium as cc

_tab = cc.chrome.open("https://www.bing.com/")

# get tab's browser
_browser = _tab.browser

# new tab
_browser.new_tab("https://www.bing.com/")

```