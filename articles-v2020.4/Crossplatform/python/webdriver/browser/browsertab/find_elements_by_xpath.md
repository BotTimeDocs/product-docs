
# BrowserTab.find_elements_by_xpath
```python
def find_elements_by_xpath(
        self,
        xpath: str,
        timeout: int = 30
    ) -> List[WebElement]
```  

I在活动浏览器中，通过给定的 XPath 查找元素。

**参数:**  
- **xpath[Required]**: str     
    - 要查找的元素的 XPath。
- **timeout**: int  
    - 操作超时，单位为秒，默认值为 30 秒。 

**返回:**  
    &emsp; [WebElement](webelement.md) 对象列表。

**例:**
***
```python
from clicknium import clicknium as cc

chrome_tab = cc.chrome.open("https://bing.com/images")

# find elements by XPath
webelements = chrome_tab.find_elements_by_xpath("//*[@id=\"ilp_t\"]/div[1]/div/*")
print("count: " + str(len(webelements)))
for i in range(3):
    webelements[i].highlight()

```