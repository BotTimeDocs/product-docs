# 管理任务记录

## 查看任务记录列表

进入“任务记录 " 页面，可以查看所有流程部署通过任何方式所触发的流程任务的执行状况。

![job](https://docimages.blob.core.chinacloudapi.cn/images/HAP/viewtaskrecord20211208.png)

+ **任务（job）**：被任务计划或手动执行方式创建出来需要完成的流程任务。
  
  任务状态说明如下：

  - 等待：任务在队列中排队，机器人当前正 **忙碌** 或 **无响应**，等待分配机器人执行该任务
  - 已分配：已经分配机器人执行该任务 (创建出 runinstance)
  - 运行中： 机器人正在执行该任务
  - 成功：任务执行成功
  - 失败：任务执行失败
  - 取消：该任务被取消

+ **执行实例（runinstance）**：流程任务会创建出具体的执行执行实例以完成任务，一个任务有可能创建多个执行实例。例如，一个任务被创建出来之后会生成具体的执行实例去完成该任务，若第一次执行失败之后且配置了失败重试机制，任务会自动再创建出一个执行实例进行失败重试。

  执行实例状态说明如下：

  - 创建：runinstance 已经创建出来
  - 运行: 该 runinstance 正在运行
  - 失败：该 runinstance 运行失败
  - 成功：该 runinstance 运行成功
  - 取消：该 runinstance 被取消

### 查看任务下的执行实例

单击某一任务下的“展开”图标，可展开对应的执行实例列表，默认展示 3 条，如果超过 3 条，点击“展开更多”按钮可以展开全部。主要包括具体的执行机器人、开始时间、结束时间、状态等。

![查看任务下的执行实例](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3joblist2.png)

### 查看实例的日志详情

你可以通过如下方式查看任务在机器人上的执行日志：

1. 在任务列表页面中点击任务下某一具体执行实例的“日志”按钮即可查看任务在该机器人上执行的具体日志。

    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow18.png)

2. 也可在“任务详情”页面中点击“查看日志”按钮查看任务在该机器人上执行的具体日志。

    > **说明：**
    >
    > 日志主要包含日志时间、日志类型、日志级别、日志内容、日志截图等内容。可以在左上角的“日志切换”中快速切换该任务在其他机器人上的执行日志。

    ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/viewlog20210413.png)

## 查看任务记录详情

单击某一任务后的“查看”按钮即可查看该任务的执行详情，任务详情主要包括执行基本信息、参数信息等内容。

  ![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow17.png)

## 调整任务优先级

调度队列中的任务将会按照任务优先级进行执行（0-5000）, 优先级越高则任务将会被优先执行。若您希望某一任务可以插队执行，则点击该任务的“调整优先级”按钮以调整优先级。

  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3editpriority1.png)

你可以输入对应的优先级数字，数字越大则任务会被越优先执行。

  ![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3editpriority2.png)

## 取消任务

在当前任务尚未执行完成时，若想取消某一任务，点击某一任务的 "取消" 按钮，即可取消当前任务。

![取消任务](https://docimages.blob.core.chinacloudapi.cn/images/Console/jobcancel20210317.png)

- 若该任务取消时属于未指派给机器人状态，则直接取消。
- 若该任务终止时已经指派给某一机器人正在执行，则向机器人发送指令进行取消，当前任务会执行失败。

## 批量操作

任务记录页面中的任务支持批量操作功能，勾选页面任务列表左侧的筛选框后，单击页面右上方的“批量操作”按钮，可进行批量调整优先级、批量执行、批量取消执行操作。

  ![批量操作](https://docimages.blob.core.chinacloudapi.cn/images/Console/batchoperate20210317.png)

## 搜索任务记录

在页面左上角搜索框中输入流程部署名称，可模糊搜索任务记录。也可根据指定时间或状态进行过滤任务记录列表信息。

