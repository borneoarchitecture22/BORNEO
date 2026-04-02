# Borneo — Setup completo

## Struttura file
```
borneo/
├── index.html        → sito pubblico
├── content.json      → contenuti (modificati dall'editor)
├── editor/
│   └── index.html    → pannello editor privato
├── images/           → logo e immagini progetti
└── _redirects        → configurazione Netlify
```

---

## STEP 1 — Crea il repository GitHub

1. Vai su **github.com** → accedi o registrati (gratis)
2. Clicca **New repository**
3. Nome: `borneo` (o quello che vuoi)
4. Seleziona **Public** (necessario per Netlify free)
5. Clicca **Create repository**
6. Carica tutti questi file nel repo (trascina nella pagina del repo)

---

## STEP 2 — Pubblica su Netlify

1. Vai su **netlify.com** → accedi con GitHub
2. Clicca **Add new site → Import an existing project**
3. Scegli **GitHub** → seleziona il repo `borneo`
4. Lascia tutto di default → clicca **Deploy site**
5. In 2 minuti il sito è online con un indirizzo tipo `https://borneo-xyz.netlify.app`

---

## STEP 3 — Genera il Personal Access Token GitHub

Serve all'editor per aggiornare i file nel repo.

1. Vai su **github.com/settings/tokens/new**
2. In "Note" scrivi: `Borneo editor`
3. Seleziona scadenza: `No expiration`
4. Spunta il checkbox **repo** (accesso completo al repository)
5. Clicca **Generate token**
6. **COPIA IL TOKEN** — viene mostrato una volta sola

---

## STEP 4 — Configura l'editor

1. Apri `https://tuo-sito.netlify.app/editor/`
2. Password di default: **borneo2024**
3. Alla prima apertura ti chiede:
   - **Repository**: `tuonomeutente/borneo`
   - **Token**: incolla il token copiato sopra
4. Clicca **Salva e continua**

---

## STEP 5 — Collega il tuo dominio

1. Compra il dominio su **Aruba.it** o **Namecheap.com** (es. `borneo.it`)
2. Su Netlify: **Domain settings → Add custom domain**
3. Segui le istruzioni per aggiornare i DNS su Aruba/Namecheap
4. Netlify attiva automaticamente HTTPS (certificato SSL gratuito)
5. In 24-48h il dominio è attivo

---

## Come usare l'editor

- Accedi a `/editor/` con la tua password
- **Logo**: clicca il riquadro in alto a sinistra
- **Progetti**: seleziona dalla lista, modifica titolo/immagine/descrizione
- **+ Aggiungi progetto**: crea un nuovo progetto vuoto
- **↑ Pubblica**: invia tutte le modifiche a GitHub → Netlify aggiorna il sito in ~30 secondi

## Cambiare la password

Apri `editor/index.html` e cerca la riga:
```javascript
const h = await hashPw('borneo2024');
```
Cambia `borneo2024` con la tua password, poi ricarica la pagina dell'editor
e cancella i dati del browser per quella pagina (o usa finestra in incognito la prima volta).

---

## Dominio consigliato

Per uno studio di architettura italiano: **borneo.it** su Aruba costa ~€5/anno.
