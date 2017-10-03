# Aggiornamento sistema produzione
## Preparazione

### Lato Semiramis test
- `Gestione sistema` > `Cockpit aggiornamenti software` > `Crea consegna`
- Deselezionare status `Riassunto` e lanciare la ricerca
- Selezionare tutti i pacchetti interessati all'installazione (riconoscibili sulla base della richiesta di sviluppo)
- Inserire nello spazio vuoto il numero di consegna, facendo attenzione a procedere in maniera progressiva
- Seguire tutta la lista delle azioni (specialmente nel caso di pacchetti contenenti classi)
- Fare attenzione ad eventuali aggiornamenti obbligatori o direttamente dipendenti

### Lato macchina test
- Andare a recuperare i pacchetti (uno per record) in `semiramis/refreshes/export`

## Esecuzione

- Prima di procedere con l'installazione, assicurarsi di aver eseguito la procedura di backup per il sistema di destinazione.

### Lato macchina produzione

- Installare i pacchetti precedentemente esportati in `semiramis/refreshes/import`
- Spegnere tutti i servizi collegati al sistema che si vuole aggiornare
- Lanciare l'applicazione batch del server MS contenuta in `semiramis/servers/<nomeMS>/<nomeMS>.bat`
- Eseguire i comandi dell'installazione automatica o di quella manuale

#### Installazione automatica
- `insrfr -codeclass:app -installtype:3`
 - Effettua tutti i riavvii, anche più del dovuto, dipende da cosa è contenuto nei pacchetti

#### Installazione manuale
- `imprfr -codeclass:app -all`
- `upgaps -codeclass:app -prepare`
- `upgaps -codeclass:app -upgrade`
- Effettuare riavvio
- `upgaps -codeclass:app -activate`
- `upgaps -codeclass:app -release`

Indipendentemente dal tipo di installazione eseguita, alla fine un messaggio avviserà dell'avvenuta installazione.

- Lanciare il comando `stop` fino a che la finestra non si chiude da sola
- Ripristinare i servizi di Semiramis, prima il servizio MS, poi tutti gli altri.
