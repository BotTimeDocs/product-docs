
# WebElement.find_element_by_xpath
```python
def find_element_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> WebElement
```  

在活动浏览器中，通过给定的 XPath 查找元素。. 

**参数:**  
    &emsp;**xpath[Required]**: str     
        &emsp;&emsp; 要查找的元素的 XPath。  
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;[WebElement](webelement.md) 对象。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by XPath
element = chrome_tab.find_element_by_xpath("//*[@id=\"ilp_t\"]")

# find sub element by XPath
subelement = element.find_element_by_xpath(".//*[@id=\"ilp_t\"]/div[1]/div/*")
subelement.highlight()

```