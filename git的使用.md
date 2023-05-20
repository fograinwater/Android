安装环境：

ubuntu



一些前置概念：

**版本控制系统**

1. 含义：版本控制系统（Version Control System，VCS）是一种软件，可以帮助软件团队的开发人员**协同工作**，并存档他们工作的完整历史记录

2. 分类：![img](https://ttt-pictures.oss-cn-hangzhou.aliyuncs.com/v2-a65cce9395b52fd175d9891a05d1b840_r.jpg)



**分布式**

1. 含义：分布式是计算机的一种算法，它研究如何把一个需要非常巨大的计算能力才能解决的问题分成许多小的部分，然后把这些部分分配给多个计算机进行处理，最后把这些计算结果综合起来得到最终的结果（简单来说就是**分解+综合**），与传统的**集中式**算法相对。

2. 优点：

- 共享稀有资源
- 平衡负载
- 安全性更高

3. 集中式和分布式的主要区别：你的本地是否有完整的版本库历史

- 假设SVN服务器没了，那你丢掉了所有历史信息，因为你的本地只有当前版本以及部分历史信息。
- 假设GitHub服务器没了，你不会丢掉任何git历史信息，因为你的本地有完整的版本库信息。你可以把本地的git库重新上传到另外的git服务商。

git的诞生：被历史牛人震惊的一天

![image-20230520095531930](https://ttt-pictures.oss-cn-hangzhou.aliyuncs.com/image-20230520095531930.png)



【注】：所有的版本控制系统，其实只能跟踪文本文件的改动，比如 TXT文件，网页，所有的程序代码等等 ，若对图片、视频及microsoft的word这些二进制格式文件修改时，版本控制系统是无法跟踪到文件的改动的，若要真正使用版本控制系统，就要**以纯文本的方式编写文件**。

文本编码：UTF-8编码，不要使用windows的记事本，建议在ubuntu上安装vscode



### 一、Git与Github互连

##### 1.配置 Git 用户信息

- `git config --global user.name "用户名"`
- `git config --global user.email "邮箱"`

##### 2.查看Git用户信息

- `git config user.name`获取当前用户名
- `git config user.email`获取当前邮箱

##### 3.Git连接GitHub

- `sudo apt install ssh`，Ubuntu环境下安装ssh

  - Windows环境下不需要安装

- 输入`ls -ah`查看主目录下有没有**.ssh**这个隐藏文件

- 生成SSH KEY：`ssh-keygen -t rsa -C "邮箱"`

- 进入 **/root/.ssh**目录，查看**id_rsa**和**id_rsa.pub**文件，将**id_rsa.pub**的内容复制到Github的**SSH keys**当中

  - 进入github的`setting`界面

  - 点击左侧的`SSH and GPG keys`
  - 点击`New SSH key`

![](https://ttt-pictures.oss-cn-hangzhou.aliyuncs.com/image-2023052013121341.png)

- 将刚刚从**id_rsa.pub**中复制的内容粘贴到Github的**Key**中即可![image-20230520131448415](https://ttt-pictures.oss-cn-hangzhou.aliyuncs.com/image-20230520131448415.png)
- Windows环境下在C盘的user目录



## 二、创建仓库

1. 在合适的地方创建一个空目录作为仓库(repository)

```
$ mkdir learngit
```

2. 进入learngit目录，通过 `git init` 命令把这个目录变成Git可以管理的仓库

```
$ git init
```

- 通过`ls -ah` 命令可以发现当前目录下多了一个`.git`的目录（一般是隐藏文件），这个目录是Git来跟踪管理版本库的，没事千万不要手动修改这个目录里面的文件



## 三、提交文件到仓库

1. 使用`git add`命令将文件暂存

```
git add <filename>
```

2. 使用`git commit`命令提交文件，" "里的内容是本次提交的说明，可以自行更改

```
git commit -m "initial commit of my project"
```

