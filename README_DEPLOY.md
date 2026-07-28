# KrioPlanet Timer — versione PWA offline

## Pubblicazione su GitHub Pages

1. Sostituisci il file HTML attuale con `index.html`.
2. Carica nella stessa directory:
   - `manifest.webmanifest`
   - `service-worker.js`
   - la cartella `icons/`
3. Mantieni nella stessa directory il tuo file esistente `Logo-Blu.svg`.
4. Pubblica le modifiche e apri una volta l’app con connessione internet.
5. Su iPhone rimuovi eventualmente la vecchia icona dalla Home e aggiungila di nuovo da Safari con **Condividi → Aggiungi alla schermata Home**.

## Offline

Dopo il primo caricamento online, HTML, manifest, icone e logo vengono memorizzati nella cache. Il timer, i preset e la libreria continuano a funzionare senza connessione. I workout personali restano nel `localStorage` del browser.

## Aggiornamenti inclusi

- Timer basato su scadenze assolute, senza accumulo dell’errore dei `setInterval`.
- Recupero automatico del ritardo quando Safari rallenta o sospende temporaneamente JavaScript.
- Durata totale corretta: nessun recupero e nessun extra dopo l’ultimo giro.
- Anello esterno coerente anche usando avanti/indietro.
- Wake Lock richiesto soltanto durante l’allenamento e rilasciato in pausa, stop, completamento o quando l’app passa in secondo piano.
- Nessuna dipendenza da Google Fonts: l’interfaccia usa i font di sistema ed è davvero disponibile offline.

## Nota Service Worker

Il Service Worker funziona su HTTPS o su localhost. GitHub Pages usa HTTPS, quindi non serve alcuna configurazione aggiuntiva.

## Icona KrioPlanet Timer

Questa versione include la nuova icona in tutti i formati necessari:

- `icons/apple-touch-icon.png` per iPhone/iPad;
- `icons/icon-192.png` e `icons/icon-512.png` per la PWA;
- versioni `maskable` per launcher Android;
- `icons/favicon-32.png` per la scheda del browser.

Carica l'intera cartella `icons` senza modificare i nomi. Se la web app era già
presente nella schermata Home di iPhone, eliminala e aggiungila nuovamente: iOS
può conservare in cache la vecchia icona.
