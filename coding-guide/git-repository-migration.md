# git 仓库迁移

优点：保留所有 commit logs

```bash
# 从原仓库中克隆一份镜像
git clone --mirror https://github.com/../old.git old.git
# 进入镜像目录
cd old.git
# 修改新仓库远程地址
git remote set-url --push origin git@gitcafe.com/.../new.git
#  推送本地镜像至新仓库
git push --mirror

```
