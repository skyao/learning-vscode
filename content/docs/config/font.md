---
title: "字体"
linkTitle: "字体"
weight: 20
date: 2021-01-29
description: >
  配置VS Code的字体
---

## 个人配置

默认字体为：

`'Droid Sans Mono', 'monospace', monospace`

在安装了文泉微米等宽黑字体之后，就可以在vs code中启用这个圆润的多的字体了：

`'WenQuanyi Micro Hei Mono', 'monospace', monospace`

然后将默认字体大小从 14 修改为 18（27寸4k显示器, mbp 上我用20）。

## 常见问题



### 无法在Ubuntu中看到汉字

我们正在进行修复。在此期间，打开应用程序菜单，然后选择文件>偏好>设置。在文本编辑器>字体部分，将 "Font Family" 设置为 `Droid Sans Mono, Droid Sans Fallback`。如果你想直接编辑 settings.json文件，可以设置 `editor.fontFamily`，如图所示。

```properties
"editor.fontFamily": "Droid Sans Mono, Droid Sans Fallback"
```
