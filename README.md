# 🚀 App Hub

En liten landningssida som samlar mina webbappar i snygga, klickbara boxar.

**Live:** https://app-hub-xl8n.onrender.com/

## Appar

| App | Beskrivning | Länk |
| --- | --- | --- |
| 📦 **Where Did I Put It** | Håll koll på var dina saker finns — sök fram dem på sekunden. | https://where-did-i-put-it.onrender.com/ |
| 📝 **Note Taker** | Anteckningar med taggar och filtrering. | https://note-taker-app-p4cw.onrender.com/ |

## Teknik

Ren statisk HTML + CSS, inga beroenden och inget byggsteg.

```
index.html          # sidan
assets/style.css    # styling (glassmorphism, responsiv grid)
render.yaml         # Render Blueprint (static site)
```

## Kör lokalt

```bash
python3 -m http.server 8000
# öppna http://localhost:8000
```

## Deploy

Sidan är deployad på Render som en **static site** via Blueprint (`render.yaml`).

- **Blueprint:** `app-hub` (ID `exs-db9pk4bbc2fs73cpa7m0`)
- **Service:** `app-hub` · runtime `static` · region Global

### ⚠️ Auto-deploy är inte aktivt

Repot är kopplat som **public Git repository URL**, eftersom Render-appen på GitHub
bara har åtkomst till `note-taker-app` och `where-did-i-put-it`. Med den kopplingen
stödjer Render inte auto-deploy eller PR Previews.

**Efter en push måste du trycka "Manual sync"** i Render-dashboarden:
https://dashboard.render.com/blueprint/exs-db9pk4bbc2fs73cpa7m0/syncs

### Aktivera auto-deploy (engångsjobb)

1. Öppna https://github.com/apps/render/installations/new (kräver GitHub-inloggning)
2. Välj kontot `fedsan68` → lägg till repot **app-hub** bland "Only select repositories"
3. I Render: **Settings** på tjänsten → koppla om repot till GitHub-kopplingen

Därefter deployar varje push till `main` automatiskt.

## Lägga till en ny app

Kopiera ett `<a class="card">`-block i `index.html`, byt `href`, ikon, titel och text.
Lägg till en färgklass (t.ex. `card--violet`) och definiera `--accent` för den i `assets/style.css`.
