# Lab 03: Git and GitHub
This repository documents my practice with 
local Git, GitHub, branches, and pull requests.

## README Responses

### 1.1 After initialization
```text
ls -la
total 16
drwxr-xr-x 3 user user 4096 Sep  3 10:42 .
drwxr-xr-x 5 user user 4096 Sep  3 10:41 ..
drwxr-xr-x 6 user user 4096 Sep  3 10:42 .git
-rw-r--r-- 1 user user  878 Sep  3 10:42 README.md
```

### 1.2 First git status
```text
git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
```

### 1.3 After the first commit
```text
git status
On branch main
nothing to commit, working tree clean
```

### 1.4 git log
```text
git log --oneline
7b8c4a6 Create lab README
```

### 1.5 git diff

Paste the `git status` and `git diff` commands and their output.
```text
git status
On branch main

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

git diff
diff --git a/README.md b/README.md
index 660e9ad..e4943d2 100644
--- a/README.md
+++ b/README.md
@@ -1,4 +1,6 @@
 # Lab 03: Git and GitHub
+This repository documents my practice with 
+local Git, GitHub, branches, and pull requests.
 
 ## README Responses
 
@@ -27,8 +29,25 @@ nothing added to commit but untracked files present (use "git add" to track)
 ```
 
 ### 1.3 After the first commit
+```text
+git status
+On branch main
+nothing to commit, working tree clean
+```
 
 ### 1.4 git log
+```text
+git log --oneline
+7b8c4a6 Create lab README
+```
 
 ### 1.5 git diff
 
```

How does this `git status` differ from the one in **1.2**?
This `git status` tracks our README while **1.2** doesn't since that was before we added it
We can see this as this `git status` tells us our README is modified rather than untracked

### 1.6 Git command reflections

In one or two sentences each, what does each command do?

- `git init`: Creates a new git repository (.git) in the current directory
- `git status`: Prints the status of the working tree (untracked files, modified, added)
- `git add`: Adds the specified file or directory (recursively) to staging meaning it keeps track of it
- `git commit`: Creates a new commit node (message + hash) containing whatever was added
- `git log`: Shows a history of the current branches' commits
- `git diff`: Shows the changes made in files that haven't been committed

### 1.7 Repository link

### 1.8 Comparing approaches

In your own words:

- How does the nested-loop approach check for a duplicate?
- How does the set-based approach check for a duplicate?
- What is the runtime and memory trade-off of each?

### 1.9 Pull request merge options

In your own words, what does each GitHub merge option do?

- Create a merge commit
- Squash and merge
- Rebase and merge
