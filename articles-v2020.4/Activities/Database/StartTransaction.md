# 执行事务（Transaction）

## 视频示例

## 概述

需在&quot;连接数据库&quot;组件内使用，无需二次配置连接。其内可放置其他数据库组件来实现执行事务功能，这些操作要么全部执行要么全部不执行。
注意：如果是对表结构删除或更新，目前除MS SQL外，其他数据库则无法实现回滚，依赖于各数据库本身功能。

## 属性

### 基本

参见 [通用配置项](../Appendix/CommonConfigurationItems.md)。

## 使用示例

1. 拖入**连接数据库**组件，选择当前所需访问数据库类型，再配置连接数据库字符串:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db1.png)

2. 双击**连接数据库**组件，点击"配置向导"按钮，如果已配置数据库字符串信息以及选择了目标数据库类型，则点击"测试连接"按钮，测试成功会提示绿色对勾，反之则失败，需要更新连接数据库字符串内容，确保无误之后重新测试连接，点击"确认"退出配置界面:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db2.png)

3. 拖入**执行事务**组件:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db10.png)

4. 拖入**执行语句**组件，配置sql语句:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db11.png)

5. 点击流程运行，并观察结果:
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db12.png)
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/connect_db9.png)
