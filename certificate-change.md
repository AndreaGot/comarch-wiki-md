# Cambio certificati sistema
## Introduzione
Con l'inizio del 2017, i maggiori browser dismetteranno gradualmente i certificati con una codifica debole. Nel caso di Comarch, tali certificati corrispondono alla codifica SHA1.

## Esecuzione
Dopo aver creato una nuova CA, è necessario utilizzarla per emettere i nuovi certificati utente. Fatto ciò, è necessario spostare gli AS sul nuovo certificato, utilizzando l'azione "crea ed emetti certificato" sull'AS stesso. É necessario ricordarsi anche il SOM, che non funziona più se si tengono i certificati vecchi.
