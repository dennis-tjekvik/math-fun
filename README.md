# Math Fun – Regneeventyret

Matematik for børn fra børnehave til 6. klasse (og lidt "Ekspert"). Det er en hjemmeside i én HTML-fil, uden login og uden server.

- **Appen finder selv niveauet.** Barnet vælger aldrig klassetrin. Den første runde i en verden finder ud af, hvor barnet er, og derefter følger sværhedsgraden med op og ned.
- **11 verdener:** Talbyen, Plus & Minus, Gange & Division, Uret, Pengebutikken, Brøkbageriet, Figurer & Vinkler, Måleværkstedet, Procent, Mønstre & Ligninger samt Data & Chance. Opgaverne bliver lavet af generatorer og testet automatisk.
- **Dagens mission** består af opvarmning, en hovedrunde og en udfordring eller en boss. Dagens point-loft gælder kun almindelige opgavepoint; missionsbonus, boss, stjerner og trofæer kommer oven i. Der er point, XP, streak, trofæer, samlekort, Lynregning og en butik, hvor forældrekoden skal bruges.
- **Flere børn på samme enhed:** hvert barn skriver selv sit navn og har sit eget niveau og sine egne point.
- **Til de mindste:** opgaverne læses op på dansk, når enheden har en dansk stemme. De mindste får store billeder og knapper og intet tidspres.

## Data og privatliv

Alt gemmes kun i browseren på enheden under nøgler, der starter med `mathfun-v1:`. Appen sender ingen data nogen steder hen. En lille service worker (`sw.js`) gemmer selve appen, så den også kan åbnes uden net fra hjemmeskærmen. Under Forældre → Backup kan man lave en gemmekode (`MF1:…`) til at flytte data eller sikkerhedskopiere dem.

## Udvikling

Kildekoden ligger i et privat arbejdsrepo (`src/`), og `build.sh` samler den til `math-fun.html`. Den fil udgives her som `index.html`. Tests kører med `npm test` og dækker generatorer, motor, lagring, UI-logik og E2E i Chrome.
