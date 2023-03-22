---
---

##### Versioon 16.0.23081.0
- Parandatud olukord, kus kasutades ostuarvel korraga mittemahaarvatavat käibemaksu ja periodiseerimist ning saates arve kinnitusringile, kuvati kinnitajale konteeringu eelvaates valede summadega kanded.

##### Versioon 16.0.23037.0
- Lisatud loogika, et KMD nn põhiosa XML faili tulevad tag-id ainult siis, kui seal on väärtus _(vältimaks olukorda, kus raamatupidaja maksuametis igaks-juhuks neid nulle igakuiselt kustutamas käis)._
- Tehniline täiendus (lisatud event OnBeforeUpdateamountswithNDV protseduuri OnBeforePostGenJnlLine).
  
##### Versioon 16.0.22244.0
- Parandatud olukord, kus peažurnaalist käsitsi muudetud KM summat (nn KM erinevust) ei võetud mittemahaarvatava KM arvutamisel arvesse.

##### Versioon 16.0.22225.0
- KMD INF-A peal on võimalik kasutada välise dokumendi numbrit müügiarve numbri asemel.
  
##### Versioon 16.0.22179.0
- Lisandus 5% käibemaksu tugi
  - KM väljavõtted (KMD seadistus) tabeli väljale "Lahtri nr." saab nüüd sisestada väärtuse 2¹, mis tähistab 5% KM puhul KMD vormi rea numbrit).
  - KMD XML faili loomisel lisatud loogika, et kui KMD luuakse aasta 2022 kuu 8 või hilisem perioodi kohta, siis lisatakse XML faili tag "transactions5".
  
##### Versioon 16.0.21320.2
- Lahendus ühilduvaks BC20-ga.
  
##### Versioon 16.0.21320.1
- Parandatud olukord, kus väga paljude (sajad tuhanded) KM kannete korral tekkis KMD loomise protsessi "Soovita ridu..." käigus viga "Arithmetic operation resulted in an overflow".
  
##### Versioon 16.0.21320.0
- Parandatud olukord, kus ei õnnestunud kasutada üle 10 märgiseid väärtusi väljadel "KM äri konteeringurühm" ning "KM toote konteeringurühm".
  
##### Versioon 16.0.21132.0
- Parandatud CONSISTENT viga, kui ostuarvel oli kombinatsioon PV + Mittemahaarvatav KM + Pöörd KM.
  
##### Versioon 16.0.21113.0
- parandatud olukord ostuarvel, kus mittemahaarvatava KM + periodiseerimise + arve kinnitamisele saatmise kombinatsiooni puhul muutus periodiseerimise graafik peale kinnituse saamist.
