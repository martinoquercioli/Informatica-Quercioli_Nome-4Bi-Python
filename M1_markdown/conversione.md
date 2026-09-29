# Conversione della relazione

La relazione dell'esercizio 7 viene convertita in un HTML autonomo e in un PDF. I comandi vanno eseguiti dalla radice del repository.

## File HTML

```bash
pandoc M1_markdown/relazione.md --standalone --toc --toc-depth=2 --metadata title="Relazione sull'ordinamento di un array" --embed-resources -o M1_markdown/relazione.html
```

- `--standalone` crea un documento HTML completo.
- `--toc` genera l'indice automatico.
- `--toc-depth=2` limita l'indice ai titoli di secondo livello.
- `--metadata title` imposta il titolo del documento.
- `--embed-resources` incorpora le risorse nel file HTML.
- `-o` indica il file di output.

## File PDF

```bash
pandoc M1_markdown/relazione.md -V geometry:margin=2.5cm -V fontsize=11pt -V lang=it --pdf-engine=xelatex -o M1_markdown/relazione.pdf
```

- `-V geometry:margin=2.5cm` imposta i margini.
- `-V fontsize=11pt` imposta il corpo del carattere.
- `-V lang=it` imposta la lingua italiana.
- `--pdf-engine=xelatex` gestisce correttamente i caratteri accentati.

I file HTML e PDF sono derivati e non devono essere versionati. Se Pandoc segnala che manca `xelatex`, va installato un motore LaTeX compatibile prima di ripetere il comando.
