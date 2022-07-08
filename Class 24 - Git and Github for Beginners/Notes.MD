# Class 24 - Git and Github for Beginners

## Agenda

- Let's Talk: #100Devs
- Review: How to Learn?
- Learn: What is this terminal thing?
- Learn: What is GIT?
- Learn: GIT Basic Commands
- Learn: What is Github
- Homework: Introduction to Git & Github

## GIT Basic Commands

**pwd**

Print Working Directory: `pwd`

**cd**

Change Directory: `cd <folder-name>`
Go up a folder: `cd ..`
Go back to home folder: `cd ~`

**touch**

Create a file with: `touch <file-name>`

**ls**

Show all the files in a folder: `ls`
Show all the files in a folder with more info: `ls -l`
Show all the files in a folder, including hidden: `ls -la` (List All)

**Note**: The `-l` and `-la` is a **flag**

**rm**

Remove a file: `rm <file-name>`
Remove a folder: `rm -r <folder-name>` (recursive)
Remove everything, even protected files: `rm -rf <folder-name>`

**code <file-name>**

Open a file in VS Code: `code <file-name>`

Must click the "Install 'code' command path" in VS Code's Command Palette.

## Git

What is Git?

Git is a version control system. It allows us to essentially create save points.
It's a fancy way of tracking changes through time.
Git enables you to take "snapshots" by making a **commit**

A commit allows us to create a snapshot.

Git enables you to roll back to previous "snapshots" (commits).

## Installing Git

For Windows, simply visit: https://gitforwindows.org

After you install Git, you can run the following:

```
$ git config --global user.name "Matthew McGrath"
$ git config --global user.email "myemail@email.com"
```

This allows all your commits to be identifiable to you.

## Basic Git Commands

**git init**

This command creates a special folder to hold all our snapshots (commits)

This _initializes_ a git _repository_

**git add <file>**

Adds file to **staging area** (not yet in that special folder).

**git add \*.html**

Adds all files that end with .html to the staging area.

**git add .**

Adds everything to staging area.

**git commit**

Adds everything in staging to the special folder as a snapshot.

If you get stuck in vim: Type i -> type your message -> escape -> type :wq ->

**git commit -m "commit message**

Adds everything in staging area to the special folder as a snapshot, providing it a commit message.

**git status**

Shows everything in staging area, as well as changed files still in working area.

**git rm --cached <filename>**

Removes a file from staging area.

**git branch -M main**

Changes name of staging area to main. Movement to steer away from branch named "master" to "main".

**Branching**

Want to try something without messing all your code up? Try using branches.

1. git status: Find out if you are on main branch first.
2. git branch <name>: Creates a new branch for you to make your changes on without affecting the rest of your code!
3. git checkout <name>: Moves you to new branch where you can make changes without affecting the rest of your code!
4. Make some changes.
5. Add your changes to staging area via git add .
6. Commit your changes with commit -m "text"
7. Move back to main branch via git checkout main, or back to new branch with git checkout <newBranch>.
8. git merge <newBranch> if you want it to be merged with main (make sure you're on main first).

## Github

So far, all our snapshots are local. If our laptop or hard drives die, our work is gone!

We can use **remote repositories** to prevent this. Github allows us to store remote repositories, for free!
