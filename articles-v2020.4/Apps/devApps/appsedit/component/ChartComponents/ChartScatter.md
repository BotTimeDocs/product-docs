# 散点图

散点图是指回归分析中，数据点在直角坐标系平面上的分布图，表示的是因变量随自变量变化的大致趋势。如使用散点图展示各商品类别销售计划和实际销售金额的变化趋势。

## 属性

### 配置

- **图表名称**：自定义图表的名称。
- **描述**：对自定义的图表的说明。
- **数据源**：通过编写表达式，设置散点图中数据的来源。
- **x 轴**：可选择一个属性的数据作为 x 轴坐标轴。
- **y 轴**：可选择一个属性的数据作为 y 轴坐标轴。
- **统计字段**：从数据源中选择一个需要进行统计操作的字段。
- **颜色**：图例的颜色。
- **标签**：是否在每个散点上显示标签值。
- **四象限**：是否展示四象限散点图。
- **气泡样式**：是否将图中的实心小圆点以空心气泡的样式展示。
- **趋势线**：是否在图中以指定的计算方式展示趋势线。
- **边距**：勾选“外边距”后，可调整该组件距离上下左右外边框的距离。
- **高**：设置组件的高度。

### 样式

- **隐藏**：组件显示还是隐藏。
- **禁用**：组件禁用还是启用。
- **样式**：可选择“默认样式”，当调整字体、外观、边距时自动显示为“自定义样式”。
- **文字**：设置组件的字体大小、颜色、样式及格式。
- **外观**：设置组件的外观样式。
- **鼠标手势**：当鼠标悬停于该组件上时，显示的鼠标光标的形状。
  
    鼠标手势选项 | 描述
    ---------|----------
    default | 默认光标（通常是一个箭头）。
    text | 此光标指示文本。 
    pointer | 光标呈现为指示链接的指针（一只手）。
    not-allowed | 禁止标记(一个被斜线贯穿的圆圈)光标。用于标示请求的操作不允许被执行。
    help | 此光标指示可用的帮助（通常是一个问号或一个气球）。
    move | 此光标指示某对象可被移动。
    progress | 带有沙漏标记的箭头光标。用于标示一个进程正在后台运行。
    grab | 光标呈现为一只手的形状，表示可以抓取某些东西。
    grabbing | 光标呈现为一只手的形状，表示可以抓取住某些东西。
    e-resize | 此光标指示矩形框的边缘可被向右（东）移动。
    n-resize | 此光标指示矩形框的边缘可被向上（北）移动。
    ne-resize | 此光标指示矩形框的边缘可被向上及向右移动（北/东）。
    nw-resize | 此光标指示矩形框的边缘可被向上及向左移动（北/西）。
    none | 没有为元素呈现光标。

- **透明度**：设置该组件的透明度，值越低越透明。

## 示例

1. 进入 **应用开发** 的编辑模式。
2. 从左侧组件面板中选择 **图表组件** 下的 **散点图** 组件，拖拽至画布中。
3. 选中该组件，在右侧属性栏为该组件配置如下属性。

    - 图表名称：自定义图表的名称，如，“散点图”。
    - 数据源：编写一段数据源的数据，如，
  `[{"H/A":"A","Team":"Torino","xG conceded":0.62,"Shot conceded":10,"Result":"3"},{"H/A":"H","Team":"Atalanta","xG conceded":2.35,"Shot conceded":23,"Result":"1"},{"H/A":"A","Team":"Milan","xG conceded":1.89,"Shot conceded":26,"Result":"0"},{"H/A":"H","Team":"Chievo","xG conceded":1.4,"Shot conceded":13,"Result":"1"},{"H/A":"A","Team":"Bologna","xG conceded":1.02,"Shot conceded":11,"Result":0},{"H/A":"H","Team":"Frosinone","xG conceded":0.56,"Shot conceded":11,"Result":"3"},{"H/A":"H","Team":"Lazio","xG conceded":1.01,"Shot conceded":16,"Result":"3"},{"H/A":"A","Team":"Empoli","xG conceded":1.56,"Shot conceded":20,"Result":"3"},{"H/A":"H","Team":"Spal","xG conceded":1.8,"Shot conceded":6,"Result":"0"},{"H/A":"A","Team":"Napoli","xG conceded":2.49,"Shot conceded":26,"Result":"1"},{"H/A":"A","Team":"Fiorentina","xG conceded":1.3,"Shot conceded":14,"Result":"1"},{"H/A":"H","Team":"Sampdoria","xG conceded":1.2,"Shot conceded":8,"Result":"3"},{"H/A":"A","Team":"Udinese","xG conceded":1.22,"Shot conceded":9,"Result":"0"},{"H/A":"H","Team":"Inter","xG conceded":2.68,"Shot conceded":17,"Result":"1"},{"H/A":"A","Team":"Cagliari","xG conceded":2.1,"Shot conceded":16,"Result":"1"},{"H/A":"H","Team":"Genoa","xG conceded":1.84,"Shot conceded":15,"Result":"3"},{"H/A":"A","Team":"Juventus","xG conceded":2.12,"Shot conceded":20,"Result":"0"},{"H/A":"H","Team":"Sassuolo","xG conceded":0.72,"Shot conceded":10,"Result":"3"},{"H/A":"A","Team":"Parma","xG conceded":0.58,"Shot conceded":6,"Result":"3"},{"H/A":"H","Team":"Torino","xG conceded":1.87,"Shot conceded":10,"Result":"3"},{"H/A":"A","Team":"Atalanta","xG conceded":2.68,"Shot conceded":23,"Result":"1"},{"H/A":"H","Team":"Milan","xG conceded":0.85,"Shot conceded":8,"Result":"1"},{"H/A":"A","Team":"Chievo","xG conceded":0.84,"Shot conceded":16,"Result":"3"},{"H/A":"H","Team":"Bologna","xG conceded":2.69,"Shot conceded":20,"Result":"3"},{"H/A":"A","Team":"Frosinone","xG conceded":1.51,"Shot conceded":11,"Result":"3"},{"H/A":"A","Team":"Lazio","xG conceded":1.77,"Shot conceded":13,"Result":"0"},{"H/A":"H","Team":"Empoli","xG conceded":0.14,"Shot conceded":5,"Result":"3"},{"H/A":"A","Team":"Real Madrid","xG conceded":3.58,"Shot conceded":30,"Result":"0"},{"H/A":"H","Team":"Viktoria Plzen","xG conceded":0.33,"Shot conceded":7,"Result":3},{"H/A":"H","Team":"CSKA Moscow","xG conceded":0.73,"Shot conceded":13,"Result":"3"},{"H/A":"A","Team":"CSKA Moscow","xG conceded":1.1,"Shot conceded":14,"Result":"3"},{"H/A":"H","Team":"Real Madrid","xG conceded":1.87,"Shot conceded":12,"Result":"0"},{"H/A":"A","Team":"Viktoria Plzen","xG conceded":1.85,"Shot conceded":13,"Result":"0"},{"H/A":"A","Team":"Porto","xG conceded":3.71,"Shot conceded":31,"Result":"0"},{"H/A":"H","Team":"Porto","xG conceded":0.56,"Shot conceded":7,"Result":"3"}]`
     - x 轴：选择可以作为 x 轴显示的字段，如，`xG conceded`。
     - y 轴：选择可以作为 y 轴显示的字段，如，`Shot conceded`。
     - 统计字段：选择需要进行统计的字段，如，`Result`。

4. 单击 **预览** ，查看应用效果。

    ![应用效果](https://docimages.blob.core.chinacloudapi.cn/images/Kris/Apps/chartscatter20210604.png)
