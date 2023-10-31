# 不支持操作选项错误

- 扩展: [NotSupportedOperationError](./notsupportedoperationerror.md)

**当目标 UI 元素不支持指定的选项值时，将引发 NotSupportedOperationOptionError。
**

## 构造函数
- [message](#message)
- [stacktrace](#stacktrace)
- [automation_tech](#automationtech)
- [control_type](#controltype)
- [operation](#operation)
- [option](#option)


### 消息
- 类型: str

异常消息。


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。

### 自动化技术
- 类型: str

自动化记录仪技术的类型。支持的记录器技术如下“UIA”，“IA”，“Java”，“IE”，“Chrome”，“Firefox”，“Edge”和“SAP”。

### 控件类型
- 类型: str

目标元素的控件类型。例如：“按钮”、“编辑”、“文档”、“复选框”、“图像”和“图像”是为图像 UiElement 指定的。

### 操作
- 类型: str

目标元素的操作方法。例如：“点击”、“检查”、“突出显示”。

### 选择
- 类型: str

操作的选项。例如：“设置文本”是“clear_text”操作的“by”的选项。