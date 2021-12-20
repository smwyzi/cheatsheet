##### 查看上次 commit 变更文件
```
git log --stat
```

##### 查看上一次 commit 变更内容
```
git show
```

##### 查看某一 commit 变更内容
```
git show COMMIT
```

---

##### 远端覆盖本地
```
git fetch --all &&  git reset --hard origin/master && git pull
```

##### 清空工作区所有修改
```
git clean -df
```

##### 如回退到 n 个版本之前（如 n=2）
```
git reset --hard HEAD^2
```
