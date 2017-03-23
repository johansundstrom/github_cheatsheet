# Om G I T - av johan sundström
---
## git/GITHUB
### Snabbfakta
#### git
* git är namnet på funktionen av versionshantering
* Version control - VCS (Version Control Systems) SVN
* git är _Lightwheight_
* Branch-based workflow (_branching_ och _merging_)
* Traceability
* Support teams and projects, multiple deployments
* Git är open source, skapat bl.a. av Linus Thorvalds 2005
* Kan vara svårtlärt
* Git är de facto standard
* Mål: One rule only: master branch is always deployable
* ('git' is British slang for "pig headed, think they are always correct, argumentative") _wiki_
#### github
* Centrala datalagringsplatser (fil- och databaser) kallas _repository_
* github är ett repository

## Kom igång
### Installera
1. http://git-scm.com/download (installera)
2. https://github.com/
3. Registrera konto på ```github.com``` och logga in

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

## Skapa _repository_ lokalt
```git init``` (skapar förutsättning för versionshantering med dold ```.git```-undermapp)

## Tre _stages_
1. **Modified** (förändrad med ej committed)
2. **Staged** (märkt för att bli committed)
3. **Committed** (säkert förvar i versionsdatabasen)

## Modify--->Stage--->Commit
Snabb beskrivning
1. ```git add .``` (stage'ar allt)
2. ```git commit -m "commit message"``` (commit'ar allt)
1. ```git status``` (visar status)
### 1. Stage file(s)
* ```git add <file> | <directory> | <'*.????'> | <.>``` (fil | mapp | wildcard | alla)
* ```git add xxx <-p>``` (visa diff) 
* ```git reset [folder/file]``` (opposite of git add)

### 2. Commit file(s)
* ```git commit -m "commit message"``` 
* ```git log``` (visar full insyn)
* ```git log (-p)``` (visar commit händelser, visar vad som ändrats)
* ```git checkout -- <file>``` (återgå till sista commit)

### Visual Studio Code
* Ett ```M```indikerar modified
* Markera fil - _Stage_

## Undoing changes
* ```git log --oneline``` (en rad)
output från ovanstående
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;d8362b7 upd
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;f8a9f38 nya filer
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;64116aa update 
```
* ```git checkout f8a9f38``` 
* ```git status``` 
* ```git checkout master``` 
* ```git checkout -- <fil>``` (återgår till sista commit)
* ```git status``` 
### Med Visual Studio Code
* Ett ```M```indikerar modified
* Markera fil - _Clean_

## Arbeta mot remote server
### Översikt kommandon
* ```git remote add origin <url>``` (samma url som på github) 
* ```git remote``` (listar anslutningar)
* ```git remote -v``` (visar url)
* ```git remote rm``` <name> (raderar anslutning)
* ```git diff HEAD``` (visar skillnader)
* ```git clone <url>``` (skapar mappar och -git och hämtar filer)
* ```git fetch```
* ```git pull origin master``` (hämta, origin - anslutningens namn)
* ```git push```

### Hämta från extern repository
* ```git remote add <name> <url>``` (skapar anslutning med namn)
* ```git remote rename <old-name> <new-name>```
* ```git pull origin master```(hämtar senaste master från anslutning origin)
origin remote (med git clone kallas anslutningen för origin)
* ```git push -u origin master```(-u parametrar i minnet, git push nästa gång)

## Branch - Merge
Snabb beskrivning
1. ```git branch <new-idea>``` (Skapar kopia av master i new-idea)
2. ```git checkout <new-idea>```(switch till branch)
3. ...arbete i branch
4. ```git checkout master``` (switch till master)
5. ```git merge <new-idea>``` (slår samman)
6. ```git branch -d <new-idea>``` (raderar branch <new-idea>)
### Skapa Branch 
* ```git branch <new-idea>``` (Skapar kopia av master i new-idea)
### Switch till Branch
1. ```git checkout <new-idea>```(switch till branch)
2. ```git rm '*.txt'```(Raderar alla *.txt i branch new-idea)
1. ```git commit -m "raderat alla *.txt"```
### Chechout master
* ```git checkout master``` (switch till master)
### Förbered för Merge
* ```git merge <new-idea>``` (slår samman)
### Branch städning
* ```git branch -d <new-idea>``` (raderar branch <new-idea>)
### Slutlig upload to repository
* ```git push```

git pull ()


1) git pull (ändringar?)
git (visar kommandon)
git VI esc:wq = write quit


Klona från externt repository
git clone https://github.com/johansundstrom/RPi_Node (hämtar från repository)

???Anslut till github
---------------------
13) git remote add origin https://github.com/johansundstrom/try_git.git
14) git push -u origin master (-u remember parameters, next time: git push)
15) git pull origin master



NEW BRANCH - PULL REQUEST
1) Create branch (name: feature?)
    2) Make changes and commit
    3) Open "Pull Requests tab" and click "New pull request" (for someone to review, show diffs)
    4) Select branch
    5) Verify
    6) Click "Create pull request"
    7) Add description, click "Create pull request".
8) "Merge pull request"
