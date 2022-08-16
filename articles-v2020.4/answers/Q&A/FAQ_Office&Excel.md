# FAQ3：Excel自动化


#### Q：删除失败或写入组件失败，一直卡在删除或写入区域/写入单元格组件

<br>

<font color=5a6877> 【解决办法A_400001】：去掉保护

 </font><br><br>
 ---
 <br>

#### Q：写入公式,单元格的格式是文本(其实是带了'),导致需要双击下单元格确认格式才能生效

<br>

<font color=5a6877> 【解决办法A_400002】：可以先设置格式在插入,或者把插入的那一列改为数值格式,或者用执行宏

 </font><br><br>
 ---
 <br>

#### Q：写入区域卡死

<br>

<font color=5a6877> 【解决办法A_400003】:某些数据含有特殊字符,比如CSV转excel的情况下


 </font><br><br>
 ---
 <br>

#### Q：Excel/WPS组件：读取单元格内容，出现换行？

<br>

<font color=5a6877> 【解决办法A_400004】:str.Trim('\n')

 </font><br><br>
 ---
 <br>

#### Q：Excel/WPS组件：写入单元格怎么换行？

<br>

<font color=5a6877> 【解决办法A_400005】:写入内容输入 +'\n' 就可以换行了

 </font><br><br>
 ---
 <br>

#### Q：Excel/WPS组件：如何取消工作表密码保护

<br>

<font color=5a6877> 【解决办法A_400006】:如下所示

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/7-1.png"/>


 </font><br><br>
 ---
 <br>
 
#### Q：Excel/WPS组件：如何关闭数据链接更新提示弹窗？

<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/7-2.png"/>

<font color=5a6877> <br><br><br>【解决办法A_400007】: 选择 Excel选项>> 高级>> 常规>>请求自动更新<br>

<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/7-3.png"/>


<img width = '400'  src ="https://docimages.blob.core.chinacloudapi.cn/images/troubleshoot/8-1.png"/>

 </font><br><br>

 <br>
