
# clicknium.send_hotkey

```python
def send_hotkey(hotkey: str) -> None
```

将热键发送到光标的当前位置。

>**附注:**  
这是一种将热键发送到系统的方法。如果需要将热键发送到特定的 UI 元素，则需要在调用此方法之前将 UI 元素设置为焦点状态。或者您可以使用另一个[send_hotkey](./send_hotkey.md) 绑定到 UI 元素。
**参数:**  
- **hotkey[Required]**: str   
       &emsp;&emsp;热键字符串表示一个键或组合键。例如，要表示字母 A，请输入字符串“A”。要表示字母 A、B 和 C，请输入参数表“ABC”。有关特殊键，请参阅 [hotkeys](https://docs.microsoft.com/en-au/dotnet/api/system.windows.forms.sendkeys?view=windowsdesktop-6.0#remarks).

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc

#send Ctrl+a
cc.send_hotkey('^a')

#send Shift+End
cc.send_hotkey('+{END}')

#send Win+e, first press 'Win', then press 'E' and release, and finally release 'Win'
cc.send_hotkey('{WIN DOWN}e{WIN UP}')
```