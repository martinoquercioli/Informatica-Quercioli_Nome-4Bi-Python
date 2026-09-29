# Esecuzione fuori ordine di un notebook

## Ordine reale di esecuzione

Le celle sono state eseguite nell'ordine `[1]`, `[2]`, `[3]`, `[4]`. I numeri tra parentesi quadre sono assegnati dal kernel e descrivono l'ordine di esecuzione, non la posizione grafica della cella.

## Valore di `posti` nella cella [3]

La cella `[3]` è stata eseguita prima della cella `[4]`. In quel momento `posti` valeva `24`, quindi l'espressione `posti - iscritti` produceva `24 - 22`, cioè `2`. La cella `[4]` ha poi modificato il valore a `22`.

## Risultato dopo il riavvio

Con `Restart Kernel and Run All Cells`, le celle vengono eseguite dall'alto verso il basso secondo l'ordine in cui sono scritte nel notebook. La prima cella assegna `posti = 24`; la seconda lo porta a `22`; la terza si interrompe perché `iscritti` non è ancora stata definita. Gli output e l'errore previsti sono:

```text
Posti disponibili: 22
NameError: name 'iscritti' is not defined
```

La cella che stampa `Iscritti: 22` non viene eseguita, perché il kernel si ferma sulla cella precedente. Anche la cella con `posti = posti - 2` non viene ripetuta dopo l'errore. La stampa `liberi: 2` appartiene invece alla cronologia già salvata, nella quale `iscritti` era stata definita prima.

## Errore da kernel vuoto

Con un kernel appena avviato, l'esecuzione grafica dall'alto verso il basso si interrompe sulla cella che contiene `print(aula, "-", "liberi:", posti - iscritti)` se `iscritti` non è stata ancora definita. Il messaggio esatto è:

```text
NameError: name 'iscritti' is not defined
```

## Correzione

Sposta la cella `iscritti = 22` prima della cella che usa `iscritti` e sposta la sottrazione di `posti` dopo quella stampa, oppure riordina tutte le celle secondo le dipendenze. In questo modo il notebook arriva in fondo senza errori e la cella della disponibilità stampa `liberi: 2`.
