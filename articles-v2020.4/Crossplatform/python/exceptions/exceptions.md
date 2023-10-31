# 异常

每当某个操作异常终止时，都会引发异常。除了python内置异常 [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html#built-in-exceptions), 我们还定义了 [BaseError](./baseerror.md)，它们都继承自BaseError。


## 点击异常 

| 异常      | 描述 |
| -----------| ----------- |
| [BaseError](./baseerror.md) |所有 Clicknium 异常都继承自此类。|
| [ArgumentError](./argumenterror.md) | 当提供给方法的至少一个参数无效时，将引发 ArgumentError。|
| [ArgumentNullError](./argumentnullerror.md) | 当将空引用传递给不接受其作为有效参数的方法时，将引发 ArgumentNullError。|
| [ArgumentOutOfRangeError](./argumentoutofrangeerror.md) |当参数的值超出调用方法定义的允许值范围时，将引发 ArgumentOutOfRangeError。|
| [BrowserNotInstallError](./browsernotinstallerror.md) |浏览器不安装错误在未安装指定的浏览器时引发。|
| [BrowserNotRunError](./browsernotrunerror.md) | 当指定的浏览器未运行时，将引发浏览器不运行错误。|
| [ExtensionOperationError](./extensionoperationerror.md) | 当扩展在操作“安装”、“更新”或“卸载”中失败时，会引发扩展操作错误。|
| [InvalidOperationError](./invalidoperationerror.md)   | 当方法调用对对象的当前状态无效时，将引发 InvalidOperationError。|
| [InvalidSelectedItemError](./invalidselecteditemerror.md)   | 当要选择的项对于对象的当前状态无效时，将引发 InvalidSelectedItemError。|
| [LocatorRequestError](./locatorrequesterror.md) | 当由于服务器请求错误而无法获取云定位器时，将引发定位器请求错误。|
| [LocatorUndefinedError](./locatorundefinederror.md) | 在定位器存储中找不到指定的定位器时，将引发定位器未定义错误。|
| [NotSupportedError](./notsupportederror.md) |当不支持调用的方法时，或者当尝试读取、查找或写入不支持调用功能的流时，将引发 NotSupportedError。 |
| [NotSupportedOperationError](./notsupportedoperationerror.md) | 当该方法由不支持操作类型的 UI 元素调用时，将引发 NotSupportedOperationError。|
| [NotSupportedOperationOptionError](./notsupportedoperationoptionerror.md)   | 当目标 UI 元素不支持指定的选项值时，将引发 NotSupportedOperationOptionError。|
| [OperationTimeoutError](./timeoutoperationerror.md) | 当某个操作未在给定时间内完成时，将引发操作超时错误。|
| [ProjectSettingNotFoundError](./projectsettingnotfounderror.md) | 项目设置未发现错误在项目设置文件时引发 `clicknium.yaml` 丢失|
| [ScreenOperationError](./screenoperationerror.md)   | 当 Windows 桌面 UI 元素的屏幕操作失败时，将引发屏幕操作错误。|
| [UiaPatternNotFoundError](./uiapatternnotfounderror.md)   | 当UIA技术找不到窗口UI元素时，会引发UiaPatternNotFoundError。|
| [UnAuthorizedError](./unauthoriederror.md) | 当用户未登录或登录状态已过期时，将引发未授权错误。|
| [UnreachableBrowserExtensionError](./unreachablebrowserextensionerror.md) | 当指定的浏览器的扩展未处于就绪状态时，将引发无法访问的浏览器扩展错误。请检查扩展是否已安装并启用。|
| [WebElementNotRespondingError](./webelementnotrespondingerror.md) | WebElementNotRespondingError在网页没有响应时引发。|
| [WebError](./weberror.md) | 针对常见的 Web 自动化异常引发 WebError。|
| [WindowError](./windowerror.md)   |对于常见窗口异常，将引发窗口错误。|
| [WindowsNativeError](./windowsnativeerror.md)   | WindowsNativeError 在 winneath 32 方法失败时引发。|


