# 日期范围选择

日期范围选择用于一定范围的日期，常用于表单场景。

## 属性

### 基本

- **值**：日期范围选择设置的内容。
  - 开始日期：设置最早日期
  - 结束日期：设置最晚日期

#### 标题

- **标题**：组件标题的显示内容，默认为组件的显示名称。
- **位置**：组件标题的位置：
  - 左：位于组件左侧
  - 上：默认选中，位于组件上方

- **对齐**：标题内容的对齐方式：
  - 左对齐
  - 右对齐
- **宽**：标题的宽度。

> **说明**:
>
>“对齐”和“宽”属性仅在“位置”属性设置为“左”时显示。

### 高级

- **日期区间**：设置可选择的日期范围：
  - 开始日期：可选择的最早日期
  - 结束日期：可选择的最晚日期
- **必填**：开启后，组件为空时提示“必填项”。
- **禁用**：动态控制组件是否禁用。

### 事件

通过单击“**添加事件**”按钮，新增事件和对应动作完成业务逻辑处理，详见[事件处理](./../commonevent.md)。

此组件支持以下事件：

- **值变化**：当日期选择器内的值发生变化后，触发相应业务逻辑。

### 通用

参见 [通用配置项](../general.md)。