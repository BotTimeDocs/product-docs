# set_text
```python
def set_text(
        self,
        text: str,
        by: Union[Literal["default", "set-text", "sendkey-after-click", "sendkey-after-focus"], InputTextBy]= InputTextBy.Default,
        overwrite: bool = True,
        timeout: int = 30
    ) -> None
```  

为目标元素设置文本，它可用于向系统输入文本。

**Parameters:**  
- **text[Requried]**: str  
    - 要输入到目标元素的文本。
- **by**: str | InputTextBy   
    - 执行文本输入操作的方法。
    - `set-text`: 调用系统方法将文本设置为目标元素。某些 Windows 应用程序元素可能不受支持。
    - `default`: 对每个目标元素类型使用不同的方法. `set-text` 对于 Web 元素和 `sendkey-after-click` 对于桌面元素。
- **overwrite**: bool  
    - 无论是覆盖还是追加目标元素上的文本，默认值都为 True。 
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.chrome.bing.search_sb_form_q).set_text("clicknium", overwrite = False)
```