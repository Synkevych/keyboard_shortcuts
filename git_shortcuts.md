```git
git init - create new repo 

git config include.path ../gitconfig 
	git show 
	git commit path 
	git add . || * || -A  - added all file to stage pre-commit
	
	git pull - получить последнюю версию с сайта 
	
	git reset - збрасывает все настройки для указаной ветки
	
	git commit -m 'Fixid the problem'

	git commit -a -m 'Rename hello to helloGitty' - не добавляет новые файлы
	
	git push -u origin master - set upstream for git pull/status
	
git remote – покажет все удаленные репозитори
	+ add origin - добавление удаленного адреса 
	+ rename origin somelse  - переименование удаленного репозитория
	+ rm origin – удалит сервер origin
	+ -v  - показать вместе с именем и удаленные адреса 
	+ add [name] git:[url] добавление удалённых репозиториев
	
	git fetch [name] извлечение/получени информации с репозитория
	git push [name]
	git branch [name] || git checkout -b name - создание ветки || и переключение на нее
	git push [name url] [branch name]git

	git reset [path file] - delete file from commit

	git marge [ветка] – слияние веток
	git diff [] [] - сравнивание веток 

	git tag [tag] [первые десять символов соответствующего коммита] - добавление тега
	git log - информация о коммитах
	gitk – программа для просмотра внутренностей проекта
	git checkout -b hotfix - create branch and switch to them

	git rm -n – dry run - удалить папку .git
		-r allow recursive removal 
		-q do not list removed files 

	git clone <repo path> -
	npm install install 
	git merge style – перед зливанням до мастеру треба на нього переключитися

	git rm --cached mylogfile.log - remove file from tree

	git push origin master --force  

	git reset HEAD .gitignore
```
## Git Log Navigating
```git
to scroll down, press
j or ↓ to move down one line at a time
d to move by half the page screen
f to move by a whole page screen

to scroll up, press
k or ↑ to move _up_ one line at a time
u to move by half the page screen
b to move by a whole page screen
press q to quit out of the log (returns to the regular command prompt)

git log --stat 		// display the files that have been changed in the commit, as well as the number of lines that have been added or deleted.

git log --stat -p	// displays both with the stats info above the patch info 

git log -p -w 		// show the patch information, but will not highlight lines where only whitespace changes have occurred. 

git log --oneline 

git diff 		// view changes that have been made but haven't been commited yet
```
### Gitignore configuration, file name - .gitignore
```git
- # marks line as a comment
- * matches 0 or more characters
- ? matches 1 character 
- [abc] - matches a, b, or c
- ** matches nested directories a/**/z matches
**/*.log anywere 
**/app/chache - anywere 
/app/ - at home 
docs/**/*.html - anywere 
```

### Tag used to add point  out particular commits to make them stand out from oters.
```git
git tag -a v1.0 	// create an annotated flag 
git tag -d v1.0 [SHA]	// delete tag with name v1.0 
git branch name SHA	// create new branch and have it point to the commit with SHA
git branch -D sidebar	// remove branch sidebar 
git merge 
git reset --hard HEAD^
git commit --amend	// Alter the most-recent commit 
git revert SHA 		// Reverse given commit
git reset 		// Erases commit 
git checkout -- file.type	//recovery file.type 
git checkout HEAD hello.rb 	//won't show differences
git revert HEAD^		//git try to undo past changes, while any changes made leter will remain untoched
	HEAD^ || HEAD~ || HEAD~1 	// refer to parent commit 
	HEAD^^ || HEAD~2		// refer to grandparent commit
	^	// indicate the parent commit
	~	// indicate the first parent commit
git reset --mixed HEAD~1  or git reset HEAD~1 	// opent current commit files in the Working Directory
git reset --soft HEAD~1  	// move files to the Staging Index 
git reset --hard HEAD~1  	// move files to the Trash and open  previous commit

git commit -a -m "Some message" // Tell the command to automatically stage files that have been modified and deleted, but 	new files you have not told Git about are not affected.

git cherry-pick SHA 	// Apply the changes introduced by some existing commits
git clone url.git folder-name	// if you need change default folder name

git pull 	// Fetch or Sync our local repository with the remote one the same s $ git fetch
git merge origin/master		// idea is merge origin/master with master
```

### Search for errors

```git
git bisect good/bad/reset 	// бынарный поиск помогает быстро проверить сотни коммитов в поисках появившейся ошибки.
git blame -L 12,22 simplegit.rb 	// анотация файла, и ограничить вывод строки с 12-той по 22-рой
```

### File searching
```git
git ls-tree -r master --name-only    // show a list of the files that are being tracked
```
