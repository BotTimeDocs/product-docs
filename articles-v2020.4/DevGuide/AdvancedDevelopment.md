# 指南六《高级开发技巧》

<br>

>导读: 
> 
> 重在带大家了解RPA流程开发时的几个高级开发技巧：
> * 技巧1：Xpath 定位技巧
> * 技巧2：IFrame选择器使用技巧
> * 技巧3： 云扩浏览器
> * 技巧4：编写代码
> * 技巧5：管理外部代码
> * 技巧5：Excel高级技巧
> * 技巧6：网页操作高级技巧
> * 技巧7：桌面端软件精准定位技巧
>

<br>

## 技巧1：Xpath 定位技巧

### （1）XPath介绍
XPath是标准的结构化查询语言，内置丰富的语法、高阶函数可以提供非常强大的目标元素特征描述能力。

XPath是一种强大、复杂的查询语言； XPath与编辑器中内置的选择器没有本质区别，均可以作为元素特征描述，可以用来定位元素； 用选择器实现不了的场景，XPath也可以胜任。XPath语法强大，但是对使用者需要有一定的理解门槛。</br></br></br>

### （2）如何在编辑器中使用XPath定位网页元素

在编辑器的选择器中可以使用XPath来定位浏览器的元素，以自动化组件“高亮”为例，步骤如下：<br>

**第1步：** 从左侧组件库拖拽一个自动化组件“高亮”至设计面板，在右侧属性面板中点击属性“选择器”右侧的“...”打开选择器窗口：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana01.png"/>
</br><br><br>

**第2步：** 在选择器的弹窗中勾选“生成XPath（仅支持WEB）”选项：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana02.png"/> 

</br><br><br>

**第3步：** 点击“指定元素”重新指定一个Web元素，例如百度一下按钮，此时选择器中的最后一个层级就自动生成了元素的XPath：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana03.png"/>

</br><br><br>

**第4步：** 点击右侧的按钮可以打开XPath编辑窗口，选择默认提供的几种XPath，也可手动进行修改：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana04.png"/>

</br><br><br>

也可直接在节点的属性中点击右键“新增”，之后选择“XPath”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana05.png"/>



<br><br><br>

### （3）如何在XPath中使用变量
在XPath中同样支持选择器中的变量使用方法，即“{{变量名}}”，需注意如在变量中有西文双引需要两个转义为一个，如图中的变量“String1”：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana07.png"/>


</br><br>
同时也支持变量和常量组合使用：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana08.png"/>

</br><br><br>

### （4）如何直接从网页获取XPath
XPath可使用编辑器自动生成，也可从浏览器中复制：按F12打开浏览器开发者模式->右键点击需要生成XPath的元素代码->选择Copy->Copy XPath->将复制过来的XPath粘贴到编辑器中使用即可：
</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana09.png"/>



<br><br>

### （5）XPath的语法
选取节点 XPath 使用路径表达式在 XML 文档中选取节点。节点是通过沿着路径或者 step 来选取的。 

* 下面列出了最常用的路径表达式：

| 表达式 | 描述 |
|------|------|
|nodename|选取此节点的所有子节点。|
|/|从根节点选取。|
|//|从匹配选择的当前节点选择文档中的节点，而不考虑它们的位置。|
|.|选取当前节点。|
|..|选取当前节点的父节点。|
|@|选取属性。|
</br>
<br>

* 一些路径表达式以及结果：

| 路径表达式 | 结果 |
|---------|---------|
|bookstore|选取 bookstore 元素的所有子节点。|
|/bookstore|选取根元素 bookstore。注释：假如路径起始于正斜杠( / )，则此路径始终代表到某元素的绝对路径！|
|bookstore/book|选取属于 bookstore 的子元素的所有 book 元素。|
|//book|选取所有 book 子元素，而不管它们在文档中的位置。|
|bookstore//book|选择属于 bookstore 元素的后代的所有 book 元素，而不管它们位于 bookstore 之下的什么位置。|
|//@lang|选取名为 lang 的所有属性。|
</br>

<br><br>

* XPath运算符

| 运算符 | 描述 | 实例 | 返回值 |
|:---------:|:---------:|:---------:|:---------:|
|&#124;|计算两个节点集|//book &#124; //cd|返回所有拥有 book 和 cd 元素的节点集|
|+|加法|6 + 4|10|
|-|减法|6 - 4|2|
|*|乘法|6 * 4|24|
|div|除法|8 div 4|2|
|=|等于|price=9.80|如果 price 是 9.80，则返回 true。如果 price 是 9.90，则返回 false。|
|!=|不等于|price!=9.80|如果 price 是 9.90，则返回 true。如果 price 是 9.80，则返回 false。|
|< |小于|price<9.80|如果 price 是 9.00，则返回 true。如果 price 是 9.90，则返回 false。|
|<=|小于或|price<=9.80|如果 price 是 9.00，则返回 true。如果 price 是 9.90，则返回 false。|
|> |大于|price>9.80|如果 price 是 9.90，则返回 true。如果 price 是 9.80，则返回 false。|
|>=|大于或等于|price>=9.80|如果 price 是 9.90，则返回 true。如果 price 是 9.70，则返回 false。|
|or|或|price=9.80 or price=9.70|如果 price 是 9.80，或者 price 是 9.70，则返回 true。|
|and|与|price>9.00 and price<9.90|如果 price 大于 9.00，并且 price 小于9.90，则返回 true。|
|mod|计算除法的余数|5 mod 2|1|

<br>

> **提示：** 更多XPath的教程和方法可自己搜索，比较专业的第三方网站如“W3School”，“菜鸟教程等”。[推荐阅读《云扩RPA流程开发课堂》](https://mp.weixin.qq.com/s/wBhI-MuHv_9O-pPQI5TcSQ)

<br><br><br>


## 技巧2：IFrame选择器使用技巧
</br>
选择器支持录制IFrame中的元素，录制后每个元素会自动绑定到IFrame中而无需手动切换域。推荐使用方法是在录制元素时直接指定IFrame中的元素即可，选择器中会自动生成该元素的信息。
<br><br>

如需编辑也建议在指定元素的基础上进行修改。确需手动编辑时，可在选择器的第三级或之后级节点增加“WebElement”属性，再在属性中依次添加该IFrame的信息，用来区分IFrame

如:“Tag”、“Name”、“Id”、“Title”等，由于要切换的是IFrame，所以“Tag”需要为“IFrame”：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana10.png"/>

</br></br>

获取IFrame的信息可以通过浏览器的开发者模式查看，以qq邮箱登录页面为例，打开邮箱页面，之后按F12进入开发者模式，找到要操作的IFrame信息：</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana11.png"/>


</br></br></br>


在完成IFrame的层级编辑后就可编辑要操作的元素信息，这里就与其他Web元素一致了，输入元素的信息，如“Name”、“Id”等，保存后即可操作IFRAME中的元素：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana12.png"/>

</br>

</br></br>

多层IFRAME时在选择器中依照层级依次创建IFrame节点，再在IFrame结束后输入要操作的元素信息即可：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615-nana13.png"/>

</br></br></br></br>

## 技巧3： 云扩浏览器

### （1）使用场景：

目前在编辑器中已内置云扩自研浏览器，主要用于需要抓取浏览器请求的场景； 

比如浏览器请求返回中有一些通过界面自动化无法获取的字段，或者比界面自动化可以更高效的获取到目标数据；
</br>

### （2）抓包配置：

* 配置文件位置：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N1.png"/>

</br></br></br>

* 文件配置介绍：

1）Encoobrowser.exe.config

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N2.png"/>

</br></br></br>


2）Cer文件夹 template.json

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N3.png"/>

</br></br></br>

对每一个 **network** 请求匹配，**key**值配到后生成带**value**前缀的文件，保存在
**PathForStoringCacheFiles**下;保存的文件会根据当前日期进行文件夹分割。文件名称为 **规则匹配值 毫秒级时间戳.json 文件,如下图所示；**

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N4.png"/>

</br></br></br>

文件内容格式如下：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N5.png"/>



</br>

文件格式为 request和response区分，其中request字段已经做了序列化处理，而response需要手动序列化，因为有些返回为一串加密string，并不能自动序列化。

</br></br></br>

## 技巧4：编写代码
>支持在流程中编写代码片段或导入外部的代码。支持C#, Python和Powershell。
>
>当组件或者简单的表达式无法满足业务需求时，可以使用自定义代码类组件完成一些复杂的功能。

</br></br>

### (1) C#代码
C#代码与编辑器的表达式是高度契合的。C#代码包含一个[执行C#代码](https://academy.encoo.com/zh-cn/wiki/Activities/CodeExecuter/CSharp/ExecuteCSharp.md?_v=v2020.1)组件和一个C#代码文件。这里介绍一下几种使用方式。

</br>

从左侧组件库中找到执行C#代码组件并拖拽至设计面板，默认会产生一个隐藏的cs代码文件.code\CSharp\执行CSharp代码.cs

</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N6.png"/>



</br></br>当编辑代码时，会把隐藏的cs代码文件.code\CSharp\执行CSharp代码.cs包含进项目中。

也可以在项目名上右键->导入文件，导入一个cs文件，然后将该cs文件拖拽入编辑器，会自动生成执行C#代码组件。</br></br>

>**注意：**
>- 执行CSharp代码组件中默认有一个Run()方法，这个Run方法是代码执行的入口，不能更改。
>- 在C#代码中可以直接使用流程定义的变量和参数，也可以直接给流程定义的变量和参数赋值。</br>

</br></br>

### （2）Python代码
流程中也可以使用python进行代码编写。Python相关的组件在组件库->代码编程->Python这个目录中。注意，使用执行Python代码组件的时候，该组件必须要在Python环境这个组件的范围内。

- [安装Python](https://academy.encoo.com/zh-cn/wiki/Activities/CodeExecuter/Python/PythonInstall.md?_v=v2020.1)

- [Python环境](https://academy.encoo.com/zh-cn/wiki/Activities/CodeExecuter/Python/PythonScope.md?_v=v2020.1)

- [执行Python组件](https://academy.encoo.com/zh-cn/wiki/Activities/CodeExecuter/Python/PythonExcuteFile.md?_v=v2020.1)
</br>

### （3）Powershell
如果你对Powershell非常熟悉，也可以使用执行[Powershell组件](https://academy.encoo.com/zh-cn/wiki/Activities/CodeExecuter/PowerShell/PowerShell.md?_v=v2020.1)，可参考微软官方文档：[什么是PowerShell？](https://docs.microsoft.com/zh-cn/powershell/scripting/overview?view=powershell-7.2)
</br></br></br>

## 技巧5：管理外部代码
### （1）Nuget代码市场
在流程中我们可以下载Nuget包，从而使用第三方的类库。</br>


<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615N7.png"/>



</br></br>

> **注意：** 安装或者卸载完，会提示是否要重新打开项目。重新打开以后更改才会生效。具体使用细节可以参照 [代码市场](https://academy.encoo.com/zh-cn/wiki/Studio/market/NuGetMarket.md)
</br>

</br></br>

### （2）私有代码市场
我们可以通过管理市场来创建私有的代码市场，这样我们可以通过这个私有市场共享和使用我们自己开发的Nuget包。关于如何配置私有代码市场，请参照 [管理市场](https://academy.encoo.com/zh-cn/wiki/Studio/market/Market.md)
</br></br>

### （3）外部代码的Package更新
当我们创建了私有的代码市场以后，我们可以把我们自己的nuget包复制到市场上。假如设置的是本地路径，就可以直接把nuget包放到这个路径上。假如设置的是网络路径，也可以把nuget复制到网络路径上。

</br>

Nuget包的版本不是由编辑器控制的，编辑器中可以看到的包的版本取决于私有市上有多少这个包的不同版本的nuget包。比如在设置的本地路径上有ESB.1.0.0.nupkg和ESB.1.0.1.nupkg两个包，那么在代码市场上就可以下载安装这两个包。
</br>
</br></br>

## 技巧5：Excel高级技巧
云扩支持用同一批组件操作WPS和EXCEL，无需区分。 
详情请见组件帮助：[打开/新建](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/OpenExcel.md)

### （1）[执行宏](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/ExecuteMacro.md)
Excel宏是一些指令集，每个人在制作表格的过程中也许会有多种功能，而一直重复做的话会非常繁琐，因此就可以通过宏录制来节约时间简化步骤，对于提高工作效率是非常有好处的。对于经常使用excel表格来工作的话，能有效地提高工作，让自己变得更轻松。

一些Excel组件里未曾覆盖到的功能,比如调整单元格的宽度,高度就可以由执行宏组件完成，参考如下示例：
</br>

**第1步.准备工作**

在[打开/新建](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/OpenExcel.md) 组件中开启宏功能：
</br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E2.png"/>


</br>
打开Excel，在Excel选项-信任中心， 开启宏权限：</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E3.png"/>



</br></br>

**第2步.生成宏代码**

宏代码的使用可以自己书写,亦可有Excel里录制宏功能完成,如图:</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E4.png"/>


</br>
</br>
录制完成后,可以点击查看宏,然后找到里面的宏代码</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E5.png"/>


</br></br></br>
可以把里面代码复制出来,放到一个txt文件钟,如：VBA.txt

按照步骤可以生成可执行的宏代码文件,里面一些参数可以自己定义</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E6.png"/>


</br></br>

**第3步.编辑执行宏组件**

</br>

如上图示，定义了3个参数,单元格地址,列宽和行高来更自由的调整单元格。</br>


<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E7.png"/>



</br></br>

**最后一步.** 使用执行宏组件,填入各种参数,就可以正确执行:</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E8.png"/>

</br></br>

### (2) [自动填充](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/AutoFillRange.md)

</br>自动填充组件，等同于我们在Excel选中一个单元格，下拉拖拽的过程；</br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E1.png"/>



</br>如果EXCEL内置有大量的序列(星期、日期、序列等），通过填充功能可以方便、快捷地输入这些内置序列。
</br>

### (3) [设置单元格格式](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/OfficeExcelFormatCells.md)
</br>这个组件包括日常涉及到数值，货币，日期，时间等等，用户体验几乎和Office Excel设置单元格效果。</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E9.png"/>


</br></br></br>

### (4) [复制粘贴](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/OfficeExcelCopyAndPasteArea.md)
</br>可以跨工作表或者当前工作表内进行区域复制粘贴，等同于在Office Excel选中一块区域复制粘贴效果。

</br></br></br>


<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E10.png"/>


</br></br></br>

### (5) [分列](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/OfficeExcel/OfficeExcelTextToColumns.md)
</br>分列就是将一列的数据按照既定分割规则填充到指定区域；</br>


<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615E11.png"/>


</br></br></br></br>

## 技巧6：网页操作高级技巧

**（1）如何获取页面元素的特定属性 ？**

可以使用[获取元素属性值](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/GetElementAttributeValue.md)组件来获取元素属性，支持自定义元素属性，只要目标元素上有对应的属性名称，都可以获取；

在浏览器中按F12快捷键，找到对应的目标元素节点，查看元素节点上是否有想要的属性值，比如索引、链接、title、以及其他属性都可以直接使用获取元素属性获取。</br></br></br>

**（2）如何批量获取元素属性？**

可以通过循环和[获取文本](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/GetText.md)、[获取元素属性值](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/GetElementAttributeValue.md)等组件获取。也可以使用[获取结构化数据](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/ExtractStructuredData.md)组件获取，使用自定义规则获取可以批量获取指定节点上的节点属性。</br></br></br>

**（3）如何滚动页面？**

可以通过[鼠标滚动(中键)](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/rotate-wheel.md)组件或[发送快捷键](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/SendHotkey.md)PgDn来滚动页面。</br></br></br>

**（4）如何操作名称相同的标签页？**

打开多个同名标签页定位元素时会默认在第一个标签页定位，如果需要定位到其他标签页元素，可以在选择器中不适用“Title”定位，改为使用“URL”或其他关键字进行定位。</br></br></br>

**（5）如何操作日期类元素？**

通常日期选择的元素均支持以标准格式输入文本，可以使用“输入文本”组件尝试输入“2022-05-13”，“2022/05/13”或“13-05-2022”等格式输入；如果页面不支持输入文本，可通过组件“设置Web元素属性值”直接对页面上日期元素的属性进行设置；

如上述方法均无效，可使用“点击”组件点击页面上的需要使用的日期：</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R1.png"/>



</br></br>
可以使用变量来“SInfo”中的属性如{{String1}}来动态设置自己需要选择的时间</br></br>

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R2.png"/>


</br></br></br>

**（6）如何判断网页是否打开？**

首先网站可以通过JS的方法“document.readyState”等于“complete”来获取网站是否加载完成</br></br>

<img width = '200'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R3.png"/>

</br></br>

- 如果使用[打开浏览器](https://academy.encoo.com/zh-cn/wiki/Activities/AppAutomation/Browser/OpenBrowser.md)组件时可以勾选“等待加载完成”属性来帮助等待页面状态。
- 如果页面始终处于加载状态，可以增加[等待元素出现](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/WaitElementAppear.md)组件指定一个页面加载完成后才会出现的元素来判断页面的加载或打开的状态。
</br></br></br>

**（7）如何获取下拉框中的选项的内容？**

</br></br>网页下拉框的选项对应的是“Select”的“Option”，如图

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R4.png"/>


</br>
</br></br></br></br>可以通过使用组件“获取元素属性值”指定这个“Select”，之后选择获取该元素的“innerhteml”</br></br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R5.png"/>


</br></br>

即可成功获取

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R6.png"/>



</br></br>桌面应用可以先添加一个“点击”组件展开下拉框，之后通过“获取区域结构”指定展开的下拉框来获取全部选项。
</br></br></br>

**（8）如何使用浏览器上“右键”菜单项？**

使用组件[点击](https://academy.encoo.com/zh-cn/wiki/Activities/UIAutomation/Click.md)指定要右键的元素，把属性“鼠标键”设置为“右键”即可。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R7.png"/>

</br>
</br></br>部分属性可能不支持默认的点击方式，如未成功触发也可修改属性“点击方式”。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DeveloperGuide/0615R8.png"/>


</br></br></br>

## 技巧7：桌面端软件精准定位技巧

**（1）如何挑选最适合的录制技术，如何切换录制技术？**

首先要确定是否需要页面操作，如操作Excel、文件、邮箱等已有相应组件的应用，推荐使用相应的组件做软件自动化操作，远比页面操作要准确、稳定并且快速。确需进行界面自动化操作的，需要安装对应的扩展，如Java扩展，Chrome扩展等。</br>
在安装扩展后指定元素时通常使用默认的Automation录制技术就会自动适配推荐的录制技术，如录制Chrome时会自动使用Chrome技术，录制桌面应用默认使用UIA技术等等。</br>
当上述自动适配的录制技术无法满足时，可以在指定元素时按“F4”来手动切换到自己需要的录制技术，如把UIA技术换为对旧应用适配更好的IA技术等。</br></br></br>

**（2）怎样让组件精准定位元素？**

使用定位的属性越多，定位就越精确，请确保在选择器中使用多个属性，且尽量避免出现和使用“Index”属性。此外在指定元素时指定到按钮上的文本会比指定按钮的框体更加精确，建议在指定元素时优先指定有文本的元素。
</br></br></br>

**（3）如何点击无法录制的元素？**

部分元素无法直接录制（如SAP表格），此时可以通过使用“点击”组件指定可以录制的元素，之后设置属性“偏移”，即可点击无法录制的元素：

<img width = '600'  src ="https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/gjkfjq-0001001.png"/>



</br></br></br>

**（4）上述技术仍无法满足使用场景时怎么办？**

1）使用AI系列组件，可以通过调用第三方的服务实现一些功能，不过需要付费使用；</br></br>

2）图像识别，图像识别即录制下指定的元素图片，在运行时将目标区域与录制时的图片进行对比，当达到设置的相似度后即可成功运行。

需要使用图像识别可在指定元素时按住Ctrl再拖动鼠标左键框选目标，这样组件运行时就会以图像识别的技术去运行。

需注意图像识别会受到诸如系统版本、分辨率、缩放比例、窗口大小等各种情况影响，推荐在默认的其他录制技术无效后再尝试使用；</br></br>

- 屏幕文本化对MFC应用支持的非常好，但对其他应用支持较差。仅推荐对MFC应用进行自动化操作时使用。
- 计算机视觉，计算机视觉组件会根据训练的模型去智能识别窗口中的元素和文本，训练的模型越久，识别的精度就越高，不过当前的训练模型仍旧有限，建议上述均无效后再尝试使用。
- 通过发送快捷键等方式实现自动化。可能有极少的应用由于框架和技术的老旧使得使用现有录制技术均不能很好的操作时，可以使用发送快捷键，坐标等方式进行兜底操作。
