# 流程组件
该组件为模板组件。

流程组件用于为控制台的流程部署创建一个可以交互的前端显示。
在讲解组件的用法之前，我们需要做如下步骤在控制台配置流程部署（详细操作步骤请参见控制台文档）：
1. 注册控制台账号
2. 在控制台指定资源组下将流程包上传至流程包管理
3. 跳转到流程部署，创建流程部署，流程部署关联上传的流程包，并配置可以运行的机器人。
4. 配置完毕后，即可打开工作台站点，创建应用。

## 添加流程组件
选中页面，拖拽“流程”组件至页面内。

在配置窗口内选择你想要的流程部署，点击确定，流程组件即可添加至当前页面。

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/workflow1.png)

添加时，系统将根据你选择的流程，在模拟界面加载出该流程包含的所有参数及其对应的默认控件。
以下罗列我们目前识别的参数类型及其对应的默认控件类型：
- Boolean：是/否
- Double：数字
- Int32：数字
- Int64：数字
- System.String：文本	
- System.DateTime：日期	
- System.String[]： 批量文件上传	
- 其他类型：文本
 
添加成功后，页面将会将组件渲染至页面
![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/workflow2.png)

## 配置显示参数

选中页面内的“流程组件”，右侧属性栏即可切换到参数选择。
参数选择会罗列你导入的流程包，版本号，及[流传文件的参数列表](../../Studio/process/developProject/Arguments/Arguments.md)。
你可以通过单击参数前的复选框，调整参数是否需要显示在应用页面上。
当你取消勾选参数时，参数不会出现在页面上，应用也不会向参数传值。
当你勾选参数时，参数会出现在页面上，应用被提交后将对参数赋值。
![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/workflow3.png)

如果你想要调换参数的次序，你可以在模拟页面中选中参数对应的组件，通过上下拖拽的方式调换参数次序。

## 单个组件设置

单击模拟界面的组件，选中组件后，即可在右侧编辑组件信息。

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/AppsV2/workflow4.png)

当前支持对控件的设置如下：
- 参数名：展示流程中当前参数的名称
- 展示名称：组件对应标签的名称
- 是否可更改：不可更改的参数，系统将作为标签展示参数默认值，若没有设置默认值，则仅展示标签
- 是否必填: 打开此选项意味着我们会在前端校验当前参数必填
- 参数类型：展示流程中当前参数的数据类型
- 控件类型：允许用户调整交互控件类型，不同参数对应的控件选择列表见下

### 参数与组件

![devmode](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/setcomponent1.png)


你对组件的所有内容的编辑，都可即时在模拟界面上查看。
