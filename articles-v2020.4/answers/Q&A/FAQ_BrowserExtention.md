# FAQ7：浏览器插件无法启动

#### Q: Chrome, Edge无法启用云扩录制器(启用按钮被浏览器禁用)怎么办？

<img width = '300'  src ="https://docimages.blob.core.chinacloudapi.cn/images/FAQ/browserproblem1.png"/>

#### A: 在部分场景中（如，系统管理员控制，Chrome, Edge浏览器安全级别较高），插件会被误报成恶意软件而无法启动。此时，可选择手动安装 Chrome, Edge扩展以便完成自动化操作

#### Edge浏览器“云扩录制器”修复

> 注意: 说明中的dir1，newId只是方便说明，使用时应根据情况使用实际值

1. 安装完扩展后(已安装可跳过)，打开浏览器扩展扩展管理，删除扩展“云扩录制器”;
2. 找到 %userprofile%\AppData\Local\Encoo\messagehost\chrome\extension 文件夹，复制nbnanilbaelilioikmjahlcehcagkfea_main.crx  重命名为nbnanilbaelilioikmjahlcehcagkfea_main1.rar，解压rar文件到路径 %userprofile%\AppData\Local\Encoo\messagehost\chrome\extension\nbnanilbaelilioikmjahlcehcagkfea_main1，为方便描述，记作dir1;
3. 打开浏览器扩展扩展管理->加载解压缩的扩展，选择文件夹dir1;
4. 加载完后，查看扩展id, 记作newId;
5. 修改 %userprofile%\AppData\Local\Encoo\messagehost\chrome\Clicknium.Web.NativeMessageHost.exe.config  文件，ENABLE_EDGE_EXTENSION_ID  字段的值替换为newId，保存;
6. 修改 %userprofile%\AppData\Local\Encoo\messagehost\chrome\encoorpamsedgemessage.json  文件，
   - 替换allowed_origins 字段中 id 为newId，保存,
   - 替换 chrome_extension_id  字段newId，保存;
7. 修改注册表项，计算机\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\Extensions下的nbnanilbaelilioikmjahlcehcagkfea改为newId
8.重启浏览器

#### Chrome浏览器“云扩录制器”修复

> 注意: 说明中的dir1，newId只是方便说明，使用时应根据情况使用实际值

1. 安装完扩展后(已安装可跳过)，打开浏览器扩展扩展管理，删除扩展“云扩录制器”;
2. 找到 %userprofile%\AppData\Local\Encoo\messagehost\chrome\extension 文件夹，复制hehpjdchdmcgogdililhbfobkmgglhcc_main.crx  重命名为hehpjdchdmcgogdililhbfobkmgglhcc1.rar，解压rar文件到路径 %userprofile%\AppData\Local\Encoo\messagehost\chrome\extension\hehpjdchdmcgogdililhbfobkmgglhcc1，为方便描述，记作dir1;
3. 打开浏览器扩展扩展管理->加载解压缩的扩展，选择文件夹dir1;
4. 加载完后，查看扩展id, 记作newId;
5. 修改 %userprofile%\AppData\Local\Encoo\messagehost\chrome\Clicknium.Web.NativeMessageHost.exe.config  文件，ENABLE_CHROME_EXTENSION_ID  字段的值替换为newId，保存;
6. 修改 %userprofile%\AppData\Local\Encoo\messagehost\chrome\encoorpachromemessage.json  文件，
   - 替换allowed_origins 字段中 id 为newId，保存,
   - 替换 chrome_extension_id  字段newId，保存;
7. 修改注册表项，计算机\HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\Extensions下的hehpjdchdmcgogdililhbfobkmgglhcc改为newId
8. 重启浏览器
