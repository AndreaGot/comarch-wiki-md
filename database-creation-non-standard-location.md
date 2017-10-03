# Creazione database in location non standard
## Introduzione
SQL Server permette di operare sui database solo tramite la location standard specificata in fase di installazione. Per poter creare un database in una location non standard, è necessario seguire una procedura apposita.

## Passi da eseguire
- Creare un database utilizzando il wizard, specificandone il nome.
- Controllare il luogo dove sono salvati i file dati e log, dalle proprietà del database
- Effettuare il detach del database
- Tagliare e incollare i due file, dati e log, dalla cartella originaria in quella destinazione
- Eseguire l'attach del database, utilizzando i file appena spostati.
 - Fare attenzione al file di log, che il sistema andrà a cercare nella cartella standard. In questo caso è sufficiente specificare il luogo dove è stato copiato.

Ora il database è disponibile per l'utilizzo
