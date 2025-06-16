# GIT Exercise
## Bundle 1
### Exercise 1
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok$ mkdir Gym-Git-Exercise-Solutions
elysee@DESKTOP-73EL1TL:~/the-gym-uok$ cd Gym-Git-Exercise-Solutions/
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/elysee/the-gym-uok/Gym-Git-Exercise-Solutions/.git/
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ touch README.md
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch -M main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git remote add origin https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git remote -v
origin  https://github.com/elyse502/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/elyse502/Gym-Git-Exercise-Solutions.git (push)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Initial project commit"
[main (root-commit) 9f5cded] Initial project commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 222 bytes | 37.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b dev
Switched to a new branch 'dev'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b test
Switched to a new branch 'test'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout dev
M       README.md
Switched to branch 'dev'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch
* dev
  main
  test
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch -d test
Deleted branch test (was 9f5cded).
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch
* dev
  main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
```








