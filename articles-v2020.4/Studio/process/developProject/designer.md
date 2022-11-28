# 表达式编辑器

## 概述

表达式编辑器是Encoo Studio的流程设计控件，用于在组件中输入/输出和计算这些表达式的方法。表达式编辑器提供了成熟的IDE编辑体验，包括智能感知、代码着色、方法提示、错误提醒等功能，只需要在输入完成后即可对表达式实时验证。当表达式内容无效时，则会显示错误图标，提示错误的详细信息以便用户及时修改。

表达式支持使用参数或属性的文本值或C#代码。支持变量、常量、文本、属性等直接使用，以及上述内容操作组合后产生新的结果。

> 表达式编辑器中的校验须在焦点离开输入框后被执行

</br>

## 数据类型

表达式功能强大，但基于组件的限制有时会需要使用特定类型的值。

限定的数据类型可在表达式编辑器的弹窗中查看：

![1](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00001.png)

或是将鼠标悬停在组件的属性项上查看：

![2](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00002.png)

## 使用变量/参数

表达式编辑器中可以直接输入变量名来使用变量：

![7](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00007.png)

也可通过点击“fx”键快速创建和选取变量：

![8](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00008.png)

详细的变量使用方法可参考[变量](https://academy.encoo.com/zh-cn/wiki/Studio/process/developProject/Variables/Variables.md)

> 在表达式中输入变量名选中，之后按快捷键 ``Ctrl+B``可以快速创建当前类型的变量。

## 使用数字常量

在表达式中支持直接使用常量：

![9](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00009.png)

## 使用文本常量

在表达式中支持使用文本需要用西文双引号 ``"`` 括起来：

![10](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00010.png)

## 运算符

表达式编辑器中支持使用C#运算符，具体可参阅Microsoft文档 [C#运算符和表达式](https://learn.microsoft.com/zh-cn/dotnet/csharp/language-reference/operators/)

## 组合使用

表达式支持将变量、常量、运算符等内容组合使用，只要结果符合限制规则即可：

![11](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00011.png)

## 使用变量的属性与方法

在表达式内输入内容后，点击 ``.``即可选择支持的方法

![12](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00012.png)

确定后即可执行

![13](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00013.png)

## 西文双引号 ``"``

表达式编辑器中如需在字符中使用西文双引号 ``"`` 时要用两个 ``""`` ：

![3](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00003.png)

或是使用char类型的字符 ``'"'`` 与其他字符串拼接：

![4](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00004.png)

## 换行与制表符

表达式不会对字符串中的换行符和制表符等特殊字符做处理，如需使用需在char类型中使用 ``'\n'``再与字符串进行拼接:

![5](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00005.png)

制表符 ``'\t'``

![6](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00006.png)

## 报错

当表达式编辑器中的内容不符合规则时就会在右上角提示相应的错误

![14](https://docimages.blob.core.chinacloudapi.cn/images/DX/DevGuide/bdsbjq-00014.png)

根据提示修改后即可正常使用。
