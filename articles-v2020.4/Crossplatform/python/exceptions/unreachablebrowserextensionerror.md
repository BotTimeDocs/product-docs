# 无法访问浏览器扩展错误

- 扩展: [WebError](./weberror.md)

**当指定的浏览器的扩展未处于就绪状态时，将引发无法访问的浏览器扩展错误。请确保已安装并启用该扩展。
**

- [message](#message)
- [stacktrace](#stacktrace)
- [browser_type](#browser_type)


### 消息
- 类型: str

异常消息。


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。

浏览器类型
- 类型: str

浏览的类型。支持的浏览器如下，“IE”，“Chrome”，“Firefox”和“Edge”。