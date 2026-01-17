# Sådan Installerer du Labels/Badges til Filer

## Problem
Du vil gerne have farver eller labels på filerne for at skelne mellem SR, JURA, PR og MAKRO filer tydeligere.

## Løsning 1: File Utils Extension (Anbefalet)

### Installation:
1. Tryk `Ctrl+Shift+X` (Mac: `Cmd+Shift+X`) for at åbne Extensions
2. Søg efter: **"File Utils"** (af sleist)
3. Klik "Install"

### Konfiguration:
Efter installation, tilføj dette til `.vscode/settings.json`:

```json
{
    "fileutils.fileAssociations": {
        "*.JURA.*.html": {
            "label": "JURA",
            "color": "#FF6B6B"
        },
        "*.MAKRO.*.html": {
            "label": "MAKRO",
            "color": "#4ECDC4"
        },
        "*.PR.*.html": {
            "label": "PR",
            "color": "#45B7D1"
        },
        "*.SR.*.html": {
            "label": "SR",
            "color": "#96CEB4"
        }
    }
}
```

## Løsning 2: Todo Tree Extension (Alternativ)

### Installation:
1. Søg efter: **"Todo Tree"** (af Gruntfuggly)
2. Installer extension

### Konfiguration:
Tilføj til `.vscode/settings.json`:

```json
{
    "todo-tree.regexCaseSensitive": false,
    "todo-tree.highlights.customHighlight": {
        "JURA": {
            "icon": "law",
            "type": "text",
            "foreground": "#FF6B6B",
            "background": "#FFE5E5"
        },
        "MAKRO": {
            "icon": "chart",
            "type": "text",
            "foreground": "#4ECDC4",
            "background": "#E5F9F7"
        },
        "PR": {
            "icon": "user",
            "type": "text",
            "foreground": "#45B7D1",
            "background": "#E5F4F9"
        },
        "SR": {
            "icon": "office",
            "type": "text",
            "foreground": "#96CEB4",
            "background": "#E5F9F2"
        }
    }
}
```

## Løsning 3: Custom CSS (Avanceret)

### Installation:
1. Installer **"Custom CSS and JS Loader"** extension
2. Opret en CSS fil med farvekodning

**Advarsel**: Dette kan påvirke performance og kræver vedligeholdelse.

## Løsning 4: Fil Nesting (Indbygget)

Aktiver fil nesting for at gruppere filer efter kategori. Se `settings.alternativ.json` for eksempel.

## Anbefaling

**Start med Løsning 1 (File Utils)** - det er den nemmeste og mest pålidelige metode til at tilføje labels og farver til filer.

## Efter Installation

1. Genindlæs vinduet: `Ctrl+Shift+P` → "Developer: Reload Window"
2. Tjek Explorer - du skulle nu se labels/farver på filerne
