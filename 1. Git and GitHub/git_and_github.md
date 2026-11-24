
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