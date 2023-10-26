# Visual Studio Code

## 为什么使用vscode?

- 轻量化、免费开源、插件多

- 方便写shaderlab

---



## 遇到的问题

### 1. 禁止自动下载.NET Runtime.

- **现象**

```
Downloading the .NET Runtime.
Downloading .NET version(s) 7.0.9 .................................................................................................................. Error!
Failed to download .NET 7.0.9:
.NET installation timed out.
Error!
.NET Acquisition Failed: Installation failed: Error: .NET installation timed out.
```

* **原因**

VScode C#扩展插件没有检测到本地的.net 环境从而导致自动下载最新版本的.net runtime

- **解决办法**
1. 检查是否安装.NET

在终端（terminal）输入命令行

```
dotnet --list-sdks
```

如果输出结果类似下图，说明已安装

![截屏2023-10-26 15 28 36](https://github.com/JpHoooo/Memo/assets/42137140/8f5a55b8-ad43-4236-beb8-3aabce933d0a)

2. 在vscode写入以下配置

在vscode中使用快捷键"command+,"打开设置面板，搜索 `Dotnet Acquisition Extension`

选择 `在Setting.json中编辑`，如图1

在图2位置输入以下代码:
```json
        {
            "extensionId": "ms-dotnettools.csharp",
            "path": "/usr/local/share/dotnet/dotnet"
        },
        {
            "extensionId": "ms-dotnettools.csdevkit", 
            "path": "/usr/local/share/dotnet/dotnet"
        },
        {
            "extensionId": "visualstudiotoolsforunity.vstuc", 
            "path": "/usr/local/share/dotnet/dotnet"
        }
```
![截屏2023-10-26 15 27 42](https://github.com/JpHoooo/Memo/assets/42137140/683aa4b9-30f8-4fb5-bee4-88eb4e5e579d)

![截屏2023-10-26 15 29 58](https://github.com/JpHoooo/Memo/assets/42137140/0b8b4203-70a3-450b-980d-a42d93fc353c)


