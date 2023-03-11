# Git的奇技淫巧
--------------
技能可以以后再学

但

帅和酷是一辈子的事情😎

---

# Git
--------------
1. 分布式版本管理工具
2. 敏捷开发
3. 开源

---

# 大纲
--------------
1. 十八般武艺
2. 代码冲突 
3. 远程仓库
4. 压缩提交
5. 标签
6. 致谢


---

# 1. 十八般武艺01
--------------

```git[1|2|3|4]
git stash save "xxx" #临时保存修改的文件
git log --oneline --graph # 日志单行流程图
git push :branch_name #删除远端分支
git rm --cached filename # 取消追踪某个文件
```

---

# 1. 十八般武艺02
--------------

```[1|2|3]
git commit --amend # 提交一个commit但是记录到上一次log中
git cherry-pick commit-id # 提交特定一次修改
git archive -o archive.zip master # 文件快照打包

```

---

# 2. 代码冲突
--------------
```git
git merge  master
git rebase -i master
```

---

# 3. 远程操作
--------------
如何将本地文件和远程仓库文件关联起来？
```git[1 | 2-3 | 4-7]
git remote -v 
git remote add origin git@github.com:SYaoJun/Sildes.git 
git remote rm origin 
# 设置上游分支
git push -u origin master 
# 从远程仓库获取指定分支
git checkout -b local_branch_yy origin/remote_branch_yy  
```

---
# 4. 压缩提交记录
--------------
如果有多次提交记录

却只想保留一条记录怎么办?

---

# 4.1 方法一 reset
--------------
```
git reset commit-id  
git add filename
git commit -m "xxx"
```

---

# 4.2 方法2 amend
--------------
``` git
# 每次压缩一条提交记录
git commit --amend "xxx" 
```

---

# 4.3 方法三 rebase
--------------
```
git rebase -i commit-id #想要压缩内容的前一次提交
pick ef124f 保留
squash fa4f8d 压缩
```
---

# 5. 标签
--------------
不同版本v1.0.0的由来
```
git tag tag_name
git tag tag_name commit-id
git tag -a tag_name -m "xxx" commit-id
git tag
git show tag_name
git push origin tag_name # 推送到远程仓库
```

---

# 6. 致谢
--------------
- 感谢知乎@游凯超文章

- 感谢CSDN@zhaoyang10文章