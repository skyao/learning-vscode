---
title: "网络"
linkTitle: "网络"
weight: 100
date: 2021-01-29
description: >
  配置VS Code的网络连接
---

> 摘录自 https://code.visualstudio.com/docs/setup/network

Visual Studio Code是建立在 Electron 之上的，并受益于 Chromium 的所有网络堆栈功能。这也意味着 VS Code 的用户可以获得谷歌浏览器中的大部分网络支持。

## 常见的主机名

VS Code 中的少数功能需要网络通信才能工作，如自动更新机制、查询和安装扩展以及遥测。为了使这些功能在代理环境下正常工作，你必须正确配置产品。

如果你在防火墙后面，需要允许VS Code使用的特定域，这里是你应该允许通信通过的主机名列表：

- `update.code.visualstudio.com` - Visual Studio Code download and update server
- `code.visualstudio.com` - Visual Studio Code documentation
- `go.microsoft.com` - Microsoft link forwarding service
- `vscode.blob.core.windows.net` - Visual Studio Code blob storage, used for remote server
- `marketplace.visualstudio.com` - Visual Studio Marketplace
- `*.gallery.vsassets.io` - Visual Studio Marketplace
- `*.gallerycdn.vsassets.io` - Visual Studio Marketplace
- `rink.hockeyapp.net` - Crash reporting service
- `bingsettingssearch.trafficmanager.net` - In-product settings search
- `vscode.search.windows.net` - In-product settings search
- `raw.githubusercontent.com` - GitHub repository raw file access
- `vsmarketplacebadge.apphb.com` - Visual Studio Marketplace badge service
- `az764295.vo.msecnd.net` - Visual Studio Code download CDN
- `download.visualstudio.microsoft.com` - Visual Studio download server, provides dependencies for some VS Code extensions (C++, C#)
- `vscode-sync.trafficmanager.net` - Visual Studio Code Settings Sync service
- `vscode-sync-insiders.trafficmanager.net` - Visual Studio Code Settings Sync service (Insiders)
- `vscode.dev` - Used when logging in with GitHub or Microsoft for an extension or Settings Sync
- `default.exp-tas.com` - Visual Studio Code Experiment Service, used to provide experimental user experiences

## 代理服务器支持

VS Code拥有与 Google Chromium 完全相同的代理服务器支持。下面是Chromium文档中的一个片段：

"Chromium 网络堆栈使用系统网络设置，这样用户和管理员就可以轻松控制所有应用程序的网络设置。网络设置包括：

 - 代理设置

 - SSL/TLS设置

 - 证书撤销检查设置

 - 证书和私钥存储"

这意味着你的代理设置应该被自动接收。

否则，你可以使用以下命令行参数来控制你的代理设置。


```properties
# 禁用代理
--no-proxy-server

# 手动代理地址
--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"

# 手动PAC地址
--proxy-pac-url=<pac-file-url>。

# 禁用每主机的代理
--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][; ...］
```

要了解这些命令行参数的更多信息，请参见Chromium网络设置。