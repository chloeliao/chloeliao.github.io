# Quick Guide for Git

### Useful Command

#### Set up the user info
The first thing to do is to set up user’s information. When the local repository is pushed to the server, every user knows who sent that commit and pushed it to the remote repository.

```console
$ git config --global user.name <user name>
$ git config --global user.email <user email address>
```

#### Clone a repository
It is common to start a project by cloning an existing repository from the server to the local system. To clone the repository, type the `$ git clone <repo>` in git bash and the repository will be copied to the current local directory.


#### Update the local repository from the server
Before adding a commit to git, it's better to update the local repository first by `$ git pull --rebase origin`.


#### Saving changes
After editing files, user can make these edited/new added/deleted files to the staging area so these files are ready to be committed. The files on the staging area will be committed at the same time so be careful.

```console
$ git add <file name>  # for adding specific edited/new added file to staging area
$ git rm <file name>  # for adding specific deleted file to staging area
$ git add -A   # for adding all edited/new added/deleted files to staging area
```


### Reference


[Learn Git with Bitbucket Cloud](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud).
