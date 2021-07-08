# 联结数据表

根据联结条件，将两个数据表联结到一起，并将结果存储到输出输出数据表变量。提供四种联结条件：全连接，内连接，左连接，右连接

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **联结配置** ：点击右侧的按钮，将弹出联结配置窗口。在此窗口可以进行联结条件的设置

### 输出

- **数据表** ：将联结两表后的结果保存到此变量

## 操作样例

1. 拖入**搭建数据表**组件至项目流程中：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable20201224.png)

2. 双击打开搭建数据表搭建器，编辑列信息和行值，创建一个类型为DataTable类型的变量用于存放输出数据表，例：table，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/BulidDataTable2020122402.png)

3. 再拖入一次**搭建数据表**组件按步骤2创建数据表table2，搭建的时候可以列名设置一列与表1一样的方便下面的联结操作，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable20201225.png)

4. 拖入**联结数据表**组件和**预览数据表**组件，双击打开联结数据表，设置联结配置，如下图所示：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable2020122502.png)

5. 点击运行，查看运行结果，检查预览出的数据表是否是两个表左连接的正确结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/JoinDataTable2020122503.png)
