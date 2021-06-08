# 连接管理

连接管理主要用户创建并管理各类数据连接器，建立与各类外部数据之间的连接，便于后续在 ViCode 中进行各类数据操作。

## 前提条件

以管理员身份登录登录企业版控制台。

## 新建数据库类连接

### 新建 MySql 数据库连接

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“MySql”，单击“下一步”按钮。

   ![新建 Mysql 数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createconnector20210329.png)

3. 在进入的“配置连接”弹框中，配置 Mysql 连接。

    - **连接名称**：自定义新建的 mysql 连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接方式**：可选择“通过配置连接”或“通过连接字符串连接”。
    - **使用 SSL 连接**：是否启用 SSL 连接。

    a. 通过配置连接

    ![通过配置连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/connectionbysetting20210329.png)

    b. 通过连接字符串连接

    ![配置 mysql 连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingmysqlconnect20210329.png)

4. （可选）单击“测试”按钮，可测试数据连接是否成功。
5. 单击“新建”按钮，完成 Mysql 的数据连接。

### 新建托管数据库

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“托管数据库”，单击“下一步”按钮。

   ![新建托管数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/trustdataconnect20210425.png)

3. 在进入的“配置连接”弹框中，配置托管数据库连接。

    - **连接名称**：自定义新建的托管数据库连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。

    ![配置数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/settingtrustconnect20210425.png)

4. 单击“新建”按钮，完成托管数据库连接。

### 新建 DB2 数据库

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“DB2”，单击“下一步”按钮。

   ![新建 DB2 数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/db2connect20210604.png)

3. 在进入的“配置连接”弹框中，配置 DB2 数据库连接。

    - **连接名称**：自定义新建的托管数据库连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接方式**：选择“通过配置连接”或“通过 Connection String 连接”连接方式。

    ![配置数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingdb2connection20210604.png)

4. 单击“新建”按钮，完成 DB2 数据库连接。

### 新建 PostgreSQL 数据库

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“PostgreSQL”，单击“下一步”按钮。

   ![新建 Postgre SQL 数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/selectpostgresql20210604.png)

3. 在进入的“配置连接”弹框中，配置 PostgreSQL 数据库连接。

    - **连接名称**：自定义新建的托管数据库连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接方式**：选择“通过配置连接”或“通过 Connection String 连接”连接方式。

    ![配置数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/postgresqlconnection20210604.png)

4. 单击“新建”按钮，完成 PostgreSQL 数据库连接。

### 新建 SQL Server 数据库

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“SQL Server”，单击“下一步”按钮。

   ![新建 SQL Server 数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/sqlserverconnection20210604.png)

3. 在进入的“配置连接”弹框中，配置 SQL Server 数据库连接。

    - **连接名称**：自定义新建的托管数据库连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接方式**：选择“通过配置连接”或“通过 Connection String 连接”连接方式。

    ![配置数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingsqlserver20210604.png)

4. 单击“新建”按钮，完成 SQL Server 数据库连接。

### 新建 Oracle 数据库

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“Oracle”，单击“下一步”按钮。

   ![新建 Oracle 数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/oracleconnection20210604.png)

3. 在进入的“配置连接”弹框中，配置 Oracle 数据库连接。

    - **连接名称**：自定义新建的托管数据库连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接方式**：选择“通过配置连接”或“通过 Connection String 连接”连接方式。

    ![配置数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingoracle20210604.png)

4. 单击“新建”按钮，完成 Oracle 数据库连接。

## 新建 API 类连接

### 新建 Restful API 连接

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“Restful API”，单击“下一步”按钮。

    ![新建 Restful API 数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createrestfulapi20210329.png)

3. 在进入的“配置连接”弹框中，配置 Restful API 连接。

    - **连接名称**：自定义新建的 Restful API 连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **基础 URL 地址**：填写基础 URL 定位地址。
    - **Headers**：填写头文件的 key 和 value 的值。
    - **Parameters**：填写参数的 key 和 value 的值。

    ![配置 Restful API ](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingrestfulapi20210329.png)

4. 单击“新建”按钮，完成 Restful API 数据连接。

## 新建文件类连接

### 新建 MiniO 文件连接

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“MiniO”，单击“下一步”按钮。

    ![新建 Minio 文件连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createminio20210413.png)

3. 在进入的“配置连接”弹框中，配置 MiniO 连接。

    - **连接名称**：自定义新建的 MiniO 连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **MiniO 服务地址**：填写 Minio 对象存储服务的地址。
    - **Access key**：填写 Minio 对象存储服务的 Access key。
    - **Secret Key**：填写 Minio 对象存储服务的 Secret Key。
    - **文件存储路径**：非必填，填写需要在 Minio 对象存储服务中创建的文件夹名称。

    ![配置 Minio 文件连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingminio20210413.png)

4. 单击“新建”按钮，完成 Minio 文件连接。

### 新建 AzureBlob 文件连接

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“AzureBlob”，单击“下一步”按钮。

    ![新建 AzureBlob 文件连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createazureblob20210413.png)

3. 在进入的“配置连接”弹框中，配置 AzureBlob 连接。

    - **连接名称**：自定义新建的 AzureBlob 连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接字符串**：填写 AzureBlob 对象存储服务的连接字符串。
    - **文件存储路径**：非必填，填写需要在 AzureBlob 对象存储服务中创建的文件夹名称。

    ![配置 AzureBlob 文件连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingazureblob20210413.png)

4. 单击“新建”按钮，完成 AzureBlob 文件连接。

### 新建 EncooStorage 文件连接

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“EncooStorage”，单击“下一步”按钮。

    ![新建 EncooStorage 文件连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createencoostorage20210413.png)

3. 在进入的“配置连接”弹框中，配置 EncooStorage 连接。

    - **连接名称**：自定义新建的 EncooStorage 连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **文件存储路径**：非必填，填写需要在 EncooStorage 对象存储服务中创建的文件夹名称，如果不填写，则自动在 EncooStorage 的根目录下创建文件夹。

    ![配置 EncooStorage 文件连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingencoostorage20210413.png)

4. 单击“新建”按钮，完成 EncooStorage 文件连接。

## 新建 RESTfulTemplate

### 1. 配置 API 类连接模板

通过导入 Postman Collection 模板文件自定义 API 类连接模板。

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“API 类连接模板配置”链接。
2. 在弹出的“新建 API 类连接模板”弹框中，选择“+”图标。

   ![选择新建图标](https://docimages.blob.core.chinacloudapi.cn/images/Console/newapi20210607.png)

3. 根据向导进行创建模板。

    - 模板名称：自定义模板名称。
    - 备注：对自定义模板名称的描述。
    - 模板文件：从本地选择已通过 Postman 工具生成的模板 json 文件，如，[示例](https://docimages.blob.core.chinacloudapi.cn/images/Console/GitHub_Demo.json)。
    - 模板图标：从本地选择一个图标作为模板图标。
    - 环境变量文件：从本地选择已通过 Postman 工具生成的环境变量 json 文件，如，[示例](https://docimages.blob.core.chinacloudapi.cn/images/Console/postman_environment.json)。

    ![创建模板](https://docimages.blob.core.chinacloudapi.cn/images/Console/createtemplate20210607.png)

4. 单击“下一步”按钮，进入“连接参数”步骤，根据情况配置参数信息。

    > **说明：**
    >
    > 此参数为在环境变量 json 文件中预先配置的。

    ![连接参数](https://docimages.blob.core.chinacloudapi.cn/images/Console/connectionargument20210607.png)

5. 单击“下一步”按钮，进入“方法确认”步骤，根据情况确认相关信息。

    ![方法确认](https://docimages.blob.core.chinacloudapi.cn/images/Console/confirm20210607.png)

6. 单击“确定”按钮，完成模板的创建。

    ![模板创建完成](https://docimages.blob.core.chinacloudapi.cn/images/Console/templatedone20210607.png)

### 2. 使用模板新建 RESTful 连接

1. 在“**云扩 RPA 控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择已创建的 RESTfulTemplate“test_demo”，单击“下一步”按钮。

    ![新建 RESTfulTemplate 连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/test_demo20210607.png)

3. 在进入的“配置连接”弹框中，配置 自定义的 RESTfulTemplate "test_demo" 连接。

    - **连接名称**：自定义新建的 RESTful 连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **参数名称**：填写自定义的参数名称对应的值。

    ![配置 RESTful 连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingconnect20210607.png)

4. 单击“新建”按钮，完成 RESTful 连接。

## 后续操作

- **查看**：在“连接管理”页面，单击“操作”栏中的“查看”选项，可查看并修改所选择的数据连接的配置信息和数据权限。
- **测试**：在“连接管理”页面，单击“操作”栏中的“测试”选项，可测试当前数据连接是否连接成功。
- **删除**：在“连接管理”页面，单击“操作”栏中的“删除”选项，可删除当前选中的数据连接。
- **管理文件连接器中的文件**：如果需要管理已创建的文件连接器下的文件，可在“数据中心 > 文件服务”中，使用“新建根目录文件夹”功能进行绑定文件连接器，具体可参见 [管理文件服务](../../v4.0.x/datacentor/fileservice/managefileservice.md)。
