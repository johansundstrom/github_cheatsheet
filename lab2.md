# Lab 2

## Samarbeten
Med samarbeten menas här att flera utvecklare kan utveckla olika grenar av ett befintligt offentligt repo. När man uppnått en fullgod ny funktion så merge'ar man in dessa i offentliga samtidigt. Konsumenter kan hela tiden ladda ned och använda rådande version. 

### Setup
1. Bekräfta att nuvarande branch är ```Master``` med ```git branch```
2. Skapa ny branch med ```git branch develop```
<<<<<<< HEAD
3. ```git branch``` notera grenarna
4. ```git branch -D develop``` raderar branch
5. ```git branch -m new_feature``` döper om aktuell branch
6. ```git checkout new_feature``` Byter till branch New_Feature
=======
3. ```git branch``` Notera grenarna
4. ```git branch -D develop``` Raderar branch
4. ```git branch develop``` Skapa på nytt
7. ```git branch``` Notera aktuell gren
6. ```git checkout develop``` Byter till branch New_Feature
5. ```git branch -m new_feature``` Döper om aktuell branch
>>>>>>> 9f2674b6a3bc0c974854fd1bc5c2b0a93d19835a
7. ```git branch``` Notera aktuell gren

### Skapa innehåll i branch
8. ```git branch``` Aktuell gren är New_Feature
9. Sänd ```touch content.txt```
10. Stage och Committ'a nya filen
11. ```git status``` Kontrollera att allt är klart
12. Sänd ```ls```
13. Notera att filer från Master och New_Feature existerar
14. ```git checkout master``` Byt till Master
15. Sänd ```ls```
16. Bevaka Finder eller Filutforskaren vid bytet
17. Notera att endast filer från Master existerar
18. ```git checkout new_feature``` Byt till New_Feature
19. Sänd ```ls```
20. Notera att filer från Master och New_Feature existerar
### Use cases
<<<<<<< HEAD
21. Besvara: Skapa en branch-struktur som passar tre personer med varsin del i utvecklingsprojektet. Master ska alltid vara deployable
22. Besvara: Skapa en passande branch-struktur  där det finns utrymme för att arbeta med en alpha- och en beta-version av utvecklingsprojektet. Master ska alltid vara deployable
### Merge branch
23. ```git checkout master``` Byt till Master
24. ```git merge new_feature``` Notera eventuella konflikter
25. Vid konflikt: Oppna filen och lös problemet
### Radera branch
26. ```git branch -d new_feature``` 
27. ```git branch``` Kontrollera borttagen branch
=======
21. Besvara: Skapa en branch-struktur som passar tre personer med varsin del i utvecklingsprojektet. Master ska alltid vara _deployable_
22. Besvara: Skapa en passande branch-struktur  där det finns utrymme för att arbeta med en alpha- och en beta-version av utvecklingsprojektet. Master ska alltid vara _deployable_
(C) Johan Sundström
>>>>>>> 9f2674b6a3bc0c974854fd1bc5c2b0a93d19835a
