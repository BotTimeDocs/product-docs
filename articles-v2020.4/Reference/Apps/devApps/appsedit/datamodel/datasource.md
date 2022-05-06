# 数据源管理

## 概述

**数据源管理** 用于管理并配置应用内的数据源的使用权限。目前支持 SQL、RESTfulAPI、RESTfulAPI 模板、文件类连接、数据表等类型的数据源。

## 前提条件

已在控制台的“数据中心 > 连接管理”中已创建对应类型的数据连接且可以测试连接成功。

## 添加数据库类数据源

### 添加数据表

1. 在数据模型页面，单击“+”图标，选择“数据表”，可自定义数据表名称。
2. 在页面右侧选项页中，可对数据表的数据、模型、权限管理进行相应地操作。

    ![数据表操作](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/datatable20211125.png)

### 添加查询语句

1. 在数据模型页面，单击“+”图标，选择“查询语句”，可自定义查询语句名称。
2. 在页面右侧选项页中，可对查询语句的配置信息、权限管理进行相应地操作。

    ![查询语句操作](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/select20211125.png)

### 添加执行语句

1. 在数据模型页面，单击“+”图标，选择“执行语句”，可自定义执行语句名称。
2. 在页面右侧选项页中，可对执行语句的配置信息、权限管理进行相应地操作。

    ![执行语句操作](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/execute20211125.png)

## 添加 RESTfulAPI 类数据源

### 添加添加 RESTfulAPI 数据源

1. 在数据模型页面，单击“+”图标，选择“RESTfulAPI”，可自定义RESTfulAPI名称。
2. 在页面右侧选项页中，可对RESTfulAPI的配置信息、权限管理进行相应地操作。

    - **请求**：下拉选择请求方式。
       - GET：从服务器取出一项或多项资源。
       - POST：在服务器新建一个资源。
       - PUT：在服务器更新资源（客户端提供改变后的完整资源）。
       - PATCH：在服务器更新资源（客户端提供改变的属性）。
       - DELETE：从服务器删除资源。
    - **Uri Query**：基于 URI 的路径信息。
    - **Headers**：填写对应 Headers 信息。
    - **Body**：返回请求内容的数据编码格式。
       - JSON：返回 JSON 格式。
       - RAW：返回未经加工的 RAW 图像格式。
       - x-www-form-unlencoded：返回 url 格式的编码，如，`Content-Type:application/x-www-form-urlencoded`。
       - Form Data：返回基于 post 方法来传递数据的格式，具体的是以一个 boundary =${boundary}来进行分割。
       - binary：返回二进制格式。
    - **Cookie**: 填写需要用到的 cookies 参数。
    - **返回结果执行**：输入对返回的结果进行处理的 JS 代码。
    - **参数**：填写需要调用的参数的名称和值。

    ![参数信息](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/RestfulAPI20210325.png)

### 添加 RESTfulAPI 模板数据源

1. 在数据模型页面，单击“+”图标，选择“RESTfulAPI 模板”。
2. 在页面右侧选项页中，可对RESTfulAPI的配置信息、权限管理进行相应地操作。
    - 操作：下拉选择需要执行的方法。
    - 参数：输入在 RESTfulAPI 模板中定义的参数对应的值。

## 添加文件类数据源

### 添加文件

1. 在数据模型页面，单击“+”图标，选择“文件”，可自定义文件名称。
2. 在页面右侧选项页中，可对文件的配置信息、权限管理进行相应地操作。
3. 在“配置信息”中，针对已添加的文件类连接，可对其进行如下操作：

    - 浏览目录
    - 上传文件
    - 获取下载 url
    - 文件分段上传后合并操作
    - 删除文件
    - 删除目录

### 添加 Excel

1. 在数据模型页面，单击“+”图标，选择“Excel”，可自定义Excel文件名称。
2. 在页面右侧选项页中，可对文件的配置信息、权限管理进行相应地操作。
3. 在“配置信息”中，各参数说明如下：

    - **文件路径**：下拉选择该资源下的已有的 Excel 文件，即，“控制台 > 数据中心 > 文件服务”中已上传的 Excel 文件。
    - **表密码**：Excel 工作簿的保护密码。
    - **方法**：下拉选择需要对工作表进行的操作。

    ![Excel 数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/exceldatasource20210730.png)
