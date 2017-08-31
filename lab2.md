# Lab 2

## Samarbeten

### Setup
1. Bekräfta nuvarande branch med ```git branch```
2. Skapa ny branch med ```git branch develop```
3. ```git branch``` Notera grenarna
4. ```git branch -D develop``` Raderar branch
5. ```git branch -m new_feature``` döper om aktuell branch
6. ```git checkout new_feature``` Byter till branch New_Feature
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
18. ```git checkout new_feature``` Byt till Master
19. Sänd ```ls```
20. Notera att filer från Master och New_Feature existerar
### Use cases
21. Besvara: Skapa en branch-struktur som passar tre personer med varsin del i utvecklingsprojektet. Master ska alltid vara deployable
22. Besvara: Skapa en passande branch-struktur  där det finns utrymme för att arbeta med en alpha- och en beta-version av utvecklingsprojektet. Master ska alltid vara deployable