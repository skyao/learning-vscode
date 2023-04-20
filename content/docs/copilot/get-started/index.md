---
title: "开始使用Copilot"
linkTitle: "开始使用"
weight: 10
date: 2023-03-14
description: >
  在 vs code 中安装配置 Copilot 以便开始使用
---



参考：

[Getting started with GitHub Copilot in Visual Studio Code - GitHub Docs](https://docs.github.com/en/copilot/getting-started-with-github-copilot/getting-started-with-github-copilot-in-visual-studio-code)

## 步骤

### 安装 copilot 扩展

打开 vs code 的 extension marketplace, 搜索 compilot：

![Selection_001](images/Selection_001.png)

### 登录组织

扩展安装完成之后，vs code 提示要登录以使用 github copilit：

![Selection_002](images/Selection_002.png)

因为我是 microsoft 组织的成员，所以就简单了，在这里点 continue 就好：

![Selection_003](images/Selection_003.png)

### github 开启 copilot

github 设置开启 copilot : [Configuring GitHub Copilot settings on GitHub.com - GitHub Docs](https://docs.github.com/en/copilot/configuring-github-copilot/configuring-github-copilot-settings-on-githubcom#enabling-or-disabling-duplication-detection)  。

完成后，vs code 左下角会有一个提示

![Menu_001](images/Menu_001.png)

点击后继续提示：

![Visual_Studio_Code_001](images/Visual_Studio_Code_001.png)

容许之后，在 vs code 右下角可以看到 copilot 的标记：

![Selection_004](images/Selection_004.png)

## 使用

### js 的简单例子 

参考文档的说明：

https://docs.github.com/en/copilot/getting-started-with-github-copilot/getting-started-with-github-copilot-in-visual-studio-code#seeing-your-first-suggestion

在 vs code 中新建 a.js 文件，输入 

```javascript
function calculateDaysBetweenDates(begin, end) {
```

就能看到 copilot 的建议代码: 

![Selection_005](images/Selection_005.png)

### golang 的简单例子

新建一个 test.go 文件，输入提示注释, 回车之后， copilot 建议代码如下：

```go
// server on port 8080
func main() {
	http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
		w.Write([]byte("Hello, World!"))
	})
	http.ListenAndServe(":8080", nil)
}
```



