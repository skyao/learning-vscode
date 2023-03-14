---
title: "SSH"
linkTitle: "SSH"
weight: 100
date: 2021-01-29
description: >
  介绍vs code的remote SSH
---

> 摘录自:  https://code.visualstudio.com/docs/remote/ssh

`Visual Studio Code Remote - SSH` 扩展允许你在任何有运行SSH服务器的远程机器、虚拟机或容器上打开远程文件夹，并充分利用VS Code的功能集。一旦连接到服务器，你可以与远程文件系统上的任何地方的文件和文件夹进行交互。

为了获得这些好处，你的本地机器上不需要有源代码，因为该扩展直接在远程机器上运行命令和其他扩展。

![](https://code.visualstudio.com/assets/docs/remote/ssh/architecture-ssh.png)

这让VS Code提供了一个本地质量的开发体验--包括完整的IntelliSense（补全）、代码导航和调试--无论你的代码在哪里托管。

### 管理扩展

VS Code 在两个地方之一运行扩展：本地的用户界面/客户端，或远程的 SSH 主机。虽然影响VS Code用户界面的扩展，如主题和片段，被安装在本地，但大多数扩展将驻留在SSH主机上。这确保你有流畅的体验，并允许你从本地机器上为SSH主机上的特定工作区安装任何需要的扩展。这样一来，你就可以从不同的机器上继续完成你的扩展。

如果你从扩展视图中安装一个扩展，它将自动安装在正确的位置。一旦安装完毕，你可以根据类别分组来判断一个扩展的安装位置。

### 转发端口/创建SSH隧道

有时在开发时，你可能需要访问远程机器上的一个没有公开的端口。有两种方法可以做到这一点，使用SSH隧道将所需的远程端口 "转发" 到你的本地机器。

### 临时转发端口

一旦你连接到主机，如果你想在会话期间临时转发一个新的端口，从命令调色板（F1，Ctrl+Shift+P）选择转发一个端口，或者在端口视图中选择添加端口按钮。你可以在底部面板中看到端口视图，或者通过运行命令 **Ports: Focus on Ports View**。

#### 始终转发端口

如果你有一直想转发的端口，你可以在你用来记忆主机和高级设置的同一个SSH配置文件中使用LocalForward指令。

例如，如果你想转发3000和27017端口，你可以按以下方式更新该文件。

```properties
Host remote-linux-machine
    User myuser
    HostName remote-linux-machine.mydomain
    LocalForward 127.0.0.1:3000 127.0.0.1:3000
    LocalForward 127.0.0.1:27017 127.0.0.1:27017
```

