## **Istanze e attributi**

> * **Numero di istanze:** 344  
> * **Numero di attributi:** 7

## **Nomi delle colonne**

Il dataset è composto dai seguenti attributi:

> * species  
> * island  
> * bill_length_mm 
> * bill_depth_mm
> * flipper_length_mm
> * body_mass_g
> * sex

## **Analisi delle domande di apprendimento**

| Domanda | Etichetta | Colonne in ingresso |
| :---- | :---- | :---- |
| A quale specie appartiene un pinguino di cui conosco le misure? | species | bill_length_mm, bill_depth_mm, flipper_length_mm, body_mass_g |
| Quanto pesa un pinguino di cui conosco specie, isola e misure del becco? | body_mass_g | species, island, bill_length_mm, bill_depth_mm |

## **Perché l'etichetta cambia**

L'etichetta cambia perché dipende dalla domanda che facciamo al computer: i dati restano uguali, ma siamo noi a decidere cosa vogliamo calcolare o indovinare ogni volta.