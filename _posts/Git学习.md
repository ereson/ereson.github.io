# Git学习笔记 --- 01
  这篇主要介绍了如何从Github上拉取一个项目。
## 1.如何从Github上拉取一个项目
* 打开Git bash，输入`mkdir file`创建一个文件夹，然后`cd file`打开这个文件夹
* 通过`git init`将这个文件夹变成本地仓库
* 添加远程仓库`git remote add + name + url`,其中`name`是个人对远程仓库的命名，`url`是远程仓库的链接（可以是http，也可以是ssh)
* 可以通过`git remote -v`看到远程仓库的目录
* `git clone + url` 将远程仓库拉下来，这个`url`同上。
* 最后通过`ls -al`查看是否下拉成功。

