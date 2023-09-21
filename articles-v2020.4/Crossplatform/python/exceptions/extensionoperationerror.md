# 扩展操作错误

- 扩展: [BaseError](./baseerror.md)

**当扩展在操作“安装”、“更新”或“卸载”中失败时，会引发扩展操作错误。**

- [message](#message)
- [stacktrace](#stacktrace)
- [extention_type](#extention_type)
- [operation](#operation)

### 消息
- 类型: str

异常消息。

### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。


### 扩展类型
- 类型: str

扩展的类型。

### 操作
- 类型: str

扩展的操作。