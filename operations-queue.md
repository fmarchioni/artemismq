# **Apache ActiveMQ Artemis - Cheatsheet Gestione Code**

## **Navigazione Messaggi**
- `browse()` – Visualizza i messaggi nella coda.
- `browse(String)` – Visualizza i messaggi filtrati.
- `browse(int, int)` – Visualizza i messaggi con paginazione.
- `browse(int, int, String)` – Visualizza i messaggi con paginazione e filtro.

## **Gestione Priorità**
- `changeMessagePriority(long, int)` – Modifica la priorità di un messaggio specifico.
- `changeMessagesPriority(String, int)` – Modifica la priorità dei messaggi filtrati.

## **Conteggio Messaggi**
- `countDeliveringMessages(String)` – Conta i messaggi in consegna.
- `countDeliveringMessages(String, String)` – Conta i messaggi in consegna raggruppati per un campo.
- `countMessages()` – Conta i messaggi nella coda.
- `countMessages(String)` – Conta i messaggi filtrati.
- `countMessages(String, String)` – Conta i messaggi filtrati raggruppati per un campo.

## **Consegna Messaggi Programmati**
- `deliverScheduledMessage(long)` – Consegna immediatamente un messaggio programmato.
- `deliverScheduledMessages(String)` – Consegna immediatamente tutti i messaggi programmati che corrispondono al filtro.

## **Abilitazione e Disabilitazione**
- `disable()` – Disabilita l'instradamento dei messaggi alla coda.
- `enable()` – Abilita l'instradamento dei messaggi alla coda.

## **Scadenza Messaggi**
- `expireMessage(long)` – Rimuove un messaggio specifico scaduto.
- `expireMessages(String)` – Rimuove i messaggi filtrati e restituisce il numero di messaggi scaduti.

## **Gestione Esecutori**
- `flushExecutor()` – Svuota gli esecutori interni.

## **Elenco Consumatori e Messaggi**
- `listConsumersAsJSON()` – Elenca tutti i consumer attivi in formato JSON.
- `listDeliveringMessages()` – Elenca tutti i messaggi in consegna.
- `listDeliveringMessagesAsJSON()` – Elenca tutti i messaggi in consegna in formato JSON.
- `listGroupsAsJSON()` – Elenca i gruppi di consumer attivi.
- `listMessageCounter()` – Elenca i contatori dei messaggi.
- `listMessageCounterAsHTML()` – Elenca i contatori dei messaggi in formato HTML.
- `listMessageCounterHistory()` – Mostra la cronologia dei contatori.
- `listMessageCounterHistoryAsHTML()` – Mostra la cronologia dei contatori in formato HTML.
- `listMessages(String)` – Elenca i messaggi filtrati.
- `listMessagesAsJSON(String)` – Elenca i messaggi filtrati in formato JSON.
- `listScheduledMessages()` – Elenca i messaggi programmati.
- `listScheduledMessagesAsJSON()` – Elenca i messaggi programmati in formato JSON.

## **Movimentazione Messaggi**
- `moveMessage(long, String)` – Sposta un messaggio in un'altra coda.
- `moveMessage(long, String, boolean)` – Sposta un messaggio in un'altra coda con gestione dei duplicati.
- `moveMessages(String, String)` – Sposta tutti i messaggi filtrati in un'altra coda.
- `moveMessages(String, String, boolean)` – Sposta tutti i messaggi filtrati con gestione dei duplicati.
- `moveMessages(int, String, String, boolean)` – Sposta un numero specifico di messaggi filtrati.
- `moveMessages(int, String, String, boolean, int)` – Sposta un numero specifico di messaggi con gestione avanzata.

## **Gestione Stato della Coda**
- `pause()` – Mette in pausa la coda.
- `pause(boolean)` – Mette in pausa la coda con opzioni.
- `resume()` – Riprende l'elaborazione dei messaggi in coda.

## **Visualizzazione Messaggi**
- `peekFirstMessageAsJSON()` – Mostra il primo messaggio nella coda in formato JSON.
- `peekFirstScheduledMessageAsJSON()` – Mostra il primo messaggio programmato in formato JSON.

## **Rimozione Messaggi**
- `removeAllMessages()` – Rimuove tutti i messaggi dalla coda.
- `removeMessage(long)` – Rimuove un messaggio specifico.
- `removeMessages(String)` – Rimuove i messaggi filtrati.
- `removeMessages(int, String)` – Rimuove un numero specifico di messaggi filtrati.

## **Gestione Gruppi**
- `resetAllGroups()` – Resetta tutti i gruppi.
- `resetGroup(String)` – Resetta un gruppo specifico.

## **Reset Contatori**
- `resetMessageCounter()` – Resetta il contatore dei messaggi.
- `resetMessagesAcknowledged()` – Resetta il contatore dei messaggi riconosciuti.
- `resetMessagesAdded()` – Resetta il contatore dei messaggi aggiunti.
- `resetMessagesExpired()` – Resetta il contatore dei messaggi scaduti.
- `resetMessagesKilled()` – Resetta il contatore dei messaggi eliminati.

## **Retry Messaggi**
- `retryMessage(long)` – Ritenta l'invio di un messaggio nella coda originale.
- `retryMessages()` – Ritenta l'invio di tutti i messaggi in DLQ alle code originali.

## **Invio Messaggi**
- `sendMessage(Map, int, String, boolean, String, String)` – Invia un messaggio testuale a una destinazione protetta.
- `sendMessage(Map, int, String, boolean, String, String, boolean)` – Invia un messaggio testuale con opzioni avanzate.

## **Gestione Dead Letter Address (DLA)**
- `sendMessageToDeadLetterAddress(long)` – Sposta un messaggio alla Dead Letter Address.
- `sendMessagesToDeadLetterAddress(String)` – Sposta i messaggi filtrati alla Dead Letter Address.

