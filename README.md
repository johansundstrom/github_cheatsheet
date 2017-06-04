# Om G I T - av johan sundström
## git och github
<img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="10%" height="10%" />

(bild: git.scm.com)
* _git_ är ett versionshanteringsprogram VCS (Version Control System), _Subversion_ (SVN) är ett annat
* Versionshantering innebär stöd för _traceability_, möjligheten att backa till tidigare versioner
* Stödjer flera användare i ett team eller projekt genom branch-based workflow (_branching_ och _merging_)
* Är de facto _standard_ och benämns vara _lightwheight_ 
* _Open source_, skapat bl.a. av Linus Thorvalds 2005
* Kan vara svårt att lära sig
* Mål: _One rule only: master branch is always deployable_
* _git_ is British slang för "_pig headed_, think they are always correct, argumentative" _wiki_

<img src="https://crossbrowsertesting.com/design/images/github-logo.png" width="15%" height="15%" />

(bild: github.com)
* Centrala datalagringsplatser (fil- och databaser) kallas _repository_ eller 
* Github är ett publikt repository
* Principen är öppen lagring gratis - betala för sluten
* git är inte github

<img src="http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s1600/Github2.png" width="30%" height="30%" />

(bild: jahya.net)


## Kom igång
### Installera <img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="5%" height="5%" />
* ```http://git-scm.com/download``` (installera)
### Förbered <img src="https://crossbrowsertesting.com/design/images/github-logo.png" width="8%" height="8%" />
* Registrera konto på ```https://github.com``` och logga in

### GUI tools (rekommenderas ej)
* GitHub for Windows
```https://windows.github.com```
* GitHub for Mac
```https://mac.github.com```

### VS Code och git <img src="https://image.apphit.com/image/visual-studio-code/visual-studio-code-logo.png" width="3%" height="3%" />
* ```http://git-scm.com/download``` krävs för tillgång till git i VS Code
* ```https://code.visualstudio.com/download``` 

## Konfigurera git från Bash/PowerShell/Terminal/DOS-prompt/Cmder
1. Öppna terminal från given mapp
1. ```git init``` (skapar lokalt dold repository för versionshantering  ```.git```-undermapp)
1. ```git config --global user.name "johansundstrom"``` ( ```--global``` ger åtkomst i alla projektmappar)
1. ```git config --global user.email "johan.sundstrom@mdh.se"```
1. ```git config user.name``` ekar användarnamn
1. ```git config user.email``` ekar epostadress
1. ```git config --list``` listar inställningar
1. ```git config --global user.name "ninja-johan"``` (ändrar username)
1. ```git config --global color.ui auto``` (färg UI)
### Konfigurera git från VS Code
* Klicka ```Initialize Git Repository``` i VS Code eller...
* Öppna VS Code's interna terminalfönster (CTRL-ö) och skriv terminalkommandon

# Versionshantering
### Tre _stages_
<img src="https://git-scm.com/images/about/index1@2x.png" width="30%" height="30%" />

(bild: github.com)
1. **Modified** - redigerad fil upptäckt (röd)
2. **Staged** - fil(er) märkt(a) för att bli committed (gul)
3. **Committed** - fil(er)säkert förvar i versionsdatabasen (grön)

## Modified--->Staged--->Committed
Snabb beskrivning
1. ```git add .``` (stage'ar allt)
1. ```git status``` (visar status)
1. ```git commit -m "commit message"``` (commit'ar allt)

### 1. Stage file(s)
* ```git add file``` | ```directory``` | ```*.????``` | ```.``` - fil | mapp | wildcard | alla
* ```git add xxx <-p>``` (visa diff) 
### Unstage file(s)
* ```git reset HEAD [folder/file]``` (opposite of git add)
### 2. Commit file(s)
* ```git commit -m "commit message"``` 
### Uncommit file(s)
* ```jj```
### 3. Add med Commit
* ```git commit -am "meddelande"```
### 4. Visa logg
* ```git log``` (visar full insyn)
* ```git log (-p)``` (visar commit händelser, visar vad som ändrats)
* ```git log author="joh"``` Visar alla commits från viss användare
### 5. Backa till tidigare version
* ```git checkout -- <file>``` (återgå till sista commit)

---
### Visa skillnader mellan arbetsfiler och repository
* ```git diff (file)```
### Visa skillnader mellan staged och repository
* ```git diff --staged```
### Radera arbetsfiler och repository-filer
* ```git rm fil.file``` Kräver git add nyfil.file och git rm gammal.file innan commit
### Byt namn på fil
* ```git mv oldname.file newname.file```
### Flyttar fil till mapp
* ```git mv oldname.file folder/newname.file```


Notis visar att förändringar väntar på att skrivas


### Visual Studio Code
* Ett ```M```indikerar modified
* ```+``` öppnar _Stage_ ```A``` visas
* Markera fil - _Stage_
* Skriv commit message, Skicka
* Klick på ```M```visar förändringar
## Undoing changes från repository (koperar tidigare stage till senast. Raderar inte)
* ```git log --oneline``` (en rad)
output från ovanstående
```
d8362b7 upd (commit meddelanden...)
f8a9f38 nya filer
64116aa update 
```
* ```git checkout f8a9f38 -- filename.ext```
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
