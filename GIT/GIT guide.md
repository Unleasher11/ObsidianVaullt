#version_controll #general_dev

source version controlle software


# Initialising git in your project 

> in the project directory run 

```bash
		git init
```
> to create a git repo (git reposotory)

# using git 

> git using snapshot AKA commits to the projects

> to project file to repo use 

```bash
		git add regex 
```

> regex : means the git  add all the file with name that regex inlcude

> to add all the files use

```bash
		git add .
```

> to create a snapshot of this files

```bash
		git commit -m " commit message "
```


# branching 
> bransh is basically an alternate history of the files in the project

> to create branch 

```bash
		git branch branch-name
```

> to move into the branch 

```bash
		git checkout branch-name 
```

# merging 
> is merging the history of 2 branches of projects

> to merge 

```bash
		git merge bransh-name
```

> this comment is runned from the branch that you want get the modification into from the Branch in the command

> example if we have branch master and alternate
> to get the last commit in the alternate brach into master branch 

> in the master branch run 

```bash
		git merge alternate
```



![[Git Explained in 100 Seconds(720P_HD).mp4]]