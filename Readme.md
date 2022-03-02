# OpenHarmony3.0 Environment construction

## 安装虚拟机(以Ubuntu为例)

### 下载虚拟机平台VMware

**下载 VMware Workstation Player**

点击链接下载：[VMware Workstation Player](https://customerconnect.vmware.com/en/downloads/info/slug/desktop_end_user_computing/vmware_workstation_player/16_0)

![0](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image0.jpg)

**安装VMware Workstation Player**

1.点击下一步

![1](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image1.png)

2.选择我接受许可协议中的条款，然后点击下一步

![2](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image2.png)

3.选择安装，然后点击下一步

![3](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image3.jpg)

4.更改安装位置，建议安装到D盘，点击下一步（一定要勾选将控制台工具添加到PATH）

![4](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image4.jpeg)

5.关闭启动时检查更新和加入体验计划，然后下一步

![5](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image5.jpeg)

6.然后下一步，点击安装，等待安装完成。

![6](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image6.png)

### 下载Ubuntn-20.04镜像

点击链接下载：[VMware Workstation Player](https://ubuntu.com/download/desktop)

![8](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image8.png)

## 创建一台新的虚拟机

![7](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image7.png)

1.选择：典型（推荐），然后点击下一步

![9](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image9.png)

2.选择稍后暗转操作系统，然后点击下一步

![10](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image10.png)

3.客户端操作系统选择Linux，版本选择Ubuntu 64位，然后点击下一步

![11](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image3.jpg)

4.命名虚拟机，并选择存储位置（建议存放在C盘以外的磁盘中），然后点击下一步

![12](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image12.png)

5.选择虚拟机最大磁盘大小（根据所需设置），建议存放在一个文件里，便于磁盘扩展，然后点击下一步

![13](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image13.png)

6.点击自定义硬件，进行配置虚拟机

![14](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image14.png)

7.修改虚拟机内存，一般根据主机内存来设置，为主机内存的一半为最好（我电脑内存为16G，这里只选择了4G），然后点击处理器

![15](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image15.png)

8.配置虚拟机处理器，根据所需配置，然后点击：新CD/DVD（SATA）

![16](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image16.png)

9.选择使用ISO文件镜像，然后点击下方关闭

![17](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image17.png)

## 启动虚拟机

### 开始安装

1.在左边滑动找到下边的中文简体，然后点击右边的：安装Ubuntu

![18](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image18.png)

2.选择键盘布局，选择Chinese（默认就行），点击继续

![19](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image19.png)

3.根据所需，点击继续

![20](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image20.png)

4.选择地区，找到上海然后点击继续

![21](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image21.png)

5.配置用户名和管理员密码，然后点击继续

![22](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image22.png)

6.等待安装完成重启虚拟机就行

![23](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image23.png)

7.重启之后，一直点击跳过就行

![24](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image24.png)

![25](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image25.png)

*注：这边安装的时候可能看不见下方的选项，按Tab键，当选择方框看不见的时候为第一次，之后再按两次Tab键即可选择到继续按钮，回车即可（如果你用的是VMware的话可以安装vmware tools全屏就好）*

### 虚拟机换源

Ubuntu服务器在国外，在更新软件或者下载软件时网速很慢，所以我们将Ubuntu的源换到国内的站点，比如清华源、中科大原。20-04系统换源界面改成了图形化，比较方便。

#### 方法一（图形化）：

1.找到/etc/apt/sources.list ,双击打开

![26](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image26.png)

2.点击其他站点，然后选择需要更换的国内站点，我这边选择的是清华源，然后点击：选择服务器

![27](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image27.png)

![28](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image28.png)

3.然后关闭这个界面，会弹出一个窗口提示：可用的软件列表已过时，点击：重新载入，然后输入密码即可

![29](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image29.png)

4.按快捷键：Ctrl+Alt+T打开终端，输入命令：
```
sudo apt update && sudo apt upgrade
```
然后回车，输入密码，回车，会提示是否同意：输入y即可

#### 方法二：

教程链接：[Ubuntu更换国内源](https://blog.csdn.net/qq_35451572/article/details/79516563)

![30](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image30.png)

## Ubuntu20.04配置

1.切换sh，从dash 改成bash，因为编译工具链有一部分需要bash
输入
```
sudo dpkg-reconfigure dash
```

![31](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image31.png)

选择No，然后回车

![32](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image32.png)

输入 
```
ls –l /bin/sh
```
回车，查看切换是否成功

![33](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image33.png)

2.软连接Python3，输入：
```sudo ln -s /usr/bin/python3 /usr/bin/python``` 
回车即可
输入python 将会显示python3.8

*注：输入：exit()即可退出Python*

![35](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image35.png)

3.安装pip3并换源
```
sudo apt install python3-pip
```
```
pip install -i https://mirrors.ustc.edu.cn/pypi/web/simple pip -U
```
```
pip config set global.index-url https://mirrors.ustc.edu.cn/pypi/web/simple
```
![36](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image36.png)
![37](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image37.png)

安装环境所需要的库：
```
sudo apt-get install build-essential gcc g++ make zlib* libffi-dev e2fsprogs pkg-config flex bison perl bc openssl libssl-dev libelf-dev libc6-dev binutils binutils-dev libdwarf-dev u-boot-tools mtd-utils gcc-arm-linux-gnueabi cpio device-tree-compiler git git-lfs ruby ccache
```
### hb的安装

安装方法：

1.运行以下命令安装hb
```
  python3 -m pip install --user ohos-build
```
2.配置环境变量（先执行：sudo apt install vim 安装vim）
```
vim ~/.bashrc
```
将以下命令拷贝到./bashrc文件最后一行（输入：i表示插入）
```
export PATH=~/.local/bin:$PATH
```
然后按Esc，输入：
```
:wq
```
回车退出
执行如下命令更显环境变量
```
source ~/.bashrc
```
执行**hb -h**
显示如下信息表示成功
```
usage: hb [-h] [-v] {build,set,env,clean,deps} ...

OHOS Build System version 0.4.3

positional arguments:
  {build,set,env,clean,deps}
    build               Build source code
    set                 OHOS build settings
    env                 Show OHOS build env
    clean               Clean output
    deps                OHOS components deps

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         show program's version number and exit
```

### SCons的安装

1.运行如下命令安装SCons
```
pip3 install scons
```
2.运行如下命令检查是否安装成功
```
scons -v
```
SCons安装成功界面，版本要求为3.0.4以上
```
SCons by Steven Knight et al.:
	SCons: v4.3.0.559790274f66fa55251f5754de34820a29c7327a, Tue, 16 Nov 2021 19:09:21 +0000, by bdeegan on octodog
	SCons path: ['/home/magic/.local/lib/python3.8/site-packages/SCons']
Copyright (c) 2001 - 2021 The SCons Foundation
```
### Python库安装
```
pip3 install pycryptodome
pip3 install six --upgrade --ignore-installed six
pip3 install ecdsa
```

![38](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image38.png)

### 下载GCC
```
wget https://repo.huaweicloud.com/harmonyos/compiler/gcc_riscv32/7.3.0/linux/gcc_riscv32-linux-7.3.0.tar.gz
```
```
tar -xvf gcc_riscv32-linux-7.3.0.tar.gz -C ~
```
配置环境变量
```
vim ~/.bashrc
```
在最后一行插入
```
export PATH=~/gcc_riscv32/bin:$PATH
```
退出，输入如下命令进行保存
```
source ~/.bashrc
```
检查GCC是否安装成功

```
riscv32-unknown-elf-gcc -v
```

![39](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image39.png)

### Git设置

```
git config --global user.name "yourname"
git config --global user.email "your-email-address"   
// 设置记住密码
git config --global credential.helper sto
```

### 下载repo工具链
```
sudo apt install curl
```
```
curl -s https://gitee.com/oschina/repo/raw/fork_flow/repo-py3>repo
```
```
sudo mv repo /usr/local/bin/repo
```
```
sudo chmod a+x /usr/local/bin/repo
```

## OpenHarmony环境搭建

**简介**
openharmony编译环境搭建是一件费事的工作。官网为此提供了docker镜像版本将需要的软件及其依赖打包到镜像中。但此镜像不支持qemu的编译，本文档提供的新镜像不仅解决了编译qemu产品的问题，还提供了qemu的运行环境。并将此环境托管到云上，极大的方便了设备开发者特别是学生的入门。

下面是详细的步骤（以下操作都是在虚拟机中）。
### 下载源码

1、确保码云(gitee)账号已注册， 登录云主机并生成/添加SSH公钥，方式如下

 在终端输入如下命令生成公钥
```
 ssh-keygen -t ed25519 -C "xxxxx@xxxxx.com"
```
 这里的 xxxxx@xxxxx.com 只是生成的 sshkey 的名称，并不约束或要求具体命名为某个邮箱。现网的大部分教程均讲解的使用邮箱生成，其一开始的初衷仅仅是为了便于辨识所以使用了邮箱。

![41](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image41.png)

2、通过查看 ~/.ssh/id_ed25519.pub 文件内容，获取到你的 public key

```
 cat ~/.ssh/id_ed25519.pub
# ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHkfXk5QqyW3Hm34ahcRTbdvJIrpmWdgHNEfXImNV1bX xxxxx@xxxxx.com
```

![40](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image40.png)

3.复制生成后的 ssh key，添加到gitee中个人设置->安全设置->SSH公钥

![42](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image42.png)

![43](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image43.png)

确定之后可以看到公钥添加成功

![44](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image44.png)

4.在终端运行如下3个命令下载源码（时间会比较长，耐心等待），建议在home文件夹下再新建一个openharmony文件夹之后，在终端中打开之后再执行如下命令
```
repo init -u git@gitee.com:openharmony/manifest.git -b master  
repo sync -c
repo forall -c 'git lfs pull'
```
如果出现供应商无效，请执行以下命令之后，再执行上面三个命令
```
sudo apt install git-lfs
```
*注：如果觉得repo过于麻烦，可以根据自己所需对工程文件进行裁剪*
可以参考这个文章把OpenHarmony的repo简化一下，拉取方便，存储少一些：[repo](https://gitee.com/Cruise2019/team_x/blob/master/image/imagehomework/repo/readme.md)

### 编译源码

1.配置产品

在终端输入
```
hb set
```

![45](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image45.png)

回车

如果出现未让输入编译路径，执行
```
hb set -root [正确路径]
```

使用上下键选择产品

如：qemu_mini_system_demo

![46](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image46.png)

回车

通过命令hb env查看刚刚设置的产品
```
hb env
```
![47](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image47.png)

2.编译

在终端输入hb build命令进行编译
```
hb build
```

如果报错
```
ccache: error: Could not find compiler "arm-none-eabi-gcc" in PATH
```
执行如下命令即可
```
sudo apt-get install gcc-arm-none-eabi
```
![48](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image48.png)

至此编译成功

### 运行

在终端输入./qemu-run命令，运行
```
./qemu-run
```

![49](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image49.png)

![50](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image50.png)

至此进入qemu_mini_system_demo，可以在终端输入help查看当前系统支持的命令

![51](https://github.com/MagicGaoxiaolong/OpenHarmony3.0/blob/master/image/image51.png)
