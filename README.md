# Baccalà

## Indice

- [Obbiettivo](#obbiettivo)
- [Requisiti funzionali](#requisiti-funzionali)
- [Requisiti non funzionali](#requisiti-non-funzionali)

### Obbiettivo

Il progetto è orientato al mondo della ristorazione e ha come obbiettivo la creazione di un servizio che permetta la consultazione e la gestione di un menù digitale.

Il gestore avrà le seguenti possibilità:

- accedere al servizio di gestione tramite un pannello web protetto da credenziali;
- aggiungere, rimuovere e modificare elementi dal menù;
- personalizzare il menù per rispecchiare l'identità del locale;
- generare un codice QR da fornire ai clienti per visualizzare il menù.

Il cliente avrà le seguenti possibilità:

- accedere liberamente al menù da una pagina web adatta a dispositivi mobili.

### Requisiti funzionali

Utente non autenticato (gestore):

- rf-1 registrazione:
  - l'utente può registrarsi al servizio tramite un form online dove inserisce indirizzo email e password.
- rf-1 login:
  - l'utente può accedere al servizio tramite una pagina di login dove inserisce indirizzo email e password;
  - l'utente può abilitare l'autenticazione a due fattori tramite email.
- rf-1 reset password:
  - nella pagina di login l'utente può chiedere di cambiare la password in caso di necessità tramite un pulsante dedicato; succesivamente deve inserire l'indirizzo email associato all'account di cui vuole cambiare password e attendere un'email contenente un link temporaneo che rimanda ad una pagina dedicata alla scelta di una nuova password.

Utente autenticato (gestore):

- rf-1 gestione menù:
  - l'utente può creare ed eliminare molteplici menù;
  - l'utente può creare categorie all'interno del menù;
  - l'utente può aggiungere, rimuovere e modificare elementi del menù;
  - gli elementi sono composti da un nome, una descrizione, la lista degli ingredienti e opzionalmente un'immagine;
  - l'utente può personalizzare il menù utilizzando layout e temi già pronti, e può inoltre modificare i parametri del tema scelto.
- rf-1 anteprima:
  - l'utente può, attraverso la pagina di modifice del menù, ottenere un'anteprima di cosa vedranno i consumatori.
- rf-1 abbonamento:
  - l' utente può pagare per abbonarsi al servizio tramite Stripe, sbloccando la funzione di [generazione del codice QR](#generazione-qr).
- <a name="generazione-qr"></a>rf-1 generazione del codice QR:
  - l'utente può generare codici QR che permettono l'accesso al menù corrispondente;
  - il codice QR può condurre a diversi menù o sezioni del menù secondo le necessità del gestore, per esempio mostrando agli utenti menù differenti in base a data e ora.

Utente non autenticato (consumatore):

- rf-1 consultazione menù:
  - l'utente può consultare il menù inquadrando il codice QR.

### Requisiti non funzionali

- rnf-1 compatibilità browser:
  - l'utente deve poter visualizzare correttamente il servizio dalle versioni più aggiornate dei browser Firefox, Safari e Chrome.
- rnf-1 usabilità:
  - l'utente trova intuitiva la navigazione dei menù e delle sue categorie: deve essere in grado di comprendere come esplorare il menù entro 10 secondi.
- rnf-1 leggibilità:
  - la grandezza di testo, immagini e widget deve essere proporzionata alla grandezza dello schermo del dispositivo utilizzato; Scopo: l'utente non trova difficoltà ad utilizzare il servizio indipendentemente dal dispositivo.
- rnf-1 sicurezza password:
  - la password deve essere lunga almeno 8 caratteri, contenere almeno un numero e una lettera maiuscola.

---

Revisione: 0.2
