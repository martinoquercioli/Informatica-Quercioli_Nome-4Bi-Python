# Riproducibilità del notebook

## Stato iniziale

Il notebook `M1_esercizio10.ipynb` deve arrivare in fondo dopo l'avvio di un kernel locale vuoto. Gli output vengono mantenuti nel primo commit per documentare la verifica.

## Rottura deliberata

Per dimostrare il problema ho definito una variabile in una cella e l'ho usata in una cella successiva. Dopo aver cancellato la cella che definiva la variabile, il notebook continuava a funzionare finché il kernel conservava il valore in memoria.

Dopo `Restart Kernel and Run All Cells`, l'esecuzione si ferma nella cella che usa la variabile rimossa con un errore `NameError`. Questo dimostra che il risultato visualizzato non garantiva la riproducibilità.

## Correzione

Ho ripristinato la cella che definisce la variabile, riordinato le celle secondo le dipendenze e ripetuto l'esecuzione con un kernel locale riavviato. Il notebook corretto arriva in fondo senza errori.

## Output e commit

Il primo commit conserva gli output prodotti dalla verifica. Dopo aver controllato il notebook, ho eseguito:

```bash
jupyter nbconvert --clear-output --inplace M1_jupyter/M1_esercizio10.ipynb
```

Il secondo commit contiene lo stesso notebook senza output salvati. Il confronto si esegue con:

```bash
git diff HEAD~1 HEAD --stat
```

La differenza principale è la rimozione delle righe JSON che rappresentano gli output delle celle. La cartella `.ipynb_checkpoints/` viene ignorata da Git e non compare tra i file non tracciati.
