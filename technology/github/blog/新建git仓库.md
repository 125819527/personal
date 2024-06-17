### 初始化本地仓库
```
  git init # 初始化
  git add . # 将工作区提交至暂存区 
  git status # 查看本地文件状态 是否提交至暂存区 
  git commit -m '描述' # 对本次代码修改进行描述
  git remote add origin https://github.com/12345/personal.git # 将本地仓库与远程仓库相连接
  git push origin main # 将数据推送远端仓库
```

### 远程操作
```
git remote add origin https://github.com/12345/personal.git # 将数据与远程相连接
git remote -v # 本都查看远端状态
git remote remove origin # 删除远端
```

### 提交撤回操作
```
git log # 查看历史提交, 可以发现历史提交commit与对应id
git reset --soft commitId # 指定回退提交到指定版本，参数表名只撤回暂存区不撤回工作区, --hard则全部去除
```

### 提交时出现网络连接错误
```
git config --global --unset http.proxy
git config --global --unset https.proxy # 去除代理

git config --global https.postBuffer 524288000
git config --global http.postBuffer 524288000 # 文件过大时提交缓存区会不足
```