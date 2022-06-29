# 打开/新建

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/OpenExcel.mp4"> </video>

## 概述

打开一个 Office Excel 工作簿并为 Excel 组件操作提供范围。

> 说明：
>
> 该组件执行结束时，将关闭指定的工作簿和 Excel 应用程序（如果在属性面板的“输出”; 提供了变量，则组件结束后不会关闭）。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

### 输入

- **密码** ：打开受密码保护的工作簿所需的密码。
- **文件路径** ：要打开或者新建的 Excel 文件全路径（同时支持相对路径）。

### 可选项

- **可视** ：勾选时，工作簿将在可视化状态下进行操作；不勾选时，所有操作将在后台进行，不可见。
- **另存为** ：将操作后的工作簿另存为。

    > **说明：**
    >
    > 若提供的另存为全路径与原路径相同，则直接覆盖重写原工作簿。

- **启用宏** ：实现 Excel 工作簿的“启用宏”效果。
- **新建文件** ：如果在指定路径下找不到工作簿则新建。
- **运行环境**：设置 Excel 的运行模式。

    - 当选择”Office/WPS”时，会使用本地安装的 Office 或 WPS 应用。
    - 当选择 "无依赖" 时，会使用编辑器内部集成的框架运行，即便 PC 未安装 Office 或 WPS 也能运行，但部分高级功能和组件不可用。
  
    > **说明：**
    >
    > Office Excel 中“高级”组件仅支持”Office/WPS”环境运行。

- **只读** ：以只读模式打开指定工作簿。
- **自动保存** ：勾选时，在组件运行内的每次更改都会自动保存工作簿；不勾选时，在该组件运行结束后将不保存更改。

## 使用示例

**此流程执行逻辑**：打开或新建一个 Excel 文档。

![打开或新建组件](https://docimages.blob.core.chinacloudapi.cn/images/Activities/OpenExcel2.png)
