# LearnGit
学习Git

##有关README
    
README文件后缀为md，代表的是MarkWord的缩写，README的编写和正常的MarkWord语言编写是一样的
[README讲解地址](http://blog.csdn.net/kaitiren/article/details/38513715)

##使用git将本地代码上传至github

>有两种方法将本地代码上传至github，一种是使用SSL，一种是HTTP。使用SSL相对比较麻烦（[学习地址](http://www.cnblogs.com/lijiayi/p/pushtogithub.html)），使用HTTP相对简单点。

* 使用HTTP的简单步骤
    * 使用xcode创建项目时会自动生成.git文件，所以我们无需手动创建
    * 添加README.md文件（也可以随后添加）
    * 连接远程仓库（即github上自己创建的仓库）`git remote add origin 仓库地址链接`
    * 先拉取`git pull origin master`（防止后面push失败）
    * `git push -u origin master`

>可能碰到的问题
* 如果输入`$ Git remote add origin 仓库地址`时提示错误信息`fatal: remote origin already exists.`，需要先删除`$ git remote rm origin` ，再重新连接
* 如果输入`$ git push origin master`，提示出错信息：`error:failed to push som refs to .......`
    >>解决办法如下：
    1、先输入`$ git pull origin master`
    2、再输入`$ git push origin master`
    3、如果出现报错 `fatal: Couldn't find remote ref master`或者`fatal: 'origin' does not appear to be a git repository`以及`fatal: Could not read from remote repository.`
    4、则需要重新输入`$ git remote add origin 仓库地址连接`
