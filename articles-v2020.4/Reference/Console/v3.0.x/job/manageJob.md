# 查看任务记录

## 查看任务记录列表
进入“任务记录"页面则可以查看所有流程部署通过任何方式所触发的流程任务的执行状况。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3joblist1.png)

## 任务及执行实例说明

**任务（job）**：被任务计划或手动执行方式创建出来需要完成的流程任务。
**执行实例（runinstance）**：流程任务会创建出具体的执行执行实例以完成任务，一个任务有可能创建多个执行实例。
例如，一个任务被创建出来之后会生成具体的执行实例去完成该任务，若第一次执行失败之后且配置了失败重试机制，任务会自动再创建出一个执行实例进行失败重试。

## 状态说明
**任务（job）**：
- 等待：待分配机器人执行该任务
- 已分配：已经分配机器人执行该任务 (创建出runinstance)
- 运行中： 机器人正在执行该任务
- 成功：任务执行成功
- 失败：任务执行失败
- 取消：该任务被取消

**执行实例（runinstance）**：
- 创建：runinstance已经创建出来
- 运行: 该runinstance正在运行
- 失败：该runinstance运行失败
- 成功：该runinstance运行成功
- 取消：该runinstance被取消


## 任务（job）下执行实例（runinstance）查看

点击某一任务下的“展开”按钮，即可展开对应的执行实例列表，默认展示3条，如果超过3条点击“展开更多”按钮可以展开全部。主要包括具体的执行机器人、开始时间、结束时间、状态等。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3joblist2.png)

## 查看任务详情 
点击某一任务后的“查看”按钮即可查看该任务的执行详情，任务详情主要包括执行基本信息、参数信息等内容。
![process](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow17.png)

## 查看日志详情
你可以通过如下方式查看任务在机器人上的执行日志：
1）在任务列表页面中点击任务下某一具体执行实例的“日志”按钮即可查看任务在该机器人上执行的具体日志。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow18.png)
2）也可在“任务详情”页面中点击“查看日志”按钮查看任务在该机器人上执行的具体日志。

日志主要包含日志时间、日志类型、日志内容、日志截图等内容。可以在左上角的“日志切换选”中快速切换该任务在其他机器人上的执行日志。

![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/process/V3workflow19.png)
## 终止任务
在当前任务尚未执行完成时，若想终止某一任务，点击某一任务的"终止"按钮，即可终止当前任务”
1）若该任务终止时属于未指派给机器人状态，则直接终止。
2）若该任务终止时已经指派给某一机器人正在执行，则向机器人发送指令进行终止，当前任务会执行失败。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3stopjob1.png)

## 调整任务优先级
调度队列中的任务将会按照任务优先级进行执行（0-5000）,优先级越高则任务将会被优先执行。若您希望某一任务可以插队执行，则点击该任务的“调整优先级”按钮以调整优先级。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3editpriority1.png)
你可以输入对应的优先级数字，数字越大则任务会被越优先执行。
![job](https://docimages.blob.core.chinacloudapi.cn/images/Console/job/V3editpriority2.png)
