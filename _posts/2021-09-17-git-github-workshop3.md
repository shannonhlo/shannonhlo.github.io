---
layout: single
title: "Vancouver DataJam Workshop Part 3: Let's Git Our First Repo Started"

permalink: /projects/:title/
date: "2021-09-17"
author_profile: true
categories:
- Git
- GitHub
- Workshop
excerpt: |
  Learn common Git commands through hands-on exercises 📑
---

This workshop is part of the [Vancouver DataJam 2021](https://www.vancouverdatajam.ca/workshops#git-github) event. It will equip participants with the basics of Git, a version control software, and how to collaborate with others on [GitHub](https://github.com/).

There are three parts:
* [Part 1](https://shannonhlo.github.io/projects/git-github-workshop1/) details installation and set up instructions
* [Part 2](https://shannonhlo.github.io/projects/git-github-workshop2/) introduces the concept of version control, Git, and GitHub
* [Part 3](https://shannonhlo.github.io/projects/git-github-workshop3/) contains hands-on exercises where participants will create a repository in GitHub, make their first commit, and become familiar with other common Git commands

## Create a repository in GitHub
Let's start by creating a repository where all the files and folders of your project will be stored.

### Step 1
Sign in to your GitHub account on [github.com](https://github.com/). If you don't have one yet, follow [these instructions](https://shannonhlo.github.io/projects/git-github-workshop1/#create-a-github-account) to create an account.

### Step 2
Click on the green "New" button on the top left to create a new repository.
![Repo step 2](..\..\assets\images\2021-09-17-git-github-workshop3\repo1.png)

### Step 3
Configure repository settings:
1. Set the repository name
2. Optional - write a short description
3. Determine whether this repository should be public or private
4. Optional - check "Add a README file" if you want to include add a longer description in the future
5. Click the green "Create repository" button

![Repo step 3](..\..\assets\images\2021-09-17-git-github-workshop3\repo2.png)

## Clone a repository
Now that you have a remote repository on GitHub, we need to make a local copy on your computer so that you can access the content and make changes.
![Clone repo](..\..\assets\images\2021-09-17-git-github-workshop3\clone1.png)

### Step 1
Click the green "Code" button to open Clone options.

### Step 2
Click the clipboard icon (orange box) to copy the link

### Step 3
Open Git Bash and use the `cd` command to navigate to the location where you want to save the local repository (i.e. a copy of your GitHub repo in the form of a folder). If you don't have Git Bash installed, follow [these instructions](https://shannonhlo.github.io/projects/git-github-workshop1/#install-git).
```
$ cd <insert file path here>
```
In the example below, I've navigated to a folder named "Workspace" in my C drive (C:\Workspace).
![Clone step 3](..\..\assets\images\2021-09-17-git-github-workshop3\clone2.png)

### Step 4
In Git Bash, type `git clone` and paste the link you copied during step 2 into the terminal.
```
$ git clone <remote repository link>
```
There is now a folder in the specific location (see step 3) with the same name as your GitHub repository (in my case, "my-first-repo"). You've created your first local repository!
```
$ git clone https://github.com/shannonhlo/my-first-repo.git
```
![Clone step 4](..\..\assets\images\2021-09-17-git-github-workshop3\clone3.png)

### Step 5
Use the `cd` command again to point towards the local repository.
```
$ cd <insert file path of local repository here>
```
You should now see (main) in blue letters like so:
![Clone step 5](..\..\assets\images\2021-09-17-git-github-workshop3\clone4.png)

## Make the first commit with a commit message
Now let's make our first change by adding a file to the local and remote repositories.

Here is an overview of the process. It's important to note that there are three areas in a local environment:
* __Working directory:__ Changes in these files aren't tracked.
* __Staging area:__ Files in this area are going to be in the next commit.
* __Local repository:__ Contains all your commits, or snapshots of changes. Other users cannot access these changes.
* __Remote repository:__ Similar to local repository but other users can access changes in the remote repository.

| ![staging](..\..\assets\images\2021-09-17-git-github-workshop3\commit1.png) |
|:--:| 
| *[Click here](https://shannonhlo.github.io/assets/images/2021-09-17-git-github-workshop3\commit1.png) to enlarge the image. [Image source](https://support.nesi.org.nz/hc/en-gb/articles/360001508515-Git-Reference-Sheet)* |
|:--:| 

### Step 1
Create a file and save it in your local repository (in my case, the folder named "my-first-repo"). I've created a text file named "sample.txt".

### Step 2
In Git Bash, use the `git status` command to check the state of your local repository and see what changes have been made. This message is telling me that there is a file named sample.txt in the working directory.
```
$ git status
```
![Commit step 2](..\..\assets\images\2021-09-17-git-github-workshop3\commit2.png)

### Step 3
Use  `git add` to add your change to the staging area. This indicates that we want to track the changes in this file.
```
$ git add <file name>
```
If we run `git status` now, the file shows up as green instead of red because it is in the staging area.
![Commit step 3](..\..\assets\images\2021-09-17-git-github-workshop3\commit3.png)

### Step 4
Use `git commit` to write a commit message for documentation purposes and create a snapshot of the changes.
```
$ git commit -m "describe changes here"
```
Notice that the changes won't appear in GitHub yet because the changes have not been pushed to the remote repository.

### Step 5
Use `git push` to "upload" the snapshot of changes to the remote repository in GitHub.
```
$ git push
```
The changes are now in the GitHub repository where other users can access and build upon your work.

## Step 6
If another user makes a change to the remote GitHub repository, you will need to "download" the changes to your computer. This is done using the `git pull` command.
```
$ git pull
```

## Create a branch
As mentioned in part 2, branches are copies or versions of the repository that allow users to make changes without affecting other users. Other users' changes will not affect your branch either.

Create a branch before working on your piece of the project and use it to make changes to avoid overwriting each other's work.
### Step 1
Use the `git checkout` command to create a new local branch and switch to it. Note that this branch won't appear on GitHub yet because it is still in the local environment.
```
$ git checkout -b <new branch name>
```
In the example below, I've created a new branch named dev_shannon. Notice that I have switched over to the new branch because the blue letters display the branch name. This means that any changes I make will be on my own version of the repository.
![Branch step 1](..\..\assets\images\2021-09-17-git-github-workshop3\branch1.png)

### Step 2
Local branches are pushed to remote repositories using the command below.
```
$ git push -u origin <new branch name>
```
The additional options `-u origin <branch name>` only need to be used the first time a local branch is pushed to a remote repository. Subsequent pushes can just use `git push`.

### Step 3
To switch to another branch (i.e. back to main), we can also use the `git checkout` command, this time without the `-b` option.
```
$ git checkout <branch name>
```

## Merge branches with a pull request
At some point in the project, you'll want to combine your work with other users. This means that branches will be merged together.

### Step 1
A pull request needs to be created in order to merge branches. In GitHub, go to the "Pull requests" tab and click the green "New pull request" button.
![Merge step 1](..\..\assets\images\2021-09-17-git-github-workshop3\merge1.png)

### Step 2
Select the two branches you want to merge by opening the drop down. The branch in "compare" will be merged into the "base" branch. Typically, the branch containing changes will be put in "compare".

Click the green "Create pull request" button.
![Merge step 2](..\..\assets\images\2021-09-17-git-github-workshop3\merge2.png)

### Step 3
Tag reviewers by clicking on "Reviewers" (orange box). Add an informative title and details in the body to document what changes were made and to help simplify the review process.
![Merge step 3](..\..\assets\images\2021-09-17-git-github-workshop3\merge3.png)

### Step 4
Click on the green "Merge pull request" button to merge the two branches.
![Merge step 4](..\..\assets\images\2021-09-17-git-github-workshop3\merge4.png)

## Useful commands
To summarize, here are the Git commands that were discussed above:
```
# clone a repository
git clone <remote repository link>

# make a first commit
git status
git add <file name>
git commit -m "describe changes here"
git push
git pull

# create a branch
git checkout -b <branch name>
git push -u origin <branch name>

# switch to another branch
git checkout <branch name>
```