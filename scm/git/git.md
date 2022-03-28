# git-learning

Gist to start learning git and to highlight its most common commands.

## Show remote repositories configured in a specific repo

```bash
$ git remote -v
origin git@github.com:rodrigoechaide/docker-learning.git (fetch)
origin git@github.com:rodrigoechaide/docker-learning.git (push)
```

Get only remote URL:

```bash
$ git config --get remote.origin.url
git@github.com:rodrigoechaide/docker-learning.git
```

Full output:

```bash
$ git remote show origin
* remote origin
  Fetch URL: git@github.com:rodrigoechaide/docker-learning.git
  Push  URL: git@github.com:rodrigoechaide/docker-learning.git
  HEAD branch: master
  Remote branch:
    master tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up-to-date)
```

## Add new remote in a repository

```bash
git remote add github git@github.com:rodrigoechaide/insecure-registries-docker-role.git
```

Verify:

```bash
$ git remote -v
github git@github.com:rodrigoechaide/insecure-registries-docker-role.git (fetch)
github git@github.com:rodrigoechaide/insecure-registries-docker-role.git (push)
gitlab git@gitlab.com:ansible-IT/ansible-generic-roles/insecure-registries-docker-role.git (fetch)
gitlab git@gitlab.com:ansible-IT/ansible-generic-roles/insecure-registries-docker-role.git (push)
```

## Clone a Project including its submodules

```bash
git clone --recursive git@github.com:rodrigoechaide/insecure-registries-docker-role.git
```

## Initialize submodules if project was cloned without --recursive switch

```bash
git submodule init
git submodule update
```

## Squash Several Commits into One

You need to specify the commit sha after which you want to squash commits into the following commit. Then for all subsequents commits you need to replace *pick* with *squash* or *fixup*

```bash
git rebase -i <commit-sha>
```

or

```bash
git rebase -i HEAD~3
```

```bash
squash fa8d7eaa Updated fortify token and configure right version of fortify maven plugin                              
squash e4fd1343 Change pom version to 21.2.0                                                                                     
pick fd211d6e Added gitlab ci/cd configuration and adjusted pom files to get integration with gitlab ci/cd setup     
                                                                                                                               
# Rebase 9a8d2904..fd211d6e onto e4fd1343 (5 commands)                                                                         
#                                                                                                                              
# Commands:                                                                                                                    
# p, pick <commit> = use commit                                                                                                
# r, reword <commit> = use commit, but edit the commit message                                                                 
# e, edit <commit> = use commit, but stop for amending                                                                         
# s, squash <commit> = use commit, but meld into previous commit                                                               
# f, fixup <commit> = like "squash", but discard this commit's log message                                                     
# x, exec <command> = run command (the rest of the line) using shell                                                           
# b, break = stop here (continue rebase later with 'git rebase --continue')                                                    
# d, drop <commit> = remove commit                                                                                             
# l, label <label> = label current HEAD with a name                                                                            
# t, reset <label> = reset HEAD to a label                                                                                     
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]                                                                   
# .       create a merge commit using the original merge commit's                                                              
# .       message (or the oneline, if no original merge commit was                                                             
# .       specified). Use -c <commit> to reword the commit message.                                                            
#                                                                                                                              
# These lines can be re-ordered; they are executed from top to bottom.                                                         
#                                                                                                                              
# If you remove a line here THAT COMMIT WILL BE LOST.                                                                          
#                                                                                                                              
# However, if you remove everything, the rebase will be aborted.                                                               
#                                                                                                                              
```

If you have a new codebase with only two commits, you should run the following command to squash the two commits into one:

```bash
git rebase -i --root
```

## Modify Author of last commit

```bash
git commit --amend --author="Author Name <email@address.com>" --no-edit
```

## Remove last commit

```bash
# Hard Reset (All the file changes does not remain in the staging area and are lost)
git reset --hard HEAD~1

# Soft Reset (All the file changes remain in the staging area)
git reset --soft HEAD~1
```

Note: The soft reset can be used to delete a file from a commit.

## Set up upstream branch for a local branch

```bash
git branch -u <remote>/<branch>
```

## Delete a branch

```bash
# Forcefully delete several branches filtering with name pattern
git branch -D `git branch --list 'minor/*'`
```

## Output Commit Logs

```bash
git log -1 --pretty=format:%h
git log -1 --abbrev-commit

# Get short hash of last commit
git rev-parse --short HEAD
```

## Set up name and email

```bash
# Config email and name in local repo only
git config user.email "johndoe@abc.com"
git config user.name "John Doe"

# Config email and name globally for all cloned repos
git config --global user.email "johndoe@abc.com"
git config --global user.name "John Doe"
```
