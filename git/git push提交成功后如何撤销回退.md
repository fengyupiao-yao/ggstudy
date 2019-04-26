
# git push提交成功后如何撤销回退 #

1. reset到想要的版本  
   	git reset --soft xxxx  
	git reset --hard xxxx  
	或者使用 git reset --soft HEAD~1  
			git reset --hard HEAD~1  
			HEAD代表当前版本，HEAD~1,就是当前版本-1

2. 查看步骤1中是否恢复正确  
   git reflog： 查看HEAD指向第一步中想要恢复的版本号。  
   git status: 发现代码还在缓存中。

3. 修改
	可修改代码再提交，或是删除。  
	git add xx , git commit ...  
	git rm --cached xx文件名xx

4. 提交  
   git push origin 分支 --force  
   如果是提交到master分支：git push --force


----------

参考文献：[https://guozh.net/?p=166](https://guozh.net/?p=166 "git push提交成功后如何撤销回退")

