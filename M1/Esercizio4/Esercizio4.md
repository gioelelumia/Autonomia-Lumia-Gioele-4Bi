# Esercizio 4 — Rompere un file CSV e riconoscere i sintomi

## I cinque file

| File | Come è fatto |
|---|---|
| [`verifiche_ok.csv`](verifiche_ok.csv) | Corretto: UTF-8, separatore `,`, voti col punto, 10 righe di dati. I cognomi con la virgola (`Rossi, De Luca` e `Dalla Torre, Gatti`) sono tra virgolette |
| [`verifiche_guasto1_separatore.csv`](verifiche_guasto1_separatore.csv) | Prima riga `sep=;` (dichiara il punto e virgola) ma i dati usano la virgola |
| [`verifiche_guasto2_virgolette.csv`](verifiche_guasto2_virgolette.csv) | Come il file corretto, ma i cognomi con la virgola **senza** virgolette |
| [`verifiche_guasto3_codifica.csv`](verifiche_guasto3_codifica.csv) | Salvato in ISO-8859-1 invece di UTF-8, con la lettera accentata di `Nicolò` |
| [`verifiche_guasto4_decimale.csv`](verifiche_guasto4_decimale.csv) | Separatore `;` e voti con la virgola decimale (`7,5`) |

## Tabella dei guasti

| Guasto | Sintomo osservato | Parametro responsabile | Correzione proposta (senza toccare le celle a mano) |
|---|---|---|---|
| 1. `;` dichiarato, virgola nei dati | Excel mette ogni riga intera in una sola colonna. In Fogli Google di solito la riga `sep=;` non viene capita e compare come una prima riga strana sopra l'intestazione vera | **Separatore di campo** | Importare scegliendo la virgola come separatore (o togliere la riga `sep=;` nell'editor di testo) |
| 2. Cognome con virgola senza virgolette | Le righe con il doppio cognome hanno una colonna in più: il cognome si spezza in due celle e `nome`, `voto` e `data` slittano a destra di una colonna | **Delimitatore di testo** | Il file va risistemato alla fonte: racchiudere il cognome tra virgolette `"..."`, oppure riesportare con il separatore `;` |
| 3. Codifica diversa da UTF-8 | `Nicolò` appare come `Nicol�` (il carattere `�` al posto della `ò`) | **Codifica** | Riaprire il file con la codifica giusta (ISO-8859-1) oppure risalvarlo in UTF-8 con l'editor di testo
| 4. Virgola decimale | La colonna `voto` resta testo (`7,5` allineato a sinistra) e `=MEDIA(C2:C11)` dà 0 o errore | **Separatore decimale** | Usare Trova e sostituisci `,` → `.` sulla colonna |
