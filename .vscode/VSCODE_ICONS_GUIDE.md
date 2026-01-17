# vscode-icons Konfiguration Guide

## Status
✅ vscode-icons er nu konfigureret til at vise forskellige ikoner for hver kategori.

## Konfigurerede Ikoner

- **JURA filer**: `_pdf` ikon (📄) - PDF ikon (rød/orange)
- **MAKRO filer**: `_image` ikon (🖼️) - Image ikon (blå)
- **PR filer**: `_document` ikon (📄) - Document ikon (grøn)
- **SR filer**: `_folder` ikon (📁) - Folder ikon (lilla)

## Hvordan Det Virker

Vi bruger custom extensions (jura, makro, pr, sr) og mapper HTML filer til disse extensions:
- `*.JURA.*.html` → behandles som `.jura` filer → får `_pdf` ikon
- `*.MAKRO.*.html` → behandles som `.makro` filer → får `_image` ikon
- `*.PR.*.html` → behandles som `.pr` filer → får `_document` ikon
- `*.SR.*.html` → behandles som `.sr` filer → får `_folder` ikon

## Anvend Ændringerne

Efter at have opdateret `settings.json`, skal du:

### 1. Anvend Ikon Customization
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv: **"Icons: Apply Icons Customization"**
3. Tryk Enter

Dette anvender de nye ikon-indstillinger.

### 2. Genindlæs Vinduet
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv: **"Developer: Reload Window"**
3. Tryk Enter

## Hvis Ikoner Ikke Skifter

### Prøv Alternative Ikon Navne
Hvis `law`, `chart`, `user`, `office` ikke virker, prøv disse alternativer:

```json
"vsicons.associations.files": [
    {
        "icon": "document",
        "filenamePatterns": ["*JURA*.html"],
        "format": "svg"
    },
    {
        "icon": "bar-chart",
        "filenamePatterns": ["*MAKRO*.html"],
        "format": "svg"
    },
    {
        "icon": "person",
        "filenamePatterns": ["*PR*.html"],
        "format": "svg"
    },
    {
        "icon": "building",
        "filenamePatterns": ["*SR*.html"],
        "format": "svg"
    }
]
```

### Tjek Tilgængelige Ikoner
vscode-icons har mange ikoner. Du kan se listen her:
- Gå til Extensions → vscode-icons → Details
- Se dokumentationen for tilgængelige ikon-navne

### Brug Præcise Filnavne (Alternativ)
Hvis `filenamePatterns` ikke virker, kan du bruge præcise filnavne:

```json
"vsicons.associations.files": [
    {
        "icon": "law",
        "filenames": ["1.JURA.INTRO.1.html", "2.JURA.INTRO.2.html"],
        "format": "svg"
    }
]
```

Men dette kræver at liste alle filnavne, hvilket ikke er praktisk.

## Nuværende Konfiguration

Ikoner er konfigureret til at matche:
- `*JURA*.html` → law ikon
- `*MAKRO*.html` → chart ikon
- `*PR*.html` → user ikon
- `*SR*.html` → office ikon

## Tips

1. **Anvend customization** efter hver ændring i settings.json
2. **Genindlæs vinduet** hvis ikoner ikke opdateres
3. **Tjek ikon-navne** i vscode-icons dokumentation hvis ikoner ikke vises
4. **Brug File Utils extension** hvis ikoner stadig ikke virker (se `.vscode/INSTALLER_LABELS.md`)

## Næste Skridt

1. Anvend ikon customization (`Ctrl+Shift+P` → "Icons: Apply Icons Customization")
2. Genindlæs vinduet
3. Tjek Explorer - filerne skulle nu have forskellige ikoner baseret på kategori
