# Quick Guide for Git

## Beginner

#### Set up the user info
The first thing to do is to set up user’s information. When the local repository is pushed to the server, every user knows who sent that commit and pushed it to the remote repository.

```console
$ git config --global user.name <user name>
$ git config --global user.email <user email address>
```
<br/>

#### Create a new repository
To create a new repository for an existing code base, type `git init` in Git Bash.
```console
$ git init
$ git add .
$ git commit -m 'initial commit'
$ git remote add origin https://github.com/user/repo.git  # link to a new Git remote
```
<br/>


#### Clone a repository
To start a project by cloning an existing repository from the server to the local system, type `git clone <repo>`. Then, the repository will be copied to the current local directory.
<br/><br/>


#### Update the local repository from the server
Before adding a commit to Git, it's better to update the local repository first by `git pull --rebase origin`.
<br/><br/>

#### Check the status of the repository
Type `git status` to see the current status of the local repository.
Type `git log` to see the entire commit history in the local repository.
<br/><br/>

#### Saving changes
After editing files, users can make these edited/new added/deleted files to the staging area so these files are ready to be committed. The files on the staging area will be committed at the same time so be careful.

```console
$ git add <file name>  # add specific edited/new added file to staging area
$ git rm <file name>  # add specific deleted file to staging area
$ git add -A   # add all edited/new added/deleted files to staging area
```
<br/>

#### Commit
Using `git commit -m <message>` to take a snapshot of files on the staging area. With –m, users can add a message describing what modifications are done.
<br/><br/>

#### Update changes to server
Use `git push` to upload the local repository to a remote repository.
<br/><br/>


## Advanced Tips
#### A better Git log
Here is a more readable way to browse commit history.
```console
$ git config --global alias.lg = "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all"
$ git lg
```
<br/>

#### List Git aliases
Use `git config --get-regexp alias` to list all aliases.
<br/><br/>

#### Unstage a file in Git
```console
$ git rm --cached <filePath>
$ git reset <filePath>
$ git restore --staged <filePath>
```
<br/>

#### Untrack files added based on .gitignore
```console
$ git rm -r --cached .
$ git add .
$ git commit -m 'update .gitignore'
```
<br/>

#### Link to the remote repository
```console
$ git remote add origin https://github.com/user/repo.git  # link to a new Git remote
$ git remote set-url origin https://github.com/user/repo.git # change the url of the remote repository
```
<br/>

## Reference
- [GitHub Docs](https://docs.github.com/en).
- [Learn Git with Bitbucket Cloud](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud).
- [Git unstage](https://www.datree.io/resources/git-unstage).
