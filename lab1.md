# Lab 1

## Versionshantering

### Setup
1. ```http://git-scm.com/download``` (installera) Senaste release 2.14.1 (2017-08-04)
2. Skapa mappen ```Mina Repositories``` i filsystemet
2. Skapa mappen ```git_lab``` inuti ```Mina Projekt```
3. Högerklicka mappen och välj ```Git Bash Here```
3. ```git config --global user.name "johansundstrom"``` - Tillägget --global ger 
åtkomst i alla projektmappar
3. ```git config --global user.email "johan.sundstrom@mdh.se"```
3. ```git config --global color.ui auto``` - Färg UI

### Skapa fil
4. Sänd ```ls``` (list) konstatera att det är tomt
4. Sänd ```touch index.html``` Skapar index.html
5. Sänd ```ls```
6. Sänd ```ls -l``` (lista rättigheter)
The letters rwx stand for Read/Write/Execute permission. These rights are shown three times, first for the ```Owner```, then the ```Group``` and lastly ```Others``` (world) (benämns ibland 7 {1+2+4}). Första biten kan vara - (fil) eller d (katalog)
6. Sänd ```ls --full``` (lista allt)
6. Sänd ```ls -a``` (lista dolda files)
6. Sänd ```ls -a --full``` (lista allt och dolda filer)
7. Besvara: När skapades filen?
8. Vad har filen för filrättigheter?
2. Läs om chmod ```https://ss64.com/bash/chmod.htm```
### Git
13. ```git init``` Skapar repository
6. Sänd ```ls -a``` 
3. ```git status```
3. Besvara: Vad har filen ```index.html``` för status (untracked | staged | committed ) och färg?
4. Besvara: Vilken branch är vi på?
### Redigera fil
18. Redigera filen ```index.html``` med t.ex. ```<html>...</html>``` och spara (Mac: open -a textedit index.html | Windows: notepad index.html)
### Stage fil
21. ```git add index.html```
3. ```git status```
3. Besvara: Vad har filen index.html för status och färg?
### Unstage fil
23. ```git reset HEAD index.html``` Fungerar det inte så använd ```git rm --cached index.html```
3. ```git status```
### Commit fil
25. ```git add index.html``` genomför stageing
3. ```git commit -m "Lagt till HTML"```
3. Besvara: Vad rapporterar git?
3. ```git status```
3. ```git log```
3. Notera commit hash typ  `42e95e5b41a4d2351ec2850812b34cf7c2112f11`

### Uncommit (återgå till tidigare)
31. Uppdatera ```index.html``` med ```<head>...</head>``` inom ```<html>...</html>```
Stage'a och commit'a ```index.html``` med meddelandet "Lagt till BODY"
3. Tryck "pil upp" för att skrolla tillbaks till ```git status```
2. ```git log```
2. Besvara: Vad visar loggen? Två commits?
2. Notera: commit hash, vilket är tidigare commit? 
2. ```git log --stat``` visar förändringar förkortat
2. ```git log --pretty=oneline``` visar hash och commit, message och HEAD
2. ```git log -p -2``` tillsammans med pil-upp/ned. visar innehållet som förändrats (avsluta med CTRL-C)
##### Återställ till  tidigare versioner
39. ```git checkout <hash> index.html``` testa att skriva så få hash-tecken som möjligt, börja med första (från vänster)
3. ```git status```
3. Besvara: Vad rapporterar git?
3. Öppna filen ```index.html``` Återställd?
31. Uppdatera ```index.html``` igen med ```<head>...</head> och <body>...</body>``` inom ```<html>...</html>```
Stage'a och commit'a ```index.html``` med meddelandet "Lagt till HEAD och BODY"
2. Bläddra med pil-upp/ned till ```git log -p -2```  visar innehållet som förändrats (avsluta med CTRL-C)

(C) Johan Sundström