# Lab 3

## Arbeta mot remote repositories

### Förutsättning: centralt repo kan vara...
* GitHub (HTTP)
* GIT (Git)
* Delat filutrymme (Local) 
* Terminal (SSH)

### Kontrollera användaruppgifter
1. ```git config user.name``` Visar aktuellt användarnamn för inloggning remote
2. ```git config user.email``` Visar aktuellt epost för inloggning remote
3. ```git config user.name "olleolle"```Ändrar aktuellt användarnamn för inloggning remote
4. ```git config user.email "olle@olle.se``` Visar aktuellt epost för inloggning remote
5. ```git config --list``` Visar aktuella inställningar

### Anslutning till remote repo
7. ```git remote``` Notera att inga anslutningar finns
8. ```git remote add origin http://github.com/johansundstrom/gitlab.git``` 
9. Notera att det går att ansluta till remote repo och hämta data utan giltigt användarnamn och lösenord
10. Gör en förändring i en fil lokalt, Stage'a och Commit'a i Master
11. ```git push origin master``` Notera att GitHub frågar efter giltigt användarnamn och lösenord
12. Om du fått giltigt användarnamn och lösenord, ställ in dessa enligt p.1-2
13. ```git push origin master``` Notera att push 
14. ```git remote``` Notera att ```origin``` listas
15. ```git remote -v``` Lista verbose. Notera (fetch) och (push) adresser
16. ```git remote rm origin``` Raderar befintliga anslutningar

### Hämtar filer från centralt repo, skapar lokal mapp samt .git 
#### git clone - används för att etablera första gången
17. Med terminalen, gå till lämplig plats i filsystemet ```cd <mapp>```
Git clone gör följande tre kommandon
* git init
* git remote add origin [url]
* git pull origin master
18. Markera en lämplig plats i filsystemet dit det externa innehållet skall skapas
19. ```git clone http://github.com/johansundstrom/gitlab.git``` Skapa lokal mapp och klonar allt
20. Notera att mapp skapats med ```ls```
21. Gå in i mappen ```cd gitlab```
22. ```ls``` Notera att det bör finnas ett innehåll
 
### Publicera lokala förändringar på ett anslutningsnamn
#### git push - används för att uppdatera centralt repo
23. Öppna och redigera fil i mappen gitlab - spara
24. stage'a och commit'a förändringarna
25. ```git push http://github.com/johansundstrom/gitlab.git``` alternativt ```git push origin master```

Hämtar förändringar från origin och uppdaterar arbetsfiler i HEAD
### uppdatera lokal repo från central repo
#### git fetch - uppdaterar lokal repo med centrala uppdateringar
26. ```git fetch http://github.com/johansundstrom/gitlab.git```
27. ```git fetch origin``` är ett enklare alternativ till ovanstående, kräver etablerad origin
Ta för vana att uppdatera lokal repo innan lokalt arbete inleds.
```git fetch``` laddar bara ned filer från central repo, men det integrerar inte de lokala arbetsfilerna. Fetch är bra för att inhämta alla förändringar i centralt repo. Det är inte destruktivt.

Hämtar förändringar från origin och uppdaterar arbetsfiler i HEAD
### uppdaterar lokal repo från central repo
#### git pull - uppdaterar lokal repo med centrala uppdateringar
Git clone gör följande två kommandon
* git fetch
* git merge origin/master
26. ```git pull origin master```
Eftersom ```git pull``` försöker att göra merge centrala förändringar med de lokala så är ```merge confict``` vanligt. Rekommendationen är därför att bara använda ```git pull``` på ren arbetskopia (lokal repo).

Ta för vana att uppdatera lokal repo innan lokalt arbete inleds

Hämtar förändringar från origin och uppdaterar arbetsfiler i HEAD

18. ```git fetch <url>``` Hämta förändringar från origin
19. ```git remote``` Lista anslutningar (```origin``` är standard kortnamn på anslutning)
20. ```git remote -v``` Lista anslutningar verbose

### 
### Hämta förändringar 
... mer kommer snart

(C) Johan Sundström
