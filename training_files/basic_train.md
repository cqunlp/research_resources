### Step.1 Install Zotero and nutstore
#### 1. Install Zetero:

Download zotero from homepage:
```
https://www.zotero.org/download
```

#### 2. Set Zotero default language to Englist
```
Edit > Preferences > Advanced > English 
```
#### 3. Register a new free account(need proxy)
```
https://www.zotero.org/user/login/
```

#### 4. Register a new nutstore account
```
https://www.jianguoyun.com/
```

#### 5. Linked nutstore 
```
https://zhuanlan.zhihu.com/p/112795057
```

#### 6. add Zotero Chrome plugin

### Step.2 Install Git and init an empty repository for test

#### 1. Install git tools
```bash
# in ubuntu or debian based system
sudo apt install git
# in windows
# visit https://gitforwindows.org/
```

#### 1. Common usage instructions(create a repository and link remote source like Github)
```bash
# create a new folder for your codebase
mkdir /path/to/my/codebase 
# enter the folder
cd /path/to/my/codebase
# init the local repository
git init
# write "#your_repository_name" into README.MD, create the README.MD at the sametime
echo "#your_repository_name" > README.MD
# add README.MD to local git repository
git add README.MD
# add all new created or modified files into git repository
git add .
# make a commit message to describe your modification, and commit the change you made.
git commit -m "a commit message"
# link the local repo to remote repo, the <url> should replaced by http links
git remote add main <url>
# push the commited changes from local to remote
git push origin main
# if you change the code after commit, but do not want make any further commits for just few changes, use this command to update the commit 
git commit --amend
```
### Step.3 Install Conda and manage virtual environment
#### 1. Install Miniconda(not recommond Anaconda):
```bash
# download using wget
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
# install miniconda
sh Miniconda3-latest-Linux-x86_64.sh
# set init in bash by default to yes
```
#### 1. Basic conda instructions:
```bash
# create a new virtural environment, with python installed
conda create -n your_env_name python=3.7
# common version
conda create -n your_env_name lib_0 lib_1 ...
# install libs
conda install lib_0
# show all environments
conda env list
# show all libs installed
conda list
```
#### 2. Change conda source to tuna:
```bash
# ref: https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/
nano ~/.condarc
# 
# paste the following config
channels:
  - defaults
show_channel_urls: true
channel_alias: https://mirrors.tuna.tsinghua.edu.cn/anaconda
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```
