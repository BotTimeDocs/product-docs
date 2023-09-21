# 不支持错误

- 扩展: [BaseError](./baseerror.md)

**当不支持调用的方法时，或者当尝试读取、查找或写入不支持调用功能的流时，将引发 NotSupportedError。
**

- [message](#message)
- [stacktrace](#stacktrace)


### 消息
- 类型: str

异常消息


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。