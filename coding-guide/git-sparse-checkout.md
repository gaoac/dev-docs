# git 检出指定目录

> SVN 下，可以很方便的只获取版本库中一个或多个目录的内容,但是 Git 的克隆，默认是直接拉取整个远程仓库，如果项目比较大，大量和自己无关的内容也会拉到本地，占用很多硬盘空间。好在 Git1.7 版本后，已经支持只 Checkout 部分内容，也就是 sparse checkout（稀疏检出）。

具体步骤如下：

```bash
# 创建目录
mkdir test
# 进入目录
cd test
# 初始化 git 仓库
git init
# 开启稀疏检出模式
git config core.sparseCheckout true
# 指定远程仓库
git remote add -f origin <远程仓库地址>
# 指定稀疏检出目录
echo 目标目录路径 >> .git/info/sparse-checkout
# 拉取远程文件
git pull origin master

```
