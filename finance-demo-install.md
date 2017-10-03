# Aggiornamento finance in DEMO

## Introduzione

Per aggiornare il sistema `DEDADEMO` (sia 5.2 che 5.3) con le fix della Finance di Comarch, è necessario collegarsi al sistema di supporto Comarch, Interroga consegne di supporto di tipo `APP`.

La visualizzazione predefinita le elenca in ordine crescente di data, ed è necessario ordinare per data di approntamento decrescente.

## Scaricare i pacchetti

- Si selezionano gli aggiornamenti da installare, con alcuni accorgimenti:
 - Si possono installare più Fix insieme, solo se appartengono allo stesso sistema (Finance, piuttosto che Fin4IT, piuttosto che Fin4FR)
 - Se una release finance non è installata, non è possibile selezionare le Fix relative, ma è necessario prima procedere all'installazione della release base.
- Una volta selezionato, leggere le indicazioni di installazione presenti per ogni pacchetto, per accertarsi di eventuali dipendenze o richieste particolari.
- Scaricare i pacchetti relativi, con il comando di riga se è uno solo, oppure col comando globale nella coolbar.

## Installazione dei pacchetti

- Per installare i pacchetti, non basta portarli nel sistema `DEDADEMO` di riferimento, ma è necessario passare per il relativo DV (`DEDAGROUPDV`) e per il test (`DEDADT`) della versione di riferimento.

- Eseguire il backup per ogni passaggio (spesso basta solo il filesystem poichè ci sono i backup della notte)
- Installare i pacchetti in DV
- Procedere come una installazione normale
