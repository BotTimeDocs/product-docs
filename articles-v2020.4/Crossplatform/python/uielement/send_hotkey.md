# send_hotkey
```python
def send_hotkey(
        self,
        hotkey: str,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None
```  

将热键发送到目标元素。

**参数:**  
- **hotkey [Required]**: str   
    - 热键字符串表示一个键或组合键。例如，要表示字母 A，请输入字符串“A”。要表示字母 A、B 和 C，请输入参数表“ABC”。有关特殊键，请参阅 [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks).  
- **preaction**: PreAction  
    - 发送热键之前要执行的操作。 
    - `setfocus`: 默认值，在发送热键之前将目标元素设置为焦点状态。
    - `click`: 在发送热键之前单击目标元素。
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui

#send Ctrl+a   
ui(locator.chrome.bing.search_sb_form_q).send_hotkey('^a')

#send Shift+End
ui(locator.chrome.bing.search_sb_form_q).send_hotkey('+{END}')

#send Win+e, first press 'Win', then press 'E' and release, and finally release 'Win'
ui(locator.chrome.bing.search_sb_form_q).send_hotkey('{WIN DOWN}e{WIN UP}')
```