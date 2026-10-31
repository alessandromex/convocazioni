# Convocazioni Under 17 – A.S.D. Pontelungo 1949

App per preparare la convocazione della gara con lo stesso layout del modulo della società:
si spuntano i convocati dalla rosa, si controllano i dati gara (già proposti) e si crea il PDF.

## Come usarla

| Dispositivo | Come si apre |
|---|---|
| **iPhone** | Apri con Safari il link di GitHub Pages → *Condividi* → *Aggiungi alla schermata Home* |
| **Android (app)** | Scarica `convocazioni.apk` dalla pagina **Releases** e aprilo per installarlo |
| **Android (senza APK)** | Apri il link con Chrome → menu ⋮ → *Installa app* |
| **PC** | Apri il link con qualunque browser |

La rosa resta salvata sul dispositivo. Con **Salva rosa.json** / **Apri rosa.json** la sposti da un dispositivo all'altro.

## Struttura

- `docs/` – l'app (pubblicata su GitHub Pages e inserita anche nell'APK)
  - `index.html` – tutta l'app in un file
  - `jspdf.umd.min.js` – libreria per creare il PDF (inclusa, così funziona anche offline)
  - `manifest.webmanifest`, `sw.js`, icone – per installarla come app e usarla senza rete
- `assets/` – icona e schermata di avvio dell'app Android
- `package.json`, `capacitor.config.json` – configurazione dell'app Android (Capacitor)
- `release.keystore` – chiave con cui viene firmato l'APK (serve per installare gli aggiornamenti sopra la versione precedente)
- `.github/workflows/android.yml` – a ogni modifica GitHub compila l'APK e lo pubblica in **Releases**

## Aggiornare l'app

Modifica `docs/index.html` e fai commit su `main`: GitHub Pages si aggiorna da solo e in pochi minuti
compare un nuovo `convocazioni.apk` in Releases. Sull'Android basta installarlo sopra quello vecchio: la rosa resta.
