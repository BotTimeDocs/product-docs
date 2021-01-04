# 获取文件/文件夹列表

获取指定路径下的文件或文件夹列表。同时提供选择&quot;遍历子文件夹&quot;选项和通配符筛选列表内容功能

## 属性

输入

- **路径** ：获取该路径下的文件或文件夹列表。支持相对和绝对路径。可在组件面板点击弹出对话框，选择要获取列表的路径；亦支持手动输入路径，若路径不存在，则运行失败。如果需要获取当前项目路径下的列表，则只输入双引号即可
- **列表模式** ：下拉框选择文件或文件夹
- **列表筛选** ：适用此筛选条件返回列表，支持通配符&quot;\*&quot; &quot;?&quot;。仅支持字符串变量和字符串
- **遍历子文件夹** ：勾选时，将同时获取指定路径子文件夹内的列表；不勾选时；则只获取指定路径内列表

输出

- **列表** ：将结果列表存储在此变量。返回类型为全路径

## 操作样例
1. 拖入**获取文件/文件夹列表**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-1.png)

2. 双击进入组件内部，配置属性参数。
 - 路径：可点击“...”选择要获取列表的路径,也支持手动输入；
 - 列表模式 ：下拉框选择文件或文件夹，这里我们选择文件；
 - 列表：将结果列表存储在此变量，如下图变量“files”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-2.png)

3. 拖入**循环操作（For Each）**组件到设计面板,循环处理文件列表中的每个文件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-3.png)

4. 在**循环操作（For Each）**组件中拖入**写入日志**组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-4.png)

5. 运行流程，打印出指定目录下的文件列表：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/fileList-5.png)