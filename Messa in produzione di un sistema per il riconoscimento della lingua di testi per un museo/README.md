# Messa in Produzione di un Sistema per il Riconoscimento della Lingua di Testi per un Museo

## Caso d'Uso Aziendale: MuseumLangAPI

### Introduzione all'Azienda
MuseumLangID, il sistema sviluppato per il riconoscimento automatico della lingua di testi museali, è pronto per essere messo in produzione. Ora l'obiettivo è fornire il modello tramite un'API REST per integrarlo facilmente nei sistemi gestionali del museo.

### Problema
Il museo richiede un accesso remoto e standardizzato alle funzionalità del modello di riconoscimento della lingua. Attualmente, il sistema è limitato all'utilizzo locale, ostacolando la collaborazione tra i vari reparti e l'integrazione con altri strumenti software.

### Obiettivo del Progetto
Implementare un'API REST utilizzando Flask o FastAPI per esporre le funzionalità del modello di riconoscimento della lingua. Questa API dovrà:

1. Ricevere testi in formato JSON.
2. Restituire il codice della lingua riconosciuta.
3. Essere scalabile e pronta per l'integrazione con sistemi esterni.

### Benefici Attesi
- **Accessibilità:** Consentire ai reparti del museo di accedere al servizio da remoto.
- **Integrazione:** Facilitare l'uso del sistema in applicazioni software esistenti.
- **Scalabilità:** Permettere un utilizzo parallelo da parte di più utenti.

### Specifiche del Progetto
#### **Tecnologie**
- Backend:
  - Python con Flask o FastAPI.
  - Modellazione basata sul progetto di riconoscimento della lingua sviluppato in precedenza.

#### **Funzionalità dell'API**
1. **Endpoint:**
   - `POST /identify-language`
     - Input: JSON contenente il testo da analizzare.
     - Output: JSON con il codice della lingua identificata e la probabilità associata.

   **Esempio di Input:**
   ```json
   {
       "text": "Questo è un esempio di testo."
   }
   ```

   **Esempio di Output:**
   ```json
   {
       "language_code": "IT",
       "confidence": 0.98
   }
   ```

2. **Logging:**
   - Registrare ogni richiesta e risposta in un file di log per motivi di audit.

3. **Errore:**
   - Restituire un messaggio d'errore se il testo è vuoto o se la lingua non può essere identificata.

Scrivi un codice ben commentato e chiaro, che riporti i vari dettagli in maniera leggibile anche da parte di chi non lo ha sviluppato.


