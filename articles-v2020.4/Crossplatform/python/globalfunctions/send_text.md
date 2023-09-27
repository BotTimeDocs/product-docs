
# clicknium.send_text

```python
def send_text(
        self,
        text: str
    ) -> None
```

将文本发送到光标的当前位置。

>**附注:**  
此方法是将文本发送到系统。如果需要将文本发送到特定的 UI 元素，则需要在调用此方法之前将 UI 元素设置为焦点状态。或者，您可以使用绑定到 UI 元素的[set_text](./../uielement/set_text.md) 。

**参数:**  
    &emsp;**text[Requried]**: str  
        &emsp;&emsp; 要发送的文本字符串。  

**返回:**  
    None

**例子:**
***
```python
from clicknium import clicknium

clicknium.find_element(locator.chrome.bing.search_sb_form_q).set_focus()

clicknium.send_text("clicknium")
```