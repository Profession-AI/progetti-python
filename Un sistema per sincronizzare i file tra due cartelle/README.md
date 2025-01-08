# Un Sistema per Sincronizzare i File tra Due Cartelle

## Caso d'Uso Aziendale: SyncEase

### Introduzione all'Azienda
SyncEase è una società tecnologica che sviluppa soluzioni software per migliorare la gestione e la condivisione dei dati aziendali. Una delle loro sfide principali è quella di garantire che i file critici siano sempre sincronizzati tra dispositivi e server, per evitare perdite di dati o versioni obsolete.

### Problema
Molte aziende si affidano a sistemi manuali o software non ottimizzati per mantenere sincronizzati i file tra due cartelle, ad esempio tra un server locale e uno di backup. Questo approccio è soggetto a errori, come la perdita di file aggiornati o la duplicazione di dati. Inoltre, il processo può essere lento, specialmente quando il volume di dati è elevato.

### Obiettivo del Progetto
L'obiettivo è sviluppare un sistema software che utilizzi il multiprocessing e il multithreading in Python per sincronizzare in modo efficiente i file tra due cartelle. Questo sistema dovrà:

1. Copiare i file nuovi o modificati dalla cartella sorgente a quella di destinazione.
2. Eliminare i file obsoleti nella cartella di destinazione se non esistono più nella sorgente.
3. Gestire grandi volumi di file in modo rapido ed efficiente, sfruttando al meglio le risorse hardware.

### Benefici Attesi
- **Riduzione degli errori:** Sincronizzazione affidabile e automatica senza intervento manuale.
- **Ottimizzazione delle prestazioni:** Utilizzo efficiente di CPU e I/O grazie al multiprocessing e al multithreading.
- **Miglioramento della sicurezza:** Backup sempre aggiornati e consistenti tra le due cartelle.

### Specifiche del Progetto
1. **Input:**
   - Due percorsi di cartelle: `source_folder` e `destination_folder`.
2. **Output:**
   - La cartella di destinazione è sincronizzata con quella sorgente.
3. **Funzionalità Chiave:**
   - Utilizzo di **multithreading** per accelerare la lettura e la scrittura dei file.
   - Utilizzo di **multiprocessing** per gestire in parallelo sottogruppi di file.
   - Verifica di:
     - File nuovi: Copia solo i file che non esistono nella cartella di destinazione.
     - File modificati: Aggiorna i file nella destinazione se quelli nella sorgente sono più recenti.
     - File obsoleti: Rimuove i file nella destinazione che non esistono più nella sorgente.

### Consegna
Scrivi un programma Python che implementi il sistema di sincronizzazione dei file. Il tuo codice deve essere ben documentato, con commenti che spieghino chiaramente le scelte implementative e il flusso del programma. Testa  il suo funzionamento con almeno 3 casi reali. Per esempio:
   - Una cartella con pochi file.
   - Una cartella con molti file.
   - Una cartella che include sottocartelle.


