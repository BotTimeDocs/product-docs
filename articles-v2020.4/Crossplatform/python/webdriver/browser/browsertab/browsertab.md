# BrowserTab

**类表示用于执行自动化操作的网页。**

## 类
- `title`: str, 返回浏览器选项卡的标题。
- `url`: str, 返回浏览器选项卡的网址。
- `is_active`: bool, 返回浏览器选项卡的网址。
- `browser`: [Browser](browser.md), 浏览器，返回选项卡的父浏览器。

## 方法
**当前浏览器选项卡的 [WebElement](webelement.md) 相关操作**
- [find_element](Ma/doc/references/python/webdriver/browser/browsertab/find_element.md): 返回给定定位器定义的 Web 元素。
- [find_element_by_xpath](Ma/doc/references/python/webdriver/browser/browsertab/find_element_by_xpath.md):通过给定的 XPath 查找元素。
- [find_element_by_css_selector](Ma/doc/references/python/webdriver/browser/browsertab/find_element_by_css_selector.md): 通过给定的 CSS 选择器查找元素。
- [find_elements](Ma/doc/references/python/webdriver/browser/browsertab/find_elements.md): 返回当前网页中给定定位器的所有匹配 Web 元素的列表。
- [find_elements_by_xpath](Ma/doc/references/python/webdriver/browser/browsertab/find_elements_by_xpath.md): 通过给定的 XPath 查找元素。
- [find_elements_by_css_selector](Ma/doc/references/python/webdriver/browser/browsertab/find_elements_by_css_selector.md): 通过给定的 CSS 选择器查找元素。
- [is_existing](Ma/doc/references/python/webdriver/browser/browsertab/is_existing.md): 检查网页的指定元素是否存在。
- [is_existing_by_xpath](is_existing_by_xpath.md): 检查给定的 XPath 是否存在 UI 元素。
- [is_existing_by_css_selector](is_existing_by_css_selector.md): 通过给定的 CSS 选择器检查 UI 元素是否存在。
- [wait_appear](Ma/doc/references/python/webdriver/browser/browsertab/wait_appear.md): 等待网页的指定元素在给定的超时内出现。
- [wait_appear_by_xpath](wait_appear_by_xpath.md): 等待给定 XPath 出现元素。
- [wait_appear_by_css_selector](wait_appear_by_css_selector.md): 等待给定的 CSS 选择器出现元素。
- [wait_disappear](Ma/doc/references/python/webdriver/browser/browsertab/wait_disappear.md): 等待网页的指定元素在给定的超时内消失。
- [wait_disappear_by_xpath](wait_disappear_by_xpath.md): 等待元素在给定的 XPath 中消失。
- [wait_disappear_by_css_selector](wait_disappear_by_css_selector.md): 等待元素被给定的CSS选择器消失。
**与当前浏览器选项卡相关的操作**
- [activate](activate.md): 激活浏览器选项卡。
- [close](Ma/doc/references/python/webdriver/browser/browsertab/close.md): 关闭浏览器标签页。如果没有打开的选项卡，浏览器也将关闭。
- [goto](goto.md): 将当前选项卡重定向到指定的 URL。
- [refresh](refresh.md): 刷新当前标签页。
- [scroll](Ma/doc/references/python/webdriver/browser/browsertab/scroll.md)：使用滚动条滚动当前浏览器选项卡。
