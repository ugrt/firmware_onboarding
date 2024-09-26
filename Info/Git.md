# Git and GitHub
Git is a very useful tool for managing source code and collaboration with others. It allows easy tracking of changes to code, the creation of different branches of code, and the merging of these different branches.

## Git
You can download Git for your OS from the [Git downloads page](https://git-scm.com/downloads).

If you are installing for Ubuntu, you can use the command: ``` sudo apt install git ```.

Depending on your Ubuntu version, you may need to use ```sudo apt-get install <program>```
when installing programs instead, but either format works for the newer versions.

There is an official [git tutorial](https://git-scm.com/docs/gittutorial), but you may find it overwhelming if you have not used Git before. There is also this [interactive Git tutorial](https://learngitbranching.js.org/) which you may find useful for learning some of the more command commands and how they work.

Some of the more common commands you'll use are:
```
git clone <https address or ssh address>    # Copy remote repo to local machine
git checkout -b <new branch>    # Create a new branch and switch to it
git branch  # List existing branches
git checkout    # Switch to existing branch
git pull    # Update local code to match remote code of current branch
git add -A  # Add new files and changes to a commit
git commit -m "<comment changes>"   # Create a commit (add your local changes to the branch)
git push    # Update the remote branch with your current branch commits
```

Most editors/IDEs like VS Code also have a graphical interface for managing your repository, which you may find easier.

### Guidelines
All code will be hosted on GitHub. Once you've cloned a repository you will be working on, you should:
- Create or switch to a branch where you will make the changes related to your task.
- ***Commit often***
  - You are able to view past commits of a branch on GitHub, where you can see the message the author left and the exact changes they made
  - Usually it's best to commit once you have something working, but the main purpose is so it's easy to keep track of when and why things were changed.
  - This also allows you to go back to a previous commit if you make a change the breaks things but you don't know exactly what did it.
  - You should also leave a clear but concise message about the changes made (Ex/ "Added command for motor speed control")
- ***Push often*** and when you've made any important changes
  - Commits are good for tracking changes you've made, but these changes are still on your local machine
  - Pushing to the remote repo ensures you do not lose any work if something happens on your local machine
  - If someone is working on the same branch, allows them to update their local repo to prevent conflicts
- ***Pull before you make changes***
  - You should pull from the remote repo before you make any changes
  - If someone else makes changes to the remote while you are working, there may be conflicts when you try to push your changes
  - Pulling every time you begin working on something and before you push your changes to the remote can reduce conflicts and make conflicts that do happen much easier to manage
- ***Create a Pull Request when done***
  - When you have finished making changes to a branch, it must be merged with the main branch
  - You can create a pull request on GitHub where someone else can review the changes and give feedback if necessary
  - When all looks good, they will merge your changes to the main branch

## GitHub
UGRT code is hosted on GitHub. To clone the repositories and push your own changes, you can use https or ssh. https doesn't require setup but sometimes repositories need ssh.

To setup SSH, you can follow the [instructions from GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

## Tutorial
Here is a quick tutorial to show you the basics.

Once Git is installed, you can clone this repository using:

``` git clone https://github.com/ugrt/REPO_NAME ``` (HTTPS)

or 

``` git clone git@github.com:ugrt/REPO_NAME.git ``` (SSH)

TODO: UPDATE REPO NAME

You may need to set your identity info before calling the above commands:

```
git config --global user.email "<email here>"
git config --global user.name "<your name here>"
```

With the repo cloned, you can view the existing branches with ```git branch```. There should be a branch called "NewFeature". Switch to that branch with ```git checkout NewFeature```.

Now that you are in the NewFeature branch, you should see a folder that wasn't there before "Git Tutorial Files". Open "NewFeature.txt" and make some changes, doesn't matter what.

When you are done with your changes, you can check the status of your repository with ```git status```. Right now, it should tell you that NewFeature.txt is not staged for commit. To stage a specific file, you can run ```git add <PATH TO FILE>``` or ```git add -A``` to add all files in the repository.

Now if you check ```git status```, you'll see the file is staged but still needs to be commited. Run ```git commit -m "<Short message about changes>"```. Then, you can ```git pull``` to make sure your local branch is still up to date (if it's not, you'll have to make another commit with the new changes. You could also run this before you make your commit if you want it all in one commit) and then ```git push``` to push your changes to the remote repository. If you view the branch on GitHub, you should now see your changes.

Once you're changes have been pushed, switch back to the main branch with ```git checkout main```. Your changes should now be gone, since they have not been merged with the main branch. If you switch back, you will find them still there on the NewFeature branch.

Now, you will create your own branch and create a pull request for it to be merged with main. Run ```git checkout -b <BranchName>``` where "\<BranchName\>" is your name or initials.

Add a file to the "GitTutorial Changes" folder. You can call it your name or whatever you want. Make some changes to any other existing files if you'd like or even create some subfolders.

When you are done, follow the same steps as before. ```git pull```, ```git add -A```, ```git commit -m "<Short message>"```, ```git push```.

