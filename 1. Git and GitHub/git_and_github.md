
----

# **`Understand Git and Github`**
-----


### **What is Git and Github**
![](images/Screenshot%202026-11-21%20204908.png)

### **Difference between Git and Github**
![](images/Screenshot%202026-11-21%20205016.png)

### **Why need Git and GitHub**
![](images/Screenshot%202026-11-21%20205048.png)

### **Install Git according to Your System**
![](images/Screenshot%202026-11-21%20211028.png)

- To check if git is installed properly run this command in CMD.
```bash
git --version
```

### **Set Up git in Your System**
- In order to use git fiirdt time in your system use these two command in cmd to set up git
![](images/Screenshot%202026-11-21%20212254.png)
![](images/Screenshot%202026-11-21%20213409.png)


### **Your first Git repository**
![](images/Screenshot%202026-11-21%20213925.png)

### **Branching in Git and Github**
![](images/Screenshot%202026-11-21%20213634.png)
![](images/Screenshot%202026-11-21%20214455.png)

- Only `.git` is new, and the folder holds nothing but that. Everything Git keeps for the project sits inside it, which ls .git lists.


### **Reading status in an empty repository**
![](images//Screenshot%202026-11-21%20215605.png)


### **Where you run git init**
![](images/Screenshot%202026-11-21%20215812.png)

### **Staging and committing**
![](images/Screenshot%202026-11-21%20220151.png)
![](images/Screenshot%202026-11-21%20220452.png)
![](images/Screenshot%202026-11-21%20220530.png)


### **Staging the file with git add**
![](images/Screenshot%202026-11-21%20220830.png)

![](images/Screenshot%202026-11-21%20222254.png)
```bash
git add .
```

### **Making the first commit**
![](images/Screenshot%202026-11-21%20221147.png)
```bash
git commit -m "Add a README for the docs assistant"
```


### **Taking a change back out of the staging area**
![](images/Screenshot%202026-11-21%20223729.png)


### **Working tree compared with staging area and repository**
![](images/Screenshot%202026-11-21%20224003.png)

### **Reading git status**
![](images/Screenshot%202026-11-22%20210945.png)
![](images/Screenshot%202026-11-22%20211039.png)
![](images/c911ffd42598405c84ebc14a0945a18d.svg)

### **The three sentences status ends with**
![](images/Screenshot%202026-11-22%20211941.png)

### **.gitignore**
![](images/Screenshot%202026-11-22%20212203.png)
![](images/Screenshot%202026-11-22%20212429.png)


### **Looking at history with git log**
![](images/Screenshot%202026-11-23%20211739.png)
![](images/Screenshot%202026-11-23%20212054.png)

```bash
git log                 # every commit, newest first
git log --oneline -n 5  # the last five, one line each
```


### **One line per commit**
![](images/Screenshot%202026-11-23%20212422.png)
```bash
git log --oneline
```

### **Seeing what changed with git diff**
![](images/Screenshot%202026-11-23%20212834.png)
![](images/Screenshot%202026-11-23%20213004.png)
![](images/73be1e027db0487890909d02cd539a89.svg)

```bash
git diff            # the folder against the staging area
git diff --staged   # the staging area against the last commit
git diff HEAD       # the folder against the last commit
```

- The same change again. git diff HEAD compares the folder with the last commit and ignores the staging area in between, so staging makes no difference to it.

![](images/Screenshot%202026-11-23%20213604.png)


### **Writing a commit message**
![](images/Screenshot%202026-11-23%20215334.png)
![](images/Screenshot%202026-11-23%20215429.png)

### **Writing a commit message**
![](images/Screenshot%202026-11-23%20215733.png)

### **Branches**
![](images/Screenshot%202026-11-24%20080359.png)

- Syntax: the same command lists branches, creates one, and deletes one.
```bash
git branch                 # list them, with a star on the one you are on
git branch <name>          # create a branch pointing at the current commit
git branch -d <name>       # delete a branch that has been merged
```
![](images/Screenshot%202026-11-25%20203041.png)
![](images/Screenshot%202026-11-25%20203625.png)
![](images/Screenshot%202026-11-25%20203446.png)
![](images/fb5a0488a1b143d98d481ca61311b2ce.svg)
![](images/Screenshot%202026-11-25%20204306.png)

### **Switching branches**
![](images/Screenshot%202026-11-25%20205420.png)
![](images/Screenshot%202026-11-25%20205549.png)

- Syntax: git switch arrived in Git 2.23 for exactly this job. git checkout still does it and is what you will see in older material.

```bash
git switch <name>       # move to an existing branch
git switch -c <name>    # create it and move to it in one step
git switch -            # back to the branch you were on before
git checkout <name>     # the older command, same move
git switch --detach     # move to previous commit
```

### **Merging a branch**

![](images/Screenshot%202026-11-25%20210903.png)
- An experiment that worked has to come back. Merging is how: you stand on the branch that should receive the work, name the branch that has it, and Git joins the two lines of history. There are two ways it can end, and the output tells you which one happened.

```bash
git switch main            # the branch that receives the work
git merge chunk-800        # the branch whose commits come in
git merge --no-edit <name> # keep Git's prepared message, open no editor
```
### **A merge that makes a commit**
![](images/Screenshot%202026-11-25%20211317.png)
- Both names are on different commits, and neither is reachable from the other. There is no name to move forward, so Git has to join the two lines instead.

```bash
git merge --no-edit chunk-800
```
### **Tidying up after a merge**
![](images/Screenshot%202026-11-25%20211707.png)
```bash
git branch -d chunk-800
```
### **Where you merge**
![](images/Screenshot%202026-11-25%20212005.png)


### **Resolving merge conflicts**
![](images/Screenshot%202026-11-25%20212954.png)
- Most merges finish on their own. Git only stops when the two sides changed the same lines, and then it hands the file back to you with both versions in it, marked. Nothing is lost and nothing is broken. The job is to edit the file into the version you want and commit it.


### **What Git does when it cannot decide**
- The merge runs, finishes what it can, and stops on the file it cannot finish.
![](images/Screenshot%202026-11-25%20213615.png)

![](images/Screenshot%202026-11-25%20220532.png)


### **Git remotes**
![](images/Screenshot%202026-11-25%20222048.png)
![](images/20badc6f5f494c219123693758d589f1.svg)

**`Syntax`**: every form of git remote you will use.

```bash
git remote add origin <URL>         # give a URL the name origin
git remote -v                       # list the remotes, with their URLs
git remote rename origin github     # change a remote's name
git remote set-url origin <URL>     # point an existing name at a different URL
git remote remove github            # forget a remote
```
![](images/Screenshot%202026-11-25%20222639.png)
![](images/Screenshot%202026-11-25%20223230.png)

### **GitHub authentication**
![](images/Screenshot%202026-11-26%20194237.png)
![](images/Screenshot%202026-11-26%20194435.png)


### **Pushing and pulling**
![](images/Screenshot%202026-11-26%20201237.png)
![](images/1a870e8444dc4d7aa77d53f600c971df.svg)

```bash
git push -u origin main    # send branch main to origin, and remember the pairing
git push                   # after -u once, this is enough
git fetch origin           # download what the remote has, change nothing you are working on
git pull                   # git fetch, then merge what came down into your branch
```
![](images/Screenshot%202026-11-26%20201746.png)


### **Cloning a repository**
![](images/Screenshot%202026-11-26%20202301.png)

- `Syntax`: the forms of git clone worth knowing.
```bash
git clone <URL>                  # into a new folder named after the repository
git clone <URL> my-folder        # into a folder you name
git clone --branch dev <URL>     # start on the dev branch instead of the default one
git clone --depth 1 <URL>        # the latest commit only, not the whole history
```

### **Cloning against init plus remote**
![](images/Screenshot%202026-11-26%20202922.png)


### **Pull requests**
![](images/Screenshot%202026-11-26%20203124.png)
![](images/85f188b8f28749668edccb6dd192dfb7.svg)

- The name is a request to the project to pull your branch in. GitHub's docs put one rule on it: “Pull requests can only be opened between two different branches”. The branch you want merged is the compare branch; the branch it should land in is the base.