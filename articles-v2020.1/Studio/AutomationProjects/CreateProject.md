# 创建自动化项目
## 创建流程
1. 打开云扩编辑器
2. 新建一个项目，并输入项目名称（以 MyFirstProject 为例） 

    ![创建项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/newProject.PNG)

3. 从组件窗口，搜索“打开浏览器”组件，并将其拖入到设计窗口连接至开始节点
4. 在该组件的属性窗口输入类别下的网址字段中填入"https://www.baidu.com"

    ![打开浏览器](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoOpenBrowser.PNG)

5. 双击“打开浏览器”组件，并点击工具栏里的“录制”，打开录制器
6. 打开IE浏览器的百度网站的首页，然后点击录制器的“智能录制”进行网站操作的录制 

    ![录制](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/baidu.PNG)

7. 点击百度首页的搜索文本框，再出现的弹框中输入要搜索的词条（以天气为例） 

    ![输入文本](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/inputTianqi.PNG)

8. 点击百度一下，或者按 Enter 键 

    ![百度一下](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/clickBaidu.png)

9. 打开录制器界面，选择文本-获取文本，点击第二栏的天气 

    ![获取文本](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/getText.png)

10. 按下键盘的“Esc”快捷键结束网站操作的录制 
11. 点击录制器的“保存&退出”将录制好的自动化流程保存至编辑器中 

    ![保存流程](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/saveExit.PNG)

12. 打开变量面板，创建一个String变量-weather，用于存储获取到的天气文本 

    ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/createVariable.PNG)

13. 点击“获取文本”组件，在属性面板中的文本字段中输入变量weather 

    ![输入变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/inputWeather.PNG)

14. 从组件窗口拖入一个“条件（If）”组件连接到“获取文本”组件，属性面板的条件字段中输入weather.Contains(“雨”)

    ![拖入条件组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoIf.PNG)

15. 拖入一个确认框组件到条件的Then部分，并在输入类别下输入相关提示信息：
 * 标题："明日天气提醒"
 * 描述："明天有雨，记得带伞哦" 

16. 拖入另一个确认框到条件的Else部分，并在输入类别下输入相关提示信息：
 * 标题："明日天气提醒"
 * 描述："明天无雨，出去走走吧"

    ![拖入确认框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/intoInput.PNG)


## 运行流程
1. 点击“运行”来尝试运行自动化流程

    ![运行项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/runProject.PNG)

2. 运行过程中，编辑器会自动回放录制的过程，并提示明天是否有雨 

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/automationProject/createProject/result.png)


