# CIGO PDF Studio — prototipo 0.1

Apri `index.html` tramite un server locale (per esempio `python -m http.server 8000`) e visita `http://localhost:8000`. È possibile pubblicare i file statici su GitHub Pages. Richiede internet per caricare le librerie PDF da jsDelivr.

## Funzioni disponibili
- Apertura e visualizzazione di PDF, anteprime, zoom
- Rotazione, eliminazione e riordino pagine
- Inserimento testo, rettangoli ed evidenziature sul PDF esportato
- Unione PDF (prima esportare eventuali annotazioni non salvate)
- Esportazione locale del PDF e annullamento delle modifiche non esportate

## Limiti noti
- Non modifica il testo già presente nel PDF.
- Le annotazioni sono applicate soltanto durante l'esportazione, non sono visibili nell'anteprima.
- Il posizionamento delle annotazioni su pagine ruotate può essere impreciso.
- Font di esportazione standard: caratteri Unicode non latini non supportati.
- Non gestisce PDF protetti da password, OCR o conversione Word.
- L'anteprima di documenti molto grandi può essere lenta.
- L'unione ricostruisce il documento e perde le annotazioni non esportate.
- Versione Windows non ancora pacchettizzata: per Tauri servono toolchain Rust/Node e configurazione specifica.

## Privacy
Il file PDF viene elaborato localmente nel browser. Le librerie JS vengono recuperate da CDN; per un funzionamento totalmente offline devono essere incluse nel pacchetto.
