# 使用 ViCode 运行并展示 RPA 流程结果

## 操作背景

抓取股票网中的数据并展示在 ViCode 应用中。

## 操作步骤

### 使用编辑器设计流程

将网页中的结构化数据抓取并显示在数据表中。

1. 拖入一个“打开浏览器”组件至流程中，并配置需要打开的网页，如，`"http://quote.eastmoney.com/center/gridlist.html#hs_a_board"`。

    ![打开浏览器](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/openbrowser20211206.png)

2. 在“打开浏览器”组件内部，拖入一个“获取结构化数据”组件, 获取股票数据。

    ![获取结构化数据](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/getextradata20211206.png)

3. 在“获取结构化数据”组件下方，拖入一个“添加数据列”组件，配置数据表的主键字段 `id`。

    ![添加数据列](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/adddatacolumn20211206.png)

4. 在“打开浏览器”组件下方，拖入一个“连接数据库”组件，将获取到的网页数据保存至数据库中。

    > **说明：**
    >
    > 此处数据库的连接字符串，来源于“控制台 > 数据中心 > 连接管理”创建的托管数据库详情中。

    ![连接数据库](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/connectdatabase20211206.png)

5. 在“连接数据库”组件内部，拖入一个“插入数据”组件，将获取到的网页数据插入至该数据库中已存在的 `gupiao` 数据表中。

    > **说明：**
    > `gupiao` 数据表，可通过“ViCode > 新建应用 > 数据模型”导入连接器并创建数据表建立。

    ![插入数据](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/insertdata20211206.png)

### 将流程发布至控制台并部署流程

1. 在编辑器中，单击菜单栏中的“发布”，将编辑完成的流程发布至控制台中。

    ![发布流程至控制台](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/publishworkflow20211206.png)

2. 发布完成的流程，在控制台的“RPA 管理 > 流程包管理”中，可查看。

    ![流程包管理](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/consoleworkflow20211206.png)

3. 单击“流程包管理”操作栏中的“流程部署”，部署完成的流程点击左侧“流程部署”菜单，可查看。

    > **说明：**
    >
    > 在流程部署过程中，需要提前将编辑好的流程发布至机器人，以指定该机器人执行。

    ![流程部署](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/workflowdeploy20211206.png)

### 使用 ViCode 设计流程的展示界面

1. 在 ViCode 应用的“数据模型”中，导入数据连接。

    > **说明：**
    >
    > 导入的“数据连接”为“控制台 > 数据中心 > 连接管理”中创建的托管数据库的数据连接。

    ![导入连接器](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/importconnect20211206.png)

2. 在托管数据库的数据连接中，选择已创建的数据表 `gupiao`，单击“确定”。

    ![创建数据表](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/createtable20211206.png)

3. 在 ViCode 应用的“大纲”页面中，拖入一个“流程”组件，并选择已配置的“流程部署”流程 `wangxin_workflowdeploy`，单击“创建”。

    ![添加流程](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/workflow20211206.png)

4. 在 ViCode 应用的“大纲”页面中，拖入一个“表格”组件，并配置数据源及相关属性，这里的数据源为上方已创建的 `gupiao` 表。

    ![表格添加数据源](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/datasource20211206.png)

    ![配置属性](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/tablesetting20211206.png)

5. 保存并预览 ViCode 应用，当点击“提交”按钮时，可执行流程且显示最新数据。

    ![显示数据](https://docimages.blob.core.chinacloudapi.cn/images/BestPractices/showdata20211206.png)
