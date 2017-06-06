# Om G I T - av johan sundström
## git och github
<img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="10%" height="10%" />

(bild: git.scm.com)
* _git_ är ett versionshanteringsprogram VCS (Version Control System), _Subversion_ (SVN) är ett annat
* Versionshantering innebär stöd för _traceability_, möjligheten att backa till tidigare versioner
* Stödjer flera användare i ett team eller projekt genom branch-based workflow (_branching_ och _merging_)
* Är de facto _standard_ och benämns vara _lightwheight_ 
* _Open source_, skapat av Linus Thorvalds 2005
* Kan vara svårt att lära sig
* git är inte filversioner 
* Mål: _One rule only: master branch is always deployable_ - man utvecklar i en branch
* _git_ is British slang för "_pig headed_, think they are always correct, argumentative" _wiki_
* Läs mer på ```https://www.git-tower.com/learn/git/ebook```

<img src="https://crossbrowsertesting.com/design/images/github-logo.png" width="15%" height="15%" />

(bild: github.com)
* Centrala datalagringsplatser (fil- och databaser) kallas _repository_ eller 
* Github är ett publikt repository och kan redigeras via webb
* Principen är öppen lagring gratis - betala för sluten
* git är inte github

<img src="http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s1600/Github2.png" width="30%" height="30%" />

(bild: jahya.net)


# Kom igång
### Installera <img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="5%" height="5%" />
* ```http://git-scm.com/download``` (installera)
### Förbered <img src="https://crossbrowsertesting.com/design/images/github-logo.png" width="8%" height="8%" />
* Registrera konto på ```https://github.com``` och logga in

### GUI tools (rekommenderas ej)
* GitHub for Windows
```https://windows.github.com```
* GitHub for Mac
```https://mac.github.com```

### git och VS Code <img src="https://image.apphit.com/image/visual-studio-code/visual-studio-code-logo.png" width="3%" height="3%" />
* ```http://git-scm.com/download``` krävs för tillgång till git i VS Code
* ```https://code.visualstudio.com/download``` 

### Konfigurera git från Bash/PowerShell/Terminal/DOS-prompt/Cmder
* ```http://git-scm.com/download``` - Installerar Bash-kommandoprompt (Linuxkommandon)
* ```http://cmder.net``` - Bättre konsol
* Öppna VS Code's interna terminalfönster (CTRL-ö) och skriv konsolkommandon
1. Öppna terminal från given mapp
1. ```git init``` - Skapa lokalt repository (dold) för versionshantering i ```.git```-undermapp
1. ```git config --global user.name "johansundstrom"``` - Tillägget ```--global``` ger åtkomst i alla projektmappar
1. ```git config --global user.email "johan.sundstrom@mdh.se"```
1. ```git config user.name``` - Ekar användarnamn
1. ```git config user.email``` - Ekar epostadress
1. ```git config --list``` - Listar inställningar
1. ```git config --global user.name "ninja-johan"``` - Ändrar username
1. ```git config --global color.ui auto``` - Färg UI
### Konfigurera git från VS Code
* Klicka ```Initialize Repository``` i VS Code eller...
* Öppna VS Code's interna terminalfönster (CTRL-ö) och skriv konsolkommandon

# Versionshantering
### Tre _stages_: Modified ---> Staged ---> Committed
<img src="https://git-scm.com/images/about/index1@2x.png" width="30%" height="30%" />

(bild: github.com)
1. **Modified** - redigerad fil upptäckt (röd)
2. **Staged** - fil(er) märkt(a) för att bli committed (gul)
3. **Committed** - fil(er)säkert förvar i versionsdatabasen (grön)

### Snabbversionen
1. ```git add .```  - Stage'ar allt
1. ```git status``` - Visar status
1. ```git commit -m "commit message"``` - Commit (lagrar versionen)

### 1. Stage file/files
* ```git add file``` | ```directory``` | ```*.????``` | ```.```  - fil | mapp | wildcard | alla
* ```git add file``` | ```directory``` | ```*.????``` | ```.``` ```<-p>``` - Visa diff
### Unstage file/files
* ```git reset HEAD file``` | ```path/file``` - Motsats till 'git add' (HEAD är aktuell branch)
### 2. Commit file(s)
* ```git commit -m 'commit message'``` 
### Uncommit file(s)
* ```git checkout -- file``` - Återgå till fil i föregående commit
### 3. Special - Add med Commit (stage och commit samtidigt)
* ```git commit -am 'commit message'```
### 4. Visa logg
* ```git log``` - Visar alla commits och ID
* ```git log (-p)``` - Visar commit händelser, visar vad som ändrats
* ```git log author="joh"``` - Visar alla commits från viss användare
### 5. Backa till tidigare version
* ```git checkout -- <file>``` - Återgå till sista commit
### 6. .gitignore - fil eller mapp som inte ska behandlas av versionsystemet
1. ```touch .gitignore``` - Skapa filen .gitignore
2. ```fil``` | ```/folder``` | ```*.txt``` - Skriv namnen på filer, mappar eller fil med wildcards som inte ska ingå
---
### Visa skillnader mellan arbetsfiler och repository
* ```git diff <file>```
### Visa skillnader mellan staged och repository
* ```git diff --staged```
### Radera arbetsfiler och repository-filer
* ```git rm fil.file``` Kräver git add nyfil.file och git rm gammal.file innan commit
### Byt namn på fil
* ```git mv oldname.file newname.file```
### Flyttar fil till mapp
* ```git mv oldplace.file folder/newplace.file```


Notis visar att förändringar väntar på att skrivas


### Visual Studio Code <img src="https://image.apphit.com/image/visual-studio-code/visual-studio-code-logo.png" width="3%" height="3%" />
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

# Arbeta mot remote repository

<img src="https://www.git-tower.com/learn/content/01-git/01-ebook/en/01-command-line/04-remote-repositories/01-introduction/basic-remote-workflow.png" width="50%" />

## Översikt kommandon
### Anslutning(ar) - 'origin' är default anslutningsnamn
* ```git remote add origin <url>``` - Använd URL från github.com (```origin``` är default anslutningsnamn)
* ```git remote add <remote> <url>``` - Använd URL från github.com (```<remote>``` är anslutningsnamnet)
* ```git remote``` - Listar anslutningsnamn
* ```git remote -v``` - Visar anslutningsnamn och URL
* ```git remote rm <remote>``` - Raderar anslutning 'remote'
* ```git remote rename <old-remotename> <new-remotename>```
### Hämta till lokal repo från anslutning
* ```git clone <url>```  - Skapar lokal mapp samt .git och hämtar filer från centralt repo
* ```git fetch <remote>``` - Hämtar förändringar från origin men uppdaterar INTE arbetsfiler i HEAD (kräver omstart av t.ex. VS Code)
* ```git pull <remote> <branch>``` - Hämtar förändringar från origin och uppdaterar arbetsfiler i HEAD
### Skicka från lokal repo till central repo på given anslutning
* ```git push <remote> <branch>``` - Publicera lokala förändringar på ett anslutningsnamn
* ```git push -u <remote> <branch>``` - Parameter -u i minnet, git push nästa gång)
### Manipulera remote
* ```git branch -dr <remote/branch>``` - Radera remote branch
* ```git diff HEAD```  - Visar skillnader i arbetsverktyget

# Branch - Merge
<img src="https://backlogtool.com/git-guide/en/img/post/stepup/capture_stepup1_5_6.png" width="60%" height="60%" />

(bild: https://backlogtool.com)

### Snabbversionen - stegen
1. ```git branch develop``` Skapar kopia av master branch i "develop" branch (eller annat namn)
2. ```git checkout develop```switch till "develop" branch. develop branch är nu aktiv- eller HEAD-branch
3. ...arbete sker nu i develop branch
4. ```git checkout master``` byt till master branch. Master är nu HEAD branch
5. ```git merge develop``` slår samman "develop" med master branch
6. ```git branch -d develop``` raderar "develop" branch


### Skapa Branch 
* ```git branch develop``` Skapar kopia av master i "develop" (eller annat namn)
### Switch till Branch
1. ```git checkout develop``` switch till "develop" branch
* develop är nu aktuell _HEAD branch_
* filerna i arbetskatalogen byts nu till de aktuella i develop branch
2. ```git rm '*.txt'``` Raderar alla *.txt i "develop" branch 
1. ```git commit -m "raderat alla *.txt"```
### Chechkout master
* ```git checkout master``` - Switch till master branch
### Förbered för Merge
* ```git merge develop``` - Slår samman
### Branch städning
* ```git branch -d develop``` (raderar branch develop)
### Slutlig upload till repository
* ```git push```


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
