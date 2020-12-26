# 获取结构化数据

获取指定页面的结构化数据，可自动翻页获取更多数据。支持整表数据或者表内单列，运行时取指定最大提取条数范围内的数据。支持桌面端和浏览器端


## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

目标
- **[选择器](../Appendix/Selector.md?_v=v2020.4)** ：用于指示要获取数据的目标区域。可通过点击**指定数据源**自动生成。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型


可选项
- **最大提取条数**：获取的最大数据条数。例如此值填写“10”，则运行时返回的数据表内最大数据条数为10条。仅支持整型变量和整型
- **下一页**：用于指示下一页按钮的位置，实现翻页获取数据的功能。可通过**指定数据源**过程中指定下一页按钮后自动生成。仅支持字符串变量和字符串
- **获取下一页数据延迟**：限定翻页后获取新页面数据的时间，超出指定时间后将执行获取数据的操作。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

## 操作样例
1. 打开含有结构化数据的网页（例：http://news.baidu.com），拖入**获取结构化数据**组件，点击指定数据源并指定第一个元素，此时，会弹出“向导”对话框提示指定数据源第二个元素，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-1.png)
2. 指定第二个元素，“向导”对话框中会显示默认文本列名称，再点击“下一步”按钮，“向导”对话框展示获取的所有数据及默认最大提取条数：50：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-2.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-3.png)
3. 添加数据表变量，点击“完成”按钮：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-4.png)

4. 根据需要点击“是”或“否”，如果选择“是”继续选择应用页面上的元素，如果选择“否”，指定元素结束
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-5.png)

5. 拖入**预览数据表**组件，并输入上述操作中定义的数据表变量dt:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-6.png)

6. 点击运行流程，查看获取的数据，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/extractStructureData-7.png)