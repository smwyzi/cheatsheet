##### 查看上次commit变更文件
```
git log --stat
```

##### 查看上一次commit内容
```
git show
```

##### 查看某一commit变更内容
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

##### 如回退到n个版本之前（如n=2）
```
git reset --hard HEAD^2
```
