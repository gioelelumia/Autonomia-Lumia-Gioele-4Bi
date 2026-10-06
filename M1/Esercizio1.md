# Esercizio 1 — Anatomia di penguins.csv


## 1. Prima riga del file (come appare nell'editor di testo)

```
species,island,bill_length_mm,bill_depth_mm,flipper_length_mm,body_mass_g,sex
```

Sono i nomi dei 7 attributi (colonne), separati da virgole. In Fogli Google la stessa riga diventa la riga 1 con un nome per cella.

## 2. Quante righe?

| Cosa conto | Numero | Formula nel foglio |
|---|---|---|
| Righe totali del file | **345** | `=CONTA.VALORI(Dati!A:A)` |
| Istanze (pinguini) | **344** | `=B4-1` |

**Differenza:** le righe totali comprendono anche la riga di intestazione, che contiene i nomi delle colonne e non è un pinguino.

## 3. I cinque parametri di lettura

| Parametro | Valore usato dal file | Da cosa l'ho capito |
|---|---|---|
| Separatore di campo | virgola `,` | nella riga di intestazione e in tutte le righe i valori sono separati da virgole |
| Delimitatore di testo | nessuno usato (lo standard è `"`) | nel file non ci sono virgolette, perché nessun valore contiene virgole |
| Codifica | UTF-8 (in pratica solo ASCII) | non ci sono lettere accentate: tutti i caratteri sono ASCII, uguale a UTF-8 |
| Separatore decimale | punto `.` | valori come `39.1` e `18.7` |
| Riga di intestazione | sì, la riga 1 | la prima riga è testo (nomi delle colonne), le altre sono dati |
