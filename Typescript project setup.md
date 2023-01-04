## Typescript project setup

1. Creare folder del progetto (es. ts-intro)
2. Aprire folder con vsc (o altro editor) e lanciare da terminale il comando  `npm init`
3. Rispondere a domande del terminale per inserire i dati del progetto (es. nome progetto, autore, git, versione ...)
4. Terminata l'operazione al punto 3, verrà creato un file 'package.json' contentente i dettagli del ns progetto. Lanciare quindi il comando `npm install --save-dev typescript` per installare la libreria typescript nel progetto (verrà visualizzato nel file 'package.json' tra le dipendenze) 
5. Ora è possibile creare file .ts e scrivere codice ts

##### Generare il file js attraverso la compilazione (qualora non si sia installato typescript globalmente )
6. All'interno del file 'package.json', dentro la voce `"scripts": { }` inserire la seguente riga di codice: `"compile": "tsc nomefile.ts"` e poi lanciare da terminale il comando `npm run compile`
7. Verrà generato il relativo file in formato .js (es. app.js)

##### Generare il file js attraverso la compilazione (qualora si sia installato typescript globalmente )
6. Lanciare da terminale il comando `tsc nomefile.ts` (nota che installare typescript globalmente rende il gioco più veloce)
7. Verrà generato il relativo file in formato .js (es. app.js)


8. Per usare ts in un progetto Node  ---> lanciare da terminale il comando `npm i -D @types/node`. Se lavoro in progetto web non serve

##### Aggiungere watch al compilatore (qualora non si sia intallato typescript globalmente)
9. All'interno del file 'package.json', dentro la voce `"scripts": { }` inserire la seguente riga di codice: `"tsc:w": "tsc -w"` 
10. Creare file 'tsconfig.json' con il seguente codice all'interno
```
{
	"compilerOptions": {
		"outDir": "build"
	},
	"include": ["src/**/*.ts"]
}
```
Con questo codice si dice al compilatore: "Vai a prendere tutti i file .ts all'interno della cartella 'src' e dopo averli compilati manda i relativi file convertiti in .js dentro ad una cartella che si chiama 'build'".
11. Creare dunque la cartella 'src' nel progetto e sposto il file in formato .ts (es. app.ts) al suo interno   (vedi screen)

![[Screenshot 2023-01-03 alle 13.19.08.png]]

12. Lanciare comando da terminale `npm run tsc:w`
13. D'ora in poi ogni cambiamento sul file .ts verrà compilato e riconvertito in .js in maniera AUTOMATICA al salvamento del file .ts
	N.B. di default il compilatore convertirà il file .ts in ECMA5 e dunque una variabile 'let' nel file .ts sarà convertita in una variabile di tipo 'var' nel file .js


fonte: https://www.youtube.com/watch?v=9CNppuTuvQs&list=PLYrQFCVhfFIt4k21sOv8Ll29ZxLQTSmR1&index=3


14. Se si vuole convertire il file .ts in codice ES6 occorre aggiungere il seguente script all'interno del file 'tsconfig.json' sotto la voce 'compilerOptions' ---> `"target": "ES6"`. Vedi screen
![[Screenshot 2023-01-04 alle 09.20.42.png]]
		N.B. In caso di importazione di moduli/file sarà necessario specificare il formato di essi (altrimenti non verrà inclusa l'estensione nei relativi file .js dopo la conversione). Vedi screen![[Screenshot 2023-01-04 alle 09.25.01.png]]
		Sarebbe meglio imparare ad usare le webpack.
		Si può anche importare nella maniera vecchia ovvero con il 'require'.

fonte: https://www.youtube.com/watch?v=2QKCw7vz40g&list=PLYrQFCVhfFIt4k21sOv8Ll29ZxLQTSmR1&index=6


