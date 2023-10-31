# 屏幕操作错误

- 扩展: [WindowsNativeError](./windowsnativeerror.md)

**当 Windows 桌面 UI 元素的屏幕操作失败时，将引发屏幕操作错误。
**

- [message](#message)
- [stacktrace](#stacktrace)
- [name](#name)
- [native_errorcode](#native_errorcode)

### 消息
- 类型: str

异常消息


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。

### 名字
- 类型: str

Win32 本机 API 名称。


### 本机错误代码
- 类型: str

Win32 本机错误代码。
