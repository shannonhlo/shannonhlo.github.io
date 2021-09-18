---
layout: single
title: "Vancouver DataJam Workshop Part 2: Let's Git Started with GitHub"

permalink: /projects/:title/
date: "2021-09-17"
author_profile: true
categories:
- Git
- GitHub
- Workshop
excerpt: |
  Learn how Git and GitHub are used to keep track of code changes and collaborate with others 📑
---

This workshop is part of the [Vancouver DataJam 2021](https://www.vancouverdatajam.ca/workshops#git-github) event. It will equip participants with the basics of Git, a version control software, and how to collaborate with others on [GitHub](https://github.com/).

There are three parts:
* [Part 1](https://shannonhlo.github.io/projects/git-github-workshop1/) details installation and set up instructions
* [Part 2](https://shannonhlo.github.io/projects/git-github-workshop2/) introduces the concept of version control, Git, and GitHub
* [Part 3](https://shannonhlo.github.io/projects/git-github-workshop3/) contains hands-on exercises where participants will create a repository in GitHub, make their first commit, and become familiar with other common Git commands

## Before we start, here are some useful resources
Install Git and create a GitHub account using the instructions in [Part 1 of this workshop here](https://shannonhlo.github.io/projects/git-github-workshop1/).

If you're looking for a quick refresher on Git commands, check out this [Git Cheat Sheet](https://www.jrebel.com/blog/git-cheat-sheet). For solutions to specific scenarios or problems, check out [Oh Shit, Git!?!](https://ohshitgit.com/) or the profanity-free version [Dangit, Git!?!](https://dangitgit.com/).

## What is version control?
Version control is a way to keep track of changes. This allows users to revert back to previous versions or "undo" a change. Keeping track of changes also makes collaboration more efficient by providing a platform to consolidate changes made by various users, identify who made each change, and also resolve conflicts like changes to the same line in a file.

Google Docs may be a familiar example of version control software. It tracks the history of changes made to a document, providing a timeline on which user made each edit.

![Google Docs Version Control](..\..\assets\images\2021-09-17-git-github-workshop2\google-docs.png)

## What is Git?
Git is one of the most commonly used version control softwares, often used by software developers and data professionals to manage code. It is useful for both individual projects to track different iterations and also enables users collaborate on projects.

Files are stored both locally on the user's computer and remotely in a location like GitHub. Local files can only be accessed by the user while users with adequate permissions can access remote files from any computer. Imagine storing a Word Document on your desktop, this is a local file. Users on another computer cannot access it. An example of a remote location would be Google Drive. Files on Google Drive can be accessed from other computers

| ![Local & Remote Repos](..\..\assets\images\2021-09-17-git-github-workshop2\local-remote-repos.png) |
|:--:| 
| *[Click here](https://shannonhlo.github.io/assets/images/2021-09-17-git-github-workshop2/local-remote-repos.png) to enlarge the image.* |
|:--:| 

### Git terminology
You will come across the following terminology when using Git:
* __Branch:__ A version of the repository that is different from the main project. These are copies of the main branch where experimental changes can be made without affecting the main project.
* __Clone:__ A copy of the repository. To create a local repository, we can clone a remote repository to a local destination.
* __Commit:__ A snapshot of changes that are saved. An accompanying message is typically written to provide context for documentation purposes.
* __Conflicts:__ When changes are made to the same line in the same file by multiple users. These need to be resolved before merging.
* __Main branch:__ Where the working/tested version of the project is stored. Generally, changes are made on other branches which are then merged to the main branch once they are reviewed.
* __Merge:__ Combine two branches to consolidate changes, usually done through a pull request.
* __Pull request (PR):__ When code has been changed on a branch and the user wants to add those changes to another branch, the changes usually need to be reviewed by another user. Users submit pull requests so that others can review their changes before being merged.
* __Repository (repo):__ A directory where the files and folders of a project are stored.

## What is GitHub?
[GitHub](https://github.com/) is a Git repository hosting service that allows users to save their project (code, figures, data, documentation etc.) in the cloud and share it with others, much like Google Drive. It makes working together on projects much simpler than traditional file sharing services because changes can be tracked, there are features to perform code reviews, and enables users to work on different copies of the same file before merging the changes back together.

Fun fact - the GitHub logo is a combination of an octopus and a cat named Octocat. It represents "how complex code combines can create peculiar things" accourding to [WhiteSource Software](https://www.whitesourcesoftware.com/resources/blog/the-hidden-stories-behind-the-open-source-logos-we-all-love/#:~:text=The%20idea%20for%20GitHub's,combines%20can%20create%20peculiar%20things.).
![GitHub Octocat](..\..\assets\images\2021-09-17-git-github-workshop2\octocat.png)

## How are Git and GitHub used?
### By a single user
Common reasons why individuals may want to use Git for their own projects include:
* Tracking changes to understand what was done and rationale behind decisions
* Backing up files
* Ability to undo a change
* Organized documentation
* Share and showcase work

### By multiple users
In addition to the reasons above, using Git to collaborate with others takes full advantage of the features available such as:
* Ability for more than one person to edit the same file at the same time
* Managing permissions for different users (i.e. read, write, admin)
* Merging changes and conflict resolution
* Reviewing code and writing comments to facilitate discussion
* Branching to work on separate copies of the repository

## Example of collaboration
The diagram below shows an example of two people working on the same project:
1. User1 and User2 have creates new branches where they are doing their respective work.
2. After 2 commits, User1 is finished making their changes and creates a pull request (PR) to merge their work with the main branch.
3. User2 reviews the changes and approves the PR, merging User1's branch (orange) with the main branch.

Note that User2's branch (green) does not contain the changes that User1 made because their branch was created before the merge. This ensures that they do not overwrite each other's work while making changes.

| ![Workflow](..\..\assets\images\2021-09-17-git-github-workshop2\git-branches-workflow.png) |
|:--:| 
| *[Click here](https://shannonhlo.github.io/assets/images/2021-09-17-git-github-workshop2/git-branches-workflow.png) to enlarge the image.* |
|:--:| 

Now you're ready for [Part 3 of the workshop](https://shannonhlo.github.io/projects/git-github-workshop3/)!
