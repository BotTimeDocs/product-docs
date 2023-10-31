# 浏览器不安装错误

- 扩展: [WebError](./weberror.md)

**浏览器不安装错误在未安装指定的浏览器时引发。**

- [message](#message)
- [stacktrace](#stacktrace)
- [browser_type](#browser_type)


### 消息
- 类型: str

异常消息


### 堆栈跟踪
- 类型: str

一个字符串，表示引发异常的函数之前的所有调用。

### browser_type
- 类型: str

浏览器的类型。支持的浏览器如下，“IE”，“Chrome”，“Firefox”和“Edge”。