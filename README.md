# Basic-Commands - VIEW ON RAW
Basic Commands for Git/Terminal


# Terminal/Git Commands
CLI commands follow the recipe of: command flag argument
  command is something that does the task
  flag is a modulation of the command to do a certain behavior and is preceded by typing a hyphen "-"
  arguments is what the command will modify
  you can have zero arguments or flags, depending on the command

## Some useful commands:

pwd #this prints the path to the current working directory

clear #clears command sin the current working directory

ls #lists files and folders in current directory

ls -a #the -a will list hidden and unhidden files/folders (the -a is a flag!)

ls -al #lists details and hidden folders etc

ls -ltrh #

cd #change directory to home directory

cd .. #change directory one level above

mkdir FileName #FileName is the name of file you want, it makes a directory

touch File_Name #creates empty file called File_name in the working directory

cp file_name Directory_you_want_to_copy_to #takes the file and copies it

cp -r Directory_name Directory_you_want_to_copy_to #copies entire directory

rm file_name #remove file

rm -r Directory_name #remove all the files in the directory, permanent!

mv file_name directory_name #moves file between directories

mv file_name new_renamed_file #makes a new file that is renamed

echo random_text_here #prints out text, allows you to see what variables are stored

## Configuring Git
#in git you need to link up the github and git

git config --global user.name "Your Name Here"

git config --global user.email "your_email@example.com"

git config --list #checks to see if you have user and email in there

# Git and GitHub commands - Intro
#There are multiple ways to create GitHub repositories. One, you could start your own repository from scratch, or two, you can "Fork" another user's repository which means to clone their project and work on it.

## To create a Local Copy of a Repo You Made

#You can create a copy of a repo you made on GitHub to make changes on it 
  #First open Gitbash

#Then create a directory on your computer where you will store the copy of the repo

    mkdir ~/directory_name

#Then navigate to the new directory

    cd ~/directory_name
    
#Now initialize a local Git repository in the directory you moved into

  git init
  
#Point your local repository to the remote repository you made on the GitHub server, this is the link you have for your github

  git remote add origin https://github.com/yourUserNameHere/test-repo.git
  
  
## Fork Another User's Repo
You can fork another user's repo on github. Then you need to make a local copy of it on your computer:

git clone https://github.com/yourUserNameHere/repoNameHere.git


## Basic Git Commands
You're in your workspace, in your computer. You are working on files in your computer. The idea is that you start in workspace, you then add a file you work on into your index of files. Then you add those files to your local repository, by "committing" aka "saving' the file. Finally, you may want to add this new version that you saved to your remote repository which is online, on GitHub. So you "push" (a push command) it there.

Suppose you are working on a directory that is under version control by Git. You need to let Git know that they need to be tracked, and they are added to index.

git add . #add all new files

git add -u #updates tracking for files that changed names or were deleted

git add -A #does both of the previous

Once you have decided that all of these files in your repository are now set to go, and they are lined up in the index you can commit them and save the version LOCALLY.

git commit -m "message" #the message is a useful description on how you changed it

Now you want to put stuff onto GitHub. Push it to GitHub.

git push
  
Now say you want to edit a certain version, or create a different version from the master so you create a "branch". 

git checkout -b branch_name #makes a new branch

git branch #tells you what branch you are on in your working directory of the repo

git checkout master #switches to master branch
  
