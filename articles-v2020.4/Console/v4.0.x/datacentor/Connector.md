# 连接管理

连接管理主要用户创建并管理各类数据连接器，建立与各类外部数据之间的连接，便于后续在小程序中进行各类数据操作。

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
    - **连接方式**：可选择“通过配置连接”或“通过 Connection String 连接”。
    - **使用 SSL 连接**：是否启用 SSL 连接。

    a. 通过配置连接

    ![通过配置连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/connectionbysetting20210329.png)

    b. 通过 Connection String 连接

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

## 后续操作

- **查看**：在“连接管理”页面，单击“操作”栏中的“查看”选项，可查看并修改所选择的数据连接的配置信息和数据权限。
- **测试**：在“连接管理”页面，单击“操作”栏中的“测试”选项，可测试当前数据连接是否连接成功。
- **删除**：在“连接管理”页面，单击“操作”栏中的“删除”选项，可删除当前选中的数据连接。
- **管理文件连接器中的文件**：如果需要管理已创建的文件连接器下的文件，可在“数据中心 > 文件服务”中，使用“新建根目录文件夹”功能进行绑定文件连接器，具体可参见 [管理文件服务](../../v4.0.x/datacentor/fileservice/managefileservice.md)。