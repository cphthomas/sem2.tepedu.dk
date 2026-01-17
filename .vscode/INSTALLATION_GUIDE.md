# Installation Guide: File Utils Extension

## Fil Nesting er nu aktiveret! ✅

Fil nesting er nu aktiveret i `settings.json`. Dette betyder at:
- JURA filer grupperes sammen
- MAKRO filer grupperes sammen  
- PR filer grupperes sammen
- SR filer grupperes sammen

**Genindlæs vinduet** for at se ændringerne:
- Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
- Skriv "Developer: Reload Window"
- Tryk Enter

## Installer File Utils Extension for Labels og Farver

### Trin 1: Installer Extension
1. Tryk `Ctrl+Shift+X` (Mac: `Cmd+Shift+X`) for at åbne Extensions
2. Søg efter: **"File Utils"**
3. Find extensionen af **sleist** (eller lignende)
4. Klik **"Install"**

### Trin 2: Genindlæs Vinduet
Efter installation:
- Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
- Skriv "Developer: Reload Window"
- Tryk Enter

### Trin 3: Tjek Konfigurationen
Konfigurationen er allerede tilføjet til `settings.json`:
- JURA filer får rød label (#FF6B6B)
- MAKRO filer får turkis label (#4ECDC4)
- PR filer får blå label (#45B7D1)
- SR filer får grøn label (#96CEB4)

### Trin 4: Verificer
Efter genindlæsning skulle du nu se:
- ✅ Fil nesting (filer grupperet efter kategori)
- ✅ Labels på filerne (hvis File Utils er installeret)
- ✅ Forskellige ikoner for hver kategori

## Hvis File Utils ikke virker

Hvis File Utils extension ikke findes eller ikke virker som forventet:

### Alternativ 1: Brug kun Fil Nesting
Fil nesting er allerede aktivt og giver god visuel adskillelse.

### Alternativ 2: Prøv "Todo Tree" Extension
1. Installer "Todo Tree" extension (af Gruntfuggly)
2. Se `.vscode/INSTALLER_LABELS.md` for konfiguration

### Alternativ 3: Deaktiver Fil Nesting
Hvis du foretrækker at se alle filer individuelt:
1. Åbn `.vscode/settings.json`
2. Skift `"explorer.fileNesting.enabled": true` til `false`
3. Genindlæs vinduet

## Nuværende Status

✅ Fil Nesting: **AKTIVERET**
⏳ File Utils: **VENTER PÅ INSTALLATION**
✅ Material Icon Theme: **AKTIVERET**
✅ Custom Icons: **KONFIGURERET**

## Tips

- **Klik på pilen** ved siden af INTRO-filer for at udvide og se relaterede filer
- **Brug søgefeltet** i Explorer til at filtrere efter kategori (JURA, PR, SR, MAKRO)
- **Genindlæs vinduet** hvis ændringer ikke vises med det samme
