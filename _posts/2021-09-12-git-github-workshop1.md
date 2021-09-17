---
layout: single
title: "Vancouver DataJam Workshop Part 1: Let's Git Set Up"

permalink: /projects/:title/
date: "2021-09-12"
author_profile: true
categories:
- Git
- GitHub
- Workshop
excerpt: |
  Learn how to set up Git and GitHub to prepare for the Vancouver DataJam workshop 📑
---

Before participating in the [Vancouver DataJam 2021](https://www.vancouverdatajam.ca/workshops) workshop on Git and GitHub, there is some set up to be done:
* Install Git and configure username/email
* Create a GitHub account

The instructions below will show you how!

## Install Git
Download the Git installer for your operating system by clicking on the corresponding links below. Detailed instructions can be [found here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
* __Linux:__ [https://git-scm.com/download/linux](https://git-scm.com/download/linux)
* __macOS:__ [https://git-scm.com/download/mac](https://git-scm.com/download/mac)
* __Windows:__ [https://git-scm.com/download/win](https://git-scm.com/download/win)

## Configure your username and email
Once Git has been installed, open your terminal (macOS and Linux) or Git Bash (Windows) and run the commands below. This sets the name and email associated with your commits.
```
# configure your username displayed in commits
$ git config --global user.name "Your Name"
```

```
# configure your email displayed in commits
$ git config --global user.email "youremail@email.com"
```
Note that the username here does not have to correspond with the username that you will set when creating a GitHub account in the next section.

## Create a GitHub account
Go to [https://github.com/](https://github.com/) and enter your email in the white box that says "Email address". This is the email you will use for your GitHub account. Click the green button that says "Sign up for GitHub" to proceed.
![GitHub Website](..\..\assets\images\2021-09-12-git-github-workshop1\github-site.png)

Follow the prompts to finish creating your account.
![GitHub Sign Up](..\..\assets\images\2021-09-12-git-github-workshop1\github-sign-up.png)

