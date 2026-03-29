# SpesaSmart Bari 🛒

Web app per trovare le migliori offerte dei supermercati di Bari e risparmiare sulla spesa.

## Funzionalità
- Offerte Sigma Puglia (volantino Pasqua 2026 — 108 prodotti)
- Ricerca e filtro per categoria
- Carrello con calcolo risparmio
- Calcolo costo carburante (benzina €1,78/L)
- Pianificazione percorso ottimale
- Condivisione lista via WhatsApp
- Consegna a domicilio (+10%, min €20)
- Pannello admin: carica PDF + estrazione AI con Claude
- Esportazione CSV

## Deploy su Vercel (gratuito, 5 minuti)

### Metodo A — GitHub (consigliato)

1. Crea un account su [github.com](https://github.com) (gratis)
2. Crea un nuovo repository: clicca **New** → nome: `spesasmart-bari` → **Create repository**
3. Carica la cartella: trascina i file nella pagina GitHub oppure usa il terminale:
   ```
   cd spesasmart
   git init
   git add .
   git commit -m "SpesaSmart Bari v1.0"
   git branch -M main
   git remote add origin https://github.com/TUO-USERNAME/spesasmart-bari.git
   git push -u origin main
   ```
4. Vai su [vercel.com](https://vercel.com) → **Sign up with GitHub**
5. Clicca **New Project** → seleziona il repository `spesasmart-bari`
6. Lascia tutto di default → clicca **Deploy**
7. In 2 minuti la tua app è live su `spesasmart-bari.vercel.app` 🎉

### Metodo B — Drag & Drop (ancora più semplice)

1. Esegui `npm run build` nella cartella del progetto
2. Vai su [vercel.com](https://vercel.com) → **New Project** → **Browse** (in basso)
3. Trascina la cartella `dist/` generata
4. Deploy automatico!

### Dominio personalizzato (opzionale)

- In Vercel: **Settings → Domains** → aggiungi `spesasmart.it`
- Acquista il dominio su [namecheap.com](https://namecheap.com) (~€10/anno)
- Segui le istruzioni per i DNS

## Sviluppo locale

```bash
npm install
npm run dev
# apri http://localhost:5173
```

## Struttura progetto

```
spesasmart/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Topbar.jsx       # Barra navigazione
│   │   ├── TabHome.jsx      # Home con configurazione
│   │   ├── TabOfferte.jsx   # Griglia offerte con filtri
│   │   ├── TabCarrello.jsx  # Carrello e pagamento
│   │   ├── TabPercorso.jsx  # Percorso e costi
│   │   ├── TabAdmin.jsx     # Pannello admin
│   │   └── Toast.jsx        # Notifiche
│   ├── data.js              # Prodotti Sigma + dati negozi
│   ├── App.jsx              # Componente principale
│   ├── main.jsx             # Entry point
│   └── index.css            # Stili globali
├── index.html
├── package.json
├── vite.config.js
└── vercel.json
```

## Prossimi passi (backend)

Per lo scraping automatico dei volantini e il database:
- **Backend**: Node.js + Express (deploy su Railway.app, gratis)
- **Database**: PostgreSQL (Railway include 1GB gratis)
- **Scraping**: Puppeteer per volantini dinamici + Claude Vision API per PDF
- **Scheduling**: cron job settimanale per aggiornamento automatico offerte

## Tecnologie

- React 18 + Vite
- CSS custom (no framework, performance ottimale)
- Claude AI API (per estrazione prodotti da PDF)

---
Made with SpesaSmart © 2026 — Bari, Puglia 🌊
