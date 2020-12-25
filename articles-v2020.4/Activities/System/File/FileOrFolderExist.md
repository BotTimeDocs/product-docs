# 文件/文件夹是否存在

判断指定文件或文件夹是否存在，并返回结果

## 属性

输入

- **类型** ：下拉框选择判断类型为文件或文件夹
- **路径** ：执行判断的文件或文件夹路径。支持相对和绝对路径。仅支持字符串变量和字符串

输出

- **路径是否存在** ：将判断结果存储在此变量
## 操作样例
1. 拖入**文件/文件夹是否存在**组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-1.png)

2. 双击进入组件内部，"路径"需手动输入，支持相对和绝对路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-2.png)

3. 新建变量"exists"，用于判断路径是否存在：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-3.png)

4. 拖入**写入日志**组件：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-4.png)

5. 运行流程，判断文件"E:\shirley\hello.txt"存在，输出"True"：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/isExist-5.png)