#                   	Git \& GitHub $~



jab bhi koii directory ke liye vs code use kar rahi hai to make sure ki yeh jo terminal hai uspai git bash activated ho naa ki comand prompt cmmands work nhi karenge nhi to kuch kuch



--> git configuration



     git config --global user.name "my name"

     git config --global user.email "email@gmail.com"

     git config --list



&nbsp;	There are two types of configurations in git

&nbsp;		\* global - this sets the configuration globally

&nbsp;		\* local - if you want to access or make changes a particular repo/project or a file using a specified email you can change it locally only for that repo

* ## *git basis*



	*git is a version control system. used to track*



	*~ this shows that we are in the root directory (aur is hi folder mai bethkar ham hamre git ko configure karenge )*



	*credential.helper=manager*

		*this credential helper which stores the credential of the user like name, id, email etc.*



* ## *git command*



##### 

1. ##### *clone \& status*



-----------------------------------------------------------------------------------------

 	there are two references remote and local

                       remote --> GitHub
	local --> laptop, pc (this system or the project file on this)

-----------------------------------------------------------------------------------------



###### ||  CLONE - cloning(copy) a repository on our local machine

 

                  git clone <--link of the repo that you want to copy from the remote system(like github)-->



     \\\\ cd - change directory (used for changing path of the terminal where we want to ammend )

                               cd "directory path"

                               dir "list of the files in the directory"

                               ls shows list of file (unhidden)

                               ls -a  shows all the files in the files present hidden and non hidden

                               ls -h only shows unhidden files

              *if there does not exists a file as .git while chehcking the dir then.you can initialize it 														by using \[git init]*

        *{jitni bhi files ko git track kar rha hai usme .git nam ka folder hamesha hota hai}*







###### || STATUS - displays the state of the code

 

                   git status



	**status types**

&nbsp;		\* untracked - new files that git doesn't yet track

&nbsp;		\* modified - changed

&nbsp;		\* staged - file is ready to be comitted

&nbsp;		\* unstaged - unchanged



&nbsp;	change | new file 

&nbsp;	(modifed)    (untracked)

&nbsp;      	     Add (staged)

&nbsp;         commit (unchanged)



     jab bhi ham koii chang yah new file bana hai to usse hame add karna padhta hai and this ADD commes in the "staged" status

&nbsp;	and then if we commit it the status becmoes unchanged 



#####  

##### *2. Add \& Commit*

######  

###### || ADD - adds new or changed files in your working directory to the git staging area.

&nbsp;              

&nbsp;                         git add <--file name-->

&nbsp;    

&nbsp;   if want to add all changes and new file do 	    ------>	**git add .** 



###### || COMMIT - it is the record of changes 

&nbsp;

&nbsp;	commit ka record hota hai add ka koii recod nhi hota hai



&nbsp;                        git commit -m "some message"



&nbsp;yeh message apne liye hota hai thoda meaning ful hona chahiye as this will help in understanding the changes made 



&nbsp;	 {} AFTER COMMITING THE CHANGES IT WILL STILL NOT VISIBLE ON THE REMOTE DIRECTORY GITHUB, ETC. FOR THIS WE HAVE TO PUSH THE COMMAND 

&nbsp;   

&nbsp;	             MESSAGE AFTER COMITING  ---      Your branch is ahead of 'origin/main' by 1 commit.

&nbsp;                                                      (use "git push" to publish your local commits)



##### *3. Push command* 

  

	*push - upload local repo content to remote repo* 



                               *git push origin main*



&nbsp;	git push is the basic command used for pushing the comits

&nbsp;	origin - this sets the changes to the remote repo and is a default name 

&nbsp;	main - here this shows the branch of the repo



##### *4. init command*



*naya project ho to yah existing project mai agar git ka repo bana ke (initialize karne ke )liye use hota hai ".git"*

	*init - used to create a new git repo*

			

				*git init* 

			       *git remote add origin <--link-->(want to add new git repo)*

			       *git remote -v (to verify remote)*

  				*git branch (to check branch)*

     				*git branch -M main (to rename branch)*

				*git push origin main*

                                           *also git push -u origin main (-u set upstream i.e. it will defaut the origin main for all and* 

                                                                           *we dont need to write orgin main AgAAg if working in the same directory for long)*





*------------------------------------------------------------------------*

     cd .. use to return to the parant directory 

&nbsp;    mkdir this is use to make new directory (folder banane ke liye)

**------------------------------------------------------------------------**



#### **WORKFLOW** 

####   **local git**

####      github repo --> clone --> changes --> add --> commit





## 

* ## Git Branches 
* for a repo we can create different branches this branches are for the teams this shares the copy of the main code to the various branches and lets modify the code 
* after the changes comitted to the specific different branches we can merge them to the main stream code 



#### 

1. #### branch commands

&nbsp;  

&nbsp;       git branch  (to check branch)

&nbsp;       git branch -M main (to rename branch)

&nbsp;       git checkout <-branch name-> (to navigate)

&nbsp;       git checkout -b <-new branch name-> (to create new branch)

&nbsp;       git branch -d <-branch name-> (to delete branch)





adding a new branch to check the changes 
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        demotoknowrepo/

nothing added to commit but untracked files present (use "git add" to track)

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        demotoknowrepo/

nothing added to commit but untracked files present (use "git add" to track)

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ git add recept.html
fatal: pathspec 'recept.html' did not match any files

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ git add recept.html
fatal: pathspec 'recept.html' did not match any files

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ cd "C:\Users\muska\Desktop\gitintro\demotoknowrepo"

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        recept.html

no changes added to commit (use "git add" and/or "git commit -a")

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git add recept.html

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git status 
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   recept.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md


presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git add .

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git status 
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   recept.html


presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git commit -m "command doc."
[main 3b9f350] command doc.
 2 files changed, 52 insertions(+)
 create mode 100644 recept.html

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git push origin main
fatal: unable to access 'https://github.com/prathagupta01/demotoknowrepo.git/': Could not resolve host: github.com

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$
 *  History restored 


presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ git push origin main
error: src refspec main does not match any
error: failed to push some refs to 'origin'

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ cd "C:\Users\muska\Desktop\gitintro\demotoknowrepo"

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git push origin main 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 741 bytes | 185.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/prathagupta01/demotoknowrepo.git
   2159118..3b9f350  main -> main

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git status 
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git remote -v
origin  https://github.com/prathagupta01/demotoknowrepo.git (fetch)
origin  https://github.com/prathagupta01/demotoknowrepo.git (push)

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ git branch 
* main

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ ls - a
ls: cannot access '-': No such file or directory
ls: cannot access 'a': No such file or directory

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ ls -a
./  ../  .git/  README.md  recept.html

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ cd . .
bash: cd: too many arguments

presence@Presence MINGW64 ~/Desktop/gitintro/demotoknowrepo (main)
$ cd ..

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ cd"C:\Users\muska\Desktop\gitintro\note"
bash: cdC:\Users\muska\Desktop\gitintro\note: No such file or directory

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ cd notw
bash: cd: notw: No such file or directory

presence@Presence MINGW64 ~/Desktop/gitintro (master)
$ cd note

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ ls -a
./  ../  remoterepo.md

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git init
Initialized empty Git repository in C:/Users/muska/Desktop/gitintro/note/.git/

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git add .

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   remoterepo.md


presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git commit -m "new file on local repo and added a git file"
[master (root-commit) abf6289] new file on local repo and added a git file
 1 file changed, 271 insertions(+)
 create mode 100644 remoterepo.md

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git status
On branch master
nothing to commit, working tree clean

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git remote add origin "https://github.com/prathagupta01/note.git"

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)
$ git git remote -v
git: 'git' is not a git command. See 'git --help'.

The most similar command is
        init

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)   
$ git remote -v
origin  https://github.com/prathagupta01/note.git (fetch)    
origin  https://github.com/prathagupta01/note.git (push)     

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)   
$ git branch 
* master

presence@Presence MINGW64 ~/Desktop/gitintro/note (master)   
$ git branch -M main 

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 2.42 KiB | 413.00 KiB/s, done.  
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/prathagupta01/note.git
 * [new branch]      main -> main

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git status
On branch main
nothing to commit, working tree clean

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git add .

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git add .

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git status 
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md


presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git commit -m "local to remote repo making "
[main 5d53a01] local to remote repo making
 1 file changed, 3 insertions(+)
 create mode 100644 README.md

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git status 
On branch main
nothing to commit, working tree clean

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 466 bytes | 155.00 KiB/s, done. 
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/prathagupta01/note.git
   abf6289..5d53a01  main -> main

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git checkout -b b1
Switched to a new branch 'b1'

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git branch 
* b1
  main

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git checkout -b b2
Switched to a new branch 'b2'

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ gt branch 
bash: gt: command not found

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ git branch
  b1
* b2
  main

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ git branch -d
fatal: branch name required

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ git branch -d b2
error: cannot delete branch 'b2' used by worktree at 'C:/Users/muska/Desktop/gitintro/note'

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ gti branch
bash: gti: command not found

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ git branch
  b1
* b2
  main

presence@Presence MINGW64 ~/Desktop/gitintro/note (b2)       
$ git checkout b1
Switched to branch 'b1'

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git branch -d b2
Deleted branch b2 (was 5d53a01).

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git add .

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git status
On branch b1
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        modified:   remoterepo.md


presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git commit -m "git branch demo"
[b1 0d8cb3c] git branch demo
 2 files changed, 4 insertions(+)

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git branch main
fatal: a branch named 'main' already exists

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git checkout main
Switched to branch 'main'

presence@Presence MINGW64 ~/Desktop/gitintro/note (main)     
$ git checkout b1
Switched to branch 'b1'

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)       
$ git push origin b1
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 389 bytes | 129.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'b1' on GitHub by visiting 
1
remote:
To https://github.com/prathagupta01/note.git
 * [new branch]      b1 -> b1

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)
$ git diff b1

presence@Presence MINGW64 ~/Desktop/gitintro/note (b1)
$ git diff main
diff --git a/README.md b/README.md
diff --git a/README.md b/README.md
index b064dce..ea8b2ce 100644
--- a/README.md
diff --git a/README.md b/README.md
index b064dce..ea8b2ce 100644
--- a/README.md
+++ b/README.md
@@ -1,3 +1,4 @@
 this project has been created locally on the system and then we have created new repo on github then we cpoied the https link anddiff --git a/README.md b/README.md
index b064dce..ea8b2ce 100644
--- a/README.md
+++ b/README.md
@@ -1,3 +1,4 @@
 this project has been created locally on the system and then we have created new repo on github then we cpoied the https link and runned the commands by which we were able to setup a local system repo to a remote system repo.

 if there is a existing project that needs to be uploaded then we can simply commit it.
+
diff --git a/remoterepo.md b/remoterepo.md
index fecbd66..8f6fc37 100644
--- a/remoterepo.md
+++ b/remoterepo.md
@@ -269,3 +269,6 @@ jab bhi koii directory ke liye vs code use kar rahi hai to make sure ki yeh jo t
 ESCOD
diff --git a/README.md b/README.md
index b064dce..ea8b2ce 100644
diff --git a/README.md b/README.md
index b064dce..ea8b2ce 100644
--- a/README.md
+++ b/README.md
@@ -1,3 +1,4 @@
 this project has been created locally on the system and then we have created new repo on github then we cpoied the https link anddiff --git a/README.md b/README.md
index b064dce..ea8b2ce 100644
--- a/README.md
+++ b/README.md
@@ -1,3 +1,4 @@
 this project has been created locally on the system and then we have created new repo on github then we cpoied the https link and runned the commands by which we were able to setup a local system repo to a remote system repo.

 if there is a existing project that needs to be uploaded then we can simply commit it.
+
diff --git a/remoterepo.md b/remoterepo.md
index fecbd66..8f6fc37 100644
--- a/remoterepo.md
+++ b/remoterepo.md
@@ -269,3 +269,6 @@ jab bhi koii directory ke liye vs code use kar rahi hai to make sure ki yeh jo t



+
+
+adding a new branch to check the changes q for quit 
(END)
q
+adding a new branch to check the changes foofw
(END)
