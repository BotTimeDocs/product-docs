# 获取屏幕文本

获取指定的文本或指定的文本元素列表。

注意：建议在无法使用 [获取文本](../GetText.md) 组件获取文本时，使用本组件。

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件
- **超时（毫秒）**：指定此组件的执行时间。单位为毫秒（ms）,1000ms = 1s。包含匹配超时（毫秒）。若超出此时间，组件还未执行，会抛出错误。

目标

- **控件元素** ：接收变量作为获取文本的目标元素。属性**控件元素**和**选择器**二者必填其一且互斥
- **[选择器](../../Appendix/Selector.md?_v=v2020.4)** ：用于指示要获取文本的目标元素。可通过点击**指定元素**自动生成。属性**控件元素**和**选择器**二者必填其一且互斥。仅支持字符串变量和字符串
- **匹配超时(毫秒)** ：限定查找目标元素时间，超出指定时间后将不再等待。若超过此时间还未匹配到指定元素则会抛出错误。单位为毫秒（ms）,1000ms = 1s。仅支持整型变量和整型

输出

- **纯文本** ：将获取到的文本内容存储到此变量。仅支持字符串变量和字符串
- **文本元素列表** ：将获取到的文本元素列表存储到此变量。你可以使用列表的子集作为点击等组件的输入。在对这些元素进行操作时，只支持模拟鼠标键盘的方式，不支持设置控件。

## 操作样例
1. 拖入**获取屏幕文本**组件并指定Adobe Acrobat右侧工具栏：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getScreenTxt1.png)

2. 运行流程并查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/getScreenTxt2.png)