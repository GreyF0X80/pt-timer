# Timer — PWA offline v1.2.0

## Pubblicazione su GitHub Pages

1. Sostituisci il file HTML attuale con `index.html`.
2. Carica nella stessa directory `manifest.webmanifest`, `service-worker.js` e la cartella `icons/`.
3. Mantieni nella stessa directory il file esistente `Logo-Blu.svg`: viene mostrato esclusivamente con il tema **Krio**.
4. Pubblica le modifiche e apri una volta l’app con connessione internet.
5. Ricarica la pagina e poi riapri la web app dalla schermata Home.

## Identità dell’app

L’app installata si chiama **Timer** e usa sempre l’icona con gli anelli e il numero 30.

All’interno dell’interfaccia:

- con il tema **Krio** compaiono il logo e la scritta `KRIOPLANET`;
- con tutti gli altri temi compaiono l’icona della web app e la scritta `TIMER`.

Su iPhone il nome sotto l’icona può restare memorizzato. Per passare da “KrioPlanet” a “Timer”, elimina la vecchia icona dalla schermata Home e aggiungi nuovamente la pagina da Safari con **Condividi → Aggiungi alla schermata Home**.

## Temi

Sono disponibili sei temi:

- Krio;
- Ghiaccio;
- Pulse;
- Energia;
- Aurora;
- Neon.

Ogni tema modifica colori principali, superfici, bagliori, sfondo e colore delle barre di sistema. Lo sfondo usa più livelli luminosi statici per dare maggiore profondità senza introdurre un’animazione continua che consumerebbe più batteria.

## Informazioni

La sezione Informazioni mostra:

- App: `Timer`;
- Versione: `1.2.0`;
- Copyright: `© 2026 MC`.

## Offline

Dopo il primo caricamento online, HTML, manifest, icone e logo vengono salvati nella cache. Timer, preset e libreria continuano a funzionare senza connessione. I workout personali restano nel `localStorage` del browser.

## Nota Service Worker

Il Service Worker funziona su HTTPS o localhost. GitHub Pages usa HTTPS e non richiede configurazioni aggiuntive. La cache di questa release è `timer-v5-brand-themes-2026-07-29`.
