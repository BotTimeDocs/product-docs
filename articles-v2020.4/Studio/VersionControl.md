# 版本控制

**版本控制面板** 用于记录项目中文件内容的变化，以便将来查看指定版本的修订情况。

## 启用版本控制功能

当前项目未启用版本控制功能时，单击“启用”，开启版本控制功能，并进行初始化。

![启用版本控制功能](https://docimages.blob.core.chinacloudapi.cn/images/Studio/enableversion20201214.png)

## 查看更改文件列表

**更改文件列表** 展示了当前项目中存在更改的文件及数量。

> **说明：**
>
> 若当前项目中存在文件更改，则分别以不同状态的图标显示添加、修改、删除操作。

## 提交更改文件列表

通过对当前项目中的文件进行操作，可以完成暂存和放弃更改。

![提交](https://docimages.blob.core.chinacloudapi.cn/images/Studio/commit20201214.png)

您可以在更改上方输入提交信息，然后单击“提交”按钮，进行提交所有更改。

## 操作更改文件列表

右击文件列表，在弹出的上下文菜单中，选择对应菜单项，可对更改的文件进行如下操作：

- **打开**：打开指定文件，并在右侧页面展示。
![打开文件](https://docimages.blob.core.chinacloudapi.cn/images/Studio/open20201214.png)

- **放弃修改**：撤回当前文件的更改，恢复到更改前的状态。
![放弃修改](https://docimages.blob.core.chinacloudapi.cn/images/Studio/giveupupdate20201214.gif)

- **与未修改的版本比较**：将当前修改的文件与修改前的文件进行比对。
  
  ![与未修改的版本比较](https://docimages.blob.core.chinacloudapi.cn/images/Studio/compare20210323.png)

- **显示历史**：显示当前所选文件的历史记录。
  
  ![显示历史](https://docimages.blob.core.chinacloudapi.cn/images/Studio/showhistory20201214.png)

## 【高级】将已启用版本控制的项目推送到Github
- **为项目添加远程仓库**：在项目文件夹执行以下命令：<br/>
  git remote add origin https://github.com/xxxx/xxx.git
  ![添加远程仓库](https://docimages.blob.core.chinacloudapi.cn/images/Studio/gitRemoteAddOrigin20220309.png)
- **推送代码**：在项目文件夹执行以下命令：<br/>
  git push -u origin master
  ![推送代码](https://docimages.blob.core.chinacloudapi.cn/images/Studio/gitPush20220309.png)
- **访问Github网站可以看见刚推送的项目文件**
  ![Github](https://docimages.blob.core.chinacloudapi.cn/images/Studio/gitDemo20220309.png)
## 【高级】从Github将项目下载至本地
- **克隆项目**：在编辑器本地项目根目录执行以下命令：<br/>
  git clone -b master https://github.com/XXXX/XXXX.git
  ![GitClone](https://docimages.blob.core.chinacloudapi.cn/images/Studio/gitClone20220309.png)
- **打开编辑器可以在本地项目看见刚才下载的项目**
    ![本地项目](https://docimages.blob.core.chinacloudapi.cn/images/Studio/gitProject20220309.png)