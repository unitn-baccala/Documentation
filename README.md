# Baccalà <!-- omit in toc -->

## Indice <!-- omit in toc -->

- [Obbiettivo](#obbiettivo)
- [Requisiti funzionali](#requisiti-funzionali)
- [Requisiti non funzionali](#requisiti-non-funzionali)

### Obbiettivo

Il progetto è orientato al mondo della ristorazione e ha come obbiettivo la creazione di un servizio che permetta la consultazione e la gestione di un menù dinamico digitale.

Il gestore avrà le seguenti possibilità:

- registrarsi e successivamente effettuare l'accesso al servizio di gestione menù tramite un pannello web;
- creare, modificare ed eliminare i propri menù;
- fornire la traduzione in più lingue dei propri menù;
- personalizzare i menù con diversi temi e layout;
- visualizzare l'anteprima dei menù;
- pagare un abbonamento per generare un codice QR da fornire ai clienti per visualizzare il menù;
- impostare il menù "attivo" rispetto alla data o all'ora mantenendo lo stesso codice QR.

Il cliente avrà le seguenti possibilità:

- accedere liberamente al menù digitale inquadrando il codice QR con il proprio dispositivo mobile;
- scegliere una delle traduzioni messe a disposizione dal gestore;
- navigare il menù attraverso le varie categorie di prodotti (primi, secondi, bevande).

### Requisiti funzionali

Utente non autenticato (gestore):

- rf-1 registrazione:
  - rf-1.1 l'utente può registrarsi al servizio tramite un form online dove inserisce indirizzo email e password ([v rnf-5](#sicurezza-password)).
- rf-2 login:
  - rf-2.1 l'utente può accedere al servizio tramite una pagina di login dove inserisce indirizzo email e password;

Utente autenticato (gestore):

- rf-3 reset password:
  - rf-3.1 nella pagina di login l'utente può chiedere di cambiare la password in caso di necessità tramite un pulsante dedicato; successivamente deve inserire l'indirizzo email associato all'account di cui vuole cambiare password e attendere un'email contenente un link temporaneo che rimanda ad una pagina dedicata alla scelta di una nuova password.
- rf-4 autenticazione a due fattori:
  - rf-4.1 l'utente può abilitare l'autenticazione a due fattori tramite email.
- rf-5 gestione menù:
  - rf-5.1 l'utente può creare ed eliminare molteplici menù;
  - rf-5.2 <a name="categorie"></a>l'utente può creare categorie all'interno del menù (ad esempio antipasti o bevande);
  - rf-5.3 l'utente può aggiungere, rimuovere e modificare elementi del menù;
  - rf-5.4 <a name="traduzione"></a>l'utente può fornire la traduzione del menù in diverse lingue;
  - rf-5.5 gli elementi sono composti da un nome, una descrizione, la lista degli ingredienti e opzionalmente un'immagine;
  - rf-5.6 l'utente può personalizzare il menù utilizzando layout e temi già pronti, e può inoltre modificare i parametri del tema scelto.
- rf-6 anteprima:
  - rf-6.1 l'utente può, attraverso la pagina di modifica del menù, ottenere un'anteprima di cosa vedranno i consumatori.
- rf-7 abbonamento:
  - rf-7.1 l'utente può pagare per abbonarsi al servizio tramite Stripe, sbloccando la funzione di [generazione del codice QR](#generazione-qr).
- <a name="generazione-qr"></a>rf-8 generazione del codice QR:
  - rf-8.1 l'utente può generare codici QR che permettono l'accesso al menù corrispondente;
  - rf-8.2 lo stesso codice QR può condurre a diversi menù o sezioni del menù, per esempio mostrando agli utenti menù differenti in base a data e ora.

Utente non autenticato (consumatore):

- rf-9 consultazione menù:
  - rf-9.1 l'utente può consultare il menù inquadrando il codice QR.
  - rf-9.2 l'utente può selezionare la traduzione del menù che preferisce tra quelle messe a disposizione dal gestore ([v rf-5.4](#traduzione))
  - rf-9.3 l'utente può navigare il menù cliccando, una per volta, le categorie dei prodotti disponibili ([v rf-5.2](#categorie)). 

### Requisiti non funzionali

- rnf-1 privacy:
  - rnf-1.1 l'applicazione non deve memorizzare alcuna informazione personale degli utenti che visualizzano il menù.
- rnf-2 compatibilità browser:
  - rnf-2.1 l'utente deve poter visualizzare correttamente il servizio dalle versioni più aggiornate dei browser Firefox, Safari e Chrome.
- rnf-3 usabilità:
  - rnf-3.1 l'utente trova intuitiva la navigazione dei menù e delle sue categorie: deve essere in grado di comprendere come esplorare il menù entro 10 secondi.
- rnf-4 leggibilità:
  - rnf-4.1 la grandezza di testo, immagini e widget deve essere proporzionata alla grandezza dello schermo del dispositivo utilizzato; Scopo: l'utente non trova difficoltà ad utilizzare il servizio indipendentemente dal dispositivo.
- <a name="sicurezza-password"></a>rnf-5 sicurezza password:
  - rnf-5.1 la password deve essere lunga almeno 8 caratteri, contenere almeno un numero e una lettera maiuscola.
- rnf-6 scalabilità:
  - rnf-6.1 il gestore può creare molteplici menù fino ad un massimo di 100.
- rnf-7 accessibilità:
  - rnf-7.1 il gestore può utilizzare il servizio scegliendo la lingua tra italiano e inglese.

---

Revisione: 0.2
