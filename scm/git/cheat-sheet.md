# git cheat sheet

Gist to start learning git and to highlight its most common commands.

```text
# Show remote repositories configured in a specific repo
$ git remote -v
origin git@github.com:rodrigoechaide/docker-learning.git (fetch)
origin git@github.com:rodrigoechaide/docker-learning.git (push)

# Get only remote URL
$ git config --get remote.origin.url
git@github.com:rodrigoechaide/docker-learning.git

# Full output
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

# Add new remote in a repository
git remote add github git@github.com:rodrigoechaide/insecure-registries-docker-role.git

# Verification
$ git remote -v
github git@github.com:rodrigoechaide/insecure-registries-docker-role.git (fetch)
github git@github.com:rodrigoechaide/insecure-registries-docker-role.git (push)
gitlab git@gitlab.com:ansible-IT/ansible-generic-roles/insecure-registries-docker-role.git (fetch)
gitlab git@gitlab.com:ansible-IT/ansible-generic-roles/insecure-registries-docker-role.git (push)

# Clone a Project including its submodules
git clone --recursive git@github.com:rodrigoechaide/insecure-registries-docker-role.git

# Initialize submodules if project was cloned without --recursive switch
git submodule init
git submodule update


# Squash Several Commits into One

# You need to specify the commit sha after which you want to squash commits into the following commit. Then for all subsequents commits you need to replace *pick* with *squash* or *fixup*

git rebase -i <commit-sha>

# or
git rebase -i HEAD~3


# If you have a new codebase with only two commits, you should run the following command to squash the two commits into one:
git rebase -i --root

# Remove last commit with a hard reset (All the file changes does not remain in the staging area and are lost)
git reset --hard HEAD~1

# Remove last commit with a soft reset (All the file changes remain in the staging area)
git reset --soft HEAD~1

Note: The soft reset can be used to delete a file from a commit.

# Skip pre-commit hooks
git commit -m "commit message" --no-verify

# Clean up pre-commit cache
pre-commit clean

# Set up upstream branch for a local branch
git branch -u <remote>/<branch>

# Forcefully delete several branches filtering with name pattern
git branch -D `git branch --list 'minor/*'`

# Output Commit Logs

git log -1 --pretty=format:%h
git log -1 --abbrev-commit

# Get short hash of last commit
git rev-parse --short HEAD

# Config email and name in local repo only
git config user.email "johndoe@abc.com"
git config user.name "John Doe"

# Config email and name globally for all cloned repos
git config --global user.email "johndoe@abc.com"
git config --global user.name "John Doe"

# Modify Author of last commit
git commit --amend --author="Author Name <email@address.com>" --no-edit

# Enable Git Trace for more verbosity

GIT_TRACE=1 <git-command>
```
