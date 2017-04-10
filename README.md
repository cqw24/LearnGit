# LearnGit
学习Git

## 有关README
    
README文件后缀为md，代表的是MarkWord的缩写，README的编写和正常的MarkWord语言编写是一样的
[README讲解地址](http://blog.csdn.net/kaitiren/article/details/38513715)

## 使用git将本地代码上传至github

```
1、先在Github上创建远程仓库

2、上传本地代码至远程仓库
//创建README.md文件
$ echo "# 工程名" >> README.md
//初始化git（可以省略，因为xcode已经帮忙创建好了.git文件）
$ git init
//提交README.md文件
$ git add README.md
$ git commit -m "first commit"
//链接Github仓库
$ git remote add origin https://github.com/cqw24/SSS.git
//将本地代码推送至仓库
$ git push -u origin master

```

>可能碰到的问题
* 如果输入`$ Git remote add origin 仓库地址`时提示错误信息`fatal: remote origin already exists.`，需要先删除`$ git remote rm origin` ，再重新连接
* 如果输入`$ git push origin master`，提示出错信息：`error:failed to push som refs to .......`
    >解决办法如下：
    1、先输入`$ git pull origin master`
    2、再输入`$ git push origin master`
    3、如果出现报错 `fatal: Couldn't find remote ref master`或者`fatal: 'origin' does not appear to be a git repository`以及`fatal: Could not read from remote repository.`
    4、则需要重新输入`$ git remote add origin 仓库地址连接`
