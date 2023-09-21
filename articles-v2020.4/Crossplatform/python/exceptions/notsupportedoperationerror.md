# 不支持操作错误

- 扩展: [NotSupportedError](./notsupportederror.md)

**当该方法由不支持操作类型的 UI 元素调用时，将引发 NotSupportedOperationError。
**

- [message](#message)
- [stacktrace](#stacktrace)
- [automation_tech](#automationtech)
- [control_type](#controltype)
- [operation](#operation)


### 消息
- 类型: str

异常消息。


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。

### 自动化技术
- 类型: str

自动化记录仪技术的类型。支持技术如下：“UIA”、“IA”、“Java”、“IE”、“Chrome”、“Firefox”、“Edge”和“SAP”。

### 控件类型
- 类型: str

目标元素的控件类型。例如：“按钮”，“编辑”，“文档”，“复选框”，“图像”和“图像”是为图像UiElment指定的。
### 操作
- 类型: str

目标元素的操作方法。例如：“点击”、“检查”、“突出显示”。