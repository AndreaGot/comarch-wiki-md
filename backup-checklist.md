# Backup
## Introduzione

Prima di procedere con l'installazione di un aggiornamento in un sistema di produzione, è assolutamente necessario procedere con un backup, in modo da ripristinare la completa funzionalità nel caso la procedura di aggiornamento non dovesse andare a buon fine.

Il metodo di backup è sostanzialmente lo stesso per tutti i sistemi.

## Procedimento

### Filesystem
Per procedere con il backup del filesystem è sufficiente eseguire la copia della cartella semiramis, anche a sistema funzionante. Nel caso il sistema sia acceso al momento del backup potranno verificarsi degli errori a causa di file aperti, ma sono ignorabili in quanto si tratta principalmente di file di log. É preferibile eseguire il backup a sistema in funzione, poichè tale copia impiega molto tempo, ma non influisce in maniera sostanziale sulle prestazioni.

Il backup può essere eseguito sia effettuando una semplice copia, sia creando direttamente un file compresso.

### Database
Per quanto riguarda i database, essendo il luogo dove le modifiche eseguite tramite Semiramis vengono applicate, è obbligatorio eseguire il backup solo a sistemi completamente spenti. Diversamente, si corre il rischio di ritrovarsi con dei backup non funzionanti perchè eseguiti durante delle operazioni di scrittura potenzialmente molto estese.

Per eseguire il backup occorre:

- Collegarsi all'istanza SQL Server sulla macchina che ospita i database.
- Individuare i database oggetto del backup, anche aiutandosi con il cockpit sistema prima di spegnere.
 - I database sono almeno un `OLTP`, un database `RP` (repository) e uno `CF` (configurazione).
- Per ogni database:
 - `Clic destro` > `Tasks` > `Backup`
 - Selezionare il percorso dove salvare i backup ricordando di inserire l'estensione .bak nel nome del file
 - Selezionare l'opzione relativa alla compressione del backup, invece che quella di default del server
 - Lanciare l'esecuzione.
- É consigliato procedere un database alla volta, nonostante sia possibile lanciare backup multipli.

Alla fine di queste due operazioni, è possibile procedere in sicurezza con l'aggiornamento.
