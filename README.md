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

### Exercise 2
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<h1>Hello, World</h1>" > home.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add .
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash
Saved working directory and index state WIP on main: ba6b00a Add Solution to Exercise 1
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<p>I am a trainee at the Gym</p>" > about.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add .
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash
Saved working directory and index state WIP on main: ba6b00a Add Solution to Exercise 1
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<h2>Our Team</h2>" > team.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git stash
Saved working directory and index state WIP on main: ba6b00a Add Solution to Exercise 1
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ ls
README.md
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash list
stash@{0}: WIP on main: ba6b00a Add Solution to Exercise 1
stash@{1}: WIP on main: ba6b00a Add Solution to Exercise 1
stash@{2}: WIP on main: ba6b00a Add Solution to Exercise 1
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash pop 1
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped refs/stash@{1} (856d2482b2bb9a4c9dfd2269ad0dfb9c802aa532)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ ls
README.md  about.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash list
stash@{0}: WIP on main: ba6b00a Add Solution to Exercise 1
stash@{1}: WIP on main: ba6b00a Add Solution to Exercise 1
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash pop 1
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (eecd2301dfb1a368665c91fd6a115d277c2ee1d3)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git commit -m "Add home and about pages" && git push
[main 4904368] Add home and about pages
 2 files changed, 2 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 381 bytes | 42.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
   ba6b00a..4904368  main -> main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash list
stash@{0}: WIP on main: 4904368 Add home and about pages
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (186fcc69be3695ca7ac6af456b548aedd1912f35)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git reset --hard
HEAD is now at 4904368 Add home and about pages
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
```







