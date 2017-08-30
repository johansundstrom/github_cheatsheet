# Lab
## Versionshantering

### Setup
1. ```http://git-scm.com/download``` (installera) Senaste release 2.14.1
2. Skapa mappen ```Mina projekt``` i filsystemet
3. Högerklicka mappen och välj ```Git Bash Here```
### Skapa fil
4. Sänd ```touch index.html``` 
5. Sänd ```ls``` (list)
6. Sänd ```ls -l``` (lista rättigheter)
The letters rwx stand for Read/Write/Execute permission. These rights are shown three times, first for the ```Owner```, then the ```Group``` and lastly ```Others``` (world) (benämns ibland 7 {1+2+4})
6. Sänd ```ls --full``` (allt)
6. Sänd ```ls -a``` (visa hidden files)
6. Sänd ```ls -a --full``` (visa allt och hidden files)
7. Besvara: När skapades filen?
8. Vad har filen för filrättigheter?
2. Läs om chmod ```https://ss64.com/bash/chmod.htm```
### Git
13. ```git init``` Skapar repository
6. Sänd ```ls -a``` (visa hidden files)
3. ```git status```
3. Besvara: Vad har filen index.html för status och färg?
4. Besvara: Vilken branch är vi på?
### Redigera fil
18. Redigera filen ```index.html``` med t.ex. ```<html>...</html>``` och spar
3. ```git status```
3. Besvara: Vad har filen index.html för status och färg?
### Stage fil
21. ```git add index.html```
3. Besvara: Vad har filen index.html för status och färg?
### Unstage fil
23. ```git reset HEAD index.html```
3. ```git status```
### Commit fil
25. ```git add index.html```
3. ```git commit -m "Min första commit"```
3. Besvara: Vad rapporterar git?
3. ```git status```
### Uncommit fil
29. Uppdatera ```index.html``` med ```<body>...</body>``` inom ```<html>...</html>```
Stage'a och commit'a ```index.html``` med meddelandet "Lagt till body"
3. Tryck "pil upp" för att skrolla tillbaks till ```git status```
2. ```git log```
2. Besvara: Vad visar loggen? Två commits?
2. Notera: commit hash 
2. ```git log --stat``` visar förändringar förkortat
2. ```git log --pretty=oneline``` visar hash och commit, message och HEAD
2. ```git log -p -2``` tillsammans med pil-upp/ned. visar innehållet som förändrats
1. ```git checkout <hash> index.html``` testa att skriva så få hash-tecken som möjligt
3. ```git status```
3. Besvara: Vad rapporterar git?