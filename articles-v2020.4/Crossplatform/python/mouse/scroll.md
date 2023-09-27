---
sidebar_position: 6
sidebar_label: scroll
---

# clicknium.mouse.scroll

```python
def scroll(
        self,
        times = 1,
        modifier_key: Literal["nonekey", "alt", "ctrl", "shift","win"]  = ModifierKey.NoneKey
    ) -> None
```  

做鼠标滚轮。

**参数:**  
    &emsp;**times**: int  
        &emsp;&emsp; 滚动的整数次数，默认值为 1。当值大于零表示向上滚动时，其他值表示向下滚动。 
    &emsp;**modifier_key**: ModifierKey  
        &emsp;&emsp; 修改键（“Alt”、“Ctrl”、“Shift”、“Win”）要随单击一起按下，默认值为 None。

**返回:**  
    &emsp;None

**例:**
***
```python
from clicknium import clicknium as cc

# Do the mouse scroll wheel with up direction and scroll 2 times and press along with modifier key "ctrl"
cc.mouse.scroll(2,'ctrl')

```