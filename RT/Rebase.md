### REBASE
N.B. di seguito sono elencati i vari passaggi per fare un rebase correttamente e quindi poter fare una P.R..
E' buona prassi interrompere la compilazione prima di effettuare questi passaggi.

- fare 'fetch' per vedere se ci sono aggiornamenti [tasto 'nuvoletta' in alto a dx dentro a git graph]. ![[Screenshot 2023-01-15 alle 17.12.33.png]]
  A volte è necessario lanciare il comando `git fetch --prune` dopo aver 'fetchato' in quanto git graph potrebbe non aver scaricato tutti gli aggiornamenti.
- entrare sul branch 'main'  [doppio click] 
- 'pullare' [tasto in basso a sx o tramite 'sync' in 'source control']
- rientrare nel branch 'feat/[nome branch]' e posizionarsi sopra al main
- premere il tasto dx e dare 'rebase'
- provare a lanciare progetto per vedere se funziona (`ng serve nome-progetto`)
- fare il sync finale 
- cancellare vecchio branch (quello secondario)