# 变量列表

使用变量列表可以创建和修改变量。

![变量列表](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/createdVariable.png)

|字段| 描述|
|---|---|
|名称（必填）| 变量的名称。 如果不向变量添加名称，则会自动生成一个名称。
|变量类型（必填）| 允许选择变量的类型。可以使用以下选项：</br> Boolean </br> Int32 </br> String </br> Object </br> Array of [T] </br> System.Data.DataTable </br> BotTimeUI.Common.Control.Interface.IUiObject </br> 浏览 .Net 类型 |
|范围（必填）| 变量可用的区域，例如特定组件。</br> 默认情况下，它们在整个项目中可用。|
|默认值（可选）| 变量的默认值。  </br> 如果此字段为空，则使用其类型的默认值初始化变量。例如，对于 Int32，默认值为 0。 |

> **注意：**
>
> 1. 变量的范围若设置为局部，只是提示该变量存在于当前范围内，但变量名需要保持全局唯一性。
>
> 2. 变量的名称不可使用系统保留字。例如：add、delete 等。

## 变量上下文菜单

![菜单](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Variable/variablePanelMenu.png)

|字段| 描述|
|---|---|
|删除 |将变量从列表中删除，但不从流程中删除。|
|添加批注| 打开“添加批注”窗口，为变量添加注释。|
|编辑批注 |打开“添加批注”窗口，对已有的注释进行更改。|
|删除批注| 删除为变量添加的注释。|
