# Sistema di monitoraggio ordini e magazzino in Python

## Descrizione del progetto

L'azienda **LogiServe S.r.l.** è una piccola realtà di e-commerce B2B specializzata nella distribuzione di componenti elettrici per officine e rivenditori. Il progetto mira a sviluppare un applicativo a riga di comando o con interfaccia testuale per la gestione del magazzino e degli ordini. L'obiettivo è simulare una soluzione gestionale reale che consenta di registrare nuovi ordini, aggiornare le giacenze dei prodotti, consultare lo stato del magazzino in tempo reale e generare report giornalieri utili per le decisioni operative.

Il progetto pone particolare attenzione a chiarezza, modularità e manutenibilità del codice, e sarà consegnato come notebook Google Colab contenente la descrizione del progetto, i dati di esempio, e le istruzioni per l'uso.

LogiServe riceve quotidianamente ordini da clienti ricorrenti e nuovi rivenditori. Per evitare rotture di stock, gestire le priorità di evasione e fornire report giornalieri al responsabile di magazzino, l'azienda necessita di uno strumento semplice ma affidabile che:

- registri gli ordini in arrivo;
- aggiorni automaticamente le giacenze dopo l'evasione;
- permetta di verificare disponibilità e soglie di riordino;
- produca report giornalieri con sintetiche informazioni su vendite, giacenze e ordini in sospeso.

L'importanza del progetto per LogiServe è elevata: riduce il rischio di out-of-stock, migliora i tempi di evasione ordini e offre dati aggregati utili per decisioni sul riassortimento e sul servizio al cliente.

## Obiettivi del progetto

Il progetto dovrà fornire, a livello di requisiti funzionali e non funzionali, le seguenti caratteristiche principali:

Funzionalità principali (requisiti funzionali)
1. Registrazione di nuovi ordini
   - Inserimento di ordini contenenti: identificativo cliente, lista di prodotti (codice, quantità richiesta), data e priorità.
   - Verifica dello stato di disponibilità al momento della registrazione (disponibile/parziale/indisponibile).

2. Aggiornamento delle giacenze
   - Riduzione delle giacenze al momento di evasione ordine.
   - Gestione di scorte negative o ordini parziali come stato separato (es. “parziale”, “in attesa”).

3. Consultazione dello stato del magazzino in tempo reale
   - Visualizzazione elenco prodotti con giacenza attuale, punto di riordino e unità di misura.
   - Filtri di ricerca per codice prodotto, categoria o soglia di giacenza.

4. Generazione di report giornalieri
   - Report sintetico giornaliero contenente: numero ordini ricevuti, ordini evasi, ordini in sospeso, prodotti più venduti, variazione giacenze.
   - Esportazione del report in formato leggibile (ad es. file di testo o CSV) per condivisione interna.

5. Persistenza dei dati (requisiti di alto livello)
   - Possibilità di caricare e salvare lo stato di magazzino e la lista ordini su file di dati (formato standard come CSV/JSON), in modo che il sistema possa essere riavviato mantenendo lo stato.

6. Tracciabilità e log
   - Tracciamento delle operazioni principali (es. registrazione ordine, evasione, modifica giacenze) con timestamp e operatore.

## Requisiti non funzionali

- Chiarezza e documentazione: codice con spiegazioni chiare delle funzioni, dell’architettura logica e delle istruzioni per l’uso.
- Modularità: componenti separate per gestione ordini, magazzino, reportistica e persistenza dati.
- Manutenibilità: codice leggibile con nomi significativi e commenti che facilitino estensioni future.
- Usabilità: interfaccia testuale intuitiva con menu e messaggi di feedback chiari.
- Robustezza: comportamento prevedibile in presenza di input incompleti o non validi (gestione di errori a livello di flusso).

## Dati e formato dei file 

Dati di esempio da includere nel notebook:

- Catalogo prodotti: file con colonne come CodiceProdotto, Nome, Categoria, GiacenzaIniziale, PuntoRiordino, UnitàMisura.
- Lista ordini: file con colonne come IDOrdine, Data, Cliente, Stato (nuovo/evaso/parziale), ElencoProdotti (codice+quantità).
- Storico operazioni: file log delle operazioni (timestamp, operazione, risorsa, dettaglio).

I file dovrebbero essere in formati standard (ad es. CSV o JSON) per permettere il caricamento e il salvataggio dello stato. Alla prima esecuzione del programma, se i file non esistono già, il programma deve crearli con dati iniziali simulati per gli scopi di questo esercizio.


## Casi di test e scenari di valutazione

Esempi di scenari utili per valutare il progetto:

- Scenari di ordine evaso completamente: verifica giacenze aggiornate correttamente.
- Ordine parziale: verifica dello stato dell’ordine e della giacenza residua.
- Scarico consistente: verifica del comportamento al raggiungimento del punto di riordino o giacenza zero.
- Import/export dei dati: caricamento dello stato iniziale e salvataggio dello stato finale.

## Valore aggiunto per l'azienda

- Riduzione del rischio di rottura di stock grazie a una visibilità immediata delle giacenze e alle notifiche dei punti di riordino.
- Migliore capacità di pianificazione degli approvvigionamenti: report giornalieri sintetici per il responsabile acquisti.
- Migliore servizio clienti: informazioni tempestive sulla disponibilità dei prodotti e sui tempi di evasione.
- Base riutilizzabile e manutenibile per futuri sviluppi (integrazione con sistemi esterni, interfacce grafiche, moduli di analisi storica).

