#### 查看某一 commit 属于哪个分支
```
git branch -r --contains COMMIT
```

#### 查看上次 commit 变更文件
```
git log --stat
```

#### 查看上一次 commit 变更内容
```
git show
```

#### 查看某一 commit 变更内容
```
git show COMMIT
```

---

#### 远端覆盖本地
```
git fetch --all &&  git reset --hard origin/master && git pull
```

#### 清空工作区所有修改
```
git clean -df
```

#### 如回退到 n 个版本之前（如 n=2）
```
git reset --hard HEAD^2
```

---

### github fork repo workflow
```
# add upstream
git remote add upstream https://github.com/whoever/whatever.git

# update local and origin
git checkout master
git pull upstream master --rebase
git push origin master -f

# develop on feature branch
git checkout -b feature
git add .
git commit -m "add feature foo"

# push feature branch
git checkout master
git pull upstream master --rebase
git checkout feature
git rebase master
git push origin feature -f

# submit pull request

# after pull request merged, update local and origin
git checkout master
git pull upstream master --rebase
git push origin master -f
```