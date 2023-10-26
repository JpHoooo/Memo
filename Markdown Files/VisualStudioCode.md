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

2. 在vscode写入以下配置

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


