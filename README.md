# lab1

> 本节目标：
>
> 1. 学习使用超星学习通，并通过邀请码加入课程。
> 2. 配置C语言运行环境
> 3. 编译运行课程的第一个C程序
> 4. 了解常用的学习工具与平台


## 获取及提交lab

**获取**：通过 `https://github.com/FDU-C-2020/lab1`，获取。

**提交**：

**提交物**：

**截止时间**：

## 1.使用学习通

超星学习通是本课程的重要教学辅助工具。它可以用作课程学习、课堂互动、作业发布与收取、资源共享等。下面将对学习通APP进行简单的介绍。

### 登录

1、登录选项处选择其他登录方式：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-0.png" width="300"/>

2、在机构栏输入并选中复旦大学：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-1.png" width="300"/>

3、选中复旦大学后会弹出复旦大学统一身份认证页面，输入用户名和密码登录：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-2.png" width="300"/>

这样就通过使用复旦的认证平台登录了学习通（为了方便下一次登录，可以完善账户信息，绑定手机号以方便通过手机号登录）。

### 加入课程

1、在APP首页的右上角存在“邀请码”，点击邀请码后通过输入邀请码方式加入课程：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-3.png" width="300"/>

2、这里输入程序设计课程的邀请码-`83341795`，以加入课程：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-4.png" width="300"/>

### 其他功能

1、加入课程后点击该课程可以进入课程内容页面：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-5.png" width="300"/>

我们可以看到学习通中可以发布主题讨论，可以进行课堂选人等。

2、点击“作业/考试”可以查看作业完成情况：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-6.png" width="300"/>

3、点击“章节”可以查看课程章节资源（主要是视频教学资源）：

<img src="https://github.com/FDU-C-2020/lab1/blob/master/imgs/xuexitong-step-7.png" width="300"/>

## 运行本学期的第一个 C 程序 （for Windows）

接下来我们尝试运行第一个 C 程序—— `helloworld.c`。
如果你从来没有使用命令行运行过 C 程序，那很好，这就是我们所期望的。
在这一部分，请丢掉你的 IDE，跟着这篇文章重新学习。

### Step 1: 下载 MinGW 包管理器

第一步，我们需要下载 MinGW，它是管理各版本 gcc（C 语言[编译器](https://baike.baidu.com/item/%E7%BC%96%E8%AF%91%E5%99%A8)）的工具。通过它，我们能很快的安装 gcc，从而快速搭建 C 语言开发环境。

[点击这里下载 MinGW](https://osdn.net/projects/mingw/downloads/68260/mingw-get-setup.exe)

### Step 2: 安装 MinGW && 下载 gcc

有人可能发现下载的安装软件相当地小，只有几十K。
这是因为我们下载的只是一个包管理器，包管理器安装后才能继续安装编译器等组件。

注意，整个安装过程都是在线的，因此请不要断开网络。

首先打开安装程序，按照提示，以默认选项进行安装即可。

![安装首页](./imgs/1.png)

安装路径默认在 C 盘，你可以自己考虑是否放在 C 盘内

![路径设置](./imgs/2.png)

> 你可以自己设置路径，但是！**请务必记住该路径**，接下来需要使用到！

包管理器安装完成后将弹出这个界面：

![包管理器界面](./imgs/3.png)

找到 `mingw32-gcc-g++-bin`，点击选择 `Mark for Installation`。

然后点击左上角的 `Installation` 菜单中的 `Apply changes` 选项，然后管理器将开始在线安装或更新被选中的组件。

下面耐心等待程序的安装。

安装完成后关闭包管理器，如果由于某种原因安装未能成功，在退出程序前程序将给予提示，选择 `review changes` 选项重新安装即可。

### Step 3: 配置环境变量

打开 控制面板 -> 系统和安全 -> 系统 -> 高级系统设置 -> 环境变量。

![环境变量](./imgs/4.png)

在系统环境变量列表中找到 `Path` 选项，点击编辑

![Path](./imgs/5.png)

点击新建，找到 MinGW 安装路径下的 bin 文件位置，添加项

我这里的路径是 `C:\MinGW\bin`，如果你将 MinGW 安装在自己设置的路径，请使用**你自己的 MinGW 安装路径下的 bin 文件位置**

### Step 4: 检验

现在，按下 `Win 键 + R`，输入 `cmd` 并回车来打开（如果你已经打开，请重启）你的 CMD 命令行。

![cmd](./imgs/6.png)

输入：

    $ gcc -v


测试 gcc 的版本，如果得到的结果与下面的结果类似，不是没有这种命令或文件的提示之类的话，就说明安装成功。

![cmd](./imgs/7.png)

### Step 4: 运行 `helloworld.c`

在 `helloworld.c` 文件所在文件夹按住 Shift 鼠标右键，在菜单栏里点击 `在此处打开 Powershell 窗口` 项，打开 Powershell

![打开powershell](./imgs/8.png)

输入：

    $ gcc .\helloworld.c -o helloworld.exe

在同文件夹下生成 `helloworld.exe` 文件

再输入：

    $ helloworld.exe

命令行是否输出 `hello world` ？

如果你成功输出 `hello world`，相信你已经学会了如何使用命令行运行 C 程序了，恭喜你！

## 运行本学期的第一个 C 程序（for Mac）

### Step 1: 打开终端

`command + 空格` 打开聚焦搜索🔍，在搜索框中输入 `terminal`，点击下方 “终端” 或直接回车，即可打开终端

![ternimal app](./imgs/mac-1.png)

### Step 2: 进入所在文件夹

打开终端后，我们需要进入 helloworld.c 文件所在的文件夹。
可以在终端内输入 `cd` + 空格，然后使用访达打开文件夹，在将文件夹拖入终端，就能直接获得文件夹所在路径。

比如：我现在要通过终端进入 `lab1` 所在的文件夹。

![open file](./imgs/mac-2.png)

然后在终端内回车，就进入了 `lab1` 的文件夹。

> 你觉得以上操作太繁琐？试试[这个](https://jingyan.baidu.com/article/ce436649281a293773afd3d8.html)

### Step 3: 检查是否安装 `gcc`

在终端输入：

    $ gcc -v

若终端返回以下内容，则说明你已经安装好 `gcc` 了，若没有返回类似内容，你需要在 `App Store` 内下载 `Xcode` 软件，再重新打开终端尝试。

![gcc version](./imgs/mac-3.png)

### Step 4: 编译并运行 `helloworld.c`

在 `helloworld.c` 所在文件夹打开终端，输入：

    $ gcc ./helloworld.c -o helloworld.out

会在同文件夹下生成 `helloworld.out` 文件

再输入：

    $ helloworld.out

看看你是否输出 `hello world` ？





