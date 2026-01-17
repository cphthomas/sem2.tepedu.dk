# Quick Start: Fil Organisering

## Hurtige Tips

### 1. Installer og Aktiver Material Icon Theme (2 minutter)
1. Tryk `Ctrl+Shift+X` (eller `Cmd+Shift+X` på Mac) for at åbne Extensions
2. Søg efter: `Material Icon Theme`
3. Klik "Install"
4. **VIGTIGT**: Efter installation skal du:
   - Tryk `Ctrl+Shift+P` (eller `Cmd+Shift+P`) 
   - Søg efter "Preferences: File Icon Theme"
   - Vælg "Material Icon Theme"
   - **ELLER** genstart Cursor/VS Code for at aktivere temaet automatisk

### 2. Hvis ikoner stadig ikke vises
- Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
- Skriv "Developer: Reload Window" og tryk Enter
- Dette genindlæser vinduet og aktiverer ikonerne

### 2. Brug Fil Nesting
- Klik på pilen ved siden af INTRO-filer for at se relaterede filer
- Eksempel: Åbn `8.PR.INTRO.1.html` → Se alle relaterede PR filer grupperet

### 3. Filtrer Filer
I Explorer, brug søgefeltet:
- `JURA` → Kun juridiske filer
- `PR` → Kun privat rådgivning
- `SOL` → Kun løsningsfiler
- `WORK` → Kun opgavefiler
- `TEST` → Kun testfiler

### 4. Hurtig Navigation
- `Ctrl+P` (Mac: `Cmd+P`) → Hurtig filnavigation
- Skriv filnavn eller kategori for at finde filer hurtigt

## Fil Mønstre

```
[NUMBER].[CATEGORY].[TYPE].[SUBTYPE].html

Eksempler:
- 8.PR.INTRO.1.html
- 11.PR.WORK.SOL.2.html
- 13.SR.TEMA.3.html
```

**Kategorier:**
- JURA (1-5)
- MAKRO (6-7)  
- PR (8-12)
- SR (13-14)

**Typer:**
- INTRO = Introduktion
- TEMA = Tema/Undervisning
- WORK = Opgave
- SOL = Løsning
- TEST = Test
