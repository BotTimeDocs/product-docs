# Error6：打开流程报错

<br>


#### Q：在编辑器打开流程时报错

<font color=5a6877>
<br>

**【错误信息】：**
找不到方法：”System.String BotTimeUI.Common.Control.Interface.IControlFactory.ToSelectorMetaData(BotTimeUI.Common.Control.Interface.IUiObject,BotTimeUI.Common.Model.GetMetaDataAdditionalInfo,System.String ByRef,System.String ByRef)“.
</font>

<font color=5a6877>
<br>

**【原因分析】**：当前编辑器版本低于开发此流程时使用的编辑器版本
<br>
**【解决办法】**：

* 方法1（推荐）：将编辑器升级到最新版本。
* 方法2：尝试删除目录%userprofile%\.nuget\packages下以encoo和bottime开头的文件夹后，重启编辑器。

</font>
<br><br>
