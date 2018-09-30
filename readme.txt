1.install git
2.git config --global user.name "hbxn98765"
  git config --global user.email "hbxn98765@tom.com"
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
                 