# 命令行&git

## 查

```shell
pwd
ls
ls 目标文件路径
ls -lah

echo hello		# 回声
cat ~/.zshrc

head ~/.zshrc		# 查看前十行
tail ~/.zshrc		# 查看后十行
less ~/.zshrc		# 分页查看, 可移动

# Linux/Mac:
head -n 15 ~/.zshrc		# 查看前 15 行文本,tail 同理
```

## 增

```shell
touch
echo
mkdir
mkdir -p
# 具体见后文的练习
```

## 删

```shell
rm 文件名/目录
rm -r		# 将目录以及以下档案, 逐一删除
rm -f		# 即使原文档属性为只读, 直接删除, 无需逐一确认; 不要问我, 梭哈
rm -rf	# 常用命令
rm -r *	# 删除当前目录下的所有文件及目录
```

## 改
```shell
mv 
# 具体见后文的练习
```

## 练习

```shell
# 增
touch 1.md
echo hi > 2.md
echo hihi >> 3.md
echo -e "1\n2n\3" > 4.md

mkdir x
mkdir -p x/xx/xxx

touch i.md j.md
mkdir y yy

echo world >> 2.md
cp 2.md 22.md

cp -r x z

# 改
mv 22.md new.md

mv new.md x/xx/xxx/xxxnew.md
```

# Git入门

```shell
# 本地仓库
git init		# 初始化一个 git 仓库, 会创建一个 .git 文件夹
git add			# 加入到提交的队列
git commit -v		# 常用推荐, 可以打开编辑器, 多些一些	git 备注信息

# 回滚版本
git reset --hard 版本号		# 回滚到所写版本号, 必须保证所有代码都已提交
git reflog		# 可以查看所有的提交

git log  与 git reflog 的区别
git log 会被上传, 别人可以看到
git reflog 是自己的私有日记, 属于私有

# git 平行开发, 分支
git branch x		# 创建一个名称是 x 的分支
git checkout x		# 切换到 x 分支
# 注意: git branch 是基于当前 commit 创建的一个新的时间线(分支), 是当前的快照, 不是当前代码

# 合并分支
# 切换到保留的分支, 执行 git merge
git merge

# 远程仓库


# git clone
```



### 小结

```sh
# 常用命令其实只有两个
git add
git commit -v
```

