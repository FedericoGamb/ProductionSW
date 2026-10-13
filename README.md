# Gestione Produzione: avvio in locale

## Cosa serve
- Un computer (o tablet Windows) con **Google Chrome** o **Microsoft Edge**. Firefox e Safari non permettono di collegare una cartella.
- I due file di questo pacchetto: `index.html` e `produzione.json`.

## Preparare la cartella
1. Crea una cartella dedicata, ad esempio `C:\Produzione`.
   Non usare direttamente Desktop, Documenti o Download e nemmeno la radice del disco: Chrome ed Edge li bloccano.
2. Copia dentro la cartella `index.html` e `produzione.json`.
3. Se esiste già una cartella con dati di produzione, **non sostituire il suo `produzione.json`**: contiene tutte le registrazioni.

## Primo avvio
1. Apri `index.html` con Chrome o Edge (tasto destro sul file, poi *Apri con*).
2. Accedi come amministratore: utente `admin`, password `1234`.
3. Clicca **Collega cartella**, scegli la cartella creata e conferma con **Consenti modifiche**.
4. Crea operatori, prodotti, codici causa scarto e codici causa fermo.
5. Esci. Gli operatori accedono con utente `user`, password `1234`, scelgono la loro card e il prodotto e registrano il turno.

## Cosa trovi nella cartella
- `produzione.json`: l'archivio dei dati. Non cancellarlo e non modificarlo a mano.
- `registrazioni.csv` e `ERP_scarti_fermi.xlsx`: si aggiornano da soli a ogni registrazione.

La cartella è la fonte dei dati. Quello inserito prima di collegarla, solo nel browser, non viene importato.

## Stato della cartella
In alto, su ogni schermata, c'è una barra che indica se i dati vengono salvati nella cartella:
- **Verde, "Cartella collegata correttamente"**: tutto a posto.
- **Arancione, "Cartella scollegata: riattiva l'accesso"**: premi **Riattiva accesso**.
- **Rosso, "Cartella non collegata" oppure "Salvataggio non riuscito: ricollega la cartella"**: premi **Collega cartella** (o **Ricollega cartella**) e scegli di nuovo la cartella.

Se l'operatore registra un turno a cartella non collegata, il programma chiede conferma prima di salvare solo nel browser.

## Report (solo amministratore)
Dal menu in alto, voce **Report**. Si può filtrare per periodo (con le scelte rapide Oggi, Ultimi 7 giorni, Questo mese), operatore, prodotto, tipo e causa. Tre viste:
- **Riepilogo**: totali raggruppati per giorno, operatore o prodotto, con % di scarto e tempi di fermo, più le cause di scarto e di fermo.
- **Dettaglio**: l'elenco delle registrazioni, con la possibilità di eliminarle.
- **Grafici**: pezzi prodotti e scartati, scarti e fermi per causa.

## Uso quotidiano
- Dopo aver riaperto il browser compare il pulsante **Riattiva accesso**: cliccalo e conferma, altrimenti i dati non vengono scritti nella cartella.
- Backup: copia ogni tanto l'intera cartella, o almeno `produzione.json`, su un'altra unità.
- Per usare gli stessi dati da due postazioni la cartella deve stare su un percorso condiviso. Non aprire il programma su due postazioni contemporaneamente: vale l'ultimo salvataggio.

## Tablet in produzione
- **Windows con Edge o Chrome**: funziona come sul computer.
- **Android con Chrome**: il collegamento alla cartella è supportato dalle versioni recenti, ma prova prima sul tablet reale.
- **iPad (Safari) o Firefox**: non è possibile collegare la cartella. Serve la versione web con un server.

## Cambiare le password
Le credenziali sono scritte nel file `index.html`: cerca `1234` nella funzione `login` e sostituiscile. Sono visibili a chi apre il file, quindi vanno bene solo per l'uso locale.
