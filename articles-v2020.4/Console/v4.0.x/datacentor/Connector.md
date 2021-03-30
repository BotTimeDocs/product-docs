# 连接管理

连接管理主要用户创建并管理各类数据连接器，建立与各类外部数据之间的连接，便于后续在小程序中进行各类数据操作。

## 前提条件

以管理员身份登录登录企业版控制台。

## 新建 MySql 数据连接

1. 在“**云扩RPA控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“MySql”，单击“下一步”按钮。

   ![新建Mysql数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createconnector20210329.png)

3. 在进入的“配置连接”弹框中，配置Mysql连接。

    - **连接名称**：自定义新建的mysql连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **连接方式**：可选择“通过配置连接”或“通过Connection String连接”。
    - **使用SSL连接**：是否启用SSL连接。

    a. 通过配置连接

    ![通过配置连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/connectionbysetting20210329.png)
    
    b. 通过Connection String连接

    ![配置mysql连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingmysqlconnect20210329.png)

4. （可选）单击“测试”按钮，可测试数据连接是否成功。
5. 单击“新建”按钮，完成Mysql的数据连接。

## 新建 Restful API 数据连接

1. 在“**云扩RPA控制台 > 数据中心 > 连接管理**”页面中，单击页面右上角的“+新建”按钮。
2. 在弹出的“新建连接”对话框中，选择“Restful API”，单击“下一步”按钮。

    ![新建Restful API数据连接](https://docimages.blob.core.chinacloudapi.cn/images/Console/createrestfulapi20210329.png)

3. 在进入的“配置连接”弹框中，配置Restful API连接。

    - **连接名称**：自定义新建的Restful API连接名称。
    - **环境类型**：下拉选择生产环境或测试环境。
    - **基础URL地址**：填写基础URL定位地址。
    - **Headers**：填写头文件的key和value的值。
    - **Parameters**：填写参数的key和value的值。

    ![配置Manage DataBase](https://docimages.blob.core.chinacloudapi.cn/images/Console/settingrestfulapi20210329.png)

4. 单击“新建”按钮，完成Restful API数据连接。

## 后续操作

- **查看**：在“连接管理”页面，单击“操作”栏中的“查看”选项，可查看并修改所选择的数据连接的配置信息和数据权限。
- **测试**：在“连接管理”页面，单击“操作”栏中的“测试”选项，可测试当前数据连接是否连接成功。
- **删除**：在“连接管理”页面，单击“操作”栏中的“删除”选项，可删除当前选中的数据连接。