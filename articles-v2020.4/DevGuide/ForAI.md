# AI专题

## 一、RPA与AI的关系

从技术上看，AI是通过机器学习，发现规律，建立模型，部署实行；RPA则自动执行重复性流程，让人得到解放。那么AI\+RPA的结合可以使机器人变得更聪明，扩大自动执行任务的范围，让RPA替代更多人的工作。

RPA 是流程自动化，把重复的流程按照一条条规则自动完成，而 AI 则是可以像人一样做出判断。两者的关系像人的手脚和大脑，RPA 根据指令去执行而 AI 更倾向于去发出指令。

<br/>

![AI01](https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/AI01.png)

云扩在RPA\+AI方面进行了多角度探索，具有以下特点：

- 基于视觉技术的独立的软件界面识别技术，让机器人可以操作更多软件
- 通过计算机视觉、自然语言处理等技术，更容易读懂非结构化数据，更理解执行环境
- 将各大顶级平台的AI能力封装成组件，在RPA流程中拖拽即用

## 二、常见应用场景

#### 应用场景1：税务运营

在财务领域，财务人员经常要从大量的报销中提取发票数据，验证发票的真实性，并在税务系统中进行抵扣申报。简单的数据操作错误就可能导致严重的后果，需要花费大量的人力物力以及成本去补正。

通过OCR技术可以从海量发票中智能提取发票关键数据，例如：发票代码、税额、金额等数据，然后使用RPA保存到Excel文件或在税务系统中自动完成验真、申报抵扣等业务操作。

#### 应用场景2：合同识别

财务人员经常要处理合同，从合同正文里肉眼提取关键信息较为麻烦且容易出错，由于合同没有标准格式，比如甲乙方的位置、合同金额、到期时间等。

通过建立AI模型并进行训练，能从合同中智能提取所需要的关键信息，例如：金额、账期、供应商等数据，然后用RPA把这些数据提交到财务系统，财务人员对数据做后续管理。

了解更多场景，请点[这里](https://www.encoo.com/industry_finance)

## 三、如何在RPA中使用AI能力

云扩已将自研和各大平台的先进AI技术封装成为自动化组件，仅需在编辑中从组件库拖拽至流程设计面板即可，无需再写代码开发。

云扩也为开发者提供了免费试用额度体验，无需先到各大平台注册账号。

<br/>

![AI02](https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/AI02.png)

例如：使用[增值税发票识别](https://academy.encoo.com/zh-cn/wiki/Activities/AI/VATInvoiceIdentification.md?uuid=74dd7758-9a7e-4385-b728-8fa5f83be05a)组件对发票进行OCR识别

<br/>

![AI03](https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/AI03.gif)

更多OCR服务快速试用请看[这里](https://academy.encoo.com/zh-cn/wiki/Reference/Console/ai-center/OCR.md?uuid=a6401df9-a6a0-4508-807a-1c27f5f85707)。

另外，云扩也提供了使用图像识别技术自动识别界面元素，具体详见[自动化原理](https://academy.encoo.com/zh-cn/wiki/DevGuide/AutomationPrinciples.md)专题。

## 四、自定义AI模型

云扩自研[文档理解](https://academy.encoo.com/zh-cn/wiki/Reference/Console/ai-center/aboutdocreader.md?uuid=3d1c7c2d-857e-4791-b738-9ff9455d85bd)技术可通过简单的框选标记，快速定制文档理解模型，让机器人具备文档理解能力，实现文档处理自动化。

- 您可以自定义上传图片，PDF 等格式模板文件，通过框选方式确定需要拖动的文本区域来快速配置模板。
- 您可以根据需要选择适合的内置模型进行模板配置，并使用通用的 OCR 识别、表格 OCR 识别、电子版 PDF 票据证照等多种模型。
- 您可以选择分类文档模板对非结构化文本进行智能抽取。

<br/>

![AI04](https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/AI04.png)

具体文档理解技术使用方法，请看[这里](https://academy.encoo.com/zh-cn/wiki/Reference/Console/ai-center/aboutdocreader.md?uuid=3d1c7c2d-857e-4791-b738-9ff9455d85bd)。

## 五、管理AI服务

当选定一种AI平台的AI服务满足业务需要时，仅需在[云扩超自动化平台](https://console.encoo.com/)的AI中心配置其AI平台购买的AppCode或Key即可，在组件中选择其平台和服务即可在流程中完成调用。

例如：在流程中使用阿里的身份证识别服务，仅需做如下操作：

1）在云扩超自动化平台配置阿里的AI服务身份证识别。 

<br/>

![AI05](https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/AI05.png)

若需使用云扩自研AI服务，仅需联系云扩商务人员完成购买。

2）在编辑器端将身份证识别组件拖拽到设计面板，配置组件属性“平台”=“阿里AI” 和 “图片文件”=“身份证路径”后即可使用。  

<br/>

![AI06](https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/AI06.png)

3）点击“运行”即可查看识别结果