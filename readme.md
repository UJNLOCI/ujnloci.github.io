## 初次运行（部署到本地）

### 下载 hugo

版本不要太高,可能会不兼容

推荐 `hugo v0.110.0` 或者 `hugo v0.111.0`，其他版本自己尝试

**将 `hugo.exe` 所在文件夹添加到环境系统变量**

终端运行 `hugo version` 命令查看是否安装成功

### 安装 go

注意版本是否是否兼容

版本 `go 1.20` 、`go 1.22` 同样添加到环境变量

### 克隆项目

创建一个文件夹作为项目根目录

打开项目根目录使用 `git` 命令克隆项目文件：

```sh
git clone https://github.com/ujnloci/ujnloci-page-dev.git
```

```sh
git clone https://github.com/ujnloci/ujnloci.github.io.git
```

在根目录新建public文件夹、将 `https://github.com/ujnloci/ujnloci.github.io.git`克隆下来的所有文件放到public文件夹下

### 启动项目

进入 `ujnloci-page-dev` 文件夹，在终端中运行 `hugo server` 后打开浏览器，进入 ` http://localhost:1313/` 查看是否成功部署。

更改信息后，终端运行 `hugo`  命令更新 `public` 文件夹 ，生成新的静态资源。

进入 `public` 文件夹（终端执行`cd public`），依次执行以下命令将静态资源上传到 `https://github.com/ujnloci/ujnloci.github.io` 仓库。

```sh
git init    ##初始化仓库
git remote add origin https://github.com/ujnloci/ujnloci.github.io.git    ##链接远程仓库
git add .
git commit -m "update"
git push -u origin main ##push到main分支
```

## 后续更新

每次更新完信息后要回到根目录并运行 `hugo` 命令重新生成静态文件（**可以先使用 `hugo server` 命令预览信息是否正确更新**），然后依次执行以下步骤将项目代码上传到 `ujnloci-page-dev` 仓库：

```sh
git add .
git status
git commit -m "update"
git push
```

然后进入 `public` 文件夹（终端执行`cd public`），依次执行以下命令将静态资源上传到 `ujnloci.github.io` 仓库:

```sh
git add .
git status
git commit -m "update"
git push
```



## 其他说明

整个网站项目部署在 `github` 上，分为两个仓库：`ujnloci-page-dev` 和 `ujnloci.github.io`，其中 `ujnloci-page-dev` 仓库是私人仓库，存放项目源代码，`ujnloci.github.io` 仓库是公开仓库，用于显示页面。

将项目部署到本地时，只需要克隆 `ujnloci-page-dev` 仓库内的源代码，然后编译后即可生成静态页资源.

每次更新信息或修改内容后都要先执行 `hugo` 命令编译静态资源，然后将源代码和静态页面资源分别上传到 `ujnloci-page-dev` 和 `ujnloci.github.io` 仓库即可。