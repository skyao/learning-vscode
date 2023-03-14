---
title: "Container"
linkTitle: "Container"
weight: 100
date: 2021-01-29
description: >
  介绍vs code的remote SSH
---

> 摘录自:  https://code.visualstudio.com/docs/devcontainers/containers

Visual Studio Code Dev Containers 扩展允许你使用Docker容器作为一个全功能的开发环境。它允许你打开容器内的任何文件夹（或装入），并利用Visual Studio Code的全部功能集。你的项目中的 devcontainer.json 文件告诉VS Code如何访问（或创建）一个具有明确定义的工具和运行时栈的开发容器。这个容器可以用来运行一个应用程序，或者用来分离处理代码库所需的工具、库或运行时。

工作区文件从本地文件系统挂载，或复制或克隆到容器中。扩展被安装并在容器内运行，在那里它们可以完全访问工具、平台和文件系统。这意味着你可以无缝切换你的整个开发环境，只需连接到一个不同的容器。

![Container Architecture](https://code.visualstudio.com/assets/docs/devcontainers/containers/architecture-containers.png)

这让VS Code提供了一个本地质量的开发体验，包括完整的IntelliSense（补全）、代码导航和调试，无论你的工具（或代码）位于何处。

## 安装

### 准备工作

安装以下内容：

- docker 和 docker-compose
- 安装 [Visual Studio Code](https://code.visualstudio.com/) 
- 安装 [Remote Development extension pack](https://aka.ms/vscode-remote/download/extension).

Dev Containers扩展支持两种主要的操作模式：

- 使用容器作为你的全职开发环境
- 附加到正在运行的容器上以检查它

## dev container 教程

https://code.visualstudio.com/docs/devcontainers/tutorial

在Docker容器中运行VS Code有很多用处，但在本攻略中，我们将重点介绍使用Docker容器建立一个与本地环境隔离的开发环境。

- 安装 Dev Containers extension
