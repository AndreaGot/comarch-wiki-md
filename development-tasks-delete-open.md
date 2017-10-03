# Cancellazione task aperti
Se nell'applicazione "Task di sviluppo" sono presenti task aperti che non è possibile cancellare, utilizzare il seguente comando per forzarne la cancellazione:

the tool `rgzrep` provides some helpful functions.


`-deleteOpenJobs` removes all open tasks. The tasks must be empty before.

`-lockedObjects` removes all objects from every!!!! open task. Check your OLTPs with chckdbt if business objects were removed in this way.

## IMPORTANTE

aggiungere `-commit` per rendere effettiva l'operazione

Per un comodo copia e incolla:

   `rgzrep -deleteOpenJobs -lockedObjects -commit`
