---
title: Windows搭建c++环境
date: 2024-10-06 17:20:22
tags:
    - Windows
    - C++
cover: img/Windows/Windows-C++-Vscode.png
---

## 1. 介绍
### 工具:
- Cmake

- Ninja

- Clang

- MinGW

- Git

Cmake: 一个强大的构建系统, 方便的链接你的头文件, 库等

Ninja: 一个小型的构建系统, 适合日常使用, 在这里作为Visual Studio的替代品

Clang: LLVM推出的C++编译器, 在速度上有很大的优势, 兼容各大主流操作系统

MinGW: 为Clang提供库文件, 头文件

Git: 强大的代码管理与传输工具

## 2. 下载
### 官网:
- Cmake
https://github.com/Kitware/CMake/releases/download/v3.30.4/cmake-3.30.4-windows-x86_64.msi

- Ninja
https://github.com/ninja-build/ninja/releases/download/v1.12.1/ninja-win.zip

- Clang
https://github.com/llvm/llvm-project/releases/download/llvmorg-18.1.8/LLVM-18.1.8-win64.exe

- MinGW
https://github.com/niXman/mingw-builds-binaries/releases/download/14.2.0-rt_v12-rev0/x86_64-14.2.0-release-win32-seh-ucrt-rt_v12-rev0.7z

- Git
https://github.com/git-for-windows/git/releases/download/v2.46.2.windows.1/Git-2.46.2-64-bit.exe

### 本站:

- Cmake
https://flowercity.xyz/files/cmake-3.30.4-windows-x86_64.rar

- Ninja
https://flowercity.xyz/files/ninja-win.zip

- Clang
https://flowercity.xyz/files/LLVM-18.1.8-win64.rar

- MinGW
https://flowercity.xyz/files/x86_64-14.2.0-release-win32-seh-ucrt-rt_v12-rev0.7z

- Git
https://flowercity.xyz/files/Git-2.46.2-64-bit.rar

## 3. 安装
在自己电脑上找一个喜欢的位置

这里本文选用 "C:\Program Files"

将上一步下载好的东西都放进去

注: 安装包如果有 Add Path 等字眼勾起来, 压缩包才执行这一步操作

### 添加环境变量

在桌面 -> 右键此电脑 -> 属性 -> 高级系统设置 -> 环境变量 -> 系统变量 -> Path

新建4个

- 你选用的目录/MinGW解压出来的文件夹名/bin

- 你选用的目录/LLVM/bin

- 你选用的目录/Ninja解压出来的文件夹名

- Cmake安装目录/bin ( 如果你之前安装的时候没有加 )

- Git安装目录/bin ( 如果你之前安装的时候没有加 )

重启电脑

## 4. 配置

### Visual Studio Code

下载你喜欢的编辑器

这里推荐 Visual Studio Code

官网下载:

https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user

本地下载:

https://flowercity.xyz/files/VSCodeUserSetup-x64-1.94.0.rar

下载好后, 右键, 管理员身份安装

( 没用管理员身份也没关系,但是为了以后配置时找目录方便,选择管理员身份安装至 C:\Program Files )

安装好之后打开, 在最左边一排找到插件( Extensions )

安装如下插件

- Chinese (Simplified) (简体中文)

- clangd

- CMake

- CMake Tools

推荐的其余插件

- Project Manager ( 多项目快捷切换 )

- koroFileHeader ( 文件头注释 )

- Polacode-2022 ( 代码截图 )

- GitLens -- Gitsupercharged ( Git 项目管理 )

- indent-rainbow ( 彩色代码缩进 )

- GitHub Theme ( 好看的主题 )

- Atom Material Icons ( 好看的产品图标 )

- Material Icon Theme ( 好看的文件图标 )

### Git 仓库

打开Github, 注册一个账号

打开 https://github.com/FlowerCountry/cppStudy

点击右上角的 Fork

等待复制入你的账户后在右上角找到一个绿色的 Code

点击

选择 Https , 复制这个网址

在你电脑上选一个你喜欢的地方( 如你的桌面 )

右键, Open Git Bush Here

输入

``` bash
git clone 你刚刚复制的网址
```

( 如果这一步不成功, 你可以回到Github上的代码仓库, 选择SSH, 复制, 重新来一次 )

右键你下载下来的代码, 选择通过 Code 打开

在左边找到CMake Tools的图标

配置第一项, 更改工具包

选择" Clang x.x.x ... "

注意不要选那个Clang_cl

之后便可以快乐的写代码了

源文件存在src目录下

头文件存在include目录下

编译和运行点击Vscode下栏的按钮 Build 和一个运行图标的三角形

## 5. 完结撒花