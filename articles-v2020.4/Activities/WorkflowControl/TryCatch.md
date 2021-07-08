# 错误捕捉（Try Catch）

针对异常处理，能够捕获流程图或活动中的指定异常类型，并显示错误通知或继续执行。由三部分组成：

- **Try** ：组件执行过程中可能抛出的异常
- **Catches** ：抛出异常时的处理方案
    - **Exception**：捕捉的异常类型，可添加多个
- **Finally** ：在组件结束时执行

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择"是"时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择"否"时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

## 操作样例

1. 拖入**打开浏览器** 组件，输入网址“https://www.aliyun.com ”。

2. 设置变量list，变量类型为`List<String>`，默认值为`new List<String>{"最新活动","产品","解决方案"}`，如下图所示：

    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-1.png)

3. 拖入**循环操作（For Each）** 组件并设置循环体为变量list；拖入**错误捕获（Try Catch）** 组件：

    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-2.png)  

4. 双击展开错误捕获组件，拖入**点击**组件至tryCatch容器内，点击指定网页最上端的“最新活动”元素，并打开选择器将Sinfo值“最新活动”用变量代替“{item}”:
    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-3.png)

5. 点击“添加新捕获”选择System.Exception选项，拖入**写入日志** 组件并填写输出`exception.Message + "切换至初始页"`；拖入**当前页跳转** 组件并输入网址“https://www.aliyun.com”。

    >**说明：**
    >
    >try容器中点击过list中第一个元素后当前页面会跳转为其他页面，导致循环点击list的其他元素时失败，为此我们在catch中设置跳转为初始页面，以此来初始化页面从而可正常点击list中其他元素：

    ![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-4.png)

6. 运行流程查看结果：
![](https://docimages.blob.core.chinacloudapi.cn/images/Activities/tryCatch-5.png)