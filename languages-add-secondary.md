# Aggiunta lingue secondarie al sistema
## Introduzione
É possibile, sulla base della licenza posseduta, aggiungere delle lingue al sistema, in modo che i campi multilingua la contengano.

## Esecuzione
- Dal Cockpit sistema, selezionare il database e andare sulla scheda `Lingue`
- Aggiungere le lingue richieste
- Eseguire il comando `crtdbinf -db:<nomeDB> -nlsAutomatic` (es. `crtdbinf -db:P4358015402 -nlsAutomatic`) dalla toolshell
