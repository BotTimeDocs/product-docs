
# WebElement.find_elements_by_css_selector
```python
def find_elements_by_css_selector(
        self,
        css_selector: str,
        timeout: int = 30
    ) -> List[WebElement]
```  

在活动浏览器中，通过给定的 CSS 选择器查找元素。

**参数:** 
    &emsp;**css_selector[Required]**: str     
        &emsp;&emsp; 用于查找元素的 CSS 选择器。
    &emsp;**timeout**: int  
        &emsp;&emsp;  操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp; [WebElement](webelement.md)对象列表。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by CSS selector
element = chrome_tab.find_element_by_css_selector("#ilp_t")

# find sub elements by CSS selector
webelements = element.find_elements_by_css_selector("IMG")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```