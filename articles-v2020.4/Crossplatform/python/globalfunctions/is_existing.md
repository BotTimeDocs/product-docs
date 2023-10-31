
# clicknium.is_existing

```python
 def is_existing(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> bool 
 ```

检查 UI 元素是否存在。

**参数:**  
- **locator[Required]**: str | _Locator   
        &emsp;&emsp;定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q
<br/>
- **locator_variables**: dict  
        &emsp;&emsp;定位器变量，设置为在定位器中初始化参数，例如：`{ "row": 1,  "column": 1}`
<br/>
- **timeout**: int  
         &emsp;&emsp;查找目标 UI 元素的超时，单位为秒，默认值为 30 秒。
<br/>

**返回:**  
     &emsp;如果 UI 元素存在，则返回 True，否则返回 False。

**例子:**
***
```python
from clicknium import clicknium as cc, locator

cc.is_existing(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
cc.is_existing(locator.chrome.bing.search_sb_form_q, variables)
```