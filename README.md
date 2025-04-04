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



## Bundle 2
### Exercise 1

```bash
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git commit -m "feat: add initial HTML structure for service page"
[ft/bundle-2 6f49858] feat: add initial HTML structure for service page
 1 file changed, 10 insertions(+)
 create mode 100644 service.html
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\princ\Desktop\DEV\Git-Exercises>     git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 443 bytes | 443.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/princoo/Bundle-1-Ex-1-Repo/pull/new/ft/bundle-2
remote:
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises>

```

### Exercise 2

```bash

PS C:\Users\princ\Desktop\DEV\Git-Exercises> git pull
Updating 6f49858..557b174
Fast-forward
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git commit -m "fix: update service page content"
[ft/service-redesign 92ddd33] fix: update service page content
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\princ\Desktop\DEV\Git-Exercises>     git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 179.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/princoo/Bundle-1-Ex-1-Repo/pull/new/ft/service-redesign
remote:
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git commit -m "changing service page content"   
[main ece6f8a] changing service page content
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Merge branch 'main' into ft/service-redesign
Writing objects: 100% (3/3), 343 bytes | 343.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
   557b174..ece6f8a  main -> main
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git add .
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git commit
[ft/service-redesign f32278a] Merge branch 'main' into ft/service-redesign
PS C:\Users\princ\Desktop\DEV\Git-Exercises> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 374 bytes | 374.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/princoo/Bundle-1-Ex-1-Repo.git
   92ddd33..f32278a  ft/service-redesign -> ft/service-redesign
PS C:\Users\princ\Desktop\DEV\Git-Exercises> 

```

