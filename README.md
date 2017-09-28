# Om G I T - av johan sundström
## Git och github!!
<img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="10%" height="10%" />

(bild: git.scm.com)
* Som ersättning för omöjliga versionshanteringar på filnivå skapades Versionshanteringsprogram
* _Git_ är ett versionshanteringsprogram VCS (Version Control System), _Subversion_ (SVN) är ett annat
* Versionshantering innebär stöd för _traceability_, möjligheten att backa till tidigare versioner
* _Git_ är inte filversioner
* Stödjer flera användare i ett team eller projekt genom branch-based workflow (_branching_ och _merging_)
* Är de facto _standard_ och benämns vara _lightwheight_
* _Open source_, skapat av Linus Thorvalds 2005
* Kan vara svårt att lära sig
* Mål: _master branch - always deployable_ - deploy i Master branch, utveckling i annan branch
* _git_ is British slang för "_pig headed_, think they are always correct, argumentative" _wiki_
* Läs mer på <a href="https://www.git-tower.com/learn/git/ebook">https://www.git-tower.com/learn/git/ebook</a> eller <a href="https://git-scm.com/book/en/v2/">https://git-scm.com/book/en/v2/</a>
* Lär/träna Git interaktivt online på <a href="https://try.github.io">https://try.github.io</a>

<img src="https://crossbrowsertesting.com/design/images/github-logo.png" width="15%" height="15%" />

(bild: github.com)
* Centrala datalagringsplatser (fil- och databaser) kallas _repository_ eller _repo's_
* Github är ett publikt repository och kan nås via webb
* Principen är öppen lagring gratis - betala för privat
* Git är inte github

<img src="http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s1600/Github2.png" width="30%" height="30%" />

(bild: jahya.net)


# Kom igång
### Installera <img src="https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png" width="10%" height="10%" />
* ```http://git-scm.com/download``` (installera med förvalda inställningar)
### Förbered <img src="https://crossbrowsertesting.com/design/images/github-logo.png" width="15%" height="15%" />
* Registrera konto på ```https://github.com``` och logga in

### GUI tools (rekommenderas ej i tidigt stadium)
* GitHub for Windows
```https://windows.github.com```
* GitHub for Mac
```https://mac.github.com```

### Git och VS Code <img src="https://image.apphit.com/image/visual-studio-code/visual-studio-code-logo.png" width="3%" height="3%" />
* ```http://git-scm.com/download``` krävs för tillgång till Git i VS Code
* ```https://code.visualstudio.com/download```
* Med Visual Studio Code finns möjlighet att arbeta med terminal eller GUI

### Konfigurera Git från Bash/PowerShell/Terminal/DOS-prompt/Cmder
* ```http://git-scm.com/download``` - Installerar Bash-kommandoprompt (Linuxkommandon)
* För Windows finns en bättre konsol ```http://cmder.net```
* Öppna VS Code's interna terminalfönster (Windows: CTRL-ö, Linux: CTRL-Shft-´)
1. Öppna terminal och förbered plats och mapp i filsystemet ```cd <mapp>``` och/eller ```mkdir <mapp>```
1. ```git init``` - Skapar lokal repository  i dolda undermappen ```.git```
1. ```git config --global user.name "johansundstrom"``` Tillägget ```--global``` ger åtkomst i alla projektmappar
1. ```git config --global user.email "johan.sundstrom@mdh.se"```
1. ```git config user.name``` - Visar användarnamn
1. ```git config user.email``` - Visar epostadress
1. ```git config --list``` - Listar inställningar
1. ```git config --global user.name "ninja-johan"``` - Ändrar username
1. ```git config --global color.ui auto``` - Färg UI
### Konfigurera Git från VS Code
* Klicka ```Initialize Repository``` i VS Code eller...
* Öppna VS Code's interna terminalfönster (CTRL-ö) och skriv konsolkommandon

### Git hjälp
* ```git <verb> --help```
* ```git help <verb>```

# <a href="https://github.com/johansundstrom/github_cheatsheet/blob/master/1_versioning.md">Versionshantering</a>
### Tre _stages_: Modified ---> Staged ---> Committed
<img src="https://git-scm.com/images/about/index1@2x.png" width="30%" height="30%" />

(bild: github.com)
1. **Modified** - Redigerade mapp(ar)/fil(er) upptäckta av Git (röd)
2. **Staged** - Mapp(ar)/fil(er) märkta för att bli committed (gul)
3. **Committed** - Mapp(ar)/fil(er) i säkert förvar inom versionsdatabasen (grön)

### Snabbversionen
1. ```git status``` - Visar filer som ändrats
1. ```git add .```  - Stage'ar allt
1. ```git status``` - Visar status
1. ```git status --short``` - Visar kort meddelande
1. ```git commit --message "commit message"``` - Commit (lagrar versionen)

### 1. Stage <mapp(ar)>/<fil(er)>
* ```git add <fil>``` | ```<mapp>``` | ```*.????``` | ```.```  - Fil | mapp | wildcard | alla
* ```git add <fil>``` | ```<mapp>``` | ```*.????``` | ```.``` Tillägget ``` --patch``` visar redigeringar mot repository
### Unstage <mapp(ar)>/<fil(er)>
* ```git reset HEAD <fil>``` | ```<path/fil>``` - Fil återgår till Modified-status (HEAD är aktuell commit)
### 2. Commit <fil(er)>
* ```git commit --message "commit message"```
### Uncommit <fil(er)>
* ```git reset HEAD <fil>``` - Återställ fil från föregående commit
### 3. Återställ fil från tidigare commit
* ```git checkout -- <fil(er)>```
### 4. Visa logg
* ```git log``` - Visar alla commits och ID
* ```git log -p``` - Visar commit händelser, visar vad som ändrats
* ```git log -p -2``` - Visar commit händelser, visar vad som ändrats, sista två händelserna
* ```git log --pretty=oneline``` - Enklare överblick över commits
* ```git log --pretty=oneline --graph``` - Lägger till en graf
* ```git log author="joh"``` - Visar alla commits från viss användare
### 5. .gitignore - fil eller mapp som inte ska behandlas av versionsystemet
1. ```touch .gitignore``` - Skapa filen ```.gitignore```
2. ```fil``` | ```/folder``` | ```*.txt``` - Lista vad som inte ska ingå (ett entry/rad)
---
### Visa skillnader mellan arbetsfiler och staging area
* ```git diff <fil(er)>```
### Visa skillnader mellan staging area och repository
* ```git diff --staged```
### Radera arbetsfiler och repository-filer
* ```git rm fil.file``` Kräver Git add nyfil.file och Git rm gammal.file innan commit
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
## Undoing changes från repository (kopierar tidigare stage till senast. Raderar inte)
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

# <a href="https://github.com/johansundstrom/github_cheatsheet/blob/master/2_collaboration.md">Samarbeten - Branch/Merge</a>
<img src="https://backlogtool.com/git-guide/en/img/post/stepup/capture_stepup1_5_6.png" width="60%" height="60%" />

(bild: backlogtool.com)

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

# <a href="https://github.com/johansundstrom/github_cheatsheet/blob/master/3_remotes.md">Arbeta mot remote repository</a>

<img src="https://www.git-tower.com/learn/content/01-git/01-ebook/en/01-command-line/04-remote-repositories/01-introduction/basic-remote-workflow.png" width="50%" />

### Snabbversion
1. ```git clone <url>```  - Skapar lokal mapp samt .git och hämtar filer från centralt repo
2. ```git pull <remote> <branch>``` - Hämtar förändringar från origin och uppdaterar arbetsfiler i HEAD
3. ```git push <remote> <branch>``` - Publicera lokala förändringar på ett anslutningsnamn
## Översikt kommandon
### Anslutning(ar) - 'origin' är default anslutningsnamn
* ```git remote add origin <url>``` - Använd URL från github.com (```origin``` är default anslutningsnamn)
* ```git remote add <remote> <url>``` - Använd url från github.com (```<remote>``` är anslutningsnamnet)
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
* ```git push -u <remote> <branch>``` - Parameter -u i minnet, Git push nästa gång)
### Manipulera remote
* ```git branch -dr <remote/branch>``` - Radera remote branch
* ```git diff HEAD```  - Visar skillnader i arbetsverktyget




1) Git pull (ändringar?)
git (visar kommandon)
git VI esc:wq = write quit


Klona från externt repository
git clone https://github.com/johansundstrom/RPi_Node (hämtar från repository)

???Anslut till github
---------------------
13) Git remote add origin https://github.com/johansundstrom/try_git.git
14) Git push -u origin master (-u remember parameters, next time: Git push)
15) Git pull origin master



NEW BRANCH - PULL REQUEST
1) Create branch (name: feature?)
    2) Make changes and commit
    3) Open "Pull Requests tab" and click "New pull request" (for someone to review, show diffs)
    4) Select branch
    5) Verify
    6) Click "Create pull request"
    7) Add description, click "Create pull request".
8) "Merge pull request"
