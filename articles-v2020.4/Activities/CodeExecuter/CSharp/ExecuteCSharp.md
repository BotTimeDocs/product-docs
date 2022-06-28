# 执行 C# 代码

## 视频示例

<video controls height='100%' width='100%' src="https://encooacademy.oss-cn-shanghai.aliyuncs.com/activity/ExecuteCSharpCode.mp4"></video>

## 概述

提供 C# 代码编辑器，支持编写 C# 类、函数等基本代码，并可直接使用编辑器中定义的变量，无需进行编辑器和 C# 代码编辑器之间的参数传递。也支持在 C#代码中通过引用命名空间直接调用 OfficeExcel。

> **小技巧：**
>
> 将项目面板中的 C#代码文件（扩展名为.cs）拖拽至编辑区域，将自动生成“执行 C#代码”组件。

## 属性

### 基本

参见 [通用配置项](../../Appendix/CommonConfigurationItems.md)。

## 使用示例

**此流程执行逻辑**：在“C#代码编辑器”中打开已选择的C#文件，编写需要执行的C#代码。
  
![执行 C#代码段](https://docimages.blob.core.chinacloudapi.cn/images/Activities/executecsharpcode20210303.png)

> **说明：**
>
> 这里支持变量的引用，事先在编辑器中定义了 String 类型的变量 `m` 和 `n`。

## 常见问题

1. **Q：如何将图片转base64？**

    **A：** 目前无对应组件，建议先用C#代码实现。

    ```C#
    //代码执行入口，请勿修改或删除
    public void Run()
    {
    //在这里编写您的代码
        try
        {
            Bitmap bmp = new Bitmap(DirStr+"/code.jpg");
            MemoryStream ms = new MemoryStream();
            bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Jpeg);
            byte[] arr = new byte[ms.Length]; ms.Position = 0;
            ms.Read(arr, 0, (int)ms.Length); ms.Close();
            base64String= Convert.ToBase64String(arr);
        }
        catch (Exception ex)
        {
            base64String="验证码图片转换错误";
        }
    }
    //在这里编写您的函数或者类"

    ```
