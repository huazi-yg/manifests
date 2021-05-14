Buildroot SDK
------

# 配置repo
## 下载repo
根据您的办公网络情况，从以下链接获取repo工具。
```
git clone https://gerrit.googlesource.com/git-repo  (谷歌官方源)
git clone https://mirrors.tuna.tsinghua.edu.cn/git/git-repo (国内清华源)
git clone https://gerrit-googlesource.lug.ustc.edu.cn/git-repo (国内中科大源)

```
## 配置REPO_URL
在到构建和谐社会的前提下，需要修改REPO_URL，可参考以下修改：

  vim repo

```
## REPO_URL = 'https://gerrit-googlesource.proxy.ustclug.org/git-repo'
REPO_URL = 'https://mirrors.tuna.tsinghua.edu.cn/git/git-repo/'
```

## 配置好的repo(二选一)
```
git clone  https://gitee.com/oschina/repo.git
git clone https://e.coding.net/codebug8/repo.git
```

# 获取视频配套各个开发板bsp源码
## 100ask_imx6ull_pro开发板
```
book@100ask:~$ git clone https://e.coding.net/codebug8/repo.git
book@100ask:~$ mkdir -p 100ask_imx6ull-sdk && cd 100ask_imx6ull-sdk
book@100ask:~/100ask_imx6ull-sdk$ ../repo/repo init -u  https://gitee.com/weidongshan/manifests.git -b linux-sdk -m imx6ull/100ask_imx6ull_linux4.9.88_release.xml  --no-repo-verify
book@100ask:~/100ask_imx6ull-sdk$  ../repo/repo sync -j4
```
## 100ask_imx6ull_pro开发板linux kernel5.4版本

```
book@100ask:~$ git clone https://e.coding.net/codebug8/repo.git
book@100ask:~$ mkdir -p 100ask_imx6ull_pro-sdk && cd 100ask_imx6ull_pro-sdk
book@100ask:~/100ask_imx6ull_pro-sdk$ ../repo/repo init -u  https://gitee.com/weidongshan/manifests.git -b linux-sdk -m imx6ull/100ask_imx6ull_linux5.4.24_release.xml  --no-repo-verify
book@100ask:~/100ask_imx6ull_pro-sdk$  ../repo/repo sync -j4
```



## 100ask_imx6ull_mini开发板
```
book@100ask:~$  git clone https://e.coding.net/codebug8/repo.git
book@100ask:~$ mkdir -p 100ask_imx6ull_mini-sdk && cd 100ask_imx6ull_mini-sdk
book@100ask:~/100ask_imx6ull_mini-sdk$  ../repo/repo init  -u  https://gitee.com/weidongshan/manifests.git -b linux-sdk -m imx6ull/100ask_imx6ull_mini_linux4.9.88_release.xml  --no-repo-verify
book@100ask:~/100ask_imx6ull_mini-sdk$  ../repo/repo sync -j4
```

## 100ask_stm32mp157_pro开发板

```
book@100ask:~$ git clone https://e.coding.net/codebug8/repo.git
book@100ask:~$ mkdir -p 100ask_stm32mp157_pro-sdk && cd 100ask_stm32mp157_pro-sdk
book@100ask:~/100ask_stm32mp157_pro-sdk$  ../repo/repo init -u  https://gitee.com/weidongshan/manifests.git  -b linux-sdk  -m stm32mp1/100ask_stm32mp157_pro_release-v2.0.xml  --no-repo-verify
book@100ask:~/100ask_stm32mp157_pro-sdk$  ../repo/repo sync -j4

```

# 获取开发板其它版本bsp源码

## 100ask_stm32mp157_pro开发板yocto系统
> 注意 需要下载资料光盘里的原件包，否则编译时会出现卡死问题。

```
book@100ask:~$ git clone https://e.coding.net/codebug8/repo.git
book@100ask:~$ mkdir -p 100ask_stm32mp157_pro-yocto && cd 100ask_stm32mp157_pro-yocto
book@100ask:~/100ask_stm32mp157_pro-yocto$  ../repo/repo init -u  https://gitee.com/weidongshan/manifests.git  -b linux-sdk  -m stm32mp1/100ask-stm32mp1-5.4.31-2.0.0.xml    --no-repo-verify
book@100ask:~/100ask_stm32mp157_pro-yocto$  ../repo/repo sync -j4
```

## 100ask_imx6ull开发板zeus 版本yocto系统
> 注意 需要下载资料光盘里的原件包，否则编译时会出现卡死问题。

```
book@100ask:~$ git clone https://e.coding.net/codebug8/repo.git
book@100ask:~$ mkdir -p 100ask_imx6ull-yocto && cd 100ask_imx6ull-yocto
book@100ask:~/100ask_imx6ull-yocto$  ../repo/repo init -u  https://gitee.com/weidongshan/manifests.git  -b linux-sdk  -m imx6ull/100ask_imx-5.4.47-2.2.0.xml  --no-repo-verify
book@100ask:~/100ask_imx6ull-yocto$  ../repo/repo sync -j4
```

# 同步代码repo sync

```
$ repo sync -j8

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
```
ls -l
```

