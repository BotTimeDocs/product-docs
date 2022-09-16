# FAQ2：元素识别定位

#### Q：验证sap客户端，有地方识别不到怎么办?

<br>


<font color=5a6877>
<br><br>

**【解决办法-A3_00019】**: 请确认编辑器权限要跟SAP保持一致

</font>
<br><br>
---
<br> 

#### Q：无法识别到指定的元素，怎么办？

<br>

<font color=5a6877> 

【解决方法A3_00001】:
1. 匹配超时的时间设置长一点
2. 录制时按F4切换录制技术，直至可以识别为止
3. 如果以上无法解决，录制时按Ctrl+框选的形式，使用图像识别
4. 如果以上无法解决，尝试更换组件，如，“坐标点击”、“CV类组件”
5. 如果以上无法解决，借助元素探测器，找到元素值，观察其特征，如果目标 title 为动态的
❖ 把动态字段的值用`*`通配符来代替
❖ 使用{{变量名}}基础变量来代替
6.  如果以上无法解决，勾选生成 选择器编辑器右上角的XPath（仅支持 WEB），使用XPath代码，如，//label[@for='confCode']/..//input[contains(@placeholder,'变量代码')]，然后重新指向元素

 </font><br><br>
---
<br>

#### Q：元素录制的时候，xpath录制会不会相对来说比较稳定？
<br>

<font color=5a6877>
<br>

**【解决办法-A3_00015】**：

xpath和自动生成的选择器的区别其实只是定位的“标准”不同，xpath是通过元素的位置，自动生成的选择器一般是元素的属性。如果要避免因元素变化导致的识别失败的话，这时候要去分析元素变得是什么，如果是位置经常变化，那xpath就不一定适用了。如果位置不变，但属性经常变化，那可能xpath会更适合一些
</font>
<br><br>
---
<br> 

#### Q：文本框中自动输入时间的时候出现乱码

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A_500006.png"/>



<br>

<font color=5a6877>
<br>**【解决办法A3_00016】**：

输入法是中文的话换成英文再试试，输入法换成英文 模拟键盘输入汉字依然可以输汉字。

</font>
<br><br>
---
<br> 


#### Q：当选择器指定元素 同时找到多个元素时候的处理办法 

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/500007.png"/>


<br>

<font color=5a6877>
<br>

【解决办法-A3_00017】

用网页属性来定位到元素后，然后再判断是否需要Index。

需要根据中间元素的一些属性来写XPath，这个需要了解下XPath的一些基础语法，[参考链接](https://www.w3school.com.cn/xpath/xpath_syntax.asp)

这个是通过元素属性定位的，如果是模糊匹配就需要用到Contain之类的语法,[参考链接](https://blog.csdn.net/qq_37635275/article/details/123486341)

</font>
<br><br>
---
<br> 


#### Q：用远程桌面跑流程，我远程桌面最小化后，就获取不到元素了

<br>

<font color=5a6877>
<br>

【解决办法-A1_00018】：远程桌面不能最小化必须窗口化

</font>
<br><br>
---
<br> 


#### Q：用循环重复做同样的操作获取网页结构化数据，为何每次获取的数据都缺少一列？

<br>

<font color=5a6877> 

【解决方法A3_00002】:

1. 排查缺少的那一列的网页结构是不是table元素。如果Table的td标签再套Div，然后Div里面再有span，有可能识别不到
2. 需要再获取一次结构化数据，在“是否需要导入全部”时，选择“否”，再选择下一行数据，然后再循环两次结构化数据获取的Datatable整合为一个。

 </font><br><br>
---
<br>

#### Q：如何使用用友U8获取结构化数据？

<br>

<font color=5a6877> 

【解决方法A3_00003】:检查识别的录制技术：
❖ 如果录制技术为JAB时可识别，则可以使用该录制技术进行获取结构化数据
❖ 如果录制技术为UIA时可识别，则需要用市场组件【FlexGrid表格抓取】来获取数据

 </font><br><br>
 ---
 <br>

#### Q：如何获取表格内的其他属性，比如Web文本上的超链接？

<br>

<font color=5a6877> 

【解决方法A3_00004】:在指定数据源后的弹窗中点击“新增”按钮，在下拉框中选择“Href”属性即可获取到文本上的超链接，此外还可以通过该方法获取Title甚至一些自定义属性：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/4-1.png"/>



获取成功后如图：
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/5-1.png"/>



 </font><br><br>
 ---
 <br>

#### Q：指定元素时报错“无法识别您所指定元素的规律，无法获取……”该如何处理？

<br>

<font color=5a6877> 

【解决方法A3_00005】:提示该错误是因为指定的第二个元素与第一个元素间不存在可以获取数据的规律，需要重新指定一个有规律的元素才能成功运行。首先需要确保指定的两个元素要在同一个页面、同一个域下，其次要保证指定的两个元素有一定的相似点，通常元素归属于同一个父节点下的同类型节点或节点属性都可匹配，具体的信息可以按F12来查看浏览器的源代码来查找可以匹配的元素。

 </font><br><br>
 ---
 <br>

#### Q：指定元素成功，但获取到的表格为空是什么原因？

<br>

<font color=5a6877> 

【解决方法A3_00006】:获取结构化数据会优先识别表格，而指定的这个表是空的，页面显示的数据未存在这个表格内，所以获取到的表就是空的。遇到这种情况可以按F12来查看并指定实际显示数据的表的位置，或者在弹出是否获取整表时点击“取消”，之后根据提示手动指定行列中的数据来逐列获取数据即可。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/5-2.png"/>
 
 </font><br><br>
 ---
 <br>

#### Q：Chrome打印页面元素验证失败，如何处理？

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/8-2.png"/>


直接指定上图中的元素后进行验证就会验证失败，这是由于该应用窗口在没有焦点的时候拿到的进程名与有焦点时不一样，录制时焦点不在该窗口上而运行时焦点在该窗口上，所以验证运行就会失败。该问题在Chrome的弹窗、Chrome打印页面或金蝶K3等窗口比较常见。

<font color=5a6877> 

<br>

【解决办法A3_00007】:

在组件进入录制状态后先按F2，在暂停倒计时时手动点击金蝶K3或Chrome的窗口，这样就会让该软件窗口处于获得焦点的状态，然后等到5秒延迟结束后再录制抓取对应元素即可。运行流程时焦点会自动保持在最新打开的窗口上，按照上述步骤录制的流程就可以正确运行。

 </font><br><br>
 ---
 <br>

#### Q：使用鼠标系列组件拖动窗口滚动条时无法定位或运行成功但未成功滚动，如何处理？

<br>

<font color=5a6877>

 【解决办法A3_00008】:上述场景不建议使用“鼠标拖动”操作滚动条来运行。

<br>

* 桌面应用可以使用组件“鼠标滚动(中键)”、使用“点击”组件点击滚动条的上下按钮或是“发送快捷键”的“{PGDN}”来更好的实现；
* Web页面不需要滚动页面，直接指定要操作的滚动后才显示的元素即可，在运行时会自动定位。

<br>

如果确需使用鼠标拖动组件操作滚动条，则需注意指定的滚动条滑块的位置，即图中框起来的区域：

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/9-1.png"/>


之后设置属性“纵坐标偏移”多少像素才能正确触发滚动操作：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/9-2.png"/>


如果指定到的是整个滚动条或滚动条上非滑块的区域就会出现组件运行成功但页面未滚动的现象。

 </font><br><br>
 ---
 <br>

#### Q：鼠标拖动成功但滚动条只滚动了一点，是怎么回事？

<br>

<font color=5a6877> 

【解决办法A3_00009】:拖动只运行一点可能是因为设置的偏移属性太小，也可能是窗口未全屏导致的，可将要执行拖动的窗口全屏后，再设置大一些的值(如1000像素)即可成功运行。

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/9-2.png"/>

 </font><br><br>
 ---
 <br>

#### Q：输入文本时被输入法拦截导致输入内容发送变化，怎么办？

<br>

<font color=5a6877> 

【解决办法A3_00010】:因为“模拟键盘”是触发key的事件来输入文本的，所以会被系统输入法所阻挡，如果需要以“模拟键盘”的方式输入文本就需要将系统的默认输入法设置为系统自带的“英语(美国) – 美式键盘”，以Win10为例：进入系统设置->打开“时间和语言”->点击“语言”->打开“键盘”，将“替代默认输入法”的选项修改为“英语(美国) – 美式键盘”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/10-1.png"/>


</font><br><br>
 ---
 <br>

#### Q：输入文本组件：运行成功但文本未被成功输入，如何解决？

<br>

<font color=5a6877> 

【解决办法A3_00011】:运行成功是因为组件找到了元素，并根据设置发送了事件，未成功输入说明发送的事件文本未显示到输入框内，可能是指定错了元素或者元素不支持设置焦点。所以首先判断一下指定的元素是否有误，即确保该组件指定的元素是要输入的文本输入框而不是输入框所在的DIV或窗体；在确认无误后可以将“输入方式”改为“模拟键盘”：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/10-2.png"/>


如仍未输入成功可将“输入前行为”改为“点击”：
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/10-3.png"/>


 </font><br><br>
 ---
 <br>

#### Q：输入文本组件：提示“元素无法输入文本”或不能指定的元素时如何处理？

<br>

<font color=5a6877> 

【解决办法A3_00012】:

“输入文本”支持“input”类型的元素，指定非该类型的元素时就会跳出该提示，解决办法是在“输入文本”前添加一个“点击”组件，点击需要输入文本的元素，之后“输入文本”组件不指定元素，将文本填入即可：

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/11-1.png"/>


或是使用“发送快捷键”、“设置剪贴板”等组件操作。
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/11-2.png"/>


 </font><br><br>
 ---
 <br>


#### Q：自动化过程中提示需要“管理员权限”时如何处理？

<br>

<font color=5a6877> 

【解决办法A3_00013】:

Windows下操作很多应用时需要更高级别的应用时需要管理员权限才能做到，比如任务管理器，资源监视器等。要录制、运行这些应用时，需要右键项目名词，之后点击“项目设置”

在弹出的窗口中找到 常规->执行权限->选择“以管理员权限运行”

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/12-1.png"/>


之后关闭编辑器，在编辑器上右键，选择“以管理员身份运行”即可：
<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/12-2.png"/>



 </font><br><br>
 ---
 <br>


#### Q：市场的模拟键盘输入组件输入长字符串会被吞掉一些内容，比如输入123456，运行时变成了23456

<br>
 
<font color=5a6877> 【解决办法A3_00014】:

这种情况一般是应用对输入密码做了特殊处理，可以手动在输入组件前后添加“延迟”组件，设置几秒的延迟；如果添加延迟没有效果，可以将要输入的文本每个字符用一个组件输入，然后在每个组件间添加“延迟”组件，这样就可以完成输入了；如果需要输入的字符串较长时可以添加一个循环，然后依次输入item就可以了。

 
 </font><br><br>
 ---
 <br>

