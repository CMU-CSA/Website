# Git Collaboration Guide

### Prerequisite
- Git installed locally (available in command line tool)

## All Needed Commands
- `$ git clone git@github.com:CMU-CSA/CSA-Web-Code.git`
- `$ git status`
- `$ git add .`
- `$ git commit` or `$ git commit -m "commit message" `
- `$ git push`
- `$ git fetch`
- `$ git merge`

## Git Configuration

Type in your command line tool:

    $ git config --global user.name "(Your Github Username)"
    $ git config --global user.emal "(Your Github Email)"

## Set up Local Repository

1.  Open your command line tool, **Terminal** or **iTerm**.
2.  Change to a directory that you want to set up as the local respository.
3.  Return to your Github repository just created and click the button on the right bottom near `SSH clone URL`
4.  Type in the following command (after the `$` sign):
        
        $ git clone git@github.com:user_name/repository_name
    
    **Note**: `git@github.com:user_name/repository_name` can be produced by the paste command `Cmd-v`, if you have done 2. above.
    You should get a folder with the same name as the Github repository you just created.

5.  Change the directory to the folder using the command `cd repository_name`.  

Now your have your current directory connected to the Github directory.


## Push Files from Local to Github

1.  Move the files you want to push to Github to the local directory you just set up.
2.  (optional) Type in the following commands (after `$`) in your command line tool, **Terminal** or **iTerm**
    
        $ git status 
    
    You will see the files changed in this directory.

3.  Type in the command:
    
        $ git add .
    
    This step updates the changes in the current directory.

4.  Type in the command:
   
        $ git commit -m "commit message"
    
    where `commit message` can be anything you want to say regard the changed files.
    This step creates a new version of your directory.

    Or

    Type in:

        $ git commit

    Then your default editor will pop up and ask you to write the `commit message`. Save it after finishing writing it.

5.  Type in the command:
    
        $ git push
    
    Now you should have your files pushed to your repository in Github. Refresh your browser and see!


## Pull Files from Github to Local

If there are changes made on the Github repository but not in the local repository, you can:

1.  Open your command line tool.
2.  Get into the directory correspond to the Github repository.
3.  Type in the command:

        $ git fetch

    Then you should have your local files updated.
4.  If you encounter conflicts, type in:

        $ git merge


## Standard of Writing Commit Message
Each time you want to commit something, please specify the following in your commit message:

- **Add new files/functions**, **Modify existing files/functions**, or **Delete files/functions**
- The names of files/functions changed (may inlcude the directory)
- A brief description about what you did

in the format of `[Action] names | Description`

e.g.
  
    $ git commit -m "[Add] views.py/home | Add the home function to the view controller"
    $ git commit -m "[Modify] models.py/activities | Fix a bug in the model"
    $ git commit -m "[Delete] templates/redundant.html | Delete a redundant file"

## Basic Knowledge of Version Control

Each time you make a commit, you actually create a new version of your repository. You can see what was changed by comparing different versions. You can switch versions back and forth. You may also merge versions, etc.

## Some Rules of Collaboration

- Follow the standard to write commit messages.
- Make sure to update your local files (`$ git fetch`) frequently, especially before commit (`$ git commit`).
- Don't have more than one person editing the same files .
