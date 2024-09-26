# Analisi dei Piloti del Mondiale di Formula 1

## Descrizione del progetto

L'azienda **F1 Analytics** è specializzata nell'analisi delle prestazioni dei piloti e dei team nel mondo della Formula 1. L'obiettivo di questo progetto è analizzare i risultati del Campionato Mondiale di Formula 1 della stagione 2008, utilizzando i dati contenuti nel file `formula1_data.csv`. 

Questo file contiene informazioni dettagliate sui piloti, i costruttori, le città e i paesi dei Gran Premi, nonché l'ordine di arrivo di ogni pilota. Basandosi su questi dati, verranno implementate diverse funzioni per fornire un'analisi approfondita dei punti, delle vittorie e dei podi sia a livello individuale che di costruttori.


## Dataset

Il dataset `formula1_data.csv` (scaricabile da qui: https://proai-datasets.s3.eu-west-3.amazonaws.com/formula1_data.csv) contiene le seguenti colonne:
1. **Driver**: Nome del pilota.
2. **Team**: Nome del costruttore per il quale il pilota gareggia.
3. **Race**: Città in cui si è svolto il Gran Premio.
4. **Country**: Paese in cui si è svolto il Gran Premio.
5. **Position**: Numero compreso tra 0 e 8 che indica l'ordine di arrivo del pilota (0 significa che il pilota non è arrivato tra i primi 8 e non ha ottenuto punti).

## Sistema di punteggio
Al termine di ogni Gran Premio, i punti vengono assegnati ai piloti in base al loro ordine di arrivo come segue:
- 1° posto: **10 punti**
- 2° posto: **8 punti**
- 3° posto: **6 punti**
- 4° posto: **5 punti**
- 5° posto: **4 punti**
- 6° posto: **3 punti**
- 7° posto: **2 punti**
- 8° posto: **1 punto**
- 9° posto o oltre: **0 punti**

# Modalità di consegna: link al notebook di Google Colab

## Obiettivi del progetto

Il progetto prevede l'implementazione delle seguenti funzionalità:

### 1. Funzione per l'analisi delle performance individuali dei piloti
La prima funzione riceve in input il nome di un pilota e restituisce una lista contenente tre informazioni chiave:
- Il **totale dei punti** accumulati dal pilota durante il campionato.
- Il **numero di vittorie**, ovvero quante volte il pilota è arrivato primo in un Gran Premio.
- Il **numero di podi**, ovvero quante volte il pilota è arrivato tra i primi tre classificati.

Questa funzione sarà utile per analizzare le performance individuali dei piloti e avere una chiara visione delle loro posizioni nel corso della stagione.

### 2. Funzione per la creazione della classifica finale dei piloti
La seconda funzione genera un dizionario contenente i nomi dei piloti come chiavi e il loro **punteggio totale** come valori. Il dizionario viene poi utilizzato per creare una classifica generale dei piloti.

Infine, la classifica sarà salvata in un file di testo (`Drivers_Standings_2008.txt`) con il seguente formato:

```
Drivers Standings 2008 Formula 1
NomePilota1: PunteggioTotale
NomePilota2: PunteggioTotale
```

### 3. Funzione per la classifica dei costruttori
La terza funzione crea un dizionario con i nomi dei **team/costruttori** come chiavi e il loro **punteggio totale** come valori. Il punteggio di ciascun team è la somma dei punti ottenuti dai piloti che hanno gareggiato per quel costruttore.

Questa funzione utilizza i dati precedentemente generati per i piloti e calcola la classifica dei costruttori. Anche questa informazione è essenziale per avere una visione chiara delle prestazioni dei team durante l'anno.

