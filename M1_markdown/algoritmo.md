# Ricerca sequenziale in un array

La ricerca sequenziale esamina gli elementi di un array da sinistra verso destra. Nell'esempio l'array contiene `{7, 6, 8, 5, 9}` e il valore cercato è `8`, che si trova all'indice `2`.

```java
public static int cerca(int[] valori, int cercato) {
    for (int indice = 0; indice < valori.length; indice++) {
        if (valori[indice] == cercato) {
            return indice;
        }
    }
    return -1;
}
```

```mermaid
flowchart TD
    A([Inizio]) --> B[Imposta indice a 0]
    B --> C{Indice minore della lunghezza?}
    C -- No --> D[Restituisci -1]
    C -- Si --> E{Elemento uguale al valore?}
    E -- Si --> F[Restituisci indice]
    E -- No --> G[Incrementa indice]
    G --> C
    D --> H([Fine])
    F --> H
```

Se l'elemento cercato non è presente, il ciclo arriva alla fine dell'array senza trovare corrispondenze. Il metodo restituisce `-1`, un valore che segnala l'assenza dell'elemento.
