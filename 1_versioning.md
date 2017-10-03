# Lab 1

## Versionshantering
Med versionshantering menas här att en mapp eller fil's innehåll kan finnas i olika versioner. Det är möjligt och också vanligt att backa till tidigare version om så behövs av någon anledning. 

### Setup
1. ```http://git-scm.com/download``` (installera) Senaste release 2.14.1 (2017-08-04)
2. Skapa mappen ```Mina Repos``` i filsystemet
3. Skapa mappen ```git_lab``` inuti ```Mina Repos```
4. Högerklicka mappen och välj ```Git Bash Here```
5. ```git config --global user.name "johansundstrom"``` - Tillägget --global ger 
åtkomst i alla projektmappar
6. ```git config --global user.email "johan.sundstrom@mdh.se"```
7. ```git config --global color.ui auto``` - Färg UI
8. ```git config --list``` Listar konfigurering

### Skapa fil
9. Med ```cd <mapp>``` och ```mkdir <ny mapp>``` gå till lämplig plats i filsystemet (Mina dokument/proj) 
10. Sänd ```ls``` (list) konstatera att det är tomt
11. Sänd ```touch index.html``` Skapar index.html
12. Sänd ```ls```
13. Sänd ```ls -l``` (listar rättigheter)
Bokstäverna rwx står för Read/Write/Execute rättighet. Dessa visas tre gånger, först för ```Owner```, därefter ```Group``` och sist ```Others``` (world). RWX benämns ibland 7 (1+2+4). Första biten kan vara - (fil) eller d (katalog)
14. Sänd ```ls -full``` (lista allt)
15. Sänd ```ls -a``` (lista mappar som börjar med dot)
16. Sänd ```ls -a -full``` (lista utökat och mappar som börjar med dot)
17. Besvara: När skapades filen?
18. Vad har filen för filrättigheter?
19. Läs om chmod ```https://ss64.com/bash/chmod.htm```
### Git
20. ```git init``` Skapar lokalt repository
21. Sänd ```ls -a``` 
22. ```git status```
23. Besvara: Vad har filen ```index.html``` för status (untracked | staged | committed ) och färg?
24. Besvara: Vilken branch är vi på?
### Redigera fil
25. Redigera filen ```index.html``` med t.ex. ```<html>...</html>``` och spara (Mac: ```open -a textedit index.html``` | Windows: ```notepad index.html``` | Linux: ```nano index.html```)
### Stage fil
26. ```git add index.html```
27. ```git status```
28. Besvara: Vad har filen index.html för status och färg?
### Unstage fil
29. ```git reset HEAD index.html``` Fungerar det inte så använd ```git rm --cached index.html```
30. ```git status```
### Commit fil
31. ```git add index.html``` genomför stageing
32. ```git commit --message "Lagt till HTML"```
33. Besvara: Vad rapporterar git?
34. ```git status```
35. ```git log```
36. Notera commit hash typ  `42e95e5b41a4d2351ec2850812b34cf7c2112f11`

### Uncommit (återgå till tidigare)
37. Uppdatera ```index.html``` med ```<head>...</head>``` inom ```<html>...</html>```
Stage'a och commit'a ```index.html``` med meddelandet "Lagt till BODY"
38. Tryck "pil upp" för att skrolla tillbaks till ```git status```
39. ```git log```
40. Besvara: Vad visar loggen? Två commits?
41. Notera: commit hash, vilket är tidigare commit? 
42. ```git log --stat``` visar förändringar förkortat (pil upp/ned, Q för avslut)
43. ```git log --pretty=oneline``` visar hash, commit message och HEAD
44. ```git log --patch -2``` Visar förändringar i innehållet (pil upp/ned, Q för avslut)
##### Återställ till  tidigare versioner
45. ```git checkout <hash> index.html``` testa att skriva så få hash-tecken som möjligt, börja med första (från vänster)
46. När Git säger ```Prevoious HEAD was <hash>... HEAD is now at <hash>...``` har ny version lästs in
47. ```git status```
48. Besvara: Vad rapporterar git?
49. Öppna filen ```index.html``` Återställd?
50. Uppdatera ```index.html``` igen med ```<head>...</head> och <body>...</body>``` inom ```<html>...</html>```
Stage'a och commit'a ```index.html``` med meddelandet "Lagt till HEAD och BODY"
51. Bläddra med pil-upp/ned till ```git log -patch -2```  visar innehållet som förändrats (avsluta med CTRL-C)

(C) Johan Sundström
