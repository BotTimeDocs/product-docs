# 新建文件/文件夹

新建文件或文件夹到指定位置

## 属性
### 基本

### 输入

- **路径** ：新建文件或文件夹的全路径。支持相对和绝对路径。若全路径中包含不存在的文件夹，则自动新建。仅支持字符串变量和字符串
- **路径类型** ：下拉框选择新建文件或文件夹
  
### 可选项
- **同名替换**：若有同名文件/文件夹则替换。

   - 勾选时：若有同名文件/文件夹则替换。
   - 不勾选时（默认不勾选）：有同名文件/文件夹则报错：“新建失败，有相同名称文件/文件夹”。
   
## 操作样例
1. 拖入**新建文件/文件夹**组件到设计面板：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/newFile-1.png)

2. 双击进入组件内部，输入新建文件/文件夹的全路径，支持相对和绝对路径：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/newFile-2.png)

3. 运行流程，可以看到指定的路径下根据用户要求创建了文件或文件夹：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/newFile-3.png)