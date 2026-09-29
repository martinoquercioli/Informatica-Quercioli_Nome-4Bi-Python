# Compilare ed eseguire un programma Java

1. Clona il repository e spostati nella cartella del progetto.

   - Controlla che esista la cartella `src/`.
   - Individua il file `MediaVoti.java`.

   ```bash
   git clone https://github.com/esempio/media-voti.git
   cd media-voti
   ```

2. Crea la cartella `bin/`, che conterrà i file compilati.

   ```bash
   mkdir -p bin
   ```

3. Compila il sorgente `src/MediaVoti.java` usando l'opzione `-d` per indicare la cartella di destinazione.

   ```bash
   javac -d bin src/MediaVoti.java
   ```

4. Esegui la classe `MediaVoti` indicando `bin/` nel classpath.

   ```bash
   java -cp bin MediaVoti
   ```

5. Controlla l'output e verifica che il comando sia stato eseguito dalla cartella principale del repository.

Se il JDK non è installato, il terminale può mostrare:

> 'javac' non è riconosciuto come comando interno o esterno.

Installa un JDK compatibile, aggiungi la sua cartella `bin` alla variabile `PATH` e riapri il terminale prima di ripetere la compilazione.
