
# WebDriver.open

```python
def open(
        self,
        url: str,
        is_maximize: bool = True,
        is_wait_complete: bool = True,
        userdata_folder_mode: Literal["automatic", "default", "custom"] = WebUserDataMode.Automatic,
        userdata_folder_path: str = "",
        args: List[str] = None,
        timeout: int = 30
    ) -> BrowserTab 
```

Open browser with specified url to get a browser tab. Browser automation extensions should be installed and enable. CDP is supported for Chrome and Edge browser, ` chromecdp` and `edgecdp` can run without browser automation extension and support `Headless mode` by set `headless` = true in open function.  

>**Remarks:**  
>- When you open and run the Python script with "Start Debugging (F5)" or "Run Without Debugging (Ctrl+F5)" in Visual Studio Code , the opened browser may be closed when exiting the debugging or running state.
>- CDP doesn't support attach existing browsers.   


**Parameters:**  
- **url[Required]**: str   
    - Url string, the target site url, eg.: <https://www.bing.com>.     
- **is_maximize**: bool  
    - is_maximize, whether to maximize the browser window, the default value is True.  
- **is_wait_complete**: bool  
    - is_wait_complete, whether to wait for the broswser to complete loading, the default value is True.  
- **userdata_folder_mode**: WebUserDataMode  
    - userdata_folder_mode defines whether using customized user data folder when opening the browser.  
    - `automatic`：use user data folder automatically.  
    - `default`：use default folder of the user data.  
    - `custom`：use the folder specified by parameter 'userdata_folder_path'.  
- **userdata_folder_path**: str  
    - User data's folder path.  
- **args**: additional arguments to pass to the browser instance. The list of Chromium flags can be found at https://peter.sh/experiments/chromium-command-line-switches/, ex: args=["--profile-directory=Default"]
  
- **timeout**: int  
    - Timeout for the operation, the unit is second, and the default value is 30 seconds. 

**Returns:**  
    &emsp;[BrowserTab](browsertab.md) object, you can execute the following operations in the browser tab such as: find_element, find_elements, close, refresh and so on.

**Example:**
***
```python
from clicknium import clicknium as cc

# open IE browser
ie_tab = cc.ie.open("https://www.bing.com")

# open Chrome browser
chrome_tab = cc.chrome.open("https://www.bing.com")
# open Chrome browser with CDP
chrome_tab_cdp = cc.chromecdp.open("https://www.bing.com")
# open Chrome browser with headless mode 
chrome_headless_tab = cc.chromecdp.open("https://www.bing.com", headless = true)


# open Edge browser
edge_tab = cc.edge.open("https://www.bing.com", is_wait_complete = True)
# open Edge browser with CDP
edge_headless_tab = cc.edgecdp.open("https://www.bing.com", is_wait_complete = True, headless = true)

# open Firefox browser
firefox_tab = cc.firefox.open("https://www.bing.com", timeout = 10)


# open Brave browser
brave_tab = cc.chromium('brave').open("https://www.bing.com", timeout = 10)

# open Vivaldi browser
vivaldi_tab = cc.chromium('vivaldi').open("https://www.bing.com", timeout = 10)

```