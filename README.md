# G I T

## GITHUB 
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
Registrera konto och logga in
2. https://github.com/

### Git config
1. Öppna VS Code från given mapp
1. Klicka "Initialize Git Repository"
1. Notis visar att förändringar väntar på att skrivas
1. Öppna terminalfönstret (CTRL-ö)
1. ```git config --global user.name "johansundstrom"```
1. ```git config --global user.email "johan.sundstrom@mdh.se"```
1. ```git config user.name```
1. ```git config user.email```
1. ```git config --list```
1. ```git config --global user.name "ninja-johan"``` (change username)

## Skapa repository lokalt
```git init```
## Three stages
1. modified (förändrad med ej committed)
2. staged (märkt för att bli committed)
3. committed (säkert förvar i databasen)

## Modify-->Stage-->Commit
### Spara ändringar
1. git status (visar status)
2. ```Stage file(s)```
1. ```git add <file> | <directory> | <*.????> | <.>``` (fil | mapp | wildcard | alla (stage file(s))
1. ```git add xxx <-p>``` (visa diff) 
1. ```git reset``` (opposite of git add )
### Commit file(s)
1. ```git commit -m "commit message"``` 
1. ```git log (-p)``` (visar commit händelser, visar vad som ändrats)

## Undoing changes
1. ```git log --oneline``` (en rad) 
2. ```  d8362b7 upd
1.    f8a9f38 nya filer
1.     64116aa update
1. git checkout f8a9f38```
1. ```git status
1. ```git checkout master``` 
1. ```git status``` 
### VS Code
Markera fil - Clean
