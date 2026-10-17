# 🚀 App Hub

En liten landningssida som samlar mina webbappar i snygga, klickbara boxar.

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

## Deploya på Render

### Alternativ A — Blueprint (rekommenderas)

1. Gå till https://dashboard.render.com/blueprints → **New Blueprint Instance**
2. Välj repot `fedsan68/app-hub`
3. Render läser `render.yaml` och skapar static site-tjänsten → **Apply**

### Alternativ B — Manuellt

1. https://dashboard.render.com → **New** → **Static Site**
2. Välj repot `fedsan68/app-hub`
3. Inställningar:
   - **Build Command:** lämna tomt
   - **Publish Directory:** `.`
4. **Create Static Site**

Varje push till `main` deployar automatiskt.

## Lägga till en ny app

Kopiera ett `<a class="card">`-block i `index.html`, byt `href`, ikon, titel och text.
Lägg till en färgklass (t.ex. `card--violet`) och definiera `--accent` för den i `assets/style.css`.
