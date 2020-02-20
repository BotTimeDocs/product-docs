# 流程图 
**流程图**可用于各种情况，从大型项目到小型项目，您都可以在其中重复使用它。

与序列不同，流程图最重要的方面是适用于更加复杂的业务逻辑。您可以运用多个不同的逻辑运算符以更多样化的方式简单快速地集成自动化项目。 

## 流程图示例 
创建一个对用户登录进行判断的实例来对流程图进行说明。

1. 创建一个空白的自动化流程项目。在工具栏-设计中单击新建项目图标新建一个项目，并输入项目名称，例如 “flowTest”。 
![创建项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-createProject.png)

2. 单击“变量”，唤出变量面板，并单击“创建变量”，创建两个String型变量（name、password）。
![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-createVariables.png)

3. 将“流程图”添加至设计窗口中，并连接到“开始”节点。
* 显示名称：“用户登录”
![流程图](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-intoFlowchart.png)

4. 双击打开流程图，将“输入框”添加至流程图中，并连接到“开始”结点。
![输入框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-intoInput1.png)

5. 在“输入框”的属性窗口中，输入如下内容： 
* 输入的内容：name 
* 标题："用户名"
* 描述："请输入用户名" 
* 显示名称：输入用户名 
![输入框属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-input1Properties.png)

6. 将“流程决策”添加到设计窗口中，并连接到“输入框”。此组件可以判断用户是否正确输入用户名。 
![流程决策](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-intoDecision1.png)

7. 在“流程决策”的属性窗口中输入如下内容： 
* 判断条件：name==""。该字段用来判断用户名是否为空 
* 显示名称：判断用户名是否为空。该字段可自行更改为您所想要的其他内容 
![流程决策属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-decision1Properties.png)

8. 添加一个“输入框”连接到流程决策的False分支。流程决策的True分支连接到上一个“输入框”，用来重新输入用户名。
![输入框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-intoInput2.png)

9. 在“输入框”的属性窗口中，输入如下内容： 
* 输入的内容：password 
* 标题："密码"
* 描述："请输入密码"
* 显示名称：输入密码 
![输入框属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-input2Properties.png)

10. 添加一个“流程决策”并连接到“输入框”。此组件能够判断用户是否正确输入密码。 
![流程决策](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-intoDecision2.png)

11. 在“流程决策”的属性窗口中输入如下内容： 
* 判断条件：password==""。该字段用来判断密码是否为空 
* 显示名称：判断密码是否为空。该字段可自行更改为您所需要的其他内容 
![流程决策属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-decision2Properties.png)

12. 添加一个“确认框”连接到流程决策的False分支。流程决策的True分支连接到上一个“输入框”，用来重新输入密码。 
![确认框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-intoConfirm.png)

13. 在“确认框”的属性窗口中输入如下内容： 
* 标题："用户登录"
* 描述：name+"登录成功" 

14. 最终，流程图如下所示： 
![示例](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-example.PNG)

在工具栏-设计中单击“运行”，输入用户名、密码，最终结果将显示Tewin登录成功。 
![结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/flow-result.png)

