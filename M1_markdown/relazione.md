# Relazione sull'ordinamento di un array

## Indice

- [Obiettivo](#obiettivo)
- [Materiale](#materiale)
- [Procedimento](#procedimento)
- [Risultati](#risultati)
- [Conclusioni](#conclusioni)

## Obiettivo

Misurare il tempo necessario a ordinare array di dimensioni diverse con un algoritmo di ordinamento semplice. Il tempo viene espresso in millisecondi.[^misura]

## Materiale

Sono stati usati Python, Visual Studio Code e quattro array di interi con dimensione 100, 1000, 10000 e 100000. La misurazione è stata ripetuta con la stessa procedura.[^ripetizione]

## Procedimento

1. Creare un array di dimensione stabilita.
2. Avviare il cronometro.
3. Ordinare l'array.
4. Fermare il cronometro e registrare il risultato.

```python
valori = [7, 6, 8, 5, 9]
valori.sort()
print(valori)
```

## Risultati

| Dimensione | Tempo prima prova (ms) | Tempo seconda prova (ms) |
|---:|---:|---:|
| 100 | 1 | 1 |
| 1000 | 3 | 2 |
| 10000 | 18 | 17 |
| 100000 | 240 | 235 |

I tempi aumentano insieme alla dimensione dell'array. Le due prove non coincidono sempre perché il sistema esegue anche altri processi.

## Conclusioni

L'esperimento mostra che la dimensione dell'input influenza il tempo di esecuzione. Per confrontare algoritmi diversi occorre mantenere uguali ambiente, dati e procedura di misura.

[^misura]: Il valore riportato è il tempo osservato dal programma durante una singola prova.
[^ripetizione]: La ripetizione riduce il rischio di basare la conclusione su una sola misura anomala.
