# Checklist aggiornamento sistema
## Introduzione
Questa pagina elenca i passi necessari da eseguire ogni qualvolta si debba aggiornare un sistema. La lista sarà molto specifica, basta saltare i passaggi nel caso non fossero necessari nel caso in esame.

## Lista passi da eseguire

- Verificare dal documento di aggiornamento eventuali limitazioni di Fix del sistema in oggetto
- Verificare dal documento di aggiornamento eventuali comandi extra da lanciare (es. doppio `insrfr`)
- Verificare sul filesystem la presenza di spazio adeguato per ospitare i backup, i pacchetti e l'ampliamento del sistema a fronte dell'installazione degli stessi
- Esportare i pacchetti dal sistema oggetto prima di procedere a un cambio release
- Spegnere il sistema oggetto
- Rimuovere le eventuali patch presenti nella cartella del sistema oggetto
- Copiare i pacchetti nella cartella `refreshes/import`
- Lanciare il bat del MessageServer
- Lanciare il comando `insrfr -codeclass:sys -codeclass:app -installtype:3` (adattabile a seconda delle esigenze)
- Una volta terminato, verificare se ci sono job creati. Se ce ne sono, ci sono conflitti da gestire
- Gestire i conflitti dalla macchina di sviluppo, tramite la task creata, avendo cura di aggiornare il progetto padre prima di lavorare.
- Attivare i conflitti
- Riavviare la macchina
- Eseguire gli aggiornamenti dati

Una volta esaurita questa lista, l'aggiornamento è completo e andato a buon fine.
