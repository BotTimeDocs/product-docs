# Java扩展 
**Jave扩展**适用于Java1.6及以上应用程序的自动化。

对于使用Java 9+ JRE 打开的应用程序：
在Java 9之前，JRE会包含attach模块，Java扩展依赖其对Java程序进行自动化。对于Java 9+，attach模块仅包含在JDK中，所以对于使用JRE9+打开的程序，需要手动在JRE目录下添加此模块。

## 常见问题  
1. 提示找不到32位/64位的Java运行环境

    Encoo找不到公共Java运行环境初始化Java扩展，需要按提示安装32位或64位的JRE。可以到以下地址下载对应版本的Java：<https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html>

    a）点击 Accept License Argument

   ![接受许可协议](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-acceptLicenseArguments.png)

    b) 按Encoo提示点击下载32位或64位的Java（x86为32位，x64为64位）

   ![下载java](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-downloadJava.png)

 2. 对于Java Applet应用或无法attach的应用，需要手动安装Java扩展到runtime目录

    a) 找到Studio或Robot安装目录下的JavaSupport文件夹

    ![查找JavaSupport文件夹](https://docimages.blob.core.chinacloudapi.cn/images/Studio/Extensions/java-javaSupport.png)

    >**说明：**
    >
    > 1.1.2009.X及之后的版本为安装目录下的Extensions\Java文件夹。

    b) 将JavaSupport文件夹中accessibility.properties复制到runtime的\lib目录下

    将JavaSupport文件夹中BotTimeJavaBridge.jar复制到runtime的\lib\ext目录下
    
    然后将BotTimeJavaBridge-*.dll和BotTimeJAWTBridge-*.dll复制到runtime的\bin\目录下。（视runtime为32或64位复制相应后缀的dll）
     
     >**说明：**
     >
     > 1.1.2009.X及之后的版本:
     > 将文件夹中accessibility.properties复制到runtime的\lib目录下，将文件夹中BotTimeJavaBridge.jar复制到runtime的\lib\ext目录下，然后将BotTimeJavaBridge-.dll和BotTimeJAWTBridge-.dll复制到runtime的\bin\目录下。

    |BotTime扩展文件|目标路径|
    |---|---|
    |BotTimeJavaBridge-32/64.dll|%JAVAHOME%\bin|
    |BotTimeJAWTBridge-32/64.dll|%JAVAHOME%\bin|
    |accessibility.properties|%JAVAHOME%\lib|
    |BotTimeJavaBridge.jar|%JAVAHOME%\lib\ext|
    |jaccess.jar|%JAVAHOME%\lib\ext|
