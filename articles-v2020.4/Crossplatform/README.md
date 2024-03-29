# ENCOO RPA 信创版

ENCOO RPA 扩展信创版集成在VS Code中，帮助您使用Python快速实现自动化脚本。
- 捕获UI元素并通过简单的点击轻松抓取数据;
- 支持具有多种自动化技术的 Web 和桌面应用程序;
- 对 Chrome、奇安信等浏览器全面支持;

## 快速设置
安装后通过“ENCOO RPA：欢迎（快速设置）”转到扩展程序的欢迎页面，或按照以下步骤操作：

**系统要求**
  - 操作系统：统信UOS、麒麟
  - 安装Python 3.7 或更高版本
  - 安装.Net 7.0 

## 创建自动化项目

- 在vscode中按 ctrl+shift+p ，选择Clicknium:Create Project. 等待python虚拟环境安装完成。
- 在虚拟环境中安装clicknium python库。

## 通过示例项目学习

- 打开命令面板：“Ctrl+Shift+P”
- 输入或选择：“Clicknium: Sample”以选择新文件夹或现有文件夹

然后，使用默认定位器存储“sample”创建示例。 

“sample.py”包含一个自动化示例：Chrome Web 自动化。

```Python
from time import sleep
from clicknium import clicknium as cc, locator, ui

def main():
    # sample code to demo web automation and desktop application
    tab = cc.chrome.open("https://www.bing.com/")
    tab.find_element(
        locator.sample.bing.search_sb_form_q).set_text('clicknium')
    tab.find_element(locator.sample.bing.svg).click()
    sleep(3)
    tab.close()

if __name__ == "__main__":
    main()
```

## 启用浏览器扩展

- 点击Visual Studio Code Activity Bar中的“Clicknium Explorer”
- 在Visual Studio Code Side Bar中显示“自动化扩展”视图。 
- 选择Chrome浏览器，然后单击“安装”按钮。 
- 安装后，打开Chrome浏览器以启用“点击记录器”扩展。



## 运行/调试

- 通过Visual Studio Code内置命令：
  - “F5”调试“sample.py”
  - “Ctrl+F5”运行“sample.py”

**注意：调试/运行前请在本机先安装对应版本的云扩RPA机器人并激活，且处于启用状态。**

## 定位器

在Visual Studio Code中，按“Ctrl + F10”将调用ENCOO RPA Recorder并最小化当前的Visual Studio Code窗口。 


调用定位器后，将鼠标移动到目标应用程序。它将突出显示已识别的元素，
要捕获元素，请按“Ctrl”并单击，元素定位器将被存储。


## 编辑和验证定位器

记录后，可以在定位器选项卡中打开、编辑和验证定位器：
![clicknium Visual Studio code](https://docimages.blob.core.chinacloudapi.cn/images/CrossPlatform/1.png)

## 在 Python 代码中使用定位器
Clicknium 提供智能自动完成体验。选择Clicknium包下的定位器类，并通过“定位器”引用定位器。{localorStoreName}.{文件夹名称}.{locator名称}。

![use locator](https://docimages.blob.core.chinacloudapi.cn/images/CrossPlatform/2.png)


## 打包自动化项目
- 项目编写完成后，按ctrl+shift+p 选择CLicknium:Package Project，再选择 zip 类型， 等待打包完成。
- 在机器人或控制台将打包后的zip格式流程包导入即可运行。


## 视频示例

<video controls height='100%' width='100%' src="https://docimages.blob.core.chinacloudapi.cn/images/CrossPlatform/%E4%BF%A1%E5%88%9B%E8%A7%86%E9%A2%91DEMO.mp4"> 
</video>

## 联系我们

- 邮箱：[contact@encootech.com](mailto:contact@encootech.com)
- 电话：400-639-2198