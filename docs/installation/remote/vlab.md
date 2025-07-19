# VLab 安装指南

本指南将帮助您在 VLab 环境中安装和配置 reccli-ts。

## VLab 介绍

[VLab](https://vlab.ustc.edu.cn) 是由科大计算机实验教学中心提供的、基于互联网的 7x24 远程进行硬件、系统和软件教学实验平台，可校外登录使用，支持 SSH、浏览器和 VNC 远程桌面方式使用。

通过 VLab 项目，在校学生可以免费申请一个 Ubuntu/Debian 的远程虚拟机用于日常使用。

## 快速安装

1. 从以下链接下载最新的 Linux 安装包：
   [reccli-ts-linux-x86_64.tar.gz](https://github.com/Vertsineu/reccli-ts/releases/download/v2.0.1/reccli-ts-linux-x86_64.tar.gz)

2. 解压下载的压缩包到任意目录：

   ```bash
   tar -xzf reccli-ts-linux-x86_64.tar.gz
   ```

3. 进入解压后的目录并运行启动脚本：

   ```bash
   cd reccli-ts
   ./run-linux.sh
   ```

## 手动安装

如果您希望从源代码安装或自定义构建，可以按照以下步骤进行手动安装：

### 前置条件

在开始手动安装前，请确保您的系统上已安装以下工具：

- [Git](https://git-scm.com/downloads) - 用于克隆源代码仓库
- [Node.js](https://nodejs.org/) (14.x 或更高版本) - 包含 npm 包管理器

如果您的系统上尚未安装 Git 和 Node.js，可以使用以下命令进行安装：

```bash
# 更新软件包列表
sudo apt update

# 安装 Git、Node.js 和 npm
sudo apt install -y git nodejs npm
```

安装完成后，可以通过以下命令验证安装是否成功：

```bash
# 检查 Git 版本
git --version

# 检查 Node.js 版本
node --version

# 检查 npm 版本
npm --version
```

### 安装步骤

按照以下步骤在 VLab 环境中安装 reccli-ts：

#### 步骤 1：下载 reccli-ts 源代码

```bash
# 从 GitHub 克隆仓库
git clone https://github.com/Vertsineu/reccli-ts.git

# 进入项目目录
cd reccli-ts
```

#### 步骤 2：安装依赖

```bash
# 安装项目依赖
npm install
npm run client:install
```

#### 步骤 3：构建项目

```bash
# 构建项目
npm run build
npm run client:build
```

#### 步骤 4：启动服务器和客户端

需要打开两个命令行窗口：

命令行窗口 1（启动服务器）：

```bash
npm run server
```

命令行窗口 2（启动客户端）：

```bash
npm run client
```

#### 步骤 5：访问应用

在 VLab 的远程桌面中打开浏览器并访问：[http://localhost:5173](http://localhost:5173)

### 端口转发设置（可选）

如果您的 VLab 没有图形界面以打开浏览器，您需要通过 SSH 端口转发将远程端口映射到本地计算机，以便在本地浏览器中访问应用。您需要在本地计算机上执行以下命令：

```bash
ssh -i vlab-vm1234.pem -L 3000:localhost:3000 -L 5173:localhost:5173 ubuntu@vlab.ustc.edu.cn
```

其中 `vlab-vm1234.pem` 和 `ubuntu` 是应替换为您在 VLab 上的 SSH 密钥和用户名。

设置端口转发后，保持 SSH 连接打开，然后在本地浏览器中访问：[http://localhost:5173](http://localhost:5173)
