
# WebDriver.attach

```python
def attach(
        self,
        locator: Union[_Locator, str],
        locator_variables: dict = {},
        is_maximize: bool = True,
        timeout = 30
    ) -> BrowserTab
```  

Attach to an opened browser tab with specified locator.

**Parameters:**  
- **locator[Required]**: str | _Locator  
    - Locator string, the visit path of locator for a UI element in the target browser tab. 
- **locator_variables**: dict  
    - Locator variables, set to initialize parameters in locator, eg: `{ "row": 1,  "column": 1}`
- **is_maximize**: bool  
    - is_maximize is set to define whether to maximize the browser window when attaching, and the default value is True.  
- **timeout**: int  
    - Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;[BrowserTab](browsertab.md) object, you can execute the following operations in the browser tab such as: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
from clicknium import clicknium as cc

# attach ie browser
ie_tab = cc.ie.attach("locator.chrome.document_newtab")

# attach chrome browser
chrome_tab = cc.chrome.attach("locator.chrome.document_newtab")

# attach edge browser
edge_tab = cc.edge.attach("locator.chrome.document_newtab", is_maximize = False)

# attach firefox browser also with parametric locator
variables = {"name":"test"}
firefox_tab = cc.firefox.attach("locator.chrome.document_newtab", variables, timeout = 10)
```