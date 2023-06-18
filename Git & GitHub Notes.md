## Git Setup
To setup Git on a Mac:
1. Open a new terminal.
2. Type *git* and press enter.
3. If Git is not installed a prompt will appear to install.
4. Setup authentication to keep your work secure and prevent anyone not authorised from making changes to your repositories (Likely SSH).

## Initialising a Git Repository
The below is an example of a process to create a practice repository:
1. In the terminal type *mkdir **git_practice*** to create a new directory (git_practice can be replaced with whatever you wish to call the new directory).
2. To then navigate to this new directory use *cd **git_practice***.
3. To turn this new directory into a Git repository use *git init*, not needed if a repository has already been cloned.
4. To create a new file with sample test for this repository use *echo "Hello Git and GitHub" >> README.txt*.
5. To then add the new file to the staging area use *git add README.txt*.
6. Finally to commit the new file use *git commit -m "First commit"*.

## Linking a Repository to GitHub
The below is an example process for creating a new repository on GitHub for the practice repository initialised above:
1. On GitHub on the repositories section, click new.
2. On the next page it will ask you to add a name for your repository, it is good practice to name this the same as the directory that you created and initialised previously. Once yo have named this click create repository.
3. Once created select the authentication method that is being used (SSH in this case).
4. To then link your local repository to GitHub copy the code displayed as "…or push an existing repository from the command line".
5. Once the command line reports that it has been complete refresh the page on GitHub and then text file created earlier should display.

## README File
When the GitHub repo is initialised you are prompted to create a README.md file, this file is meant to be read as soon as someone opens the project in GitHub, the aim of this document is to introduce, explain and share information required to understand what the project is about.

Elements to include on a README file should include:
- **Project Title** - The name of the project.
- **Description** - You should always describe the main purpose of the project, this should include things like answers to the following:
	- Why did you build this project.
	- What problems does this project solve.
  Also include your motivations for the project and what you have learned from it.
- **Features** - If your project has multiple features then you should list them good features are a way to make your project standout.
- **How to Use** - It's beneficial to write a step-by-step list of instructions on how to install and use your project, as well as including any software or package requirements.
- **Technologies** - Use this part to list all the technologies and/or frameworks used and the purpose that they served.
- **Collaborators** - If anyone has contributed to the project in anyway it's important to give them credit for their contribution. Include an team member or collaborators names, as well as a link to their profile on GitHub.
- **License** - It's important to list a licence on the README as it lets collaborators know what they may or may not be allowed to change on your project.

READMEs should be brief but also detailed, it's important to keep them up to date and self-explanatory with no ambiguity. The amount of time spent working on the project should be reflected in the amount of time that is spent writing the README, this can be beneficial if you ever were to step away from the project and need to reacquaint yourself, it will also leave a positive impression on anyone who views your profile.

## Markdowns With READMEs
Using markdown formatting for your READMEs allows for a more interesting read, have plain unformatted text can be uninteresting to read and in some cases hard to follow depending on how much work has been put into it. Including a README with the file extension .md allows these files to be formatted with markdown.

## Cloning the Repository
To clone the repository you first have to navigate to the location you would like to clone it to, this can be done by using *ls*, to list the directories & *cd **directory*** to navigate to that directory (*directory being the name of the directory you wish to clone the repository to*.

To then clone the repository you will have to use *git clone* followed by the link of the repository that you can copy from GitHub.

## Branch Management
When working as a team on a repository it's important to keep any code you are woking on isolated from the main repository so that you don't make any changes that could be detrimental to someone else's code. For this we create a branch which is a divergence of the main repository and allows any changes to be stored and saved without affecting the main branch. (Branches can also be created from other branches).

From these branches the changes can then be reviewed by others and eventually merged back into the main, it's important that only clean code is merged back into the main branch as this essentially is the complete working version of the project.

When changes have been made on the branch and you are happy with the code that is written it's important to commit along with an associating commit message, once confident that the changes are good you can push the commit to the remote GitHub repository.

Pull requests allow for the team to collaborate and propose changes to the branch before it is merged into the main branch making the changes a permanent part of the project. When creating a pull request it's important to include as much information as possible to inform all concerned parties of your intentions with the changes made the more detail you include the less guess work that is involved when reviewing the branch. It is good practice to not alter to many files at once on a single branch as it can complicate the review process.

When reviewing a pull request fro someone else's branch it is good practice to be as constructive as possible with any feedback you provide, not only say what should be changed but also explain why you think it should be changed. It's important to be clear on the suggested changes so there is no mistake as to what should be changed. In addition to these think towards the future as well, if these changes when implemented could affect some things that could be added in the future, foresight to future possibilities can allow for code to be written so they don't need to be modified later.

Once all changes have been approved the branch can then be merged back into the main repository and then deleted to keep things tidy.

## Creating a New Branch
You will want to be able to make changes without affecting others who may be using the same repository, for this we need to create a new branch where we can commit changes without disturbing the main repository.

## Git Branch
Before you create a new branch it is good practice to check the current branch that your local repository is on, this can be done by using *git branch* which will then display the current branch. The branch you are working on is displayed with an asterisk.

To create a new branch use *git branch* followed by the name of the branch you want to create, this name cannot contain any white spaces, you can use either "-" or "*_*" for word breaks.

## Changing the Branch
In order to change the current branch that is being worked on you will have to use the command *git checkout* followed by the name of the branch you wish to switch to.

## Switch and Create (One Command)
It is possible top both create and switch to a new branch with a single command, to do this the command is *git checkout -b* followed by the name of the branch you want to create, this will create a new branch and switch to it as well.

## Git Initialise
To initialise a project use **git init**, this command will set up all the tools Git needs to track any project changes.

## Git Workflow
Git projects consist of 3 parts:
1. Working Directory - Where all the work will be done, creating, editing, deleting, organising files.
2. Staging Area - Where changes to the Working Directory will be listed.
3. Repository - Where Git will permanently store the changes as an alternate version of the project
The Git process is, editing in the Working Directory, adding files to the Staging Area & saving changes to a Repository, changes are saved with a commit.

## Git Status
You can check status of any changes using **git status**, any new files added can be visible by Git and will be shown in RED to display that it has not yet started to track these changes.

## Git Add
For Git to start tracking newly added files or changes to already existing files they need to be added to the Staging Area, this can be done with **git add *filename***. (*filename* referring to the full name of the file you are adding or have made changes to), you can add as many files as you need to add by also adding the name of those files, alternatively with *git add .* you can add all new or modified files in one go instead of individually.

Once this is done the file will be green to display that it is now in the Staging Area and ready to be committed.

## Git Diff
For files added to the Staging Area, any further changes made in the Working Directory can be can be compared back to the version in the Staging Area, this can be achieved with "git diff ***filename***", any lines that would not have changed will be displayed in **White**, any additions will be indicated with a "+" prefix and the line itself will be **Green**. These changes can be moved to the Staging Area with the previous git add.

## Git Commit
A commit is the final step and permanently stores changes from the Staging Area inside the Repository. This can be achieved with **git commit -m "*message*"** (the *message* should describe the point of the commit).
Commit message conventions:
- Must be in quotation marks.
- Must be written in the present tense.
- Should be 50 characters or less.

## Git Log
If you need to refer back to an earlier version of a project this can be achieved with *git log*, this will display all commits chronologically with the following outputs:
- 40 character code (SHA) to uniquely identify the commit, shown in **Orange**.
- The author of the commit.
- The date and time of the commit
- The message defined during the commit.

## Additional Log Functions
- *git log --oneline* - Used to display the commits in a single line format, first 7 characters of the SHA followed by the commit message.
- *git  log -s "keyword"* - Displays a list of commits that contain your selected keyword.
- *git log --oneline --graph* - Displays a more visual representation of how the branches and commits are alongside the main repository, the use of *--oneline* shortens the overall description without it the display will become quite long.

## Git Commit Amend
If you are working on a commit that you realise you have forgot a few minor aspects like adding semi-colons to the end of lines you can easily amend the current commit by using *git commit --amend*, what this does is technically replace the entire previous commit with this new one so will prompt you to edit your commit message, however if you have no need to change your message you can just include *--no--edit* following the first bit of code.

## Git Alias Commands
When grouping commands it's easy to end up writing quite long lines of code in the terminal, to ease this process there is a feature that allows you to create an alias for each command using the following *git config --global alias.**name** "command"* the command being the name of the command you wish to create an alias for and the  name being the alias that you wish to assign to that command.

For example *git config --global alias.co "checkout"* would assign "checkout" with the alias "co" shortening the code that needs to be typed out to complete a command.

You can also wrap a sequence of Git commands that you may use regularly under and alias to increase efficiency.

## Head Commit
When using Git, the commit you are currently on is called the "HEAD" commit, this will be the most recent commit unless changed. To check this the command will be *git show HEAD*. The additions of the HEAD commit will be shown in **Green**.

## Git Checkout
If you make any changes since the last commit and then suddenly decide that you would like to remove those changes you can use the command *git checkout HEAD* followed by the name of the file where the changes have been made, this will restore it to how it looked in the HEAD commit (closing the file and re-opening it will display those changes).

If you are wanting to restore multiple files to the HEAD commit then the command will be *git checkout HEAD .* (allows multiple files to restored to the previous commit).

## Git Reset
If you make any unwanted changes to a file that are then added to the staging area, you can remove that file from the staging area before a commit allowing you to only commit the changes that you want, this can be done with *git reset HEAD* followed by the filename you would like to remove.

In addition to the above if there are any changes a commit that are unwanted you can rewind back to a previous commit restoring the HEAD back to this point, this can be achieved with *git reset* followed by the first 7 characters of the SHA of the commit you wish to revert back to.

## HEAD Shortcut
A shortcut that can be used instead of writing out HEAD is to instead use *--*.

## Git Stash
If you are working on some code that you are not ready to commit yet but realise that you forgot to add something to a previous commit ion order to continue, it is possible to store the current changes to then be reimplemented once you have backtracked to a previous commit. This can be done with *git stash*, this will store all of your current work in a hidden directory to allow you to alter a previous commit.

Once you have built upon a previous commit you can then reimplement your code by using *git stash pop*, from here you can now continue building up your code till you are ready to commit it.

## Git Log Stuck
If the cursor gets stuck in the Git log pressing *q* will escape this.

## Pushing a Branch
Once you are happy with the changes that you have made to you're branch and everything has been brought to the repository via a commit then it's time to push those changes to view them on GitHub, this can be achieved with *git push --set-upstream origin* followed by the name of the branch you have been working on.

## Pull Requests
Pull requests (PR's) allow other team members to review you're branch and approve the changes before the branch is then integrated back into the main repository. To do this you will have to create a pull request on GitHub, this will allow you to select a base (usually the main repository) and a branch you wish to compare against that base.

This will visually display all the changes made in comparison to the base with a "+" shown against lines and files that have been added (these will also be shown in **Green**), any lines or files that have been removed will be shown with a "-" shown against those lines (these will be shown in **Red**).

When you then click pull request you will be prompted to leave a comment, this will allow you to leave a description of the changes made where you can summarise what you have done and why. You can directly link reviewers that you would like to take a look at this.

## Git Merge
If you want to include changes you have made to a branch onto another or the main this can be used with *git merge* followed by the name of the branch that you want to merge into your current branch.

**Note** - You will likely have been working on the branch you want to merge so you will have to then switch to the branch you with to merge to, this can be done with *git checkout* followed by the name of the branch that you wish to merge your work to.

## Merge Conflict
If a branch gets merged into the main while you are working on another then this will create a conflict, as the branch that you are now working will contain differences besides those you have been working on, in some cases things that you will be working on would have been changed so in that case Git will not know which changes you would like to keep.

If you do happen to try and merge it will display any conflicts within the code editor, by listing the conflict line of the branch we are trying to merge to followed by the line on the branch we are merging as well as special markings to highlight the conflicted area, in order to then resolve the conflict you will have to delete the conflicting line of the 2, along with all of the markings that were added by Git.

## Delete Branch
Once a branch has been merged there is no need to keep that branch anymore and it can then be deleted, this can be done with the command *git branch -d* followed by the name of the branch that you wish to delete. 

If the branch hasn't been merged then you will have to capitalise the D e.g. *git branch -D* followed by the branch name.

## Git Collaborations
The workflow for Git collaborations should typically follow the below:
1. Fetch and merge changes from remote.
2. Create a branch to work on a new feature
3. Develop the feature on your branch and commit the work.
4. Fetch and merge from the remote again incase new commits were made while you were working.
5. Push your branch to the remote.

## Remotes
If working collaboratively on a project with another person the easiest way to do this is by using remotes, it allows collaborators to make their own individual changes and then merge them when they are ready to do so.

To clone a remote repository you can use *git clone "remote_location" "clone_name"*.
- Remote location tells git where to find the remote, this can be either a web address of a file path.
- Clone name is the you will give the directory for git to clone the repository.

When you have a clone of the remote on your computer one thing Git will do is give the remote address you cloned from the name origin, you can check a list of the Git projects remotes with *git remote -v*.

## Switch Between Remotes
To allow you to switch between the remote and clone you will need to use *cd ../"name"*

## Git Fetch
If the origin remote is altered in any way then your clone will no longer be up to date, an easy way to see if any changes have been made is with *git fetch* this will bring the changes over without merging them on a remote branch. This only brings the changes over to your local copy, they are still not visible and changes cannot be made yet, to allow this you will have to integrate them with a merge *git merge origin/main*, when you do this Git performs a fast-forward bringing your local main branch up to speed with the latests commits made on the remote.

## Git Push Origin
Once any changes have been finalised with a commit you then need to push your branch up to the remote for others to review your changes, this can be done with *git push origin* followed by the name of the branch you were working on.

## GitHub Pages
GitHub pages is a service that allows you to deploy a website to the internet, it is a free service and includes features such as:
- Easy setup
- Seamless collaboration using Git and GitHub
- Free hosting with >95% uptime
- Live updating with normal GitHub workflow

When you are ready to share your project this is known as deploying, this can happen multiple times across the course of the project and consists of packaging and sharing on the internet.

Deploying on GitHub pages is automatic, once set up, deploying happens whenever you push local changes to your remote.