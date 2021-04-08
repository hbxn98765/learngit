1.install git
  git的工作需要调用 curl,zlib,openssl,expat,libiconv等库的代码，需要先安装这些依赖工具。
   apt-get install libcur14-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev
  
 
  sudo apt-get install git

  源码安装：https://git-scm.com/download
    apt-get install libcur14-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev

  tar -zxf git-1.7.2.2.tar.gz
  cd git-1.7.2.2
  make prefix=/usr/local all
  sudo make prefix=/usr/local install


  
  git --version
 
2.配置
   /etc/gitconfig  --> git config --system
   ~/.gitconfig    --> git config --global
   .git/config

  git config --global user.name "hbxn98765"
  git config --global user.email "hbxn98765@tom.com"

  指定文本编辑器(Vi,Vim,Emacs)
  git config --global core.editor Vi

  差异分析工具 vimdiff
  git config --global merge.tool vimdiff

  git config --list

3.mkdir learngit
  cd learngit
  pwd (show dir)(ls -ah)

4.git init   初始化仓库
  git add    添加文件到暂存区
  git commit 将暂存区内容添加到仓库中
  git rm     删除工作区文件
  git reset  回退版本
  git mv     移动或重命名工作区文件

  远程操作
  git remote 远程仓库操作
  git fetch  从远程获取代码库
  git pull   下载远程代码并合并
  git push   上传远程代码并合并

  分支管理
  git branch (branchname)   创建分支
  git checkout (branchname) 切换分支
  git merge                 合并分支

  



5.add file note   (utf-8 bom)
  git add readme.txt readme2.txt readme3.txt
  git comit -m "write a readme.txt file" #告诉git,把文件提交到仓库
  
6.git log //显示日志 git log --pretty=oneline
  git reset --hard Head^
  git reset --hard 1094a
  gir reflog
  
  git reset HEAD 暂存区的目录树被重写,被master分支替换，但工作区不受影响
  git rm --cached <file> 会直接从暂存区删除文件，工作区不做改变

  git checkout .或者git checkout --<file> 会用暂存区全部或指定的文件替换工作区的文件
  git checkout HEAD .或者 git checkout HEAD <file>会用分支中的全部或部分文件替换工作区。 

  
7.git status
8.git diff HEAD -- readme.txt

9.git checkout -- file #--很重要，回到最近一次git commit 或git add的状态。

10.git rm
   git commit  #git checkout -- text.txt
   
11.git remote add origin git@github.com:hbxn98765/learngit.git
                 
