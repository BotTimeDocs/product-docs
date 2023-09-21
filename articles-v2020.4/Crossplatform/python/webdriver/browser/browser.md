# Browser

**浏览器类提供浏览器操作的方法。**

## 性能
- `tabs`: 列出[[BrowserTab](./browsertab/browsertab.md)], 获取浏览器的所有选项卡。

## 方法
- [new_tab](./new_tab.md): 在当前浏览器中打开一个新选项卡，返回 [BrowserTab](./browsertab/browsertab.md).  
- [get_tab](./get_tab.md): 通过指定的标题和/或 url 获取选项卡，返回 [BrowserTab](./browsertab/browsertab.md).  
- [get_active_tab](./get_active_tab.md): 获取浏览器的当前活动选项卡，返回 [BrowserTab](./browsertab/browsertab.md).  
- [close](./close.md): 关闭浏览器。
- [maximize](./maximize.md): 最大化浏览器窗口。