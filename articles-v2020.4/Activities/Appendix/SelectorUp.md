# 选择器改动

新版本编辑器将选择器从项目文件中分离，以便支持不同自动化组件使用相同元素，同时也使选择器更易于维护。

> 如需使用该功能，请将编辑器更新至1.1.2301.01及以上版本 


## 使用说明

### 选择


自动化组件录制元素，完成录制后“选择元素”状态会发生变化，自动创建并关联选择器：


![按钮状态](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0001.png)

    
录制的选择器内容存储在项目路径下的 project.selector中：


![文件路径](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0002.png)


通过选择器ID绑定组件和选择器：


![选择器ID](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0003.png)



### 切换

之后其他想使用相同元素的选择器时，只许点击组件右侧的“选择元素”按钮：


![选择元素按钮](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0004.png)


即可在弹窗中选择使用已有元素，使用方法与使用导入的元素市场一致：


![选择元素弹窗](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0005.png)


同时也支持编辑选择器中的ID直接切换选择器：


![选择器ID](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0003.png)


如已安装其他元素项目，可先点击下拉框切换至“项目元素”后再选择需要使用的元素：

![选择器ID](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector00011.png)


### 修改


支持点击“选择器”属性在选择器窗口中修改,详见[选择器](https://academy.encoo.com/wiki/Activities/Appendix/Selector.md)
    

![选择器窗口](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0006.png)

    
修改完成后可选择是否新建选择器：


![选择器窗口弹窗](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0007.png)


选择“是”时会新建一个选择器，对应一个新的ID；


选择“否”时会修改原有选择器，ID不变；

选择“取消”时会放弃修改的内容返回编辑器。


此外也支持直接编辑project.selector文件，双击或右键打开项目路径下的project.selector文件：


![右键项目](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0008.png)


即可进入到选择器编辑状态，使用方法详见元素市场：

![元素市场窗口](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector0009.png)


### 删除


双击或右键打开project.selector文件，在新标签页中右键点击选择器或文件夹即可删除，使用方法与元素市场一致：


![元素市场删除](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector00010.png)


> 删除已被组件引用的选择器会导致相关组件无法运行，请谨慎操作。


## 注意事项

    1. 暂不支持直接发布项目中的project.selector到元素市场；

    2. 旧版本编辑器创建的项目仍将选择器存储在xaml中，不会受到该功能影响；

    3. 新版本支持原有的base64格式选择器，但仍会将其存储到xaml中。


