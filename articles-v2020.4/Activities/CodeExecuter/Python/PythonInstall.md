# 安装 Python

## 视频示例

## 概述

选择已下载至本地的 Python 安装文件，安装到指定目录。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

### 可选项

- **安装至目录**：输入 Python 的安装目录，可接变量。

  >**说明：**
  >
  > 若不输入，则使用默认安装路径：C:\Users\{user}\AppData\Local\Programs。

### 输入

- **安装文件路径**：Python 安装包所在的文件路径，可接变量。
  
  > **说明：**
  >   
  > 文件类型支持 ".exe" 和 ".msi"。

## 使用示例
1. 从 [Python 官网](https://www.python.org/downloads/)下载 python 安装包，保存至本地电脑。
2. 拖入**安装 Python** 组件至流程中。
3. 双击打开该组件，选择已下载的 Python 安装包。
4. 配置需要对应安装路径的属性参数。
   
   ![配置安装路径](https://docimages.blob.core.chinacloudapi.cn/images/Activities/installpython20201216.png)

5. 保存并运行流程。
6. 在命令行提示符中输入`python` ,出现版本号信息，即安装成功。
   ![验证Python是否安装成功](https://docimages.blob.core.chinacloudapi.cn/images/Activities/pythonsucess20201216.png)