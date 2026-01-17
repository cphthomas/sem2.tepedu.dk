# Farver og Labels til Filkategorier

## Nuværende Løsning: Distinkte Ikoner

Vi har nu konfigureret forskellige ikoner for hver kategori:
- **JURA** (⚖️): `law` ikon - juridisk/domstol
- **MAKRO** (📊): `chart` ikon - graf/statistik
- **PR** (👤): `user` ikon - privat/bruger
- **SR** (🏢): `office` ikon - kontor/selskab

## Bedre Visuel Adskillelse - Anbefalede Extensions

### 1. File Utils (Anbefalet for Labels)
**Extension**: "File Utils" af sleist
- Tilføjer labels/badges til filer
- Kan tilføje farvede tags baseret på filnavn
- Installation: Søg efter "File Utils" i Extensions

### 2. Todo Tree (Til Labels/Badges)
**Extension**: "Todo Tree" af Gruntfuggly
- Kan bruges til at markere filer med badges
- Understøtter custom patterns
- Installation: Søg efter "Todo Tree" i Extensions

### 3. Peacock (Til Workspace Farvekodning)
**Extension**: "Peacock" af John Papa
- Giver workspace en farve
- Kan hjælpe med at skelne mellem projekter
- Installation: Søg efter "Peacock" i Extensions

## Alternativ Løsning: Fil Nesting med Kategorier

Vi kan aktivere fil nesting og gruppere filer efter kategori. Dette vil:
- Gruppere alle JURA filer sammen
- Gruppere alle PR filer sammen
- osv.

Se `.vscode/settings.json` for at aktivere fil nesting igen.

## Custom CSS (Avanceret)

Hvis du vil have fuld kontrol, kan du:
1. Installere "Custom CSS and JS Loader" extension
2. Tilføje custom CSS der farvekoder filnavne baseret på mønstre

**Advarsel**: Dette kan påvirke performance og kræver vedligeholdelse.

## Anbefalet Tilgang

1. **Brug de nuværende ikoner** - de er nu konfigureret til at være meget distinkte
2. **Overvej File Utils extension** - hvis du vil have labels/badges
3. **Brug søgefeltet** - filtrer efter kategori (JURA, PR, SR, MAKRO)
4. **Overvej fil nesting** - grupper relaterede filer sammen

## Hurtig Reference: Ikoner per Kategori

| Kategori | Ikon Type | Beskrivelse |
|----------|-----------|-------------|
| JURA | ⚖️ law | Juridisk/domstol ikon |
| MAKRO | 📊 chart | Graf/statistik ikon |
| PR | 👤 user | Privat/bruger ikon |
| SR | 🏢 office | Kontor/selskab ikon |

## Næste Skridt

1. Genindlæs vinduet (`Ctrl+Shift+P` → "Developer: Reload Window")
2. Tjek om ikonerne nu er mere distinkte
3. Overvej at installere "File Utils" extension for labels
4. Eller aktiver fil nesting for at gruppere filer efter kategori
