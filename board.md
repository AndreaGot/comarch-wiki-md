# Board
## Introduzione
Board è un sistema adottato da alcuni clienti, che si basa su task presenti a livello di database che interrogano determinate viste e creano un file di testo che viene poi interpretato da una applicazione esterna.

## Come si usa
Per modificare il comportamento di una esportazione board è sufficiente collegarsi al database su cui si vuole operare. All'interno ci sono alcune viste identificate dal prefisso BOARD_, che contengono i dati necessari.

Basta modificare la vista (avendo cura di fare il backup di quella attiva) e le modifiche saranno subito verificabili lanciando la vista stessa, oppure procedendo all'esportazione Board vera e propria.

## Problemi segnalati
- Il cliente ha segnalato un problema di aggiornamento dei dati: Nonostante l'esportazione programmata venisse eseguita senza problemi, l'applicativo lato cliente non sembrava aggiornare i dati.
 - Il problema è stato risolto riavviando il server Board, come tra l'altro consigliato nei log dell'applicazione stessa.
