Buildroot SDK
---
# 配置repo

## 下载repo
根据您的办公网络情况，从以下链接获取repo工具。

`git clone https://gerrit.googlesource.com/git-repo` (谷歌官方源)
`git clone https://mirrors.tuna.tsinghua.edu.cn/git/git-repo` (国内清华源)
`git clone https://gerrit-googlesource.lug.ustc.edu.cn/git-repo` (国内中科大源)

## 配置REPO_URL
在到构建和谐社会的前提下，需要修改REPO_URL，可参考以下修改：

  vim repo

```
## REPO_URL = 'https://gerrit-googlesource.proxy.ustclug.org/git-repo'
REPO_URL = 'https://mirrors.tuna.tsinghua.edu.cn/git/git-repo/'
```

## 配置好的repo
```
https://git.dev.tencent.com/codebug8/repo.git
```
# 初始化仓库 repo init
## mini437x开发板
```
$ mkdir -p mini437x
$ cd mini437x
$ repo init -u https://dev.tencent.com/u/codebug8/p/manifest/ -b linux-sdk -m ti437x/mini437x_linux_release.xml --no-repo-verify
```
## firefly-rk3288开发板
## roc-rk3399开发板
## ti335x开发板
新建目录存放仓库



# 同步代码repo sync

```
$ repo sync -j4

```
```
Fetching projects: 100% (3/3)
Fetching projects: 100% (3/3), done.
Checking out files: 100% (10246/10246), done.
Checking out files: 100% (56938/56938), done.es:  18% (10547/56938)
Syncing work tree: 100% (3/3), done
```
# 代码目录
查看下载好的源码目录

