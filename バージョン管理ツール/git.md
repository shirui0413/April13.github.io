---
layout: post
title: git勉強
categories: git
tags: git github
---

* content
{:toc}


# Git 勉強

#### Create

###### Create a new repository with commond

```cmd
git init			// create repository
```

###### add new or modified files to repository

```
git add file1 file2		// add files to repository
git add dir				// add directory to repository
git add .				// add all files in the directory to repository
```

###### commit

```
git commit -m "an explanation for commit"
```



#### branch

###### view a list of branches

```git
git branch				// display local branches
git branch -a			// display branches including remote branches
```

###### create a branch

```
git branch <branchname>
```

###### change the branch name

```
git branch -m <oldname> <newname>
```

###### switch branch

```
git checkout brancthName	// switch to the branch
git checkout -				// quickly s
```



#### commit

###### changing a just before commit

```
git commit --amend		// use vim editor 
```

###### changing an older or multiple commits

if you need to change the messages of an older or multple commits, you can use an interactive 「git rebase」to change one or more older commits.

1. Navigate to the repository containing the commit message you want to change.
2. Type 「git rebase -i HEAD~N」, where 「N」is the number of  commit to perform a rebase on. if you want to change the 4th and the 5th latest commits, you would type:

```
git rebase -i HEAD~5
```



#### remote 

###### clone

```
git clone git@github.com:shirui0413/PS_FilesDelete.git folder-name    // clone a repository from remote
```

###### display

```
git remote -v	// show remote info
```

###### push

```
git push remoteName localBranchName:remoteBranchName	// complete writing

```









## CMD

###### directory

```cmd
md ps_file_del		// create a new directory
cd ps_file_del		// moving into the directory
```

###### file

```cmd 
echo "# ps_file_del" >> README.md		// create a .md file with content"..."
echo i am a text file. >> test.txt		// create a .txt file whih content 
```

