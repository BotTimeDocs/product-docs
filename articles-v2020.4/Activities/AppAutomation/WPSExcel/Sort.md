# 排序

对某列进行排序，提供&quot; 升序，降序&quot; 两种排序模式。工作表内所有行数据随之改变

## 属性

### 基本

- **显示名称** ：默认为该组件的名称。支持更改，用户自定义此组件的显示名称
- **失败后继续** ：设置当此组件运行失败时，是否忽略此错误继续运行下一个组件。下拉框选择，当选择 "是" 时，如果该组件运行时遇到错误，该流程也会继续执行下一个组件，并不会停止；当选择 "否" 时，如果该组件运行时遇到错误，该流程将会停止执行并抛出错误
- **前延时(毫秒)** ：指定在此组件执行前的等待时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为上一个组件执行完毕后，等待一秒钟后执行此组件
- **后延时(毫秒)** ：指定在此组件执行后的延迟时间。单位为毫秒（ms）,1000ms = 1s。若此处填写 1000，意为此组件执行完毕后，等待一秒钟后执行下一个组件

### 输入

- **工作表** ：执行排序的目标工作表。仅支持字符串变量和字符串
- **列号** ：对此列进行排序操作。填入列索引（例：1，即对第一列进行排序）。仅支持整型变量和整型
- **顺序** ：下拉框选择排序模式为升序或降序

## 操作样例

1. 新建一个 Excel 文件，在 A1: B7 处填入需要被读取的值:

    ![1](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)

2. 拖入 **打开/新建** 组件，不勾选新建文件，再填入需要打开的 Excel 文件路径:

    ![2](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps5.png)

3. 双击 **打开/新建** 组件，拖入 **排序** 组件至 **打开/新建** 组件中，填写工作表和列号，设置排序规则为降序:

    ![3](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps24.png)

4. 点击流程运行，观察运行结果:

    ![4](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps25.png)

5. 将流程中 **排序** 组件的排序规则设置排序规则为升序:

    ![5](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps26.png)

6. 再次点击流程运行，观察运行结果:

    ![6](https://docimages.blob.core.chinacloudapi.cn/images/Activities/wps9.png)
