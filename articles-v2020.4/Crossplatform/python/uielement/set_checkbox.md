# set_checkbox
```python
def set_checkbox(
        self,
        check_type: Literal["check", "uncheck", "toggle"] = CheckType.Check,
        timeout: int = 30
    ) -> None
```  

设置复选框控件的检查状态。

**参数:**  
    &emsp;**check_type**: str | CheckType   
        &emsp;&emsp;  检查操作类型：“检查”、“取消选中”或“切换”。 
    &emsp;**timeout**: int  
        &emsp;&emsp; 操作超时，单位为秒，默认值为 30 秒。

**返回:**  
    &emsp;None