# how to use git

## git 简介

1. 创建版本库

   ```
   mkdir helloword
   cd helloworld
   pwd
   ```

2. ```
   git init 把这个目录变成Git可以管理的仓库
   ```

3. ​

```
 git add readme.txt
 git commit -m "wrote a readme file"
```

4. ```
   git status 命令看看结果
   git diff readme.txt 比较两者的不同
   git log 看看记录
   git reset --hard HEAD^ 退回到上一个版本
   git reset --hard 3333333 回到这个版本
   git reflog 记录每一次命令
   git checkout --readme.txt 丢弃工作区的修改
   当你不但修改了工作区的内容，还添加了暂存区，想丢弃修改，分为两步
   第一步： git reset HEAD file
   第二步： git checkout --file
   git rm 用于删除一个文件

   ```

5. 添加远程仓库

```
git remote add origin git@github.com:raojixian/helloworld.git
git pull 与远程代码保持一致
git push -u origin master 将本地内容推送到远程库上
此后，每次本地提交，就可以使用命令：git push origin master

```

6. 从远程库克隆

```
git clone git@github.com:raojixian/helloworld.git
```

## 分支管理

```
查看分支： git branch
创建分支： git branch <name>
切换分支： git checkout <name>
创建+切换分支： git checkout -b <name>
合并某分支到当前分支： git merge <name>
删除分支： git branch -d <name>
```

```
当git无法自动合并分支时，就必须首先解决冲突，解决冲突后，再提交，合并完成
用git log--graph 命令就可以看到分支合并图
```

