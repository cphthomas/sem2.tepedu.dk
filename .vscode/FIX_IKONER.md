# Fix Ikoner - Alle Filer Skal Have Nyt Ikon

## Problem
Kun nogle filer får nyt ikon (fx kun nogle MAKRO filer).

## Løsning

### 1. Anvend Ikon Customization (KRITISK!)
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv: **"Icons: Apply Icons Customization"**
3. Tryk Enter
4. **VENT** til kommandoen er helt færdig (kan tage 10-30 sekunder)

### 2. Genindlæs Vinduet
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv: **"Developer: Reload Window"**
3. Tryk Enter

### 3. Luk og Genåbn Cursor (Hvis stadig ikke virker)
1. Luk Cursor helt
2. Åbn Cursor igen
3. Åbn workspace igen

## Nye Ikoner (Mere Distinkte)

- **JURA filer**: `react` ikon (blå React logo) ⚛️
- **MAKRO filer**: `python` ikon (blå/gul Python logo) 🐍
- **PR filer**: `node` ikon (grøn Node.js logo) 🟢
- **SR filer**: `docker` ikon (blå Docker logo) 🐳

## Hvis Ikoner Stadig Ikke Virker

### Prøv Alternative Ikoner
Hvis `react`, `python`, `node`, `docker` ikke virker, prøv disse:

```json
"vsicons.associations.files": [
    {
        "icon": "angular",
        "extensions": ["jura"],
        "format": "svg"
    },
    {
        "icon": "java",
        "extensions": ["makro"],
        "format": "svg"
    },
    {
        "icon": "php",
        "extensions": ["pr"],
        "format": "svg"
    },
    {
        "icon": "ruby",
        "extensions": ["sr"],
        "format": "svg"
    }
]
```

### Tjek om Ikoner Findes
1. Gå til Extensions → vscode-icons → Details
2. Se dokumentationen for tilgængelige ikon-navne
3. Prøv ikoner der helt sikkert findes (fx `html`, `css`, `js`, `ts`)

## Vigtigt!

**Du SKAL køre "Icons: Apply Icons Customization" efter hver ændring!**

Uden dette trin vil ikonerne ikke opdatere for alle filer.

## Debug

Hvis kun nogle filer får nyt ikon:
1. Tjek om file associations matcher alle filerne korrekt
2. Prøv at genstarte Cursor helt
3. Tjek om der er cache problemer (prøv at slette `.vscode` cache)
