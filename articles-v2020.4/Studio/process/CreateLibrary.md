# 创建组件项目

## 组件项目

**组件项目**是一个包含一个或多个可重复使用组件的项目。通过将该项目发布到组件市场，可以将其作为组件包安装到其他项目中，作为依赖项进行使用。

组件项目的创建类似于[创建流程项目](./CreateProject.md)，其主要区别在于组件项目可在其他项目中进行引用。

在你启动编辑器并创建一个组件项目后，默认情况下，该项目将会存放在路径-%USERPROFILE%\Documents\Encoo下。

## 创建流程

本示例将教你如何创建一个组件项目，并将其发布到组件市场，在其他项目中进行使用。我们将从一个Excel文件中获取部分数据，并将其添加到另一个Excel文件中。

1. 打开云扩RPA编辑器

2. 在开始页，新建一个组件项目，并输入项目名称（以Excel数据迁移为例）。选择位置并设置类型，关于高级设置可查看[创建流程项目](./CreateProject.md)，此处皆使用默认值
![创建组件项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/newlibrary20201112.png)

3. 打开参数列表，创建两个字符串型（String）的输入变量，其将作为发布后组件的输入属性：
    - 读取路径  --要读取数据的Excel文件所在路径
    - 写入路径  --要写入数据的Excel文件所在路径
![打开参数列表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/createref20201112.png)
4. 从组件面板搜索“打开/新建”组件，并将其拖入到编辑区域连接至开始节点
![打开新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/opencreate20201112.png)

5. 在该组件的属性面板，输入以下内容：
    - 文件路径：读取路径
![读取路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/readpath20201112.png)
6. 从组件面板搜索“读取区域”组件，，并将其拖入到“打开/新建”组件内部
![读取区域组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/readarea20201112.png)
7. 在该组件的属性面板，输入以下内容：
    - 工作表："Sheet1"  --要读取数据的工作表名称（以默认名称Sheet1为例）
    - 区域："A1:B6" --要读取的区域
    - 数据：Data  --单击该字段后的输入框，输入Data作为变量名称，全选Data并使用快捷键Ctrl+B创建该变量
![读取区域属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setactivities20201112.png)
8. 再次从组件面板拖入一个“打开/新建”组件，连接到上一个“打开/新建”组件
![第二个打开新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/opencreatetwo20201112.png)

9.  在该组件的属性面板，输入以下内容：
    - 文件路径：写入路径
![写入路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/writepath20201112.png)
10. 从组件面板搜索“写入区域”组件，，并将其拖入到第二个“打开/新建”组件内部
![写入区域](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/writearea20201112.png)
11. 在该组件的属性面板，输入以下内容：
    - 工作表："Sheet1"  --要写入数据的工作表名称（以默认名称Sheet1为例）
    - 起始单元格："A1"
    - 数据表：Data  
![写入区域属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setwritearea20201112.png)
## 运行流程

1. 点击“运行”或使用快捷键 Ctrl+F6 来尝试运行流程

2. 设置参数的默认值并确认，将会从第一个Excel文件中读取一部分数据填写到第二个Excel文件中。 
![设置流程参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setflowref20201112.png)

## 发布组件项目

如果你要将这个项目做为可重用的组件，添加到其他自动化项目中，就需要将其打包，发布到组件市场中。

1. 打开创建的组件项目

2. 在菜单栏，点击“发布到组件市场”，打开发布窗口
   ![发布到组件市场](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/publishactivities20201112.png)
    - 选择你要发布的目标市场，若没有市场，可点击“管理市场”进行创建。关如何创建市场，请查看[管理市场](../market/Market.md)
    - 在**最新版本号**字段中，你可以设置当前发布的版本号
    - 在**描述**字段中，你可以添加有关此组件项目的详细信息

## 导出组件项目
如果需要将组件项目导出，供其他项目进行引用，可选择项目进行右击选择“导出项目”，在弹出的“导出项目”对话框中，按需选择导出相关配置。

![导出项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Debugging/exportproject20201214.png)

>**说明：**
>导出的组件项目以“.egs”为扩展名，区别于以“.dgs”为扩展名的流程项目。

## 安装并使用组件

如果你要在另外一个自动化项目中使用该组件包，需要先安装，将其添加为自动化项目的依赖项。

1. 创建一个流程项目，可查看[创建流程项目](./CreateProject.md)

2. 在组件面板中，点击“组件市场”，打开组件市场窗口


3. 在窗口左侧选择之前创建的市场，搜索发布的组件包并选择。在我们的示例中，该组件包名为Excel数据迁移

4. 单击“安装”，安装完成关闭窗口。此时，该组件包已添加到当前流程项目中，并在组件面板中可见
![组件安装](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/useactivitiesmarket20201112.png)

5. 从组件面板中，将“Excel数据迁移”组件拖入到编辑区域并连接到开始节点

6. 在该组件的属性面板，输入以下内容：
    - 读取路径："C:\Users\用户名\Documents\Encoo\使用组件项目所编辑的组件\start.xlsx"  --要读取数据的Excel文件全路径
    - 写入路径："C:\Users\用户名\Documents\Encoo\使用组件项目所编辑的组件\final.xlsx" --要写入数据的Excel文件全路径

    >注意：
    >
    >若组件含有路径类属性，不能使用相对路径，必须使用全路径。

7. 点击“运行”，即可将start.xlsx的部分数据迁移到final.xlsx中
![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/runresult20201112.png)