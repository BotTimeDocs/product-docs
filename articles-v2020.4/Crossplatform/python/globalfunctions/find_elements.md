
# clicknium.find_elements
```python 
def find_elements(
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[UiElement]
```

返回给定定位器的所有匹配 UI 元素的列表。

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp;定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q。
    &emsp;**locator_variables**: dict  
        &emsp;&emsp;定位器变量，设置为在定位器中初始化参数，例如`{ "row": 1,  "column": 1}`, 

    &emsp;**timeout**: int  
        &emsp;&emsp;查找所有匹配的 UI 元素的超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;具有类型的匹配元素列表 [UiElement](../../python/uielement/uielement.md).

**例子:**
***
```python
from clicknium import clicknium as cc, locator, ui

cc.edge.open("https://www.bing.com/")
ui(locator.store.sample.bing.search_sb_form_q).set_text('clicknium')
ui(locator.store.sample.bing.svg).click()

result_elements = cc.find_elements(locator.store.sample.bing.a_search_result)
for elem in result_elements:
    elem.highlight(duration=1)
```