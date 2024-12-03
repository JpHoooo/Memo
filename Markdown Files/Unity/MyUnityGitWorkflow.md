## 我的Unity-Git工作流

1. <mark>创建Unity工程</mark>

2. <mark>打开工程根目录，打开Terminal，输入指令进行Git初始化</mark>

```git
git init    
```

    （此时文件下会生成一个隐藏文件夹`.git`）

3. <mark>建立新的远程仓库</mark>

```git
gh repo create [Name] -g Unity -add-readme --public
```

    （详见：[GitHub CLI | gh_repo_create](https://cli.github.com/manual/gh_repo_create)）    

4. <mark>新建远程连接</mark>

```git
git remote add origin https://github.com/[usernName]/[repoName].git
```

    （详见：[git remote 命令](https://www.runoob.com/git/git-remote.html)）

5. <mark>分支管理</mark>

```git
git branch main
git checkout main
```

    （详见：[Git 分支管理](https://www.runoob.com/git/git-branch.html)）

6. <mark>拉取文件</mark>
   
   *这一步骤主要是拉取远程仓库里的`.gitignore`文件*

```git
git pull origin main
```

    （详见：[git pull 命令](https://www.runoob.com/git/git-pull.html)）

7. <mark>根据项目实际情况修改 `.gitignore` 文件</mark>
   
   *这一步骤主要是以防类似 .vscode / .vsconfig 这类隐藏且无用的文件上传到远程仓库中*

    （详见：[Unity Ignore](https://github.com/github/gitignore/blob/main/Unity.gitignore) 和 [Git Ignore Docs](https://git-scm.com/docs/gitignore)）

8. <mark>添加文件到缓冲区</mark>

```git
git add .
git status
```

    （详见：[git add 命令](https://www.runoob.com/git/git-add.html) 和 [git status 命令](https://www.runoob.com/git/git-status.html)）

9. <mark>提交暂存区到本地仓库</mark>

```git
git commit -m [yout infomation]
```

    （详见：[git commit 命令](https://www.runoob.com/git/git-commit.html)）

10. <mark>传远程代码并合并</mark>

```git
git push origin main
```

    （详见：[git push 命令](https://www.runoob.com/git/git-push.html)）


