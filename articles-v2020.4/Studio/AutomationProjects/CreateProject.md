# 创建自动化项目
### 自动化项目
**自动化项目**是用于管理所有跟单个自动化任务相关的所有流程文件的集合，比如你需要创作一个定时处理客户订单的自动化流程，就可以创建一个自动化项目，跟这个任务相关的所有子流程文件、依赖项等信息都会出现在这个项目中。自动化项目是你进行开发、发布以及部署给机器人运行的基本单位。通常情况下，每一个独立的工作任务都应该创建一个新的自动化项目。

在你启动编辑器并创建一个新项目后，默认情况下，该项目将会存放在路径-%USERPROFILE%\Documents\Encoo下。

该项目中包含了以下两个部分：
- 自动创建的Main.xaml流程文件。该文件作为流程执行时的开始文件，包含编辑器的主要流程。
- 其他的.xaml流程文件。这些文件需要通过[调用流程](../../Activities/WorkflowControl/InvokeWorkflow.md?_v=v2020.4)组件，将其与Main.xaml文件连接起来，因为当运行或调试自动化流程时，将从Main.xaml文件开始。

## 创建流程
本示例将教你如何创建并运行一个基本自动化项目。我们将会打开浏览器，搜索天气预报，获取明天的天气信息，并进行提示：明天是否有雨。

1. 打开云扩RPA编辑器
2. 新建一个项目，并输入项目名称（以 MyFirstProject 为例） </br>
   针对高级设置下的**桌面录制技术**选择，推荐使用UIA3。

   UIA3和UIA的区别在于对于不同技术的支持力度不同： </br>
   * 对于WPF和Windows Store Apps，UIA3支持力度更佳；
   * 对于C#和WinForms，UIA支持力度更佳。

    >注意：
    >
    >UIA3和UIA不可以同时使用于同一个项目中。

    ![创建项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/newProject.PNG)

3. 从组件面板，搜索“打开浏览器”组件，并将其拖入到编辑区域连接至开始节点
4. 在该组件的属性面板中，输入以下内容：
    - 浏览器类型：IE
    - 网址："https://www.baidu.com"

    ![打开浏览器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoOpenBrowser.PNG)

5. 双击“打开浏览器”组件，并点击菜单栏-工具下的“智能录制”，打开录制器
6. 打开IE浏览器的百度网站的首页，然后点击录制器的“智能录制”进行网站操作的录制 

    ![录制](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/baidu.PNG)

7. 点击百度首页的搜索文本框，在出现的弹框中输入要搜索的词条（以天气为例） 

    ![输入文本](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/inputTianqi.PNG)

8. 点击百度一下，或者按 Enter 键 

    ![百度一下](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/clickBaidu.png)

9.  打开录制器界面，选择“文本”->“获取文本”，当出现黄色矩形框时，点击明天的天气信息以获取天气文本

    ![获取文本](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/getText.png)

10. 按下键盘的“Esc”快捷键结束网站操作的录制 
11. 点击录制器的“保存&退出”将录制好的自动化流程保存至编辑器中 

    ![保存流程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/saveExit.PNG)

12. 打开变量列表，创建一个字符串型（String）变量-weather，用于存储获取到的天气文本 

    ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/createVariable.PNG)

13. 选中“获取文本”组件，在属性面板中，输入以下内容：
    - 文本：weather 

    ![输入变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/inputWeather.PNG)

14. 从组件面板拖入一个“条件（If）”组件连接到“获取文本”组件，在该组件的属性面板中，输入以下内容：
    - 判断条件：weather.Contains(“雨”)

    ![拖入条件组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoIf.PNG)

15. 拖入一个确认框组件到条件的Then部分，并在该组件的属性面板中，输入以下内容：
    - 标题："明日天气提醒"
    - 描述："明天有雨，记得带伞哦" 

    ![拖入确认框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoInput.PNG)

16. 拖入另一个确认框到条件的Else部分，并在该组件的属性面板中，输入以下内容：
    - 标题："明日天气提醒"
    - 描述："明天无雨，出去走走吧"


## 运行流程
1. 点击“运行”来尝试运行自动化流程

    <!-- ![运行项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/runProject.PNG) -->

2. 运行过程中，编辑器会自动回放录制的过程，并提示明天是否有雨 

    <!-- ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/result.png) -->


