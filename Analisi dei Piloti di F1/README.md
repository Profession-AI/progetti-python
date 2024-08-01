# Analisi dei Piloti del Mondiale di Formula 1

Il dataset formula1_data.csv contiene i risultati del mondiale di Formula 1 della Stagione 2008.

Esso contiene 180 righe e le seguenti 5 colonne:

1. Driver: Nome del Pilota
2. Team: Costruttore  per il quale il pilota gareggia
3. Race: Città dove si è svolto il Gran Premio
4. Country: Paese dove si è svolto il Gran Premio
5. Position: Numero compreso tra 0 e 8 che rappresentano l’ordine di arrivo del pilota nella singola gara (0 significa che il pilota non è arrivato tra i primi 8).

Al termine di un gran premio, vengono assegnati i punti ai piloti in base all’ordine di arrivo: 10 al vincitore, 8 al secondo, 6 al terzo, e poi a scalare di 1 punto fino all’ottavo.

Implementa un insieme di funzioni per analizzare i risultati del Campionato Mondiale di Formula 1 utilizzando i dati nel file csv a tua disposizione

In particolare dovrai implementare le seguenti funzioni:

1. Una funzione che riceve in input il nome di un pilota e restituisce una lista contenente il totale dei punti del pilota, il numero di vittorie (quante volte il pilota è arrivato primo) e il numero dei podi (quante volte il pilota è salito sul podio).
2. Una funzione che non riceve alcun parametro in ingresso e deve restituire un dizionario formato da coppie chiave valore, dove la chiave è una stringa che contiene il nome del pilota, mentre il valore associato alla chiave è un intero che rappresenta il totale dei punti che il pilota ha conseguito alla fine del campionato mondiale.

Salva poi la classifica in un file di testo di tipo txt con il seguente formato:

Drivers Standings 2008 Formula 1

NomePilota1: PunteggioTotale

NomePilota2: PunteggioTotale…


3. Una funzione che non riceve alcun parametro in ingresso e deve restituire un dizionario formato da coppie chiave valore, dove la chiave è una stringa che contiene il nome del costruttore, mentre il valore associato alla chiave è un intero che rappresenta il totale dei punti che il costruttore ha conseguito alla fine del campionato mondiale. I punti conseguiti da un costruttore sono la somma dei punti che i piloti che corrono per il costruttore hanno conseguito durante l’anno.Per fare ciò, utilizza i dati salvati sul file creato precedentemente
