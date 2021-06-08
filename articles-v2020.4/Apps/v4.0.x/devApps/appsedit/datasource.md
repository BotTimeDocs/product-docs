# 数据源管理

数据源管理页面用于管理并配置应用内的数据源的使用权限。目前支持 SQL、RESTfulAPI、RESTfulAPI 模板、数据表四种类型的数据源。

## 添加数据源入口

- **方式一**：在“应用开发”的编辑页面中，单击“数据源”图标，即可进入数据源管理页面，如下图所示。

    ![数据源入口 1](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/datasource120210326.png)

- **方式二**：在“应用开发”的编辑页面中，单击“大纲”图标后，即可进入“数据源”选项页面，如下图所示。
  
   ![数据源入口 2](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/datasource220210326.png)

## 添加数据源

单击左侧页面右上角的“+”图标，可新建一个 SQL、RESTfulAPI、RESTfulAPI 模板、数据表数据源。

### 添加 SQL 数据源

添加 SQL 数据源，即，执行 SQL 语句。

> **说明：**
>
> 支持 Mysql、Oracle 数据库。

1. 在数据源页面，单击“新增”图标，选择“SQL”，可自定义 SQL 数据源名称。
2. 在页面右侧弹框中，输入各参数。

    - **资源**：下拉选择在 **云扩 RPA 控制台 > 数据中心 > 连接管理** 中已创建的数据连接。也可在下拉框中单击“**+新建连接**”，根据向导进行新建数据库连接。
    - **SQL**：输入需要对已选择的资源进行执行的 SQL 语句。
    - **参数**：（可选）根据需要，填写对 SQL 语句中需要用到的参数进行自定义。

    ![SQL 组件参数](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/sqlcenter20210325.png)

3. 编写完成的 SQL 语句，单击“运行”按钮，可测试查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/sql20210325.png)

4. 单击“保存”按钮，编写完成的代码将保存至数据源管理页面。

### 添加 RESTfulAPI 数据源

添加 RESTfulAPI 数据源，即，调用 RestfulAPI 接口对资源进行 CRUD 操作。

1. 在数据源页面，单击“新增”图标，选择“RestfulAPI”，可自定义 RestfulApI 数据源名称。
2. 在页面右侧弹框中，输入各参数。

    - **资源**：下拉选择在 **云扩 RPA 控制台 > 数据中心 > 连接管理** 中已创建的 RestfulApi 连接。也可在下拉框中单击“**+新建连接**”，根据向导进行新建 RestfulApi 连接。
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

3. 单击“测试”按钮，测试接口返回情况。
4. 单击“保存”按钮，编写完成的信息将保存至数据源管理页面。

### 添加 RESTfulAPI 模板数据源

1. 在数据源页面，单击“新增”图标，选择“RestfulAPI 模板”，可自定义 RestfulApI 模板数据源名称。
2. 在页面右侧弹框中，操作各参数。

    - 资源：下拉选择在 **云扩 RPA 控制台 > 数据中心 > 连接管理** 中已创建的自定义 RESTfulAPI 模板数据连接。
    - 操作：下拉选择需要执行的方法。
    - 参数：输入在 RESTfulAPI 模板中定义的参数对应的值。

    ![新建 RESTfulAPI 模板数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/createrestfulapitemplate20210608.png)

3. 单击“测试”按钮，测试接口返回情况。

   ![测试结果](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/restapiresult20210608.png)

4. 单击“保存”按钮，编写完成的信息将保存至数据源管理页面。

### 添加数据表数据源

1. 在数据源页面，单击“新增”图标，选择“数据表”，可自定义数据表数据源名称。
2. 在页面右侧弹框中，输入各参数。

    - **资源**：选择创建数据表时自定义的数据连接器名称。
    - **操作**：下拉选择操作类型，支持新增数据、更新数据、删除数据、查找数据四个操作。
    - **指定行**：仅当更新数据、删除数据和查找数据时，出现“指定行”字段，表示指定为第几行的数据进行操作。
    - **字段赋值**：仅当新增数据、更新数据时，出现“字段赋值”字段，表示为指定的字段进行赋值。

    ![数据表数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/createdatatablesave20210511.png)

3. 单击“保存”按钮，保存已配置的信息。
4. 单击“测试”按钮，可在下方查看运行结果。

    ![运行结果](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/datatbletestresult20210512.png)

## 编辑数据源

在已添加的数据源列表中，选择需要修改的数据源列表，单击右侧页面的“编辑”按钮，可修改数据源。

![编辑数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/editdatasource20210326.png)

## 删除数据源

单击左侧页面右上角的“删除”图标，可删除已创建且选中的数据源。

![删除数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/deletedatasource20210326.png)

## 搜索数据源

在左侧页面上方的搜索框中输入需要搜索的数据源名称，可搜索数据源列表。

![搜索数据源](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/searchcode20210326.png)

## 查看并配置数据源权限

选择任一数据源列表，在右侧“权限信息”选项卡中，可查看并配置该数据源的权限信息。

![查看并配置数据源权限](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/grant20210326.png)
