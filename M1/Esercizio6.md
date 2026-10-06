# Esercizio 6 — Il prezzo del biglietto: media o mediana?

## Tabella (4 righe × 3 indici)

| Gruppo | N | Media | Mediana | Dev. standard | Media − Mediana |
|---|---|---|---|---|---|
| Tutti | 891 | 32,20 | 14,45 | 49,69 | 17,75 |
| 1ª classe | 216 | 84,15 | 60,29 | 78,38 | **23,87** |
| 2ª classe | 184 | 20,66 | 14,25 | 13,42 | 6,41 |
| 3ª classe | 491 | 13,68 | 8,05 | 11,78 | 5,63 |

- Media: `=MEDIA.SE(C2:C892;1;J2:J892)`
- Mediana: `=ARRAYFORMULA(MEDIANA(SE(C2:C892=1;J2:J892)))`
- Deviazione standard: `=ARRAYFORMULA(DEV.ST.C(SE(C2:C892=1;J2:J892)))`

## Cosa si osserva

In tutti e quattro i casi la media è **più alta** della mediana: pochi biglietti molto cari alzano la media. Lo scarto più grande è in 1ª classe (23,87), dove la media è circa 1,4 volte la mediana.

## Media o mediana per il giornale?

Userei la **mediana**: «metà dei passeggeri pagò meno di 14,45 (sterline, da verificare nel dizionario dei dati)». La media (32,20) è tirata su da pochi biglietti da 200–500, e quasi nessuno ha davvero pagato 32: non descrive un passeggero tipico. La mediana è meno sensibile ai valori estremi. In 1ª classe, dove media e mediana sono molto diverse e la deviazione standard (78,38) è quasi quanto la media, i prezzi sono molto sparpagliati e la mediana resta la scelta più onesta.

## Il valore responsabile

È **512,3292**, il massimo di `Fare` (compare 3 volte, gli altri più alti sono 263). Tolti questi tre valori la media della 1ª classe scende da 84,15 a 78,12, cioè di circa 6 punti. Quindi da solo non spiega tutti i 23,87 di scarto: il resto è dovuto a tanti altri biglietti molto cari.
