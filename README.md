# Git-Exercise-Solutions

# Bundle 1
## Exercise 1

```bach
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git init
Reinitialized existing Git repository in C:/Users/princ/Desktop/DEV/Git-Exercises/.git/
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch -M main
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git commit -m "ft(ReadMe)
>>
>> - Adding the README file and its content
>>
>> "
[main (root-commit) e553fef] ft(ReadMe)
 1 file changed, 1 insertion(+)
 create mode 100644 README
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git remote add origin https://github.com/princoo/Bundle-1-Ex-1-Repo.git
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 286 bytes | 286.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push origin
fatal: The current branch test has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin test

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\princ\Desktop\DEV\Git-Exercises>     git push --set-upstream origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/princoo/Bundle-1-Ex-1-Repo/pull/new/test
remote: 
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch -r
  origin/main
  origin/test
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git switch dev
Switched to branch 'dev'
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch
* dev
  main
  test
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push origin
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\princ\Desktop\DEV\Git-Exercises>     git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/princoo/Bundle-1-Ex-1-Repo/pull/new/dev
remote:
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch
* dev
  main
  test
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch -r
  origin/dev
  origin/main
  origin/test
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch -D test
Deleted branch test (was e553fef).
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push origin --delete test
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
 - [deleted]         test
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch -r
  origin/dev
  origin/main
PS C:\Users\princ\Desktop\DEV\Git-Exercises>

```


### Exercise  2

```bash
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash
Saved working directory and index state WIP on dev: e553fef ft(ReadMe)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash
Saved working directory and index state WIP on dev: e553fef ft(ReadMe)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add team.html
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash
Saved working directory and index state WIP on dev: e553fef ft(ReadMe)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash list
stash@{0}: WIP on dev: e553fef ft(ReadMe)
stash@{1}: WIP on dev: e553fef ft(ReadMe)
stash@{2}: WIP on dev: e553fef ft(ReadMe)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash pop 1        
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped refs/stash@{1} (2d9942ae008ca299007556c09b07c7e425ae56e9)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash list
stash@{0}: WIP on dev: e553fef ft(ReadMe)
stash@{1}: WIP on dev: e553fef ft(ReadMe)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash pop 1
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (44ceb6ceee22406c6079b7d9cc63b6d856e97c3d)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git commit -m "adding unstashed changes to remote"
[dev aeb2e31] adding unstashed changes to remote
 2 files changed, 20 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 430 bytes | 430.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
   e553fef..aeb2e31  dev -> dev
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash list
stash@{0}: WIP on dev: e553fef ft(ReadMe)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git stash pop 0
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (d25fa2cfcebffa3a58d7bccba14dd4e9c4544daa)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git reset --hard
HEAD is now at aeb2e31 adding unstashed changes to remote
PS C:\Users\princ\Desktop\DEV\Git-Exercises> 

```



