# get_text
```python
def get_text(self, timeout: int = 30) -> str
```

获取目标元素的文本。

**参数:**    
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;str

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui
    
text = ui(locator.chrome.bing.search_sb_form_q).get_text()
```

- 对于 Windows 应用程序的编辑控件，它返回编辑控件的值。
```python
from clicknium import clicknium as cc, locator, ui
    
# return value of the edit document
text = ui(locator.notepad.document).get_text()
```

- 对于窗口应用程序的按钮、菜单项等控件，它返回控件的名称。
```python
from clicknium import clicknium as cc, locator, ui
    
# return name of the menuitem
text = ui(locator.notepad.menuitem_format).get_text()
# text is 'format'
```

- 对于 Web 元素，它返回 innerText。
```python
from clicknium import clicknium as cc, locator
tab = cc.chrome.open("https://contoso.com")
# return inner text of div
text = tab.find_element(locator.chrome.form.divItem).get_text()
```