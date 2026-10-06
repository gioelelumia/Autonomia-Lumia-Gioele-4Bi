## 1. Raccolta dei Dati
Raccogliamo le vecchie bollette della luce e i registri degli anni passati. Uniamo questi numeri con i dati della segreteria per sapere quando la scuola è rimasta aperta o chiusa.

## 2. Preparazione dei Dati
Sistemiamo la tabella correggendo gli errori accumulati nel tempo. 

* **Buchi nei dati:** Mesi interi senza registrazioni perché nessuno ha segnato i numeri o si sono perse le bollette.
*  **Errori di scrittura:** Valori scritti a mano con cifre invertite o unità di misura sbagliate.
*  **Date sballate:** Bollette arrivate a intervalli di giorni irregolari (mesi da 30 giorni misurati insieme a periodi più lunghi).

## 3. Scelta della Rappresentazione e Definizione del Problema
Decidiamo gli elementi chiave per far funzionare il programma:
- **Istanza:** Un singolo mese del passato (ad esempio "Gennaio 2025").
- **Attributi:** La temperatura media del mese, quanti giorni di scuola ci sono stati, le ore di accensione dei riscaldamenti o dei condizionatori e i consumi del mese prima.
- **Etichetta:** I kWh di luce consumati davvero in quel mese.
- **Tipo di problema:** È un problema di **regressione**, perché dobbiamo calcolare un numero (i kWh) e non una categoria.

## 4. Scelta del Modello
Scegliamo un programma di calcolo capace di trovare il legame tra il freddo, i giorni di scuola e la corrente usata.

## 5. Addestramento
Diamo al computer la tabella con i vecchi dati. Il programma studia gli esempi per capire da solo quali fattori fanno salire o scendere i consumi.

## 6. Valutazione
Facciamo una prova per vedere se il computer riesce a indovinare i consumi dell'anno scorso senza guardare le bollette vere. Se sbaglia troppo, correggiamo il programma o i dati.

## 7. Distribuzione e Utilizzo
Mettiamo il programma a disposizione della segreteria della scuola in un file Excel. In questo modo, inserendo le previsioni del tempo e i giorni di lezione futuri, la scuola saprà quanta spesa mettere a budget per la luce.