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

4.git init

5.add file note   (utf-8 bom)
  git add readme.txt readme2.txt readme3.txt
  git comit -m "write a readme.txt file" #告诉git,把文件提交到仓库
  
6.git log //显示日志 git log --pretty=oneline
  git reset --hard Head^
  git reset --hard 1094a
  gir reflog
  
7.git status
8.git diff HEAD -- readme.txt

9.git checkout -- file #--很重要，回到最近一次git commit 或git add的状态。

10.git rm
   git commit  #git checkout -- text.txt
   
11.git remote add origin git@github.com:hbxn98765/learngit.git
                 
