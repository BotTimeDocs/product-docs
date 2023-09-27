
# clicknium.find_element

```python
def find_element(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        window_mode: Literal["auto", "topmost", "noaction"] = WindowMode.Auto
    ) -> UiElement 
```

返回由给定定位器定义的 UI 元素。

> **附注:**  
>别名方法 `ui()` 相当于 `clicknium.find_element()`. 

**参数:**  
	&emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp;定位器字符串，目标 UI 元素的定位器的访问路径，, 例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 Chrome，定位器名称为 &emsp;&emsp;search_sb_form_q
<br/>
    &emsp;**locator_variables**: dict  
        &emsp;&emsp;定位器变量，设置为初始化定位器中的参数，例如： `{ "row": 1,  "column": 1}`.  
<br/>
    &emsp;**window_mode**: WindowMode  
         &emsp;&emsp;它定义在调用操作之前是否将 UI 元素的父窗口设置为最顶层。
         &emsp;&emsp;`auto`: 默认值，默认情况下将窗口设置为最顶层。
         &emsp;&emsp;`topmost`: 始终将窗口设置为最顶层
         &emsp;&emsp;`noaction`: 对最顶层模式不执行任何操作
<br/>

**返回:**  
    &emsp;第一个匹配的 UI 元素，类型为 [UiElement](../../python/uielement/uielement.md).

**例子:**
***
```python

from clicknium import clicknium as cc, locator, ui

searchBox = cc.find_element(locator.chrome.bing.search_sb_form_q)
#or 
searchBox = ui(locator.chrome.bing.search_sb_form_q)

#parametric locator
variables = {"name":"test"}
searchBox = ui(locator.chrome.bing.search_sb_form_q, variables)
```