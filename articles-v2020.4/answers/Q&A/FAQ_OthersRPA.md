# FAQ4：其它_流程开发问题

#### Q：2022年7月 新版本发布后 为什么没有引用项目 这个选项？

 <br>

<font color=5a6877> 【解决办法A5_00001】: 

至2022年7月 新版本发布
7月新版本编辑器，合并了组件项目及前期引用项目的用法，通过创建一个组件项目，并将其发布到组件市场，在其他项目中进行使用(而不是仅限于单个项目引用) ，具体详见文档：[《创建组件项目》](https://academy.encoo.com/zh-cn/wiki/Studio/process/CreateProject/CreateLibrary.md?uuid=4f2d5853-ffb5-45e0-85e2-4decc0dd15d7)


如何将流程发布成组件 可以看文档：[《如何将流程发布成组件》](https://academy.encoo.com/zh-cn/wiki/BestPractices/workflow-activity.md?_v=v2020.4&uuid=1b1ab067-7487-4efe-b35a-5dfdc6638847)

2022年7月之后的版本 界面上目前不支持，已开发的流程 若想要引用，具体操作步骤可见文档：[《【技术方案】(旧版本创建好的流程项目) "引用项目"在 2206.10之后的编辑器使用》](https://c9vrjkv7og.feishu.cn/docx/doxcnd7y9aDxQNC9RI2Uzxj78Wg)


 </font><br><br>
 ---
 <br>

#### Q：屏幕解锁，设置了对应的解锁组件，但是不生效 ？

<br>

<font color=5a6877> 【解决办法A5_00002】: 

* 排查方法一：尝试通过组件进行锁屏，即在流程中配对使用锁屏与解锁组件。目前已知在个别特殊环境下，手动锁屏时解锁组件无法正常解锁，但通过组件锁屏时能够正常解锁。

* 排查方法二：在“控制面板 > 系统与安全 > 管理工具 > 本地策略”下找到“交互式登录：无需按 Ctrl+Alt+Del”这一项，勾选“已启用”项。

 </font><br><br>
 ---
 <br>


#### Q：市场组件如何重命名？
<br>

<font color=5a6877>
<br>**【解决办法-A5_00003】**：可以双击更改

</font>
<br><br>
---
<br> 

#### Q：如何设置编辑器成英文版本
<br>

<font color=5a6877>
<br>**【解决办法-A5_00004】**：切换成英语版本：
`%userprofile%\AppData\Local\Encoo Studio\app-1.1.2111.6`（编辑器安装目录）
下的Encoo.Studio.exe.Config
zh-CN 改成 en-US

</font>
<br><br>
---
<br> 

#### Q：元素录制的时候，xpath录制会不会相对来说比较稳定？
<br>

<font color=5a6877>
<br>**【解决办法-A5_00005】**：

xpath和自动生成的选择器的区别其实只是定位的“标准”不同，xpath是通过元素的位置，自动生成的选择器一般是元素的属性。如果要避免因元素变化导致的识别失败的话，这时候要去分析元素变得是什么，如果是位置经常变化，那xpath就不一定适用了。如果位置不变，但属性经常变化，那可能xpath会更适合一些
</font>
<br><br>
---
<br> 

#### Q：文本框中自动输入时间的时候出现乱码

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A_500006.png"/>



<br>

<font color=5a6877>
<br>**【解决办法-A5_00006】**：

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

【解决办法-A5_00007】

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

【解决办法-A5_00008】：远程桌面不能最小化必须窗口化

</font>
<br><br>
---
<br> 

#### Q：查询sql，查询语句如何传参？
请问数据库连接操作里，union的查询sql应该怎么配置？查询条件要外面传入的。我看查询语句组件好像不支持传参。
可以参数写成{0}，然后跟在sql后面写参数变量吗

<br>

<font color=5a6877>
<br>

【解决办法-A5_00009】：支持填写参数/变量的 ，以拼接的方式实现

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/A_500009.png"/>


</font>
<br><br>
---
<br> 
