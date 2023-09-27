
# WebElement.execute_js_file

```python
def execute_js_file(
        self,
        javascript_file: str, 
        method: str = '', 
        timeout: int = 30
    ) -> str
```  

为目标元素执行 Javascript 文件。

> **备注:**
>在参数 `javascript_file`, 中指定的要执行的 Javascript 文件中，使用“_context$.currentElement.”作为目标元素。

**参数:**  
    &emsp;**javascript_file[Required]**: str    
        &emsp;&emsp;  Javascript 文件路径，例如："c:\\test\test.js".  
    &emsp;**method**: str    
        &emsp;&emsp; 要调用的方法应该在 Javascript 文件中定义。如果任何参数需要传递给方法，它可以包含在此参数值中，例如：SetText（“test”）。
    &emsp;**timeout**: int  
        &emsp;&emsp; 要调用的方法应该在 Javascript 文件中定义。如果任何参数需要传递给方法，它可以包含在此参数值中，例如：SetText（“test”）。

**返回:**  
    &emsp;Str,  执行结果。

**例:**
***
```python
from clicknium import clicknium as cc

# open Chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# execute js, set text for target element

# test.js content can be:  
#  function SetText(st){  
#     _context$.currentElement.value = st;
#     console.log("execute js");
#     return "success"
#  }

result = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q).execute_js_file("C:\\test\\test.js", "SetText(\"click\")")
```