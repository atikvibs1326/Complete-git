# Complete-git
-What is git?
Imagine You and your friends are working on a project and 
and everyone is contributing that one project and after some new changes made to the project your application brokes down 
so now you think like what if i would go back to the date before the changes where made to codebase and see actually what went wrong .
So, for this we use git ,Git is a version control system that allows us to keep the track of the project changes  by keeping a log

What is github?
Github is an platform it is an website that gives users a place to manage their git repositories
eg like you have a email system with nice gui so who provides you the amazing gui to interact send/recive mails
Eg: Outlook,Gmail,Yahoomail.and all 


-Setup?
go to Git.csm 
 download git for your preffered OS Mac,Linux,Windows
dont download the git ui Client as we are interacting using command-line-interface.

after installation open the GitBash on windows or directly on mac

-GitCommand

-cd 
 this command used to change the directory from one to        another 
-cd~
 this is used to go back from one directory
-mkdir 
 this used to create new folder

now we know all the history of the project is recorded by the git but how do we see the folder so in the current repository there is ".git" folder which is hidden for everyone
how can we see it?
using the git init command.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------

-git init
this command used to create a new Git repository or initialize an existing directory as a Git repository. When you run git init in a directory, Git creates a new subdirectory named .git that contains all the necessary files to manage the repository. These files include the object database, the configuration files, the index, and the log files.

-touch filename.extension
 this command is used to create a new file in the the folder youre in
	for eg: you do- 
		touch names.txt

Now? in the world does any one know that you did created an file in the project naming as 'name.txt' does this record have been maintained to check this we have a file command known as

git status
this will display the changes that have been made  in this current working directory/folder also it will display the changes as "untracked files"

Now,
Untracked files -> now git does not automatically track these changes .
we need to do it explicility 

for this we use  acommand known as

git add '.' or specific file/folder name

-git add
is a command used to add changes to the staging area in Git. When you make changes to the files in your working directory, Git does not automatically track these changes. You need to explicitly tell Git which changes you want to include in the next commit using the git add command.

The git add command has several different options and forms, but the most common usage is to add all changes to the staging area for the next commit.
The period (.) at the end of the command specifies the current directory and all its subdirectories. This will add all changes in the current directory to the staging area.

You can also use the git add command to add specific files or directories to the staging area
	for eg:
		git add names.txt

to keep the record of this file you need to commit this file for that use command known as

-git commit -m "any message to pass"
	this will commit or in simple language it will take the photo of changes that have been made and will save it in .git folder by the name and his email address
Note : if you haven`t configured email and username this may give error message 
	 in order to that you need to confing username and email to do so.

-git config --global user.name "Your Name"
-git config --global user.email "you@example.com


lets, makes more changes to our names.txt 
 to do so we'll write some data into the names.txt 
-vi names.txt hit enter
	-press i
	-Add data for eg:
		My cat name is
		Bravo he is male cat
		i also have a female cat
		her name is Mylove
	-:x hit enter 
-back to the cli 

-cat "file-name "
 this command is used to display the content inside the file.
	for eg :
		cat names.txt


-if we want to remove from the stage without commit it like we got something on the stage by mistake and now we dont want just want to go back so we have a command known as

-git restore --staged names.txt

-Viewing the overall history of the project we use command known as

-git log
	it basically shows who made what changes at what time in which folder


to delete a file we use a certain command known as

* rm -rf filename
	rm basically used to delete the file and rf is used for forcefully removing the file

git stash
this is a command in the Git version control system that allows you to temporarily save changes that are not yet ready to be committed. This is useful when you need to switch to a different branch or work on a different task without committing the changes you've made so far.

When you run git stash, Git takes all the changes you've made since your last commit and saves them on a new stack of changes. You can then switch to another branch or work on a different task without worrying about the changes you've made interfering with your work.

Later, when you're ready to continue working on the original task, you can use git stash apply to restore the saved changes from the stack back to your working directory. You can also use git stash list to see a list of all the stashed changes you've saved, and git stash drop to remove a specific stash from the stack.

In summary, git stash is a helpful tool for temporarily saving changes that aren't ready to be committed, allowing you to switch tasks without worrying about losing your work or interfering with other tasks.

Now lets Learn about github and how git and github work together
to do so

Goto-Githu.com -to your profile and-create a repository
after creating a repository you wil get an url of the that github repository copy that url .
after copying the Repository url goto git bash and do ass following
- git push origin master and paste the url 
	git push -means all the files push to the repository where the origin is the Url where we want to insert and master means the main branch of the repository.
-Fork
	fork is done to make a copy of exisiting project to your local machine and now you can make the changes or add features or fix bug issues to that local project 
	this will allow user to work and also the main branch is not affected. 
-Upstream 
-the project from where you have forked like the main project repository is called as "upstream"  

