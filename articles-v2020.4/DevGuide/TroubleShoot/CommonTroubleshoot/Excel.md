# Excel 报错

## 限制条件

- 使用 1.1.2204.9 及之后版本的编辑器/机器人，支持未安装 Excel 和 WPS 时也可使用部分 Excel 组件
- 建议使用官方正版 Excel 或 WPS，Office 2013 以上

## 常见排查步骤

1. **0x80010105**

    【错误信息】：”打开/新建失败，错误代码：0x80010105(RPC_E_SERVERFAULT)“

    【解决办法】：检查是否安装福昕 PDF 阅读器，找到“excel 选项”，点开后点击“加载项”，最下面有个管理加载项的下拉菜单，选“COM 加载项”，点“转到”，这时会弹出一个框，把里面 pdf 软件的加载项前面的勾去掉，点确定；

2. **0x800706BA**

    【错误信息】：”执行宏失败，错误代码：RPC 服务器不可用。 (异常来自 HRESULT: 0x800706BA)“

    【解决办法】：检查宏脚本是否可以在 excel 中手动调用，其次检查宏函数名字是否以譬如 set 等关键字开头；再者，如果某些数据含有特殊字符时在 CSV 转 excel 的情况下，也会出现此问题。

3. **0x80029C4A**

    【错误信息】：加载类型库/DLL 时出错。 (Exception from HRESULT: 0x80029C4A (TYPE_E_CANTLOADLIBRARY))

    【解决办法】：

    - 解决方式一：在注册表中查找 000208D5-0000-0000-C000-000000000046 项 会找到多个，找到一个带有 Typeid 的那个子项，修改 TypeId 的值为{00020813-0000-0000-C000-000000000046} version 为 excel20013 对应的是 1.8, 其他版本可以自己查。修改之后刷新其他项会自动更新。然后查找 00020813-0000-0000-C000-000000000046 项，这个项里面也可以看到 version。保证这个项指定的程序是你电脑上 Excel 的可执行路径就行了
   - 解决方式二：从官方下载 Office 完全卸载工具，链接：<https://support.microsoft.com/zh-cn/office/%E4%BB%8E-pc-%E5%8D%B8%E8%BD%BD-office-9dd49b83-264a-477a-8fcc-2fdf5dbf61d8>

    ![解决办法](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/excel0120220506.png)

   - 解决方式三：使用 Office Tool 工具卸载，链接：Office Tool Plus 官方网站（<https://otp.landian.vip/zh-cn/>）

    ![解决办法](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/excel0220220506.png)

4. **0x80070057**

    【错误信息】：0x80070057 (E_INVALIDARG))

    【解决办法】：检查是否同时安装 wps 和 office，并且将 wps 设置为默认程序，如果是，则卸载 wps 即可；

5. **0x800A03EC**

    【错误信息】：执行宏（0x800A03EC）

    【解决办法】：需要确认一下是不是行号或者列号是不是有错误，也有可能是宏文件本身无法打开或者 VBA 脚本出错

    【错误信息】：打开/新建 HRESULT E_FAIL, Exception from HRESULT: 0x800A03EC

    【解决办法】：导致的原因有多种，一般是由于该 EXCEL 文件的编辑环境发生较大变化，如 64 位系统环境下编辑的 EXCEL 不一定能在 32 位系统环境下顺利读取。

6. **0x80004002**

    【错误信息】：无法将类型为“System.__ComObject”的 COM 对象强制转换为接口类型“Microsoft.Office.Interop.Excel.Worksheet”。此操作失败的原因是对 IID 为“{000208D8-0000-0000-C000-000000000046}”的接口的 COM 组件调用 QueryInterface 因以下错误而失败: 不支持此接口 (异常来自 HRESULT: 0x80004002 (E_NOINTERFACE))。

    【解决办法】：https://www.nowlecture.com/index.php?app = news&mod = Topic&act = view&id = 1102

7. **0x800AC472**

    【解决办法】：关掉”打开/新建“组件属性中的”可视“选项。

8. **0x8001010A**

    【错误信息】：0x8001010A (RPC_E_SERVERCALL_RETRYLATER)

    【解决办法】：参考 [解决办法](https://stackoverflow.com/questions/26073754/error-exception-from-hresult-0x8001010a-rpc-e-servercall-retrylater)。

9. **0x8002000A**

    【错误信息】：excel 超出当前范围。 (异常来自 HRESULT: 0x8002000A (DISP_E_OVERFLOW))

    【解决办法】：定位不到错误行的情况下，可以全选把单元格格式都设为文本

10. **0x8002801D**

    【错误信息】：[错误] 打开/新建失败。详细错误信息：Unable to cast COM object of type 'Microsoft.Office.Interop.Excel.ApplicationClass' to interface type 'Microsoft.Office.Interop.Excel._Application'. This operation failed because the QueryInterface call on the COM component for the interface with IID '{000208D5-0000-0000-C000-000000000046}' failed due to the following error: 库没有注册。 (Exception from HRESULT: 0x8002801D (TYPE_E_LIBNOTREGISTERED)).

    【解决办法】：排查电脑是否安装过 wps，如是，重新安装 wps

11. **0x8007065E**

    【错误信息】： [错误] 打开/新建失败。详细错误信息：Retrieving the COM class factory for component with CLSID {00024500-0000-0000-C000-000000000046} failed due to the following error: 8007065e 这个类型的数据不受支持。 (Exception from HRESULT: 0x8007065E).

    【解决办法】：<https://blog.csdn.net/weixin_34293911/article/details/94269260?ops_request_misc=&request_id=&biz_id=102&utm_term=0x8007065E&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-94269260.nonecase&spm=1018.2226.3001.4187>

12. **0x80004002**

    【错误信息】：无法将类型为“System.__ComObject”的 COM 对象强制转换为接口类型“Microsoft.Office.Interop.Excel.Worksheet”。此操作失败的原因是对 IID 为“{000208D8-0000-0000-C000-000000000046}”的接口的 COM 组件调用 QueryInterface 因以下错误而失败: 不支持此接口 (异常来自 HRESULT: 0x80004002 (E_NOINTERFACE))。

    【解决办法】：参考 [解决办法](https://www.nowlecture.com/index.php?app=news&mod=Topic&act=view&id=1102)。

13. **0x80004005**

    【错误信息】：[错误] 替换失败。详细错误信息：未指定的错误(异常来自 HRESULT: 0x80004005（E_FAIL）)

    【解决办法】：排查一下连接的 Access 数据库是否有权限，正常情况下是没有权限导致

14. **0x8001010A**

    【错误信息】：0x8001010A (RPC_E_SERVERCALL_RETRYLATER)

    【解决办法】：https://stackoverflow.com/questions/26073754/error-exception-from-hresult-0x8001010a-rpc-e-servercall-retrylater

15. **0x80040154**

    【错误信息】：详细错误信息：检索 COM 类工厂中 CLSID 为{00024500-0000-0000-C000-000000000046}的组件失败，原因是出现以下错误：80040154 没有注册类（异常来自 HRESULT: 0x80040154(REGDB_E_CLASSNOTREG))。

    【解决办法】：在操作系统中注册的 COM 组件的多个版本（WPS/Excel）弄乱了，参考 <https://blog.csdn.net/cxygs5788/article/details/106351373?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2.pc_relevant_default&utm_relevant_index=5>

16. **0x800A01A8**

    【错误信息】：[错误] Exception from HRESULT: 0x800A01A8

    【解决办法】：获取文件夹类别，一个个打开 excel 处理完关闭的时候，前面 excel 还没关闭好，进程被占用，前面打开加一个延时

17. **0x8FE3301F**

    【错误信息】：创建透视表失败。详细错误信息：Exception from HRESULT: 0x8FE3301F

    【解决办法】：检查创建透视表范围的列头是否为空，在创建透视表时，必须使用组合为带有标志列列表的数据。如果要更改数据透视表字段的名称，必须键入字段的新名称。

18. **80080005**

    【错误信息】：检索 COM 类工厂中 CLSID 为 {00021A20-0000-0000-C000-000000000046} 的组件时失败，原因是出现以下错误:  80080005

    【解决办法】：参考 [解决办法](https://blog.csdn.net/weixin_30564901/article/details/96374065?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165104533516782395315682%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165104533516782395315682&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-96374065.142^v9^control,157^v4^new_style&utm_term=80080005&spm=1018.2226.3001.4187)。

19. **取消读取单元格内容出现的换行**

    【解决办法】：str.Trim('\n')

20. **写入单元格时如何换行**

    【解决办法】：写入内容输入 +'\n' 就可以换行了

21. **取消工作表密码保护**

    ![解决办法](https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/excel0320220506png.png)

22. **筛选出错: 类 Range 的 AutoFilter 方法无效**

    【解决办法】：这种跟我们组件的全局筛选冲突，: 在 excel 里先取消筛选。

23. **一直卡在删除或写入组件**

    【解决办法】：在”选项 > 信任中心 > 受保护的视图“中，去掉”受保护的视图“

24. **Your stream was neither an OLE2 stream, nor an OOXML stream.**

    【解决办法】：检查源文件是否有问题，比如，重命名过、源文件本身格式不对
