# select_items
```python
def select_items(
        self,
        items: list,
        clear_selected: bool = True,
        timeout: int = 30
    ) -> None
```  

为目标元素选择多个选项，这些选项可以支持多个选择。

**参数:**  
    &emsp;**items [Required]**: list  
        &emsp;&emsp; 要选择的选项。
    &emsp;**clear_selected**: bool  
        &emsp;&emsp; 是否清除现有选择，默认值为 True。
    &emsp;**timeout**: int  
        &emsp;&emsp;  操作超时，单位为秒，默认值为 30 秒。
**返回:**  
    &emsp;None

**例子:**
***
- 在 Web 元素上选择多个项目
  
```python
from clicknium import clicknium as cc, locator, ui
chrome_tab = cc.chrome.open("https://contoso.com")  
chrome_tab.find_element(locator.chrome.page.multiselect).select_item({'One', 'Three'})  
# as showing below, 'One' and 'Three' are selected.
```

![sample](../../../img/select_items_sample2.png)  