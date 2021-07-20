# 写入区域

写入数据表数据到工作表

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延迟(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延迟(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **工作表** ：写入数据表数据的目标工作表。若指定工作表不存在则自动新建。仅支持字符串变量和字符串
- **起始单元格** ：数据表数据开始写入的单元格地址。若为单元格地址，则从指定单元格为起始写入数据表；若为单元格区域，则只填充数据到指定区域。仅支持字符串变量和字符串
- **数据表** ：写入工作表内的数据表数据。可传入&quot; 读取区域&quot; 的输出变量，实现复制粘贴效果。仅支持数据表变量

### 可选项

- **添加列头** ：勾选时，数据表列头也将写进工作表

## 使用示例

1. 拖入 **打开/新建** 组件，勾选是否新建文件，再填入需要打开或者新建的 Excel 文件，并配置所需选项内容:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps1.png)

2. 双击 **打开/新建** 组件，拖入 **搭建数据表** 组件，并点击 "点击打开'数据表搭建器'" 设置数据表内容，将数据表输出到变量:
    ![2-1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps46.png)

    ![2-2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps47.png)

    ![2-3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps48.png)

3. 拖入 **写入区域** 组件，配置工作表名称、起始单元格位置以及输入的数据表(类型为 datatable)，右边配置选项中可以勾选是否添加列头，如果勾选则会将 datatable 的列名称也写入到 excel 中，反之则不会写入:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps49.png)

4. 点击流程运行，观察运行结果:

    ![4](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps50.png)
