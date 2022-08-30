# 选择器

点击**选择器**属性右侧的按钮，弹出下述界面。用户可在此窗口查看所指定元素的详细信息，同时提供编辑功能，用户可以自定义指定元素信息

![img](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector001.png)

## 图像预览页

此区域仅在使用图像识别方式指定元素时会显示，显示的是指定元素的截图。

## 选择器编辑窗口

此区域中，你可以看到和选中元素相关的所有节点和属性信息。你可以对相关信息进行编辑。

使用时请注意：
- 首行 **Application AutomationType=...**：固定不可更改，保存目标应用进程信息，用来定位目标应用程序进程。
- 复选框：选中状态，表示应用此节点信息来定位指定元素；非选中状态，表示不应用此节点信息来定位指定元素。
- 当使用图片识别的方式指定元素时，**Image** 标签会固定于最后一行，其上的节点信息用来定位锚点元素。
- 属性：通过下拉框可以更改属性名，同时下拉框右侧的文本框可以填写属性值。
  
    - 属性名：指定元素后，优先生成和使用页面Title来定位元素，如果页面Title未设定，则使用URL来定位页面，并且可以在属性列表中选择Name、Title、Role、URL等属性进行更换。选择器支持的属性列表请参见[支持的属性列表](https://academy.encoo.com/zh-cn/wiki/Activities/Appendix/SupportedAttribute.md?uuid=b1d2d88d-5322-469b-9df0-939db05d256a)
    - 属性值：支持填写变量（请参见[支持变量的属性](Activities/../SupportedVariableName.md)）和常量，并且AutomationId/ClassName/Name这些属性的值支持通配符。
      
      >**说明：**
      >
      >- 当属性值为变量时，格式为：{VariableName}或{{VariableName}}，即将变量写在花括号里面。
      >- 在index属性中使用
      >- 当属性值为常量、变量混合时，常量的格式为:{VariableName}，变量的格式为：{{VariableName}}且变量需要在编辑器中定义，否则为常量。如，/html/body/div[4]/div/div/div[2]/table/tbody//td[@data-value="**{{dateddd}}**"]，这一串常量变量混合的情况，加粗字体为变量的写法。
      >- 选择器不支持直接使用变量拼接运算符，会将其视为字符串，如{VariableName}+1。如需拼接运算符可在拼接后再赋值给选择器中的变量。
- 删除节点或属性：将节点或属性前的复选框状态改为不选即可

## 指定元素按钮

使用指定元素按钮，你可以指定选择器选中的元素。

## 验证按钮

使用验证按钮，你可以对已选中的元素信息进行验证，确认这些信息能否成功定位元素。

>**说明：**
>
>支持验证属性值为变量（有默认值）的情况。

## XPath 选项

如果你希望使用 XPath 的形式对元素进行描述，而非使用默认的节点和属性的方式，你可以勾选 *生成 XPath* 选项，然后使用指定元素按钮，重新指定元素。

指定完成后，你可以获得对应元素的 XPath 表达式。编辑器提供了多种表达式的写法，包含在 XPath 列表中：

![img](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/selector002.png)

>**说明：**
>
>XPath 选项只支持 Web 元素。</br>
>更多选择器的高级用法请参见[高级开发技巧](https://academy.encoo.com/zh-cn/wiki/DevGuide/AdvancedDevelopment.md)
