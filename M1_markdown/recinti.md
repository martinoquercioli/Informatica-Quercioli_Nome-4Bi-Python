# Recinti di codice annidati

## Primo livello

Il primo esempio mostra un normale blocco Java. Nell'anteprima il codice viene colorato come Java.

```java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
```

## Secondo livello

Il secondo esempio mostra come scrivere il blocco Java precedente dentro un recinto esterno. Nell'anteprima il recinto interno appare come testo sorgente.

````markdown
```java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
```
````

## Terzo livello

Il terzo esempio mostra il sorgente del recinto esterno dentro un recinto ancora più grande. Per distinguere i livelli si aggiunge un carattere ` all'esterno.

`````text
````markdown
```java
public class Saluto {
    public static void main(String[] args) {
        System.out.println("Ciao");
    }
}
```
````
`````

L'ultimo paragrafo è testo normale perché tutti i recinti sono stati chiusi.
