# Währungsrechner — Beratung Hagl

Statische Webanwendung zur Echtzeit-Währungsumrechnung (EUR · USD · GBP).

## Deployment auf Vercel

### Option 1 — Vercel CLI (empfohlen)

```bash
npm i -g vercel
cd waehrungsrechner
vercel
```

Beim ersten Mal einmalig anmelden. Danach:
- Projekt wird automatisch erkannt (statisch, kein Build-Schritt)
- URL wird direkt ausgegeben (z. B. `https://waehrungsrechner.vercel.app`)

Für Production-Deploy:

```bash
vercel --prod
```

### Option 2 — Vercel Dashboard (ohne CLI)

1. [vercel.com](https://vercel.com) öffnen → **Add New Project**
2. Diesen Ordner als ZIP hochladen **oder** GitHub-Repo verknüpfen
3. Framework: **Other** (kein Build-Schritt nötig)
4. **Deploy** klicken — fertig

### Option 3 — GitHub + Vercel (automatisch)

1. Ordner in ein GitHub-Repo pushen
2. In Vercel: **Import Git Repository** → Repo auswählen
3. Bei jedem Push auf `main` wird automatisch neu deployed

## Projektstruktur

```
waehrungsrechner/
├── index.html      # Gesamte App (HTML + CSS + JS)
├── vercel.json     # Vercel-Konfiguration
└── README.md       # Diese Datei
```

## Technik

- **Kein Framework, kein Build-Schritt** — reines HTML/CSS/JS
- Kursdaten: [fawazahmed0/exchange-api](https://github.com/fawazahmed0/exchange-api) (kostenlos, kein API-Key)
- CI: Beratung Hagl (Farben, Schrift Inter, Leitmetapher)

