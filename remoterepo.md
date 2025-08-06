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



