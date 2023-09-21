# WindowsNativeError

- 扩展: [WindowError](./windowerror.md)

**WindowsNativeError 在 winneath 32 方法失败时引发。**

- [message](#message)
- [stacktrace](#stacktrace)
- [name](#name)
- [native_errorcode](#native_errorcode)

### 消息
- 类型: str

异常消息。


### 堆栈跟踪
- type: str

一个字符串，表示引发异常的函数之前的所有调用。

### 名字
- 类型: str

Win32 本机 API 名称。


### native_errorcode
- 类型: str

Win32 本机错误代码。