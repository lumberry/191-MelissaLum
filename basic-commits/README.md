# Git Kata: Basic Commits
This kata will introduce you to the `git add` and `git commit` commands.

This is a very introductory kata. if you have used `git status`, `git log --oneline --graph`, `git add` and `git commit` extensively you should probably skip it.

You can look at the bottom of this file, if you have not yet done basic git configuration.

## Setup:

1. Run `. setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

1. Use `git status` to see which branch you are on.
	On branch master

	No commits yet
	
2. What does `git log` look like?
	fatal: your current branch 'master' does not have any commits yet
	
3. Create a file
4. What does the output from `git status` look like now?
	On branch master

	No commits yet

	Untracked files:
	  (use "git add <file>..." to include in what will be committed)
			file1.txt

	nothing added to commit but untracked files present (use "git add" to track)

5. `add` the file to the staging area
6. How does `git status` look now?
	On branch master

	No commits yet

	Changes to be committed:
	  (use "git rm --cached <file>..." to unstage)
			new file:   file1.txt
			
7. `commit` the file to the repository
8. How does `git status` look now?
	On branch master
	nothing to commit, working tree clean
	
9. Change the content of the file you created earlier
10. What does `git status` look like now?
	On branch master
	Changes not staged for commit:
	  (use "git add <file>..." to update what will be committed)
	  (use "git restore <file>..." to discard changes in working directory)
			modified:   file1.txt

	no changes added to commit (use "git add" and/or "git commit -a")
	
11. `add` the file change
12. What does `git status` look like now?
	On branch master
	Changes to be committed:
	  (use "git restore --staged <file>..." to unstage)
			modified:   file1.txt
			
13. Change the file again
14. Make a `commit`
15. What does the `status` look like now? The `log`?

`git status`
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   file1.txt

no changes added to commit (use "git add" and/or "git commit -a")

`git log`
commit c289916fd86b115db2e555ccaae207dbaaea6100 (HEAD -> master)
Author: melissa <lumma@uci.edu>
Date:   Fri Jan 24 18:15:55 2020 -0800
	we are making more changes

commit 0d2af0c5c58e1b18a444fc5a3e1adb0595fc12a1
Author: melissa <lumma@uci.edu>
Date:   Fri Jan 24 18:12:34 2020 -0800 
	committing testing file!
	
16. Commit the newest change

## Useful commands
- `git add`
- `git commit`
- `git commit -m "My commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` to create a file (or `sc filename ''` in PowerShell)
- `echo content > file` to overwrite file with content (or `sc filename 'content'` in PowerShell)
- `echo content >> file` to append file with content (or `ac filename 'content'` in PowerShell)


## Git Initial Configuration
1. `git config --global user.name "John Doe"`
1. `git config --global user.email "johndoe@example.com`

For the vim scared:
- `git config --global core.editor nano`

For the windows peeps:
- `git config --global core.editor notepad`

Other editor options:
- `git config --global core.editor "atom --wait"`
- `git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst"`
