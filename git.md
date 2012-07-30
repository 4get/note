git --bare init
远程仓库必须使用 git --bare init 初始化 

git remote add origin ssh://yangyaowu@172.16.55.253/home/yangyaowu/apollo_linux-2.6.34.git
git push origin master 

git push origin :testing
删除远程的testing分支 

git push origin testing:master
将本地的testing 分支合并到远程的master分支

git push origin testing:testing
将本地的testing分支合并到远程的testing分支，如果远程不存在testing分支，则在远程创建testing分支

常用 -p 选项展开显示每次提交的内容差异，用 -2 则仅显示最近的两次更新
git log -2
git log -p -2
-p 按补丁格式显示每个更新之间的差异。
--stat 显示每次更新的文件修改统计信息。
--shortstat 只显示 --stat 中最后的行数修改添加移除统计。
--name-only 仅在提交信息后显示已修改的文件清单。
--name-status 显示新增、修改、删除的文件清单。
--abbrev-commit 仅显示 SHA-1 的前几个字符，而非所有的 40 个字符。
--relative-date 使用较短的相对时间显示（比如，“2 weeks ago”）。
--graph 显示 ASCII 图形表示的分支合并历史。
--pretty 使用其他格式显示历史提交信息。可用的选项包括 oneline，short，full，fuller 和 format（后跟指定格式）。

git log --since=2.weeks
-(n)        仅显示最近的 n 条提交
--since, --after 仅显示指定时间之后的提交。
--until, --before 仅显示指定时间之前的提交。
--author 仅显示指定作者相关的提交。
--committer 仅显示指定提交者相关的提交。

git checkout 6b88043702c545c77542fcec12be0ac18e878ed8 -b zp // checkout一个叫zp的分支, 使用id为6b...8ed8的版本

git reflog
git reset --hard HEAD@{12}
git reset --hard 6b88043702c545c77542fcec12be0ac18e878ed8

git-config --list

git gc
git gc --aggressive
git prune

http://liuhui998.com/2010/11/06/remove_commits_completely/
当我们在执行git gc命令时，它会调用git prune命令把这些悬空对象(dangling objects)清除掉(prune)；一般默认是清除超过二周的悬空对象。
git reflog expire --expire-unreachable=0 --all
git gc --prune=0
git fsck --lost-found

在每个clone下来的仓库中手动设置不要检查特定文件的更改情况,每个新的仓库都必须手动设置一次.
git update-index --assume-unchanged /path/to/file

--ignore-paths="^tags/old*|^tags/builds*|
git svn clone --ignore-paths="^others/product_tools*|^others/u_rescovery*|^others/生产工具*|^others/crosstool-ng*|^others/bootloader_h2*" svn://172.16.68.158/trident cowork_trident_3mimi

--------------------------------------------
git log --pretty=format:"%h - %an, %cr, %cd : %s"
选项   说明
%H  提交对象（commit）的完整哈希字串
%h  提交对象的简短哈希字串
%T  树对象（tree）的完整哈希字串
%t  树对象的简短哈希字串
%P  父对象（parent）的完整哈希字串
%p  父对象的简短哈希字串
%an 作者（author）的名字
%ae 作者的电子邮件地址
%ad 作者修订日期（可以用 -date= 选项定制格式）
%ar 作者修订日期，按多久以前的方式显示
%cn 提交者(committer)的名字
%ce 提交者的电子邮件地址
%cd 提交日期
%cr 提交日期，按多久以前的方式显示
%s  提交说明

git log --pretty=format:"%h %s" --graph
选项 说明
-p 按补丁格式显示每个更新之间的差异。
--stat 显示每次更新的文件修改统计信息。
--shortstat 只显示 --stat 中最后的行数修改添加移除统计。
--name-only 仅在提交信息后显示已修改的文件清单。
--name-status 显示新增、修改、删除的文件清单。
--abbrev-commit 仅显示 SHA-1 的前几个字符，而非所有的 40 个字符。
--relative-date 使用较短的相对时间显示（比如，“2 weeks ago”）。
--graph 显示 ASCII 图形表示的分支合并历史。
--pretty 使用其他格式显示历史提交信息。可用的选项包括 oneline，short，full，fuller 和 format（后跟指定格式）。

git log --since=2.weeks

git log -1 --pretty=%ci



==
统计
提交最多的文件
git log --name-status  | grep "^M" | sort | uniq -dc | sort -nr
git log --name-status  | grep "^M" | sort | uniq -dc | sort -nr | head -40

统计文件$f的提交次数
git log --pretty=%ai $f | cut -c 1-4 | sort | uniq -dc 
git log --pretty=%ai $f | cut -c 1-7 | sort | uniq -dc 

git format-patch  -1 #version

patch -p1 < *.patch 
使用 git -diff产生的patch都应该在patch(1)时指定-p1
