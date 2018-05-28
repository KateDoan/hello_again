# Git Config
git config --global user.name "KateDoan"
git config --global user.email "kate.tradoan@gmail.com"

# Set your text editor
git config --global core.editor "notepad"

# Create a new repostiory from the command line:
echo "# smoking_trial_2018" >> README.md
git init
git add README.md
git remote add origin https://github.com/KateDoan/smoking_trial_2018.git
git push -u origin master

# Exit Vim editor window
Press Esc then :wq

# Contribute to an existing repository
## download a repository on GitHub.com to our machine
git clone https://github.com/me/repo.git

## change into the `repo` directory
cd repo

## create a new branch to store any new changes
git branch my-branch

## switch to that branch (line of development)
git checkout my-branch

## make changes, for example, edit `file1.md` and `file2.md` using the text editor

## stage the changed files
git add file1.md file2.md

## take a snapshot of the staging area (anything that's been added)
git commit -m "my snapshot"

## push changes to github
git push --set-upstream origin my-branch

## create a new directory, and initialize it with git-specific functions
git init my-repo

## change into the `my-repo` directory
cd my-repo

## create the first file in the project
touch README.md

## git isn't aware of the file, stage it
git add README.md

## take a snapshot of the staging area
git commit -m "add README to initial commit"

## push changes to github
git push --set-upstream origin master

## assumption: a project called `repo` already exists on the machine, and a new branch has been pushed to GitHub.com since the last time changes were made locally

## change into the `repo` directory
cd repo

## update all remote tracking branches, and the currently checked out branch
git pull

## change into the existing branch called `feature-a`
git checkout feature-a

## make changes, for example, edit `file1.md` using the text editor

## stage the changed file
git add file1.md

## take a snapshot of the staging area
git commit -m "edit file1"

## push changes to github
git push

## Reset, checkout, revert
git checkout -b old-project-state 0ad5a7a6\
git reset --hard 0ad5a7a6\
git reset --soft 0ad5a7a6\
git checkout hotfix\
git revert HEAD\~2\
git reset HEAD\~2 foo.py\
git checkout HEAD~2 foo.py

## Keep forked repo updated
1. Clone your fork:\
git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git
2. Add remote from original repository in your forked repository:\
cd into/cloned/fork-repo\
git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git\
git fetch upstream
3. Updating your fork from original repo to keep up with their changes:\
git pull upstream master