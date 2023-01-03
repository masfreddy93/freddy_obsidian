1. Creare folder del progetto (es. ts-intro)
2. Aprire folder con vsc (o altro editor) e lanciare da terminale il comando  `npm init`
3. Rispondere a domande del terminale per inserire i dati del progetto (es. nome progetto, autore, git, versione ...)
4. Terminata l'operazione al punto 3, verrà creato un file 'package.json' contentente i dettagli del ns progetto. Lanciare quindi il comando `npm install --save-dev typescript` per installare la libreria typescript nel progetto (verrà visualizzato nel file 'package.json' tra le dipendenze) 
5. Ora è possibile creare file .ts e scrivere codice ts


### Generare il file js attraverso la compilazione

##### Qualora non si sia installato typescript globalmente 
6. All'interno del file 'package.json', dentro la voce `"scripts": { }` inserire la seguente riga di codice: `"compile": "tsc nomefile.ts"` e poi lanciare da terminale il comando `npm run compile`
7. Verrà generato il relativo file in formato .js (es. app.js)

##### Qualora non si sia installato typescript globalmente 
6. Lanciare da terminale il comando `tsc nomefile.ts` (nota che installare typescript globalmente rende il gioco più veloce)
7. Verrà generato il relativo file in formato .js (es. app.js)