---
title: "安装概述"
linkTitle: "概述"
weight: 1
date: 2021-01-29
description: >
  概述介绍VS Code的安装
---





## setup

>  摘录自：https://code.visualstudio.com/docs/setup/setup-overview

使用Visual Studio Code启动和运行是快速而简单的。它的下载量很小，所以你可以在几分钟内安装，并试一试VS Code。

### 跨平台

VS Code是一个免费的代码编辑器，它可以在macOS、Linux和Windows操作系统上运行。

请遵循以下特定平台的指南：

- macOS
- Linux
- Windows

VS Code是轻量级的，应该可以在大多数可用的硬件和平台版本上运行。你可以查看系统要求以检查你的计算机配置是否被支持。

### 更新节奏

VS Code每个月都会发布一个新的版本，包含新的功能和重要的错误修复。大多数平台支持自动更新，当新版本可用时，你会被提示安装。你也可以通过在Linux和Windows上运行帮助>检查更新，或者在macOS上运行代码>检查更新来手动检查更新。

注意：如果你喜欢按照自己的计划更新VS Code，你可以禁用自动更新。

### Insiders nightly build

如果你想尝试我们的nightly build，以尽早看到新功能或验证错误修复，你可以安装我们的Insiders构建。Insiders 版本与每月的稳定版本并排安装，你可以在同一台机器上自由地使用这两种版本。Insiders版本是VS Code开发团队日常使用的版本，我们非常感谢人们尝试新功能并提供反馈。

### 便携模式

Visual Studio Code支持便携模式的安装。这种模式使VS Code创建和维护的所有数据都在自己附近，所以它可以在不同的环境中移动，例如，在USB驱动器上。详情请见VS Code便携模式文档。

### 附加组件

VS Code首先是一个编辑器，并以其占用空间小而自豪。与传统的往往包括所有的东西IDE不同，你可以根据你关心的开发技术调整你的安装。在阅读完平台指南后，请务必阅读 "附加组件 "主题，了解如何定制你的VS Code安装。

### 扩展

VS Code的扩展允许第三方增加对额外的支持。

- 语言 - C++, C#, Go, Java, Python
- 工具 - ESLint, JSHint , PowerShell
- 调试器 - PHP XDebug.
- 按键映射 - Vim, Sublime Text, IntelliJ, Emacs, Atom, Brackets, Visual Studio, Eclipse

扩展集成到VS Code的用户界面、命令和任务运行系统中，所以你会发现通过VS Code的共享界面可以很容易地使用不同的技术。查看VS Code的扩展市场，看看有什么可用的。

### 接下来的步骤

一旦你安装并设置了VS Code，这些主题将帮助你了解更多关于VS Code的知识：

- 附加组件 - 了解如何安装Git、Node.js、TypeScript和Yeoman等工具。
- 用户界面 - 快速了解VS Code。
- 基本编辑 - 了解强大的VS Code编辑器。
- 代码导航 - 快速浏览你的源代码。
- 调试 - 直接在VS Code编辑器中调试你的源代码。
- 代理服务器支持 - 配置你的代理设置。

如果你想快速运行一些东西，可以试试Node.js教程的演练，它能让你在几分钟内用VS Code调试一个Node.js网络应用。

### 常见问题

#### 我如何创建和运行一个新的项目？

VS Code 不包括传统的 文件 > 新项目 对话框或预装的项目模板。你需要根据你的开发兴趣来添加额外的组件和脚手架。有了像Yeoman这样的脚手架工具和通过npm包管理器提供的大量模块，你肯定能找到合适的模板和工具来创建你的项目。

#### 我怎样才能 "干净 "地卸载VS Code？

如果你想在卸载 VS Code 后删除所有用户数据，你可以删除用户数据文件夹 `Code` 和 .`vscode`。这将使您回到安装VS Code之前的状态。如果你不想卸载VS Code，这也可以用来重置所有设置。

文件夹的位置会因你的平台不同而不同。

- Windows - 删除 `%APPDATA%Code` 和 `%USERPROFILE%\.vscode`。
- macOS - 删除 `$HOME/Library/Application Support/Code` 和 `~/.vscode`。
- Linux - 删除 `$HOME/.config/Code` 和 `~/.vscode`。
