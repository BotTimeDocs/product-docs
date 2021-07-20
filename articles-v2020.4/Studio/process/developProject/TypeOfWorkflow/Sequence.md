# 序列

## 概述

**序列**是最小的项目类型。它们适用于线性过程，因为它们使你能够无缝地从一个组件转到另一个组件，并可以充当单个组件块。

序列的关键特征之一是它们可以作为独立的自动化项目或流程图的一部分而一次又一次地被重用。

请注意，由于Windows Workflow Foundation的限制，每当你希望将大量组件从一个序列复制到另一个序列时，建议事先向下滚动到编辑区域的底部。

>**注意：**
>
>序列不使用连接线。

## 使用示例

创建一个询问用户的姓名及年龄，然后显示他的答案的示例，来对序列进行说明。具体操作如下：

1. 创建一个空白的流程项目。在“开始页”中点击“新建流程项目”新建一个项目，并输入项目名称，例如 “sequenceTest”。

    ![创建项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/sequencetestitem20201019.png)

2. 从组件面板拖动“序列”组件到编辑区域

    ![序列](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/sequenceactivity20201019.png)

3. 创建两个字符串型（String）变量，如Name和Age，以便你可以在其中存储来自用户的数据。将默认字段保留为空，以表示没有默认值。

    ![创建变量](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-createVariables.png)

4. 将两个“输入框”组件拖到编辑区域上，一个在另一个下面。

    ![输入框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/inputboxinsequence20201019.png)

5. 选择第一个“输入框”，然后在属性面板中添加一个要求填入用户姓名的描述和一个自定义标题。

6. 在输入的内容字段中，添加Name变量。这表明此变量将被用户此时添加的值更新。

    ![输入框属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-input1Properties.png)

7. 对第二个 “输入框”组件重复步骤5-6 ，询问用户年龄，并将其存储在Age变量中。

    ![输入框属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-input2Properties.png)

8. 在第二个“ 输入框”下添加“确认框”组件。

    ![确认框](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/comfirminsequence20201019.png)

9. 选择“确认框”，然后在属性面板的“描述”字段中添加变量和字符串，以使你可以显示从用户那里收集的所有信息，例如：Name+"的年龄为"+Age+"岁。"</br>（可选）“标题”字段可填入"用户信息"

    ![确认框属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-confirmProperties.png)

10. 最终，序列如下所示：

    ![示例](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/seq-example.PNG)

在运行面板中点击“运行”，输入Tewin，24，最终结果将显示Tewin的年龄为24岁。

![结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/typeOfWorkflow/sequenceresult20201019.png)
