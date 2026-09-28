# Varianti di Markdown a confronto

| Costrutto | Markdown originale | CommonMark | GitHub Flavored Markdown |
|:---|:---:|:---:|:---:|
| Blocchi di codice recintati | Parziale | Sì | Sì |
| Tabelle | No | No | Sì |
| Caselle di spunta | No | No | Sì |
| Testo barrato | No | No | Sì |
| Collegamenti automatici | Sì | Sì | Sì |
| Note a piè di pagina | No | No | Sì |

## Esempi GFM

- [x] Scrivere il documento
- [x] Controllare l'anteprima
- [ ] Verificare i collegamenti
- [ ] Controllare l'immagine
- [ ] Eseguire il notebook locale
- [ ] Preparare il commit

La versione ~~superata~~ della consegna non va più utilizzata.

Un collegamento automatico è visibile all'indirizzo https://commonmark.org/.

Per le consegne del corso conviene usare GitHub Flavored Markdown perché il repository viene letto soprattutto su GitHub e questa variante supporta tabelle, checkbox e testo barrato. CommonMark offre una base più portabile, ma non riconosce tutte le estensioni usate nella consegna. Markdown originale è ancora utile per la sintassi essenziale, ma non basta per rappresentare ogni requisito. Nell'anteprima di Visual Studio Code le estensioni GFM possono essere rese in modo simile, mentre uno strumento che implementa solo CommonMark mostrerà la tabella e le checkbox come testo non esteso. Le note a piè di pagina e altri dettagli possono quindi perdere la loro resa speciale.
