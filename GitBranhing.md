https://github.com/discover-devops/DevOps_Workbook


====================================

 Introduction to DevOps

 What is Software Development?
 Software Development Life Cycle
Traditional Models for SDLC
Why DevOps?
What is DevOps?
DevOps Lifecycle
DevOps Tools

================================

Linux Ref:

https://www.geeksforgeeks.org/linux-tutorial/ -----> MUST

1: Commands
2: How to install package  apt/yum
3: How to create dir/files
4: Bit of file system



https://www.virtualbox.org/
https://www.geeksforgeeks.org/how-to-install-ubuntu-on-virtualbox/
=================================

Coding : Not needed for this Course.
But if you know, you will have advanatge 
=====================================
Git Installation:
-------------------

https://git-scm.com/download/win
https://git-scm.com/download/mac

Install Git Locally on a LINUX Machine:
-----------------------------------------------
#1: Create an EC2 instance
#2: Install Git

apt-get update
apt-get install git
git --version


These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects



$ git + verb 
e.g  git init


Confiigure Git
----------------

git config --global user.name "devOps"
git config --global user.email "devOps@gmail.com"
git config --global code.editor "path_of_your_editor"

git config --global code.editor "notepad"
git config --global code.editor "vi"




Git $ git init
Initialized empty Git repository in /root/myproject/.git/


Git $ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
Git $


Git $ touch myfile.txt
Git $ ls
myfile.txt

Git $ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        myfile.txt

nothing added to commit but untracked files present (use "git add" to track)
Git $

Git $ git add myfile.txt
Git $
Git $ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   myfile.txt

Git $
Git $ git commit -m "Added a new file"
[master (root-commit) aba1d11] Added a new file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 myfile.txt
Git $

Git $ git status
On branch master
nothing to commit, working tree clean
Git $

Git $ ls
myfile.txt
Git $ echo "This is my new code" > code.py
Git $
Git $ ls
code.py  myfile.txt
Git $ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        code.py

nothing added to commit but untracked files present (use "git add" to track)
Git $
Git $
Git $ git add code.py
Git $ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   code.py

Git $ git commit -m "Added a puthong code file"
[master 72b7d6b] Added a puthong code file
 1 file changed, 1 insertion(+)
 create mode 100644 code.py
Git $
Git $ git status
On branch master
nothing to commit, working tree clean
Git $

Git $ git log
commit 72b7d6b35067c216258b383b411bb740c4f4c51f (HEAD -> master)
Author: devOps <devOps@gmail.com>
Date:   Wed Mar 20 02:49:18 2024 +0000

    Added a puthong code file

commit aba1d1159dfd6d05475d74f76a3d3a4974c4a518
Author: devOps <devOps@gmail.com>
Date:   Wed Mar 20 02:30:28 2024 +0000

    Added a new file
Git $

when ever we are commiting ------> Genereate a # -----> HASH
Ever commit has  it's OWN HASH

----------------
Modify a file example
-----------

Git $ echo "Adding a line" > myfile.txt
Git $ cat myfile.txt
Adding a line
Git $
Git $
Git $ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   myfile.txt

no changes added to commit (use "git add" and/or "git commit -a")
Git $


Modify: git add + git commit

-------

File ----> modify ----> stagging -----> unstage file

======================

GitIgnore
----------
Git $ ls
code.py  myfile.txt  mynewfile.txt
Git $ git status
On branch master
nothing to commit, working tree clean
Git $
Git $
Git $ touch a.mov
Git $
Git $
Git $ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        a.mov

nothing added to commit but untracked files present (use "git add" to track)
Git $


Git $ touch .gitignore
Git $ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        a.mov

nothing added to commit but untracked files present (use "git add" to track)
Git $


Git $ vi .gitignore
Git $
Git $
Git $ cat .gitignore
a.mov
Git $ git status
git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
Git $
Git $ git add .gitignore
Git $ git commit -m "Added GitIgnore File"
[master da559bb] Added GitIgnore File
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
Git $ git status
On branch master
nothing to commit, working tree clean
Git $


========================================

  19  git init
   20  clear
   21  ls -la
   22  cd .git
   23  ls
   24  cd ..
   25  clear
   26  git status
   27  touch myfile.txt
   28  ls
   29  git status
   30  git add myfile.txt
   31  git status
   32  git commit -m "Added a new file"
   33  git status
   34  clear
   35  ls
   36  echo "This is my new code" > code.py
   37  ls
   38  git status
   39  git add code.py
   40  git status
   41  git commit -m "Added a puthong code file"
   42  clear
   43  git status
   44  git log
   45  ls
   46  touch mynewfile.txt
   47  git status
   48  git add mynewfile.txt
   49  git status
   50  git commit -m " Added new file"
   51  git log
   52  clear
   53  ls
   54  echo "Adding a line" > myfile.txt
   55  cat myfile.txt
   56  git status
   57  git add myfile.txt
   58  git status
   59  git commit -m " Modify the file myfile.txt"
   60  git status
   61  git log
   62  clear
   63  ls
   64  vi code.py
   65  ls -lrt
   66  date
   67  cat code.py
   68  git status
   69  git restore  code.py
   70  git status
   71  cat code.py
   72  clear
   73  ls
   74  git status
   75  vi code.py
   76  git status
   77  git add code.py
   78  git status
   79  git restore --staged code.py
   80  git status
   81  "git restore code.py
   82  git restore code.py
   83  git status
   84  cat code.py
   85  clear
   86  ls
   87  git status
   88  touch a.mov
   89  git status
   90  touch .gitignore
   91  git status
   92  vi .gitignore
   93  cat .gitignore
   94  git status
   95  git add .gitignore
   96  git commit -m "Added GitIgnore File"
   97  git status
   98  clear
   99  ls -la
  100  touch b.mov
  101  ls
  102  git status
  103  vi .gitignore
  104  clear
  105  git status
  106  git add .gitignore
  107  git commit -m "Added one more file "
  108  git status
  109  ls
  110  vi .gitignore
  111  git add .gitignore
  112  git commit -m "Addeed new line "
  113  ls
  114  clear
  115  git status
  116  ls
  117  touch 1.mov xyz.mov
  118  ls
  119  git status
  120  cat .gitignore
======================================

Git Branching
-------------------

Git $ git branch
* master
Git $ git branch b100 master
Git $ git branch
  b100
* master
Git $
Git $
Git $ git checkout b100
Switched to branch 'b100'
Git $ ls
1.mov  a.mov  b.mov  code.py  myfile.txt  mynewfile.txt  xyz.mov
Git $
Git $
Git $ touch bug.py
Git $ git status
On branch b100
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        bug.py

nothing added to commit but untracked files present (use "git add" to track)
Git $ git add bug.py
Git $
Git $
Git $ git commit -m "Added a bug file"
[b100 eecd61e] Added a bug file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 bug.py
Git $

Git $ git status
On branch b100
nothing to commit, working tree clean
Git $ git branch
* b100
  master
Git $ ls
1.mov  a.mov  b.mov  bug.py  code.py  myfile.txt  mynewfile.txt  xyz.mov
Git $ git checkout master
Switched to branch 'master'
Git $
Git $
Git $ ls
1.mov  a.mov  b.mov  code.py  myfile.txt  mynewfile.txt  xyz.mov
Git $
Git $ git merge b100
Updating 85d7369..eecd61e
Fast-forward
 bug.py | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 bug.py
Git $
========================

Git $ git merge b500
Merge made by the 'ort' strategy.
 file500 | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file500
Git $ git status
On branch master
nothing to commit, working tree clean
Git $
Git $
Git $ git log
commit fa2b778eba19c8cb826782378e90d5c99494e1f5 (HEAD -> master)
Merge: ff9cfb4 4b2f9ae
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:26:44 2024 +0000

    Merge branch 'b500'

commit ff9cfb4bf93bc5498fda5c7640b19042d3af20b2
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:25:09 2024 +0000

    Added mster file st master branch

commit 4b2f9aefe6c25242b4650e137c874646c2f681e6 (b500)
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:21:53 2024 +0000

    Added the file 500 over branch 500

commit eecd61ec676844c4411c60bd5a80046320fa0ea5
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:02:02 2024 +0000

    Added a bug file

commit 85d73697b5c4d6b5fdae864c22827fdce728f8db
Author: devOps <devOps@gmail.com>
Date:   Wed Mar 20 03:30:46 2024 +0000

    Addeed new line

commit b7fc053394ec97554ad7a742983704ae5cf737d5
Author: devOps <devOps@gmail.com>
Date:   Wed Mar 20 03:24:09 2024 +0000

    Added one more file
Git $
Git $
Git $
Git $
Git $ git branch
  b500
* master
Git $ git branch -d b500
Deleted branch b500 (was 4b2f9ae).
Git $
Git $
Git $ git status
On branch master
nothing to commit, working tree clean
Git $ git log
commit fa2b778eba19c8cb826782378e90d5c99494e1f5 (HEAD -> master)
Merge: ff9cfb4 4b2f9ae
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:26:44 2024 +0000

    Merge branch 'b500'

commit ff9cfb4bf93bc5498fda5c7640b19042d3af20b2
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:25:09 2024 +0000

    Added mster file st master branch

commit 4b2f9aefe6c25242b4650e137c874646c2f681e6
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:21:53 2024 +0000

    Added the file 500 over branch 500

commit eecd61ec676844c4411c60bd5a80046320fa0ea5
Author: devOps <devOps@gmail.com>
Date:   Thu Mar 21 02:02:02 2024 +0000

    Added a bug file

commit 85d73697b5c4d6b5fdae864c22827fdce728f8db
Author: devOps <devOps@gmail.com>
Date:   Wed Mar 20 03:30:46 2024 +0000

    Addeed new line

commit b7fc053394ec97554ad7a742983704ae5cf737d5
Author: devOps <devOps@gmail.com>
Date:   Wed Mar 20 03:24:09 2024 +0000

    Added one more file
Git $
Git $
Git $
Git $






In Git, there are primarily two types of merges:

Fast-forward merge: 
This occurs when the branches being merged have diverged but one branch's commits are all directly reachable from the other branch. In this case, Git can simply move the pointer of the branch being merged into to the latest commit of the other branch. This results in a linear history without creating a merge commit.

Three-way merge: 
This type of merge is used when the branches being merged have diverged and there isn't a simple linear path between them. Git identifies a common ancestor commit for the two branches and then compares the changes made in each branch since that ancestor. It then combines these changes into a new commit, known as a merge commit

=====================

Remote Repo
--------------

echo "# 19thMarch" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main

git remote add origin https://github.com/discover-devops/19thMarch.git
git push -u origin main
