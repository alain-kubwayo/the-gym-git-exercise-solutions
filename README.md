# GIT Exercise - Solutions

This project is created to contain all solutions to the series of GIT exercises provided by The Gym Rwanda.

## Bundle 1

### Exercise 1

```bash
➜  git mkdir the-gym-git-exercises
➜  git ls
the-gym-git-exercises
➜  git cd the-gym-git-exercises 
➜  the-gym-git-exercises git init
Initialized empty Git repository in /Users/alain/Documents/the-gym/git/the-gym-git-exercises/.git/
➜  the-gym-git-exercises git:(main) code .
➜  the-gym-git-exercises git:(main) git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
➜  the-gym-git-exercises git:(main) ✗ git add README.md
➜  the-gym-git-exercises git:(main) ✗ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

➜  the-gym-git-exercises git:(main) ✗ git commit -m "initialize project"
[main (root-commit) df498e9] initialize project
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
➜  the-gym-git-exercises git:(main) git remote add origin https://github.com/alain-kubwayo/the-gym-git-exercise-solutions.git
➜  the-gym-git-exercises git:(main) git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 320 bytes | 320.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/alain-kubwayo/the-gym-git-exercise-solutions.git
 * [new branch]      main -> main
➜  the-gym-git-exercises git:(main) git checkout -b dev
Switched to a new branch 'dev'
➜  the-gym-git-exercises git:(dev) git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/alain-kubwayo/the-gym-git-exercise-solutions/pull/new/dev
remote: 
To https://github.com/alain-kubwayo/the-gym-git-exercise-solutions.git
 * [new branch]      dev -> dev
➜  the-gym-git-exercises git:(dev) git checkout -b test
Switched to a new branch 'test'
➜  the-gym-git-exercises git:(test) git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/alain-kubwayo/the-gym-git-exercise-solutions/pull/new/test
remote: 
To https://github.com/alain-kubwayo/the-gym-git-exercise-solutions.git
 * [new branch]      test -> test
➜  the-gym-git-exercises git:(test) git checkout dev
Switched to branch 'dev'
➜  the-gym-git-exercises git:(dev) git branch -D test
Deleted branch test (was df498e9).
➜  the-gym-git-exercises git:(dev) git push origin --delete test
To https://github.com/alain-kubwayo/the-gym-git-exercise-solutions.git
 - [deleted]         test
➜  the-gym-git-exercises git:(dev) 
```

### Exercise 2

```bash
➜  the-gym-git-exercises git:(dev) ✗ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
➜  the-gym-git-exercises git:(dev) ✗ git stash list
➜  the-gym-git-exercises git:(dev) ✗ git add home.html
➜  the-gym-git-exercises git:(dev) ✗ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

➜  the-gym-git-exercises git:(dev) ✗ git stash
Saved working directory and index state WIP on dev: ae3f7c8 add solution to exercise 1 of bundle 1
➜  the-gym-git-exercises git:(dev) git stash list
➜  the-gym-git-exercises git:(dev) git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
➜  the-gym-git-exercises git:(dev) ✗ git add about.html
➜  the-gym-git-exercises git:(dev) ✗ git stash
Saved working directory and index state WIP on dev: ae3f7c8 add solution to exercise 1 of bundle 1
➜  the-gym-git-exercises git:(dev) git stash list
➜  the-gym-git-exercises git:(dev) git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
➜  the-gym-git-exercises git:(dev) ✗ git add team.html
➜  the-gym-git-exercises git:(dev) ✗ git stash
Saved working directory and index state WIP on dev: ae3f7c8 add solution to exercise 1 of bundle 1
➜  the-gym-git-exercises git:(dev) git stash list
➜  the-gym-git-exercises git:(dev) git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (a874b7c9e0ff2af138b33d8b9a30b438697e42f7)
➜  the-gym-git-exercises git:(dev) ✗ git stash list
➜  the-gym-git-exercises git:(dev) ✗ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (641a22f2dee1013b5475e36605071f5ce527346e)
➜  the-gym-git-exercises git:(dev) ✗ git add --all
➜  the-gym-git-exercises git:(dev) ✗ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

➜  the-gym-git-exercises git:(dev) ✗ git commit -m "add home and about pages"
[dev d1c459f] add home and about pages
 2 files changed, 18 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
➜  the-gym-git-exercises git:(dev) git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 518 bytes | 518.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/alain-kubwayo/the-gym-git-exercise-solutions.git
   ae3f7c8..d1c459f  dev -> dev
➜  the-gym-git-exercises git:(dev) git status
On branch dev
nothing to commit, working tree clean
➜  the-gym-git-exercises git:(dev) git stash list
➜  the-gym-git-exercises git:(dev) git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (5518c343ad8310bf7168ce5b462d333122fa66f8)
➜  the-gym-git-exercises git:(dev) ✗ git reset --hard 
HEAD is now at d1c459f add home and about pages
➜  the-gym-git-exercises git:(dev) ✗ 
```
## Bundle 2

### Exercise 2

➜  the-gym-git-exercise git:(main) ✗ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
➜  the-gym-git-exercise git:(ft/service-redesign) ✗ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
➜  the-gym-git-exercise git:(ft/service-redesign) ✗ git add .
➜  the-gym-git-exercise git:(ft/service-redesign) ✗ git commit -m "feat: add list of services"
[ft/service-redesign 450d331] feat: add list of services
 1 file changed, 5 insertions(+)
➜  the-gym-git-exercise git:(ft/service-redesign) git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 407 bytes | 407.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/alain-kubwayo/the-gym-git-exercise/pull/new/ft/service-redesign
remote: 
To https://github.com/alain-kubwayo/the-gym-git-exercise.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
➜  the-gym-git-exercise git:(ft/service-redesign) git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
➜  the-gym-git-exercise git:(main) git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
➜  the-gym-git-exercise git:(main) ✗ git add .
➜  the-gym-git-exercise git:(main) ✗ git commit -m "feat: add old services"
[main 171d685] feat: add old services
 1 file changed, 7 insertions(+), 1 deletion(-)
➜  the-gym-git-exercise git:(main) git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 389 bytes | 389.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/alain-kubwayo/the-gym-git-exercise.git
   6391ea2..171d685  main -> main
➜  the-gym-git-exercise git:(main) git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
➜  the-gym-git-exercise git:(ft/service-redesign) git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
➜  the-gym-git-exercise git:(ft/service-redesign) ✗ git status
On branch ft/service-redesign
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
➜  the-gym-git-exercise git:(ft/service-redesign) ✗ git add services.html
➜  the-gym-git-exercise git:(ft/service-redesign) ✗ git commit
[ft/service-redesign 4b86d54] Merge branch 'main' into ft/service-redesign
➜  the-gym-git-exercise git:(ft/service-redesign) git push origin ft/service-redesign 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 412 bytes | 412.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/alain-kubwayo/the-gym-git-exercise.git
   450d331..4b86d54  ft/service-redesign -> ft/service-redesign
➜  the-gym-git-exercise git:(ft/service-redesign) 