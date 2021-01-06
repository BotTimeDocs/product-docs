# 读取文件

读取指定文件内容并可将其数据存储在变量中

## 属性

### 可选项
- **编码方式** ：文件的编码方式。可以在 [此处](../../Appendix/Encoding.md?_v=v2020.4) 找到每个字符编码的完整代码列表。要指定要使用的编码类型，请使用&quot; 名称&quot;字段中的值。如果未指定编码类型，则活动将搜索文件的字节顺序标记以检测编码。如果未检测到字节顺序标记，则默认选择系统ANSI代码页。仅支持字符串变量和字符串

### 输出

- **文件内容** ：将目标文件内容存储到此变量

### 输入

- **文件路径** ：读取此路径文件的内容。支持相对和绝对路径。可在组件面板点击弹出对话框，选择目标文件；亦支持手动输入路径，若路径不存在，则运行失败。仅支持字符串变量和字符串

## 操作样例
1. 拖入**读取文件**组件到设计面板，双击进入组件内部，在组件面板点击“...”弹出对话框，选择目标文件；或者手动输入路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/readFile-1.png)

2. 添加输出结果变量fileContent：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/readFile-2.png)

3. 拖入**写入日志**组件，可以输出选择的文件内容信息。

4. 运行流程，查看输出的文件内容信息：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/readFile-3.png)

