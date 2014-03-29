---
layout: post
title: Simple command line RPG
date: 2014-03-29 11:36:00
categories: xcode github rpg c++ tips
---

Starting a new expeirimental [Command line RPG](https://github.com/wastegas/monster) project but this time using [Xcode](https://developer.apple.com/xcode/) rather than [Vim](http://www.vim.org/) like all my other projects. It's my first time using the source control features in Xcode. The repository setup with Xcode was pretty straight forward.

Here's the high level steps to get Xcode working with your github repository:
+ Create a new repository in GitHub
+ Create a new project in Xcode and make sure to let it create a local repository
+ Do an initial commit to your local repo by selecting 'Commit' from the 'Source Control' menu
+ Add a your remote repository but selecting 'Source Control' then from the 'Master' sub-menu 'Configure <your project>'
+ Select 'Remotes' from the dialog menu then add the URL to your remote repository
