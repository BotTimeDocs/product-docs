# select_item
```python
def select_item(
        self,
        item: str,
        timeout: int = 30
    ) -> None
```  

当目标元素是下拉列表类型控件时，为目标元素选择一个选项。

**参数:**  
    &emsp;**item [Required]**: str   
        &emsp;&emsp; 下拉控件的目标选项。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None

**Example:**
***
- 在网络上选择项目（类型为选择）
![sampel1](../../../img/select-item-sample1.png)

```python
from clicknium import clicknium as cc, locator, ui

chrome_tab = cc.chrome.open("https://contoso.com")
chrome_tab.find_element(locator.chrome.page.select).select_item('One')

```
- 选择窗口文件“另存为”对话框中的项目

![sample](../../../img/select_item_sample2.png)  
```python
from clicknium import clicknium as cc, locator, ui

ui(locator.notepad.combobox_filetype).select_item('All Files  (*.*)')

```