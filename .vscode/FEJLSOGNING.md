# Fejlsøgning: Filer vises ikke i Explorer

## Problem: Filer vises ikke, men ikoner er ændret

Dette betyder at Material Icon Theme virker, men filerne er skjult eller Explorer viser dem ikke korrekt.

## Løsninger (prøv i rækkefølge):

### 1. Tjek at Explorer-panelet er åbent
- Tryk `Ctrl+Shift+E` (Mac: `Cmd+Shift+E`) for at åbne Explorer-panelet
- Eller klik på fil-ikonet i venstre sidebar

### 2. Genindlæs vinduet
- Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
- Skriv "Developer: Reload Window"
- Tryk Enter

### 3. Tjek Explorer-indstillinger
- Tryk `Ctrl+,` (Mac: `Cmd+,`) for at åbne Settings
- Søg efter "explorer"
- Tjek at følgende er sat korrekt:
  - `explorer.fileNesting.enabled`: skal være `false` (hvis filer skal vises alle sammen)
  - `files.exclude`: skal være tom eller kun indeholde filer du vil skjule

### 4. Tjek om filer er skjult af fil nesting
Hvis fil nesting er aktiveret, kan relaterede filer være skjult under hovedfilerne:
- Klik på pilen ved siden af filer for at udvide dem
- Eller deaktiver fil nesting i settings.json (som allerede er gjort)

### 5. Tjek Explorer-filtre
- I Explorer-panelet, tjek om der er noget i søgefeltet øverst
- Ryd søgefeltet hvis der er noget i det
- Tjek om der er aktive filtre i Explorer-toolbar

### 6. Tjek workspace-root
- Sørg for at du har åbnet det rigtige workspace/projekt
- Tjek at du er i root-mappen hvor HTML-filerne ligger

### 7. Genstart Cursor helt
Hvis intet virker:
- Luk Cursor helt
- Åbn det igen
- Åbn workspace igen

## Hvis filerne stadig ikke vises:

1. Tjek om filerne faktisk findes:
   - Åbn terminal i Cursor (`Ctrl+` ` eller `Cmd+` `)
   - Kør: `ls *.html` (Mac/Linux) eller `dir *.html` (Windows)
   - Dette viser om filerne faktisk findes

2. Tjek .gitignore eller .cursorignore:
   - Disse filer kan skjule filer fra Explorer
   - Tjek om HTML-filer er i ignore-listerne

3. Tjek Explorer-sortering:
   - Højreklik i Explorer-panelet
   - Tjek sorteringsindstillinger
   - Prøv at sortere efter "Name" eller "Type"

## Aktuelle indstillinger:

Fil nesting er nu **deaktiveret**, så alle filer skulle vises individuelt i Explorer.

Hvis du vil aktivere fil nesting igen (for at gruppere relaterede filer), kan du:
1. Åbn `.vscode/settings.json`
2. Skift `"explorer.fileNesting.enabled": false` til `true`
3. Fjern kommentarer fra `explorer.fileNesting.patterns`
