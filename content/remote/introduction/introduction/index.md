---
title: "概述"
linkTitle: "概述"
weight: 1
date: 2021-01-29
description: >
  概述介绍VS Code的远程开发
---

> 内容摘录自： https://code.visualstudio.com/docs/remote/remote-overview



Visual Studio代码远程开发允许你使用容器、远程机器或Linux的 Windows子系统（WSL）作为一个全功能的开发环境。你可以：

- 在你部署的同一操作系统上开发，或使用更大或更专业的硬件。
- 将你的开发环境分开，避免影响你的本地机器配置。
- 让新的贡献者容易上手，让每个人都在一个一致的环境中。
- 使用你的本地操作系统上没有的工具或运行时，或管理它们的多个版本。
- 使用Windows Subsystem for Linux开发你的Linux部署的应用程序。
- 从多个机器或地点访问一个现有的开发环境。
- 调试在其他地方运行的应用程序，如客户站点或云中。

要获得这些好处，你的本地机器上不需要有源代码。远程开发扩展包中的每个扩展都可以直接在容器内、在WSL中或在远程机器上运行命令和其他扩展，因此，一切都像你在本地运行时那样感觉。

![architecture](images/architecture.png)



远程开发扩展包

远程开发扩展包包括三个扩展: 

- remote - SSH - 通过使用SSH打开远程机器/虚拟机上的文件夹连接到任何位置。
- Dev Containers - 在一个容器内（或装入）使用单独的工具链或基于容器的应用程序。
- WSL - 在Windows Subsystem for Linux中获得由Linux驱动的开发体验。









