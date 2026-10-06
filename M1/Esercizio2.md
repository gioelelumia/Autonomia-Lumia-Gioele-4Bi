# Esercizio 2 — Le scale di misura delle colonne del Titanic

## Tabella (12 colonne)

| Colonna | Tipo caricato dal foglio | Scala di misura | Operazione che ha senso / che non ha senso |
|---|---|---|---|
| PassengerId | Numero | Nominale (è solo un codice) | **Sì:** contare i passeggeri, controllare i doppioni. **No:** la media |
| Survived | Numero | Nominale (0 = morto, 1 = vivo) | **Sì:** contare gli 0 e gli 1, la moda. **No:** sommarla o farne la deviazione standard come se fosse una quantità |
| Pclass | Numero | Ordinale (1ª > 2ª > 3ª, distanze non misurate) | **Sì:** ordinare, mediana, moda. **No:** la media (una classe «media» di 2,3 non esiste) |
| Name | Testo | Nominale | **Sì:** contare, cercare un nome. **No:** media o mediana |
| Sex | Testo | Nominale | **Sì:** moda e conteggio maschi/femmine. **No:** mediana |
| Age | Numero (177 vuoti) | Rapporti | **Sì:** media, mediana, rapporti (40 anni = il doppio di 20). **No:** sommarla con Fare (unità diverse) |
| SibSp | Numero | Rapporti (conteggio, 0 = nessuno) | **Sì:** `SibSp + Parch` = familiari a bordo. **No:** sommarla con Fare |
| Parch | Numero | Rapporti (conteggio, 0 = nessuno) | **Sì:** media di genitori/figli per passeggero. **No:** sommarla con Age |
| Ticket | Misto (661 numeri e 230 testi) | Nominale (codice del biglietto) | **Sì:** contare chi ha lo stesso biglietto. **No:** la media, anche quando il codice è fatto di cifre |
| Fare | Numero | Rapporti (zero vero, «costa il doppio» ha senso) | **Sì:** media, mediana, rapporto fra due prezzi. **No:** sommarla con Age |
| Cabin | Testo (687 vuoti) | Nominale | **Sì:** contare le cabine indicate, moda. **No:** ordinarle come se una valesse più di un'altra |
| Embarked | Testo (2 vuoti) | Nominale (C, Q, S sono porti) | **Sì:** moda e conteggio per porto. **No:** media o mediana |

## Nota sulle colonne segnalate (numeriche ma non di rapporti)

- **PassengerId:** il foglio la carica come numero, ma i numeri sono solo etichette. Il passeggero 400 non è «il doppio» del 200. È nominale.
- **Survived:** carica come numero, ma 0 e 1 sono i nomi di due categorie (morto/vivo), non una misura. È nominale.
- **Pclass:** carica come numero, ma indica solo un ordine (1ª, 2ª, 3ª): non sappiamo quanto la 1ª sia «più» della 2ª. È ordinale.

Anche **Ticket** ha il tipo incoerente: il foglio lo legge come «misto» perché i codici fatti solo di cifre diventano numeri e gli altri restano testo, ma la scala è sempre nominale.
