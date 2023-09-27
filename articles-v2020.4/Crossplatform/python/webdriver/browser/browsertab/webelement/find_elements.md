
# WebElement.find_elements
```python
def find_elements(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        timeout: int = 30
    ) -> List[WebElement]
```  

返回当前网页中给定定位器的所有匹配 Web 元素的列表。

**参数:**  
    &emsp;**locator[Required]**: str | _Locator   
        &emsp;&emsp; Locator string定位器字符串，目标 UI 元素的定位器的访问路径，例如：“locator.chrome.bing.search_sb_form_q”，定位器存储为 chrome，定位器名称为 search_sb_form_q
    &emsp;**locator_variables**: dict  
        &emsp;&emsp; Locator variables, 设置为在定位器中初始化参数，例如： `{ "row": 1,  "column": 1}`
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp; [WebElement](webelement.md) 对象列表。

**例:**
***
```python
from clicknium import clicknium as cc, locator, ui

tab = cc.edge.open("https://www.bing.com/")
tab.find_element(locator.new_store.sample.bing.search_sb_form_q).set_text('clicknium')
tab.find_element(locator.new_store.sample.bing.svg).click()
web_element = tab.find_elements(locator.new_store.sample.bing.a_search_list)
result_elements = web_element.find_elements(locator.new_store.sample.bing.a_search_result)
for elem in result_elements:
    elem.highlight(duration=1)
tab.close()
```