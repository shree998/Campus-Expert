Module 11 answers
=================

## Why use ssh agent?
ssh agent handles signing data using your ssh key, it also stores your private key password so you don’t have to enter it every time a service requires you to authenticate with your private key. Gitkranken can also generate new key pairs and add them to GitHub for you.

## What happens when newbies push and pull
When you push your contributions to a remote repo you send your local copy of the repo with all your commits to the remote copy, if merged, this enables everyone who clones the repo from GitHub to download your changes too.

When you pull from a remote repo you download all the new changes that have been made since you last pulled or cloned the repo

## Githooks
Teams could use githooks to force code styles or run automated test scripts on the commit. 

## Writing hooks
Hooks can be written in most executable languages so your options are endless, you could enforce a certain style of commit message, run code tests before the commit is made. Hooks need a shebang line at the top of the file indicating what language they are in and are placed in the .git/hooks directory 
