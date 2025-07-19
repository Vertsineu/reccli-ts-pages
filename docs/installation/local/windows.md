# Windows 安装指南

本指南将帮助您在 Windows 系统上安装和配置 reccli-ts。

## 系统要求

安装包支持以下系统环境：

- Windows 10 或更高版本
- 至少 500MB 可用磁盘空间

## 快速安装

1. 从以下链接下载最新的 Windows 安装包：
   [reccli-ts-windows-x86_64.zip](https://github.com/Vertsineu/reccli-ts/releases/download/v2.0.0/reccli-ts-windows-x86_64.zip)

2. 解压下载的 ZIP 文件到随意的一个临时目录下

3. 双击解压后文件夹中的 `run-windows.bat` 文件启动 reccli-ts

4. 启动成功后，打开浏览器并访问: [http://localhost:5173](http://localhost:5173)

就这么简单！无需额外配置，程序会自动设置所需的环境并启动本地服务器。

## 手动安装

如果您希望从源代码安装或自定义构建，可以按照以下步骤进行手动安装：

### 前置条件

在开始手动安装前，请确保您的系统上已安装以下工具：

- [Git](https://git-scm.com/downloads) - 用于克隆源代码仓库
- [Node.js](https://nodejs.org/) (14.x 或更高版本) - 包含 npm 包管理器

### 安装步骤

按照以下顺序执行命令：

#### 1. 克隆 GitHub 仓库

```bash
git clone https://github.com/Vertsineu/reccli-ts.git
```

#### 2. 进入项目目录

```bash
cd reccli-ts
```

#### 3. 安装依赖并构建项目

```bash
# 安装项目依赖
npm install
npm run client:install
```

```bash
npm run build
npm run client:build
```

#### 4. 启动服务器和客户端

需要打开两个命令行窗口：

命令行窗口 1（启动服务器）：

```bash
npm run server
```

命令行窗口 2（启动客户端）：

```bash
npm run client
```

#### 5. 访问应用

打开浏览器并访问：[http://localhost:5173](http://localhost:5173)

手动安装可以让您完全控制构建过程，适合开发人员或需要自定义配置的高级用户。
