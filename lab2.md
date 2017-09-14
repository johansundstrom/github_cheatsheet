# Lab 2

## Samarbeten
Med samarbeten menas här att flera utvecklare kan utveckla olika grenar av ett befintligt offentligt repo. När man uppnått en fullgod ny funktion så merge'ar man in dessa i offentliga samtidigt. Konsumenter kan hela tiden ladda ned och använda rådande version. 

### Setup
1. Bekräfta att nuvarande branch är ```Master``` med ```git branch```
### Branch
2. Skapa ny branch med ```git branch develop```
3. ```git branch``` Notera grenarna
4. ```git branch -D develop``` Raderar branch
4. ```git branch develop``` Skapa på nytt
7. ```git branch``` Notera aktuell gren
6. ```git checkout develop``` Byter till branch New_Feature
7. ```git branch -m new_feature``` Döper om aktuell branch
8. ```git branch``` Notera aktuell gren

### Skapa innehåll i branch
10. ```git branch``` Aktuell gren är New_Feature
11. Sänd ```touch content.txt```
12. Stage och Committ'a nya filen
13. ```git status``` Kontrollera att allt är klart
14. Sänd ```ls```
15. Notera att filer från Master och New_Feature existerar
16. ```git checkout master``` Byt till Master
17. Sänd ```ls```
18. Bevaka Finder eller Filutforskaren vid bytet
19. Notera att endast filer från Master existerar
20. ```git checkout new_feature``` Byt till New_Feature
21. Sänd ```ls```
22. Notera att filer från Master och New_Feature existerar

### Merge
23. ```git branch``` Notera aktuell brach
24. ```git checkout master``` Byt till Master branch
25. ```git merge new_feature``` Slår samman ```new_feature```med aktuell branch (```master```)

### Uppstädning
26. ```git branch -d develop``` Raderar develop branch

### Use cases
27. Besvara: Skapa en branch-struktur som passar tre personer med varsin del i utvecklingsprojektet. Master ska alltid vara _deployable_
28. Besvara: Skapa en passande branch-struktur  där det finns utrymme för att arbeta med en alpha- och en beta-version av utvecklingsprojektet. Master ska alltid vara _deployable_

(C) Johan Sundström
