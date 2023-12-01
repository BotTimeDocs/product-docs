# 《RPA入门指南》【云扩科技】

<br>

## 一、指南目录：

#### 第一部分 ：“7”大RPA开发指南，带你上手企业级流程开发

*  [指南一、《自动化原理》](https://academy.encoo.com/zh-cn/wiki/DevGuide/AutomationPrinciples.md)
*   [指南二、《组件详解》](https://academy.encoo.com/zh-cn/wiki/DevGuide/ComponentDetails.md)
*   [指南三、《流程开发的主要步骤》](https://academy.encoo.com/zh-cn/wiki/DevGuide/ComponentDetails.md)
*   [指南四、《流程设计指南》](https://academy.encoo.com/zh-cn/wiki/DevGuide/ProcessDesign.md)
*   [指南五、《RPA流程开发最佳实践》——企业级流程(必读)★★★](https://academy.encoo.com/zh-cn/wiki/DevGuide/BestPractices.md)
*   [指南六、《高级开发技巧》](https://academy.encoo.com/zh-cn/wiki/DevGuide/AdvancedDevelopment.md)
*   [指南七、《Windows远程桌面专题(企业版)》](https://academy.encoo.com/zh-cn/wiki/DevGuide/RDP.md)

<br><br>

#### 第二部分 ：RPA运行与管理--控制台进阶

* [管理1、《流程运行概述》](https://academy.encoo.com/zh-cn/wiki/RunManager/ProcessRunOverview.md) 
* [管理2、《控制台入门》](https://academy.encoo.com/zh-cn/wiki/RunManager/ConsoleQuickStart.md) 
* [管理3、《流程运行管理》](https://academy.encoo.com/zh-cn/wiki/RunManager/ProcessRunManager.md) 
* [管理4、《权限与安全》](https://academy.encoo.com/zh-cn/wiki/RunManager/PermissionsAndSecurity.md) 
* [管理5、《企业级运维》](https://academy.encoo.com/zh-cn/wiki/RunManager/EnterpriseOM.md) 
 
 
<br><br>
 

#### 第三部分 COE介绍

[RPA在企业内部落地最佳的推动方式是建立COE卓越中心。](https://academy.encoo.com/zh-cn/wiki/COE/coe.md)

<br><br>

#### 附： 云扩社区--免费官方技术支持&RPA学习交流

<img width = '400'  src ="https://doria-encooacademyimages.oss-cn-shanghai.aliyuncs.com/2022/12/21/16716261706592.jpg"/>

<font color = 5a6877 size=2 >


[说明] 
* 官方支持时间：工作日 10:00-19:00
* 技术支持老师：云简、云智、云能、云易
* 温馨提示：若同时间问题排队、请稍作等待
 </font>

<br><br><br><br>

## 二、正文<内容导读>

#### 第一部分 ：“7”大RPA开发指南，带你上手企业级流程开发

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-pwyt{color:#808080;text-align:left;vertical-align:middle}
.tg .tg-uzvj{border-color:inherit;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 636px">
<colgroup>
<col style="width: 249px">
<col style="width: 387px">
</colgroup>
<thead>
  <tr>
    <th class="tg-uzvj" colspan="2">指南一、《自动化原理》</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-uzvj">主要内容</td>
    <td class="tg-uzvj">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-lboi">1.1 什么是自动化， 为什么要自动化?</td>
    <td class="tg-lboi"></td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="4">1.2 自动化的底层__原理解释</td>
    <td class="tg-cly1">元素详解__桌面元素&amp;网页元素分别是什么？</td>
  </tr>
  <tr>
    <td class="tg-cly1">选择器：描述符(cv组件)、元素选择的基本原理、通配符，变量和XPath</td>
  </tr>
  <tr>
    <td class="tg-cly1">执行元素动作：点击(鼠标键盘模拟或设置控件)、输入文本(清空文本选项)</td>
  </tr>
  <tr>
    <td class="tg-cly1">超时与匹配超时：超时时间= 匹配元素的时间 + (匹配到元素后)等待元素消失的时间</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="5">1.3 自动化驱：扩展/插件</td>
    <td class="tg-cly1">WEB扩展：Chrome、Firefox、Microsoft Edge、360安全浏览器</td>
  </tr>
  <tr>
    <td class="tg-cly1">远程自动化扩展：Citrix、Windows远程桌面(RDP)——注意此功能插件仅支持企业版</td>
  </tr>
  <tr>
    <td class="tg-cly1">数据库扩展：DB2</td>
  </tr>
  <tr>
    <td class="tg-cly1">桌面自动化扩展：java扩展</td>
  </tr>
  <tr>
    <td class="tg-cly1">系统扩展：Windows屏幕解锁</td>
  </tr>
  <tr>
    <td class="tg-cly1">1.4 自动化环境</td>
    <td class="tg-cly1">独立桌面 、Session保持、锁屏运行</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在说明RPA自动化的概念解释，<br>重点在后续实际RPA流程开发过程中了解掌握。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-wa1i" colspan="2">指南二、《组件详解》</td>
  </tr>
  <tr>
    <td class="tg-nrix">主要内容</td>
    <td class="tg-nrix">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">2.1 什么是组件？</td>
    <td class="tg-cly1">组件的组成部分：组件名称、组件面板、弹窗、属性栏</td>
  </tr>
  <tr>
    <td class="tg-cly1"></td>
    <td class="tg-cly1">组件类型：<br>（1）内置组件 ：内置在编辑器 组件库 中，直接拖拽至流程设计面板即可使用；<br>（2）市场组件：从 组件市场下载 后即可使用；<br>（3）团队市场组件 ： 云扩自带的云空间，供企业团队内部自研业务组件。</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="2">2.2 如何找到组件</td>
    <td class="tg-cly1">组件类别：<br>（1）页面动作、鼠标/键盘<br>（2）浏览器、表格/Excel/WPS、邮件、PDF、文件/文件夹<br>（3）判断/循环、应用程序、操作系统、流程控制<br>（4）AI、开发服务、代码编程、数据处理、触发器、数据库操作<br>（5）SAP、高级自动化、手机自动化</td>
  </tr>
  <tr>
    <td class="tg-cly1">容器类组件<br>（1）打开/新建Excel<br>（2）打开浏览器<br>（3）连接数据库<br>（4）打开应用程序<br>（5）Python环境<br>（6）连接设备（手机）</td>
  </tr>
  <tr>
    <td class="tg-cly1">2.3 如何自研组件？</td>
    <td class="tg-cly1">两种方式让开发者可以根据实际需要自定义组件。<br><br>（1）在编辑器中使用组件项目自定义: 无代码的方式在编辑器中创建组件项目自定义组件。<br>（2）在Visual Studio中编程实现: 如果你是一名.NET开发者，可以选择使用此方式在Visual Studio中编码开发组件。</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在带大家了解云扩编辑器流程编辑中，会使用到的组件概念、不同组件类型及使用用途。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-wa1i" colspan="2">指南三、《流程开发的主要步骤》</td>
  </tr>
  <tr>
    <td class="tg-nrix">主要内容</td>
    <td class="tg-nrix">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2" rowspan="9"><img src="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/%E6%8C%87%E5%8D%97%E4%B8%89pic.png" width="620" height="150"></td>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在带大家了解云扩RPA 流程开发全流程，包括从设计、开发、测试、试运行、部署五个阶段到项目验收之后运维的长期过程。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">指南四、《流程设计指南》</td>
  </tr>
  <tr>
    <td class="tg-nrix">主要内容</td>
    <td class="tg-nrix">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="3">4.1 序列、流程图、状态机区别</td>
    <td class="tg-cly1">序列：没有箭头指向，流程自上而下运行，业务逻辑简单明了，所以通常用来分组简单的业务流程；</td>
  </tr>
  <tr>
    <td class="tg-cly1">流程图：实现相对复杂逻辑的业务流程，组件之间用连线连接，同一个组件在对应的逻辑条件下可执行多次；</td>
  </tr>
  <tr>
    <td class="tg-cly1">状态机：当打开系统后如果有多种状态存在，以登录场景距离有以下集中不同状态，则使用状态机(登录状态 / 输入用户名密码并点击登录后的角色选择状态/页面 / 未登录状态)。</td>
  </tr>
  <tr>
    <td class="tg-cly1">4.2 流程模板</td>
    <td class="tg-cly1">基本模块：创建日志、环境初始化、数据初始化、主业务处理及结束处理</td>
  </tr>
  <tr>
    <td class="tg-cly1">4.3 输入/输出 &amp; 输入/输出加密</td>
    <td class="tg-cly1">（1）输入 ：一个业务流程得到预期结果的“前提条件”；<br>（2）输出：有输入的前提下，经过一系列业务上的逻辑判断等操作后得出的“预期结果”。<br>（3）输入/输出加密：输入输出中有些数据是敏感的，需要进行加密方式处理，比如最常见的账号密码</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="4">4.4 日志</td>
    <td class="tg-cly1">日志类型介绍<br>（1）系统日志：机器人，编辑器产生的执行日志，技术支持时需要；<br>（2）业务日志：流程必要的信息作为日志来输出，用于业务核对或后续业务逻辑/流</td>
  </tr>
  <tr>
    <td class="tg-cly1">程运行情况检查，分别有三个级别选项：<br>（1）Debug——最详细<br>（2） Info —— Info 和 Error ，第二详细<br>（3）Error——最简单</td>
  </tr>
  <tr>
    <td class="tg-cly1">如何定义日志级别？</td>
  </tr>
  <tr>
    <td class="tg-cly1">日志输出位置：编辑器日志、机器人日志、控制台日志</td>
  </tr>
  <tr>
    <td class="tg-cly1">4.5 通知</td>
    <td class="tg-cly1">业务通知，一般情况下流程运行成功、失败、中间需要人工介入等情况，建议进行通知。<br><br>通知方式有：<br>（1）短信<br>（2）邮件<br>（3）Dingding<br>（4）企微</td>
  </tr>
  <tr>
    <td class="tg-cly1">4.6 错误处理(Trycatch)</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在带大家了解云扩RPA 流程开发设计开发过程中需要知道——流程结构要素：<br>序列、流程图、状态机、输入/输出、日志、错误捕获等。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">指南五、《RPA流程开发最佳实践》——企业级流程(必读) ★★★★★</td>
  </tr>
  <tr>
    <td class="tg-wa1i">主要内容</td>
    <td class="tg-wa1i">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">5.1 代码管理</td>
    <td class="tg-cly1">（暂略）</td>
  </tr>
  <tr>
    <td class="tg-cly1">5.2 开发协作与共享</td>
    <td class="tg-cly1">（暂略）</td>
  </tr>
  <tr>
    <td class="tg-cly1">5.3 安全</td>
    <td class="tg-cly1">（暂略）</td>
  </tr>
  <tr>
    <td class="tg-cly1">5.4 稳定性</td>
    <td class="tg-cly1">（暂略）</td>
  </tr>
  <tr>
    <td class="tg-cly1">5.6 多流程协作</td>
    <td class="tg-cly1">（暂略）</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>开发一个企业级流程必须考虑的几个流程开发要素，及开发流程管理中需要提前预知的几个方面。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2"> 指南六、《高级开发技巧》</td>
  </tr>
  <tr>
    <td class="tg-nrix">主要内容</td>
    <td class="tg-nrix">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">6.1 高级元素选择技巧——XPath介绍</td>
    <td class="tg-cly1">（1）如何在编辑器中使用XPath定位网页元素<br>（2）如何在XPath中使用变量<br>（3）如何直接从网页获取XPath<br>（4）XPath的语法<br>（5）IFrame选择器使用技巧</td>
  </tr>
  <tr>
    <td class="tg-cly1">6.2 云扩浏览器</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-cly1">6.3 编写代码：</td>
    <td class="tg-cly1">C#代码、Python代码、Powershell</td>
  </tr>
  <tr>
    <td class="tg-cly1">6.4 管理外部代码：</td>
    <td class="tg-cly1">Nuget代码市场、私有代码市场、外部代码的Package更新</td>
  </tr>
  <tr>
    <td class="tg-cly1">6.5 Excel高级技巧</td>
    <td class="tg-cly1">执行宏、自动填充、设置单元格格式、复制粘贴、分列</td>
  </tr>
  <tr>
    <td class="tg-cly1">6.6 网页操作高级技巧</td>
    <td class="tg-cly1">（1）如何获取页面元素的特定属性<br>（2）如何批量获取元素属性<br>（3）如何滚动页面<br>（4）如何操作日期类元素<br>（5）如何判断网页是否打开<br>（6）如何获取下拉框中的选项的内容<br>（7）如何使用浏览器上“右键”菜单项</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="3">6.7 桌面端软件精准定位技巧</td>
    <td class="tg-cly1">如何挑选最适合的录制技术，如何切换录制技术？</td>
  </tr>
  <tr>
    <td class="tg-cly1">怎样让组件精准定位元素？</td>
  </tr>
  <tr>
    <td class="tg-cly1">特殊自动化场景处理</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在介绍高级自动化场景，实际业务开发过程必然会遇到的复杂自动化场景，及对应需要使用到的RPA自动化技巧。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">指南七、《Windows远程桌面专题(企业版)》</td>
  </tr>
  <tr>
    <td class="tg-nrix">主要内容</td>
    <td class="tg-nrix">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">7.1 什么是远程桌面扩展(定义)？</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-cly1">7.2 远程情况下，几个不同情况的流程开发自动化场景</td>
    <td class="tg-cly1">（1）准备工作<br>（2）Java自动化<br>（3）网页自动化<br>（4）编辑流程<br>（5）录制<br>（6）卸载远程桌面扩展</td>
  </tr>
  <tr>
    <td class="tg-cly1">7.3 远程常见问题</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在介绍企业开发过程中，经常遇见的远程场景开发、交付、运维过程的远程自动化配置及使用办法。</td>
  </tr>
</tbody>
</table>

<br><br><br>

#### 第二部分 ：RPA运行与管理--控制台进阶

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-pwyt{color:#808080;text-align:left;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 631px">
<colgroup>
<col style="width: 130px">
<col style="width: 501px">
</colgroup>
<thead>
  <tr>
    <th class="tg-nrix" colspan="2">管理1、《流程运行概述》</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-wa1i">主要内容</td>
    <td class="tg-wa1i">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">1.1 机器人</td>
    <td class="tg-cly1">（1）什么是机器人?<br>（2）机器人结构;<br>（3）机器人执行多个任务的方式是什么?<br>（4）机器人部署类型</td>
  </tr>
  <tr>
    <td class="tg-cly1">1.2 流程运行环境</td>
    <td class="tg-cly1">（1）离线<br>（2）独立桌面<br>（3）锁屏/解锁<br>（4）静默运行</td>
  </tr>
  <tr>
    <td class="tg-cly1">1.3 流程运行监控 - 机器人</td>
    <td class="tg-cly1">日志有：实时日志、历史日志；<br><br>日志从类型看，可分为：<br>（1）系统日志<br>（2）业务日志<br><br>日志从级别看，可分为：<br>（1）Debug<br>（2）Info<br>（3）Error</td>
  </tr>
  <tr>
    <td class="tg-cly1">1.4 其他流程监控形式：录屏、截图</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在介绍流程运行环节，需要知道的基础流程运行概念：机器人、运行环节环境；具体的监控形式：日志、录屏、截屏</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">管理2、《控制台入门》</td>
  </tr>
  <tr>
    <td class="tg-wa1i">主要内容</td>
    <td class="tg-wa1i">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">2.1 什么是控制台？</td>
    <td class="tg-cly1">（1）流程库<br>（2）机器人管理<br>（3）流程调度<br>（4）流程运行监控和报警<br>（5）开发服务<br>（6）文件<br>（7）资产<br>（8）连接器：主要用以实现数据互联互通，如：MySql、SqlServer、AzureBlob等。<br>（9）组织与权限</td>
  </tr>
  <tr>
    <td class="tg-cly1">2.2 控制台的组成：</td>
    <td class="tg-cly1">（1）离线<br>（2）独立桌面<br>（3）锁屏/解锁<br>（4）静默运行</td>
  </tr>
  <tr>
    <td class="tg-cly1">2.3 私有化控制台</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在介绍云扩控制台的基本构成、对应模块支持的功能。以及何种情况下，建议私有化部署控制台。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">管理3、《流程运行管理》</td>
  </tr>
  <tr>
    <td class="tg-wa1i">主要内容</td>
    <td class="tg-wa1i">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">3.1 触发器</td>
    <td class="tg-cly1">即自动化流程运行的触发条件，控制台支持：<br>（1）人工方式(手动)触发执行<br>（2）定时任务触发执行<br>（3）监听数据队列消息触发;</td>
  </tr>
  <tr>
    <td class="tg-cly1">3.2 执行资源调度（运行环境）</td>
    <td class="tg-cly1">（1）指定到多个机器人<br>（2）指定到机器人组</td>
  </tr>
  <tr>
    <td class="tg-cly1">3.3 流程运行权限</td>
    <td class="tg-cly1"></td>
  </tr>
  <tr>
    <td class="tg-cly1">3.4 运行监控入门</td>
    <td class="tg-cly1">（1）机器人与计算机<br>（2）监控计算机性能</td>
  </tr>
  <tr>
    <td class="tg-cly1">3.5 流程监控</td>
    <td class="tg-cly1">（1）关于总体监控，详见总体监控产品说明<br>（2）关于机器人监控，详见机器人监控产品说明<br>（3）关于机器人组监控，详见机器人组监控产品说明<br>（4）关于机器人运行统计表，详见机器人运行统计表产品说明<br>（5）关于用户流程统计表，详见用户流程统计表产品说明</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>重在介绍云扩控制台流程调度三个概念组成： 1. 触发器；2.自动化流程；3. 执行资源。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">管理4、《权限与安全》</td>
  </tr>
  <tr>
    <td class="tg-wa1i">主要内容</td>
    <td class="tg-wa1i">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1">4.1 许可证主要分为：</td>
    <td class="tg-cly1">（1）编辑器/机器人许可(固定许可VS浮动许可）<br>（2）Vicode应用许可<br>（3）文档理解模板许可<br>（4）个人版许可证</td>
  </tr>
  <tr>
    <td class="tg-cly1">4.2 组织架构管理</td>
    <td class="tg-cly1">（1）3个概念：租户、部门、用户<br>（2）如何邀请与激活？</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : 主要介绍许可证在控制台的<br>（1）几个不同存在形式，及对应的产品许可类型；<br>（2）对应的组织架构管理概念及具体的权限邀请激活方式。</td>
  </tr>
  <tr>
    <td class="tg-cly1" colspan="2"></td>
  </tr>
  <tr>
    <td class="tg-nrix" colspan="2">管理5、《企业级运维》</td>
  </tr>
  <tr>
    <td class="tg-nrix">主要内容</td>
    <td class="tg-nrix">涉及知识点</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="3">5.1 私有化部署指南</td>
    <td class="tg-cly1">为什么需要私有化部署？私有化环境需求</td>
  </tr>
  <tr>
    <td class="tg-cly1">高可用指南</td>
  </tr>
  <tr>
    <td class="tg-cly1">企业私有市场</td>
  </tr>
  <tr>
    <td class="tg-pwyt" colspan="2">本章主要 : <br>主要介绍企业级运维——私有化部署相关模块的部署环境要求及具体部署办法，及企业私有市场的运用与管理。</td>
  </tr>
</tbody>
</table>

<br><br><br>

#### 第三部分  COE-RPA卓越中心介绍
[RPA在企业内部落地最佳的推动方式是建立COE卓越中心。](https://academy.encoo.com/zh-cn/wiki/COE/coe.md)卓越中心COE（Center of Excellence）是一个跨职能的虚拟组织结构，能够促进协作支持企业内部的RPA专业部署和落地实现；COE将RPA深入有效地嵌入组织，并在未来部署中重新分配累积的知识和资源。
