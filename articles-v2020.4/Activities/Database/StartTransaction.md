# 执行事务（Transaction）

需在&quot;连接数据库&quot;组件内使用，无需二次配置连接。其内可放置其他数据库组件来实现执行事务功能，这些操作要么全部执行要么全部不执行。
注意：如果是对表结构删除或更新，目前除MS SQL外，其他数据库则无法实现回滚，依赖于各数据库本身功能。

## 属性
基本
- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件


## 操作样例
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
