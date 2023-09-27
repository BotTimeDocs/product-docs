
# WebElement.execute_js

```python
def execute_js(
        self,
        javascript_code: str, 
        method: str = '', 
        timeout: int = 30
    ) -> str
```  

为目标元素执行 Javascript 代码。

> **备注:**
> 在 Javascript 代码中，执行参数 `javascript_code`, 中指定的，方法是使用“_context$.currentElement.”作为目标元素。

**参数:**  
    &emsp;**javascript_code[Required]**: str    
        &emsp;&emsp; 中指定的，方法是使用“_context$.currentElement.”作为目标元素。
    &emsp;**method**: str    
        &emsp;&emsp; 要调用的方法应该在 Javascript 代码中定义。如果任何参数需要传递给方法，它可以包含在此参数值中，例如：SetText（“test”）。
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;Str,  执行结果

**例:**
***
```python
from clicknium import clicknium as cc

# open chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")

# execute js, set text for target element
webEle = chrome_tab.find_element(locator.chrome.bing.search_sb_form_q)
js = "function SetText(text){_context$.currentElement.value = text; console.log(\"exit 0\"); return \"success\"}"

result = webEle.execute_js(js, "SetText(\"click\")")
```