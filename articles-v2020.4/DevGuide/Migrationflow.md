# IE流程迁移

微软于今年2月14日正式停止对IE的支持，届时IE浏览器将正常运行，继而基于IE自动化流程也无法继续使用。不过云扩RPA采用的先进自动化技术可以将IE流程快速切换至Edge或其他浏览器上运行，为此，需要做如下的工作：


## 安装扩展

安装并启用浏览器扩展，以Edge浏览器为例，详情可查看[浏览器扩展](https://academy.encoo.com/zh-cn/wiki/Studio/Extensions/EdgeExtension.md)：

![](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/lcqy-00001.png)</br>


## 修改项目文件

进入自动化流程，将流程“**浏览器类型**”为“**IE**”/“**默认**”的修改为其他浏览器，如**Edge**浏览器：

![](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/lcqy-00002.png)</br>

当“浏览器类型”为“默认”时，也可通过右键项目文件进入项目设置，将自动化-浏览器类型从IE修改为Edge：

![](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/lcqy-00003.png)</br>



## 执行流程

完成上述步骤保存并运行，执行时将会拉起修改后的浏览器类型，不再使用IE运行自动化流程，完成浏览器流程替换工作。



> 需注意切换浏览器类型仅支持IE页面在新浏览器中打开时页面、元素未变化，当页面发生变化，或页面采用仅IE支持的特殊技术（如模态框）时，切换后仍需修改、重新录制元素后才能正确运行
