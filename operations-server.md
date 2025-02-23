# Cheatsheet Operazioni Server AMQ

## Gestione Indirizzi  
### `addAddressSettings(String, String)`  
Aggiunge impostazioni per indirizzi che corrispondono al pattern specificato.  

### `createAddress(String, String)`  
Crea un nuovo indirizzo con il routing-type specificato.  

### `deleteAddress(String)`  
Elimina un indirizzo.  

---

## Gestione Code  
### `createQueue(String, String)`  
Crea una coda con un indirizzo specificato.  

### `destroyQueue(String)`  
Distrugge una coda.  

### `updateQueue(String, String, Integer, Boolean)`  
Aggiorna una coda con nuovi parametri.  

---

## Sicurezza  
### `addUser(String, String, String, boolean)`  
Aggiunge un utente.  

### `removeUser(String)`  
Rimuove un utente.  

### `addSecuritySettings(String, String, String, String, String, String, String, String)`  
Aggiunge impostazioni di sicurezza per gli indirizzi.  

---

## Connessioni  
### `closeConnectionWithID(String)`  
Chiude una connessione specifica.  

### `listConnectionsAsJSON()`  
Elenca tutte le connessioni in formato JSON.  

---

## Operazioni Avanzate  
### `forceFailover()`  
Forza l'arresto del server e il failover.  

### `reloadConfigurationFile()`  
Forza il broker a ricaricare il file di configurazione.  

### `rollbackPreparedTransaction(String)`  
Esegue il rollback di una transazione preparata.  

---

## Strumenti di Debug  
### `listAddresses(String)`  
Elenca tutti gli indirizzi nel broker.  

### `listQueues(String, int, int)`  
Cerca code esistenti.  

### `listConsumersAsJSON(String)`  
Elenca tutti i consumer associati a una connessione in JSON.  

---

## Server Web Integrato  
### `startEmbeddedWebServer()`  
Avvia il server web incorporato.  

### `stopEmbeddedWebServer()`  
Ferma il server web incorporato.  

### `restartEmbeddedWebServer(long)`  
Riavvia il server web incorporato con un tempo di attesa specificato.  

