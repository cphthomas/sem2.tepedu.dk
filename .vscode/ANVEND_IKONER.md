# Anvend Ikon Ændringer - VIGTIGT!

## Problem: Kun nogle ikoner ændrer sig

Hvis kun nogle ikoner (fx MAKRO) ændrer sig, men ikke alle, skal du:

### 1. Anvend Ikon Customization (KRITISK!)
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv: **"Icons: Apply Icons Customization"**
3. Tryk Enter
4. Vent til kommandoen er færdig

### 2. Genindlæs Vinduet
1. Tryk `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`)
2. Skriv: **"Developer: Reload Window"**
3. Tryk Enter

### 3. Luk og Genåbn Cursor (Hvis stadig ikke virker)
1. Luk Cursor helt
2. Åbn Cursor igen
3. Åbn workspace igen

## Nuværende Konfiguration

- **JURA filer**: `_vue` ikon (grøn) - Vue.js ikon
- **MAKRO filer**: `_image` ikon (blå) - Image ikon ✅ Virker!
- **PR filer**: `_sql` ikon (blå) - SQL ikon
- **SR filer**: `_yaml` ikon (lilla) - YAML ikon

## Hvis Ikoner Stadig Ikke Skifter

### Prøv Alternative Ikoner
Hvis `_vue`, `_sql`, `_yaml` ikke virker, prøv disse:

```json
"vsicons.associations.files": [
    {
        "icon": "_js",
        "extensions": ["jura"],
        "format": "svg"
    },
    {
        "icon": "_image",
        "extensions": ["makro"],
        "format": "svg"
    },
    {
        "icon": "_ts",
        "extensions": ["pr"],
        "format": "svg"
    },
    {
        "icon": "_json",
        "extensions": ["sr"],
        "format": "svg"
    }
]
```

### Tjek Ikon Navne
Se liste over tilgængelige ikoner:
- Gå til Extensions → vscode-icons → Details
- Se dokumentationen for ikon-navne

## Vigtigt!

**Du SKAL køre "Icons: Apply Icons Customization" efter hver ændring i settings.json!**

Uden dette trin vil ikonerne ikke opdatere.
