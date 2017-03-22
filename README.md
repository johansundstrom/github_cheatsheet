# G I T

## OM GIT
* lightwheight
* version control - VCS (Version Control Systems) SVN
* branch-based workflow (branching and merging)
* Traceability
* support teams and projects, multiple deployments
* git är open source, skapat bl.a. av Linus Thorvalds
* Kan vara svårtlärt
* git är de facto standard
* Mål: One rule only: master branch is always deployable

## LEARN GIT
### Installera
1. http://git-scm.com/download (installera)
### Registrera konto och logga in
2. https://github.com/

### git config
 3. Öppna VS Code från given mapp
4. Klicka "Initialize Git Repository"
1. Notis visar att förändringar väntar på att skrivas
1. Öppna terminalfönstret (CTRL-ö)
1. ```git config --global user.name "johansundstrom"```
1. ```git config --global user.email "johan.sundstrom@mdh.se"```
1. ```git config user.name```
1. ```git config user.email```
1. ```git config --list```
1. ```git config --global user.name "ninja-johan"``` (change username)

## Skapa repository
```git init```

## Klona från externt repository
```git clone https://github.com/johansundstrom/RPi_Node``` (hämtar från repository)

???Anslut till regithub
---------------------
1. ```git remote add origin https://github.com/johansundstrom/try_git.git```
1. ```git push -u origin master``` (-u remember parameters, next time: git push)
1. git pull origin master

Edit --> Stage --> Commit
------------------------- 
* Spara ändringar
git status (visar status)
**Stage file(s)**
git add <file> | <directory> | <*.????> | <.> (fil | mapp | wildcard | alla (stage file(s))
git add xxx <-p> (visa diff) 
git reset (opposite of git add )
**Commit file(s)**
git commit -m "commit message" 
git log (-p) (visar commit händelser, visar vad som ändrats


Undoing changes
---------------
git log --oneline (en rad)
    d8362b7 upd
    f8a9f38 nya filer
    64116aa update
git checkout f8a9f38
git status 
git checkout master
git status
--VS Code--
Markera fil - Clean

git push
git pull ()


1) git pull (ändringar?)
git (visar kommandon)
git VI esc:wq = write quit

Three stages
1) committed (säkert förvar i databasen)
2) modified (förändrad med ej committed)
3) staged (märkt för att bli committed)

NEW BRANCH - PULL REQUEST
1) Create branch (name: feature?)
    2) Make changes and commit
    3) Open "Pull Requests tab" and click "New pull request" (for someone to review, show diffs)
    4) Select branch
    5) Verify
    6) Click "Create pull request"
    7) Add description, click "Create pull request".
8) "Merge pull request"
