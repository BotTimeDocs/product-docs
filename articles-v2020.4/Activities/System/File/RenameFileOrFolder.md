# 重命名文件/文件夹

可实现对指定文件或文件夹重命名

## 属性

输入

- **类型** ：选择操作文件或文件夹
- **原路径** ：输入原文件或文件夹路径。仅支持字符串变量和字符串
- **新名称** ：输入文件或文件夹新名称。仅支持字符串变量和字符串

可选项

- **是否覆盖** ：选择是否覆盖同名文件或文件夹

输出

- **新路径** ：输出重命名后的文件或文件夹路径。仅支持字符串变量

## 操作样例
1. 拖入**重命名文件/文件夹**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/renameFile-1.png)

2. 双击进入组件内部，配置属性参数。
- 重命名类型：可以选择文件或者文件夹；
- 原路径：点击“...”弹出对话框，选择目标文件/文件夹，或者手动输入路径；
- 新名称：支持输入字符串变量和字符串：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/renameFile-2.png)

3. 运行流程，E盘的文件“新建 DOC 文档.doc”已经被重命名为“新的文件名.doc”：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/renameFile-4.png)