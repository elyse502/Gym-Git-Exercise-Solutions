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

<br /><hr /><br />

## Bundle 2
### Exercise 1
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch
  dev
* ft/bundle-2
  main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<h1>Our Services</h1>" > services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add services.html page"
[ft/bundle-2 e3b6ad4] Add services.html page
 1 file changed, 1 insertion(+)
 create mode 100644 services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push origin -u ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 305 bytes | 152.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
```

### Excercise 2
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ vi services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add services we offer"
[ft/service-redesign 6088d7e] Add services we offer
 1 file changed, 9 insertions(+)
 elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push origin -u ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 346 bytes | 346.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<p>We are here for you</p>" >> services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ cat services.html
<h1>Our Services</h1>
<p>We are here for you</p>
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add new changes"
[main 008a8d0] Add new changes
 1 file changed, 1 insertion(+)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 305 bytes | 305.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
   5fda941..008a8d0  main -> main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git diff main..ft/service-redesign
diff --git a/services.html b/services.html
index d750762..c61b134 100644
--- a/services.html
+++ b/services.html
@@ -1,2 +1,10 @@
 <h1>Our Services</h1>
-<p>We are here for you</p>
+<ul>
+    <li>Web Design<li/>
+    <li>Mobile App Development<li/>
+    <li>Graphic Design<li/>
+</ul>
+
+
+
+
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ vi services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add .; git commit
[ft/service-redesign a2bd91c] Merge branch 'main' into ft/service-redesign
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 363 bytes | 363.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
   6088d7e..a2bd91c  ft/service-redesign -> ft/service-redesign
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
```

<br /><hr /><br />

## Bundle 3
### Exercise 1
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<h1>Our Team</h1>" > team.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add Team Section"
[ft/team-page 78d7b16] Add Team Section
 1 file changed, 1 insertion(+)
 create mode 100644 team.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push origin -u ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 296 bytes | 98.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git branch ft/contact-page
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git log -1
commit 78d7b16b0cb391960de82e56077360a8a704e8fb (HEAD -> ft/team-page, origin/ft/team-page)
Author: elyse502 <elyseniyibizi502@gmail.com>
Date:   Wed Jun 18 11:02:07 2025 +0300

    Add Team Section
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git cherry-pick 78d7b16b0cb391960de82e56077360a8a704e8fb
[ft/contact-page 253508f] Add Team Section
 Date: Wed Jun 18 11:02:07 2025 +0300
 1 file changed, 1 insertion(+)
 create mode 100644 team.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<h1>Our Contacts</h1>" > contact.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add new changes" && git push origin -u ft/contact-page
[ft/contact-page a65e498] Add new changes
 1 file changed, 1 insertion(+)
 create mode 100644 contact.html
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 544 bytes | 108.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ echo "<h1>FAQ</h1>" > faq.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Create faq page" && git pus
h origin -u ft/faq-page
[ft/faq-page e0efb60] Create faq page
 1 file changed, 1 insertion(+)
 create mode 100644 faq.html
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 279 bytes | 55.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git revert 78d7b16b0cb391960de82e56077360a8a704e8fb
[ft/faq-page c3c5dbe] Revert "Add Team Section"
 1 file changed, 1 deletion(-)
 delete mode 100644 team.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 276 bytes | 92.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
   e0efb60..c3c5dbe  ft/faq-page -> ft/faq-page
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
```

### Exercise 2
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ vi faq.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   faq.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add new changes to faq page" && git push
[main 8988189] Add new changes to faq page
 1 file changed, 4 insertions(+)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 349 bytes | 116.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
   5fa6e42..8988189  main -> main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ vi home.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git add . && git commit -m "Add new changes to home page"
[ft/home-page-redesign eac8e42] Add new changes to home page
 1 file changed, 2 insertions(+)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$ git push origin -u ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 322 bytes | 322.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/Gym-Git-Exercise-Solutions$
```

<br /><hr /><br />

## Bundle 4
### Exercise 1
```bash
elysee@DESKTOP-73EL1TL:~$ cd the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
* main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git fetch; git pull
Already up to date.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git remote add git-copy https://github.com/elyse502/Gym-Git-Exercise-Solutions-copy.git
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git remote -v
git-copy        https://github.com/elyse502/Gym-Git-Exercise-Solutions-copy.git (fetch)
git-copy        https://github.com/elyse502/Gym-Git-Exercise-Solutions-copy.git (push)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ ls
README.md  about.html  contact.html  faq.html  home.html  services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ vi home.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git add .; git commit -m "Updated home page"
[main 53f3441] Updated home page
 1 file changed, 4 insertions(+), 2 deletions(-)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 324 bytes | 162.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
   75bd185..53f3441  main -> main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git push git-copy main
Username for 'https://github.com': elyse502
Password for 'https://elyse502@github.com':
To https://github.com/elyse502/Gym-Git-Exercise-Solutions-copy.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/elyse502/Gym-Git-Exercise-Solutions-copy.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git push --force git-copy main
Username for 'https://github.com': elyse502
Password for 'https://elyse502@github.com':
Enumerating objects: 65, done.
Counting objects: 100% (65/65), done.
Delta compression using up to 4 threads
Compressing objects: 100% (55/55), done.
Writing objects: 100% (65/65), 13.89 KiB | 677.00 KiB/s, done.
Total 65 (delta 21), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (21/21), done.
To https://github.com/elyse502/Gym-Git-Exercise-Solutions-copy.git
 + 72d3960...53f3441 main -> main (forced update)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ ls
README.md  about.html  contact.html  faq.html  home.html  services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$
```

### Exercise 2
```bash
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
* main
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ ls
README.md  about.html  contact.html  faq.html  home.html  services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ vi services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git status
On branch ft/footer
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git add .; git commit -m "Add new changes"
[ft/footer 1d1b464] Add new changes
 1 file changed, 9 insertions(+), 8 deletions(-)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ vi services.html
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git status
On branch ft/footer
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git add .; git commit -m "Add second chang
e"
[ft/footer 6fd0e47] Add second change
 1 file changed, 1 insertion(+), 1 deletion(-)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git push origin ft/footer
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 628 bytes | 314.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/footer
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/footer -> ft/footer
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git merge --squash ft/footer
Updating 956b83a..6fd0e47
Fast-forward
Squash commit -- not updating HEAD
 services.html | 17 +++++++++--------
 1 file changed, 9 insertions(+), 8 deletions(-)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git commit -m "service page changes squashing"
[ft/squashing bd8b638] service page changes squashing
 1 file changed, 9 insertions(+), 8 deletions(-)
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$ git push origin ft/squashing
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 390 bytes | 195.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/elyse502/Gym-Git-Exercise-Solutions/pull/new/ft/squashing
remote:
To https://github.com/elyse502/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/squashing -> ft/squashing
elysee@DESKTOP-73EL1TL:~/the-gym-uok/2-sprint/git/Gym-Git-Exercise-Solutions$
```








