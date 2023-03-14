---
title: "Dev Container Extension"
linkTitle: "Dev Container"
weight: 200
date: 2021-01-29
description: >
  介绍vs code的Dev Container 扩展
---



## 介绍

> https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers

Dev Containers 扩展允许你使用 Docker 容器作为一个全功能的开发环境。无论你是否部署到容器，容器都是一个伟大的开发环境，因为你可以：

- 在你部署的同一操作系统上用一致的、容易复制的工具链进行开发。
- 在不同的、独立的开发环境之间快速交换，并安全地进行更新，而不必担心影响你的本地机器。
- 让新的团队成员/贡献者很容易在一个一致的开发环境中启动和运行。
- 尝试新技术或克隆代码库的副本，而不影响你的本地设置。

该扩展启动（或附加到）一个运行定义好的工具和运行时栈的开发容器。工作区文件可以从本地文件系统装入容器，或者在容器运行后复制或克隆到容器中。扩展被安装并在容器内运行，它们可以完全访问工具、平台和文件系统。

你在使用VS Code时，就像所有东西都在你的机器上本地运行一样，只不过现在它们被分离在一个容器内。



## 操作

1. Clone `https://github.com/Microsoft/vscode-remote-try-node` 到本地.
2. 打开 vscode, `ctrl + shift + p` ，输入 "open folder in container"，找到上面的目录
3. vscode会自动完成各种工作


### vscode-remote-try-node

```bash
[26 ms] Dev Containers 0.262.3 in VS Code 1.73.1 (6261075646f055b99068d3688932416f2346dd3b).
[25 ms] Start: Resolving Remote
[1436 ms] Setting up container for folder or workspace: /home/sky/work/code/vscode/vscode-remote-try-go
[1439 ms] Start: Check Docker is running
[1439 ms] Start: Run: docker version --format {{.Server.APIVersion}}
[1455 ms] Server API version: 1.41
[1455 ms] Start: Run: docker volume ls -q
[1470 ms] Start: Run: docker ps -q -a --filter label=vsch.local.folder=/home/sky/work/code/vscode/vscode-remote-try-go --filter label=vsch.quality=stable
[1482 ms] Start: Run: docker ps -q -a --filter label=devcontainer.local_folder=/home/sky/work/code/vscode/vscode-remote-try-go
[1494 ms] Start: Run: /usr/share/code/code --ms-enable-electron-run-as-node /home/sky/.vscode/extensions/ms-vscode-remote.remote-containers-0.262.3/dist/spec-node/devContainersSpecCLI.js up --user-data-folder /home/sky/.config/Code/User/globalStorage/ms-vscode-remote.remote-containers/data --workspace-folder /home/sky/work/code/vscode/vscode-remote-try-go --workspace-mount-consistency cached --id-label devcontainer.local_folder=/home/sky/work/code/vscode/vscode-remote-try-go --log-level debug --log-format json --config /home/sky/work/code/vscode/vscode-remote-try-go/.devcontainer/devcontainer.json --default-user-env-probe loginInteractiveShell --mount type=volume,source=vscode,target=/vscode,external=true --skip-post-create --update-remote-user-uid-default on --mount-workspace-git-root true
[1671 ms] (node:23511) [DEP0005] DeprecationWarning: Buffer() is deprecated due to security and usability issues. Please use the Buffer.alloc(), Buffer.allocUnsafe(), or Buffer.from() methods instead.
[1671 ms] (Use `code --trace-deprecation ...` to show where the warning was created)
[1672 ms] @devcontainers/cli 0.23.2. Node.js v16.14.2. linux 5.15.0-53-generic x64.
[1672 ms] Start: Run: docker buildx version
[1706 ms] github.com/docker/buildx v0.9.1-docker ed00243a0ce2a0aee75311b06e32d33b44729689
[1706 ms] 
[1707 ms] Start: Resolving Remote
[1708 ms] Start: Run: git rev-parse --show-cdup
[1711 ms] Start: Run: docker ps -q -a --filter label=devcontainer.local_folder=/home/sky/work/code/vscode/vscode-remote-try-go
[1724 ms] Start: Run: docker inspect --type image mcr.microsoft.com/devcontainers/go:0-1.17-bullseye
[2245 ms] local container features stored at: /home/sky/.vscode/extensions/ms-vscode-remote.remote-containers-0.262.3/dist/node_modules/vscode-dev-containers/container-features
[2246 ms] Start: Run: tar --no-same-owner -x -f -
[2257 ms] Start: Run: docker buildx build --load --build-arg BUILDKIT_INLINE_CACHE=1 -f /tmp/devcontainercli-sky/container-features/0.23.2-1669275188600/Dockerfile-with-features -t vsc-vscode-remote-try-go-ae2cb9ac2a65dfc105652be16da2b666 --target dev_containers_target_stage --build-arg VARIANT=1.17-bullseye --build-arg NODE_VERSION=lts/* --build-arg _DEV_CONTAINERS_BASE_IMAGE=dev_container_auto_added_stage_label /home/sky/work/code/vscode/vscode-remote-try-go/.devcontainer
[+] Building 7.0s (3/5)                                                   ``` 
