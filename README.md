# Baccalà <!-- omit in toc -->

## Indice <!-- omit in toc -->

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
  - rf-1.1 l'utente può registrarsi al servizio tramite un form online dove inserisce indirizzo email e password.
- rf-2 login:
  - rf-2.1 l'utente può accedere al servizio tramite una pagina di login dove inserisce indirizzo email e password;
  - rf-2.2 l'utente può abilitare l'autenticazione a due fattori tramite email.
- rf-3 reset password:
  - rf-3.1 nella pagina di login l'utente può chiedere di cambiare la password in caso di necessità tramite un pulsante dedicato; successivamente deve inserire l'indirizzo email associato all'account di cui vuole cambiare password e attendere un'email contenente un link temporaneo che rimanda ad una pagina dedicata alla scelta di una nuova password.

Utente autenticato (gestore):

- rf-4 gestione menù:
  - rf-4.1 l'utente può creare ed eliminare molteplici menù;
  - rf-4.2 l'utente può creare categorie all'interno del menù;
  - rf-4.3 l'utente può aggiungere, rimuovere e modificare elementi del menù;
  - rf-4.4 gli elementi sono composti da un nome, una descrizione, la lista degli ingredienti e opzionalmente un'immagine;
  - rf-4.5 l'utente può personalizzare il menù utilizzando layout e temi già pronti, e può inoltre modificare i parametri del tema scelto.
- rf-5 anteprima:
  - rf-5.1 l'utente può, attraverso la pagina di modifica del menù, ottenere un'anteprima di cosa vedranno i consumatori.
- rf-6 abbonamento:
  - rf-6.1 l'utente può pagare per abbonarsi al servizio tramite Stripe, sbloccando la funzione di [generazione del codice QR](#generazione-qr).
- <a name="generazione-qr"></a>rf-7 generazione del codice QR:
  - rf-7.1 l'utente può generare codici QR che permettono l'accesso al menù corrispondente;
  - rf-7.2 il codice QR può condurre a diversi menù o sezioni del menù secondo le necessità del gestore, per esempio mostrando agli utenti menù differenti in base a data e ora.

Utente non autenticato (consumatore):

- rf-8 consultazione menù:
  - rf-8.1 l'utente può consultare il menù inquadrando il codice QR.

### Requisiti non funzionali

- rnf-1 compatibilità browser:
  - rnf-1.1 l'utente deve poter visualizzare correttamente il servizio dalle versioni più aggiornate dei browser Firefox, Safari e Chrome.
- rnf-2 usabilità:
  - rnf-2.1l'utente trova intuitiva la navigazione dei menù e delle sue categorie: deve essere in grado di comprendere come esplorare il menù entro 10 secondi.
- rnf-3 leggibilità:
  - rnf-3.1 la grandezza di testo, immagini e widget deve essere proporzionata alla grandezza dello schermo del dispositivo utilizzato; Scopo: l'utente non trova difficoltà ad utilizzare il servizio indipendentemente dal dispositivo.
- rnf-4 sicurezza password:
  - rnf-4.1 la password deve essere lunga almeno 8 caratteri, contenere almeno un numero e una lettera maiuscola.

---

Revisione: 0.2
