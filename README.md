# Ristorante

> Applicazione web per il ristorante, sviluppata con **React**, **TypeScript** e **Vite**.


## Indice

- [Tecnologie](#-tecnologie)
- [Requisiti](#-requisiti)
- [Installazione](#-installazione)
- [Script disponibili](#-script-disponibili)
- [Struttura del progetto](#-struttura-del-progetto)
- [Qualità del codice](#-qualità-del-codice)
- [Deploy](#-deploy)
- [Contribuire](#-contribuire)
- [Licenza](#-licenza)

---

## Tecnologie

| Strumento | Versione | Ruolo |
|---|---|---|
| [React](https://react.dev) | 19 | Libreria UI |
| [TypeScript](https://www.typescriptlang.org) | 6.0 | Tipizzazione statica |
| [Vite](https://vite.dev) | 8 | Dev server e bundler |
| [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react) | 6 | Supporto React e Fast Refresh (HMR) |
| [ESLint](https://eslint.org) | 10 | Analisi statica del codice |
| [typescript-eslint](https://typescript-eslint.io) | 8 | Regole ESLint per TypeScript |

## Requisiti

- **Node.js** `20.19+` oppure `22.13+` (o qualsiasi versione `>= 24`)
- **npm** (incluso in Node.js)

Verifica la versione installata con:

```bash
node -v
```

## Installazione

1. Clona il repository:

   ```bash
   git clone https://github.com/<tuo-utente>/ristorante.git
   cd ristorante
   ```

2. Installa le dipendenze:

   ```bash
   npm install
   ```

3. Avvia il server di sviluppo:

   ```bash
   npm run dev
   ```

4. Apri il browser su [http://localhost:5173](http://localhost:5173).

## Script disponibili

| Comando | Descrizione |
|---|---|
| `npm run dev` | Avvia il server di sviluppo con hot reload |
| `npm run build` | Esegue il type-check (`tsc -b`) e crea la build di produzione in `dist/` |
| `npm run preview` | Serve in locale la build di produzione per verificarla |
| `npm run lint` | Analizza il codice con ESLint |

## Struttura del progetto

```
ristorante/
├── public/               # File statici serviti così come sono (es. favicon.svg)
├── src/
│   ├── main.tsx          # Punto di ingresso dell'applicazione
│   └── ...               # Componenti, stili e risorse
├── index.html            # Template HTML principale
├── vite.config.ts        # Configurazione di Vite
├── eslint.config.js      # Configurazione di ESLint (flat config)
├── tsconfig.json         # Configurazione TypeScript (riferimenti)
├── tsconfig.app.json     # Opzioni TypeScript per il codice in src/
├── tsconfig.node.json    # Opzioni TypeScript per i file di configurazione
└── package.json
```

## Qualità del codice

Il progetto usa ESLint con le seguenti configurazioni:

- `@eslint/js` – regole JavaScript consigliate
- `typescript-eslint` – regole consigliate per TypeScript
- `eslint-plugin-react-hooks` – rispetto delle regole degli Hook di React
- `eslint-plugin-react-refresh` – compatibilità dei componenti con il Fast Refresh di Vite

TypeScript è configurato in modalità rigorosa sugli elementi inutilizzati (`noUnusedLocals`, `noUnusedParameters`) e con `erasableSyntaxOnly` e `verbatimModuleSyntax` attivi.

Prima di aprire una pull request esegui:

```bash
npm run lint
npm run build
```

## Deploy

La build di produzione genera file statici nella cartella `dist/`, pubblicabili su qualsiasi hosting statico (GitHub Pages, Netlify, Vercel, Cloudflare Pages…).

```bash
npm run build
```

> **GitHub Pages:** se il sito viene servito da un sotto-percorso (es. `https://<utente>.github.io/ristorante/`), aggiungi `base: '/ristorante/'` in `vite.config.ts`.

## Contribuire

1. Fai un fork del progetto
2. Crea un branch per la tua modifica: `git checkout -b feature/nuova-funzionalita`
3. Esegui il commit: `git commit -m "Aggiunge nuova funzionalità"`
4. Fai il push del branch: `git push origin feature/nuova-funzionalita`
5. Apri una pull request

## Licenza

<!-- Scegli una licenza (es. MIT) e aggiungi il file LICENSE al repository. -->
Distribuito con licenza **MIT**. Vedi il file [`LICENSE`](./LICENSE) per i dettagli.
