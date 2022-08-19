# Error3：Office Excel自动化

<br>

 <font color=grey size=2 > 
 
 引导：
 
> RPA流程自动化中，Office自动化操作需要官方excel软件,
> 请注意不要使用 <font color=green size=2 >**非官方破解、绿色等**</font>版本非官方版本软件(其接口**不支持**)；
> 另外WPS或Office未安装好、或者Office或WPS版本冲突导致现象导致的异常,
> 需要对Office/WPS软件进行修复。
> </font>

<br><br>
<br>

#### Q：加载类型库/DLL 时出错。 (Exception from HRESULT: 0x80029C4A (TYPE_E_CANTLOADLIBRARY)) 

<font color=5a6877>
<br>

**【解决办法-AC0018-1】** ：如下 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0018-1.png"/>


<br>

**【解决办法-AC0018-2】** ：

从[官方下载](https://support.microsoft.com/zh-cn/office/%E4%BB%8E-pc-%E5%8D%B8%E8%BD%BD-office-9dd49b83-264a-477a-8fcc-2fdf5dbf61d8)Office完全卸载工具

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0018-2.png"/>


<br>

**【解决办法-AC0018-3】** ：

使用Office Tool工具卸载，链接：[Office Tool Plus 官方网站](https://otp.landian.vip/zh-cn/)

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0018-3.png"/>

</font><br><br>
---
<br>

#### Q：0x80070057 (E_INVALIDARG))

<font color=5a6877>
<br>

**【解决办法-AC0001】** ：

检查是否同时安装wps和office，并且将wps设置为默认程序，如果是卸载wps即可；
</font><br><br>
---
<br>


#### Q：检索 COM 类工厂中 CLSID 为 {00021A20-0000-0000-C000-000000000046} 的组件时失败，原因是出现以下错误: 0x80080005

<font color=5a6877>
<br>

**【解决办法-AC0004】** ：

除用工具彻底卸载wps或Office外,如果下图所示注册表,也整个删除

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0004.png"/>

</font><br><br>
---
<br>


#### Q：环境_COM类相关，报错信息：0x80004002 

无法将类型为“System.__ComObject”的 COM 对象强制转换为接口类型“Microsoft.Office.Interop.Excel.Worksheet”。此操作失败的原因是对 IID 为“{000208D8-0000-0000-C000-000000000046}”的接口的 COM 组件调用 QueryInterface 因以下错误而失败: 不支持此接口 (异常来自HRESULT:0x80004002 (E_NOINTERFACE))。

【问题原因】：电脑安装先后多个Office Excel版本，或者安装过WPS。

<font color=5a6877>
<br>

**【解决办法-AC0003】** ：

* 在注册表中找到：
HKEY_CLASSES_ROOT\TypeLib\{00020813-0000-0000-C000-000000000046}
在其子项中，删除与当前Excel版本不一致的选项即可。
注意：删除注册表选项前，请先备份删除的选项。
如下图所示：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0003.png"/>


</font><br><br>
---
<br>


#### Q：详细错误信息：检索COM类工厂中CLSID为{00024500-0000-0000-C000-000000000046}的组件失败，原因是出现以下错误：80040154没有注册类（异常来自HRESULT:0x80040154(REGDB_E_CLASSNOTREG))。

<font color=5a6877>

【原因分析】：在操作系统中注册的COM组件的多个版本（WPS/Excel）弄乱了
<br>

**【解决办法-AC0005】** ：[点击查看链接：COM类错误80040154](https://blog.csdn.net/cxygs5788/article/details/106351373?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&utm_relevant_index=5)
<br><br>

**补充：如何修复对应的WPS和office365？**<br>

* (1) WPS COM 如何修复？<br>

<br>【解决办法】：解决方式如下，即用修复工具修复一下 ，WPS用对应WPS的配置工具，WPS修复示意图：<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/WPS-修复.png"/>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/WPS修复-1.png"/>

<br><br>

* (2) Office 365 如何修复？

<br>【解决办法】：解决方式如下，即用修复工具修复一下 ，Office 365用自带修复方案 <br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/365修复-1.png"/>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/365-2.png"/>


</font><br><br>
---
<br>


### 2.2 EXCEL-打开新建

#### Q：详细错误信息：Excel尚未安装. 

<font color=5a6877>
<br>

**【解决办法-AC0019】** ：

* 可能是wps安装的问题，你可以试下打开新建组件，切换运行环境为无依赖。
<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0019-2.png"/>


<br>

* 运行的时候 设置一下 这个 别选 管理员运行 ，WPS第三方不支持管理员 或者要管理员必须就建议按照office excel。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0019-1.png"/>


<br>*补充：wps是per user 安装，不能用管理员运行。 以上办法都不行时，试一下官方工具卸载之后重装WPS或Office*

</font><br><br>
---
<br>


#### Q：WPS“打开/新建”-打开.xlsm文件报错，[错误]文件扩展名不正确

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0020.png"/>

<font color=5a6877>

【原因分析】：

* .xlsm格式是只支持在excel里面打开，wps不支持

* 编辑器1.1.2204.9版本开始，合并excel和WPS分类，“打开/新建”合并为一个，新版本功能不会再出现此类问题报错。

<br>

**【解决办法-AC0020】** ：
用excel-打开/新建 ，替换掉wps-打开/新建

</font><br><br>
---
<br>


#### Q：打开/新建失败，错误代码：0x80010105(RPC_E_SERVERFAULT)

<font color=5a6877>
<br>

**【解决办法-AC0007】** ：

检查是否安装福昕PDF阅读器，找到“excel选项”，点开后点击“加载项”，最下面有个管理加载项的下拉菜单，选“COM加载项”，点“转到”，这时会弹出一个框，把里面pdf软件的加载项前面的勾去掉，点确定；

</font><br><br>
---
<br>

#### Q：打开/新建 HRESULT E_FAIL，报错信息：0x800A03EC

<font color=5a6877>
<br>

**【解决办法-AC0008】** ：

检查文件是否能正常打开，导致的原因有多种，一般是由于该EXCEL文件的编辑环境发生较大变化，如64位系统环境下编辑的EXCEL不一定能在32位系统环境下顺利读取。

</font><br><br>
---
<br>


#### Q：打开/新建失败，报错信息：0x8002801D

详细错误信息：Unable to cast COM object of type 'Microsoft.Office.Interop.Excel.ApplicationClass' to interface type 'Microsoft.Office.Interop.Excel._Application'. This operation failed because the QueryInterface call on the COM component for the interface with IID '{000208D5-0000-0000-C000-000000000046}' failed due to the following error: 库没有注册。 (Exception from HRESULT: 0x8002801D (TYPE_E_LIBNOTREGISTERED)).

<font color=5a6877>
<br>

**【解决办法-AC0009】** ：排查电脑是否安装过wps,如 是:重新安装wps

</font><br><br>
---
<br>


#### Q：打开/新建失败。详细错误信息：Retrieving the COM class factory for component with CLSID {00024500-0000-0000-C000-000000000046} failed due to the following error: 8007065e 这个类型的数据不受支持。 (Exception from HRESULT: 0x8007065E).

<font color=5a6877>

【原因分析】：安装的Excel版本不正确

<br>

**【解决办法-AC0011】** ：[点击查看：CLSID 为 {00024500-0000-0000-C000-000000000046} 的组件失败](https://blog.csdn.net/weixin_34293911/article/details/94269260?ops_request_misc=&request_id=&biz_id=102&utm_term=0x8007065E&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-94269260.nonecase&spm=1018.2226.3001.4187)

</font><br><br>
---
<br>


#### Q：定时任务，打开/新建失败，HRESULT:0x80080005

【原因分析】：如果许多 COM+ 应用程序在 This User 属性中指定的不同用户帐户下运行，则计算机无法分配内存以创建新用户的新桌面堆。 因此，进程无法启动。

<font color=5a6877>

<br>

**【解决办法-AC0010】** ：具体解决办法,详见链接：[启动多个 COM+ 应用程序时出错：错误代码80080005 -- 服务器执行失败](https://docs.microsoft.com/zh-cn/troubleshoot/windows-server/application-management/error-8008005-when-start-complus-applications)

</font><br><br>
---
<br>


#### Q：OPC Compliance error [M4.3]：Producers shall not create a document element that contains refinements to the Dublin Core elements，except tor the two specified in the schema：

<font color=5a6877>

【原因分析】：Excel兼容性导致

<br>

**【解决办法-AC0021】** ：点击查看链接[使用poi读取excel异常](https://blog.csdn.net/IM507/article/details/100561304)，参考链接内容看下应该是否文件有问题，可以把打开失败的文件名抛出，整理成一个列表比那与之后查看

</font><br><br>
---
<br>

### 2.3 Excel-读取写入

#### Q：excel 超出当前范围。 (异常来自 HRESULT:0x8002000A (DISP_E_OVERFLOW))，excel 某些单元格格式有问题，读取就会有异常

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0013.png"/>

<font color=5a6877>
<br>

**【解决办法-AC0013】** ：定位不到错误行的情况下，可以全选把单元格格式都设为文本

</font><br><br>
---
<br>


#### Q：读取区域失败 ，错误示例“详细错误信息：A1：L1输入区域无效”

<font color=5a6877>
<br>

**【解决办法-AC0022】** ：确认一下，区域表示的“冒号”用了中文冒号，需要使用英文冒号

读取区域失败，详细错误信息：以下方法或属性之间的调用具有二义性：
“System.Data.DataRowColection.Add(System.Data.DataRow)”和“System.Data.DataRowCollection.Add(params object[])”
【解决办法】：可以试试把参数类型改成DataRow，然后看下哪里用的object[]

</font><br><br>
---
<br>

#### Q：读取区域失败，[错误] Exception from HRESULT:0x800A01A8

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0014.png"/>

<font color=5a6877>
<br>

**【解决办法-AC0014】** ：获取文件夹类别，一个个打开excel处理完关闭的时候，前面excel还没关闭好，进程被占用，前面打开加一个延时

</font><br><br>
---
<br>


#### Q：写入单元格失败，0x800A03EC。

<font color=5a6877>
<br>

**【解决办法-AC0016】** ：检查写入单元格是否合法超出excel范围


</font><br><br>
---
<br>


#### Q：操作Excel文件，[错误]创建透视表失败。详细错误信息：异常来自HRESULT:0x8FE3301F

<font color=5a6877>
<br>

**【解决办法-AC0017】** ：检查创建透视表范围的列头是否为空


</font><br><br>
---
<br>


#### Q：工作表筛选_筛选出错，[错误]类Range的AutoFilter方法无效

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0023.png"/>

<font color=5a6877>
<br>

**【解决办法-AC0023】** ：报错与组件的全局筛选冲突  解决办法:在excel里先取消筛选

</font><br><br>
---
<br>


#### Q：使用筛选组件失败，且电脑只安装Wps，错误: 0x80070057

<font color=5a6877>
【原因分析】：Wps接口实现Office接口兼容性问题，若只安装Office情况能正常执行；

<br>

**【解决办法-AC0001】** ：按照下方的在步骤操作确认

1. 设置第二个筛选条件和第一个一样；
2. 更新编辑器版本，最新版本已经做了兼容性处理；

</font><br><br>
---
<br>


### 2.4 Excel-执行宏

#### Q：执行宏失败，错误代码：RPC 服务器不可用。 (异常来自 HRESULT:0x800706BA)

<font color=5a6877>
<br>

**【解决办法-AC0015】** ：检查宏脚本是否可以在excel中手动调用，其次检查宏函数名字是否以譬如set等关键字开头.

补充：报错描述的是rpc通信错误，文件过大也会使得rpc通信失败 

</font><br><br>
---
<br>


#### Q：执行宏失败。详细错误信息：不信任到Visual Basic Project的程序连接

<font color=5a6877>
<br>

**【解决办法-AC0025】** ：<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0025.jpg"/>

</font><br><br>
---
<br>


#### Q：执行宏失败。详细错误信息：不信任到Visual Basic Project的程序连接

<font color=5a6877>
<br>

**【解决办法-AC0025】** ：<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0025.jpg"/>

</font><br><br>
---
<br>

#### Q：执行宏失败。详细错误信息：800A0023

<font color=5a6877>
<br>

**【解决办法-AC0043】** ：vba脚本问题。800A0023一般指“未定义” Sub 或 Function，具体参考链接：[[导入]vbscript错误代码及对应解释大全/VBScript 语法错误](https://blog.csdn.net/b88054/article/details/101574710?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165811707416782425154685%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165811707416782425154685&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2%7Eall%7Efirst_rank_ecpm_v1%7Erank_v31_ecpm-8-101574710-null-null.142%5Ev32%5Eexperiment_2_v1,185%5Ev2%5Econtrol&utm_term=800A0023&spm=1018.2226.3001.4187)

</font><br><br>
---
<br>

#### Q：打开/新建失败。详细错误信息：The document cannot be opened because there is an invalid part with an unexpected content type. 

<font color=5a6877>
<br>

**【解决办法-AC0045】** ：

网上有个同样的PPT文件的错误， 可能是那个excel是用Mac os里面新建的，你可以在Windows上新建一个excel, 然后把那个错误的excel里面内容复制过来试下，这里还提供了一种使用代码修复的方式：
https://stackoverflow.com/questions/18910623/the-document-cannot-be-opened-because-there-is-an-invalid-part-with-an-unexpecte  
</font><br><br>
---
<br>


#### Q：执行宏 - 添加链接失败。详细错误信息：Exception from HRESULT: 0x800A03EC

<font color=5a6877>

<br>

【原因分析】：

* （1）先装的office 然后再装的wps，wps会默认把excel改成wps打开，然后wps的执行宏是要收费的，所以会报错；
<br>
* （2）写入单元格超出合法excel范围了

<br>

**【解决办法-AC0012】** ：

**解决办法一：** 把wps这几项取消勾选

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/0x800A03EC.png"/>


<br>

**解决办法二：**需要确认一下是不是行号或者列号是不是有错误，也有可能是宏文件本身无法打开

</font><br><br>
---
<br>


### 2.5 Excel-其他报错

#### Q：环境_COM类相关，报错信息：0x8001010A (RPC_E_SERVERCALL_RETRYLATER)

<font color=5a6877>
<br>

**【解决办法-AC0006】** ：详见链接，关掉可视 [c# - Error:-(Exception from HRESULT: 0x8001010A (RPC_E_SERVERCALL_RETRYLATER)) - Stack Overflow](https://stackoverflow.com/questions/26073754/error-exception-from-hresult-0x8001010a-rpc-e-servercall-retrylater)

</font><br><br>
---
<br>


#### Q：创建透视数据表失败，详细错误信息：类 PivotTable 的 PivotFields 方法无效

<font color=5a6877>
<br>

**【解决办法-AC0026】** ：要根据创建透视表数据源区域重新算列索引<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0026.png"/>

</font>
<br><br>
---
<br>

#### Q：新建文件/文件夹失败，详细错误信息：不支持给定路径的格式。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0027.png"/>

<font color=5a6877>
<br>

**【解决办法-AC0027】** ：

系统-文件下的组件，如果出现报错"不支持给定路径的格式"时，一般是传入的路径的字符串开头存在一个不可见的字符，可以通过string.TrimStart(string[0])的方式来移除掉

</font>
<br><br>
---
<br>

#### Q：Your stream was neither an OLE2 stream, nor an OOXML stream.

<font color=5a6877>

【原因分析】：文件有问题,重命名过或者本身格式不对

<br>

**【解决办法-AC0028】** ：修复文件或者换一个文件试试

</font>
<br><br>
---
<br>

#### Q：写入区域失败。详细错误信息：无法对多重选择区域执行此操作

<font color=5a6877>
<br>

**【解决办法-AC0029】** ：确认excel表格是否有合并单元格，有的话取消之后再进行写入操作。

</font>
<br><br>
---
<br>

#### Q：排序失败。详细错误信息：指定的参数已超出有效值的范围

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0040.png"/>

<font color=5a6877>
<br>

**【解决办法-AC0040】** ：确认excel表格列头里面,是不是有合并单元格。
</font>
<br><br>
---
<br>


#### Q：详细错误信息：无法保存。(异常来自HRESULT:0x80030103(STG_E_CANTSAVE))

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0041.png"/>


<font color=5a6877>
<br>

**【解决办法-AC0041】** ：偶现三方环境接口异常，重启编辑器试一下。

</font>
<br><br>
---
<br>


#### Q： [错误]写入单元格失败。详细错误信息：详细错误信息：灾难性故障(异常来自 HRESULT:0x8000FFFF(_UNEXPECTED))

<br>

<font color=5a6877>
<br>

**【解决办法-AC0042】** ：选择无依赖方式 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/AC0042.png"/>

</font>
<br><br>
---
<br>