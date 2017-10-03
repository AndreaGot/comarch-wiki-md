# Comandi dopo upgrade
Dopo un aggiornamento è bene controllare lo stato delle tabelle ed eventualmente correggere gli errori:

- `chkdbt -analyseTables -all -table:% -olap -oltp –repository`
- `rgzbo` per gli oggetti che danno errori.


Per cancellare guid errati, come nel caso dei ruoli di autorizzazione (ad esempio oggetti linkati erroneamente copiando DB da un sistema a un altro) lanciare il comando

- `wrksec -deleteInvalid`

Per utilizzare labels di altre lingue (tipo `de`) dove non disponibili (tipo traduzioni in `en` e `it` mancanti), lanciare il comando

  - `cpysystbl -all`
