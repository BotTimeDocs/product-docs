# mouse_up

```python
def mouse_up(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        mouse_location: MouseLocation = MouseLocation(),
        by: Union[Literal["default", "mouse-emulation", "control-invocation"], MouseActionBy] = MouseActionBy.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None
``` 

鼠标向上按钮在目标元素上。

**Parameters:**  
     &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; 可用值为：“左”、“右”和“中心”，默认值为“左”。
    &emsp;**mouse_location**: MouseLocation  
        &emsp;&emsp; 设置[MouseLocation](./mouselocation.md) 以定义释放鼠标按钮的元素位置。默认位置是元素的中心。
    &emsp;**by**: MouseActionBy  
        &emsp;&emsp; 定义执行释放鼠标按钮的方法。
        &emsp;&emsp; `mouse-emulation`: 通过模拟鼠标来执行操作。
        &emsp;&emsp; `control-invocation`: 通过调用其 UI 方法来执行操作。如果它是 Windows 桌面元素，则可能不受支持。
        &emsp;&emsp; `default`: 自动选择每个元素类型的方法。对于 Web 元素，使用`control-invocation`; 对于Window元素, 使用 `mouse-emulation`.  
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; 要随操作一起按下的修饰键（“alt”、“ctrl”、“shift”、“win”），默认值为 none。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.chrome.bing.svg).mouse_up(mouse_button = "left")
```