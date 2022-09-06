# 批量提取发票数据


大家好，我是财务专员小C，目前我最头疼的工作是每天都要肉眼查看数十张发票数据，并把发票的关键数据数据录入到Excel中，用于在税务系统中进行抵扣申报。这件事情每天都要花费我3个小时以上，既担心不小心看错了发票数据还要不停的手动写到Excel中。整个过程无比枯燥乏味，头发都快掉完了。
直到有一天遇到了云扩RPA，使用流程自动化解决了我的大难题，头发也变得茂密了。

# 准备工作

开始前，先梳理好要做的事情，也就是想用RPA自动化哪些步骤：
1. 准备好发票图片
2. 确定要提取哪些发票数据
3. 将提取的发票数据保存到Excel中

# 前置条件

* 安装最新版云扩RPA编辑器
* 已注册云扩超自动化平台用于登录编辑器
* 已有发票图片文件（示例中将以提取“增值税发票”为例）

# 开始编写流程

##创建自动化流程目
1. 打开云扩RPA编辑器并使用云扩超自动化平台账号登录
    
2. 创建名为【提取发票数据并保存到Excel】的流程

## 初始化

1. **创建发票文件夹，用于存放发票和保存发票数据**
       * 右键单击项目名称，并创建名为【发票】的相对目录，如下图示： 
       <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/发票相对目录.png"/></div>

       * 右键【发票】文件夹并打开，创建【发票图片】和【发票数据】的文件夹，分别用于存放发票和保存发票数据。在【发票数据】文件夹创建Excel文件 Data.xlsx
       <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/发票数据文件夹.png"/></div> 
     
1. **定义变量用于指定发票所在文件夹、发票数据保存到Excel的路径**
在编辑器中打开Main.xaml文件并在变量面板中并以变量：
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/变量面板.png"/></div>

3. **定义数据表，用于存储发票信息**
      * 在左侧组件库搜索框输入【流程图】找到流程图组件，并拖拽至设计面板，点击其名称并更名为【初始化】。
      * 右键组件并在菜单中点击【批注 - 添加批注】，填写这个步骤要做的内容。
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/添加批注.png"/></div>
        
      **注意**：更改组件名称和为组件添加批注非必须，是为了帮助我们更清晰的理解每一步在做什么，养成这个习惯会让我们开发的流程阅读性更高。特别是在需要多人协作的复杂流程中，会让协作效率有很大提高。
    * 双击流程图（初始化）组件并在其内部拖入【搭建数据表】组件，构建一个空的数据表，用于在后续步骤中存储提取的发票数据。
  <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/搭建数据表.png"/></div>
  
    * 双击【搭建数据表】组件后，并点击【数据表搭建器】在弹窗中定义列名即要提取的发票关键数据名称（发票代码、发票号码等），并在【输出数据表】属性中输入 invoiceData , 选中后按快捷键 CTRL+B快速生成此变量。完成后如下图示：
   <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/输出数据表.png"/></div>
 
    * 最后需要把刚自动生成的变量 invoiceData的范围更改为根目录【流程图_Root】下，因为接下来要在外层逻辑中使用此变量存储数据。更多关于变量的知识可以在变量及类型介绍课程中学习。
  <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/变量范围修改.png"/></div>
     
     **小结**：
    在上述步骤中我们:
    
    1. 发票文件放到了相对目录【发票\发票图片】文件夹中等待被识别
    2. 在【发票\发票数据】下创建了excel文件Data.xlsx用于保存提取的发票数据
    3. 使用【搭建数据表】组件构建了空的DataTable类型变invoiceData用于临时存储提取的发票数据，为保存到Excel做准备
    
## 提取发票数据

4. **使用内置发票识别组件提取出发票关键数据，并保存到临时DataTable变量**
    
    * 在【初始化】下方拖入新的流程图组件，并连接在下方。更名为【提取发票数据】并添加相应批注。
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/初始化.png"/></div>
    
    * 双击此组件并在其内部设计面板中拖入【遍历文件夹】组件更名为【遍历发票所在文件夹】，用于从发票图片目录循环获取发票路径。
     <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/遍历发票所在文件夹.png"/></div>
    
    * 双击此组件展开，在此组件右侧点击【fx】从变量列表中选中之前定义的变量【发票文件夹】。并在此组件内容拖入组件【写入日志】，用于在流程日志中方便查看当前读取的是哪张发票，如果流程执行过程中出现问题，也会快速帮助我们定位问题。具体写法如下图示：
      图中变量filePath 指当前处理的发票完整路径，由【遍历文件夹】组件自动生成。
   <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/遍历发票所在文件夹.png"/></div>
      
    * 在组件库【AI】目录下找到组件【增值税发票】并拖拽到【写入日志】组件下方。
    <div align=center><img width = '600' height ='' src ="hhttps://docimages.blob.core.chinacloudapi.cn/images/COE/遍历文件夹具体写法.png"/></div>
    
    * 在组件库【AI】目录下找到组件【增值税发票】并拖拽到【写入日志】组件下方。
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/拖拽写入日志组件.png"/></div>
    
    * 点击【设置参数】并完成以下配置：
        * 在【平台】属性中从列表选择【云扩AI】。当然也可选择其他平台（阿里云、百度AI等），云扩为每位开发者提供了试用额度，进行体验各个平台的识别效果。
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/设置ai参数"/></div>
        
        * 在【图片文件】属性右侧点击【fx】选择 filePath变量
        * 在【识别结果】属性右侧点击【fx】选择使用建议的变量 result
此组件完成配置如下图示：
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/设置ai参数2.png"/></div>
    
    * 在【增值税发票识别】组件下方拖入【写入日志】组件，用于在日志中拿到识别结果，帮助我们在接下来的【获取节点值】组件中分析JSON数据，定位关键数据节点。
      拼接字符串：filePath+"的提取结果为："+result
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/发票识别写入日志.png"/></div>
      
      到这步时，我们先暂停流程编写，在编辑器工具栏点击【运行】来查看下是否能够成功提取了发票数据。运行后会在日志面板中成功输出了发票数据。
      <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/识别json数据.png"/></div>
      
      在输出面板中单击识别出来的JSON格式的发票数据，右键复制到剪贴板，用于接下来分析这段JSON数据。
      
      继续接下来的步骤。
    * 拖入【获取节点值（字符串）】组件并更名为【获取节点值（发票代码）】，点击【选择节点】打开弹窗并在弹窗中将刚才复制的JSON数据粘贴到文本框，并在字符串最开始位置去除日志产生的非发票信息。
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/json复制文本框.png"/></div>
    
    * 点击【生成结构树】将JSON数据格式化为树状结构，便于查看。
    <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/生成结构树.png"/></div>
    
    * 从树状结构中展开【data】节点并找到关键节点【发票代码】，并会在弹窗左下角【节点路径】中自动生成此JSON结构的【发票代码】节点路径。
     <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/发票代码节点路径.png"/></div>
    
    * 点击【确定】回到设计面板：
        * 属性【节点路径】属性上自动填写上了 “发票代码” 所在的节点。
        * 属性【JSON字符串】选择变量 result
        * 属性【值】，点击右侧【fx】生成变量 发票代码
        ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/发票代码.png "")
         <div align=center><img width = '600' height ='' src ="https://docimages.blob.core.chinacloudapi.cn/images/COE/发票代码节点路径.png"/></div>
        
    * 同样的做法，在下方依次拖入【获取节点值（字符串）】组件分别获取发票数据中的发票号码、开票日期、税额、销方名称、销方税号和金额。
    ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/节点值.png "")
    * 在最下方拖入组件【添加数据行】组件，用于将获取的上方各发票节点数据保存至变量 invoiceData 中。
    * 在属性【数据表】中选择使用变量 invoiceData
    * 在属性【数组】中填写值  new object[]{发票代码,发票号码,开票日期,税额,销方名称,销方税号,金额}
    ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/添加数据行.png "")
    
     **小结**： 
     在章节中我们完成了遍历发票所在文件夹拿到了发票路径，并使用【增值税发票识别】组件提取了发票关键数据，保存到了变量 invoiceData 中。此章节完成流程如图：
     ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/完成流程图.png "")
     
      接下来我们把 invoiceData 中的数据保存到Excel中。
      

## 将发票数据保存至Excel文件

5. **将提取的发票数据保存到本地Excel文件中**
    * 在【提取发票数据】下方拖入新的流程图组件，并连接在下方。更名为【保存发票数据至Excel】并添加相应批注。
    ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/保存Excel.png "")
    
    * 双击展开此组件，并从【表格/Excel/WPS】目录下找到【打开/新建】组件拖入其内部。
        * 属性【文件路径】，选择使用变量 发票数据保存至文件
        * 属性【新建文件】，勾选，指若未发现此路径文件，则会新建一个文件
        * 属性【可视】，勾选，指在流程执行过程中可以在界面上看到整个过程
        ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/打开新建.png "")
        
    * 在【打开/新建】组件范围拖入【写入区域】组件，用于将发票数据写入到Excel文件中。
        * 属性【工作表】，设置为 “Sheet1”，指将数据写入到 Sheet1中
        * 属性【起始单元格】，设置为 “A1”，指将数据在 Sheet1中从A1单元格开始写
        * 属性【数据表】，设置为 invoiceData，指将数据发票数据invoiceData写入到 Excel中
    ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/打开新建写入区域.png "")
    
## 运行流程

    到这里我们就已完成了整个流程【提取发票数据并保存至Excel】的编写，让我们来运行下流程看下结果吧。
    ![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/运行.png "")
    
1. 运行
在编辑器工具栏中点击【运行】，在输出面板中可以看到整个运行过程。

2. 查看结果
回到项目结构位置，右键 发票 并打开文件夹。
![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/项目位置.png "")

    打开发票数据目录下的Data.xlsx查看提取的发票数据
![blockchain](https://docimages.blob.core.chinacloudapi.cn/images/COE/打开Excel文件.png "")

    **总结**
    整个流程开发过程中我们：
    * 为了让流程更具有可读性，我们为每个组件更新了名称和添加了批注
    * 在第一步初始化中定义了空的数据表结构，用于存储提取的发票数据
    * 了解了如何遍历文件夹及获取其文件夹内的文件路径
    * 了解了如何使用AI【增值税发票识别】组件提取发票数据
    * 了解了如何使用【获取节点值】组件分析JSON类型数据并快速定位了要获取的数据节点路径
    * 把提取的发票数据成功写入了excel文件
    * 在流程执行时如何使用不同账号和关键字搜索商品

    **更多自动化开发课程在这里**

* AI专题
* 抓取电商平台数据