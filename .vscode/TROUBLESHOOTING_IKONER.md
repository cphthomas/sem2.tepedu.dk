# Fejlsøgning: Ikoner viser ikke forskel

## Problem
Material Icon Theme viser ikke forskellige ikoner for JURA, MAKRO, PR og SR filer.

## Mulige Løsninger

### 1. Genindlæs Ikon Temaet
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv "Preferences: File Icon Theme"
3. Vælg "Seti (Cursor)" eller et andet tema
4. Vælg "Material Icon Theme" igen
5. Dette genindlæser ikon-temaet

### 2. Opdater Material Icon Theme
1. Gå til Extensions (`Ctrl+Shift+X`)
2. Find "Material Icon Theme"
3. Klik "Update" hvis der er en opdatering
4. Genindlæs vinduet

### 3. Tjek Material Icon Theme Version
Material Icon Theme's `customClones` funktion kræver version 5.0.0 eller nyere.

### 4. Prøv Alternative Ikoner
Hvis `law`, `chart`, `user`, `office` ikke virker, prøv disse alternativer:

```json
"material-icon-theme.files.associations": {
    "*.JURA.*.html": "document",      // Alternativ 1
    "*.MAKRO.*.html": "bar-chart",    // Alternativ 2
    "*.PR.*.html": "person",          // Alternativ 3
    "*.SR.*.html": "building"         // Alternativ 4
}
```

### 5. Installer vscode-icons Extension (Alternativ)
Hvis Material Icon Theme ikke virker:

1. Installer "vscode-icons" extension
2. Skift ikon tema til "vscode-icons"
3. Konfigurer custom associations i settings.json

### 6. Brug File Nesting i Stedet
Hvis ikoner ikke virker, kan fil nesting hjælpe med visuel adskillelse:
- Se `settings.alternativ.json` for eksempel
- Aktiver fil nesting for at gruppere filer efter kategori

### 7. Tjek Settings.json Syntax
Sørg for at JSON er korrekt formateret:
- Ingen komma efter sidste element
- Alle strings i anførselstegn
- Korrekt nesting af objekter

## Nuværende Konfiguration

Ikoner er konfigureret til:
- **JURA**: `law` ikon (⚖️) - Rød (#FF6B6B)
- **MAKRO**: `chart` ikon (📊) - Turkis (#4ECDC4)
- **PR**: `user` ikon (👤) - Blå (#45B7D1)
- **SR**: `office` ikon (🏢) - Grøn (#96CEB4)

## Hvis Intet Virker

Overvej at bruge:
1. **File Utils extension** for labels/badges (se `.vscode/INSTALLER_LABELS.md`)
2. **Fil nesting** for at gruppere filer visuelt
3. **Søgefeltet** i Explorer til at filtrere efter kategori
