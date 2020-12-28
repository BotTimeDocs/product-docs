# 连接数据库

连接到指定数据库.点击 *配置向导* 后可进行连接测试。组件执行结束后自动断开连接，所有数据库相关操作均需放置在此组件内且无需二次配置连接。

> 如果您需要连接 DB2 数据库，请确保您已安装 *Microsoft Visual C++ 2005 RunTime Pack*。如果未安装，您可以下载 [RunTimePack.zip](https://docimages.blob.core.chinacloudapi.cn/images/Studio/DataBase/RuntimePack.zip) 并安装。

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


### 输入

- **ConncetionString** ：用于与数据库建立连接。仅支持字符串变量和字符串。例如：MySQL连接字符串"Server=服务器地址;Database=DB名称;Port=端口号;Uid=uid;Pwd=password;"
- **ProviderName** ：连接的数据库类型。现支持五种：SQL Server, MySql, Oracle, DB2, Teradata


## 操作样例
1. 拖入**连接数据库**组件，选择当前所需访问数据库类型，再配置连接数据库字符串:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db1.png)

2. 双击**连接数据库**组件，点击"配置向导"按钮，如果已配置数据库字符串信息以及选择了目标数据库类型，则点击"测试连接"按钮，测试成功会提示绿色对勾，反之则失败，需要更新连接数据库字符串内容，确保无误之后重新测试连接，点击"确认"退出配置界面:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db2.png)

3. 拖入**查询**组件，配置sql语句查询语句，并输出到变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db3.png)
4. 拖入**预览数据表**组件，输入变量填写查询组件中定义的输出变量:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db4.png)
5. 点击流程运行，观察结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db5.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db6.png)
