# 网络问题

## Acknowledgements

[Network issues - Unity Manual](https://docs.unity3d.com/ru/2019.3/Manual/upm-network.html)

## Cause

这个问题跟代理有关系，公司的网络受到了某些限制，正常上网是无法直接连接到'api.unity.com'，只有通过搭梯子这种方式才能够连接。但windows自动更新之后，即便搭梯子也无法访问，于是有了以下报错

## Issue

`Cannot connect to 'api.unity.com' (error code: ECONNRESET). Verify your environment firewall policies allow connection to this host name. If your system is behind a proxy, verify your proxy environment variables (HTTP_PROXY and HTTPS_PROXY) are properly set.`

## Solution

**Setting environment variables for the Unity Hub**

These instructions create a command file on Windows.

The file launches the Hub with the environment variables set. You can either double-click the file, or invoke it from the command prompt. Unity passes these environment variables on to any Unity Editor process launched from the Hub.

1. Open a text editor such as Notepad.

2. Enter the following text, replacing **proxy-url** with the correct proxy server URL and adjusting the Hub install path if needed:
   
   ```powershell
   @echo off
   set HTTP_PROXY=proxy-url
   set HTTPS_PROXY=proxy-url
   start "" "C:\Program Files\Unity Hub\Unity Hub.exe"
   ```

        **Note:** If there are spaces in the path, you must use double quotes around the path to the program.

        **一般梯子软件会提供代理地址**

3. Save the file to a location where you can easily find it (such as the `Desktop`), and make sure the file has the `.cmd` (for example, `launchUnityHub.cmd`)


