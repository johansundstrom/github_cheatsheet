# Lab 2

## Samarbeten - Branch/Merge
Med samarbeten menas här att flera utvecklare samtidigt kan skapa nya grenar (branch)av ett befintligt offentligt repo. I dessa kan arbeten pågå och utvecklas utan att störa huvudgrenen. Efter att man uppnått en fullgod ny funktion i en ny gren så merge'as dessa in i och uppgraderar huvudgrenen. Konsumenter kan hela tiden ladda ned och använda versionen som ligger i huvudgrenen samtidigt som arbeten pågår i olika mer eller mindre offentliga grenar. 

### Setup
1. Bekräfta att nuvarande branch är ```Master``` med ```git branch```
### Branch
2. Skapa ny branch med ```git branch develop```
3. ```git branch``` Notera grenarna
4. ```git branch --delete develop``` Raderar branch develop
4. ```git branch develop``` Skapa på nytt
7. ```git branch``` Notera aktuell gren
6. ```git checkout develop``` Byter till branch develop
7. ```git branch --move new_feature``` Flyttar eller döper om aktuell branch
8. ```git branch``` Notera aktuell gren

### Skapa innehåll i branch
10. ```git branch``` Aktuell gren är New_Feature
11. ```touch content.txt``` Skapa fil
12. Stage och Committ'a nya filen
13. ```git status``` Kontrollera att allt är klart
14. ```ls``` Notera att filen skapades
15. Notera att filer från branch Master och New_Feature existerar
16. ```git checkout master``` Byt till Master
17. ```ls``` Filen content.txt ska inte finnas i master 
18. Bevaka Finder eller Filutforskaren vid bytet
19. Notera att endast filer från Master existerar
20. ```git checkout new_feature``` Byt till New_Feature
21. Sänd ```ls```
22. Notera att filer från Master och New_Feature existerar
23. ```git log --oneline --decorate --graph --all -5``` Lista de 5 senaste händelserna

### Merge
23. ```git branch``` Notera aktuell branch
24. ```git checkout master``` Byt till master branch
25. ```ls``` Notera att ```content.txt``` INTE finns i ```Master```
26. ```git merge new_feature``` Slår samman ```new_feature```med aktuell branch (```master```)
27. ```ls``` Notera att ```content.txt``` FINNS i ```Master```

### Uppstädning
28. ```git branch -d develop``` Raderar develop branch

### Use cases
29. Besvara: Skapa en branch-struktur som passar tre personer som på varsit håll kan utveckla utan att störa vandra. De tre delarna är faster-login, log-bugfix och social-feature i utvecklingsprojektet. Master ska alltid vara _deployable_ och samtliga utvecklare ska ha tillgång en samlad gren.

30. Besvara: Skapa en passande branch-struktur för en applikation som ständigt utvecklas och skapar major och minor versioner. Master ska alltid vara _deployable_

31. Besvara: Hur skulle en struktur kunna se ut för ett pågående utvecklingsarbete som passar fyra utvecklingsteam (planning, order, lager och fakturering) i en organisation. Planningteamet styr och sammanställer projektet från de tre övriga grupperna. Varje teamledare ansvarar för sitt team på fem person och varje person kan se sidledes och ett steg upp.

(C) Johan Sundström
