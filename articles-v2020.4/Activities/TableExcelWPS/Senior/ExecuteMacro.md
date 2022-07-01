# 执行宏

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExecuteMacro.mp4"></video>

## 概述

执行外部宏文件或者 XLSM 格式的内部宏，支持实参传递。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **宏名** ：执行宏的方法名。内部宏和外部宏均需填充此项。
- **传入实参** ：传入宏文件的实参。
- **宏文件路径** ：执行此外部宏文件。为空时，默认执行工作表内部宏。

### 输出

- **返回值** ：将宏执行后返回的值存储在此变量，前提为执行宏后有返回值。

## 使用示例

**前置必要组件**：[打开/新建](../../TableExcelWPS/OpenExcel.md)

**此流程执行逻辑**：在 Excel 中执行指定的宏。

![宏文件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro3.png)

![配置执行宏组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/ExecuteMacro1.png)

**执行结果**：
在“输出面板”日志中打印所有 sheet 名称。

## 常见问题

1. **Q：执行宏时报错：“[错误] 执行宏失败。详细错误信息：不信任到 Visual Basic Project 的程序连接。”**

    **A：** 在 Excel 的“选项 > 信任中心 > 信任中心设置 > 宏设置”中，勾选“信任对 VBA 工程对象模型的访问”选项。

    ![Excel 宏](https://docimages.blob.core.chinacloudapi.cn/images/Activities/excelmacro20210824.png)

2. **Q：执行宏时报错：[错误] 执行宏失败。详细错误信息：无法运行“C”宏。可能是因为该宏在此工作簿中不可用，或者所有的宏都被禁用。”**

    **A：** 在 Excel 的“打开/新建”组件中，勾选“启用宏”属性，然后在 Excel 的“选项 > 信任中心 > 信任中心设置 > 宏设置”中，勾选“启用”选项。

3. **Q：一个 xls 文件当前受保护，现知道密码，如何用编辑器解开？打开后需如下步骤解除保护“启用编辑-审阅-保护工作簿-输入密码”**

    **A：** 使用 VBA 录制一个宏，然后工具调用宏，可参见 [vba 录制宏并且工具调运来完成工作簿的保护](https://v.qq.com/x/page/a3268yagt3a.html)，执行宏可参考 [VBA 代码](https://exceloffthegrid.com/vba-code-protect-unprotect-workbooks/)。
