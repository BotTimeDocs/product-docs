# 网络错误

- 扩展: [BaseError](./baseerror.md)

**针对常见的 Web 自动化异常引发 WebError。**

- [message](#message)
- [stacktrace](#stacktrace)
- [browser_type](#browser_type)


### 消息
- 类型: str

异常消息。


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。

### 浏览器类型
- 类型: str

浏览器的类型。支持的浏览器如下，“IE”，“Chrome”，“Firefox”和“Edge”。