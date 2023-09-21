# clear_text
```python
def clear_text(
        self,
        by: Union[Literal["set-text", "send-hotkey"], ClearTextBy],
        clear_hotkey: Union[Literal["CAD", "ESHD", "HSED"], ClearHotKey] = ClearHotKey.CtrlA_Delete,
        preaction: Literal["setfocus", "click"] = PreAction.SetFocus,
        timeout: int = 30
    ) -> None
```  

目标元素的清除文本。

**参数:**  
     &emsp;**by**: ClearTextBy  
        &emsp;&emsp; 清除目标元素文本的方法
        &emsp;&emsp; `set-text`: 通过设置目标元素的属性来清除其文本。
        &emsp;&emsp; `send-hotkey`: 通过向目标元素发送热键来获取文本。还需要相应地指定“clear_hotkey”和“预操作”参数。 
    &emsp;**clear_hotkey**: ClearHotKey  
        &emsp;&emsp; 如果 by 设置为“发送热键”，则使用此参数指定热键，默认值为 `CAD`.  
        &emsp;&emsp; `CAD` 意思是`{CTRL}{A}-{DELETE}`: 首先发送组合键“{CTRL}{A}”，然后发送“{DELETE}”。
        &emsp;&emsp; `ESHD` 意思是 `{END}-{SHIFT}{HOME}-{DELETE}`: 首先发送“{END}”，然后发送组合键“{SHIFT}{HOME}，然后发送密钥”{DELETE}”。
        &emsp;&emsp; `HSED` 意思是 `{HOME}-{SHIFT}{END}-{DELETE}`:首先发送“{HOME}”，然后发送组合键“{SHIFT}{END}，然后发送”{DELETE}”。
    &emsp;**preaction**: PreAction  
        &emsp;&emsp; 如果 by 设置为“发送热键”，请为在将热键发送到明文之前要执行的操作指定此参数。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例子:**
***
- 桌面文件“另存为”对话框
![sample1](../../../img/clear_text_sample1.png)  
对于文件“另存为”对话框，使用clear_text清除“文件名”输入框中的现有内容，在这种情况下，可以通过设置为“设置文本”。

```python
from clicknium import clicknium as cc, locator, ui  

ui(locator.chrome.edit_1001).clear_text(by="set-text")
```

- 微信消息输入框
![sample1](../../../img/clear_text_sample2.png)  
这种类型的 UI 元素不支持“设置文本”来清除文本，请使用以下方式。

```python
from clicknium import clicknium as cc, locator, ui  

ui(locator.wechat.edit1).clear_text(by="send-hotkey", clear_hotkey="CAD", preaction="click")

```

- 网页输入文本框

```python
chrome_tab = cc.chrome.open("https://contoso.com/")
chrome_tab.find_element(locator.chrome.contoso.text).set_text("hello")
chrome_tab.find_element(locator.chrome.contoso.text).clear_text(by=ClearTextBy.SetText)
```