# click
```python
def click(
        self,
        mouse_button: Literal["left", "middle", "right"] = MouseButton.Left,
        mouse_location: MouseLocation = MouseLocation(),
        by: Union[Literal["default", "mouse-emulation", "control-invocation"], MouseActionBy] = MouseActionBy.Default,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey,
        timeout: int = 30
    ) -> None
```  

单击目标元素。

**参数:**  
    &emsp;**mouse_button**: MouseButton  
        &emsp;&emsp; 可用值为：“左”、“右”和“中心”，默认值为“左”。
<br/>
    &emsp;**mouse_location**: MouseLocation  
        &emsp;&emsp; 它设置为定义要单击的元素的位置。默认位置是元素的中心。通过定义 [MouseLocation](./mouselocation.md) 对象来自定义位置.   
        <br/>
    &emsp;**by**: MouseActionBy  
        &emsp;&emsp; 定义单击 UI 元素的方法。
        &emsp;&emsp; `mouse-emulation`: 通过模拟鼠标单击目标 UI 元素。
        &emsp;&emsp; `control-invocation`: 通过调用目标 UI 元素的 UI 方法单击其。如果它是 Windows 桌面元素，则可能不受支持。
        &emsp;&emsp; `default`: 自动选择每种元素类型的方法。对于 Web 元素，请使用 `control-invocation`; 对于 Window元素, 用 `mouse-emulation`.  
        <br/>
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; 要同时按下的修饰键（“alt”、“ctrl”、“shift”、“win”）和默认值为 none。   
        <br/>  
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。
        <br/>

**返回:**  
    &emsp;None

**例子:**

- 点击左键
***
```python
from clicknium import clicknium as cc, locator, ui
ui(locator.chrome.bing.svg).click(mouse_button = "left")

tab = cc.chrome.open("https://contoso.com")
tab.find_element(locator.chrome.contoso.svg).click(mouse_button = "left")
```

- 使用自定义鼠标位置单击鼠标位置
对于按钮“5”作为下面应用程序中的目标元素，我们可以通过设置其鼠标位置来单击其他按钮。 
![sample1](../../../img/click_sample1.png)

> 附注
>- 鼠标位置在  `clicknium.common.models.MouseLocation`中定义


```python
from clicknium import clicknium as cc, locator, ui
from clicknium.common.models.MouseLocation import MouseLocation

# click center of button '5'
ui(locator.applicationframe.button_num5butto).click()

# click button '6' 
# The click position is 100% of target element width away from the center of button '5' in x direction
ui(locator.applicationframe.button_num5butto).click(mouse_location=MouseLocation(xrate=1))

# click button '8'
# The click position is -100% of target element height away from the center of button '5' in y direction
ui(locator.applicationframe.button_num5butto).click(mouse_location=MouseLocation(yrate=-1))
```

- 点击modifier_key
对于 Windows 文件资源管理器，如下所示：
![sample2-1](../../../img/click_sample21.png)  
单击文件夹“test3”作为 `ui(locator.explorer.edit_system_item).click()`, 然后选择从“测试1”更改为“测试3”
![sample2-2](../../../img/click_sample22.png)  
单击文件夹“test3”作为`ui(locator.explorer.edit_system_item).click(modifier_key=ModifierKey.Ctrl)`, 然后“test1”和“test3”都在选择中。
![sample2-3](../../../img/click_sample23.png) 