# Esercizio 3 — Indici di posizione su tips.csv

## Risultati

| Colonna | Media `=MEDIA(...)` | Mediana `=MEDIANA(...)` | Moda `=MODA(...)` |
|---|---|---|---|
| total_bill | 19,79 | 17,80 | 13,42 |
| tip | 3,00 | 2,90 | 2,00 |
| size | 2,57 | 2 | 2 |

Esempio per total_bill: `=MEDIA(Dati!A2:A245)`, `=MEDIANA(Dati!A2:A245)`, `=MODA(Dati!A2:A245)`.

**Moda di `day`:** la funzione `MODA` non funziona sul testo, quindi ho contato ogni giorno con `=CONTA.SE(Dati!E2:E245;A12)` e ho preso il più frequente con `=INDICE(A12:A15;CONFRONTA(MAX(B12:B15);B12:B15;0))`.

| Giorno | Thur | Fri | Sat | Sun |
|---|---|---|---|---|
| Conti | 62 | 19 | **87** | 76 |

Moda di `day` = **Sat**.

## Commenti (quattro righe)

- **total_bill:** media 19,79 contro mediana 17,80, la media è più alta di circa 2 (+11%). Pochi conti molto alti la «tirano su»: distribuzione un po' asimmetrica verso destra.
- **tip:** media 3,00 e mediana 2,90 sono molto vicine, quindi secondo questi indici è quasi simmetrica. Per esserne sicuri servirebbe un istogramma, perché ci sono poche mance alte (massimo 10).
- **size:** media 2,57 contro mediana e moda 2. Quasi tutti i tavoli sono da 2 persone e pochi tavoli grandi (fino a 6) alzano la media: asimmetria verso destra.
- **day:** media e mediana non sono state richieste perché `day` è una variabile nominale (testo). Non si possono sommare i giorni, e l'ordine alfabetico (Fri, Sat, Sun, Thur) non è un ordine con significato. L'unico indice possibile è la moda..
