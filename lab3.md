# Lab 3

## Central repository

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
10. ```git remote``` Notera att ```origin``` listas
11. ```git remote -v``` Lista verbose. Notera (fetch) och (push) adresser
12. ```git remote rm origin``` Raderar befintliga anslutningar



##### Fortsättningsvis talar vi endast om HTTP.
12. ```git clone <url>``` (ex. http://github.com/johansundstrom/gitlab.git) Skapa lokal mapp och klonar allt
2. ```git fetch <url>``` Hämta förändringar från origin
3. ```git remote``` Lista anslutningar (```origin``` är standard kortnamn på anslutning)
4. ```git remote -v``` Lista anslutningar verbose

### Hämta förändringar 
... mer kommer snart

(C) Johan Sundström
