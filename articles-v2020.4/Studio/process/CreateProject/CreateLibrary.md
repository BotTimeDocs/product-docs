# 创建组件项目

## 组件项目

**组件项目** 是一个包含一个或多个可重复使用组件的项目。通过将该项目发布到组件市场，可以将其作为组件包安装到其他项目中，作为依赖项进行使用。

组件项目的创建类似于 [创建流程项目](./CreateProject.md)，其主要区别在于组件项目可在其他项目中进行引用。

在你启动编辑器并创建一个组件项目后，默认情况下，该项目将会存放在路径-`%USERPROFILE%\Documents\Encoo` 下。

## 创建流程

本示例将教你如何创建一个组件项目，并将其发布到组件市场，在其他项目中进行使用。我们将从一个 Excel 文件中获取部分数据，并将其添加到另一个 Excel 文件中。

1. 打开云扩 RPA 编辑器

2. 在开始页，新建一个组件项目，并输入项目名称（以 Excel 数据迁移为例）。选择位置并设置类型，关于高级设置可查看 [创建流程项目](./CreateProject.md)，此处皆使用默认值
![创建组件项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/newlibrary20201112.png)

3. 打开参数列表，创建两个字符串型（String）的输入变量，其将作为发布后组件的输入属性：
    - 读取路径  --要读取数据的 Excel 文件所在路径
    - 写入路径  --要写入数据的 Excel 文件所在路径
![打开参数列表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/createref20201112.png)
4. 从组件面板搜索“打开/新建”组件，并将其拖入到编辑区域连接至开始节点
![打开新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/opencreate20201112.png)

5. 在该组件的属性面板，输入以下内容：
    - 文件路径：读取路径
![读取路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/readpath20201112.png)
6. 从组件面板搜索“读取区域”组件，，并将其拖入到“打开/新建”组件内部
![读取区域组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/readarea20201112.png)
7. 在该组件的属性面板，输入以下内容：
    - 工作表："Sheet1"  --要读取数据的工作表名称（以默认名称 Sheet1 为例）
    - 区域："A1: B6" --要读取的区域
    - 数据：Data  --单击该字段后的输入框，输入 Data 作为变量名称，全选 Data 并使用快捷键 Ctrl+B 创建该变量
![读取区域属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setactivities20201112.png)
8. 再次从组件面板拖入一个“打开/新建”组件，连接到上一个“打开/新建”组件
![第二个打开新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/opencreatetwo20201112.png)

9. 在该组件的属性面板，输入以下内容：
    - 文件路径：写入路径
![写入路径](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/writepath20201112.png)
10. 从组件面板搜索“写入区域”组件，，并将其拖入到第二个“打开/新建”组件内部
![写入区域](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/writearea20201112.png)
11. 在该组件的属性面板，输入以下内容：
    - 工作表："Sheet1"  --要写入数据的工作表名称（以默认名称 Sheet1 为例）
    - 起始单元格："A1"
    - 数据表：Data  
![写入区域属性](https://docimages.blob.core.chinacloudapi.cn/images/Studio/workingProcess/setwritearea20201112.png)

## 运行流程

1. 点击“运行”或使用快捷键 Ctrl+F5 来尝试运行流程

2. 设置参数的默认值并确认，将会从第一个 Excel 文件中读取一部分数据填写到第二个 Excel 文件中。
![设置流程参数](https://docimages.blob.core.chinacloudapi.cn/images/Studio/path20210508.png)
