# 支持的属性列表

下表列出 IUiObject 元素所支持获取的属性

| 类别 | 属性名 |
| --- | ---|
| <div style="width:40pt"> 桌面 <br>(UIA)</div> |Name, IsEnabled, AccessKey, AutomationId, BoundingRectangle,  ProcessId, LocalizedControlType, ItemType, ItemStatusw, IsPassword, IsOffscreen, AcceleratorKey, HelpText, ClassName, IsKeyboardFocusable, IsContentElement, IsControlElement, HasKeyboardFocus, FrameworkId, ControlTypeStr |
| 桌面 <br>(Java)|Name, Role, BoundingRectangle, States (包含: active, pressed, armed, busy, checked, editable, expandable, collapsed, expanded, enabled, focusable, focused, iconified, modal, opaque, resizable, multiselectable, selectable, selected, showing, visible, vertical, horizontal, singleline, multiline, transient, managesDescendants, indenterminate, truncated), Actions, Selection, Hypertext, Text, TextStr, Value, ValueStr, Table, IndexInParent, IsKeyboardFocusable, IsEditable, IsOffscreen, ProcessId |
| Web |pagetitle, readystate, url, htmlwindowname, title, cookie, innertext, innertextshort, outertext, outertextshort, innerhtml, innerhtmlshort, outerhtml, outerhtmlshort, tag, parentcustomid, ancestorid, ancestorname, ancestorcss, tablerow, tablecol, rowname, colname, columncount, rowcount, ischecked, sinfostate, sinfo, sinfoshort, css_selector, selecteditem, selecteditems, isleaf, isvisible|

## 部分属性名说明

下列列出上述部分属性名的解释说明，其它支持的属性名可以在网页端使用 F12 或使用编辑器中 [元素探测器](../Appendix/UiDetector.md)，查看 DOM 结构。

| 属性名         | 解释说明                                                        |
| -------------- | ------------------------------------------------------------ |
| Pagetitle      | 页面名                                                       |
| ReadyState     | 页面加载状态，Document.readyState === "complete" ?  "1" : "0" |
| Id             | id 属性是元素在网页内的唯一标识符。比如，网页可能包含多个 `<p>` 标签，id 属性可以指定每个 `<p>` 标签的唯一标识符 |
| Url            | 当前网页地址                                                 |
| HtmlWindowName | js 中的 `window.name`                                            |
| Title          | title 属性用来为元素添加附加说明。大多数浏览器中，鼠标悬浮在元素上面时，会将 title 属性值作为浮动提示，显示出来 |
| Cookie         | 网页 cookie 值                                                 |
| InnerText      | 删除特殊字符后的 elem.textContent，表示一个节点及其后代的“渲染”文本内容 |
| InnerTextShort | elem.textContent  512 字以内，表示一个节点及其后代的文本内容 |
| OuterText      | 同 InnerText                                                  |
| OuterTextShort | 同 InnerTextShort                                             |
| InnerHtml      | elem.innerHTML，设置或获取 HTML 语法表示的元素的后代         |
| OuterHtml      | - elem.outerHTML，outerHTML`属性获取描述元素（包括其后代）的序列化 HTML 片段</br>- 它也可以设置为用从给定字符串解析的节点替换元素 |
| OuterHtmlShort | - elem.outerHTML512 字以内，outerHTML 属性获取描述元素（包括其后代）的序列化 HTML 片段</br>- 它也可以设置为用从给定字符串解析的节点替换元素 |
| Tag            | 当前元素的标签名                                             |
| ParentCustomid | 直接父组件的 parentcustomid，没有的情况生成新的               |
| AncestorId     | 向上父节点中第一个有 id 的节点对应的 id 值                       |
| AncestorName   | 向上父节点中第一个有 name 的节点对应的 name 值                   |
| Ancestorcss    | 向上父节点中第一个有 class 的节点对应的 class 值                 |
| TableRow       | 在 table 中的第几行                                            |
| TableCol       | 在 table 中的第几列                                            |
| RowName        | 同行中第一个的 Text                                           |
| ColName        | 同列中第一个的 Text                                           |
| ColumnCount    | 所在 table 的总列数                                            |
| RowCount       | 所在 table 的总行数                                            |
| IsChecked      | checkbox，radio  是否选择                                    |
| SinfoState     | "disabled" 或 "enabled"                                        |
| SInfo          | 特征名（可以理解为是显示的文本）                             |
| SinfoShort     | 返回 512 字以内                                        |
| CssSelector    | 所有父亲节点的和自己的 tag 名组合                             |
| SelectedItem   | option 的第一个选择项 text                                     |
| SelectedItems  | option 的所有选择项 text                                       |
| IsLeaf         | 是否叶子节点                                                 |
| CanInput       | 是否是选择框                                                 |
| CanCheck       | 是否是复选框                                                 |
