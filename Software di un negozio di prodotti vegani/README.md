# Software gestionale per BioMarket

BioMarket, una catena di negozi specializzata in prodotti vegani, ha aperto un nuovo negozio in Via Tan 6 e ha necessità di un **software gestionale** semplice e funzionale per la gestione dell’inventario e delle vendite. Il software dovrà essere **testuale**, accessibile da **riga di comando**, e garantire la **persistenza dei dati** attraverso file di testo per permettere di conservare le informazioni.

## Obiettivi del Software

Il software gestionale dovrà fornire le seguenti funzionalità:

1. **Registrazione di nuovi prodotti**: Inserire prodotti con nome, quantità, prezzo di acquisto e prezzo di vendita.
2. **Elenco dei prodotti disponibili**: Visualizzare tutti i prodotti presenti in magazzino con quantità e prezzo.
3. **Registrazione delle vendite**: Tenere traccia delle vendite, diminuendo la quantità dei prodotti venduti dall'inventario.
4. **Calcolo dei profitti**: Mostrare il profitto lordo (totale delle vendite) e il profitto netto (profitto lordo meno il costo di acquisto dei prodotti venduti).
5. **Menu di aiuto**: Mostrare un menu di aiuto con tutti i comandi disponibili.
6. **Persistenza dei dati**: Salvare tutte le informazioni relative ai prodotti e alle vendite in un file di testo, garantendo la persistenza tra le esecuzioni del programma.

## Valore Aggiunto

Il software gestionale proposto offre numerosi vantaggi operativi:

- **Automatizzazione della gestione dell’inventario**: BioMarket potrà facilmente gestire le scorte di magazzino, registrare nuovi prodotti e tenere traccia delle quantità disponibili, senza dover ricorrere a processi manuali.
- **Monitoraggio delle vendite**: La registrazione delle vendite permette una visione precisa delle quantità vendute per ciascun prodotto e offre una panoramica dettagliata delle vendite giornaliere.
- **Gestione finanziaria semplificata**: La funzionalità di calcolo dei profitti consente al negozio di monitorare in tempo reale la redditività delle vendite, differenziando tra il profitto lordo e quello netto.
- **Semplicità d'uso**: L'interfaccia testuale e la navigazione a comandi rendono il software semplice da utilizzare anche per personale con competenze informatiche limitate.

## Fasi del Progetto

### 1. Registrazione dei prodotti
L'utente può inserire nuovi prodotti specificando il **nome**, la **quantità**, il **prezzo di acquisto** e il **prezzo di vendita**. Se un prodotto esiste già nel magazzino, il sistema aggiorna solo la quantità disponibile.

### 2. Elenco dei prodotti
Questa funzione visualizza una lista di tutti i prodotti attualmente presenti nel magazzino con il rispettivo prezzo e quantità.

### 3. Registrazione delle vendite
L'utente può registrare una vendita specificando il **nome del prodotto** e la **quantità venduta**. Il sistema verifica che il prodotto sia disponibile nel magazzino e sottrae la quantità corrispondente.

### 4. Calcolo dei profitti
Il sistema calcola il **profitto lordo**, che rappresenta il totale delle vendite, e il **profitto netto**, che sottrae il costo di acquisto dei prodotti venduti dal profitto lordo.

### 5. Menu di aiuto
Un semplice menu testuale che elenca tutti i comandi disponibili, inclusi l’aggiunta di prodotti, la registrazione delle vendite, il calcolo dei profitti e l'elenco dei prodotti.

### 6. Persistenza dei dati
Il sistema salva tutti i dati relativi ai prodotti e alle vendite in file di testo, garantendo che le informazioni rimangano disponibili anche dopo la chiusura del programma.

## Esempio di Interazione

Di seguito un esempio di interazione tra l'utente e il software gestionale:

**Utente:** Inserisci un comando: `aggiungi`  
**Sistema:** Nome del prodotto: `latte di soia`  
**Sistema:** Quantità: `20`  
**Sistema:** Prezzo di acquisto: `0.80`  
**Sistema:** Prezzo di vendita: `1.40`  
**Sistema:** AGGIUNTO: 20 X latte di soia

**Utente:** Inserisci un comando: `elenca`  
**Sistema:**  
PRODOTTO | QUANTITA' | PREZZO  
latte di soia | 20 | €1.40

**Utente:** Inserisci un comando: `vendita`  
**Sistema:** Nome del prodotto: `latte di soia`  
**Sistema:** Quantità: `5`  
**Sistema:** Aggiungere un altro prodotto? (si/no): `no`  
**Sistema:** VENDITA REGISTRATA: 5 X latte di soia: €1.40

**Utente:** Inserisci un comando: `profitti`  
**Sistema:** Profitto: lordo=€7.00 netto=€3.00

## Conclusione

Il software gestionale sviluppato per BioMarket permetterà di ottimizzare le operazioni quotidiane del negozio, rendendo la gestione del magazzino e delle vendite più efficiente e trasparente. Con la possibilità di tracciare i profitti in tempo reale e tenere sotto controllo l'inventario, BioMarket potrà focalizzarsi sull'espansione del business e sulla crescita sostenibile.

