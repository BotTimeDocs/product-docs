# 抓取电商平台商品数据

大家好，我是小A，我是一家年入300万营业额网店店铺的运营人员，店铺除了拥有优质的商品外，店铺商品的价格同样在业内最低，所以店铺粉丝量也在不断增长。为了确保我店铺的商品价格在业内保持竞争力，我每天需要在各大电商平台查看其他竞争店铺的商品定价，以及时分析并做出调整。但是这项工作每天大约花费我2个小时，既枯燥又无聊，长期以往感觉早晚要废，直到有一天遇到了云扩RPA，使用流程自动化解决了我的大难题，人生得到了解放，终于可以节省出时间做些更有意义的事情了 

想知道我是怎么做的吗？那么就跟我一起来吧。

# **准备工作**

开始前，先梳理好要做的事情，也就是想用RPA自动化哪些步骤：

1.  登录电商平台网站
    
2.  搜索同类商品
    
3.  获取各商家的商品信息及价格列表
    
4.  将商品数据保存到Excel中
    

## **前置条件**

-   已有京东账号（本节课程将使用用户名+密码的方式登录京东并抓取数据，开始前请确保已有账号）
    
-   [安装最新版云扩RPA编辑器](https://academy.encoo.com/zh-cn/wiki/Studio/quickStart/Installation.md?uuid=b99286da-9595-4c22-9355-f59b1d179c82)
    

## 编写自动化流程

### **1.  创建自动化流程项目**
    
打开云扩RPA编辑器并创建名为【获取商品信息】的流程
    
![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/1.png)

### **2.  初始化流程**

为了确保流程稳定运行，且不会覆盖已有文件产生冲突，并始终把最新获取的数据保存至一个名为【商品数据.xlsx】的excel文件中，我们需要做一些特定处理，逻辑如下：

首先判断相对路径下是否有文件 【商品数据.xlsx】，此文件将用于保存抓取的商品信息。若本地已有此文件则先删除，在后续流程中重新创建此文件；若没有则跳过此步骤。

**具体做法如下：**
# 1. 在左侧组件库【流程控制】目录下找到组件【序列】拖拽至设计面板，并连接在【Start】节点下方

【序列】组件适用于逻辑简单的顺序工作流场景。此节这段逻辑比较简单只有2步，判断文件是否存在，存在则删除，所以可以选择使用【序列】。当然，同样也可以选择使用【流程图】，【流程图】适用于逻辑判断较多且复杂的业务场景，想了解更多请点击[这里](https://www.bilibili.com/video/BV1Fa411i7sn?spm_id_from=333.999.0.0)。

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/2.png)

小技巧: 为了让自己或其他伙伴更好的理解要做的事情，可以更改组件名称或选中组件并鼠标右键，在菜单中选择【批注】，填写内容并固定在组件上。完成后如下图：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/3.png"/> 

# 2.  判断文件是否存在
    

双击此组件，进入此组件中。并实现逻辑：判断【商品数据.xlsx】文件是否存在，若存在则先删除，若不在则跳过，在后续的步骤中重新创建。

## 2.1  从左侧组件目录中搜索组件【文件/文件夹是否存在】，并拖拽至设计面板。在弹窗中的组件属性中填写如下图中内容。点击【确定】回到设计面板。
    

路径："商品数据.xlsx"

路径是否存在：exists 

注意：exists是变量，用于存储判断结果，点击其右侧【fx】后在弹窗中点击【使用】自动创建变量exists并应用在组件中。

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/4.png)

## 2.2  在组件库找到组件【条件(if)】并拖拽至组件【文件/文件夹是否存在】下方。
    

在弹窗中填写逻辑判断 exists == true ，如下图。

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/5.png)

## 2.3  在组件【条件（if）】中的【条件成立】区域中，把组件【删除文件/文件夹】拖拽至此处。并在填写如下内容：
    

文件：“商品数据.xlsx”

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/6.png)

小结：

到此步咱们完成了流程初始化的逻辑：判断【商品数据.xlsx】文件是否存在，若存在则先删除，若不在则跳过。

# 3.  登录京东网站
    
本节课程将使用流程运行前填写【用户名、密码和商品关键字】的方式搜索相关信息，即流程运行前先填写这些信息后再执行。这样写的好处是只要填写了用户名、密码和商品关键字，团队中的其他人都可以使用这个流程，无需再修改流程。

接下来为大家讲解如何实现及如何使用。

本章节将自动化以下逻辑：

-   打开京东网站首页
    
-   在首页判断是否显示关键字【请登录】，若出现关键字【请登录】则是为当前未登录，若未出现则断定为当前是未登录状态
    
-   若当前是已登录状态，则直接根据商品关键字抓取数据；若当前是未登录状态，则使用【用户名+密码】完成登录
    

## 3.1  打开京东网站
    

注意：在开始前请先安装浏览器扩展，以确保可以实现自动化。本节将在Chrome浏览器中操作，则需先安装【Chrome扩展】

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/7.png)

### 3.1.1  点击左上角【流程图_Root】回到第一个设计面板，从左侧组件库找到【打开浏览器】并拖拽到第一个组件下方，填写相应批注。如图所示：
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/8.png)

### 3.1.2  双击【打开浏览器】组件进入内部编辑区域，并在网址属性中填写京东地址：
    

网址："https://www.jd.com"

浏览器类型：Chrome

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/9.png)

## 3.2  判断是否已登录
    

若在已登录的情况下，避免重复登录做多余的事情，我们可以先判断是否已登录，若已登录则跳过登录步骤，直接开始搜索。

### 3.2.1  把组件【判断元素是否存在】拖拽进来
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/10.png)

### 3.2.2  点击【指定元素】，此时编辑器最小化，在京东首页上把鼠标移动至【你好，请登录】位置，待边框高亮时单击即可完成录制。如下视频所示：
    

在此组件的属性【结果】中点击【fx】并生成变量isLogin，用于保存判断结果。

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/11.png)

### 3.2.3  在【判断元素是否存在】组件下方添加组件【条件（if）】，并在属性判断条件中设置：
    

判断条件：isLogin == true

在【条件成立】区域中添加组件【点击】，即在页面上点击【请登录】前往登录页面。同上，使用【指定元素】在页面上选取【请登录】位置高亮后回到设计面板。如下图所示：

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/12.png)

在【条件不成立】区域中添加组件【写入日志】，并填写内容“已有用户登录！”，让我们可以在日志中可以明白已登录且跳过了登录步骤。如下图所示：

<img width = '685'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/13.png"/> 

## 3.3 登录

 在浏览器手动点击【请登录】，进入 [登录页](https://passport.jd.com/new/login.aspx?ReturnUrl=https%3A%2F%2Fwww.jd.com%2F)。

### 3.3.1 回到编辑器设计面板，并在【点击】组件下方在增加一个【点击】组件，以完成自动点击页面上的【账号登录】

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/14.png"/> 


### 3.3.2 接下来我们继续从组件面板拖拽2个【输入文本】组件放在下方，并使用其【指定元素】分别指定页面上的【用户名和密码】框。
![]()  
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/15.png"/> 

### 3.3.3  定义流程参数和赋值
    
为了让流程使用者在不修改流程的前提下使用不同账号和查询不同商品，我们可以使用【参数】的方式实现。

流程参数适用于在运行流程时期望把特定信息告诉流程，使流程根据这些信息做相应的事情。例如在这个流程中：

-   小王可以输入自己的账号+想要搜索的商品关键字“啤酒”告诉流程，让流程把啤酒相关的数据抓取下来；
    
-   小王可以输入自己的账号+想要搜索的商品关键字“威士忌”告诉流程，让流程把威士忌相关的数据抓取下来；
    

实现逻辑如下图所示：

步骤1：打开参数面板

步骤2：定义参数 用户名 、密码

步骤3：把用户名赋值给第一个【输入文本】组件，即在页面用户名文本框中填写用户名；

步骤4：把密码赋值给第一个【输入文本】组件，即在页面密码框中填写密码；

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/16.png)

注意：为了确保密码的安全性，建议参数密码的参数类型选择为 Encoo.DataType.Password, 这样的话在输入密码时则会以星号*的方式显示。

### 3.3.4 最后在最下方再次拖入一个【点击】组件，使用【指定元素】选取页面上的【登录】按钮。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/17.png"/> 



为了确认是否写的准确，可以先尝试运行一次流程，预期结果是成功完成登录，并回到京东首页。

# 4. 搜索商品关键字

完成登录后，在首页的输入框中搜索商品关键字

### 4.1  回到【打开浏览器】设计区域，在【序列】下方添加组件【输入文本】，用于在搜索框中输入商品关键字
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/18.png)

### 4.2 单击组件【输入文本】的【指定元素】选取浏览器页面上的【搜索框】，待黄色高亮时单击并返回到设计面板。
    

### 4.3 在【参数面板】添加String类型的参数【商品关键字】并设置默认值 “茅台”，再把填充到【输入文本】组件属性中。如下图所示：
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/19.png)

### 4.4 在【输入文本】下方添加组件【点击】，用于自动化点击页面上的【搜索】按钮。
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/20.png)

# 5. 获取商品数据

根据商品关键字查看搜索结果，并从商品列表中获取商品名称和价格信息。将数据保存在变量dataTable中。在这一步我们使用【获取结构化数据】组件完成这些操作。

【获取结构化数据】组件适用于抓取页面表格、列表等结构化的数据，仅需几步简单点击就可完成，在下面视频中将会为大家讲解如何操作。想了解更多，可以看[这里](https://www.bilibili.com/video/BV1pB4y1U7Gx)。

### 5.1  在最下方添加组件【获取结构化数据】，并完成以下事情：
    

-   指定搜索结果页面为数据源
    
-   选取商品名称为第一列
    
-   选取价格为第二列
    
-   指定最多获取50行内容
    
-   将数据保存在变量dataTable中
    

参考视频示例：

### 5.2 选中【获取结构化数据】组件，打开【变量面板】，将变量dataTable的【范围】设置为 流程图_Root， 以用于接下来保存此数据至Excel文件中。

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/21.png)

# 6. 将商品数据保存至excel文件

将根据商品关键字搜索的结果保存至excel文件【商品数据.xlsx】中。

### 6.1 从组件库Excel目录下找到组件【打开/新建】并拖拽至设计面板，连接在【打开浏览器】下方，在弹窗中填写相应属性，如下图示。
    

文件路径："商品数据.xlsx" ，当前项目的相对路径

新建文件：勾选，即每次流程执行时都会新建此文件

自动保存：勾选，即有新数据时则会自动保存

可视：勾选，即整个操作过程可在屏幕上看到

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/22.png"/>

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/23.png)

### 6.2  将数据变量dataTable保存至Excel中。在【打开/新建】组件中添加组件【写入区域】，并指定如下属性：
    

工作表："Sheet1"

起始单元格："A1"

数据表：dataTable，即存储的内容为变量dataTable数据
<img width = '685'  src ="https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/24.png"/>

# 7. 运行流程并查看结果

### 7.1 运行
    

在编辑器工具栏中点击【运行】，并在弹窗中分别输入京东用户名、密码和欲检索的商品关键字。

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/25.png)

### 7.2  查看结果
    

### 7.2.1 运行结束后，在项目的相对路径目录下找到【商品数据.xlsx】
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/26.png)

### 7.2.2 双击【商品数据.xlsx】文件查看商品数据
    

![](https://docimages.blob.core.chinacloudapi.cn/images/Course/GetJDData/27.png)

# 总结

到这里咱们就已完成了整个流程编写，整个过程中我们：

-   为了流程更稳定，在流程开始阶段添加了数据文件是否存在的判断逻辑
    
-   为了避免多余的步骤，实现了搜索前先判断是否已登录的逻辑
    
-   在判断是否登录及接下来的步骤中学会了简单使用【指定元素】功能指定页面控件的能力
    
-   了解了如何使用【获取结构化数据】抓取搜索结果列表
    
-   把搜索出的商品数据成功写入了excel文件
    
-   在流程执行时如何使用不同账号和关键字搜索商品
    

# 更多自动化流程在这里

-   批量识别发票并表格
    
-   库房材料核对及应收应付对帐
    

# 小技巧

-   在流程编写过程中多使用【批注】功能，流程会更容易维护哦
    
-   使用编辑器自带的【FX】功能，会自动产生变量减少出错的概率
    
-   选中组件右键单击或按F1可快速查看帮助文档，文档有详细的示例说明
    

# 示例流程文件
![[京东-获取商品信息.dgs]]